# Etapa (b) — Levantamento Bibliográfico

> **Como preencher:** este documento deve ser preenchido **em conjunto pelo grupo**, mas com registro individualizado da contribuição de cada integrante em cada passo. Substitua os campos entre `[ ]` pelas informações do seu grupo. Não apague as instruções em itálico — elas ajudam na avaliação do orientador.

---

## 1. Identificação do Grupo

| Campo | Informação |
|---|---|
| Curso / Disciplina | Computabilidade e Complexidade de Algoritmos |
| Projeto de Pesquisa / IC | Aplicação e análise de complexidade do algoritmo de caminho mínimo em grafos de afinidade |
| Orientador(a) | Andrea Ono Sakai |
| Data de entrega desta etapa | 12/09/2026 |
| Revisão após parecer da orientadora | 19/09/2026 |
| Integrantes do grupo | Daniel Vieira Santos, Kevin dos Santos Vieira, Eduardo Alves dos Reis |
| Tema (da etapa "a") | Aplicação e análise de complexidade do algoritmo de caminho mínimo em grafos (Dijkstra) no Player2, focado no grafo de afinidade entre usuários, comparando o crescimento teórico previsto pela notação assintótica com o tempo de execução medido na prática. |

> **Papel deste levantamento no trabalho:** os artigos listados aqui formam a revisão da literatura, que é a base da pesquisa. Eles vão para o fichamento e sustentam a parte teórica e a discussão. Os tempos de execução medidos no Player2 não saem deste levantamento: são uma etapa complementar do grupo, descrita na etapa (c), e depois são comparados com o que a literatura aponta.

---

## FASE 1 — Planejamento da Busca

### Passo 1 — Pergunta de pesquisa e palavras-chave

**1.1 Problema/pergunta de pesquisa (versão de trabalho)**
*Ainda não precisa ser a versão final (isso vem na etapa "c"), mas deve orientar a busca desta fase.*

> Como o tempo de execução do algoritmo de Dijkstra se comporta, na prática, em relação ao crescimento teórico previsto pela notação assintótica, quando aplicado a grafos de afinidade de tamanhos crescentes?

**1.2 Conceitos-chave e sinônimos**
*Liste os conceitos centrais da pergunta e seus sinônimos, em português e inglês.*

| Conceito-chave | Sinônimos / termos relacionados (PT) | Sinônimos / termos relacionados (EN) |
|---|---|---|
| Algoritmo de Dijkstra | menor caminho, caminho mínimo | shortest path, Dijkstra's algorithm |
| Complexidade de algoritmos | análise assintótica, notação Big O | algorithm complexity, asymptotic analysis, Big O notation |
| Grafos ponderados | grafo com pesos, rede ponderada | weighted graph, weighted network |
| Sistemas de recomendação por afinidade | matching, recomendação de usuários | recommendation system, affinity matching, user matching |

*Responsável por este passo: Kevin dos Santos Vieira*

---

### Passo 2 — Strings de busca

*Combine os termos do passo 1 com operadores booleanos (`AND`, `OR`, `NOT`). Use aspas para termos compostos e truncamento (`*`) quando a base permitir.*

| Nº | String de busca | Base(s) em que será usada | Elaborada por |
|---|---|---|---|
| 1 | `("Dijkstra's algorithm" OR "shortest path algorithm") AND ("asymptotic complexity" OR "time complexity" OR "Big O notation")` | IEEE Xplore, ACM Digital Library | Daniel Vieira Santos |
| 2 | `("weighted graph" OR "graph theory") AND ("recommendation system" OR "affinity matching" OR "user matching")` | Google Scholar, ACM Digital Library | Daniel Vieira Santos |
| 3 | `("algoritmo de Dijkstra" OR "caminho mínimo") AND ("complexidade assintótica" OR "análise de algoritmos")` | Portal de Periódicos CAPES, Google Scholar | Kevin dos Santos Vieira |

---

### Passo 3 — Bases de dados escolhidas

*Selecione de 2 a 4 bases relevantes ao tema. Registre a justificativa — isso vai para a seção de metodologia do artigo/relatório de IC.*

| Base de dados | Por que foi escolhida | Responsável pela busca nesta base |
|---|---|---|
| IEEE Xplore | Referência em publicações de ciência da computação e engenharia, com forte cobertura de algoritmos e complexidade computacional | Daniel Vieira Santos |
| ACM Digital Library | Base especializada em computação, reúne artigos sobre estruturas de dados, grafos e análise de algoritmos com boa profundidade técnica | Kevin dos Santos Vieira |
| Google Scholar | Cobertura ampla e multidisciplinar, útil para localizar trabalhos aplicados (sistemas de recomendação, matching) que não estão indexados só em bases técnicas | Kevin dos Santos Vieira |
| Portal de Periódicos CAPES | Acesso gratuito via login institucional a periódicos nacionais e internacionais, útil para encontrar produção acadêmica em português sobre o tema | Eduardo Alves dos Reis |

---

### Passo 4 — Critérios de inclusão e exclusão

**Critérios de inclusão:**
- Artigos publicados nos últimos 10 anos (2016 em diante), com exceção das obras seminais e consolidadas sobre a complexidade do Dijkstra (artigo original e resultados clássicos de filas de prioridade e de avaliação experimental), que são referência obrigatória para a fundamentação teórica
- Trabalhos revisados por pares (artigos de periódico ou de conferência). Preprints do arXiv só entram como apoio, identificados como tal na lista final, quando tratam diretamente do tema
- Disponíveis em português ou inglês
- Disponíveis na íntegra (texto completo, não apenas resumo)
- Relacionados a pelo menos um dos dois eixos do tema: complexidade/análise de algoritmos de caminho mínimo, ou grafos aplicados a recomendação/matching

**Critérios de exclusão:**
- Resumos ou abstracts sem acesso ao texto completo
- Artigos duplicados entre bases
- Trabalhos fora do escopo (ex.: Dijkstra aplicado apenas a roteamento de redes de computadores, sem relação com análise de complexidade)
- Materiais não revisados por pares (blogs, posts de fórum, documentação de bibliotecas)

*Definidos em conjunto por: Daniel Vieira Santos e Kevin dos Santos Vieira*

---

## FASE 2 — Execução da Busca e Triagem

> As buscas abaixo foram executadas em 12/09/2026, usando as strings do Passo 2 como base, em mecanismos de busca acadêmica com cobertura das bases indicadas (IEEE Xplore, ACM Digital Library, arXiv, Google Scholar e a biblioteca digital da Sociedade Brasileira de Computação, SBC OpenLib, que reúne boa parte do que estaria acessível via Portal CAPES para esse tema).

### Passo 5 — Execução das buscas e registro dos resultados

*Anote quantos resultados cada string trouxe em cada base (útil para o fluxograma tipo PRISMA, se o projeto exigir). Exporte as referências (BibTeX, RIS, CSV) para um gerenciador de referências.*

| Base | String usada (nº) | Data da busca | Nº de resultados | Executada por |
|---|---|---|---|---|
| IEEE Xplore / ACM Digital Library (busca acadêmica combinada) | 1 | 12/09/2026 | 8 | Daniel Vieira Santos |
| Google Scholar / ACM Digital Library (busca acadêmica combinada) | 2 | 12/09/2026 | 9 | Kevin dos Santos Vieira |
| Portal CAPES / SBC (busca acadêmica combinada, termos em português) | 3 | 12/09/2026 | 9 | Kevin dos Santos Vieira |

**Total de resultados brutos (soma de todas as buscas):** 26

**Gerenciador de referências utilizado:** Zotero
**Formato de exportação:** BibTeX

---

### Passo 6 — Triagem por título e resumo (1ª filtragem)

*Leia apenas título e resumo de cada resultado. Classifique: incluir / excluir / dúvida. Remova duplicatas entre bases.*

| Item de controle | Quantidade |
|---|---|
| Total de resultados antes da triagem | 26 |
| Duplicatas removidas | 3 |
| Classificados como "Incluir" | 15 |
| Classificados como "Excluir" | 8 |
| Classificados como "Dúvida" | 0 |

*A triagem detalhada, artigo por artigo, deve ser registrada na planilha de controle do projeto (aba "Triagem de Artigos"). Aqui, registre apenas o resumo quantitativo.*

**Como as dúvidas foram resolvidas?** *(ex.: discussão em grupo, consulta ao orientador)*
Não houve casos de dúvida nesta triagem: os títulos e resumos deixavam claro o escopo de cada artigo. Os principais motivos de exclusão foram trabalhos fora do eixo do tema (ex.: computação quântica aplicada a caminhos mínimos, roteamento em redes de pagamento tipo blockchain, correspondência de malhas 3D) ou material não revisado por pares (slides de aula, sites de visualização).

*Responsável(is) por esta triagem: Kevin dos Santos Vieira*

---

### Passo 7 — Triagem por leitura completa (2ª filtragem)

*Para os artigos que passaram na primeira filtragem, leia introdução e conclusão. Aplique os critérios de inclusão/exclusão (passo 4) de forma mais rigorosa.*

| Item de controle | Quantidade |
|---|---|
| Total de artigos que entraram nesta filtragem | 15 |
| Aprovados (conjunto definitivo para fichamento) | 7 |
| Excluídos nesta etapa | 8 |

**Principais motivos de exclusão nesta filtragem:**
- Foco excessivamente teórico, sem análise empírica de desempenho (ex.: provas de limites assintóticos sem implementação ou testes práticos)
- Aplicação em domínio muito distante do escopo do projeto (ex.: redes ópticas, sistemas distribuídos de larga escala) sem contribuição direta para a comparação entre teoria e prática em grafos de afinidade

*Responsável(is) por esta triagem: Daniel Vieira Santos*

---

### Passo 7.1 — Revisão do conjunto após o parecer da orientadora (19/09/2026)

Depois do parecer de 15/09/2026, o grupo revisou o conjunto aprovado no Passo 7:

- **Removido:** Chen et al. (2020). O trabalho trata de aprendizado semissupervisionado para recomendação e não envolve o Dijkstra nem análise de complexidade, então não contribui para a pergunta de pesquisa.
- **Unificado:** os dois trabalhos do ETC 2026 (Fernandes; Castro; de Freitas-Rodrigues e Fernandes et al.) eram versões do mesmo estudo. Nos anais publicados pela SBC só consta a versão "Análise assintótica e empírica de filas de prioridade avançadas aplicadas ao Algoritmo de Dijkstra" (p. 41-45, DOI 10.5753/etc.2026.22057), que foi a mantida.
- **Referências conferidas:** o artigo do REIC 2026 teve DOI e volume confirmados na página da revista (v. 24, n. 1, DOI 10.5753/reic.2026.7147).
- **Incluídos:** cinco trabalhos consolidados sobre a complexidade do Dijkstra, encontrados por busca retroativa (snowballing) nas referências dos artigos já selecionados, todos revisados por pares e com DOI: o artigo original de Dijkstra (1959), os heaps de Fibonacci de Fredman e Tarjan (1987), a avaliação teórica e experimental de Cherkassky, Goldberg e Radzik (1996), o resultado de otimalidade universal de Haeupler et al. (FOCS 2024) e o algoritmo de Duan et al. (STOC 2025).

| Item de controle | Quantidade |
|---|---|
| Conjunto aprovado no Passo 7 | 7 |
| Removidos (fora do escopo) | 1 |
| Unificados (duplicata) | 1 |
| Incluídos por busca retroativa | 5 |
| **Conjunto definitivo para fichamento** | **10** |

*Responsável(is) por esta revisão: ⚠️ PREENCHER*

---

## 3. Lista Final de Artigos Selecionados (Conjunto Definitivo)

*Liste aqui os artigos que passaram por todas as filtragens e seguirão para o fichamento (etapa "j"). Referência completa no formato ABNT/APA definido pelo projeto.*

A lista está separada pelo papel de cada trabalho na revisão da literatura. Os itens marcados como preprint não passaram por revisão por pares e entram só como apoio.

**Eixo 1: Fundamentos e complexidade teórica do Dijkstra**

1. DIJKSTRA, E. W. A note on two problems in connexion with graphs. Numerische Mathematik, v. 1, p. 269-271, 1959. DOI: 10.1007/BF01386390.
2. FREDMAN, M. L.; TARJAN, R. E. Fibonacci heaps and their uses in improved network optimization algorithms. Journal of the ACM, v. 34, n. 3, p. 596-615, 1987. DOI: 10.1145/28869.28874.
3. HAEUPLER, B.; HLADÍK, R.; ROZHOŇ, V.; TARJAN, R. E.; TĚTEK, J. Universal optimality of Dijkstra via beyond-worst-case heaps. In: IEEE Annual Symposium on Foundations of Computer Science (FOCS), 65., 2024, Chicago. Proceedings [...]. IEEE, 2024. p. 2099-2130. DOI: 10.1109/FOCS61266.2024.00125.
4. DUAN, R.; MAO, J.; MAO, X.; SHU, X.; YIN, L. Breaking the sorting barrier for directed single-source shortest paths. In: Annual ACM Symposium on Theory of Computing (STOC), 57., 2025, Praga. Proceedings [...]. New York: ACM, 2025. p. 36-44. DOI: 10.1145/3717823.3718179.

**Eixo 2: Análise empírica: teoria vs. tempo medido**

5. CHERKASSKY, B. V.; GOLDBERG, A. V.; RADZIK, T. Shortest paths algorithms: theory and experimental evaluation. Mathematical Programming, v. 73, n. 2, p. 129-174, 1996. DOI: 10.1007/BF02592101.
6. FERNANDES, A. C.; CASTRO, L.; CLEMENTINO, T.; FREITAS, R. de. Análise assintótica e empírica de filas de prioridade avançadas aplicadas ao Algoritmo de Dijkstra. In: Encontro de Teoria da Computação (ETC), 11., 2026, Gramado. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2026. p. 41-45. DOI: 10.5753/etc.2026.22057.
7. RIOS, M. L.; S. NETO, F. S.; NETTO, J. F. M. Análise e comparação dos algoritmos de Dijkstra e A-Estrela na descoberta de caminhos mínimos em mapas de grade. In: Encontro de Teoria da Computação (ETC), 1., 2016, Porto Alegre. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2016. p. 887-890. DOI: 10.5753/etc.2016.9852.
8. SILVA E SILVA, L. G.; CARMONA CORTES, O. A. Paralelização do algoritmo de Dijkstra para grafos não direcionados de grande escala. Revista Eletrônica de Iniciação Científica em Computação, v. 24, n. 1, 2026. DOI: 10.5753/reic.2026.7147.
9. CASTRO, L.; CLEMENTINO, T.; DE FREITAS-RODRIGUES, R. Implementation and brief experimental analysis of the Duan et al. (2025) algorithm for single-source shortest paths. arXiv preprint arXiv:2511.03007, 2025. *(preprint)*

**Eixo 3: Caminho mínimo aplicado a recomendação**

10. DAI, J.; JIA, Z.; GAO, X.; CHEN, G. A hierarchical optimizer for recommendation system based on shortest path algorithm. arXiv preprint arXiv:1911.08994, 2019. *(preprint)*

*(Adicione quantas linhas forem necessárias.)*

---

## 4. Contribuição Individual dos Integrantes

> **Importante:** cada integrante deve descrever, com suas próprias palavras, o que efetivamente fez em cada passo desta etapa. Contribuições genéricas como "ajudei em tudo" não serão aceitas. Use verbos de ação e seja específico (ex.: "executei a busca no IEEE Xplore com a string 2 e obtive 84 resultados; fiz a triagem por título/resumo de 40 desses").

### Integrante 1 — Daniel Vieira Santos
- **Passo(s) em que atuou:** Passos 1 (apoio), 2, 3 (IEEE Xplore), 4 e 7
- **O que fez em cada passo:** Elaborou as strings de busca do Passo 2 combinando os conceitos-chave com operadores booleanos, executou a busca com a string 1 (voltada a IEEE Xplore/ACM), obtendo 8 resultados, ajudou a definir os critérios de inclusão e exclusão do Passo 4 junto com o Kevin, e conduziu a triagem por leitura completa do Passo 7, aprovando 7 dos 15 artigos que chegaram a essa fase.
- **Tempo dedicado (aprox.):** 3H
- **Evidência da contribuição:** envio dos documentos das etapas (b) e (c) ao repositório do grupo (commit 8daf051, 12/09/2026): https://github.com/Dannzinho/Complexidade-do-Algoritmo-de-Dijkstra-em-Grafo-de-Afinidade/commit/8daf051

### Integrante 2 — Kevin dos Santos Vieira
- **Passo(s) em que atuou:** Passos 1, 3 (ACM Digital Library, Google Scholar e SBC), 4, 5 e 6
- **O que fez em cada passo:** Definiu a pergunta de pesquisa de trabalho e o quadro de conceitos-chave/sinônimos do Passo 1, executou as strings 2 e 3 (9 resultados cada), ajudou a definir os critérios de inclusão e exclusão do Passo 4 junto com o Daniel, e fez a triagem por título/resumo do Passo 6, removendo 3 duplicatas e classificando 15 dos 26 resultados como "incluir".
- **Tempo dedicado (aprox.):** 4H
- **Evidência da contribuição:** artigos localizados com as strings 2 e 3: [ETC 2026](https://sol.sbc.org.br/index.php/etc/article/view/43639), [REIC 2026](https://doi.org/10.5753/reic.2026.7147), [ETC 2016](https://doi.org/10.5753/etc.2016.9852) e [Dai et al. 2019](https://arxiv.org/abs/1911.08994); Passos 1 e 6 registrados no documento: [b_Levantamento_Bibliografico_Preliminar.md](https://github.com/Dannzinho/Complexidade-do-Algoritmo-de-Dijkstra-em-Grafo-de-Afinidade/blob/main/b_Levantamento_Bibliografico_Preliminar.md)

### Integrante 3 — Eduardo Alves dos Reis
- **Passo(s) em que atuou:** Passo 3 (Portal de Periódicos CAPES)
- **O que fez em cada passo:** Ficou responsável pela base Portal de Periódicos CAPES no Passo 3, verificando o acesso institucional e levantando os termos de busca em português usados na string 3.
- **Tempo dedicado (aprox.):** 1H30
- **Evidência da contribuição:** base consultada: [Portal de Periódicos CAPES](https://www.periodicos.capes.gov.br); termos em português da string 3 e base registrados nos Passos 2 e 3 do documento: [b_Levantamento_Bibliografico_Preliminar.md](https://github.com/Dannzinho/Complexidade-do-Algoritmo-de-Dijkstra-em-Grafo-de-Afinidade/blob/main/b_Levantamento_Bibliografico_Preliminar.md)

*(Copie o bloco acima para cada integrante adicional do grupo.)*

### 4.1 Quadro-resumo de participação por passo

| Passo | Responsável(is) | % estimado de participação de cada um |
|---|---|---|
| 1. Pergunta e palavras-chave | Kevin dos Santos Vieira | Kevin 100% |
| 2. Strings de busca | Daniel Vieira Santos | Daniel 100% |
| 3. Bases de dados | Daniel, Kevin e Eduardo | Daniel 35% / Kevin 40% / Eduardo 25% |
| 4. Critérios de inclusão/exclusão | Daniel Vieira Santos e Kevin dos Santos Vieira | Daniel 50% / Kevin 50% |
| 5. Execução das buscas | Daniel Vieira Santos e Kevin dos Santos Vieira | Daniel 35% (string 1) / Kevin 65% (strings 2 e 3) |
| 6. Triagem título/resumo | Kevin dos Santos Vieira | Kevin 100% |
| 7. Triagem texto completo | Daniel Vieira Santos | Daniel 100% |

### 4.2 Quadro-resumo geral de participação na etapa

| Integrante | % estimado de participação total nesta etapa |
|---|---|
| Daniel Vieira Santos | 40% |
| Kevin dos Santos Vieira | 40% |
| Eduardo Alves dos Reis | 20% |

*A soma das porcentagens deve ser igual a 100%. Divergências de percepção sobre a participação devem ser discutidas em grupo antes do envio — o orientador pode solicitar esclarecimentos individuais em caso de disparidade relevante.*

---

## 5. Checklist Final da Etapa

**Fase 1 — Planejamento**
- [x] Pergunta de pesquisa de trabalho definida
- [x] Conceitos-chave e sinônimos (PT/EN) listados
- [x] Strings de busca elaboradas com operadores booleanos
- [x] Bases de dados escolhidas e justificadas
- [x] Critérios de inclusão e exclusão definidos

**Fase 2 — Execução e triagem**
- [x] Buscas executadas e resultados registrados por base/string
- [x] Referências exportadas para o gerenciador de referências
- [x] Triagem por título/resumo concluída (com duplicatas removidas)
- [x] Triagem por texto completo (introdução/conclusão) concluída
- [x] Conjunto definitivo de artigos para fichamento compilado
- [x] Conjunto revisado após o parecer da orientadora (Passo 7.1)

**Documentação**
- [x] Contribuição individual de cada integrante registrada por passo
- [x] Quadro-resumo de participação preenchido (soma = 100%)

---
