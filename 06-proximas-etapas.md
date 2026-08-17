# Parte 6 — Próximas etapas recomendadas

Ordenadas por **valor de informação dividido por custo**. Cada uma converte especulação em fato ou produz receita. Nenhuma é "escrever mais documento".

---

## Etapa 1 — O teste dos 30 minutos `BLOQUEANTE`

**Custo:** 30 min · **Quem:** você · **Quando:** antes de qualquer outra coisa

Escolha **um bairro** e **uma categoria**. Rode 15–20 perguntas nas quatro IAs. Registre quem é citado.

Modelo de perguntas (nomeando o bairro sempre — o ChatGPT não sabe onde você está, achado N3):

```
1.  Qual a melhor [categoria] na [bairro], em Fortaleza?
2.  Me indica uma [categoria] boa perto da [referência conhecida do bairro].
3.  Qual [categoria] em [bairro] atende [necessidade específica]?
4.  [Categoria] em [bairro] que abre aos domingos?
5.  Qual a [categoria] mais bem avaliada da [bairro]?
6.  Vou me mudar pra [bairro], que [categoria] você recomenda?
7.  [Categoria] em Fortaleza que faz [serviço específico]?
8.  Compare as melhores [categoria] da [bairro].
...até 20, variando intenção: informacional, comparativa, transacional, decisão
```

**Leitura do resultado:**

| O que aparece | Leitura | Decisão |
|---|---|---|
| Nomes de negócios locais, sempre os mesmos 3–5 | Janela aberta e disputada — **melhor cenário** | ✅ GO |
| Nomes locais variando muito entre IAs | Janela aberta e frouxa | ✅ GO, pitch vira consistência |
| Só agregadores (TripAdvisor, iFood, Doctoralia) | O pitch morre — não há concorrente a mostrar | 🔄 Redesenhar |
| "Não posso recomendar" | Categoria fora do jogo | ❌ Trocar categoria |

**Guarde os prints.** Independente do resultado, eles viram o primeiro ativo do produto.

---

## Etapa 2 — Cinco conversas na rua `BLOQUEANTE`

**Custo:** 2h · **Quem:** você ou a pessoa executora · **Quando:** logo após a Etapa 1

Cinco donos de negócio do perfil de aceite. **Sem vender nada.** Mostrar o print e escutar.

Três perguntas, nesta ordem, e depois calar a boca:
1. *"Você sabia que dava pra perguntar isso pra uma IA?"* → mede consciência do problema
2. *"Isso te incomoda?"* → mede intensidade da dor
3. *"Se alguém resolvesse isso pra você, quanto isso valeria?"* → **não** perguntar "você pagaria R$ 4.900?"; deixar o número vir dele

**O que você está medindo:** se pelo menos 3 dos 5 demonstrarem incômodo real, o produto tem demanda. Se 4 dos 5 derem de ombros, o problema não dói o suficiente **ainda** e o produto está adiantado em 12 meses.

**Por que esta etapa é bloqueante:** é a única que testa o item 4 da §5.5 — se o comerciante aceita o preço. Nenhum documento responde isso.

---

## Etapa 3 — Verificar o motor Python

**Custo:** 5 min · **Quem:** você

Três respostas possíveis: está em outro repositório/máquina (me aponte) · nunca virou código (é escopo, ~8–12h) · você lembrou da skill, que declara Python no frontmatter mas não tem código.

Não bloqueia as três primeiras vendas. Bloqueia a escala: com automação, o Raio-X vai de 20 min para ~2 min por alvo — a diferença entre 13h e 1h30 por bairro de 40 alvos.

---

## Etapa 4 — Varredura competitiva local, de verdade

**Custo:** 1h · **Quem:** a pessoa executora

Meu mapeamento é remoto e a busca é enviesada para conteúdo em inglês/EUA. O que falta:

- Existe agência GEO em Fortaleza que a busca não pegou? (LinkedIn "GEO" + Fortaleza, Instagram, grupos locais de marketing)
- **Quem já vende site para o comércio da região, e por quanto?** É com esse preço que o cliente vai te comparar, não com a GeoStack
- A GeoStack atende Nordeste remotamente? (define se ela é concorrente real ou teórica)

---

## Etapa 5 — Corrigir os documentos que ficaram falsos

**Custo:** 20 min · **Quem:** você

Quatro correções, senão a próxima sessão (sua ou de outro LLM) reproduz os mesmos erros:

| Documento | Corrigir |
|---|---|
| Nexum Visible §13 | Promptado **não** é R$ 199 — é R$ 99/399/799 |
| Nexum Visible §1 | Declarar que a vedação a "criação de site" é **da unidade Visible**, não da casa |
| Nexum Visible §9 | Declarar que o piso de R$ 2.000/mês é **da Visible**, não regra geral |
| plano_agencia_geo | Marcar como **desatualizado**: o gap "nenhuma agência pura de GEO" foi ocupado pela GeoStack |

---

## Etapa 6 — Construir o template do site

**Custo:** 12–16h `[I]` · **Quando:** junto com a unidade #1, não antes

Sem ele, "10 dias úteis" é promessa e cada site é artesanal. HTML estático, 5–7 páginas, schema JSON-LD parametrizado, `llms.txt`, `robots.txt` liberando os crawlers de IA, LCP < 2,5s, conteúdo sem dependência de JS.

**Novidade vinda da auditoria:** o achado N3 (o ChatGPT não sabe onde você está; consistência NAP entre site/GBP/diretórios é determinante) faz o **Bloco C subir para o centro do produto**. O template precisa gerar o documento de identidade canônica como saída, não como anexo.

---

## Etapa 7 — Ajustar o produto ao que a auditoria revelou

**Custo:** 1h de decisão sua

| Ajuste | De | Para |
|---|---|---|
| Recorrente | R$ 690/mês | **R$ 890/mês** |
| Laudo avulso | R$ 690 | **R$ 890** |
| Ferramenta | Promptado desde o cliente 1 | **Nenhuma até o cliente 4** |
| Argumento de preço | "mais caro que freelancer, mais barato que anúncio" | **"R$ 13.180 no ano 1 vs R$ 41.880 da GeoStack, com site incluso"** |
| Argumento principal | 58% de queda de CTR | **83% dos negócios invisíveis no ChatGPT vs 14% no Google** |
| Escopo | sem gestão de avaliações | **incluir orientação de avaliações** (20+ novas em 3 meses = 2,5× mais chance) |

---

## Etapa 8 — Unidade #1, o caso zero

Só depois das Etapas 1, 2 e 6. Alguém que você conhece, na categoria que passou no Gate 1, de graça ou a custo, **com autorização escrita de uso público do resultado**.

Objetivo real: cronometrar as 19h estimadas, achar onde trava, e produzir o primeiro antes/depois brasileiro — que é o ativo que nenhum concorrente tem e que a GeoStack não publica.

---

## Sequência e tempo

```
Etapa 1  (30 min)  ─┐
                    ├─▶  se GO ──▶ Etapa 3+5 (25 min) ──▶ Etapa 6 + Unidade #1
Etapa 2  (2h)      ─┘                    │
                                    Etapa 4 (1h, em paralelo)
     se qualquer uma falhar ──▶ redesenhar antes de gastar um dia
```

**Até a decisão go/no-go fundamentada: 3 horas de trabalho.**
**Até a primeira unidade paga `[I]`: 3 a 4 semanas.**

---

## O que NÃO fazer agora

- ❌ Escrever mais documento de produto. Você tem quatro. É o padrão C1.
- ❌ Comprar ferramenta antes do cliente 4
- ❌ Registrar marca, comprar domínio, fazer identidade visual antes do Gate 1
- ❌ Treinar a pessoa executora antes de saber se o pitch funciona
- ❌ Prospectar antes de ter o print que prova o problema
