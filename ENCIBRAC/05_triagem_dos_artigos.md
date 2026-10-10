# Etapa 5 Busca e triagem dos artigos

## Solicitação

Registre as buscas realizadas e justifique a inclusão ou exclusão de cada artigo.

## Registro das buscas

| Base | String usada | Data | Filtros | Resultados encontrados | Responsável |
|---|---|---|---|---:|---|
| IEEE Xplore / ACM Digital Library (busca acadêmica combinada, incluindo arXiv) | 1 | 12/09/2026 | Publicações de 2016 em diante; inglês; artigos de periódico e conferência, com preprints do arXiv aceitos só como apoio | 8 | Daniel Vieira Santos |
| Google Scholar / ACM Digital Library (busca acadêmica combinada) | 2 | 12/09/2026 | Publicações de 2016 em diante; inglês; somente resultados com texto completo disponível | 9 | Kevin dos Santos Vieira |
| Portal CAPES / SBC OpenLib (busca acadêmica combinada, termos em português) | 3 | 12/09/2026 | Publicações de 2016 em diante; português; anais de eventos e periódicos revisados por pares | 9 | Kevin dos Santos Vieira |
| Busca retroativa (snowballing) nas referências dos artigos selecionados | Não se aplica | 12/09/2026 | Obras seminais e consolidadas sobre a complexidade do Dijkstra, revisadas por pares e com DOI, sem limite de período | 5 | Eduardo Alves dos Reis |

## Resumo da triagem

- Total de resultados encontrados: 26 nas buscas por string, mais 5 por busca retroativa
- Duplicatas removidas: 3 na triagem inicial, mais 1 unificada na revisão de 19/09/2026 (duas versões do mesmo estudo do ETC 2026)
- Artigos avaliados por título e resumo: 23
- Artigos selecionados para leitura completa: 15
- Artigos incluídos no conjunto final: 10 (7 aprovados na leitura completa, menos 1 fora do escopo e 1 duplicata, mais 5 da busca retroativa)

## Decisões

| Artigo | Título e resumo | Texto completo | Motivo da exclusão ou inclusão |
|---|---|---|---|
| Fernandes et al. (2026), ETC | Incluir | Aprovar | Compara teórica e empiricamente heaps e bucket queues no Dijkstra, ligado diretamente à relação entre complexidade e tempo medido |
| Fernandes; Castro; de Freitas-Rodrigues (2026), ETC | Incluir | Excluir | Duplicata: versão do mesmo estudo acima. Nos anais publicados só consta a versão de p. 41-45 (DOI 10.5753/etc.2026.22057), que foi a mantida |
| Silva e Silva; Carmona Cortes (2026), REIC | Incluir | Aprovar | Mede tempo, speedup e eficiência do Dijkstra em grafos de tamanhos crescentes, com versões sequencial e paralelas |
| Rios; S. Neto; Netto (2016), ETC | Incluir | Aprovar | Analisa a complexidade do Dijkstra e compara com o A* em mapas de grade, unindo análise teórica e testes |
| Castro; Clementino; de Freitas-Rodrigues (2025), arXiv | Incluir | Aprovar | Mede na prática o algoritmo de Duan et al. (2025) contra o Dijkstra; entra como preprint de apoio |
| Dai et al. (2019), arXiv | Incluir | Aprovar | Usa caminho mínimo como base de recomendação em rede social; único trabalho do eixo de recomendação, entra como preprint de apoio |
| Chen et al. (2020) | Incluir | Excluir | Removido na revisão de 19/09/2026: trata de aprendizado semissupervisionado para recomendação, sem Dijkstra nem análise de complexidade |
| Dijkstra (1959) | Não se aplica (busca retroativa) | Aprovar | Artigo original do algoritmo, base obrigatória da fundamentação teórica |
| Fredman; Tarjan (1987) | Não se aplica (busca retroativa) | Aprovar | Introduz os heaps de Fibonacci e o limite O(m + n log n) do Dijkstra |
| Cherkassky; Goldberg; Radzik (1996) | Não se aplica (busca retroativa) | Aprovar | Avaliação teórica e experimental clássica de algoritmos de caminho mínimo, referência para comparar teoria e prática |
| Haeupler et al. (2024) | Não se aplica (busca retroativa) | Aprovar | Prova a otimalidade universal do Dijkstra com um heap de working set, resultado teórico recente central para o tema |
| Duan et al. (2025) | Não se aplica (busca retroativa) | Aprovar | Primeiro algoritmo a superar o limite O(m + n log n) do Dijkstra em grafos esparsos dirigidos |
| 8 trabalhos excluídos na 1ª filtragem (agrupados por motivo) | Excluir | Não se aplica | Fora do eixo do tema, como computação quântica aplicada a caminhos mínimos, roteamento em redes de pagamento do tipo blockchain e correspondência de malhas 3D, ou material não revisado por pares, como slides de aula e sites de visualização de algoritmos |
| 8 trabalhos excluídos na 2ª filtragem (agrupados por motivo) | Incluir | Excluir | Foco só teórico, com provas de limites assintóticos sem implementação nem testes práticos, ou aplicação em domínio distante do projeto, como redes ópticas e sistemas distribuídos de larga escala, sem contribuição para a comparação entre teoria e prática |

Observação: os cinco trabalhos da busca retroativa são anteriores a 2016 ou puramente teóricos. Eles entram pela exceção prevista nos critérios de inclusão para obras seminais e consolidadas sobre a complexidade do Dijkstra, e não pelo filtro de análise empírica aplicado na leitura completa.

## Produto da etapa

Conjunto definitivo de artigos e registro das decisões.

## Checklist

- [x] Todas as buscas possuem data e string.
- [x] As duplicatas foram removidas.
- [x] Os critérios foram aplicados igualmente.
- [x] Toda exclusão possui justificativa.
- [x] Os artigos finais estão diretamente ligados ao problema.
