# Resumo de Aula: Documentação de Software

**Disciplina / Contexto:** DevOps / Engenharia de Software  
**Professor:** Prof. Me. Deivison S. Takatu  
**Instituição:** FATEC  

---

## Pergunta Provocativa Inicial
> *"Se eu entrar hoje no GitHub do seu projeto, consigo entender e executar o projeto sem perguntar nada para vocês?"*

A documentação tem como objetivo principal **reduzir a dependência de explicações informais**, permitindo que qualquer pessoa compreenda e execute o projeto de forma autônoma.

---

## O que acontece SEM Documentação?

A falta de documentação adequada gera gargalos críticos no ciclo de vida de um projeto de software:

* **Gargalos de Pessoas:** Dependência excessiva de desenvolvedores específicos e conhecimento perdido quando alguém deixa a equipe.
* **Onboarding Lento:** Dificuldade e demora para novos integrantes começarem a produzir.
* **Erros de Configuração:** Configurações esquecidas, divergentes entre ambientes ou executadas de formas inconsistentes.
* **Aumento de Custos:** Maior tempo gasto para manutenção, investigação e resolução de problemas (Troubleshooting).
* **Retrabalho:** Perguntas repetitivas sobre instalação, execução, testes e deploy.

---

## O que é Documentação de Software?

É o conjunto de informações organizadas que apoia as pessoas no ciclo completo do sistema: **compreender, utilizar, desenvolver, testar e manter**.

### Uma boa documentação responde:
1. O que é o projeto e para que serve?
2. Como instalar e configurar os pré-requisitos?
3. Como executar e testar o sistema?
4. Como contribuir e realizar mudanças no código?

### Os 4 Pilares da Documentação:
* **Comunicação:** Compartilhar conhecimento de forma assíncrona e transparente.
* **Manutenção:** Facilitar correções de bugs e evolução do sistema.
* **Colaboração:** Permitir o trabalho em equipe eficiente.
* **Continuidade:** Garantir a sustentabilidade do projeto independentemente das pessoas.

> *"Documentar não é apenas registrar, é tornar o conhecimento reutilizável."*

---

## Documentação e a Cultura DevOps

O **DevOps** integra pessoas, processos e tecnologia para entregar software continuamente. A documentação atua registrando:
* Como o código é desenvolvido e versionado.
* Como as alterações são validadas (testes e revisões).
* Como a pipeline de CI/CD funciona.
* Como o sistema é implantado (deploy) e monitorado.

### Quem consome a documentação?

| Papel | Necessidade / Utilização |
| :--- | :--- |
| **Desenvolvedor (Dev)** | Inicia o trabalho com menor dependência direta do time. |
| **Testador (QA)** | Identifica como executar o sistema e validar cenários de teste. |
| **Analista DevOps** | Configura pipelines de CI/CD, ambientes e processos de deploy. |
| **Gestor / PM** | Acompanha processos, decisões arquiteturais e escopo do projeto. |
| **Usuário / Cliente** | Aprende a utilizar as funcionalidades do produto final. |

---

## Conexão entre Áreas da Computação

 A documentação une múltiplos domínios da TI:

* **Engenharia de Software (ES):** Requisitos, arquitetura, código-fonte e testes.
* **Gestão de Projetos (GP):** Escopo, cronograma, riscos e entregas.
* **DevOps:** Integração e Entrega Contínua (CI/CD), infraestrutura, deploy e monitoramento.
* **Segurança da Informação:** Gestão de vulnerabilidades, políticas, controle de acessos e incidentes.
* **Qualidade de Software (QA):** Critérios de aceitação, baterias de testes e evidências.
* **Produto / UX:** Necessidades dos usuários, jornadas, regras de negócio e usabilidade.

---

## Tipos de Documentação

1. **Documentação Técnica:** Descreve a arquitetura, endpoints de APIs, modelagem de banco de dados, componentes e configurações do ambiente.
2. **Documentação de Projeto:** Registra objetivos de negócio, requisitos, decisões tomadas (ADRs) e organização das entregas.
3. **Documentação de Processo:** Detalha fluxos de trabalho como estratégia de branches (Git Flow), padrões de commits, Pull Requests, pipelines de CI/CD e procedimentos de deploy.

---

## O Arquivo README.md (Porta de Entrada)

O `README.md` é o primeiro documento consultado em um repositório no GitHub. Ele deve conter:

### Estrutura Essencial de um bom README:
1. **Descrição Geral:** Propósito e visão do projeto.
2. **Tecnologias e Pré-requisitos:** Stack utilizada, versões mínimas/recomendadas (ex: Node.js 18+, Docker, PostgreSQL 14).
3. **Instalação e Execução (Passo a Passo Reproduzível):**
   * Clonar repositório
   * Entrar no diretório
   * Instalar dependências
   * Configurar variáveis de ambiente
   * Executar a aplicação
   * Executar os testes
4. **Variáveis de Ambiente:** Descrição das chaves necessárias sem expor valores reais (ex: utilizar arquivo `.env.example`).
5. **Estrutura do Projeto:** Explicação sucinta sobre a organização de diretórios e responsabilidade das pastas principais (ex: `src/`, `tests/`, `docs/`, `.github/workflows/`).
6. **Procedimentos de Teste:** Comandos para testes unitários, integração ou performance.
7. **Guia de Contribuição e Links Úteis.**

---

## 🛑 O que NÃO colocar na Documentação (Segurança)

A segurança deve ser preservada em todos os documentos públicos ou compartilhados. **NUNCA inclua:**

❌ **Senhas e credenciais:** Senhas de acesso a bancos de dados, logins administrativos ou de usuários.  
❌ **Chaves de API e Tokens:** Segredos como chaves da AWS, tokens do Stripe, JWT secrets, etc.  
❌ **Dados Sensíveis / PII:** Informações pessoais de clientes, dados bancários ou bases de produção reais.  
❌ **Arquivos `.env` com dados reais:** Mantenha apenas arquivos de exemplo (`.env.example`).  
❌ **Detalhes Internos de Infraestrutura Restrita:** Informações detalhadas da rede privada que possam facilitar ataques cibernéticos.

---

## 🛠️ Atividade Prática Proposta

1. **Definição de Projeto:** Escolher um projeto de software, elaborar sua documentação apresentando objetivo, problema a resolver, escopo e requisitos funcionais/não-funcionais.
2. **Elaboração do `README.md`:** Criar ou atualizar o arquivo na raiz do repositório GitHub contendo:
   * Pré-requisitos e stack.
   * Instruções claras de instalação, configuração e execução.
   * Documentação de APIs, banco de dados e variáveis de ambiente (se aplicável).
   * Procedimentos para testes e deploy.

---

## 📖 Referências Bibliográficas Relevantes

* HUMBLE, J.; FARLEY, D. *Entrega Contínua: Como Entregar Software de Forma Rápida e Confiável*. Bookman, 2013.
* KIM, G.; HUMBLE, J.; DEBOIS, P.; WILLIS, J. *Manual de DevOps: Como obter agilidade, confiabilidade e segurança em organizações tecnológicas*. Alta Books, 2018.
* SATO, D. *DevOps na prática: entrega de software confiável e automatizada*. Casa do Código, 2014.
* MUNIZ, A. et al. *Jornada DevOps: Unindo Cultura Ágil, Lean e Tecnologia Para Entrega De Software Com Qualidade*. Brasport, 2019.
* VITALINO, J. F. N.; CASTRO, M. A. N. *Descomplicando o Docker*. Brasport, 2018.