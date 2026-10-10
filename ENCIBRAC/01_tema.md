# Etapa 1 Tema e delimitação

## Solicitação

Defina um tema específico, relevante e viável para o artigo de revisão bibliográfica.

## Identificação

- Grupo: 11
- Integrantes: Daniel Vieira Santos, Kevin dos Santos Vieira, Eduardo Alves dos Reis
- Data: 18/08/2026 (entrega inicial), revisado em 19/09/2026 após o parecer da orientadora

## Preenchimento

### Área geral

Complexidade de algoritmos em grafos, com foco em algoritmos de caminho mínimo e análise por notação assintótica.

### Tema delimitado

Análise da complexidade do algoritmo de Dijkstra a partir da literatura, comparando o crescimento teórico previsto pela notação assintótica com o desempenho medido na prática. Como estudo de caso complementar, o grupo usa o grafo de afinidade do Player2, aplicativo próprio que recomenda usuários com maior afinidade entre si.

### Do tema amplo ao específico

- Tema amplo: Complexidade de algoritmos em grafos
- Objeto estudado: O algoritmo de Dijkstra (caminho mínimo de origem única) e o efeito da fila de prioridade na sua complexidade
- Contexto ou aplicação: Grafos ponderados aplicados a recomendação por afinidade, tendo o Player2 como estudo de caso
- Aspecto que será analisado: A relação entre a complexidade assintótica teórica do Dijkstra e o tempo de execução medido conforme o grafo cresce
- O que ficará fora do estudo: Outros algoritmos de caminho mínimo como objeto principal (Bellman-Ford, A*, Floyd-Warshall aparecem só como comparação quando a literatura usar), o grafo de distância geográfica (descartado a pedido da orientadora), roteamento em redes de computadores e a qualidade das recomendações do Player2

### Justificativa

O Dijkstra é um dos algoritmos de grafos mais usados em sistemas reais, de roteamento a recomendação. A literatura recente mostra que a distância entre o limite teórico e o desempenho prático ainda é um assunto aberto: em 2025 surgiu um algoritmo assintoticamente mais rápido, mas o Dijkstra continua vencendo nos testes. Revisar esse debate ajuda a entender quando a notação O de fato prevê o tempo real, e o Player2 dá um caso concreto para discutir isso fora do ambiente puramente teórico.

### Viabilidade

- Há artigos científicos disponíveis? Sim. O levantamento chegou a 10 trabalhos, entre clássicos e publicações de 2016 a 2026.
- O tema pode ser estudado no prazo? Sim
- O grupo possui acesso às fontes necessárias? Sim

## Produto da etapa

Tema delimitado e justificativa.

## Checklist

- [x] O tema é específico.
- [x] O tema é relevante.
- [x] O tema é viável.
- [x] O recorte está claro.
- [x] O tema foi validado pelo professor.

## Contribuições

| Integrante | Atividade realizada |
|---|---|
| Daniel Vieira Santos | Pesquisou semelhanças do tema com projetos passados e enviou o documento ao repositório do grupo (commit f463e7e) |
| Kevin dos Santos Vieira | Pesquisou artigos e validou as informações usadas na delimitação e na justificativa |
| Eduardo Alves dos Reis | Preencheu a documentação da etapa |
