# Resumo da Aula 02 – Conceitos de Integração e Entrega Contínua de Software

**Disciplina:** DevOps / CI/CD  
**Professor:** Prof. Me. Deivison S. Takatu  

---

## 1. O Problema de Entregar Software (Antes vs. Depois do DevOps)

- **Cenário Antigo (Antes do DevOps):**
  - Áreas de Desenvolvimento (DEV) e Operações/Infraestrutura (OPS) trabalhavam isoladas em silos.
  - Testes e deploys manuais, lentos, repetitivos e altamente propensos a erros humanos.
  - Atrasos na entrega, falhas recorrentes em produção, retrabalho e o famoso problema do *"funciona na minha máquina, mas dá erro no servidor"*.
- **Cenário Moderno (Com DevOps):**
  - Cultura, filosofia e conjunto de práticas que integram DEV e OPS.
  - Uso de **testes automatizados** rápidos, confiáveis e consistentes.
  - **Pipelines de CI/CD** para automação contínua.
  - Entregas rápidas, previsíveis e seguras: *entregar software não deveria ser arriscado*.

---

## 2. DevOps: O Ciclo Infinito do Desenvolvimento Moderno

O ciclo de vida DevOps é contínuo e dividido nas seguintes etapas:

1. **PLAN (Planejamento):** Definição do que será desenvolvido utilizando metodologias ágeis (Sprint, Kanban).
   - *Ferramentas:* Jira, Trello, Azure Boards.
2. **CODE (Codificação):** Escrita, revisão e versionamento do código-fonte de forma colaborativa.
   - *Boas Práticas:* Código limpo, uso de IDEs, manutenção de testes e documentação.
3. **BUILD (Compilação e Build Automatizado):** Transformação do código em artefato executável (JAR, pacote NPM, imagem Docker).
   - *Passos:* Compilação, resolução de dependências, empacotamento, análise estática de código (SonarQube) e publicação de artefato.
4. **TEST (Testes Automatizados e Qualidade):** Validação automatizada para detectar bugs precocemente (testes unitários, integração, e2e, segurança).
5. **RELEASE (Liberação e Controle de Versões):** Definição do número de versão (SemVer) e passagem por *Quality Gates* (portões de qualidade e aprovações).
6. **DEPLOY (Implantação Automatizada):** Publicação automatizada nos ambientes de produção em minutos e com suporte a *rollback* automatizado.
   - *Exemplo:* Kubernetes (EKS), Docker Registry (ECR) e *Rolling Updates*.
7. **OPERATE (Operação e Gestão de Infraestrutura):** Garantia de estabilidade, disponibilidade e escalabilidade com Infraestrutura como Código (IaC).
   - *Ferramentas:* Kubernetes, Ansible.
8. **MONITOR (Observabilidade e Monitoramento Contínuo):** Coleta de dados contínuos para realimentar o ciclo de planejamento.
   - **Métricas:** Dados numéricos (uso de CPU, memória, latência, taxa de erro).
   - **Logs:** Registros textuais de eventos e transações.
   - **Traces:** Rastreamento de requisições através de microserviços.

---

## 3. Pilares da Automação de Entregas

- **Integração Contínua (CI):** Prática de integrar alterações de código frequentemente no repositório compartilhado. Cada commit dispara build, testes e validações automáticas para detectar erros no início do ciclo.
- **Entrega Contínua (Continuous Delivery):** Automatiza a preparação do software para publicação. O artefato fica sempre pronto para ir para produção, dependendo apenas da decisão de negócio/aprovação.
- **Deploy Contínuo (Continuous Deployment):** A publicação em produção acontece de forma 100% automatizada assim que o código passa por todas as etapas e validações do pipeline.

---

## 4. Versionamento de Software e Versionamento Semântico (SemVer)

- **Versionamento:** Atribuição de identificadores únicos a versões do projeto para garantir rastreabilidade, auditoria e facilidade de reversão (*rollback*).
- **Versionamento Semântico (SemVer):** Padrão **MAJOR.MINOR.PATCH** (exemplo: `v2.4.1`):
  - **MAJOR (Ápice):** Alterações incompatíveis com versões anteriores (quebram a API/compatibilidade).
  - **MINOR (Incremento):** Adição de novas funcionalidades mantendo compatibilidade com versões anteriores.
  - **PATCH (Correção):** Correção de bugs (*bug fixes*) sem alterar a compatibilidade ou novas funcionalidades.
- **Tipos comuns de alteração:** *Bug Fix*, *New Feature*, *Feature Enhancement*, *Refactoring*, *Performance*, *Security Patch*, *Dependency Update*, *Adding Tests*.

---

## 5. Ferramentas e Práticas: Git, Tags e Deploy

- **Git:** Sistema de controle de versão distribuído criado por Linus Torvalds.
  - Configuração inicial: `git config --global user.name "<Nome>"` e `git config --global user.email "<Email>"`.
- **Tags no Git:**
  - Marcadores para identificar commits importantes no histórico (ex: releases `v1.0.0`).
  - *Tipos:* **Leve** (apenas ponteiro/nome) e **Anotada** (inclui autor, data e mensagem).
  - *Comandos principais:* `git tag <nome_da_tag>` e `git push origin <nome_da_tag>`.
- **Deploy & Vercel:**
  - **Deploy:** Processo de colocar a aplicação no ar para o usuário final.
  - **Vercel:** Plataforma de hospedagem simplificada com integração nativa com GitHub/GitLab, deploys automáticos a cada `push` e suporte a frameworks modernos (React, Next.js, Vue).

---

## 6. Atividade Prática Proposta

1. Configuração do Git e VS Code.
2. Criação de arquivos base (`index.html`, `style.css`, `script.js`).
3. Inicialização e publicação do repositório no GitHub.
4. Registro de alterações, criação de commits e adição de **tags de versão**.
5. Documentação do processo e envio da atividade.