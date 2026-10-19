# Etapa 8 Redação do artigo

## Solicitação

Escreva a primeira versão completa do artigo seguindo a estrutura abaixo.

# Título

Complexidade assintótica e tempo medido do algoritmo de Dijkstra: uma revisão bibliográfica narrativa

## Palavras-chave

Algoritmo de Dijkstra; complexidade assintótica; fila de prioridade; análise empírica

## Introdução

O algoritmo de Dijkstra (1959) encontra os caminhos mais curtos de um vértice de origem até os demais vértices de um grafo com pesos não negativos. A cada passo, ele escolhe o vértice ainda não fixado com a menor distância provisória e atualiza a distância dos seus vizinhos. O algoritmo é usado tanto em redes rodoviárias (Fernandes et al., 2026) quanto em sistemas de recomendação baseados em grafos ponderados (Dai et al., 2019).

Para decidir como implementar um algoritmo, costuma-se usar a análise assintótica, expressa pela notação O. No caso do Dijkstra, o custo depende da fila de prioridade, a estrutura que escolhe o próximo vértice: com um vetor simples, o algoritmo custa O(n²); com o heap de Fibonacci, custa O(m + n log n), em que n é o número de vértices e m o número de arestas (Fredman; Tarjan, 1987). Estudos experimentais, porém, mostram que a opção com a melhor notação O nem sempre é a mais rápida na prática (Cherkassky et al., 1996; Fernandes et al., 2026; Castro et al., 2025). Surge, assim, o problema que orienta este trabalho: como o tempo de execução medido do algoritmo de Dijkstra se relaciona com o crescimento previsto pela análise assintótica à medida que o grafo cresce, e que fatores explicam as diferenças relatadas na literatura?

A pergunta tem motivação prática. O grupo desenvolve o Player2, aplicativo em Python que recomenda usuários por afinidade usando o Dijkstra sobre um grafo ponderado. O Player2 não é medido neste artigo: ele apenas motiva a investigação, que se apoia somente na literatura. Diante disso, este artigo tem como objetivo analisar, por meio de revisão bibliográfica narrativa, a relação entre a complexidade assintótica do algoritmo de Dijkstra e o seu tempo de execução medido, identificando os fatores que explicam as diferenças entre teoria e prática.

## Metodologia

Este trabalho é uma revisão bibliográfica narrativa, sem protocolo formal de revisão sistemática. A busca usou três strings, que combinam termos em português e inglês com os operadores AND e OR:

1. `("Dijkstra's algorithm" OR "shortest path algorithm") AND ("asymptotic complexity" OR "time complexity" OR "Big O notation")`, em IEEE Xplore e ACM Digital Library;
2. `("weighted graph" OR "graph theory") AND ("recommendation system" OR "affinity matching" OR "user matching")`, em Google Scholar e ACM Digital Library;
3. `("algoritmo de Dijkstra" OR "caminho mínimo") AND ("complexidade assintótica" OR "análise de algoritmos")`, no Portal de Periódicos CAPES, no Google Scholar e na SBC OpenLib.

Foram incluídos trabalhos publicados a partir de 2016, em português ou inglês, revisados por pares, com texto completo disponível e ligados à complexidade do caminho mínimo ou ao uso de grafos em recomendação. Obras seminais anteriores a 2016 foram aceitas como exceção, e preprints do arXiv entraram apenas como apoio. Foram excluídos duplicados, trabalhos fora do escopo, resumos sem texto completo e materiais não revisados por pares.

As buscas foram executadas em 12/09/2026, em ferramentas de busca acadêmica que cobrem as bases indicadas. O registro do grupo não separa os resultados por base: as strings 1, 2 e 3 trouxeram 8, 9 e 9 resultados, respectivamente, e esses 26 resultados foram triados. Após remover 3 duplicatas, 23 foram avaliados por título e resumo e 15 seguiram para a leitura completa, na qual também foram excluídos trabalhos só teóricos e aplicações distantes do tema, restando 7. Após o parecer da orientadora, um trabalho fora do escopo foi removido, duas versões do mesmo estudo foram unificadas e cinco obras seminais foram incluídas por busca nas referências dos trabalhos selecionados. O conjunto final tem 10 trabalhos, 8 revisados por pares e 2 preprints (Quadro 1). Cada trabalho foi lido na íntegra e fichado, e os fichamentos foram comparados em uma matriz de síntese organizada em três eixos.

**Quadro 1 — Trabalhos analisados, por eixo da revisão**

| Eixo | Trabalho | Natureza |
|---|---|---|
| 1. Fundamentos teóricos | Dijkstra (1959) | Teórico |
| 1. Fundamentos teóricos | Fredman e Tarjan (1987) | Teórico |
| 1. Fundamentos teóricos | Haeupler et al. (2024) | Teórico |
| 1. Fundamentos teóricos | Duan et al. (2025) | Teórico |
| 2. Análise empírica | Cherkassky et al. (1996) | Teórico e experimental |
| 2. Análise empírica | Fernandes et al. (2026) | Teórico e experimental |
| 2. Análise empírica | Rios et al. (2016) | Teórico e experimental |
| 2. Análise empírica | Silva e Silva e Carmona Cortes (2026) | Experimental |
| 2. Análise empírica | Castro et al. (2025) | Experimental (preprint) |
| 3. Recomendação | Dai et al. (2019) | Aplicado (preprint) |

Fonte: elaborado pelos autores (2026).

## Revisão da literatura

### Fundamentos teóricos: o papel da fila de prioridade

No artigo original, Dijkstra (1959) divide os vértices em três grupos: os que já têm a distância mínima definida, os candidatos e os ainda não alcançados. A cada passo, o candidato mais próximo é fixado. Implementada com um vetor simples, essa ideia custa O(n²). Todas as versões posteriores mantêm a mesma ideia e mudam apenas a estrutura usada para achar o candidato mais próximo.

Fredman e Tarjan (1987) mostram que essa estrutura define o custo do algoritmo. Com o heap de Fibonacci, que faz a inserção e a diminuição de chave em tempo constante amortizado, o Dijkstra passa a custar O(m + n log n). Esse foi o melhor limite conhecido para grafos dirigidos com pesos reais não negativos até 2025. O trabalho é teórico e não testa a estrutura na prática.

Dois trabalhos recentes reabriram o tema. Haeupler et al. (2024) provam que o Dijkstra, com um heap especial, é universalmente ótimo para ordenar os vértices pela distância: para cada grafo, nenhum algoritmo faz essa ordenação de forma significativamente mais rápida. Já Duan et al. (2025) apresentam um algoritmo O(m log^(2/3) n), mais rápido que o Dijkstra em teoria para grafos dirigidos esparsos, porque evita ordenar todos os vértices. Os dois resultados não se contradizem: um trata de ordenar os vértices, o outro de calcular apenas as distâncias. Como todos os trabalhos deste eixo são teóricos, nenhum diz se essas melhorias aparecem no tempo de execução real.

### Análise empírica: o limite assintótico frente ao tempo medido

Cherkassky et al. (1996) compararam diversas implementações de caminho mínimo em grafos sintéticos e concluíram que nenhuma foi a melhor em todos os casos e que as de melhor limite teórico nem sempre foram as mais rápidas. As versões do Dijkstra com buckets, estruturas que agrupam os vértices por faixa de distância, se mostraram muito robustas. Quase 30 anos depois, Fernandes et al. (2026) chegaram à mesma conclusão: em redes rodoviárias dos Estados Unidos com até cerca de 26 milhões de vértices, a bucket queue mais simples foi mais rápida que os heaps, embora o seu limite teórico seja pior. Os autores atribuem o resultado à estrutura mais simples, ao melhor uso da memória cache e às operações de custo constante.

Castro et al. (2025) testaram na prática o algoritmo de Duan et al. (2025). As implementações seguiram os limites teóricos, mas o Dijkstra foi de 3 a 4 vezes mais rápido em todos os casos testados. Pelos cálculos dos autores, o novo algoritmo só venceria em grafos com mais de 10^67 vértices. Como o trabalho ainda é um preprint, ele é usado aqui apenas como apoio.

Dois estudos completam o eixo. Silva e Silva e Carmona Cortes (2026) mostram que versões paralelas do Dijkstra foram mais rápidas que a sequencial, mas que, em grafos pequenos, o custo fixo da GPU anulou o ganho. Rios et al. (2016) mostram que, com um destino fixo, o A* examina menos vértices que o Dijkstra em mapas de grade. Os estudos do eixo usam grafos, versões do algoritmo e formas de medir diferentes, por isso os seus números não podem ser comparados diretamente, mas todos indicam que o tempo medido depende da implementação tanto quanto da notação O.

### Caminho mínimo em sistemas de recomendação

Dai et al. (2019) usam o caminho mínimo para gerar uma primeira lista de recomendações em uma rede geossocial e depois reordenam essa lista com um classificador, que teve 82% de acurácia. O trabalho confirma o uso do caminho mínimo em recomendação, mas não informa qual algoritmo usa, não mede tempo de execução e é um preprint. Entre os trabalhos selecionados, portanto, o uso do caminho mínimo em recomendação está documentado, mas o seu desempenho não.

### Síntese crítica

Os trabalhos convergem em um ponto: o custo do Dijkstra é decidido pela fila de prioridade, e a melhor notação O não garante o menor tempo. Na teoria, o limite O(m + n log n) foi refinado por Haeupler et al. (2024) e superado por Duan et al. (2025). Na prática, estruturas com limites piores, como as bucket queues, venceram os heaps (Cherkassky et al., 1996; Fernandes et al., 2026), e o algoritmo assintoticamente mais rápido perdeu para o Dijkstra (Castro et al., 2025).

Os próprios limites teóricos mostram quando a notação O deixa de decidir a escolha. Em grafos densos, em que m se aproxima de n², O(m + n log n) e O(n²) passam a ter a mesma ordem de crescimento (Dijkstra, 1959; Fredman; Tarjan, 1987), e a diferença entre as duas versões fica por conta das constantes de implementação, justamente o fator que os estudos experimentais apontam.

Há também lacunas. Nenhum dos trabalhos analisados mede o Dijkstra em grafos de afinidade ou de recomendação, os dois estudos que informam a linguagem usam C++, e o eixo de recomendação depende de um único preprint.

## Considerações finais

Este artigo analisou a relação entre a complexidade assintótica do algoritmo de Dijkstra e o seu tempo de execução medido. Em resposta ao problema de pesquisa, a literatura indica que a notação O descreve bem a tendência de crescimento do custo, mas não basta para prever qual implementação será mais rápida nos tamanhos de grafo usados na prática. As diferenças são explicadas pela fila de prioridade e pelas suas constantes de implementação, pelo uso da memória cache, pela faixa dos pesos, pela estrutura do grafo e pelo tamanho da instância, já que, em grafos pequenos, custos fixos podem superar o ganho de uma técnica (Silva e Silva; Carmona Cortes, 2026).

Esta revisão tem limitações: é narrativa, as buscas foram feitas em uma única data e em poucas bases, metade dos trabalhos é apenas teórica e a principal evidência experimental sobre o algoritmo de Duan et al. (2025) ainda é um preprint.

Como trabalho futuro, propõe-se medir o Dijkstra em um grafo de afinidade real, como o do Player2, variando o número de vértices e de arestas, repetindo cada medição várias vezes e comparando a curva de tempo com a prevista pela notação O. Se o grafo for denso, vale comparar a versão com vetor simples e a versão com heap, já que os seus limites coincidem nesse caso. Também será preciso definir como a afinidade entre usuários vira peso de aresta, porque o Dijkstra só funciona com pesos não negativos e procura o caminho de menor soma.

## Resumo

A escolha da implementação do algoritmo de Dijkstra costuma se basear na análise assintótica. Este artigo analisa, por meio de revisão bibliográfica narrativa, a relação entre a complexidade assintótica do Dijkstra e o seu tempo de execução medido, identificando os fatores que explicam as diferenças entre teoria e prática. Foram analisados 10 trabalhos, entre obras seminais e publicações de 2016 a 2026, organizados em três eixos: fundamentos teóricos, análise empírica e aplicação em recomendação. Os estudos teóricos mostram que o custo do Dijkstra depende da fila de prioridade e que o limite clássico O(m + n log n) foi superado em 2025 em grafos dirigidos esparsos. Os estudos experimentais mostram que a opção com melhor limite nem sempre é a mais rápida: bucket queues venceram heaps, e o algoritmo assintoticamente mais rápido foi de 3 a 4 vezes mais lento que o Dijkstra. Conclui-se que a notação O descreve a tendência de crescimento do custo, mas não prevê sozinha o tempo medido. Nenhum dos trabalhos mede o Dijkstra em grafos de afinidade, lacuna que motiva estudos de caso futuros.

## Referências

CASTRO, L.; CLEMENTINO, T.; FREITAS, R. de. Implementation and brief experimental analysis of the Duan et al. (2025) algorithm for single-source shortest paths. arXiv, 2025. Preprint. Disponível em: https://arxiv.org/abs/2511.03007. Acesso em: 10 out. 2026.

CHERKASSKY, B. V.; GOLDBERG, A. V.; RADZIK, T. Shortest paths algorithms: theory and experimental evaluation. Mathematical Programming, v. 73, n. 2, p. 129-174, 1996. DOI: 10.1007/BF02592101.

DAI, J.; JIA, Z.; GAO, X.; CHEN, G. A hierarchical optimizer for recommendation system based on shortest path algorithm. arXiv, 2019. Preprint. Disponível em: https://arxiv.org/abs/1911.08994. Acesso em: 10 out. 2026.

DIJKSTRA, E. W. A note on two problems in connexion with graphs. Numerische Mathematik, v. 1, p. 269-271, 1959. DOI: 10.1007/BF01386390.

DUAN, R.; MAO, J.; MAO, X.; SHU, X.; YIN, L. Breaking the sorting barrier for directed single-source shortest paths. In: ANNUAL ACM SYMPOSIUM ON THEORY OF COMPUTING, 57., 2025, Praga. Proceedings [...]. New York: ACM, 2025. p. 36-44. DOI: 10.1145/3717823.3718179.

FERNANDES, A. C.; CASTRO, L.; CLEMENTINO, T.; FREITAS, R. de. Análise assintótica e empírica de filas de prioridade avançadas aplicadas ao Algoritmo de Dijkstra. In: ENCONTRO DE TEORIA DA COMPUTAÇÃO, 11., 2026, Gramado. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2026. p. 41-45. DOI: 10.5753/etc.2026.22057.

FREDMAN, M. L.; TARJAN, R. E. Fibonacci heaps and their uses in improved network optimization algorithms. Journal of the ACM, v. 34, n. 3, p. 596-615, 1987. DOI: 10.1145/28869.28874.

HAEUPLER, B.; HLADÍK, R.; ROZHOŇ, V.; TARJAN, R. E.; TĚTEK, J. Universal optimality of Dijkstra via beyond-worst-case heaps. In: IEEE ANNUAL SYMPOSIUM ON FOUNDATIONS OF COMPUTER SCIENCE, 65., 2024, Chicago. Proceedings [...]. [S. l.]: IEEE, 2024. p. 2099-2130. DOI: 10.1109/FOCS61266.2024.00125.

RIOS, M. L.; S. NETO, F. S.; MAGALHÃES NETTO, J. F. Análise e comparação dos algoritmos de Dijkstra e A-Estrela na descoberta de caminhos mínimos em mapas de grade. In: ENCONTRO DE TEORIA DA COMPUTAÇÃO, 1., 2016, Porto Alegre. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2016. p. 887-890. DOI: 10.5753/etc.2016.9852.

SILVA E SILVA, L. G.; CARMONA CORTES, O. A. Paralelização do algoritmo de Dijkstra para grafos não direcionados de grande escala. Revista Eletrônica de Iniciação Científica em Computação, v. 24, n. 1, p. 162-170, 2026. DOI: 10.5753/reic.2026.7147.

## Checklist

- [x] A introdução termina com o objetivo.
- [x] A metodologia descreve o processo realmente realizado.
- [x] A revisão compara os artigos.
- [x] A conclusão responde ao problema.
- [x] O resumo representa o texto completo.

## Contribuições

| Integrante | Atividade realizada |
|---|---|
| Daniel Vieira Santos | Fez a busca com a string 1 e os fichamentos 3, 4, 5 e 9, usados no artigo |
| Kevin dos Santos Vieira | Fez as buscas com as strings 2 e 3 e os fichamentos 6, 7, 8 e 10, usados no artigo |
| Eduardo Alves dos Reis | Redigiu o artigo, a partir da matriz de síntese e dos fichamentos, e revisou o texto final |
