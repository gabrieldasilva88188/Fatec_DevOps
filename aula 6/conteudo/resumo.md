# Resumo da Aula 06 – Revisão Ferramentas e Pipelines

**Disciplina:** DevOps / CI/CD  
**Professor:** Prof. Me. Deivison S. Takatu  

---

## 1. DevOps: O Ciclo Infinito do Desenvolvimento Moderno

DevOps é uma cultura e conjunto de práticas que integra as equipes de **Desenvolvimento (DEV)** e **Operações (OPS)**, eliminando silos organizacionais para acelerar entregas com qualidade e confiabilidade.

### As Etapas do Ciclo Infinito:
1. **PLAN (Planejamento):**
   - Definição do que, como e quando desenvolver utilizando metodologias ágeis (Sprints, Kanban, Roadmaps).
   - *Ferramentas:* Jira, Trello, Azure Boards.
2. **CODE (Codificação):**
   - Escrita, revisão e versionamento do código-fonte de forma colaborativa.
   - *Boas Práticas:* Código limpo, uso de IDEs adequadas, manter testes e documentação.
   - *Ferramentas:* Git, GitHub, GitLab.
3. **BUILD (Compilação e Build Automatizado):**
   - Transformação do código em artefato executável (`.jar`, imagem Docker, pacote NPM, binário).
   - *Passos:* Compilação, resolução de dependências, empacotamento, análise estática e publicação de artefatos.
   - *Ferramentas:* Gradle, Sonatype Nexus.
4. **TEST (Testes Automatizados e Qualidade):**
   - Execução automatizada de testes para detectar falhas antes de chegar ao usuário final (garante velocidade e segurança).
5. **RELEASE (Liberação e Controle de Versões):**
   - Aprovação e versionamento semântico (ex.: `v2.4.1` - Major.Minor.Patch).
   - Validação por *Quality Gates* (cobertura de testes, análise de segurança e aprovações).
   - *Ferramentas:* Jenkins, OpenStack.
6. **DEPLOY (Implantação Automatizada):**
   - Publicação automatizada em ambientes de produção com baixo risco e capacidade de *rollback* em caso de falha.
   - *Ferramentas:* AWS, Docker, Chef, Ansible.
7. **OPERATE (Operação e Gestão de Infraestrutura):**
   - Manutenção da estabilidade, disponibilidade e escalabilidade da aplicação (Gerenciamento de Infraestrutura como Código - IaC).
   - *Ferramentas:* Kubernetes, Ansible.
8. **MONITOR (Observabilidade e Monitoramento Contínuo):**
   - Coleta de dados reais em produção para fechar o ciclo e realimentar a fase de *PLAN*.
   - **Métricas:** Dados numéricos (CPU, memória, latência, taxa de erros).
   - **Logs:** Registros textuais de eventos e transações.
   - **Traces:** Rastreamento do caminho das requisições entre microsserviços.
   - *Ferramentas:* Grafana, Graylog.

---

## 2. Estrutura e Estágios da Pipeline

- **Conceito:** Sequência automatizada de estágios responsável por conduzir o software desde o commit até o deploy de forma confiável.
- **Regras Principais:**
  - **Build uma única vez:** O mesmo artefato é promovido entre ambientes (Dev $\rightarrow$ Homologação $\rightarrow$ Produção).
  - **Mesmo Deploy em Todos os Ambientes:** Mantém padronização e consistência.
  - **"Falhou? Para tudo!":** Se houver erro em qualquer fase, a pipeline é interrompida imediatamente.
- **Estágios Detalhados:**
  - *Build:* Compilação, verificação inicial e geração de artefatos.
  - *Testes:* Validação automática contínua.
  - *Qualidade:* Análise estática de padrões e conformidade.
  - *Segurança:* Análise de vulnerabilidades, dependências e dados sensíveis.
  - *Artefatos (Package):* Empacotamento, versionamento e armazenamento.
  - *Deploy:* Preparação de ambiente e publicação automatizada.
  - *Release & Monitoramento:* Liberação oficial e monitoramento de saúde em produção.

---

## 3. GitHub Actions e Automação

- **GitHub Actions:** Plataforma nativa do GitHub para automação de *workflows* acionados por gatilhos do repositório (`push`, `pull_request`, `tags`, `releases`).
- **GitHub Marketplace:** Catálogo de *Actions* e extensões prontas para automação de build, testes, segurança, deploy e cache.
- **Exemplo de Projeto:**  
  [github.com/deivisontakatu/projeto-pipelines-devops](https://github.com/deivisontakatu/projeto-pipelines-devops)

---

## 4. Atividade Prática Proposta

1. **Integração de Pipeline:** Configurar um *workflow* no GitHub Actions que execute automaticamente a cada `push` na branch principal (`main`).
2. **Análise de Repositórios:** Buscar e analisar pelo menos **3 repositórios no GitHub** que utilizem pipelines de CI/CD, destacando:
   - Características do projeto;
   - Funcionalidades da pipeline;
   - Gatilhos (*triggers*) utilizados;
   - Histórico de execuções e automações.