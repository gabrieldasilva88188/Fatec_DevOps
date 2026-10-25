# 📘 Fatec DevOps – Aula 9 | Atividade: Documentação de Projeto com README

![Disciplina](https://img.shields.io/badge/disciplina-DevOps-blue)
![Aula](https://img.shields.io/badge/aula-9-informational)
![Foco](https://img.shields.io/badge/foco-documenta%C3%A7%C3%A3o-green)
![Markdown](https://img.shields.io/badge/formato-Markdown-lightgrey?logo=markdown)

Repositório da **Atividade da Aula 9** da disciplina de **DevOps (Fatec)**. O objetivo foi **documentar um projeto de software real** por meio de um `README.md` completo, seguindo boas práticas de documentação em repositórios GitHub.

---

## 🔗 Projeto documentado

| | |
|---|---|
| **Projeto** | 🌱 **Green Hills – Estufa Automatizada Inteligente** (TCC do curso Técnico em Desenvolvimento de Sistemas – ETEC Fernando Prestes) |
| **Repositório** | 👉 **[github.com/gabrieldasilva88188/TCC-Green-Hills](https://github.com/gabrieldasilva88188/TCC-Green-Hills)** |
| **README entregue** | [README.md do Green Hills](https://github.com/gabrieldasilva88188/TCC-Green-Hills/blob/main/README.md) |

> O entregável desta atividade é o **README do repositório Green Hills**. Clique nos links acima para acessar o projeto e a documentação produzida.

---

## 📑 Sumário

1. [Enunciado da atividade](#1-enunciado-da-atividade)
2. [Sobre o projeto escolhido](#2-sobre-o-projeto-escolhido)
3. [O que foi feito](#3-o-que-foi-feito)
4. [Checklist de atendimento ao enunciado](#4-checklist-de-atendimento-ao-enunciado)
5. [Conteúdo do README entregue](#5-conteúdo-do-readme-entregue)
6. [Como visualizar o resultado](#6-como-visualizar-o-resultado)
7. [Competências trabalhadas](#7-competências-trabalhadas)
8. [Autor](#8-autor)

---

## 1. Enunciado da atividade

A atividade pedia que fosse escolhido um projeto de software e elaborada a sua documentação, contendo:

1. **Objetivo**, **problema** que pretende resolver, **escopo** e principais **requisitos funcionais e não funcionais**.
2. **Tecnologias** utilizadas, **arquitetura** da aplicação e **organização dos principais componentes**.
3. Criação ou atualização do **`README.md` no GitHub**, com **pré-requisitos**, **instruções de instalação, configuração e execução**.
4. Quando aplicável, documentação de **APIs**, **banco de dados**, **variáveis de ambiente** e **procedimentos de testes e deploy**.

---

## 2. Sobre o projeto escolhido

O **Green Hills** é uma solução de automação para estufas agrícolas que monitora e controla condições ambientais de forma remota. Sensores conectados a um **Arduino UNO** (temperatura, umidade do ar e umidade do solo) enviam leituras para uma aplicação web em **PHP + MySQL**, que exibe gráficos interativos, gera relatórios em PDF e controla o acesso por três níveis de usuário (`adminMaster`, `admin` e `comum`).

| Camada | Tecnologias |
|--------|-------------|
| Hardware | Arduino UNO R3, DHT11/DHT22, FC-28, bomba d'água, válvula solenoide, ventoinha |
| Front-end | HTML5, CSS3, JavaScript, Bootstrap 5 |
| Back-end | PHP 8.1, MySQL 8.0 |
| Bibliotecas | AnyChart (gráficos), TCPDF (PDF), Cleave.js (máscara de CPF) |

---

## 3. O que foi feito

- 📖 **Análise do código** do projeto (conexões com o banco, endpoint do Arduino, cadastro de usuários, vínculo de estufas e relatórios) para que a documentação refletisse o funcionamento real.
- 🧱 **Reestruturação do README** do Green Hills, que passou de uma descrição geral para uma documentação técnica completa.
- 🛠️ **Correção de problemas** do README anterior, como o bloco de código quebrado na seção de execução e referências a arquivos/pastas que não correspondiam ao repositório.
- 📐 **Diagramas em Mermaid** (arquitetura e modelo entidade-relacionamento), renderizados automaticamente pelo GitHub.
- ⚠️ **Mapeamento de limitações e melhorias futuras**, útil como roadmap do projeto.

---

## 4. Checklist de atendimento ao enunciado

| Item do enunciado | Atendido | Onde no README do Green Hills |
|-------------------|:--------:|-------------------------------|
| Objetivo | ✅ | [1. Visão geral](https://github.com/gabrieldasilva88188/TCC-Green-Hills#1-vis%C3%A3o-geral) |
| Problema a ser resolvido | ✅ | 1.2 Problema que resolve |
| Escopo | ✅ | 1.3 Escopo |
| Requisitos funcionais e não funcionais | ✅ | [2. Requisitos](https://github.com/gabrieldasilva88188/TCC-Green-Hills#2-requisitos) |
| Tecnologias utilizadas | ✅ | [3. Tecnologias utilizadas](https://github.com/gabrieldasilva88188/TCC-Green-Hills#3-tecnologias-utilizadas) |
| Arquitetura e organização dos componentes | ✅ | [4. Arquitetura](https://github.com/gabrieldasilva88188/TCC-Green-Hills#4-arquitetura) e [5. Estrutura do repositório](https://github.com/gabrieldasilva88188/TCC-Green-Hills#5-estrutura-do-reposit%C3%B3rio) |
| Pré-requisitos | ✅ | [6. Pré-requisitos](https://github.com/gabrieldasilva88188/TCC-Green-Hills#6-pr%C3%A9-requisitos) |
| Instalação, configuração e execução | ✅ | [7. Instalação, configuração e execução](https://github.com/gabrieldasilva88188/TCC-Green-Hills#7-instala%C3%A7%C3%A3o-configura%C3%A7%C3%A3o-e-execu%C3%A7%C3%A3o) |
| Variáveis de ambiente / configuração | ✅ | 8. Configuração (credenciais e parâmetros) |
| Banco de dados | ✅ | 9. Banco de dados |
| Documentação de APIs | ✅ | 10. Documentação da API e das rotas |
| Testes | ✅ | 12. Testes |
| Deploy | ✅ | 13. Deploy |

---

## 5. Conteúdo do README entregue

Resumo das seções presentes no README do Green Hills:

1. **Visão geral** – objetivo, problema e escopo.
2. **Requisitos** – 12 funcionais, 8 não funcionais e perfis de usuário.
3. **Tecnologias utilizadas** – hardware e software.
4. **Arquitetura** – diagrama do fluxo Arduino → servidor PHP → MySQL → relatórios.
5. **Estrutura do repositório** – árvore de pastas e arquivos.
6. **Pré-requisitos**.
7. **Instalação, configuração e execução** – XAMPP/WAMP, Docker (opcional) e gravação do firmware.
8. **Configuração** – credenciais e parâmetros de conexão.
9. **Banco de dados** – diagrama ER, tabelas e backup.
10. **API e rotas** – endpoint `salvar.php` e páginas da aplicação.
11. **Segurança**.
12. **Testes** – roteiro manual e checklist funcional.
13. **Deploy** – hospedagem e checklist de produção.
14. **Limitações conhecidas e melhorias futuras**.
15. **Equipe** e 16. **Licença**.

---

## 6. Como visualizar o resultado

1. Acesse o repositório do projeto: **[TCC-Green-Hills](https://github.com/gabrieldasilva88188/TCC-Green-Hills)**.
2. Role até a seção do README exibida na página inicial do repositório (os diagramas Mermaid são renderizados pelo próprio GitHub).
3. Para rodar o projeto localmente, siga a seção *Instalação, configuração e execução* do README, ou clone diretamente:

```bash
git clone https://github.com/gabrieldasilva88188/TCC-Green-Hills.git
```

---

## 7. Competências trabalhadas

- Escrita de documentação técnica em **Markdown**.
- Organização de um repositório no **GitHub** (README como porta de entrada do projeto).
- Levantamento de **requisitos funcionais e não funcionais**.
- Representação de **arquitetura** e **modelo de dados** com diagramas como código (Mermaid).
- Documentação de **instalação, configuração, testes e deploy**, práticas centrais da cultura **DevOps** para tornar um projeto reproduzível.
- Revisão crítica de código com identificação de **melhorias de segurança e manutenção**.

---

## 8. Autor

**Gabriel da Silva**
GitHub: [@gabrieldasilva88188](https://github.com/gabrieldasilva88188)

Projeto documentado desenvolvido em equipe como TCC (ETEC Fernando Prestes) por Felipe Ferreira de Souza, Gabriel da Silva, Giovanni Camargo Maruccio, João Henrique Pedroso Oliveira e Nikensley Pierre, com orientação de Claudio Roberto Corredato e Carlos Eduardo Alves de Oliveira.

---

*Atividade desenvolvida para fins acadêmicos – Fatec, disciplina de DevOps.* 🌿
