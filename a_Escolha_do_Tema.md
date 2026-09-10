# Etapa (a) — Escolha do Tema

> **Como preencher:** este documento deve ser preenchido **em conjunto pelo grupo**, mas com registro individualizado da contribuição de cada integrante. Substitua os campos entre `[ ]` pelas informações do seu grupo. Não apague as instruções em itálico — elas ajudam na avaliação do orientador.

---

## 1. Identificação do Grupo

| Campo | Informação |
|---|---|
| Curso / Disciplina | Computabilidade e Complexidade de Algoritmos |
| Projeto de Pesquisa / IC | Aplicação e análise de complexidade do algoritmo de caminho mínimo em grafos de afinidade |
| Orientadora | Andrea Ono Sakai |
| Data de entrega desta etapa | 18/08/2026 |
| Integrantes do grupo | Daniel Vieira Santos | Kevin dos Santos Vieira | Eduardo Alves dos Reis |

---

## 2. Tema Escolhido

### 2.1 Área geral de interesse
*Qual grande área do conhecimento/disciplina motivou a escolha (ex.: complexidade dos algoritmos, classes de problemas P, NP, Algoritmos Gulosos, Programação Dinâmica, Divisão e conquista)?*

Complexidade de algoritmos em grafos, mais especificamente algoritmos de caminho mínimo (Dijkstra), usando notação assintótica para analisar o desempenho.

### 2.2 Tema delimitado (versão final)
*Escreva o tema já delimitado, de forma específica — não o tema amplo. Lembre-se: o tema deve ser enunciado em 1 a 2 frases, como um assunto (ainda não é uma pergunta de pesquisa, isso vem na etapa "c").*

> **Tema:** Aplicação e análise de complexidade do algoritmo de caminho mínimo em grafos (Dijkstra) no Player2, aplicativo de recomendação que sugere usuários com maior afinidade entre si. O foco é entender como o algoritmo se comporta à medida que o grafo de afinidade cresce, comparando o crescimento teórico previsto pela notação assintótica com o tempo de execução medido na prática.

### 2.3 Do amplo ao específico
*Mostre o raciocínio de delimitação — como vocês chegaram do tema amplo ao tema específico.*

| Tema amplo (ponto de partida) | Tema delimitado (ponto de chegada) |
|---|---|
| Complexidade de algoritmos em grafos | Aplicação e análise de complexidade do algoritmo de Dijkstra no Player2, sistema real do grupo, avaliando seu comportamento em um grafo de afinidade entre usuários |

---

## 3. Justificativa da Escolha

### 3.1 Relevância
*Por que esse tema é importante ou atual? Para quem ele importa (academia, mercado, sociedade)?*

Algoritmos de caminho mínimo em grafos, como o Dijkstra, são usados em uma quantidade enorme de sistemas reais, de aplicativos de recomendação a sistemas de geolocalização e roteamento. Entender a complexidade e o comportamento prático desse algoritmo é relevante tanto para a academia, servindo como validação empírica de conceitos de análise de algoritmos vistos na disciplina, quanto para o mercado, ajudando a decidir quando e como aplicar o algoritmo em sistemas com volumes e estruturas de dados distintos. O grupo já tem um sistema próprio onde esse algoritmo se aplica: o Player2, que usa Dijkstra para recomendar usuários com maior afinidade entre si, com base em um grafo cujas arestas são ponderadas conforme o grau de afinidade entre os usuários. Analisar esse algoritmo dentro de um sistema real e já em funcionamento aproxima a teoria vista em sala de um cenário concreto de aplicação.

### 3.2 Viabilidade
*O grupo avaliou se tem tempo, recursos, acesso a dados/fontes e domínio mínimo do assunto para desenvolver esse tema até o fim do projeto?*

| Critério | Avaliação (Sim/Parcial/Não) | Observação |
|---|---|---|
| Tempo disponível é suficiente | Sim | A implementação do Dijkstra já existe no Player2, o que reduz o trabalho a ajustes e à etapa de análise |
| Há acesso a fontes/dados necessários | Sim | Player2 já possui base de usuários e grafo de afinidade prontos para uso |
| O grupo já tem domínio mínimo do tema | Sim | O tema é abordado diretamente no tópico de grafos da disciplina e o grupo já implementou Dijkstra no Player2 |
| Recursos técnicos necessários estão disponíveis | Sim | O projeto já está desenvolvido (Python/Flet) |

### 3.3 Originalidade / Não-redundância
*O grupo verificou rapidamente (via um levantamento preliminar) se o tema já é excessivamente explorado ou se existe um ângulo próprio a ser explorado?*

O algoritmo de Dijkstra em si já é amplamente documentado na literatura, mas o ângulo próprio do grupo está em analisá-lo dentro de um sistema real e já implementado pelo próprio grupo, o Player2, em vez de partir de um cenário puramente teórico ou de dados sintéticos genéricos. Isso permite fazer uma análise empírica com dados e código reais.

---

## 4. Validação com o Orientador

| Campo | Informação |
|---|---|
| Data da conversa/validação | `[dd/mm/aaaa]` |
| Tema aprovado pelo orientador? | Sim, com ajustes |
| Observações ou ajustes solicitados pelo orientador | A orientadora pediu para o grupo focar em apenas um dos dois sistemas, em vez de comparar afinidade e distância geográfica ao mesmo tempo. O grupo optou por seguir apenas com o Player2 (grafo de afinidade) |

---

## 5. Contribuição Individual dos Integrantes

> **Importante:** cada integrante deve descrever, com suas próprias palavras, o que efetivamente fez nesta etapa. Contribuições genéricas como "ajudei em tudo" não serão aceitas. Use verbos de ação e seja específico (ex.: "pesquisei 5 temas candidatos e apresentei prós/contras ao grupo").

### Integrante 1 — Daniel Vieira Santos
- **O que fez nesta etapa:** Pesquisas e Associações com projetos passados
- **Tempo dedicado (aprox.):** 2h30min
- **Evidência da contribuição** 

### Integrante 2 — Kevin dos Santos Vieira
- **O que fez nesta etapa:** Pesquisas e validação das informações
- **Tempo dedicado (aprox.):** 2h30min
- **Evidência da contribuição:** 

### Integrante 3 — Eduardo Alves dos Reis
- **O que fez nesta etapa:** Preenchimento da documentação
- **Tempo dedicado (aprox.):** 1h30min
- **Evidência da contribuição:** 

### 5.1 Quadro-resumo de participação

| Integrante | Contribuição principal | % estimado de participação nesta etapa |
|---|---|---|
| Daniel Vieira Santos | Pesquisa referente a semelhanças do projeto com projetos passados | 35% |
| Kevin dos Santos Vieira | Pesquisa de artigos e validação das informações coletadas | 35% |
| Eduardo Alves dos Reis | Preenchimento da documentação | 30% |

*A soma das porcentagens deve ser igual a 100%. Divergências de percepção sobre a participação devem ser discutidas em grupo antes do envio — o orientador pode solicitar esclarecimentos individuais em caso de disparidade relevante.*

---

## 6. Checklist Final da Etapa

- [x] Tema delimitado e redigido em 1-2 frases
- [x] Justificativa de relevância escrita
- [x] Viabilidade avaliada pelo grupo
- [x] Verificação preliminar de originalidade realizada
- [x] Tema validado com o orientador
- [x] Contribuição individual de cada integrante registrada
- [x] Quadro-resumo de participação preenchido (soma = 100%)

---
