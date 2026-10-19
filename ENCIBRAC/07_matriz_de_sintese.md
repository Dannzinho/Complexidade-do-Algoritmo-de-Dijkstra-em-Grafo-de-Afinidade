# Etapa 7 Matriz de síntese e organização da revisão

## Solicitação

Compare os artigos e organize a revisão por temas ou eixos. Não produza apenas uma sequência de resumos.

## Eixos da revisão

1. Fundamentos teóricos: o papel da fila de prioridade
2. Análise empírica: o limite assintótico frente ao tempo medido
3. Caminho mínimo em sistemas de recomendação

## Matriz de síntese

| Eixo | Artigos relacionados | Convergências | Divergências | Limitações | Lacunas |
|---|---|---|---|---|---|
| 1. Fundamentos teóricos | Dijkstra (1959); Fredman e Tarjan (1987); Haeupler et al. (2024); Duan et al. (2025) | O custo do Dijkstra depende da estrutura que escolhe o próximo vértice: O(n²) com vetor simples e O(m + n log n) com heap de Fibonacci. | Haeupler et al. (2024) provam que o Dijkstra é ótimo para ordenar os vértices por distância; Duan et al. (2025) o superam no cálculo só das distâncias. Os resultados tratam de problemas diferentes, por isso não se contradizem. | Todos são teóricos e não medem tempo de execução. | Nenhum indica a partir de que tamanho de grafo as melhorias teóricas aparecem no tempo real. |
| 2. Análise empírica | Cherkassky et al. (1996); Fernandes et al. (2026); Castro et al. (2025, preprint); Silva e Silva e Carmona Cortes (2026); Rios et al. (2016) | A opção com melhor limite teórico nem sempre é a mais rápida: buckets venceram heaps (Cherkassky et al., 1996; Fernandes et al., 2026) e o Dijkstra foi de 3 a 4 vezes mais rápido que o algoritmo de Duan et al. (Castro et al., 2025). | Os estudos usam grafos diferentes (sintéticos, redes rodoviárias, grades), versões diferentes do algoritmo e formas diferentes de medir, o que impede comparar os números entre si. | Uma única família de grafos e uma máquina (Fernandes et al., 2026); preprint (Castro et al., 2025); geração dos grafos não descrita (Silva e Silva; Carmona Cortes, 2026); resultados só em gráficos (Rios et al., 2016); hardware de 1996 (Cherkassky et al., 1996). | Nenhum estudo mede o Dijkstra em grafos de afinidade, e os dois que informam a linguagem usam C++. |
| 3. Recomendação | Dai et al. (2019, preprint) | Com um único trabalho, não há convergência interna; ele confirma que o caminho mínimo é usado como base de recomendação. | Dai et al. (2019) indicam que ordenar só pelo caminho mínimo gera recomendações fracas e reordenam a lista com um classificador. | Preprint; grafo geossocial, não de afinidade; não informa o algoritmo usado nem mede tempo. | Falta estudo sobre o desempenho do Dijkstra em grafos de afinidade entre usuários. |

## Roteiro da revisão da literatura

### Eixo 1

- Ideia principal: o custo do Dijkstra é definido pela fila de prioridade, e o limite clássico O(m + n log n) é ótimo para ordenar os vértices, mas não para calcular só as distâncias.
- Evidências que serão usadas: a ideia original e a versão O(n²) (Dijkstra, 1959); o heap de Fibonacci e o limite O(m + n log n) (Fredman; Tarjan, 1987); a otimalidade universal do Dijkstra (Haeupler et al., 2024); o algoritmo O(m log^(2/3) n) para grafos dirigidos esparsos (Duan et al., 2025).
- Comparação entre estudos: os dois primeiros criam o algoritmo e o seu limite clássico; os dois recentes vão além dele em direções diferentes, um provando a otimalidade para ordenar e o outro superando o limite no cálculo das distâncias.
- Ligação com o problema: define o crescimento previsto pela notação O, que é o termo de comparação da pergunta.

### Eixo 2

- Ideia principal: na prática, a melhor notação O não garante o menor tempo, porque constantes, uso da cache, faixa de pesos e tipo de grafo pesam no resultado.
- Evidências que serão usadas: buckets mais robustos que heaps (Cherkassky et al., 1996); bucket queue simples mais rápida em redes rodoviárias com até cerca de 26 milhões de vértices (Fernandes et al., 2026); Dijkstra de 3 a 4 vezes mais rápido que o algoritmo de Duan et al. (Castro et al., 2025); custo fixo da GPU em grafos pequenos (Silva e Silva; Carmona Cortes, 2026); efeito do destino fixo (Rios et al., 2016).
- Comparação entre estudos: Cherkassky et al. (1996) e Fernandes et al. (2026) chegam à mesma conclusão com quase 30 anos de diferença; Castro et al. (2025) estendem essa conclusão ao algoritmo mais recente; os outros dois servem como apoio.
- Ligação com o problema: responde à parte central da pergunta, mostrando como o tempo medido se afasta do previsto e por quê.

### Eixo 3

- Ideia principal: o caminho mínimo é usado em recomendação, mas o seu desempenho nesse uso não foi estudado nos trabalhos selecionados.
- Evidências que serão usadas: caminho mínimo como primeira ordenação de recomendações em rede geossocial, reordenada por um classificador com 82% de acurácia (Dai et al., 2019).
- Comparação entre estudos: ao contrário dos eixos 1 e 2, este trabalho não analisa complexidade nem tempo.
- Ligação com o problema: sustenta a motivação do artigo (o Player2) e mostra a lacuna a ser apontada nas considerações finais.

## Síntese crítica provisória

Os trabalhos convergem em um ponto: o custo do Dijkstra é decidido pela fila de prioridade, e a melhor notação O não garante o menor tempo. Na teoria, o limite O(m + n log n) de Fredman e Tarjan (1987) foi refinado por Haeupler et al. (2024) e superado por Duan et al. (2025). Na prática, estruturas com limites piores venceram os heaps (Cherkassky et al., 1996; Fernandes et al., 2026), e o algoritmo assintoticamente mais rápido perdeu para o Dijkstra em todos os testes (Castro et al., 2025). As divergências vêm de estudos feitos com grafos, versões e máquinas diferentes. Como lacuna, nenhum trabalho mede o Dijkstra em grafos de afinidade, e o eixo de recomendação depende de um único preprint.

## Checklist

- [x] Os artigos foram agrupados por ideias.
- [x] Há comparações entre estudos.
- [x] As divergências foram registradas.
- [x] As lacunas são específicas e sustentadas pelas leituras.

## Contribuições

| Integrante | Atividade realizada |
|---|---|
| Daniel Vieira Santos | Fez os fichamentos 3, 4, 5 e 9 (etapa 6), usados como base da matriz |
| Kevin dos Santos Vieira | Fez os fichamentos 6, 7, 8 e 10 (etapa 6), usados como base da matriz |
| Eduardo Alves dos Reis | Elaborou a matriz de síntese, a partir dos fichamentos da etapa 6, organizou os artigos em três eixos e revisou a síntese crítica |
