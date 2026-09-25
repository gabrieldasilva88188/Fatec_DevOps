# Resumo da Aula 07 — Testes Automatizados

## 1. Introdução aos Testes Automatizados

**Testes automatizados** são verificações executadas automaticamente por ferramentas para validar o comportamento esperado de uma aplicação.

Eles permitem:
- Verificar funcionalidades sem depender da execução manual de cada cenário.
- Executar validações durante o desenvolvimento.
- Integrar os testes às pipelines de Integração Contínua (CI).
- Identificar possíveis falhas automaticamente após alterações no código.

### Por que automatizar os testes?

- **Reduzir erros humanos:** diminui a dependência de verificações manuais e repetitivas.
- **Aumentar a velocidade:** executa diversas verificações em poucos segundos ou minutos.
- **Identificar falhas rapidamente:** detecta problemas logo após uma alteração no código.
- **Garantir consistência:** executa os mesmos cenários de teste sempre que necessário.
- **Aumentar a confiabilidade:** verifica continuamente se as funcionalidades existentes continuam funcionando.

---

## 2. Pipeline de Testes

Uma **pipeline** é uma sequência de validações automatizadas executadas durante o ciclo de entrega do software.

Princípios apresentados na aula:

- **Build uma única vez.**
- O mesmo artefato é promovido entre os ambientes.
- O mesmo deploy é utilizado nos diferentes ambientes.
- Fluxo: **Desenvolvimento → Homologação → Produção**.
- Se uma etapa falhar, o processo pode ser interrompido.
- Nenhuma etapa continua após um erro.

### Exemplo de pipeline

Após um desenvolvedor alterar o código e enviá-lo ao GitHub, a pipeline pode:

1. Baixar o código atualizado.
2. Compilar a aplicação.
3. Executar testes automáticos.
4. Verificar a qualidade do código.
5. Gerar uma nova versão da aplicação.
6. Publicar em ambiente de homologação.

### Pipeline de testes

Executa automaticamente validações no sistema após o processo de build.

Principais funções:
- Execução automática de testes.
- Validação contínua da aplicação.
- Identificação rápida de falhas.

### Pipeline de qualidade

Realiza verificações automatizadas para avaliar se o código atende aos padrões definidos antes de avançar para as próximas etapas.

O objetivo é identificar antecipadamente:
- Problemas de qualidade.
- Inconsistências.
- Possíveis falhas no código.

---

## 3. GitHub Actions Marketplace

O **GitHub Actions Marketplace** é um catálogo de Actions, ferramentas e extensões que podem ser utilizadas em workflows do GitHub Actions.

As soluções disponíveis podem auxiliar em etapas como:
- Build.
- Testes.
- Qualidade.
- Segurança.
- Deploy.
- Cache.

As Actions podem ser desenvolvidas pelo GitHub, por parceiros ou pela comunidade.

---

## 4. Situação-Problema: Cálculo de Descontos

A aula apresenta o exemplo de uma loja de roupas na qual os vendedores realizavam cálculos de descontos manualmente.

### Problemas

- **Erros humanos:** cálculos incorretos geravam divergências nos valores cobrados.
- **Inconsistência:** cada vendedor podia aplicar descontos de forma diferente.
- Retrabalho e perda de confiança no processo de vendas.

Foi desenvolvido um sistema web para calcular os descontos automaticamente, seguindo regras definidas pela empresa.

### Regras do exemplo

- Compras **abaixo de R$ 100** recebem **10% de desconto**.
- Compras **iguais ou superiores a R$ 100** recebem **5% de desconto**.

A automação busca reduzir falhas, agilizar o atendimento e eliminar a dependência de cálculos manuais.

---

## 5. Tipos de Testes

A aula apresenta três tipos principais de testes:

| Tipo | Objetivo |
|---|---|
| **Testes Unitários** | Validar funções e métodos de forma isolada. |
| **Testes de Integração** | Verificar a comunicação e o funcionamento conjunto entre módulos. |
| **Testes de Performance** | Avaliar velocidade e estabilidade sob carga. |

Os diferentes tipos de testes atuam em conjunto para verificar qualidade, confiabilidade, estabilidade e funcionamento correto do software.

---

## 6. Testes Unitários

Os **testes unitários** validam pequenas partes do sistema, como:

- Funções.
- Métodos.
- Componentes isolados do código.

Características:
- São rápidos.
- São automatizados.
- Podem identificar falhas durante o desenvolvimento.
- Facilitam a manutenção do software.
- Aumentam a confiabilidade das funcionalidades.
- Podem reduzir custos com correções futuras.

### Exemplo da aula

Se a regra de desconto esperada é de **10% ou 5%**, uma alteração para **15%** pode fazer o teste falhar, indicando que o comportamento da aplicação mudou em relação ao esperado.

**Ideia principal:** testar a lógica individual de uma pequena parte do sistema.

---

## 7. Testes de Integração

Os **testes de integração** verificam a comunicação e o funcionamento conjunto entre:

- Módulos.
- Serviços.
- APIs.
- Bancos de dados.

Eles identificam problemas que podem não aparecer quando cada componente é testado isoladamente.

Também ajudam a:
- Validar fluxos completos.
- Aumentar a estabilidade do sistema.
- Reduzir riscos de inconsistências em produção.

### Exemplo da aula

Se o texto de um botão for alterado para **“Calcular”**, um teste que procura o botão **“Calcular Desconto”** pode falhar durante a interação.

**Ideia principal:** verificar se diferentes partes do sistema funcionam corretamente juntas.

---

## 8. Testes de Performance

Os **testes de performance** avaliam o comportamento da aplicação em situações relacionadas a:

- Carga.
- Tempo de resposta.
- Consumo de recursos.

Eles permitem identificar:
- Gargalos.
- Lentidão.
- Falhas relacionadas ao desempenho.

Também ajudam a validar:
- Estabilidade.
- Escalabilidade.
- Experiência do usuário.
- Capacidade da aplicação de executar operações dentro do tempo esperado.

### Exemplo da aula

Se o tempo máximo esperado de resposta for alterado para **1 ms**, a aplicação pode não conseguir responder dentro do tempo configurado, causando a falha do teste.

**Ideia principal:** verificar se o sistema mantém um desempenho adequado sob determinadas condições.

---

## 9. Qualidade de Software

A **qualidade de software** representa a capacidade do sistema de atender:

- Requisitos.
- Necessidades do usuário.
- Objetivos do negócio.

Um software de qualidade deve apresentar:
- Confiabilidade.
- Estabilidade.
- Facilidade de manutenção.
- Capacidade de evolução ao longo do tempo.

No contexto de **DevOps**, a qualidade não é responsabilidade exclusiva dos testes. Ela passa a fazer parte de todo o ciclo de:

**Desenvolvimento → Entrega → Operação**

> “Qualidade deve fazer parte do processo.”

---

## 10. ESLint

O **ESLint** é uma ferramenta de **análise estática** utilizada para identificar problemas de:

- Padronização.
- Qualidade.
- Possíveis inconsistências em códigos JavaScript.

Em DevOps e Integração Contínua, o ESLint pode atuar como uma validação automatizada dentro da pipeline.

Ele auxilia no controle de qualidade e pode impedir a integração de códigos que não seguem os padrões definidos pelo projeto.

### Exemplo da aula

Ao adicionar:

`const x = 1;`

se a variável nunca for utilizada, o ESLint pode identificar o problema **no-unused-vars**.

---

## 11. O que acontece quando um teste falha?

Quando uma etapa da pipeline identifica um problema, o processo pode ser interrompido para evitar que uma versão inválida avance.

Principais consequências:

1. A alteração não avança para as próximas etapas.
2. A equipe recebe feedback sobre o problema.
3. O código pode ser corrigido antes da entrega.
4. Reduz-se o risco de levar uma versão com falhas para outro ambiente.

---

## 12. Conclusão

A adoção de práticas de **DevOps** e **Integração Contínua** permite tornar a aplicação mais confiável e preparada para mudanças constantes.

A automação de:
- Testes.
- Validações.
- Builds.

permite reduzir falhas, aumentar a qualidade das entregas e acelerar continuamente o desenvolvimento.

### Resumo dos principais conceitos

- **Testes Unitários:** garantia da lógica individual.
- **Testes de Integração:** validação da comunicação entre módulos.
- **Testes de Performance:** avaliação de carga, velocidade e estabilidade.
- **ESLint:** qualidade e padronização do código.
- **Pipeline:** sequência automatizada de validações e etapas de entrega.
- **GitHub Actions:** permite automatizar workflows e pipelines.

---

## 13. Atividade da Aula

Criar um novo projeto que integre os três tipos de testes automatizados:

1. Teste unitário.
2. Teste de integração.
3. Teste de performance.

Cada tipo de teste deve poder ser executado e analisado de forma independente.

Depois, criar uma **pipeline de Integração Contínua (CI)** utilizando um arquivo `.yml` no **GitHub Actions**, configurada para executar automaticamente a cada `push` na branch `main`.

A pipeline deve:

1. Instalar as dependências.
2. Executar os três tipos de testes.
3. Apresentar os resultados.

---

## 14. Referências apresentadas na aula

- HUMBLE, J.; PRIKLANDNICKI, R. *Entrega Contínua: Como Entregar Software de Forma Rápida e Confiável*. São Paulo: Bookman, 2013.
- MUNIZ, A. et al. *Jornada DevOps: Unindo Cultura Ágil, Lean e Tecnologia Para Entrega de Software Com Qualidade*. São Paulo: Brasport, 2019.
- SATO, D. *DevOps na prática: entrega de software confiável e automatizada*. São Paulo: Casa do Código, 2014.
- SILVA, R. *Entrega contínua em Android: Como automatizar a distribuição de apps*. São Paulo: Casa do Código, 2016.
- ARUNDEL, J.; DOMINGUS, J. *DevOps nativo de nuvem com Kubernetes*. São Paulo: Novatec, 2019.
- MORAES, G. *Caixa de Ferramentas DevOps: Um guia para construção, administração e arquitetura de sistemas modernos*. São Paulo: Casa do Código, 2015.
- PIRES, A.; MILITÃO, J. *Integração Contínua com Jenkins*. São Paulo: Casa do Código, 2019.
- VITALINO, J. F. N.; CASTRO, M. A. N. *Descomplicando o Docker*. 2. ed. São Paulo: Brasport, 2018.
- SILVERMAN, R. E. *Git: guia prático*. São Paulo: Novatec, 2019.
- KIM, G.; HUMBLE, J.; DEBOIS, P.; WILLIS, J. *Manual de DevOps: Como obter agilidade, confiabilidade e segurança em organizações tecnológicas*. São Paulo: Starlin Alta Editora, 2018.
