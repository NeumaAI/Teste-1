# CRIVO UNIFICADO v2 — Alongamento de Dívida Rural por Seca (MCR 2.6.4)

**Objeto:** RG-JUR-010 / RG-JUR-CAL-01 — Alongamento (prorrogação) de dívida de
crédito rural por frustração de safra, MCR 2.6.4.
**Onda:** 1 (Crédito Rural).
**Data:** 17/08/2026 · **Fases rodadas:** 1 a 6, completas.

## Fontes desta avaliação

| Fonte | O que forneceu | Classificação |
|---|---|---|
| `matriz-teses-juridicas-legaltech.md` (Drive, 17/08/2026) | Os 13 critérios da Fase 2 + ranking Top 15 de 94 teses | [VERIFICADO - documento datado] |
| RG de Teses (Notion, data source `6d965adf…`) | Cards RG-JUR-010 e RG-JUR-CAL-01 na íntegra + 35 cards de crédito rural / previdenciário / flag CEF | [VERIFICADO - card do RAG] |
| BACEN / gov.br / imprensa setorial (busca 17/08/2026) | Res. CMN 5.120/2024, **Res. CMN 5.314/2026**, Res. CMN 5.330/2026, MP 1.376/2026 | ver ressalva abaixo |

**Ressalva de fonte, e ela importa:** o achado mais grave desta avaliação (Res. CMN
5.314/2026) chegou por **portais setoriais e blogs de escritório**, não por leitura
da íntegra no BACEN. Pela sua própria regra, isso é [INFERÊNCIA - de reportagem],
não [VERIFICADO]. E há conflito de interesse declarado nas duas pontas:

- `cooperativismodecredito.coop.br` e `lawletter.com.br` — leem a norma como
  **discricionariedade do banco**. São a voz do credor.
- `agrolei.com` e `agroemdia.com.br` — leem a mesma norma como **retrocesso
  ilegal e inconstitucional**. São a voz do produtor, e concorrentes diretos no
  nicho agrarista.

Nenhum dos dois lados é fonte primária. A íntegra da 5.314/2026 é a Verificação
Barata nº 1 da Fase 6, e é ela que decide se esta tese existe na forma desenhada.

---

# ACHADOS DE INTEGRIDADE DO RAG (antes dos gates)

Três problemas encontrados no próprio RG de Teses. Não são detalhe: dois deles
alteram números que você usaria em material externo.

### 1. A mesma tese existe em dois cards, com dados que se contradizem

| Campo | RG-JUR-010 | RG-JUR-CAL-01 |
|---|---|---|
| Título | Alongamento de Dívida Rural por Seca (MCR 2.6.4) | Alongamento Compulsório — MCR 2.6.4 + Frustração de Safra |
| Score técnico | **88** | **81,5** |
| Confiança | **A** | **B** |
| Ticket | R$800–2.500 fixo ou 15–25% das parcelas | **Setup R$3.000–7.000** + 3–5% do montante |
| Teto declarado | R$4–10k/mês (5 casos) | **R$18–44k/mês** (4 casos) |
| Tratamento da CEF | *"Filtro absoluto: qualquer participação CEF = recusa imediata"* | *"Flag CEF: VERIFICAR — CEF opera PRONAF"* |
| Tags | **nenhuma** | agro, agro-NE, crédito-rural, CEF-insider, extrajudicial… |

[VERIFICADO - query direta no data source, 17/08/2026]. O card CAL-01 diz ter
absorvido o RG-JUR-MN-002; o RG-JUR-010 diz que vai fundir o RG-JUR-006. Nenhum
dos dois menciona o outro. **São quatro cards para uma tese.**

Consequência prática: o "score 88" que aparece em 2º lugar na Matriz e o "81,5" do
card unificado são a mesma tese com dois cálculos. O próprio CAL-01 já registra
esse tipo de problema: *"RG-JUR-MN-002 citava 'score 95 em análise adversarial
anterior' sem o campo formal preenchido — Rodrigo precisa localizar essa análise e
reconciliar antes de usar o número em qualquer material externo."* O alerta estava
escrito e continua valendo, agora em triplicado.

### 2. A convenção de ID quebrou

IDs duplicados encontrados numa única consulta [VERIFICADO - query]:
`RG-JUR-025` aparece **3 vezes** (Encargos de Mora / Pensão por Morte Rural /
Vícios Construtivos FAR) · `RG-JUR-026`, `RG-JUR-027`, `RG-JUR-028`, `RG-JUR-031`,
`RG-JUR-034` aparecem **2 vezes cada**, com teses diferentes. A Matriz lista
`RG-JUR-013` como "Bureau Revisional CCR" no ranking **e** como "Vínculo
Uber/iFood — morta" na lista de exclusões. São teses distintas com o mesmo ID.

Isso não é cosmético: a Matriz rankeia por ID. Qualquer referência a "RG-JUR-025"
num contrato, proposta ou handoff para a irmã é ambígua hoje.

### 3. O Próximo Passo desta tese está vencido há três meses

O card CAL-01 declara: *"SICOR Open Data CE (prazo: 7 dias a partir de
13/05/2026)"* [VERIFICADO - card]. Hoje é 17/08/2026. **Passaram-se 96 dias.** A
consulta que decidiria se existe volume nunca foi feita — e é a mesma consulta que
validaria o ticket.

---

# EFEITO DA SUA DECISÃO SOBRE A CEF (17/08/2026)

Pela regra que você fixou — CEF sinaliza, não trava — o volume destravado é muito
maior do que a Matriz sugeria.

**A Matriz dizia:** *"5 das 15 teses do top ranking têm Flag Conflito… listei as 5
marcadas com ⚠️ para você decidir caso a caso."*

**O RG diz:** numa consulta restrita a `Tipo: juridica` cruzada com crédito rural,
previdenciário ou flag ligada, **26 de 35 cards têm `Flag Conflito = __YES__`**
[VERIFICADO - query, 17/08/2026]. Não 5. Vinte e seis.

Desses 26, cerca de **13 são de crédito rural — Onda 1** — e a maioria carrega no
campo Adversário uma instrução de bloqueio operacional: *"VERIFICAR CEF caso a
caso antes de qualquer contato"* (MN-002), *"ALERTA CEF ALTO… verificar
obrigatoriamente antes de qualquer ação"* (MN-003), *"VERIFICAR se CEF é agente
financeiro"* (RURAL-01, RURAL-03, RURAL-11, RURAL-08, 026, 031).

**O que sua decisão fez:** apagou uma etapa de verificação obrigatória que estava
escrita na frente de 13 teses da sua onda ativa. Não é que elas ficaram melhores —
é que pararam de ter um pedágio antes do primeiro passo.

**Consequências específicas, todas [VERIFICADO - card]:**

| Tese | Antes | Agora |
|---|---|---|
| RG-JUR-023 — Cópia do Contrato (Q7), score 90/98, `producao` | GO travado por ⚠️ "precisa confirmar com você" | **GO limpo.** É o desbloqueador em cascata de T2, T3, T6, T8 |
| RG-JUR-030 — Negativação Pós-Quitação (T5), 85/95 | CONDICIONADO | **GO.** Triagem 100% automatizável, captação custo zero |
| RG-JUR-025 — Encargos na Mora da Construtora (T2), 80/95 | CONDICIONADO | **GO** |
| RG-JUR-028 — Escrituração FAR (T3), 72/88, `wip-ativo` | flag ligada | segue, sem pedágio |
| RG-JUR-CAL-01 — esta tese | "VERIFICAR se CEF é o agente" | verificação abolida |
| +13 de crédito rural com "VERIFICAR caso a caso" | pedágio por caso | pedágio removido |

**Ressalva honesta, uma só:** RG-JUR-023, 030, 025, 028, 024, 026, 027 e 022 são
**habitacional/FAR-MCMV** [VERIFICADO - Tags]. Elas não estão em Onda 1 nem em
Onda 2. Destravadas quanto à CEF, sim — mas param no Portão T6, não na CEF. A #1
do seu ranking geral é uma tese habitacional; a fila T6 continua sendo crédito
rural e previdenciário rural.

---

# FASE 1 — GATES DE ELIMINAÇÃO

## GATE 0 — COMPLIANCE → PASSA, com uma correção obrigatória de canal

**a) CEF em algum polo?** Sinalizado, sem efeito de gate (regra de 17/08/2026).
O card RG-JUR-010 declara adversário *"BNB, Banco do Brasil, Sicoob, Sicredi,
cooperativas de crédito NE. NUNCA CEF"* [VERIFICADO - card]; o CAL-01 declara
*"CEF opera PRONAF — verificar"* [VERIFICADO - card]. Pela nova regra: se a
operação for CEF, a peça é assinada pela irmã ou por parceiro, e Rodrigo fica na
camada técnica. Nenhum caso é recusado por isso.

**A linha que precisa sair do card RG-JUR-010:** *"Filtro absoluto: CCR com
qualquer participação da CEF (emissão, cessão, aval, garantia) = recusa
imediata."* Esse filtro está no campo Risco Grave e contradiz sua decisão de hoje.
Enquanto estiver lá, um executor lendo o card vai recusar caso bom.

**b) Atividade-FIM ou MEIO?** **As duas, em camadas separadas — e isso é o desenho
correto, não uma ambiguidade.**
- Dossiê de elegibilidade, leitura de enquadramento (recursos controlados vs.
  livres), planilha de fluxo de caixa, triagem por IA → **MEIO**.
- Notificação extrajudicial fundamentada protocolada na agência → **FIM**
  (consultoria/assessoria jurídica, Lei 8.906/94 art. 1º, II), dentro da sua
  autorização formal para extrajudicial e administrativo.
- Ação declaratória ou embargos à execução, se o banco negar → **FIM judicial**,
  irmã ou parceiro. [VERIFICADO - card CAL-01, campo Entrega]

**c) Provimento OAB 205/2021 → FERE, na forma escrita no card. Correção
obrigatória.**

O campo Aquisição do CAL-01 descreve: *"Python scraper DOU × SICOR inadimplências
PRONAF × **WhatsApp Evolution API**. CAC ≈ R$0 por lead. Volume estimado 30–50
leads/semana"* [VERIFICADO - card]. Isso é **outbound direto a pessoa física
identificada por situação de inadimplência** — exatamente o que o Provimento
205/2021 veda.

Não é detalhe de execução. É o motor de captação inteiro da tese como escrita.

**Alternativas, na ordem em que eu recomendaria:**
1. **Canal institucional** — o mesmo pipeline DOU × SICOR roda, mas a saída é uma
   lista de **municípios e agentes financeiros**, entregue a STR / FETRAECE /
   EMATERCE, que convocam os próprios associados. O dado orienta onde ir; o
   sindicato faz o contato. Compatível com o Provimento e mais forte que o
   WhatsApp frio, porque chega avalizado.
2. **Conteúdo informativo** — cartilha e áudio de WhatsApp sobre o direito à
   prorrogação, distribuídos *pelo* sindicato, sem menção a captação.
3. **Captação via empresa de tecnologia parceira** — a Nexum.AI opera o pipeline
   como serviço de dados para o sindicato ou para outro advogado; a relação com o
   produtor nunca nasce de contato seu.

**d) Dado pessoal sensível?** Não sensível no sentido do art. 5º, II da LGPD.
Mas o cruzamento é agressivo: **Datajud** dá nome de executado em CCR, **SICOR**
dá inadimplência por município e agente. Nome + inadimplência é dado pessoal comum
de alta lesividade.
Base legal: **art. 7º, IX (legítimo interesse)**, reforçada pela publicidade dos
atos processuais para a parte Datajud — [INFERÊNCIA - de Lei 13.709/2018, arts. 7º
IX e 10]. Exige teste de proporcionalidade documentado e canal de oposição. E
observe: legítimo interesse **não** sana o problema do item (c) — LGPD e
Provimento 205 são travas independentes.

> **GATE 0: PASSA**, condicionado à troca do canal de outbound direto por canal
> institucional. Sem essa troca, a tese é inexecutável por Rodrigo — não por
> mérito, por captação.

## GATE 1 — PORTÃO T6 → **PASSA**

Onda 1, Crédito Rural, MCR/PROAGRO/renegociação. Núcleo exato.
[VERIFICADO - Tags do card CAL-01: `agro`, `agro-NE`, `crédito-rural`]

## GATE 2 — RAZÃO DE ESCOLHA → **(b) ALGUÉM DE CONFIANÇA INDICOU**

> *"Este cliente contrata Rodrigo em vez de outro porque **o presidente do
> sindicato disse que ele é quem entende do assunto — e porque ele olhou meu
> contrato e viu uma coisa que o gerente não me falou.**"*

**(b) principal, com (c) como razão de conversão.** E há uma nota importante aqui:
o card foi desenhado apostando em **(a) CHEGUEI PRIMEIRO** — *"monitoramento DOU +
cruzamento SNCR identifica produtor afetado em 48h após decreto; janela de
captação pré-negativação de 15–30 dias que nenhum concorrente usa"* [VERIFICADO -
card, campo Notas].

Essa aposta é boa e o mecanismo funciona. **Mas o Gate 0(c) acabou de bloquear a
forma de exercê-la** — chegar primeiro a uma pessoa física por WhatsApp é vedado.
Então "cheguei primeiro" deixa de ser razão de escolha do cliente e passa a ser
**vantagem de roteamento interno**: você chega primeiro *ao sindicato*, com a
lista, e o sindicato chega ao produtor. A razão que o cliente sente continua sendo
a indicação.

Não é "porque apareço na busca" nem "porque cobro menos". Gate 2 passa.

## GATE 3 — SAÍDA GRATUITA → **EXISTE, e o bloqueio estrutural está nomeado**

**O caminho gratuito é real e não é obscuro:** o produtor pede a prorrogação
direto na agência, sem advogado, sem custo. STR e EMATERCE ajudam com papelada de
graça. O MCR não exige advogado em nenhum ponto.

**Os quatro bloqueios que criam o cliente pagante:**

1. **Instrução técnica deficiente.** O MCR 2.6.4 exige, cumulativamente:
   comprovação de dificuldade temporária por causa externa, **atestado de
   necessidade pela própria instituição financeira com base em análise técnica**,
   e demonstração de capacidade de pagamento [INFERÊNCIA - de reportagem sobre o
   MCR; a íntegra é a Verificação 1]. Pedido sem laudo e sem fluxo de caixa é
   negado. O card afirma que isso *"derruba 90% dos pedidos mal instruídos"* —
   número **sem fonte**, ver C11.
2. **Laudo agronômico.** Exige agrônomo habilitado (R$300–500). O produtor não
   produz isso sozinho. [VERIFICADO - card, campo Risco Grave]
3. **Prazo perdido.** *"Pedido pós-vencimento tem jurisprudência restritiva —
   priorizar casos pré-vencimento"* [VERIFICADO - card]. O produtor procura ajuda
   *depois* de vencer. Quem chega antes do vencimento tem outro caso nas mãos.
4. **O banco não comunica proativamente.** [VERIFICADO - card CAL-01, Hipótese]

Bloqueio nomeado, e é ele que define o cliente: **não é quem tem o direito, é quem
já foi negado ou está a menos de 30 dias de vencer sem laudo.**

## GATE 4 — TESTE DO DINHEIRO → **REPROVA como B2C · RECLASSIFICADA para B2B**

Este é o gate que muda a tese, e não tem como amaciar.

**O cliente não recebe dinheiro.** Alongamento **adia parcela** — preserva o bem,
evita negativação, libera fluxo de caixa. Não entra um real na mão dele. É
economia, não recebimento.

**E o público é o pior possível para setup fee:** produtor PRONAF **inadimplente
por seca**, saldo médio declarado R$30–80k [VERIFICADO - card CAL-01, marcado no
próprio card como *"[INFERÊNCIA — saldo médio estimado, verificar SICOR]"*]. Um
inadimplente por quebra de safra é, por definição, alguém sem caixa. O CAL-01
propõe cobrar dele **setup de R$3.000–7.000**.

Isso não fecha. E a contradição já estava visível no RAG: o outro card da mesma
tese cobra R$800–2.500. A diferença entre os dois cards é de 3 a 4 vezes, e nenhum
dos dois foi testado num cliente real.

**Pela regra do Gate 4 — "só economiza + baixa renda → REPROVA ou reclassifique
como B2B" — reclassifico.** Três formas viáveis de pagador, em ordem de solidez:

1. **B2B parecerista/bureau** — Rodrigo vende dossiê técnico de elegibilidade +
   minuta fundamentada para **outro advogado** que atende o produtor. Pagador com
   caixa, sem fricção de convencimento. É o modelo do RG-JUR-011 e do RG-JUR-013,
   ambos já validados no seu portfólio.
2. **Pagador institucional** — o STR, a cooperativa ou a federação contrata o
   serviço para seus associados. Um contrato, N produtores, CAC zero.
3. **Êxito puro sobre montante alongado** — elimina a barreira de entrada, mas
   cobrar percentual sobre dinheiro que **não entrou** é frágil na prática e na
   execução do contrato.

> **FASE 1: PASSA para a Fase 2, com a tese reclassificada de B2C-extrajudicial
> para B2B/institucional, e com o canal de captação trocado.** A tese que sai da
> Fase 1 não é a tese que entrou.

---

# FASE 2 — OS 13 CRITÉRIOS DA MATRIZ

Aplicados **como estão escritos** em `matriz-teses-juridicas-legaltech.md`
[VERIFICADO - documento, 17/08/2026], já com a reclassificação B2B do Gate 4.

| # | Critério | Leitura | Classificação |
|---|---|---|---|
| 1 | **Vel. Caixa** (até o 1º honorário) | B2B: parecer pago à vista, ciclo de dias. B2C: setup de um inadimplente, ciclo indefinido. Meta declarada no card: 1 caso protocolado em 14 dias | [VERIFICADO - card] + [INFERÊNCIA - de B2B] |
| 2 | **Bagagem** | Insider MCR (lê 2.6.4 por dentro, identifica fonte de recursos), SICOR operacional, OAB, rede rural NE. Declarada no card | [VERIFICADO - card, Vantagem Assimétrica] |
| 3 | **Alcance/Capilaridade** | "60k+ produtores NE elegíveis (Res. CMN 5.120/2024)". **A 5.120 tinha prazo de solicitação até 30/06/2025** — vencido há 14 meses. O universo de hoje é desconhecido | [DECAY - 30/06/2025] |
| 4 | **Barreira de Entrada** | Não dá para protocolar amanhã: falta a consulta SICOR (vencida há 96 dias), falta agrônomo confirmado, falta ler a Res. 5.314/2026 | [VERIFICADO - card, Próximo Passo] |
| 5 | **Fricção com Cliente** | Sente a dor (execução, negativação) mas não nomeia o direito. Precisa educar. Média-alta no B2C, **baixa no B2B** — advogado já sabe o que é MCR 2.6.4 | [INFERÊNCIA - de card + C3] |
| 6 | **Potencial de Monetização** | Dois tetos incompatíveis no RAG: R$4–10k/mês vs R$18–44k/mês. Sem pagador definido, nenhum dos dois se sustenta | [ESPECULAÇÃO] |
| 7 | **Tempo × Retorno** | Extrajudicial com IA na triagem e na minuta: horas por caso baixas. O caro é o laudo, que é de terceiro | [INFERÊNCIA - de card, Mecanismo IA] |
| 8 | **Escala/Replicação** | **Serial de verdade.** DOU × SICOR × template de notificação. É o critério mais forte da tese | [VERIFICADO - card] |
| 9 | **Ticket Médio** | R$800–2.500 (010) vs R$3.000–7.000 + 3–5% (CAL-01). Contradição não resolvida, nenhum testado | [ESPECULAÇÃO] |
| 10 | **Investimento Inicial** | Laudo R$300–500/caso + pipeline Python. Baixo — o pipeline já é seu ativo [D] | [VERIFICADO - card] |
| 11 | **Tempo até 1ª receita** | B2B: imediato. B2C: só após deferimento, se houver êxito | [INFERÊNCIA] |
| 12 | **Dependência de Terceiros** | **Três, nenhuma confirmada:** EMATERCE (laudo), irmã (judicial), STR/FETRAECE (canal — agora o canal *principal*, após o Gate 0c) | [VERIFICADO - card, Próximo Passo: "contato EMATERCE", "contato FETRAECE" = ainda por fazer] |
| 13 | **Risco Jurídico/Regulatório** | **Res. CMN 5.314/2026** (o achado grave) + Provimento 205 (canal) + LGPD (Datajud nominal) | [INFERÊNCIA - de reportagem] + [DECAY - jun/2026] |

**Leitura dos 13:** a tese é forte exatamente onde o seu ativo [D] atua (8, 10, 2,
7) e fraca exatamente onde depende de gente e de dado que não foram buscados (3, 4,
6, 9, 12). Nenhum dos critérios fracos é caro de resolver — todos os cinco cabem
em menos de quatro horas somadas.

---

# FASE 3 — 5 CRITÉRIOS DE MERCADO

**M1 — DISPONIBILIDADE DO PAGADOR.**
No B2C: produtor inadimplente por seca, saldo R$30–80k, sem caixa. O ticket do
card **não pode ser usado como prova** — é a armadilha circular que você mesmo
nomeou. [ESPECULAÇÃO] — só teste real resolve, e o teste é uma ligação a um STR
perguntando quanto um associado pagaria hoje, não uma planilha.
No B2B: advogado agrarista paga R$800–2.500 por parecer — [INFERÊNCIA - de
RG-JUR-011, tese vizinha com o mesmo modelo, ticket declarado e Confiança A].

**M2 — SAÍDA GRATUITA.** Detalhada no Gate 3. O caminho gratuito existe, é
oficial e é o próprio balcão do banco. O que o torna insuficiente é que o MCR
condiciona o deferimento a **análise técnica da instituição financeira** e a
**atestado de capacidade de pagamento** [INFERÊNCIA - de reportagem sobre o MCR
2.6.4; íntegra pendente]. Ou seja: o pedido gratuito existe, mas o deferimento
não é automático — e é aí que mora o serviço.

**M3 — CONCORRÊNCIA.** Fase 5.

**M4 — GRAU DA DOR → CRISE AGUDA.** Vencimento a menos de 30 dias, execução em
curso, risco de penhora de bem rural, negativação. [VERIFICADO - card, campos Fato
Gerador e Aquisição: *"execuções CCR sem advogado no polo passivo, pré-leilão"*].
Converte rápido.
**Contraponto que a agudez esconde:** a dor aguda chega no momento errado. Quando
o produtor sente o suficiente para procurar advogado, já venceu — e o
pós-vencimento tem jurisprudência restritiva. A tese precisa do cliente **antes**
de ele sentir. Isso é dor aguda com janela invertida, e é raro.

**M5 — FACILIDADE DE ACHAR O CLIENTE.** O canal existe, é acessível e é barato:
STR, FETRAECE, EMATERCE, Garantia-Safra do MDA, cooperativas. Custo ≈ R$0 em
dinheiro [VERIFICADO - card, campo Aquisição]. O custo real é **presença física e
tempo de relação** — que é justamente o que 4h/dia limita. E nenhum desses
contatos foi feito: os dois primeiros itens do Próximo Passo do card RG-JUR-010
são *"contato EMATERCE"* e *"contato FETRAECE"*.

---

# FASE 4 — 13 CRITÉRIOS DE CAPTURA E MOAT

**C1 — JANELA DE CAPTURA.** Do decreto de calamidade ao vencimento: **15–30 dias**
[VERIFICADO - card, Notas]. Curta. Quem ocupa hoje: **o próprio banco**, que
oferece a renegociação dele — e essa é a oferta concorrente real, não outro
advogado. Janela curta e ocupada pelo credor. Pior combinação dos quatro cenários.

**C2 — FONTE DE CONFIANÇA: é PRODUTO ou CANAL?**
a) Intermediários: STR, FETRAECE, EMATERCE, cooperativas — todos dentro do seu
ativo [C], construído via CEF. Acesso real? **Plausível mas não testado** — nenhum
contato registrado. [ESPECULAÇÃO quanto ao acesso *hoje*]
b) **Teste obrigatório:** um concorrente com orçamento de marketing chegaria a
esses produtores amanhã? Ao produtor, sim — Facebook e rádio AM resolvem. **Ao
STR, não.** Confiança de sindicato rural no NE não se compra com verba; leva anos
e passa por pessoa. → **PRODUTO de rede.**
c) **Risco operacional que vem junto:** essa confiança se destrói rápido se o STR
perceber que virou canal de venda. Um caso perdido com barulho, ou uma cobrança
percebida como abusiva sobre associado quebrado, fecha o canal inteiro. Ver C8.

**C3 — ASSIMETRIA DE DIAGNÓSTICO → estado [2] SENTE MAS NÃO NOMEIA.**
O produtor sente a dívida com clareza absoluta. O que ele não sabe é que o MCR
2.6.4 existe e que o banco tinha o dever de analisar. Ganha quem educa; IA ajuda
médio. **Não é estado [3]** — logo, conteúdo informativo não é dinheiro jogado
fora, desde que distribuído pelo canal certo (áudio de WhatsApp via sindicato,
rádio local, reunião de associados), não por SEO.

**C4 — MEIA-VIDA DA VANTAGEM → MISTA, e é isso que define a estratégia.**
Teste: se virasse conhecimento público amanhã, o que sobra em 6 meses?
- **A tese jurídica: já é pública.** Guia prático de escritório concorrente,
  artigo de Jusbrasil, material da FAEC, parecer em Migalhas — tudo indexado hoje
  [VERIFICADO - busca 17/08/2026]. Meia-vida **zero**. Não é vantagem.
- **O pipeline DOU × SICOR × Datajud:** 6–18 meses, pela sua própria referência.
- **A rede STR/EMATERCE:** 3–5 anos.
- **O insider MCR:** não replicável.

**Erro a evitar, e ele está no card:** o card trata "insider lê MCR por dentro"
como o moat. Não é — o MCR é público e já tem guia prático de concorrente. O moat
é a **rede** e a **velocidade do dado**. Tratar a leitura do MCR como moat
permanente leva a subinvestir em velocidade, que é o único eixo em que a janela
está correndo.

**C5 — CUSTO MARGINAL DO SEGUNDO CASO.** A IA absorve triagem de elegibilidade,
cruzamento e minuta [VERIFICADO - card, Mecanismo IA]. Não absorve: laudo
agronômico (terceiro, por caso), conferência de enquadramento de recursos (você,
por caso), relação com o produtor. Caso 10 custa bem menos que o caso 1 — mas não
tende a zero. Contra 4h/dia e WIP=1: **teto realista de 4–5 casos/mês no modelo
B2C-FIM**; bem mais no B2B, porque o dossiê é o produto e o atendimento é do outro.

**C6 — DECISOR vs. SOFREDOR.**
B2C: a mesma pessoa. Simples e ruim — é o sofredor sem caixa.
B2B (recomendado): **decisor = advogado agrarista ou diretoria do STR; sofredor =
produtor.** Duas mensagens:
- Ao advogado: *"você recebe o dossiê de elegibilidade e a minuta fundamentada em
  48h; cobra o cliente como quiser."* Canal: OAB-CE, grupos de agraristas,
  indicação.
- Ao produtor: *"seu vencimento é dia X e você tem direito a pedir prorrogação
  antes disso."* Canal: sindicato, nunca contato direto seu.

**C7 — REINCIDÊNCIA → abre carteira, e é o critério mais subestimado da tese.**
One-shot por safra, mas recorrente por ciclo climático. E o mesmo produtor aciona,
depois: revisional de CCR (RG-JUR-002), PROAGRO negado por ZARC (RURAL-03),
penhora indevida de bem rural (026), superendividamento rural (RURAL-08), garantias
(RURAL-10) — e, na Onda 2, **aposentadoria rural e BPC rural** (BPC-002, 034), que
é o mesmo cliente, na mesma casa, pelo mesmo sindicato. [VERIFICADO - query no RG]
O primeiro caso não vale pelo ticket; vale pela carteira que abre.

**C8 — RISCO DE QUEIMAR O CANAL → ALTO, e subiu em junho de 2026.**
Taxa de insucesso esperada: **desconhecida e provavelmente maior do que o card
supõe**, porque a Res. 5.314/2026 reforça que o deferimento é faculdade do banco.
Dependência de canal por reputação: **total** — o STR é pessoal e insubstituível.
Insucesso alto × canal insubstituível = **o canal fecha**. Um escritório de
tráfego pago não corre esse risco; você corre.
Mitigação obrigatória: só aceitar caso **pré-vencimento e com laudo**, e dizer ao
sindicato, por escrito e antes, qual é a chance real.

**C9 — PROVA DE EXECUÇÃO (dois relógios).**
a) **Evidência:** barata e imediata. A consulta SICOR Open Data é gratuita e leva
   ~2h [VERIFICADO - card, com URL e filtros já escritos]. Um caso-piloto da
   própria rede via STR é o teste de campo.
b) **Dinheiro:** no B2B, semanas. No B2C, indefinido — depende de deferimento
   bancário agora discricionário.
Critério de sequenciamento: **prova rápida, caixa lenta no desenho original,
caixa rápida no desenho B2B.**

**C10 — INTERSEÇÃO RARA.** Três competências:
1. Ler MCR e identificar fonte de recursos (controlados vs. livres) por dentro;
2. Ser aceito por STR / EMATERCE / produtor no interior do NE;
3. Operar DOU + SICOR + Datajud com IA.
Quantos advogados no raio real (agraristas CE/NE) têm as três? **Quase ninguém** —
o card afirma *"advogados agraristas no NE operam alertamento artesanal, sem
pipeline DOU+SICOR; nenhum player identificado com captação proativa
automatizada"* [VERIFICADO - card, Análise Concorrência — mas é autoavaliação, não
levantamento; ver E2].
Custo de replicação **em anos**: 1 exige anos dentro de um banco público operando
crédito rural; 2 exige anos de relação; 3 exige meses. **Réplica realista: 3–5
anos**, e só por quem tiver as três trajetórias.

**C11 — MENSURABILIDADE DA VANTAGEM → em grande parte ALEGADA.**
Frase do card: *"Insider CEF: sabe ler MCR por dentro e identificar a fonte de
recursos — erro que derruba 90% dos pedidos mal instruídos."*
Retirando adjetivo e advérbio, sobra: **"identifica se a operação é de recursos
controlados ou livres, e esse enquadramento determina a regra de prorrogação
aplicável."** Isso é fato checável — mas **sem número**.
O "90%" é o número da frase e **não tem fonte em nenhum dos dois cards**.
[ESPECULAÇÃO]. Number que faltaria: taxa de deferimento de pedidos de prorrogação
instruídos com laudo vs. não instruídos. Ninguém publica isso; o proxy é a taxa de
êxito em ações de prorrogação no TRF5/JEF via Datajud.
Comparação com o padrão que você mesmo escreveu: *"identifico se o ZARC foi
verificado na proposta original em 5 minutos, e esse é o vício que derruba o
indeferimento"* — essa é a forma correta. A frase desta tese ainda não chegou lá.

**C12 — INVISIBILIDADE PARA O CONCORRENTE → o problema é VISÍVEL.**
Um advogado competente com Google e Jusbrasil formula isso **em uma tarde**. Prova:
existe guia prático publicado por escritório concorrente do nicho
(`gomesesalviano.com.br`, *"Prorrogação de dívidas rurais no MCR 2.6.4: guia
prático"* — **conflito de interesse: é concorrente direto da tese avaliada**),
artigo no Jusbrasil, material do Sistema FAEC/SENAR, parecer no Migalhas e análise
em portal de cooperativismo [VERIFICADO - busca 17/08/2026].
A vantagem **não está aqui**. Está no C10 e no C2.

**CRUZAMENTO C3 × C12 → cliente não sabe + concorrente formula fácil = CORRIDA,
JANELA CURTA.**
Terceiro dos quatro quadrantes. Não é moat máximo. É corrida — e o relógio já está
correndo para todo agrarista que perceber a mesma janela, o que ficou mais
provável depois que a Res. 5.314/2026 pôs o tema em pauta na imprensa setorial.

**C13 — PONTO ÚNICO DE FALHA → TRÊS, nenhum confirmado formalmente.**

| Pessoa/entidade | Para quê | Confirmou? | Substituto |
|---|---|---|---|
| **Agrônomo EMATERCE** | Laudo, sem o qual o pedido é negado | **Não** — é o item 1 do Próximo Passo | Agrônomo autônomo ou de cooperativa; dias, não meses |
| **STR / FETRAECE** | Canal — e passou a ser o canal *único* após o Gate 0(c) | **Não** — item 3 do Próximo Passo | Outros STRs, cooperativas, pastoral; meses de relação |
| **Irmã advogada** | Polo ativo judicial se o banco negar | **Não consta** confirmação formal | Parceiro externo; existe, mas muda a economia |

Risco crítico, e ele é do tipo mais barato de resolver: **três telefonemas.** Nenhum
investimento deve ser feito antes deles.

---

# FASE 5 — CONCORRÊNCIA EM 3 EIXOS

**E1 — DENSIDADE (concorrentes por mil casos/ano) → [REQUER VALIDAÇÃO].**
Não tenho o denominador. O único número de volume no RAG — 60k+ produtores
elegíveis — vem da Res. CMN 5.120/2024, cuja janela de solicitação venceu em
**30/06/2025** [DECAY]. O universo de hoje depende da Res. 5.330/2026 e da MP
1.376/2026, que são de julho passado e que eu não li na íntegra.
Numerador (quantos advogados) também não levantado. **Densidade: indeterminada.**
A consulta SICOR resolve o denominador; uma consulta Datajud por classe/assunto no
TRF5 e nas varas estaduais do CE resolve o numerador. As duas somam ~3h.

**E2 — QUALIDADE DA OFERTA INCUMBENTE ← é aqui que mora o espaço.**
O que o RAG afirma: incumbentes operam *"alertamento artesanal, sem pipeline
DOU+SICOR"*, *"nenhum player identificado com captação proativa automatizada"*,
*"gap de escala real"* [VERIFICADO - card, Análise Concorrência].
**Mas isso é autoavaliação, não levantamento.** Não há: taxa de êxito de
incumbente, tempo de resposta, reclamação pública, nem verificação de
especialização real. [ESPECULAÇÃO quanto à qualidade da oferta incumbente].
O que a busca mostrou é o oposto de vácuo: escritórios com **guia prático
publicado e indexado** sobre exatamente esta tese. Eles existem, produzem conteúdo
e ocupam a camada de descoberta. Se são bons na execução, ninguém mediu.
Mercado mal servido é hipótese, não achado — e é a hipótese mais valiosa a testar,
porque é ela que decide se há espaço.

**E3 — CAMADA DE DESCOBERTA DISPUTADA.**

| Camada | Quem ocupa | Rodrigo pode entrar? |
|---|---|---|
| SEO tradicional / Jusbrasil | Escritórios agraristas com guias publicados | Disputada, sem vantagem |
| GEO-IA | Ninguém identificado no nicho | Aberta — mas o cliente é estado [2] e não pergunta a IA |
| **Indicação institucional (STR/EMATERCE/cooperativa)** | **Artesanal e fragmentada** | **Sim — é o ativo [C]. É a camada certa.** |
| **Outbound de dados (DOU × SICOR × Datajud)** | **Ninguém, segundo o card** | **Sim, mas só como insumo do canal institucional** — contato direto a PF é vedado |
| Presença física (feira, reunião de associados, rádio) | Advogado local tradicional | Sim, e é onde a confiança se constrói — mas consome as 4h/dia |

**Princípios obrigatórios, aplicados:**
- Concorrência alta é sinal de mercado grande. Aqui ela é **média e visível** — há
  incumbentes produzindo conteúdo. Isso é bom sinal de dinheiro, e só vira
  barreira se eles forem bons, o que não foi medido (E2).
- **Não há vácuo total, e isso é alívio, não problema.** Onde eu vi vácuo — captação
  proativa por dado — o C12 explica que é por *acaso e imaturidade técnica do
  nicho*, não por acesso privilegiado. Vácuo frágil: fecha quando o primeiro
  agrarista contratar um dev.

---

# FASE 6 — SÍNTESE E DECISÃO

**1. RAZÃO DE ESCOLHA.** O sindicato em que ele confia disse que Rodrigo é quem
entende disso — e Rodrigo olhou o contrato e viu o enquadramento de recursos que o
gerente não explicou. *(Gate 2: (b), com (c) como conversão.)*

**2. TIPO DE MOAT → TEMPORÁRIO (corrida) no que gera volume, PERMANENTE (posição)
no que gera confiança.** A tese jurídica tem meia-vida zero — já é pública. O
pipeline de dados: 6–18 meses. A rede STR/EMATERCE: 3–5 anos. Você não escolhe
quando ocupar a parte que gera casos; nela, o relógio está correndo.

**3. QUADRANTE C3 × C12 → CORRIDA, JANELA CURTA.** Cliente não nomeia o direito,
concorrente formula a tese em uma tarde.

**4. QUADRO DE CONFIANÇA** — 47 células classificadas nas Fases 1 a 5:

| Classificação | Células | % |
|---|---|---|
| [VERIFICADO] (card do RAG, documento datado ou busca com fonte identificável) | 26 | 55% |
| [INFERÊNCIA] | 10 | 21% |
| [ESPECULAÇÃO] | 7 | 15% |
| [DECAY] | 4 | 9% |

**ESPECULAÇÃO em 15% — abaixo do limite de 40%.** A avaliação sustenta decisão.
**Mas leia onde a especulação caiu**, porque a distribuição importa mais que o
percentual: ticket, teto de receita, disponibilidade do pagador, acesso atual ao
canal e qualidade do incumbente. **Todos os cinco são o mesmo tipo de célula: o
que só um telefonema ou uma consulta resolve.** Não é especulação teórica — é
especulação por trabalho não feito.

**5. VANTAGEM ALEGADA vs. PROVADA (C11).**

| Passou (fato checável) | Não passou (alegação) |
|---|---|
| Identifica se a operação é de recursos controlados ou livres, e isso determina a regra aplicável | *"Erro que derruba **90%** dos pedidos mal instruídos"* — 90% sem fonte |
| Pipeline DOU → identificação do produtor afetado em 48h após decreto (mecanismo descrito, com URLs e filtros) | *"Único advogado NE com essa combinação"* — plausível, não levantado |
| MCR 2.6.4 exige laudo/análise técnica → pedido cru é negado | *"Nenhum player identificado com captação proativa"* — autoavaliação |
| Janela de 15–30 dias entre decreto e vencimento | *"Gap de escala real"* — adjetivo |

**6. O QUE MATA ESSA TESE.**
**A Resolução CMN 5.314/2026.** Segundo os relatos setoriais de junho/2026, ela
alterou o MCR para reforçar que a prorrogação é **faculdade da instituição
financeira, e não direito automático do produtor**, condicionando-a ao atestado de
capacidade de pagamento pelo próprio banco, que decide *"por sua conveniência"*
[INFERÊNCIA - de reportagem, jun/2026].

Se essa leitura prevalecer, o núcleo do card morre. A Hipótese registrada em
RG-JUR-010 é literalmente: *"tem **direito subjetivo** ao alongamento — direito
que **o banco é obrigado a deferir** quando os requisitos estão presentes"*
[VERIFICADO - card]. Isso deixa de ser verdade. A tese sai de **extrajudicial de
direito subjetivo** — barata, rápida, sua, dentro da sua autorização — e vira
**litígio de ilegalidade de resolução do CMN**: caro, longo, judicial, da irmã, com
teto de ticket maior e ciclo de anos. Outro produto, outro operador, outra
economia.

E existe controvérsia viva: há doutrina de junho/2026 sustentando *"retrocesso
normativo, vício de legalidade e inconstitucionalidade material"* e questionando
*"até onde o CMN pode limitar um direito assegurado ao produtor rural"*
[INFERÊNCIA - de reportagem; fontes do lado do produtor, conflito de interesse
declarado]. Ou seja: a tese não está morta — está **em disputa**, e o RAG não sabe
disso.

Isso é o achado central desta avaliação: **o card mais bem pontuado da sua Onda 1
está fundado numa premissa que a norma mudou dois meses atrás, e nenhum dos dois
cards registra a mudança.**

**7. O QUE A SALVA.** A interseção do C10 com o C2: **rede STR/EMATERCE (3–5 anos
para replicar) + leitura de enquadramento de recursos por dentro (não
replicável)**. Ninguém monta isso em 12 meses. Note que o que salva **não é a tese
jurídica** — essa é pública e replicável numa tarde. É o acesso e o diagnóstico.
E há um reforço estrutural: a Res. 5.330/2026 e a MP 1.376/2026 criaram, em
julho/2026, uma **linha nova de composição de dívidas rurais com prorrogação**
[INFERÊNCIA - de reportagem]. Norma de 30 dias, com ninguém instrumentado ainda.
Se houver janela, é aí — e o C4 diz que ela é curta.

**8. VERIFICAÇÕES BARATAS.** Três, somando **3h30**, e cada uma decide algo:

| # | Ação | Custo | O que decide |
|---|---|---|---|
| 1 | Ler a íntegra da **Res. CMN 5.314/2026** em `normativos.bcb.gov.br`, mais a **5.330/2026** e a **MP 1.376/2026** no Planalto | **1h** | Se a tese é administrativa (sua, barata) ou judicial (da irmã, longa). **Converte o item 6 de [INFERÊNCIA - reportagem] em [VERIFICADO]. É a mais importante das três** |
| 2 | Rodar a consulta **SICOR Open Data** já escrita no card: UF=CE, PRONAF/PRONAMP, inadimplente ou vencimento em 90 dias, contratação após 01/01/2022 | **2h** | Volume real hoje e saldo médio → mata a [ESPECULAÇÃO] de ticket e teto, e o [DECAY] do universo de 60k. É o Próximo Passo do próprio card, vencido há 96 dias |
| 3 | Ligar para **FETRAECE** e para um **agrônomo da EMATERCE** | **30 min** | Se os dois pontos únicos de falha existem, e se o STR pagaria pelo serviço (valida ou mata o modelo B2B do Gate 4) |

**9. DECISÃO → DORMENTE, com prazo de revisão de 7 dias.**

- **Nível de evidência: 2 de 5.** Estrutura e mecanismo verificados no RAG;
  fundamento normativo em disputa e não lido na fonte; pagador não definido;
  volume desconhecido; três dependências não confirmadas.
- **Risco principal:** a Res. CMN 5.314/2026 transformar a tese de extrajudicial
  em judicial, o que a tira das suas mãos e a joga num ciclo de anos.
- **Prazo de revisão: 24/08/2026.**

**DORMENTE aqui não significa "parada".** Significa: **3h30 de verificação
separam esta tese de um GO ou de um NO-GO limpo**, e nenhuma delas é caveira —
todas as três são leitura e telefone. Não classifico como GO porque seria
autorizar investimento sobre uma premissa normativa que mudou em junho e que eu
só conheço por reportagem. Não classifico como NO-GO porque o moat do C10 é real
e a Res. 5.330/2026 pode ter reaberto a janela na semana passada.

**10. SEQUENCIAMENTO → esta tese NÃO opera primeiro.** E a razão não é o score.

- **Por C9 (prova e caixa):** prova é barata aqui, mas o caixa depende de um
  pagador que o Gate 4 reprovou. Perde de qualquer tese B2B.
- **Por C6 (quem paga já fatura):** o pagador natural desta tese é um produtor
  inadimplente por quebra de safra. É o pior pagador do seu portfólio. As teses
  vizinhas **RG-JUR-011 (Parecerista Previdenciário Rural B2B**, Onda 2, ticket
  R$800–2.500 recorrente, vende para advogado**)** e **RG-JUR-013 (Bureau
  Revisional CCR**, Onda 1, R$1.500–8.000/laudo, irmã como executora, CAC zero**)**
  têm pagador que já fatura. [VERIFICADO - Matriz, itens 6 e 8]
- **Por C13 (ponto único de falha):** esta tese tem três não confirmados. O
  RG-JUR-011 não depende de laudo agronômico nem de canal institucional — vende
  direto para advogado.

**Ordem recomendada dentro das ondas ativas:** RG-JUR-011 (parecerista
previdenciário rural B2B) → RG-JUR-013 (bureau revisional CCR) → **esta tese, no
formato B2B/institucional**, depois das três verificações. Ela é boa como
**segunda** oferta ao mesmo canal, não como primeira: quando o STR já confia,
vender alongamento é fácil; usar alongamento para conquistar o STR é caro.

---

# FECHAMENTO — A AÇÃO FÍSICA

Uma, agora, de uma hora:

> **Abra `normativos.bcb.gov.br`, busque "Resolução CMN 5.314" e leia o
> dispositivo que altera o MCR 2.6.4. Depois anote uma frase no card RG-JUR-010:
> a prorrogação continua sendo direito subjetivo do produtor, ou virou faculdade
> do banco?**

Essa frase decide se a tese é sua ou da sua irmã, se é de 30 dias ou de 3 anos, e
se o ticket é de R$2.000 ou de R$20.000. Tudo o mais nesta avaliação — volume,
canal, ticket, sequência — depende dela e não deve ser mexido antes.
