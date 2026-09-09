# Resumo da Aula 05 – Pipeline de Integração Contínua (CI)

**Disciplina:** DevOps / CI/CD  
**Professor:** Prof. Me. Deivison S. Takatu  

---

## 1. Introdução e Estrutura de Pipelines

- **O que é uma Pipeline?**
  - Sequência de validações e etapas automatizadas executadas durante todo o ciclo de entrega do software.
  - Conduz o código desde o commit até o deploy de forma rápida, previsível e confiável (*Humble & Priklandnicki, 2013; Sato, 2014*).
- **Regras e Boas Práticas do Pipeline:**
  1. **Build uma única vez:** O mesmo artefato gerado na etapa inicial é promovido entre os ambientes (Desenvolvimento  Homologação Produção).
  2. **Mesmo Deploy em Todos os Ambientes:** Mantém a consistência no processo de publicação.
  3. **"Falhou? Para Tudo!":** Se qualquer etapa/validação falhar, a execução do pipeline é interrompida imediatamente, impedindo o avanço de código defeituoso.

---

## 2. Etapas Principais do Pipeline de CI/CD

1. **Pipeline de Build (Compilação):**
   - Baixa o código atualizado e compila a aplicação.
   - Verifica a integridade inicial do código e gera os artefatos base (`.jar`, `.war`, `.apk`, containers Docker, etc.).
2. **Pipeline de Testes:**
   - Executa testes automatizados (unitários, integração, funcionais).
   - Identifica falhas rapidamente para garantir que novas alterações não quebrem recursos existentes.
3. **Pipeline de Qualidade:**
   - Realiza verificações automatizadas de padronização, conformidade e análise estática de código (ex.: SonarQube).
4. **Pipeline de Segurança:**
   - Analisa vulnerabilidades no código e em dependências/bibliotecas utilizadas.
   - Detecta configurações inseguras e exposição acidental de credenciais/informações sensíveis.
5. **Pipeline de Artefatos (Package):**
   - Empacota e versiona o software, armazenando os artefatos gerados em repositórios apropriados.
6. **Pipeline de Deploy:**
   - Prepara o ambiente de destino, configura variáveis/parâmetros e automatiza a publicação do artefato no ambiente de execução.
7. **Pipeline de Release e Monitoramento:**
   - Cria e controla a liberação oficial da versão para os usuários e monitora a saúde da aplicação em produção.

---

## 3. GitHub Actions e Marketplace

- **GitHub Actions:** Plataforma de automação nativa do GitHub para criar e executar *workflows* de CI/CD integrados ao repositório.
- **Gatilhos (Triggers):** Eventos que iniciam a execução automática da pipeline (ex.: `push`, `pull_request`, criação de `tags` ou `releases`).
- **GitHub Marketplace:** Catálogo de soluções, extensões e *Actions* reutilizáveis desenvolvidas pelo GitHub, parceiros ou pela comunidade para etapas de build, testes, segurança, cache e deploy.
- **Exemplo Prático disponibilizado pelo professor:**  
  [github.com/deivisontakatu/projeto-pipelines-devops](https://github.com/deivisontakatu/projeto-pipelines-devops)

---

## 4. Atividade Prática Proposta

1. Selecionar **3 Actions** disponíveis no *GitHub Marketplace*.
2. Desenvolver um projeto prático que utilize essas ferramentas em um fluxo automatizado, aplicando cada Action em uma etapa adequada da pipeline (ex.: setup de linguagem, linter/testes e deploy).
3. Configurar o arquivo de *workflow* no GitHub Actions, executar a pipeline e validar o funcionamento.
4. Documentar no projeto quais Actions foram utilizadas, suas funções e como contribuíram para a automação.