# Template de Definição de Objetivos da Pesquisa Científica
### Computabilidade e Complexidade de Algoritmos

> **Como usar este template:** respondam cada pergunta no espaço indicado por `> Resposta:`. Sigam o passo a passo e usem os exemplos apenas como referência de estrutura — o conteúdo deve ser sobre o tema do grupo.

---

## Identificação do Grupo

| Campo | Informação |
|---|---|
| Curso / Disciplina | Computabilidade e Complexidade de Algoritmos |
| Projeto de Pesquisa / IC | Aplicação e análise de complexidade do algoritmo de caminho mínimo em grafos de afinidade |
| Orientador(a) | Andrea Ono Sakai |
| Data de entrega desta etapa | 12/09/2026 |
| Integrantes do grupo | Daniel Vieira Santos, Kevin dos Santos Vieira, Eduardo Alves dos Reis |
| Tema (da etapa "a") | Aplicação e análise de complexidade do algoritmo de caminho mínimo em grafos (Dijkstra) no Player2, aplicativo de recomendação que sugere usuários com maior afinidade entre si. O foco é entender como o algoritmo se comporta à medida que o grafo de afinidade cresce, comparando o crescimento teórico previsto pela notação assintótica com o tempo de execução medido na prática. |

## PARTE 1 — DEFINIR O OBJETIVO GERAL

### 1.1 Tema específico do grupo

**Pergunta:** Qual foi o tema específico que o grupo definiu?

> Resposta: O grupo escolheu analisar a complexidade do algoritmo de Dijkstra aplicado a um grafo de afinidade entre usuários, usando como estudo de caso o Player2, aplicativo desenvolvido pelo próprio grupo que recomenda usuários com maior afinidade entre si.

### 1.2 Passo a passo para chegar ao objetivo geral

**Passo 1 — Delimitação do tema**
Delimitem o tema específico por área, tempo, espaço ou aplicação.

> Resposta: O tema foi delimitado por aplicação: em vez de estudar o Dijkstra de forma puramente teórica, o grupo restringiu a análise a um único sistema real e já desenvolvido, o Player2, e a um único tipo de grafo, o de afinidade entre usuários (a orientadora pediu para o grupo focar em apenas um cenário, então a comparação com um segundo sistema, baseado em distância geográfica, foi descartada).

**Passo 2 — Formulação da problemática**
Transformem o tema em uma pergunta que expresse o problema de pesquisa.

*Exemplo:* "Quais os principais impactos da árvore de decisão em IA para definir estratégias de marketing para segmentação de clientes?"

> Resposta: Como o tempo de execução do algoritmo de Dijkstra se comporta, na prática, em relação ao crescimento teórico previsto pela notação assintótica, quando aplicado a um grafo de afinidade entre usuários que aumenta de tamanho?

**Passo 3 — Transformar a pergunta em objetivo geral**
Reescrevam a pergunta como uma afirmação, usando um verbo no infinitivo.

*Exemplo:* "Analisar os principais impactos da árvore de decisão em IA para definir estratégias de marketing para segmentação de clientes."

> Resposta: Analisar a aplicação do algoritmo de Dijkstra em um grafo de afinidade entre usuários no sistema Player2, com o propósito de comparar o crescimento assintótico teórico com o tempo de execução medido empiricamente conforme o grafo aumenta de tamanho.

**Passo 4 — Ajustes finais**
Revisem o objetivo geral seguindo os critérios abaixo:

- [x] É claro, direto e mensurável?
- [x] Evitei verbos fracos como "estudar" ou "conhecer"?
- [x] Usei um verbo forte (explorar, analisar, investigar, compreender, avaliar, propor, desenvolver, aplicar, identificar)?

**Modelo genérico de referência:**
> "[Verbo no infinitivo] a aplicação de [conceito ou técnica] em [contexto específico], com o propósito de [finalidade principal]."

**Outros exemplos de objetivos gerais (referência):**
- Investigar o uso de árvores de decisão para prever exportações de vinho no Brasil, com base em dados da Embrapa entre 2000 e 2025.
- Analisar o impacto da classificação automática de vinhos finos e de mesa por meio de algoritmos de inteligência artificial, a fim de apoiar estratégias de exportação.
- Desenvolver um modelo computacional baseado em árvore binária de busca para otimizar a recomendação de rotas de ambulância em cenários urbanos.

### 1.3 Respostas finais da Parte 1

**1) Qual a problemática?**

> Resposta: Como o tempo de execução do algoritmo de Dijkstra se comporta, na prática, em relação ao crescimento teórico previsto pela notação assintótica, quando aplicado a um grafo de afinidade entre usuários que aumenta de tamanho?

**2) Qual o objetivo geral?**

> Resposta: Analisar a aplicação do algoritmo de Dijkstra em um grafo de afinidade entre usuários no sistema Player2, com o propósito de comparar o crescimento assintótico teórico com o tempo de execução medido empiricamente conforme o grafo aumenta de tamanho.

---

## PARTE 2 — DEFININDO OS OBJETIVOS ESPECÍFICOS

### 2.1 Objetivo geral pesquisado

Copiem aqui o objetivo geral definido na Parte 1 (deve conceituar os assuntos abordados no tema).

> Resposta: Analisar a aplicação do algoritmo de Dijkstra em um grafo de afinidade entre usuários no sistema Player2, com o propósito de comparar o crescimento assintótico teórico com o tempo de execução medido empiricamente conforme o grafo aumenta de tamanho.

### 2.2 Assuntos da pesquisa

Escrevam de 4 a 5 assuntos que serão abordados na pesquisa.

*Exemplo (para o tema de árvore de decisão em IA e marketing):*
- Conceituar árvore de decisão
- Conceituar inteligência artificial
- Quais são as estratégias de marketing para segmentação de clientes?
- Analisar a relação existente entre árvore de decisão e inteligência artificial
- Apresentar quais são os resultados das estratégias de marketing para segmentação de clientes sem e com IA

**Assuntos do grupo:**
1. Resposta: Conceituar o algoritmo de Dijkstra e sua complexidade assintótica
2. Resposta: Conceituar grafos ponderados e sua aplicação em sistemas de recomendação por afinidade
3. Resposta: Descrever como o Dijkstra foi implementado no grafo de afinidade do Player2
4. Resposta: Medir empiricamente o tempo de execução do algoritmo em diferentes tamanhos de grafo
5. Resposta: *(opcional)* Comparar os resultados empíricos obtidos com o crescimento teórico previsto pela notação assintótica

### 2.3 Estrutura básica do artigo

Definam a estrutura do artigo, incluindo introdução e considerações finais.

*Exemplo de estrutura:*
- Introdução
- Conceituar árvore de decisão
- Conceituar inteligência artificial
- Quais são as estratégias de marketing para segmentação de clientes
- Analisar a relação existente entre árvore de decisão e inteligência artificial
- Apresentar quais são os resultados das estratégias de marketing para segmentação de clientes sem e com IA
- Considerações finais

**Estrutura do grupo:**
- Introdução
- Resposta: Fundamentação teórica — o algoritmo de Dijkstra e a notação assintótica
- Resposta: Grafos de afinidade em sistemas de recomendação
- Resposta: Metodologia — implementação e ambiente de testes usados no Player2
- Resposta: Resultados — análise empírica do tempo de execução em diferentes tamanhos de grafo
- Considerações finais

### 2.4 Objetivos específicos classificados

Classifiquem os objetivos específicos em **Conceituais** e **Técnicos**.

*Exemplo:*
- **Objetivos Conceituais**
  - Conceituar árvore de decisão
  - Conceituar inteligência artificial
- **Objetivos Técnicos**
  - Quais são as estratégias de marketing para segmentação de clientes
  - Analisar a relação existente entre árvore de decisão e inteligência artificial
  - Apresentar quais são os resultados das estratégias de marketing para segmentação de clientes sem e com IA

**Objetivos específicos do grupo:**

- **Objetivos Conceituais**
  - Resposta: Conceituar o algoritmo de Dijkstra e sua complexidade assintótica (notação O)
  - Resposta: Conceituar grafos ponderados aplicados a sistemas de recomendação por afinidade

- **Objetivos Técnicos**
  - Resposta: Descrever a implementação do algoritmo de Dijkstra no grafo de afinidade do Player2
  - Resposta: Medir empiricamente o tempo de execução do algoritmo em diferentes tamanhos de grafo
  - Resposta: *(opcional)* Comparar os resultados obtidos empiricamente com o crescimento teórico previsto pela notação assintótica

---

## CHECKLIST FINAL DO GRUPO

- [x] O tema específico está delimitado (área, tempo, espaço ou aplicação)
- [x] A problemática está formulada como pergunta
- [x] O objetivo geral está no infinitivo, claro e mensurável
- [x] Foram listados de 4 a 5 assuntos do artigo
- [x] A estrutura do artigo foi definida (introdução, desenvolvimento, considerações finais)
- [x] Os objetivos específicos foram classificados em Conceituais e Técnicos
