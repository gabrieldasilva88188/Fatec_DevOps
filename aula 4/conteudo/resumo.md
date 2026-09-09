# Resumo da Aula 04 – Ferramentas de Integração e Entrega Contínua

---

## 1. DevOps e o Ciclo do Desenvolvimento Moderno
- **Cultura e Filosofia DevOps:** Integração contínua entre as equipes de Desenvolvimento (DEV) e Operações (OPS) para eliminar silos, reduzir falhas e acelerar entregas com qualidade.
- **Etapas do Ciclo Infinito:**
  - **Plan (Planejamento):** Definição de tarefas e prioridades em metodologias ágeis (ex.: Jira, Trello, Azure Boards).
  - **Code (Codificação):** Escrita colaborativa e versionamento do código-fonte com foco em boas práticas e documentação.
  - **Build (Compilação):** Transformação do código em artefatos executáveis (JAR, imagens Docker, pacotes NPM) com automação e verificação estática de código (SonarQube).
  - **Test (Testes Automatizados):** Execução de testes de unidade, integração e performance para garantir que apenas *builds* confiáveis avancem.
  - **Release (Liberação):** Versionamento semântico (*Major.Minor.Patch*) e aplicação de *Quality Gates* para validação antes da produção.
  - **Deploy (Implantação):** Implantação rápida e automatizada no ambiente produtivo com suporte a *rollbacks* automáticos.
  - **Operate (Operação):** Manutenção da estabilidade e escalabilidade via infraestrutura como código (IaC), orquestração de containers (Kubernetes) e automação (Ansible).
  - **Monitor (Observabilidade):** Coleta e análise contínua de dados do sistema produtivo divididos em:
    - **Métricas:** CPU, memória, latência e taxa de erros.
    - **Logs:** Registros detalhados de eventos e exceções.
    - **Traces:** Rastreamento do caminho das requisições entre serviços.

---

## 2. Ferramentas e Ecossistema de CI/CD
- **Utilidade das Ferramentas:** Automação de tarefas repetitivas como compilação, execução de testes, análise de qualidade, controle de *releases* e publicação em múltiplos ambientes.
- **Plataformas de CI/CD Destacadas:** GitHub Actions, GitLab CI/CD, Jenkins, Azure DevOps, Argo CD, CircleCI, Bamboo, Spinnaker e TeamCity.
- **GitHub Actions:** Solução de automação integrada nativamente aos repositórios do GitHub, disparando *workflows* com base em eventos como `push`, `pull request` ou criação de *tags*.

---

## 3. Conceito de Pipelines de CI/CD
- **Definição de Pipeline:** Sequência automatizada de estágios que conduz o software de forma confiável do *commit* até o *deploy* em produção.
- **Garantia de Qualidade:** Pipelines aplicam validações constantes em tempo real para permitir feedback rápido aos desenvolvedores e entrega contínua sem intervenção manual.

---

## 4. Atividade Prática
- **Análise Comparativa de Plataformas:** Leitura e estudo do artigo *"Practical Comparison Between the CI/CD Platforms Azure DevOps and GitHub"* (Manolov, Gotseva, Hinov, 2025).
- **Entregável:** Mapeamento de todas as ferramentas citadas, realizando uma síntese comparativa de suas funcionalidades, vantagens, limitações e cenários adequados de uso.