# Etapa 6 Leitura e fichamento

## Solicitação

Preencha uma cópia deste template para cada artigo selecionado.

Os 10 fichamentos abaixo seguem a ordem da lista final da etapa de levantamento bibliográfico (Eixo 1: fundamentos e complexidade teórica; Eixo 2: análise empírica; Eixo 3: aplicação em recomendação).

---

# Fichamento 1 de 10

## Identificação do artigo

- Referência completa: DIJKSTRA, E. W. A note on two problems in connexion with graphs. Numerische Mathematik, v. 1, p. 269-271, 1959.
- DOI ou URL: https://doi.org/10.1007/BF01386390
- Base de origem: Busca retroativa nas referências dos artigos selecionados
- Leitor responsável: Eduardo Alves dos Reis
- Data da leitura: 07/10/2026

## Fichamento

### Problema investigado

Dois problemas em grafos com arestas de comprimento conhecido: construir a árvore de menor comprimento total que liga todos os nós, e encontrar o caminho de menor comprimento total entre dois nós dados.

### Objetivo do estudo

Apresentar procedimentos simples para resolver os dois problemas, que exijam pouca memória e poucos cálculos se comparados aos métodos conhecidos na época.

### Método utilizado

Descrição construtiva dos algoritmos. Para o caminho mínimo, os nós são divididos em três conjuntos: os que já têm distância mínima definida, os que são candidatos e os ainda não alcançados. A cada passo o candidato com menor distância é fixado e as distâncias dos seus vizinhos são atualizadas.

### Contexto, amostra ou dados

Trabalho teórico, sem experimentos nem conjunto de dados. Considera grafos com arestas de comprimento positivo.

### Principais resultados

O procedimento encontra o caminho mínimo de forma correta e só precisa guardar informação sobre um número de arestas proporcional ao número de nós, o que era vantagem frente aos métodos da época. É a origem do algoritmo de Dijkstra, cuja versão com vetor simples tem custo O(n²).

### Limitações apresentadas

O artigo não faz análise formal de complexidade com notação assintótica e não usa fila de prioridade. Também não trata pesos negativos.

### Contribuição para o nosso artigo

Serve como ponto de partida da fundamentação teórica: define o algoritmo que será analisado e mostra que a ideia central (fixar sempre o nó mais próximo) é a mesma em todas as versões posteriores, que só mudam a estrutura usada para escolher esse nó.

### Comentário crítico

Texto curto e direto, que se sustenta até hoje. Como não traz a análise de custo em notação O, a complexidade O(n²) e as versões com heap precisam ser buscadas em trabalhos posteriores, como Fredman e Tarjan (1987).

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.

---

# Fichamento 2 de 10

## Identificação do artigo

- Referência completa: FREDMAN, M. L.; TARJAN, R. E. Fibonacci heaps and their uses in improved network optimization algorithms. Journal of the ACM, v. 34, n. 3, p. 596-615, 1987.
- DOI ou URL: https://doi.org/10.1145/28869.28874
- Base de origem: Busca retroativa nas referências dos artigos selecionados
- Leitor responsável: Eduardo Alves dos Reis
- Data da leitura: 09/10/2026

## Fichamento

### Problema investigado

O custo dos algoritmos de otimização em redes, como o Dijkstra, depende das operações da fila de prioridade. Com os heaps comuns, a operação de diminuir chave (decrease-key) pesa no tempo total.

### Objetivo do estudo

Propor uma nova estrutura de heap, o heap de Fibonacci, e mostrar como ela melhora o limite de tempo de vários algoritmos de grafos.

### Método utilizado

Projeto da estrutura e análise amortizada das operações. Depois, os autores aplicam o heap a algoritmos conhecidos e recalculam suas complexidades.

### Contexto, amostra ou dados

Trabalho teórico, sem experimentos. Os problemas analisados incluem caminho mínimo de origem única, todos os pares de caminhos mínimos, árvore geradora mínima e emparelhamento bipartido ponderado.

### Principais resultados

O heap de Fibonacci faz inserção, busca do mínimo e decrease-key em tempo amortizado O(1), e remoção do mínimo em O(log n) amortizado. Com isso o Dijkstra passa a rodar em O(m + n log n), o melhor limite conhecido para grafos com pesos reais não negativos até 2025.

### Limitações apresentadas

Os limites são amortizados, ou seja, valem para a sequência de operações e não para cada operação isolada. O artigo não avalia o desempenho prático da estrutura.

### Contribuição para o nosso artigo

É a referência para a complexidade O(m + n log n) do Dijkstra e mostra que a fila de prioridade é o que define o custo do algoritmo. Essa ideia é a base para discutir por que estruturas diferentes produzem tempos medidos diferentes.

### Comentário crítico

Resultado teórico muito forte, mas os estudos experimentais (Cherkassky et al., 1996; Fernandes et al., 2026) mostram que o heap de Fibonacci costuma perder na prática para estruturas mais simples, por causa das constantes altas e do pior uso de cache. É um bom exemplo de que o melhor limite assintótico nem sempre vira o menor tempo.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.

---

# Fichamento 3 de 10

## Identificação do artigo

- Referência completa: HAEUPLER, B.; HLADÍK, R.; ROZHOŇ, V.; TARJAN, R. E.; TĚTEK, J. Universal optimality of Dijkstra via beyond-worst-case heaps. In: IEEE Annual Symposium on Foundations of Computer Science (FOCS), 65., 2024, Chicago. Proceedings [...]. IEEE, 2024. p. 2099-2130.
- DOI ou URL: https://doi.org/10.1109/FOCS61266.2024.00125 (versão aberta: https://arxiv.org/abs/2311.11793)
- Base de origem: Busca retroativa nas referências dos artigos selecionados
- Leitor responsável: Daniel Vieira Santos
- Data da leitura: 06/10/2026

## Fichamento

### Problema investigado

A análise de pior caso diz pouco sobre o desempenho do Dijkstra em um grafo específico. Os autores perguntam se o Dijkstra é o melhor possível para cada grafo, e não só no pior caso geral.

### Objetivo do estudo

Mostrar que o Dijkstra, com uma fila de prioridade adequada, é universalmente ótimo para o problema de ordenar os vértices pela distância até a origem.

### Método utilizado

Prova de limites inferiores para o problema de ordenação por distância, em um modelo de tempo e em um modelo de comparações. Em seguida, criam um heap com a propriedade de working set (remover um item custa log do número de itens inseridos depois dele) e provam que o Dijkstra com esse heap atinge esses limites.

### Contexto, amostra ou dados

Trabalho teórico, sem experimentos. Vale para grafos com pesos escolhidos de forma adversarial.

### Principais resultados

Com o heap de working set, o Dijkstra é universalmente ótimo em tempo de execução para a ordenação por distância. Com pequenos acréscimos (busca antecipada em vértices gargalo), também fica ótimo em número de comparações.

### Limitações apresentadas

O resultado vale para o problema de ordenar os vértices por distância, não para calcular só as distâncias. Na versão básica, a otimalidade em comparações só vale a menos de um termo aditivo O(n). O modelo de comparações é considerado pelos próprios autores mais forte e menos realista que o modelo de tempo.

### Contribuição para o nosso artigo

Mostra que a estrutura da fila de prioridade e a forma do grafo mudam o custo real do Dijkstra, indo além do limite de pior caso. Ajuda a explicar por que dois grafos do mesmo tamanho podem ter tempos diferentes.

### Comentário crítico

Trabalho recente e de grande peso (premiado na FOCS 2024). É totalmente teórico, então não diz nada sobre constantes ou tempo de relógio. Combina com Duan et al. (2025): um mostra que o Dijkstra é ótimo para ordenar, o outro que não é ótimo para só calcular distâncias.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.

---

# Fichamento 4 de 10

## Identificação do artigo

- Referência completa: DUAN, R.; MAO, J.; MAO, X.; SHU, X.; YIN, L. Breaking the sorting barrier for directed single-source shortest paths. In: Annual ACM Symposium on Theory of Computing (STOC), 57., 2025, Praga. Proceedings [...]. New York: ACM, 2025. p. 36-44.
- DOI ou URL: https://doi.org/10.1145/3717823.3718179 (versão aberta: https://arxiv.org/abs/2504.17033)
- Base de origem: Busca retroativa nas referências dos artigos selecionados
- Leitor responsável: Daniel Vieira Santos
- Data da leitura: 08/10/2026

## Fichamento

### Problema investigado

O Dijkstra com heap de Fibonacci roda em O(m + n log n), e o termo n log n vem do fato de ele, na prática, ordenar os vértices por distância. Esse limite era visto como uma barreira de ordenação para grafos esparsos.

### Objetivo do estudo

Encontrar um algoritmo determinístico para caminho mínimo de origem única em grafos dirigidos com pesos reais não negativos que seja assintoticamente mais rápido que o Dijkstra em grafos esparsos.

### Método utilizado

Combina ideias do Dijkstra e do Bellman-Ford em uma estratégia de divisão e conquista. O algoritmo resolve recursivamente um subproblema de caminho mínimo limitado a partir de uma fronteira de vértices. Algumas rodadas de relaxação ao estilo Bellman-Ford reduzem essa fronteira a poucos vértices pivô, e assim evita ordenar todos os vértices.

### Contexto, amostra ou dados

Trabalho teórico, no modelo de comparação e adição, sem experimentos.

### Principais resultados

Algoritmo determinístico com tempo O(m log^(2/3) n), o primeiro a superar o limite do Dijkstra em grafos esparsos dirigidos nesse modelo. Isso mostra que o Dijkstra não é ótimo para calcular apenas as distâncias.

### Limitações apresentadas

O limite continua acima de linear. A análise supõe grau de entrada e saída constante (obtido por uma transformação do grafo) e trata empates de distância com uma ordem auxiliar. O resultado não cobre técnicas específicas para pesos inteiros.

### Contribuição para o nosso artigo

É o avanço teórico mais recente sobre o tema e mostra que o limite clássico do Dijkstra não é o fim da história. Junto com Castro et al. (2025), que implementaram esse algoritmo, forma o melhor exemplo da diferença entre ser mais rápido na notação O e ser mais rápido no relógio.

### Comentário crítico

Resultado de grande impacto (premiado na STOC 2025), mas o próprio desenho com recursão e parâmetros dependentes de log n já indica constantes altas. O artigo não avalia desempenho prático, então precisa ser lido junto com a avaliação experimental de Castro et al. (2025).

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.

---

# Fichamento 5 de 10

## Identificação do artigo

- Referência completa: CHERKASSKY, B. V.; GOLDBERG, A. V.; RADZIK, T. Shortest paths algorithms: theory and experimental evaluation. Mathematical Programming, v. 73, n. 2, p. 129-174, 1996.
- DOI ou URL: https://doi.org/10.1007/BF02592101
- Base de origem: Busca retroativa nas referências dos artigos selecionados
- Leitor responsável: Daniel Vieira Santos
- Data da leitura: 09/10/2026

## Fichamento

### Problema investigado

Existem muitos algoritmos e implementações de caminho mínimo com limites teóricos diferentes, mas pouca evidência sobre qual funciona melhor na prática e em que tipo de grafo.

### Objetivo do estudo

Revisar a teoria dos principais algoritmos de caminho mínimo de origem única e comparar experimentalmente suas implementações em diferentes famílias de grafos.

### Método utilizado

Implementação de diversos códigos, entre variantes do Bellman-Ford e do Dijkstra com filas de prioridade diferentes (heaps e estruturas de buckets), testados de forma padronizada em várias famílias de grafos geradas para isso.

### Contexto, amostra ou dados

Famílias de grafos sintéticos, como grades e grafos aleatórios, com variação de tamanho, densidade e faixa de pesos, incluindo instâncias pensadas para ser difíceis para certos algoritmos.

### Principais resultados

Nenhum código foi o melhor em todos os casos, e as implementações com os melhores limites teóricos nem sempre foram as mais rápidas. Variantes do Dijkstra com estruturas de buckets se mostraram muito robustas em grafos com pesos não negativos.

### Limitações apresentadas

Os resultados dependem das famílias de grafos e do hardware da época. Grafos reais de grande escala, como redes rodoviárias atuais, não estavam no conjunto testado.

### Contribuição para o nosso artigo

É o estudo clássico que confronta teoria e prática no caminho mínimo, exatamente a pergunta do nosso artigo. Também serve de modelo de método para a medição no Player2: variar o tamanho do grafo e comparar o tempo com o crescimento esperado.

### Comentário crítico

Trabalho amplo e muito citado. A conclusão de que buckets vencem heaps em pesos inteiros foi confirmada quase 30 anos depois por Fernandes et al. (2026), o que reforça a solidez do resultado. Por ser de 1996, os tempos absolutos não valem mais, só as tendências.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.

---

# Fichamento 6 de 10

## Identificação do artigo

- Referência completa: FERNANDES, A. C.; CASTRO, L.; CLEMENTINO, T.; FREITAS, R. de. Análise assintótica e empírica de filas de prioridade avançadas aplicadas ao Algoritmo de Dijkstra. In: Encontro de Teoria da Computação (ETC), 11., 2026, Gramado. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2026. p. 41-45.
- DOI ou URL: https://doi.org/10.5753/etc.2026.22057
- Base de origem: SBC OpenLib (string 3)
- Leitor responsável: Kevin dos Santos Vieira
- Data da leitura: 06/10/2026

## Fichamento

### Problema investigado

Apesar dos avanços teóricos recentes, o Dijkstra com fila de prioridade otimizada continua sendo a solução mais rápida na prática. Falta saber qual fila funciona melhor e por quê.

### Objetivo do estudo

Comparar teórica e empiricamente heaps e bucket queues no Dijkstra, explorando otimizações que vêm da monotonicidade do algoritmo e da limitação dos pesos.

### Método utilizado

Tabela comparando a complexidade teórica de cada estrutura, seguida de implementação em C++20 e medição do tempo médio de execução. Foram testados heap binário, heap de Fibonacci e bucket queues de 1 a 6 níveis, com e sem decrease-key.

### Contexto, amostra ou dados

Redes rodoviárias reais dos EUA do 9º DIMACS Implementation Challenge, grafos esparsos e dirigidos com pesos inteiros (peso máximo até 10^6), com até cerca de 2,6 × 10^7 vértices. Máquina com Intel Core i7-1165G7, 8 GB de RAM e Ubuntu 24.04.3.

### Principais resultados

As bucket queues foram mais rápidas que os heaps nas instâncias testadas, e a de 1 nível com decrease-key foi a mais rápida, ao contrário do que a análise assintótica indicaria. Os autores atribuem isso à estrutura mais simples, à melhor localidade de cache e ao custo O(1) de inserção e decrease-key. Mais níveis nem sempre trouxeram ganho.

### Limitações apresentadas

Uma única família de grafos e uma única máquina. O consumo de memória não foi medido. Para pesos muito grandes, varrer muitos buckets pode ficar mais caro.

### Contribuição para o nosso artigo

É a evidência mais direta e recente de que a estrutura com pior limite teórico pode ser a mais rápida na prática. Ajuda a interpretar os tempos do Player2, porque a fila de prioridade usada lá (em Python) pesa no resultado tanto quanto o tamanho do grafo.

### Comentário crítico

Artigo curto, mas bem alinhado à nossa pergunta. O texto não traz os tempos em tabela, só em gráfico, o que dificulta citar números exatos. Como os pesos de afinidade do Player2 podem não ser inteiros, é preciso cuidado ao transferir a conclusão sobre bucket queues.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.

---

# Fichamento 7 de 10

## Identificação do artigo

- Referência completa: RIOS, M. L.; S. NETO, F. S.; NETTO, J. F. M. Análise e comparação dos algoritmos de Dijkstra e A-Estrela na descoberta de caminhos mínimos em mapas de grade. In: Encontro de Teoria da Computação (ETC), 1., 2016, Porto Alegre. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2016. p. 887-890.
- DOI ou URL: https://doi.org/10.5753/etc.2016.9852
- Base de origem: SBC OpenLib (string 3)
- Leitor responsável: Kevin dos Santos Vieira
- Data da leitura: 07/10/2026

## Fichamento

### Problema investigado

Qual de dois algoritmos, o Dijkstra (busca não informada) ou o A* (busca informada), encontra caminhos mínimos de forma mais eficiente em mapas de grade.

### Objetivo do estudo

Comparar o comportamento e a complexidade do Dijkstra e do A* em mapas de grade com custo uniforme.

### Método utilizado

Os dois algoritmos ganham uma condição de parada ao atingir o destino e uma função de reconstrução do caminho. O A* usa a distância de Manhattan como heurística. Os autores apresentam o pseudocódigo, a análise de complexidade e comparam a expansão de nós e o número de operações.

### Contexto, amostra ou dados

Mapas de grade com custo uniforme. O comportamento é ilustrado em uma grade 7×7, e o número de operações é comparado em grades de tamanhos diferentes, não especificados no texto.

### Principais resultados

O artigo indica O(E log V) para o Dijkstra e conclui que o A* resolve o problema de forma mais eficiente, com a diferença no número de operações aumentando conforme o mapa cresce.

### Limitações apresentadas

O artigo não lista limitações. Pela leitura, os resultados aparecem só em gráficos, sem valores numéricos, os tamanhos testados não são detalhados e não há informação de hardware ou implementação.

### Contribuição para o nosso artigo

Mostra uma análise de complexidade do Dijkstra feita em linguagem acessível e reforça que a estrutura do grafo e a existência de um destino fixo mudam o custo prático do algoritmo.

### Comentário crítico

Trabalho curto e mais didático. A análise atribui ao A* a complexidade O(V log V), o que só vale com uma heurística muito favorável, e a comparação com o Dijkstra é injusta quando este não usa heurística. Deve ser usado como apoio, não como evidência central.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.

---

# Fichamento 8 de 10

## Identificação do artigo

- Referência completa: SILVA E SILVA, L. G.; CARMONA CORTES, O. A. Paralelização do algoritmo de Dijkstra para grafos não direcionados de grande escala. Revista Eletrônica de Iniciação Científica em Computação, v. 24, n. 1, p. 162-170, 2026.
- DOI ou URL: https://doi.org/10.5753/reic.2026.7147
- Base de origem: SBC OpenLib (string 3)
- Leitor responsável: Kevin dos Santos Vieira
- Data da leitura: 08/10/2026

## Fichamento

### Problema investigado

O Dijkstra sequencial fica lento em grafos grandes, e não está claro quanto a paralelização ajuda em cada tecnologia.

### Objetivo do estudo

Comparar o Dijkstra sequencial com versões paralelas em OpenMP, MPI e CUDA, medindo tempo de execução, speedup e eficiência.

### Método utilizado

Versão ingênua do Dijkstra, com busca linear do vértice de menor distância (O(n²) no pior caso) e listas de adjacência. Cada configuração foi executada 30 vezes, com média, mediana, variância e desvio padrão. Speedup calculado como tempo sequencial dividido pelo paralelo.

### Contexto, amostra ou dados

Grafos não direcionados de 256 a 16.384 vértices. Máquina com Intel Core i5-9300H, 16 GB de RAM, GPU NVIDIA GTX 1650 e Windows 11.

### Principais resultados

Todas as versões paralelas foram mais rápidas que a sequencial. O sequencial levou em média cerca de 189 s com 16.384 vértices. O speedup máximo foi de 6,31 no OpenMP (8 threads), 6,64 no MPI (4 processos) e 37,8 na GPU com 16.384 vértices. Em grafos pequenos a GPU foi mais lenta ou quase igual ao sequencial.

### Limitações apresentadas

O MPI ficou sem memória nos maiores grafos. O tamanho de bloco na GPU foi fixo. Hardware e tempo limitados pelo contexto acadêmico.

### Contribuição para o nosso artigo

Traz medições de tempo do Dijkstra em tamanhos crescentes de grafo, com método estatístico (30 execuções) que pode ser copiado na medição do Player2. Também mostra que em grafos pequenos o custo fixo de uma técnica pode superar o ganho, algo esperado no Player2.

### Comentário crítico

Usa a versão O(n²) sem fila de prioridade, então não serve para discutir o efeito do heap. O artigo não explica como os grafos foram gerados, e alguns valores citados na conclusão não batem com as tabelas, o que pede cuidado ao citar números.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.

---

# Fichamento 9 de 10

## Identificação do artigo

- Referência completa: CASTRO, L.; CLEMENTINO, T.; DE FREITAS-RODRIGUES, R. Implementation and brief experimental analysis of the Duan et al. (2025) algorithm for single-source shortest paths. arXiv preprint arXiv:2511.03007, 2025. (preprint)
- DOI ou URL: https://arxiv.org/abs/2511.03007
- Base de origem: arXiv (string 1)
- Leitor responsável: Daniel Vieira Santos
- Data da leitura: 10/10/2026

## Fichamento

### Problema investigado

O algoritmo de Duan et al. (2025) tem o melhor limite assintótico conhecido, mas ninguém sabia se ele é mais rápido que o Dijkstra na prática.

### Objetivo do estudo

Implementar e avaliar experimentalmente o algoritmo de Duan et al. (2025) e compará-lo com o Dijkstra.

### Método utilizado

Implementação em C++20 de uma versão de pior caso e de uma variante com memória O(n), ambas comparadas ao Dijkstra. Ajuste de curvas aos tempos medidos para estimar a partir de que tamanho o novo algoritmo passaria a vencer.

### Contexto, amostra ou dados

Grafos aleatórios esparsos (até 2^25 vértices), grades (até cerca de 1,6 × 10^7 vértices) e redes rodoviárias dos EUA (até cerca de 2,3 × 10^7 vértices). Máquina com Intel Core i5-10400F, 32 GB de RAM e Linux Mint 21.3.

### Principais resultados

As implementações seguem os limites teóricos, mas o Dijkstra foi de 3 a 4 vezes mais rápido em todos os casos testados. Pela estimativa dos autores, a versão de pior caso só venceria o Dijkstra com mais de 10^67 vértices.

### Limitações apresentadas

As constantes altas impedem o uso prático do algoritmo. A estimativa do ponto de virada é muito sensível às constantes ajustadas. O próprio título define o estudo como uma análise breve.

### Contribuição para o nosso artigo

É o exemplo mais forte da diferença entre teoria e prática: um algoritmo assintoticamente melhor perde para o Dijkstra em qualquer tamanho de grafo realista. Responde diretamente à nossa pergunta de pesquisa.

### Comentário crítico

Resultado muito relevante, mas é preprint, sem revisão por pares, por isso entra só como apoio. O resumo fala em grafos de até 10 milhões de vértices, enquanto o texto testa até 2,3 × 10^7, uma inconsistência pequena que vale registrar.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.

---

# Fichamento 10 de 10

## Identificação do artigo

- Referência completa: DAI, J.; JIA, Z.; GAO, X.; CHEN, G. A hierarchical optimizer for recommendation system based on shortest path algorithm. arXiv preprint arXiv:1911.08994, 2019. (preprint)
- DOI ou URL: https://arxiv.org/abs/1911.08994
- Base de origem: arXiv, via Google Scholar (string 2)
- Leitor responsável: Kevin dos Santos Vieira
- Data da leitura: 10/10/2026

## Fichamento

### Problema investigado

Em redes geossociais, consultas que recomendam os k prestadores de serviço mais próximos por palavra-chave e localização costumam ser resolvidas com caminho mínimo, mas ordenar só pelo comprimento do caminho gera recomendações pouco convincentes.

### Objetivo do estudo

Propor um otimizador hierárquico que reordena os resultados do caminho mínimo usando características dos prestadores de serviço.

### Método utilizado

O caminho mínimo entre usuário e prestador gera a ordenação inicial. Depois, um classificador random forest atribui a cada prestador um nível de 1 a 5, e um otimizador por constante ajusta a nota pelo número de comentários para ordenar dentro de cada nível.

### Contexto, amostra ou dados

Base de dados do Yelp (mais de 6,5 milhões de avaliações), dividida em 80% para treino e 20% para teste.

### Principais resultados

O classificador teve 82% de acurácia. O artigo mostra um exemplo em que a ordem das recomendações muda após a otimização, sem comparação quantitativa com a ordenação só por caminho mínimo.

### Limitações apresentadas

O artigo não lista limitações. Pela leitura, ele não diz qual algoritmo de caminho mínimo usa, só reporta a acurácia do classificador e se apoia em um único exemplo.

### Contribuição para o nosso artigo

Mostra que caminho mínimo em grafo ponderado é usado como base de sistemas de recomendação, que é o papel do Dijkstra no Player2.

### Comentário crítico

Apoio fraco: é preprint, o grafo é geossocial e não de afinidade entre usuários, e não há análise de complexidade nem de tempo. Vale procurar um trabalho revisado por pares que trate recomendação por afinidade em grafo para fortalecer esse eixo.

## Checklist

- [x] O artigo foi lido além do resumo.
- [x] O método e os resultados foram identificados.
- [x] As limitações foram registradas.
- [x] A conexão com o tema foi explicada.
