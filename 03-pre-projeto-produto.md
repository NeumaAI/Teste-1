# Parte 3 — O produto montado

---

## 1. Identidade

### Nome recomendado: **PRIMEIRA RESPOSTA**

Motivo: nomeia o benefício, não o mecanismo. Não contém "site" (que puxa comparação de preço com freelancer) nem "GEO/AIO" (jargão que o comerciante não entende e que soa a promessa vazia — Dor 3 do seu mapa). É a pergunta que o dono do negócio faz sozinho quando ouve o nome.

Alternativas, se preferir: *Fonte Citada* (mais técnico, melhor para B2B) · *Nexum Local* (amarra à marca-mãe, mas herda o peso de explicar Nexum) · *Antes de Escolher* (foco no momento de decisão do consumidor).

### Frase de posicionamento
> Quando alguém pergunta ao ChatGPT qual é o melhor [serviço] aqui na região, alguém é respondido. Nós fazemos com que seja você — e mostramos o antes e o depois.

### O que é vendido
Um projeto fechado, de 10 dias úteis, que entrega um site construído para ser citado por IA, com medição documentada e um kit que organiza o marketing do cliente pelos 12 meses seguintes.

### O que é entregue de verdade (a diferença)
A concorrência entrega um site. Este produto entrega **um site + um laudo**. O laudo é o produto; o site é o meio.

---

## 2. A dor, na ordem em que o cliente a sente

Não inverta esta ordem no pitch. Ela vem da crítica C6.

```
1. SINTOMA        "Tá entrando menos gente nova do que ano passado."
                            ↓
2. CAUSA VISÍVEL  "O pessoal não pesquisa mais no Google como antes."
                            ↓
3. CAUSA REAL     "Eles perguntam pro ChatGPT. E o ChatGPT responde
                   com o nome do seu concorrente."   ← aqui entra o print
                            ↓
4. MECANISMO      "Seu site foi feito pra aparecer numa lista de links.
                   A IA não lê lista — ela lê conteúdo que responde."
                            ↓
5. SOLUÇÃO        Primeira Resposta.
```

O passo 3 é onde a venda acontece, e ele **não é falado — é mostrado**. Print do ChatGPT com o concorrente dele em destaque, na tela do celular, na frente dele.

---

## 3. Escopo — o que entra na caixa

Escopo fechado. Nada fora dele sem novo contrato. Isto é o que faz do serviço um produto.

### Bloco A — Laudo de Entrada (dias 1–2)
- **20 perguntas-âncora** montadas para o negócio dele: as perguntas reais que um cliente faria a uma IA antes de escolher (variações de "melhor X em [bairro]", "X que atende [necessidade específica]", "X aberto [horário]", comparações, e o nome dele direto)
- Cada pergunta rodada em **ChatGPT, Gemini, Perplexity e Claude** — 80 respostas registradas com print e data
- **Placar de entrada:** em quantas ele aparece, em quantas o concorrente aparece, quem são os citados, e o que a IA diz sobre ele quando diz algo
- Documento de 6–8 páginas, linguagem de dono de negócio, zero jargão

> Este bloco **é o produto de entrada gratuito em versão reduzida** (5 perguntas). A versão de 20 é paga e faz parte do projeto.

### Bloco B — O Site (dias 3–7)
Site novo, de 5 a 7 páginas, sobre template próprio já preparado. Não é design autoral — é **arquitetura de citação**:

- **Página-fonte por serviço** — uma página por serviço principal, cada uma respondendo de forma autossuficiente a um bloco de perguntas do Laudo. Resposta direta nos primeiros 2 parágrafos, sem enrolação de "somos uma empresa que preza pela qualidade"
- **Página de perguntas frequentes reais** — as perguntas do Laudo, respondidas com número, prazo, preço-faixa e condição. Não FAQ decorativo
- **Página de identidade canônica** — nome, endereço, telefone, horário, área de atendimento, credenciais, tempo de mercado, nomes das pessoas responsáveis com qualificação. Esta é a página que a IA usa para saber que ele existe e é confiável
- **Camada técnica** (não aparece na tela, é o que faz funcionar):
  - Schema JSON-LD: `LocalBusiness` + `Service` + `FAQPage` + `Person` + `OpeningHoursSpecification`
  - `llms.txt` na raiz
  - `robots.txt` liberando GPTBot, ClaudeBot, PerplexityBot, Google-Extended, CCBot
  - HTML semântico, sem conteúdo dependente de JavaScript
  - Performance: LCP < 2,5s
  - Sitemap + canonical corretos

### Bloco C — Identidade Consistente (dias 7–8)
O efeito documentado é multiplicativo, não aditivo: dados divergentes entre fontes derrubam a citação. Então:
- Documento de **identidade canônica** (uma única versão de nome, endereço, telefone, descrição, serviços)
- Replicação verificada em: Google Business Profile, Apple Maps, Bing Places, Instagram, Facebook, WhatsApp Business, e os 3–5 diretórios do setor dele
- Checklist assinado do que foi corrigido e onde

### Bloco D — Kit de Marketing Organizado (dia 9)
Isto é o "organize a vida do marketing dele" do seu pedido. É o que ninguém entrega e é o que gera indicação.

- **Calendário de 12 conteúdos** — um por mês, cada um amarrado a uma pergunta do Laudo que ele ainda não responde bem. Não é "poste 3× por semana"; é "escreva estas 12 coisas, nesta ordem, e você cobre o que te falta"
- **Modelo de página-fonte** — o esqueleto para ele (ou quem escreve pra ele) produzir conteúdo que tem chance de ser citado: resposta direta no topo, número com fonte, nome e credencial de quem afirma, sem filler
- **Regra dos 3 sinais** — o cartão de bolso: toda página precisa de (1) uma resposta direta em até 40 palavras, (2) um número verificável com origem, (3) uma pessoa nomeada com qualificação. Falta um → não vai ser citada
- **Lista de exclusão** — o que parar de fazer, com motivo

### Bloco E — Laudo de Saída (dia 60)
- As **mesmas 20 perguntas**, nas **mesmas 4 IAs**, mesma metodologia
- Placar comparado, lado a lado, com print e data
- Veredito honesto — inclusive quando não mexeu
- Recomendação do próximo passo

> **O Bloco E é o produto inteiro.** É ele que transforma "mais uma agência" em "obra com laudo", e é ele que gera a indicação: o cliente mostra o antes/depois para outro dono de negócio.

### O que explicitamente NÃO entra
Redes sociais · anúncios pagos · e-commerce/checkout · sistema de agendamento · blog com produção recorrente · identidade visual/logo · fotografia · e-mail marketing · manutenção evolutiva do site.

---

## 4. Por que isso é um sarrafo alto (e não mais uma agência)

Cinco padrões que o produto estabelece e que nenhum concorrente local pratica:

| Padrão | O mercado hoje | Primeira Resposta |
|---|---|---|
| **Medição** | "Melhorou a presença digital" | 20 perguntas × 4 IAs, antes e depois, com print e data |
| **Honestidade prévia** | Aceita todo cliente que paga | Recusa quem não tem chance, no diagnóstico, de graça |
| **Escopo** | Orçamento sob consulta, escopo elástico | Preço público, escopo fechado, 10 dias úteis |
| **Promessa** | "Primeiro lugar no Google/ChatGPT" | Nenhuma promessa de posição. Promessa de construção + medição |
| **Handoff** | Cliente fica refém da agência | Kit que ele opera sozinho; recorrência é opcional, não amarra |

O item mais forte é a **honestidade prévia** — vem direto do vetor de ataque da sua Terceira Camada: *"a razão de escolha vira 'ele me disse a verdade antes de cobrar'"*. Num mercado envenenado por agência que promete e não entrega (sua Dor 3, FI 18), o único posicionamento sem concorrência é o do sujeito que diz "não vale a pena pra você" e vai embora.

---

## 5. Preço e escada

### O SKU

| Item | Preço | Prazo | Margem `[I]` |
|---|---|---|---|
| **Raio-X (isca)** | R$ 0 | 20 min | — |
| **Laudo Completo** (avulso) | R$ 690 | 48h | ~90% |
| **PRIMEIRA RESPOSTA** (produto principal) | **R$ 4.900** | 10 dias úteis | ~75% |
| **Manutenção de Visibilidade** | **R$ 690/mês** — mín. 6 meses | mensal | ~80% |
| Domínio + hospedagem (repasse) | ~R$ 60/mês | — | 0% (transparente) |

**Condição de pagamento:** 50% na assinatura, 50% na entrega do Bloco B. Sem parcelamento longo — projeto de 10 dias não comporta risco de inadimplência de 6 meses.

**Se o cliente já tem site que presta:** desconto de R$ 900 (vira reestruturação, não construção). Se o site é Wix travado ou não tem acesso, sem desconto — refazer é mais barato que consertar.

### Por que R$ 4.900

- **Acima** do freelancer de site (R$ 800–2.500) por margem larga o suficiente para não ser comparável — se estivesse em R$ 2.500 seria comparado, e perderia
- **Abaixo** dos R$ 5.000 psicológicos, que é onde o comerciante local pede prazo e some
- **Dentro** do gap que seu próprio plano NUCLEO documentou: *"território de R$ 1k–5k para PME está aberto"*
- Compatível com a escada da GEO Brand Intelligence (Sprint R$ 2,5–4,5k), com o site somado por cima

### Contradição a resolver `[!]`
O retainer de R$ 690/mês **viola o anti-padrão da Nexum Visible** (*"nunca abaixo de R$ 2.000/mês"*). A regra continua válida — **para o público dela** (advogado/escritório B2B, ticket de setup R$ 8k). Comércio local não paga R$ 2.000/mês por visibilidade e não deveria. São públicos diferentes.

**Decisão necessária sua:** ou você aceita que a regra dos R$ 2.000 é específica da Nexum Visible e este SKU tem outra régua, ou você mata o recorrente daqui e vende só o projeto. Não dá para manter as duas coisas escritas em documentos ativos sem escolher.

### Economia do produto

Com 3 clientes projeto + 3 recorrentes: **R$ 14.700 + R$ 2.070 = R$ 16.770** no mês de pico.
Custo direto: Promptado R$ 199/mês + hospedagem + eventual redator. Pessoa executora: ver §7.

---

## 6. Argumentos de venda

### 6.1 O pitch de 40 segundos (para a abordagem ativa)

> "Posso te mostrar uma coisa de trinta segundos? Eu perguntei pro ChatGPT qual a melhor [categoria] aqui [no bairro]. Ó a resposta. [mostra a tela] Aparece [concorrente], aparece [concorrente], e o seu nome não tá aqui. Isso não é o Google — é a IA, e é onde tá indo a pesquisa de quem ainda não te conhece. Eu faço exatamente isso: fazer você ser o nome que aparece aí. Quer que eu te mande o raio-x completo do seu caso? É de graça, sai amanhã, e se eu ver que não vale a pena pra você eu te falo."

Por que funciona: abre com prova, não com pergunta. Não pede nada. Termina oferecendo a possibilidade de o próprio vendedor dizer não — que é o gancho de confiança.

### 6.2 As sete provas (usar uma, não sete)

| # | Argumento | Dado |
|---|---|---|
| 1 | A pesquisa mudou de lugar | 60% das buscas no Google terminam sem clique; **77% no celular** `[V]` doc GEO 04/03 |
| 2 | Quem rankeava está perdendo | Queda de **58% no CTR** dos primeiros colocados após AI Overviews `[V]` Ahrefs, via plano NUCLEO |
| 3 | Site otimizado pro Google não serve pra IA | 62% de quem domina SEO é invisível nas IAs `[V]` GEO Brand Intelligence |
| 4 | Isso tem método, não é sorte | Citação inline +30% · estatística +30% · **quote de especialista +41%** `[V]` pesquisa Princeton, via NUCLEO |
| 5 | Marca pequena precisa de ajuda estrutural | Marca global é citada em 73% das respostas; **marca de nicho, em 11%** `[V]` doc GEMINI |
| 6 | A janela fecha | Vantagem de conteúdo/GEO tem meia-vida de **12–24 meses** `[I]` Terceira Camada |
| 7 | Você não vai ter que confiar em mim | Antes e depois, mesmas perguntas, mesmas IAs, print e data |

**Regra:** um argumento por conversa. Sete provas em sequência é discurso de vendedor, e mata a credibilidade que a prova visual acabou de construir.

### 6.3 Objeções — respostas prontas

| Objeção | Resposta |
|---|---|
| *"Já tenho site."* | "Ótimo — não vou refazer por refazer. Deixa eu rodar o raio-x. Se seu site já está sendo citado, eu te falo e não te vendo nada." |
| *"Pago R$ 200 pro rapaz que cuida do meu site."* | "E ele cuida bem. Isso aqui é outra coisa — ele faz seu site funcionar, eu faço a IA te citar. São camadas diferentes; a maioria dos sites bons não é citada." |
| *"Isso funciona mesmo?"* | "Em parte. Eu construo o que aumenta a chance de ser citado, e meço. O que eu não faço é prometer posição — quem promete tá mentindo, porque o ChatGPT é de terceiro e muda sem avisar. Por isso a medição." |
| *"R$ 4.900 tá caro."* | "Comparado a site, tá. Comparado a um mês de anúncio pago que para de existir quando você para de pagar, é barato. E vem com o laudo — você vai saber se funcionou." |
| *"Vou pensar."* | "Claro. Deixa eu te mandar o raio-x de graça enquanto isso — aí você pensa com dado na mão, não com meu papo." |
| *"Meu sobrinho faz site."* | "Faz mesmo, e provavelmente bem. Pergunta pra ele se ele mexe com schema JSON-LD e llms.txt. Se ele mexer, contrata ele — sério. Se ele não souber o que é, o site vai ficar bonito e invisível pra IA." |
| *"E se não funcionar?"* | "Aí o laudo de 60 dias vai mostrar que não funcionou, e eu vou ter te dito isso por escrito. É o único jeito honesto de vender isso." |

### 6.4 O que NUNCA dizer
- "Primeiro lugar no ChatGPT" / "garanto que você vai aparecer"
- "GEO", "AIO", "AEO", "schema", "LLM" no primeiro contato — só depois do cliente já ter concordado com o diagnóstico
- "Vamos dobrar seu faturamento"
- Qualquer número de resultado que não venha de medição do próprio cliente

---

## 7. Operação — quem faz o quê

### 7.1 A divisão

| Etapa | Quem | Tempo | Delegável hoje? |
|---|---|---|---|
| Montar lista de alvos do bairro | Pessoa | 2h (uma vez, 40 alvos) | ✅ |
| Rodar o Raio-X (5 perguntas, 4 IAs) | Pessoa | 20 min/alvo | ✅ |
| Abordagem + pitch | Pessoa | 15 min/alvo | ✅ |
| **Gate de aceite — este cliente tem chance?** | **Rodrigo** | **10 min** | ❌ ver 7.2 |
| Laudo Completo (20 perguntas × 4 IAs) | Pessoa | 2h | ✅ com a skill |
| Coleta de conteúdo com o cliente | Pessoa | 1h30 | ✅ |
| Redação das páginas-fonte | Pessoa | 4h | ⚠️ com o Kit + revisão |
| Montagem do site no template | Pessoa | 3h | ✅ |
| **Camada técnica (schema, llms.txt, robots, perf.)** | **Rodrigo** | **45 min** | ❌ ver 7.2 |
| **Revisão final antes de publicar** | **Rodrigo** | **20 min** | ❌ |
| Identidade canônica + replicação | Pessoa | 2h | ✅ |
| Kit de Marketing (do template) | Pessoa | 1h | ✅ |
| Entrega ao cliente | Pessoa | 1h | ✅ |
| Laudo de Saída (dia 60) | Pessoa | 1h30 | ✅ |

**Total pessoa:** ~19h por unidade entregue · **Total Rodrigo:** **1h15 por unidade** — dentro do cap de 2h da Parte 2.

### 7.2 Por que essas três etapas não são delegáveis ainda

1. **Gate de aceite** — recusar cliente sem chance é o coração do posicionamento e o que protege o canal (critério C8). Errar aqui queima o bairro inteiro. Delegável **depois** de 5 casos, quando existir um critério escrito calibrado em casos reais.
2. **Camada técnica** — sua própria decisão registrada na Nexum Visible: *"Schema/JSON-LD permanece com Rodrigo (diferencial técnico)"*. Delegável quando virar script ou checklist verificável.
3. **Revisão final** — enquanto não houver histórico, publicar errado é irreversível na frente do cliente.

### 7.3 Remuneração da pessoa executora `[?]` — decisão sua

Três modelos, com o trade-off:

| Modelo | Como | A favor | Contra |
|---|---|---|---|
| **Comissão pura** | 25–30% do projeto (R$ 1.225–1.470) + 20% do recorrente | Custo zero se não vender | Ela banca 19h de risco; rotatividade alta |
| **Fixo + comissão** (recomendado) | R$ 800/mês + 15% (R$ 735/unidade) | Segura a pessoa nos 2 primeiros meses, que é onde tudo morre | Custo fixo antes de receita |
| **Por entrega** | R$ 1.200 por unidade concluída | Simples, previsível | Não incentiva prospecção, só execução |

Com o modelo recomendado e 3 unidades/mês: custo da pessoa R$ 3.005, receita R$ 14.700, **margem líquida ~76%**.

---

## 8. O motor de prospecção ativa

Isto responde ao *"pode rodar de forma ativa, entrando em contato e propondo"*.

### 8.1 Como a lista é montada

Filtro em 4 camadas sobre o bairro-alvo:

1. **Tem site?** Sem site → fora da fase 1 (ciclo de venda longo demais). Com site → entra
2. **Paga por presença digital?** Rodar "site:instagram.com [nome]" com post patrocinado, ou olhar se aparece em Google Ads. Paga → prioridade máxima
3. **Categoria tem pergunta?** O consumidor pergunta antes de escolher? Clínica, pet shop, restaurante, academia, imobiliária, escola, oficina → sim. Loja de conveniência, banca → não
4. **Lista de exclusão:** advogado/escritório (→ Nexum Visible) · concorrente direto de cliente já ativo

Meta: **40 alvos qualificados** por bairro.

### 8.2 A sequência ativa

```
D+0   Raio-X gratuito (5 perguntas × 4 IAs, 20 min) — sem avisar o alvo
D+1   Abordagem presencial ou WhatsApp com o print. Pitch de 40s.
      → Interessado: agenda o Laudo Completo (48h)
      → Não: registra motivo, sai da lista por 6 meses
D+3   Entrega do Laudo. Aqui a proposta aparece — nunca antes.
D+5   Follow-up único. Um. Não existe segundo.
D+10  Se não fechou: entra na lista de reaquecimento (90 dias)
```

**Taxa esperada `[E]` — não medida, calibrar após os 20 primeiros:**
40 alvos → 20 Raio-X entregues → 6 aceitam o Laudo → 2–3 fecham. Ciclo de 10–15 dias.

### 8.3 O ativo que se acumula

Cada Raio-X rodado é permanente. Depois de 40, você tem o **mapa de visibilidade em IA do bairro inteiro** — quem é citado, quem não é, por qual pergunta. Isso é:
- Argumento de venda para os 34 que não fecharam ("o mapa do seu bairro mudou, olha aqui")
- Base de conteúdo pública ("Estudo: quem a IA recomenda na Aldeota")
- E o conteúdo público é ele próprio otimizado para GEO — o produto vendendo o produto

---

## 9. Stack

| Função | Ferramenta | Status |
|---|---|---|
| Diagnóstico e otimização de conteúdo | Skill `geo-otimizacao-conteudo` | ✅ existe, 5 camadas |
| Gate OAB (se algum dia atender advogado) | Skill `geo-juridico` | ✅ existe |
| Teste nas 4 IAs | Manual, prompts padronizados | ✅ prompts já escritos na GEO Brand Intelligence |
| Relatório visual | Gamma | ✅ decidido |
| Monitoramento recorrente | Promptado R$ 199/mês | ✅ decidido |
| Site | Template próprio — **a construir** | ❌ **é a única peça de engenharia real que falta** |
| Automação do teste (motor Python) | — | ❌ **não existe** (Parte 0, §0.4) |

**A peça crítica é o template.** Ele é o que transforma "10 dias" de promessa em realidade. Sem template, cada site é artesanal e o produto não é produto. Construir uma vez, usar em todas as unidades. Estimativa `[I]`: 12–16h para a v1, com HTML estático + os blocos de schema parametrizados.

O motor Python, se for construído, deve automatizar **o Raio-X** (rodar N perguntas em N IAs e tabular) — porque é a tarefa mais repetida do produto: 20 min × 40 alvos × cada bairro. Mas **não é bloqueante**: dá para vender e entregar as 3 primeiras unidades 100% manual.

---

## 10. As 3 primeiras unidades — como escolher

Você falou em "montar os três primeiros sites". A escolha deles decide se o produto pega ou morre:

| Unidade | Perfil | Objetivo | Preço |
|---|---|---|---|
| **#1 — Caso zero** | Alguém que você já conhece e confia, na categoria certa | Cronometrar o processo real, achar onde trava, gerar o antes/depois | R$ 0 ou custo, **em troca de uso público do resultado, por escrito** |
| **#2 — Primeiro pago** | Alvo da prospecção fria, categoria diferente da #1 | Validar que o pitch funciona com desconhecido | R$ 4.900 cheio |
| **#3 — Teste de handoff** | Qualquer um do funil | **A pessoa conduz sozinha** a parte comercial; você só faz os 3 gates | R$ 4.900 cheio |

Categorias diferentes nas três, de propósito: gera três cases setoriais em vez de um, e testa se o template aguenta variação.

**A #1 não é favor — é o laboratório.** É onde as 19h estimadas viram tempo real medido, e onde você descobre o que o Kit precisa ter antes de ser entregue a um cliente pagante.
