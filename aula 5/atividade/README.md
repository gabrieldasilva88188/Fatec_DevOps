# Aula 5 — Atividade: Testes Automatizados e Integração Contínua (CI)

Atividade da disciplina de **DevOps (Fatec)** sobre testes automatizados e pipeline de
**Integração Contínua** com **GitHub Actions**.

[![CI](https://github.com/gabrieldasilva88188/atividade5-projeto-DevOpv/actions/workflows/ci.yml/badge.svg)](https://github.com/gabrieldasilva88188/atividade5-projeto-DevOpv/actions/workflows/ci.yml)

## 🔗 Repositório do projeto

O código completo da atividade está em um repositório separado:

**👉 [atividade5-projeto-DevOpv](https://github.com/gabrieldasilva88188/atividade5-projeto-DevOpv)**

```bash
git clone https://github.com/gabrieldasilva88188/atividade5-projeto-DevOpv.git
```

## 📋 Enunciado

1. Criar um projeto que integre **três tipos de testes automatizados**: unitário, integração e performance.
2. Organizar o projeto para que cada tipo de teste possa ser **executado e analisado de forma independente**.
3. Criar uma pipeline de CI em um arquivo `.yml` no **GitHub Actions**, executada automaticamente a **cada push na branch `main`**, que:
   - instale as dependências;
   - execute os três tipos de testes;
   - apresente os resultados.

## 🧪 O que foi desenvolvido

Uma API REST de tarefas (**Flask + SQLite**) usada como base para os testes.

| Tipo de teste | Ferramenta | O que valida | Resultado local |
|---|---|---|---|
| **Unitário** | pytest + pytest-cov | Validações e regras de negócio, com repositório simulado (sem banco) | 37 testes, 100% de cobertura (mínimo: 90%) |
| **Integração** | pytest | API HTTP + serviço + SQLite reais | 16 testes |
| **Performance** | Locust | Carga de 20 usuários contra o servidor real, com limites (SLOs) | P95 de 14 ms, 0% de falhas, ~140 req/s |

**Limites do teste de performance:** a pipeline falha se o P95 for maior que 500 ms,
se houver mais de 1% de falhas ou se a vazão ficar abaixo de 20 req/s.

## 🗂️ Estrutura do projeto

```
atividade5-projeto-DevOpv/
├── app/                          # Aplicação (validators, service, repository, api, server)
├── tests/
│   ├── unit/                     # Testes unitários
│   ├── integration/              # Testes de integração
│   └── performance/              # Testes de performance (Locust)
├── scripts/
│   ├── run_performance.py        # Sobe o servidor, roda o Locust e encerra
│   └── summarize_results.py      # Resumo em Markdown dos relatórios
├── .github/workflows/ci.yml      # Pipeline de CI
├── requirements.txt              # Dependências de execução
├── requirements-dev.txt          # + pytest, pytest-cov
└── requirements-perf.txt         # + locust
```

## ⚙️ Pipeline de CI

Arquivo: [`.github/workflows/ci.yml`](https://github.com/gabrieldasilva88188/atividade5-projeto-DevOpv/blob/main/.github/workflows/ci.yml)

Disparada em **push na `main`** (e manualmente via *workflow_dispatch*).

```
push na main
   ├── Testes unitários      ─┐
   ├── Testes de integração  ─┼─ (em paralelo)
   └── Testes de performance ─┘
                 │
          Resultado final (falha se qualquer etapa falhou)
```

Cada job instala suas dependências, executa os testes, publica uma **tabela de resultados**
na página *Summary* da execução e anexa os relatórios completos como *artifacts*
(JUnit, cobertura HTML, relatório HTML do Locust).

## ▶️ Como executar localmente

```bash
git clone https://github.com/gabrieldasilva88188/atividade5-projeto-DevOpv.git
cd atividade5-projeto-DevOpv

python -m venv .venv
source .venv/Scripts/activate        # Git Bash no Windows (Linux/Mac: source .venv/bin/activate)
pip install -r requirements-dev.txt -r requirements-perf.txt
```

Cada tipo de teste roda de forma independente:

```bash
python -m pytest tests/unit -m unit                  # unitários
python -m pytest tests/integration -m integration    # integração
python scripts/run_performance.py                    # performance
```

Relatórios gerados em `reports/unit/`, `reports/integration/` e `reports/performance/`.

## 🛠️ Tecnologias

Python 3.12 · Flask · SQLite · Waitress · pytest · pytest-cov · Locust · GitHub Actions

## 👤 Autor

**Gabriel da Silva** — [@gabrieldasilva88188](https://github.com/gabrieldasilva88188)
Fatec — DevOps, Aula 5
