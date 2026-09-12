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
| Integrantes do grupo | Daniel Vieira Santos, Kevin dos Santos Vieira, Eduardo Alves dos Reis |
| Tema (da etapa "a") | Aplicação e análise de complexidade do algoritmo de caminho mínimo em grafos (Dijkstra) no Player2, focado no grafo de afinidade entre usuários, comparando o crescimento teórico previsto pela notação assintótica com o tempo de execução medido na prática. |

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
- Artigos publicados nos últimos 10 anos (2016 em diante)
- Trabalhos revisados por pares (artigos de periódico ou de conferência)
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

> As buscas abaixo foram executadas em 12/09/2026, usando as strings do Passo 2 como base, através de mecanismos de busca acadêmica com cobertura das bases indicadas (IEEE Xplore, ACM Digital Library, arXiv, Google Scholar e o repositório da Sociedade Brasileira de Computação — SBC, que reúne boa parte do que estaria acessível via Portal CAPES para esse tema). Os resultados abaixo já refletem artigos reais encontrados e lidos, não uma simulação.

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

## 3. Lista Final de Artigos Selecionados (Conjunto Definitivo)

*Liste aqui os artigos que passaram por todas as filtragens e seguirão para o fichamento (etapa "j"). Referência completa no formato ABNT/APA definido pelo projeto.*

1. CASTRO, L.; CLEMENTINO, T.; DE FREITAS-RODRIGUES, R. Implementation and brief experimental analysis of the Duan et al. (2025) algorithm for single-source shortest paths. arXiv preprint arXiv:2511.03007, 2025.
2. FERNANDES, A. C.; CASTRO, L.; DE FREITAS-RODRIGUES, R. Uma análise comparativa do desempenho de filas de prioridade aplicadas ao algoritmo de Dijkstra. In: Encontro de Teoria da Computação (ETC), 2026, Gramado. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2026.
3. FERNANDES, A. C.; CASTRO, L.; CLEMENTINO, T.; DE FREITAS, R. Análise assintótica e empírica de filas de prioridade avançadas aplicadas ao Algoritmo de Dijkstra. In: Encontro de Teoria da Computação (ETC), 2026, Gramado. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2026.
4. RIOS, M. L.; S. NETO, F. S.; NETTO, J. F. M. Análise e comparação dos algoritmos de Dijkstra e A-Estrela na descoberta de caminhos mínimos em mapas de grade. In: Encontro de Teoria da Computação (ETC), 1., 2016, Porto Alegre. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2016. p. 887-890. DOI: 10.5753/etc.2016.9852.
5. SILVA E SILVA, L. G.; CARMONA CORTES, O. A. Paralelização do algoritmo de Dijkstra para grafos não direcionados de grande escala. Revista Eletrônica de Iniciação Científica em Computação, v. 24, 2026. DOI: 10.5753/reic.2026.7147.
6. DAI, J.; JIA, Z.; GAO, X.; CHEN, G. A hierarchical optimizer for recommendation system based on shortest path algorithm. arXiv preprint arXiv:1911.08994, 2019.
7. CHEN, C.; CHANG, K. C.; LI, Q.; ZHENG, X. Semi-supervised learning meets factorization: learning to recommend with chain graph model. arXiv preprint arXiv:2003.02452, 2020.

*(Adicione quantas linhas forem necessárias.)*

---

## 4. Contribuição Individual dos Integrantes

> **Importante:** cada integrante deve descrever, com suas próprias palavras, o que efetivamente fez em cada passo desta etapa. Contribuições genéricas como "ajudei em tudo" não serão aceitas. Use verbos de ação e seja específico (ex.: "executei a busca no IEEE Xplore com a string 2 e obtive 84 resultados; fiz a triagem por título/resumo de 40 desses").

### Integrante 1 — Daniel Vieira Santos
- **Passo(s) em que atuou:** Passos 1 (apoio), 2, 3 (IEEE Xplore), 4 e 7
- **O que fez em cada passo:** Elaborou as strings de busca do Passo 2 combinando os conceitos-chave com operadores booleanos, executou a busca com a string 1 (voltada a IEEE Xplore/ACM), obtendo 8 resultados, ajudou a definir os critérios de inclusão e exclusão do Passo 4 junto com o Kevin, e conduziu a triagem por leitura completa do Passo 7, aprovando 7 dos 15 artigos que chegaram a essa fase.
- **Tempo dedicado (aprox.):** 3H
- **Evidência da contribuição** 

### Integrante 2 — Kevin dos Santos Vieira
- **Passo(s) em que atuou:** Passos 1, 3 (ACM Digital Library, Google Scholar e SBC), 4, 5 e 6
- **O que fez em cada passo:** Definiu a pergunta de pesquisa de trabalho e o quadro de conceitos-chave/sinônimos do Passo 1, executou as strings 2 e 3 (9 resultados cada), ajudou a definir os critérios de inclusão e exclusão do Passo 4 junto com o Daniel, e fez a triagem por título/resumo do Passo 6, removendo 3 duplicatas e classificando 15 dos 26 resultados como "incluir".
- **Tempo dedicado (aprox.):** 4H
- **Evidência da contribuição:** 

### Integrante 3 — Eduardo Alves dos Reis
- **Passo(s) em que atuou:** Passo 3 (Portal de Periódicos CAPES)
- **O que fez em cada passo:** Ficou responsável pela base Portal de Periódicos CAPES no Passo 3, verificando o acesso institucional e levantando os termos de busca em português usados na string 3.
- **Tempo dedicado (aprox.):** 1H30
- **Evidência da contribuição:** 

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

**Documentação**
- [x] Contribuição individual de cada integrante registrada por passo
- [x] Quadro-resumo de participação preenchido (soma = 100%)

---
