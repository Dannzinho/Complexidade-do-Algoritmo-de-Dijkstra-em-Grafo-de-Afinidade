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
| Revisão após parecer da orientadora | 19/09/2026 |
| Integrantes do grupo | Daniel Vieira Santos, Kevin dos Santos Vieira, Eduardo Alves dos Reis |
| Tema (da etapa "a") | Aplicação e análise de complexidade do algoritmo de caminho mínimo em grafos (Dijkstra) no Player2, aplicativo de recomendação que sugere usuários com maior afinidade entre si. O foco é entender como o algoritmo se comporta à medida que o grafo de afinidade cresce, comparando o crescimento teórico previsto pela notação assintótica com o tempo de execução medido na prática. |

### O que é revisão da literatura e o que é medição no Player2

| Parte do trabalho | O que entra | De onde vem | Peso no trabalho |
|---|---|---|---|
| Revisão da literatura | Complexidade teórica do Dijkstra, papel da fila de prioridade, avanços recentes no problema do caminho mínimo e resultados de estudos que já mediram o algoritmo na prática | Os 10 artigos selecionados na etapa (b) e o fichamento | Base da pesquisa, atende ao que a disciplina pede |
| Medição no Player2 | Tempo de execução do Dijkstra do Player2 em grafos de afinidade de tamanhos crescentes | Experimento feito pelo próprio grupo | Complemento, estudo de caso que é comparado com a revisão |

A medição não substitui o fichamento. Ela só entra depois da revisão, para verificar se o comportamento observado no Player2 bate com o que os artigos descrevem. Nos objetivos abaixo, cada item está marcado como **[Revisão]** ou **[Medição no Player2]**.

## PARTE 1 — DEFINIR O OBJETIVO GERAL

### 1.1 Tema específico do grupo

**Pergunta:** Qual foi o tema específico que o grupo definiu?

> Resposta: O grupo escolheu analisar, a partir da literatura, a complexidade do algoritmo de Dijkstra aplicado a grafos ponderados, usando como estudo de caso complementar o grafo de afinidade do Player2, aplicativo desenvolvido pelo próprio grupo que recomenda usuários com maior afinidade entre si.

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

> Resposta: Analisar, por meio de revisão da literatura, a complexidade do algoritmo de Dijkstra e a relação entre seu crescimento assintótico teórico e seu desempenho prático, com o propósito de confrontar essas conclusões com o tempo de execução medido no grafo de afinidade do Player2 conforme o grafo aumenta de tamanho.

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

> Resposta: Analisar, por meio de revisão da literatura, a complexidade do algoritmo de Dijkstra e a relação entre seu crescimento assintótico teórico e seu desempenho prático, com o propósito de confrontar essas conclusões com o tempo de execução medido no grafo de afinidade do Player2 conforme o grafo aumenta de tamanho.

---

## PARTE 2 — DEFININDO OS OBJETIVOS ESPECÍFICOS

### 2.1 Objetivo geral pesquisado

Copiem aqui o objetivo geral definido na Parte 1 (deve conceituar os assuntos abordados no tema).

> Resposta: Analisar, por meio de revisão da literatura, a complexidade do algoritmo de Dijkstra e a relação entre seu crescimento assintótico teórico e seu desempenho prático, com o propósito de confrontar essas conclusões com o tempo de execução medido no grafo de afinidade do Player2 conforme o grafo aumenta de tamanho.

### 2.2 Assuntos da pesquisa

Escrevam de 4 a 5 assuntos que serão abordados na pesquisa.

*Exemplo (para o tema de árvore de decisão em IA e marketing):*
- Conceituar árvore de decisão
- Conceituar inteligência artificial
- Quais são as estratégias de marketing para segmentação de clientes?
- Analisar a relação existente entre árvore de decisão e inteligência artificial
- Apresentar quais são os resultados das estratégias de marketing para segmentação de clientes sem e com IA

**Assuntos do grupo:**
1. Resposta: **[Revisão]** Conceituar o algoritmo de Dijkstra e sua complexidade assintótica, incluindo o papel da fila de prioridade
2. Resposta: **[Revisão]** Levantar o que os estudos empíricos publicados mostram sobre a diferença entre a complexidade teórica e o tempo medido do Dijkstra
3. Resposta: **[Revisão]** Conceituar grafos ponderados e sua aplicação em sistemas de recomendação por afinidade
4. Resposta: **[Medição no Player2]** Descrever a implementação do Dijkstra no grafo de afinidade do Player2 e medir seu tempo de execução em diferentes tamanhos de grafo
5. Resposta: **[Medição no Player2]** Comparar os tempos medidos no Player2 com o crescimento teórico e com os resultados levantados na revisão

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
- Resposta: Revisão da literatura: o algoritmo de Dijkstra, a notação assintótica e as filas de prioridade
- Resposta: Revisão da literatura: estudos empíricos sobre o desempenho do Dijkstra
- Resposta: Revisão da literatura: grafos de afinidade em sistemas de recomendação
- Resposta: Estudo de caso (medição no Player2): implementação, ambiente de testes e tempos medidos
- Resposta: Discussão: comparação entre os tempos medidos no Player2 e o que a literatura aponta
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
  - Resposta: **[Revisão]** Conceituar o algoritmo de Dijkstra e sua complexidade assintótica (notação O), incluindo o impacto da fila de prioridade
  - Resposta: **[Revisão]** Conceituar grafos ponderados aplicados a sistemas de recomendação por afinidade
  - Resposta: **[Revisão]** Sintetizar o que os estudos empíricos publicados mostram sobre a relação entre complexidade teórica e tempo medido do Dijkstra

- **Objetivos Técnicos**
  - Resposta: **[Medição no Player2]** Descrever a implementação do algoritmo de Dijkstra no grafo de afinidade do Player2
  - Resposta: **[Medição no Player2]** Medir o tempo de execução do algoritmo em diferentes tamanhos de grafo
  - Resposta: **[Medição no Player2]** Comparar os tempos medidos com o crescimento teórico previsto pela notação assintótica e com os resultados levantados na revisão

---

## CHECKLIST FINAL DO GRUPO

- [x] O tema específico está delimitado (área, tempo, espaço ou aplicação)
- [x] A problemática está formulada como pergunta
- [x] O objetivo geral está no infinitivo, claro e mensurável
- [x] Foram listados de 4 a 5 assuntos do artigo
- [x] A estrutura do artigo foi definida (introdução, desenvolvimento, considerações finais)
- [x] Os objetivos específicos foram classificados em Conceituais e Técnicos
- [x] Está explícito o que é revisão da literatura e o que é medição no Player2
