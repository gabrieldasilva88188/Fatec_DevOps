# Resumo de Aula: Projeto Prático de DevOps

**Disciplina / Contexto:** Projeto Final de DevOps  
**Professor:** Prof. Me. Deivison S. Takatu  
**Instituição:** FATEC  

---

## Visão Geral e Objetivos do Projeto

O **Projeto Final de DevOps** consiste no desenvolvimento colaborativo de uma aplicação web em grupo para aplicar, de ponta a ponta, os conceitos e ferramentas estudados na disciplina.

### Objetivos Principais:
1. **Aplicar conceitos práticos de DevOps** no ciclo de vida de desenvolvimento de software.
2. **Desenvolver uma aplicação web funcional e integrada.**
3. **Automatizar** processos de teste, integração (CI) e deploy (CD).
4. **Padronizar ambientes** de desenvolvimento, testes e execução utilizando contêineres.
5. **Monitorar** a disponibilidade e saúde operacionais da aplicação.

---

## Requisitos e Arquitetura da Aplicação

O tema e as funcionalidades são definidos pelo próprio grupo, devendo responder a uma necessidade real ou problema identificável.

### Camadas da Arquitetura:
* **Front-end:** Interface com o usuário.
* **Back-end:** Camada de regras de negócio e APIs/endpoints.
* **Banco de Dados:** Persistência de dados.
* **Middleware (quando aplicável):** Camadas de integração, controle de acesso/autenticação e validação.

---

## Pilares Práticos do Projeto

### 1. Gestão de Código e Trabalho Colaborativo (Git & GitHub)
* **Repositório:** Código-fonte e documentação centralizados.
* **Estratégia de Branches:** Ramificações organizadas para novas *features* e correções de bugs.
* **Commits Semânticos:** Mensagens objetivas, organizadas e descritivas.
* **Pull Requests (PRs):** Padrão obrigatório para integração de alterações.
* **Code Review:** Revisão de código cruzada entre membros do time antes do *merge*.

---

### 2. Testes Automatizados
O projeto exige a implementação e execução automatizada de diferentes níveis de testes:
* **Testes Unitários:** Validação isolada de funções, componentes e regras de negócio.
* **Testes de Integração:** Validação da comunicação correta entre módulos e componentes (ex: Back-end com Banco de Dados).
* **Testes End-to-End (E2E):** Simulação dos principais fluxos de uso do ponto de vista do usuário final.
* **Testes de Performance:** Avaliação de métricas de latência, tolerância a carga e taxa de erros.

---

### 3. Integração Contínua (CI)
Automação via **GitHub Actions** (ou ferramenta equivalente pré-autorizada):
* Instalação automática de dependências.
* Checagem de sintaxe, formatação e qualidade de código (*linting*).
* Execução automática das baterias de testes a cada *Push* ou *Pull Request*.
* *Build* automatizado da aplicação para verificação de integridade.

---

### 4. Containerização e Padronização (Docker)
* **Dockerfiles:** Configuração de build para Back-end e Front-end (se aplicável).
* **Orquestração local:** Configuração de portas, redes virtuais e variáveis de ambiente (ex: `docker-compose`).
* **Instruções Limpas:** Documentação técnica contendo comandos diretos de construção (*build*) e execução dos contêineres.

---

### 5. Entrega Contínua e Deploy (CD)
* **Build e Push:** Construção e publicação automática de imagens Docker atualizadas.
* **Implantação Automatizada:** Deploy contínuo do sistema em ambiente público ou de demonstração.
* **Health Check:** Verificação automática pós-deploy para confirmar disponibilidade e versão implantada.

---

### 6. Observabilidade, Logs e Monitoramento
Garantia de saúde operacional do ambiente rodando:
* **Logs Centralizados:** Registro estruturado de eventos importantes e captura de exceções/erros.
* **Métricas Operacionais:** Acompanhamento de tempo de resposta, disponibilidade e status da aplicação.

---

### 7. Configuração e Segurança
Boas práticas de segurança em DevSecOps:
* **12-Factor App:** Separação estrita entre código-fonte e configurações de ambiente.
* **Gestão de Segredos:** Uso exclusivo de arquivos `.env` locais (disponibilizando apenas `.env.example` sem credenciais reais no repositório).
* **Proteção de Acessos:** Proteção rígida contra vazamento de senhas, chaves de API e tokens privados.
* **Análise de Vulnerabilidade:** Verificação automatizada de dependências na pipeline, quando viável.

---

## 📦 Entregáveis do Projeto

Para a avaliação final, o grupo deve entregar:

1. **Repositório GitHub:** Código-fonte completo, histórico de commits, branches e histórico de Pull Requests.
2. **Evidências de Teste:** Relatórios de execução dos testes automatizados.
3. **Pipeline CI/CD:** Arquivos de workflow configurados e rodando com sucesso.
4. **Artefatos Docker:** Dockerfiles e arquivos de composição totalmente funcionais.
5. **Documentação Técnica:** `README.md` detalhado com pré-requisitos, passo a passo de execução, arquitetura e variáveis de ambiente.
6. **Aplicação Publicada:** Link de acesso público ou ambiente demonstrativo 100% reproduzível.
7. **Apresentação Técnica:** Apresentação funcional demonstrando a arquitetura, pipeline e execução ao vivo.

---

## 🔗 Materiais de Apoio e Repositórios de Exemplo

O professor disponibilizou os seguintes repositórios no GitHub como referência técnica:

* **Atividade / Roteiro do Projeto:** [github.com/deivisontakatu/aula-devops/tree/main/Atividade](https://github.com/deivisontakatu/aula-devops/tree/main/Atividade)
* **Exemplo de Projeto DevOps:** [github.com/deivisontakatu/projeto-devops](https://github.com/deivisontakatu/projeto-devops)
* **Exemplo com Docker:** [github.com/deivisontakatu/projeto-docker](https://github.com/deivisontakatu/projeto-docker)
* **Exemplo com Kubernetes:** [github.com/deivisontakatu/projeto-kubernetes](https://github.com/deivisontakatu/projeto-kubernetes)
* **DevOps com GitHub Actions e Testes:** [github.com/deivisontakatu/projeto-devops-testes](https://github.com/deivisontakatu/projeto-devops-testes)
* **Gestão de Variáveis de Ambiente:** [github.com/deivisontakatu/projeto-variavel-ambiente](https://github.com/deivisontakatu/projeto-variavel-ambiente)

---

## 📚 Referências Bibliográficas

* ARUNDEL, J.; DOMINGUS, J. *DevOps nativo de nuvem com Kubernetes*. São Paulo: Novatec, 2019.
* HUMBLE, J.; FARLEY, D. *Entrega Contínua: Como Entregar Software de Forma Rápida e Confiável*. São Paulo: Bookman, 2013.
* KIM, G.; HUMBLE, J.; DEBOIS, P.; WILLIS, J. *Manual de DEVOPS: Como obter agilidade, confiabilidade e segurança em organizações tecnológicas*. São Paulo: Alta Books, 2018.
* MORAES, G. *Caixa de Ferramentas DevOps: Um guia para construção, administração e arquitetura de sistemas modernos*. São Paulo: Casa do Código, 2015.
* MUNIZ, A. et al. *Jornada Devops: Unindo Cultura Ágil, Lean e Tecnologia Para Entrega De Software Com Qualidade*. São Paulo: Brasport, 2019.
* PIRES, A.; MILITÃO, J. *Integração Contínua com Jenkins*. São Paulo: Casa do Código, 2019.
* SATO, D. *DevOps na prática: entrega de software confiável e automatizada*. São Paulo: Casa do Código, 2014.
* SILVA, R. *Entrega contínua em Android: Como automatizar a distribuição de apps*. São Paulo: Casa do Código, 2016.
* SILVERMAN, R. E. *Git: guia prático*. São Paulo: Novatec, 2019.
* VITALINO, J. F. N.; CASTRO, M. A. N. *Descomplicando o Docker*. 2. ed. São Paulo: Brasport, 2018.