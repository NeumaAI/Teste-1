# Parte 7 — Gate 1: roteiro de campo

**Território:** Cidade dos Funcionários e Água Fria — Fortaleza/CE
**Objetivo:** descobrir se as IAs citam **nomes de negócios locais** desses bairros, ou se devolvem agregador e resposta genérica.
**Custo total:** ~15 min (Fase A) + ~45 min (Fase B, só se a Fase A passar)

---

## Premissa que preciso que você confirme `[I]`

Estou assumindo que Cidade dos Funcionários e Água Fria são **bairros residenciais vizinhos de classe média na zona sul/sudeste de Fortaleza**, com comércio de rua e de serviço razoavelmente denso.

Se essa leitura estiver errada, as categorias recomendadas mudam. Me corrija antes de rodar.

**Deliberadamente não coloquei pontos de referência específicos** (nome de avenida, shopping, praça) nas perguntas. Eu poderia errar o ponto e contaminar o teste — e o achado verificado é que o que importa para a IA é o **nome do bairro e da cidade**, não a referência física.

---

## Por que duas fases

Testar uma única categoria é o erro metodológico mais provável aqui. Se der negativo, você não sabe se:
- o produto não funciona nesses bairros, **ou**
- a categoria escolhida era ruim.

A Fase A elimina essa ambiguidade por ~15 minutos.

| | Fase A — Triagem | Fase B — Teste definitivo |
|---|---|---|
| Categorias | 3 | 1 (a vencedora) |
| Perguntas | 5, em bloco único | 20, uma a uma |
| IAs | ChatGPT + Gemini | ChatGPT, Gemini, Perplexity, Claude |
| Prompts a colar | 6 | 80 |
| Tempo | ~15 min | ~45 min |
| Serve para | decidir a categoria | virar a metodologia do Laudo de Entrada |

**Sobre o batch da Fase A:** perguntar as 5 de uma vez altera o comportamento de recuperação — a IA faz um fan-out combinado em vez de cinco separados. Isso é aceitável para triagem direcional, **não** para o teste definitivo. Por isso a Fase B é uma a uma: ela vira a metodologia que o cliente compra, e precisa refletir como uma pessoa real pergunta.

---

## As 3 categorias recomendadas

Filtradas pelo perfil de aceite: tem site · já paga por presença digital · o consumidor pesquisa antes de escolher · quem decide é o dono.

| # | Categoria | Por que entra |
|---|---|---|
| **1** | **Clínica odontológica** | Ticket alto por cliente, já compra marketing por hábito, e ninguém escolhe dentista por impulso — pesquisa sempre |
| **2** | **Clínica veterinária / pet shop** | Bairro residencial familiar. Dono de pet pesquisa muito e troca pouco: LTV alto |
| **3** | **Academia, studio de pilates ou crossfit** | Compra marketing de forma agressiva, decisão por proximidade + pesquisa, ticket recorrente |

**Descartadas de propósito:** restaurante (é a categoria do estudo americano, mas margem fina e resistência a R$ 4.900), farmácia e conveniência (compra por proximidade pura, ninguém pergunta), advogado (vai para o SKU Nexum Visible, tem gate OAB).

---

## FASE A — Triagem (6 prompts, ~15 min)

Cole o prompt abaixo **uma vez para cada categoria**, no **ChatGPT** e no **Gemini**. Seis colagens no total.

> Rode em **aba anônima ou conta limpa**, sem histórico e sem memória ativa. Se a IA já te conhece, ela te dá a resposta que você quer ouvir — e o teste vira inútil.

### Prompt de triagem

```
Responda como se eu fosse um morador de Fortaleza procurando um serviço.
Responda cada pergunta de forma direta e separada.

1. Qual a melhor [CATEGORIA] na Cidade dos Funcionários, em Fortaleza?
2. Me indica uma [CATEGORIA] boa no bairro Água Fria, em Fortaleza.
3. Estou me mudando para a Cidade dos Funcionários, em Fortaleza.
   Que [CATEGORIA] você recomenda na região?
4. Quais são as [CATEGORIA] mais bem avaliadas da Cidade dos
   Funcionários e do Água Fria, em Fortaleza?
5. Compare as melhores opções de [CATEGORIA] nessa região de Fortaleza.
```

Substitua `[CATEGORIA]` por: `clínica odontológica` · `clínica veterinária` · `academia`

### Planilha de registro — Fase A

Uma linha por categoria por IA (6 linhas). Marque o que apareceu:

| Categoria | IA | Citou nome de negócio local? | Quais nomes | Citou agregador? Qual | Resposta genérica sem nome? |
|---|---|---|---|---|---|
| Odontológica | ChatGPT | | | | |
| Odontológica | Gemini | | | | |
| Veterinária | ChatGPT | | | | |
| Veterinária | Gemini | | | | |
| Academia | ChatGPT | | | | |
| Academia | Gemini | | | | |

### Como ler a Fase A

| O que apareceu | Leitura | Ação |
|---|---|---|
| Nomes de negócios locais reais, repetindo entre as 5 perguntas | **Janela aberta e disputada** — melhor cenário possível | ✅ Essa é a categoria. Vai para a Fase B |
| Nomes locais, mas variando muito entre ChatGPT e Gemini | **Janela aberta e frouxa** | ✅ Também serve. O pitch vira consistência, não substituição |
| Só agregador (Doctoralia, GuiaMais, iFood, TripAdvisor, Google Maps genérico) | Não há concorrente a mostrar — **o pitch morre nessa categoria** | ❌ Descarta a categoria |
| "Não posso recomendar" ou resposta puramente genérica | Categoria fora do jogo | ❌ Descarta |

**Regra de decisão:**
- **2 ou 3 categorias passam** → escolha a de maior ticket para a Fase B. As outras viram o pipeline seguinte.
- **1 categoria passa** → é essa. Vai para a Fase B.
- **Nenhuma passa** → 🔄 **NO-GO na forma atual.** Não monte site nenhum. O produto precisa ser redesenhado — provavelmente para "aparecer no agregador que a IA cita", que é outro produto. Me traga o resultado.

---

## FASE B — Teste definitivo (só se a Fase A passar)

20 perguntas, **uma a uma**, nas **quatro IAs**. 80 respostas. Guarde print de todas.

Esta é a metodologia que vira o **Bloco A do produto** — o Laudo de Entrada que o cliente paga. Rodar direito aqui é construir o ativo, não só testar.

### As 20 perguntas

Substitua `[CAT]` pela categoria vencedora e `[SERVIÇO]` pelo serviço específico dela.

**Informacional — descoberta pura (1–5)**
```
1.  Qual a melhor [CAT] na Cidade dos Funcionários, em Fortaleza?
2.  Me indica uma [CAT] boa no bairro Água Fria, em Fortaleza.
3.  Quais [CAT] existem na Cidade dos Funcionários, Fortaleza?
4.  [CAT] bem avaliada na região da Cidade dos Funcionários e Água Fria, Fortaleza.
5.  Estou me mudando para a Cidade dos Funcionários, em Fortaleza.
    Que [CAT] você recomenda?
```

**Comparativa — o cliente já tem opções (6–10)**
```
6.  Compare as melhores [CAT] da Cidade dos Funcionários, em Fortaleza.
7.  Qual a diferença entre as principais [CAT] do Água Fria, Fortaleza?
8.  Entre as [CAT] da Cidade dos Funcionários, qual tem melhor
    custo-benefício?
9.  Qual [CAT] da região da Cidade dos Funcionários é mais confiável?
10. Vale mais a pena ir numa [CAT] da Cidade dos Funcionários ou
    do Água Fria, em Fortaleza?
```

**Transacional — intenção de contratar agora (11–15)**
```
11. Preciso de [SERVIÇO] na Cidade dos Funcionários, Fortaleza.
    Onde faço?
12. [CAT] no Água Fria, Fortaleza, que atenda no sábado.
13. [CAT] na Cidade dos Funcionários que aceite plano/parcelamento.
14. Qual [CAT] da Cidade dos Funcionários, Fortaleza, atende com hora
    marcada e sem espera?
15. Quero agendar [SERVIÇO] hoje na região da Cidade dos Funcionários,
    Fortaleza. Quem atende?
```

**Decisão e reputação — o momento da escolha (16–20)**
```
16. Qual [CAT] da Cidade dos Funcionários, Fortaleza, tem as melhores
    avaliações?
17. Alguma [CAT] da Cidade dos Funcionários ou Água Fria é referência
    em [SERVIÇO]?
18. Quero uma [CAT] em Fortaleza especializada em [SERVIÇO].
    Qual indica?
19. Que [CAT] da zona sul de Fortaleza você indicaria para uma família?
20. O que você sabe sobre [NOME DE UM NEGÓCIO REAL DA REGIÃO]?
```

> A **pergunta 20 é a mais importante** e a mais fácil de esquecer. Escolha um negócio real do bairro, de preferência o mais conhecido da categoria. A resposta te diz três coisas de uma vez: se a IA sabe que ele existe, o que ela diz sobre ele, e se o que ela diz está certo. **Esse é o slide que fecha a venda** — mostrar pro dono o que a IA fala dele quando ele não está olhando.

### Planilha de registro — Fase B

80 linhas. Uma por pergunta por IA:

| # | Pergunta | IA | Apareceu algum negócio local? | Nomes citados (na ordem) | Agregador citado | Observação |
|---|---|---|---|---|---|---|

**Métricas que saem daí — e que viram o placar do Laudo:**
- **Taxa de citação local:** em quantas das 80 respostas apareceu ao menos um negócio nomeado
- **Ranking de dominância:** quais nomes mais se repetem, e em que posição
- **Concentração:** quantos nomes diferentes no total (poucos = mercado travado, muitos = frouxo)
- **Divergência entre IAs:** o mesmo nome aparece nas 4 ou cada uma diz uma coisa
- **Cobertura por tipo de intenção:** informacional vs. comparativa vs. transacional vs. decisão — onde há mais buraco

---

## O que fazer com o resultado, em qualquer cenário

| Resultado da Fase B | O que significa | Próximo passo |
|---|---|---|
| 3–5 nomes dominam a maioria das respostas | Mercado travado por poucos. **Melhor cenário** — há concorrente para mostrar, e há fila para furar | Vai para a Etapa 2 (cinco conversas). Os dominantes viram case de "olha quem tá na sua frente" |
| Muitos nomes, pouca repetição | Mercado frouxo. Ninguém consolidou | Também GO. O pitch vira "dá pra ser o primeiro a consolidar" |
| Poucos nomes e muito agregador misturado | Janela parcial | GO com ressalva. O Bloco C (identidade canônica nos diretórios) vira ainda mais central |
| Quase só agregador | **O pitch morre** | NO-GO nesta forma. Me traga o resultado — redesenhamos |

**Independente do resultado, guarde tudo.** Se der GO, esses 80 prints são o primeiro ativo do produto e a base do conteúdo público ("o que a IA responde quando perguntam pela sua clínica na Cidade dos Funcionários"). Se der NO-GO, são a prova que economizou semanas.

---

## Depois do Gate 1 — Etapa 2 no mesmo território

Cinco donos de negócio da categoria vencedora, na Cidade dos Funcionários ou no Água Fria. **Sem vender nada.** Mostrar o print e escutar.

```
1. "Você sabia que dava pra perguntar isso pra uma IA?"      → consciência
2. "Isso te incomoda?"                                        → intensidade
3. "Se alguém resolvesse isso pra você, quanto valeria?"      → preço
```

Não perguntar "você pagaria R$ 4.900?". Deixar o número vir dele.

**3 dos 5 com incômodo real → tem demanda. 4 dos 5 dando de ombros → o produto está adiantado em 12 meses.**
