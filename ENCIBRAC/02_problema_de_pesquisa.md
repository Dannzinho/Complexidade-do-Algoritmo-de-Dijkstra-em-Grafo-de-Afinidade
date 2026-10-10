# Etapa 2 Problema de pesquisa

## Solicitação

Transforme o tema em uma pergunta clara, específica e respondível por meio da literatura científica.

## Tema aprovado

Análise da complexidade do algoritmo de Dijkstra a partir da literatura, comparando o crescimento teórico previsto pela notação assintótica com o desempenho medido na prática. Como estudo de caso complementar, o grupo usa o grafo de afinidade do Player2, aplicativo próprio que recomenda usuários com maior afinidade entre si.

## Pergunta de pesquisa

Como o tempo de execução do algoritmo de Dijkstra se comporta, na prática, em relação ao crescimento teórico previsto pela notação assintótica, quando aplicado a um grafo de afinidade entre usuários que aumenta de tamanho?

## Verificação

- O que se deseja descobrir ou compreender? Se o tempo real do Dijkstra cresce do jeito que a notação assintótica prevê, e quais fatores (fila de prioridade, constantes, estrutura do grafo, hardware) explicam as diferenças.
- Qual é o objeto da pergunta? O algoritmo de Dijkstra e a sua complexidade de tempo.
- Qual é o contexto ou recorte? Grafos ponderados de tamanho crescente, com o grafo de afinidade entre usuários do Player2 como caso de aplicação.
- A pergunta pode ser respondida por artigos científicos? Sim. A parte central, a relação entre complexidade teórica e tempo medido, é tratada diretamente por estudos teóricos (Fredman e Tarjan, 1987; Haeupler et al., 2024; Duan et al., 2025) e por avaliações experimentais (Cherkassky et al., 1996; Fernandes et al., 2026; Castro et al., 2025). A medição no Player2 só ilustra e discute o que a literatura aponta.
- Por que essa pergunta é relevante? Porque a escolha de um algoritmo ou de uma estrutura de dados costuma ser feita só pela notação O. A literatura mostra casos em que a estrutura com melhor limite teórico perde na prática, e entender isso ajuda a tomar decisões melhores em sistemas reais.

## Produto da etapa

Pergunta de pesquisa aprovada.

## Checklist

- [x] Está escrita em forma de pergunta.
- [x] É clara e objetiva.
- [x] Está alinhada ao tema.
- [x] Pode ser respondida por revisão bibliográfica.
- [x] Não exige experimento que não será realizado.

## Contribuições

| Integrante | Atividade realizada |
|---|---|
| Kevin dos Santos Vieira | Formulou a versão de trabalho da pergunta de pesquisa e o quadro de conceitos-chave usado na busca |
| Daniel Vieira Santos | Transformou os conceitos da pergunta em strings de busca com operadores booleanos e registrou a versão final da pergunta e dos objetivos no repositório do grupo |
| Eduardo Alves dos Reis | Levantou os termos em português equivalentes aos conceitos da pergunta, usados na string 3, e verificou o acesso ao Portal de Periódicos CAPES para confirmar que a pergunta tinha fontes disponíveis |
