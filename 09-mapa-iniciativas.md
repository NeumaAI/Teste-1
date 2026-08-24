# Mapa de Iniciativas por Prontidão × Maturidade

**Data:** 24/08/2026 · **Protocolo:** Prompt-Mestre v1.0, etapas E1→E5 executadas em passagem única
**Decisão de portão:** opção B (varredura literal + sinônimos). O RAG vetorial não existe nesta sessão; a substituição está declarada em [`08-e0-declaracao-cobertura.md`](08-e0-declaracao-cobertura.md).
**Correção da E0:** a fonte `CARDS` foi destravada durante a execução — o database `📋 RG de Teses` é acessível por SQL e contém **94 cards**. A E0 declarava essa fonte inacessível. A declaração estava errada e está corrigida aqui.

---

## 1. Painel de cobertura

| Fonte | Varrido | Não varrido |
|---|---|---|
| **Repo** `/home/user/Teste-1` | 11 arquivos, 2.760 linhas, integralmente | — |
| **Notion — páginas** | 8 consultas semânticas; 12 páginas abertas integralmente | o restante do workspace |
| **Notion — CARDS** (`RG de Teses`) | 94 cards, campos `Título/Status/Pipeline/Score/Confiança/Flag CEF/Aritmética/Entrega/Aquisição/Próximo Passo/Risco` | **corpo das páginas dos 94 cards** — li a linha da tabela, não o texto de cada card |
| **Google Drive** | busca `fullText`/`title`; metadado de ~10 arquivos | **conteúdo integral** — nenhum documento do Drive foi lido nesta sessão |
| **Skills** (`/root/.claude/skills/synced/`) | 79 skills listadas | conteúdo não lido |
| **RAG Pessoal local** (`C:\Users\rodri\OneDrive\…\PASTA_DAS_VERDADES_UNICAS`) | ❌ inacessível | **é a base integral da Auditoria de 13/08** — toda evidência sobre Aluminacle/Boi Fest é indireta |
| **Histórico de conversas** | ❌ não é base consultável por API | tudo |

**Consultas externas sem retorno utilizável (E4):** preço de ovino/cordeiro CE 2026 (CEPEA sem cotação recuperável); mercado B2B de parecer previdenciário terceirizado (o Código de Ética da OAB veda tabela pública de preço — a ausência é estrutural, não falha de busca).

---

## 2. Inventário consolidado (E1 + E2)

Uma linha por iniciativa. Toda linha tem âncora literal. Merges registrados.

| # | Iniciativa | Fonte (id) | Âncora literal (≤200c) |
|---|---|---|---|
| **N1** | Nexum Opera — Agente SDR white-label | Notion `3bb28fec…4a9048f5e60f95648a` | "status ativo, data início 10/03/2026, data receita 28/03/2026, stack Node/Express/OpenAI/Supabase/WhatsApp/Railway" |
| **N2** | Nexum Local — Presença Local Express | Notion `3c228fec…9492f4891527e0d1` (20/08) | "Beta: R$ 697 para os 3 primeiros clientes. Faixa inicial após cases: R$ 997." |
| **N3** | GEO / visibilidade em IAs *(família)* | repo `README.md` + Notion `33128fec…` | "Serviço GEO first para PMEs brasileiras — diagnóstico + execução de visibilidade em IAs (ChatGPT, Gemini, Perplexity) no ticket que PME consegue pagar" |
| **N4** | NBS — Nexum Brand System | Notion `33128fec…98a8f63881b4c8ae` | "criação de marca completa para PMEs … operado por executor júnior (filha) com supervisão mínima de Rodrigo (~1h por projeto)" |
| **N5** | Microprojetos Python white-label (8+6) | Notion `33128fec…98a8f63881b4c8ae` | "Catálogo de 8 microprojetos (Python + trilha M365) que reaproveitam o padrão técnico validado no CEOPE … vendáveis a qualquer PME" |
| **N6** | Diagnóstico de Governança de IA (escritórios) | Notion `35928fec…9c68daca8b663fe4` | "Dor escolhida: Governança de IA para escritórios pequenos/médios (Score FI 16). Ativo ~80% pronto: políticas do Bloco B do Blueprint (17/05) = pacote revendível" |
| **J1** | Escrituração FAR Pós-Quitação (T3) | CARDS `RG-JUR-028` | `Status: wip-ativo · Pipeline: producao · ST 72 · SF 88 · Flag CEF: SIM` — "Honorários fixos R$2.000 + 20% sobre dano moral médio R$7.000 = R$3.400/caso" |
| **J2** | Obrigação da CEF de fornecer cópia do contrato (Q7) | CARDS `RG-JUR-023` | `validada · producao · ST 90 · SF 98 · Flag CEF: SIM` — "Ticket menor (R$500–1.500 fixos). Mas é pré-requisito para T2, T3, T6, T8." |
| **J3** | Parecerista Previdenciário Rural B2B (B9) | CARDS `RG-JUR-011` + Notion `3be28fec…9c4cc3575b5944e0` §17 | "Ticket R$800–2.500/parecer … 5 advogados parceiros × 4 pareceres × R$1.500 médio = R$30k/mês no teto" · decisão 16/08: "Avançar / Bloqueio: Nenhum — pode operar" |
| **J4** | Aposentadoria Rural / Segurado Especial (B7) | CARDS `RG-JUR-034` + EstadoAtual §17 | "Porta B7 (atendimento direto): registrada, mas travada — falta parceiro judicial fechado para polo ativo no JEF Federal." |
| **J5** | Bureau Revisional CCR — laudo + recálculo BACEN | CARDS `RG-JUR-013` | `validada · ST 85 · Conf A` — "Ticket R$1.500–8.000/laudo … Modelo bureau + executor: Rodrigo produz, irmã/parceiro peticiona" |
| **J6** | FUNDEF/FUNDEB — herdeiros e excluídos | CARDS `RG-JUR-015` + EstadoAtual §17 | "Ticket R$3.000–15.000 por caso … 5 casos/mês = R$30k/mês" · bug: "nenhum tinha rubrica identificável — todos apareciam como já sacados no site da SEDUC" (N=50) |
| **A1** | Arquibancada Studio (paródia/hino/canto) | Notion `3be28fec…8a05dcba21e4ba91` | "Criado 15/08/2026 — RAG e instruções prontos … Serviço customizado US$25–5.000 (benchmark geral)" |
| **A2** | Luca DJ — música sob encomenda | Notion `3a228fec…994dc919edb0d1f6` | "RADAR — gaps de preço e intake não fechados, decisão binária pendente desde 19/07/2026 · R$ 97–197 por música" |
| **A3** | DeepDrift — canal faceless EN | Notion `38128fec…9ca2ca411a89756a` | "GO CONDICIONAL 62/100, aguardando gatilho (BPC caso #1) · AdSense + Spotify/Distrokid + Memberships — US$200–800/mês (ano 1)" |
| **T1** | Terreno Russega — ovinocultura (2 ha, Aquiraz) | Notion `35d28fec…a637f1e79f91af97` | "Meta discutida: R$ 5.000/mês líquidos com ovinocultura · Capacidade estimada: 70 animais em 2 ha com sistema forrageiro próprio" |
| **D1** | Produtos digitais de prompts | Notion `3bb28fec…4a9048f5e60f95648a` | "Ativo com biblioteca de prompts, guia, checklist e página de vendas." + "não há evidência de venda real" |

### Merges executados
- **N3** funde: `Nexum Visible` (Notion, 18/05) + `GEO — Nexum Brand Intelligence` (Notion, 16/04) + `Produto site GEO/AIO` (repo, 17/08). Justificativa na própria fonte: *"Você não tem uma ideia nova — tem três versões da mesma ideia, com escadas de preço que não conversam entre si"* (repo `00-achados-fontes-pessoais.md`).
- **A1** funde: `Parodi.AI` (2025). Justificativa literal: *"Parodi.AI (2025) e Arquibancada Studio são a mesma ideia — só nunca tinha sido formalizada antes."* `Boi Fest` entra como prova, não como linha própria.

### POSSÍVEL_DUPLICATA — não fundi, decisão é sua
1. **N2 × N3.** Mesmo comprador (PME local de Fortaleza), mesma cidade, mesmo canal, escadas de preço incompatíveis: R$697–997 (N2, wiki 20/08) × R$4.900 (N3, repo `07-gate1`, 17/08) × R$2.500–4.500 (N3, card GEO Sprint). N2 declara consumir N3 como submódulo: *"AI Search Ready Lite — Recorte do framework Nexum Visible"*. Ou N3 é o SKU premium de N2, ou são duas frentes disputando o mesmo dono de negócio com preços que se destroem.
2. **A1 × "Agência de Áudio B2B"** (blueprint, R$300–800/jingle). A fonte registra: *"Overlap com Boi Fest/Arquibancada Studio — considerar fundir"*. Fusão não decidida.
3. **J5 × RG-JUR-013.1 × RG-JUR-014** — três cards de laudo CCR B2B com escopos quase idênticos e IDs colididos (ver §6).

---

## 3. E3 — Prontidão

Escala 0–3 por dimensão · `PRONTIDÃO = soma/18 × 100`

| # | P1 Oferta | P2 Pagador | P3 Ativo | P4 Prova | P5 Operação | P6 Risco | Σ | **%** |
|---|---|---|---|---|---|---|---|---|
| **J3** B9 Parecerista | 2 | 2 | 2 | 0 | 3 | 3 | 12 | **66,7** |
| **N3** GEO | 2 | 2 | 1 | 0 | 3 | 3 | 11 | **61,1** |
| **N2** Nexum Local | 3 | 1 | 1 | 0 | 3 | 3 | 11 | **61,1** |
| **N6** Governança de IA | 2 | 2 | 2 | 0 | 3 | 2 | 11 | **61,1** |
| **A1** Arquibancada | 1 | 1 | 2 | 1 | 3 | 3 | 11 | **61,1** |
| **D1** Prompts | 2 | 1 | 2 | 0 | 3 | 3 | 11 | **61,1** |
| **N4** NBS | 2 | 1 | 2 | 0 | 2 | 3 | 10 | **55,6** |
| **A2** Luca DJ | 2 | 1 | 1 | 0 | 3 | 3 | 10 | **55,6** |
| **A3** DeepDrift | 1 | 1 | 1 | 0 | 3 | 3 | 9 | **50,0** |
| **J2** Q7 cópia do contrato | 2 | 2 | 1 | 0 | 2 | 1 | 8 | **44,4** |
| **J5** Bureau CCR | 2 | 2 | 1 | 0 | 2 | 1 | 8 | **44,4** |
| **J1** FAR T3 (wip-ativo) | 2 | 2 | 1 | 0 | 1 | 1 | 7 | **38,9** |
| **N5** Microprojetos Python | 1 | 1 | 1 | 0 | 3 | 1 | 7 | **38,9** |
| **T1** Ovinocultura | 1 | 1 | 1 | 0 | 1 | 2 | 6 | **33,3** |

### Justificativas com âncora — apenas onde a nota é decisiva

- **J3 P5=3 / P6=3.** *"pode operar já — Rodrigo assina sozinho, sem depender de terceiro"* + a autorização formal: *"Rodrigo possui autorização formal da CEF, aprovada pela OAB-CE, para advocacia extrajudicial e administrativa"*. Parecer não é polo ativo; INSS não é CEF. É a única frente jurídica com P6=3.
- **J1 P5=1 / P6=1.** *"Flag CEF: nunca Rodrigo no polo ativo"* + o registro do risco correlato: *"Erro aqui = PAD"*. Exige parceiro judicial, e a parceira designada está declarada como bloqueio: *"Dra. Irmã não confirmada formalmente … Bloqueio crítico."*
- **N2 P3=1.** Sprints 0 a 10 estão todos abertos. A própria fonte: *"Construir `local-presence-factory` como orquestrador e um template web único por vertical"* — o template não existe.
- **N2 P2=1.** *"Escolher quatro verticais candidatas"* segue como Sprint 0 não executado. Nenhuma empresa nomeada.
- **N3 P1=2.** A oferta existe, mas a base de preço foi invalidada pela sua própria auditoria de 17/08 (4 dados falsos), e o repo trava: *"Status: pré-projeto. Não rodar antes dos gates da Parte 4."*
- **T1 P5=1.** Exige diarista + zootecnista + veterinário + engenheiro de pesca. Fora de operação solo.
- **P4 = 0 em 13 das 14 linhas.** Nenhuma iniciativa do portfólio tem prova externa de demanda. A única exceção é A1 com P4=1, herdada de Boi Fest — e a própria auditoria diz: *"não apresenta valor, data de pagamento, arquivo final ou prova externa"*.

---

## 4. E4 — Maturidade de mercado

Regra dura aplicada: nenhum número sem fonte primária nomeada e datada. Onde não há, o campo é `NULO` e a linha vai a `PENDENTE_DE_FONTE`.

### Calculável — 3 mercados

| Mercado | M1 | M2 | M3 | M4 | **%** | Fonte |
|---|---|---|---|---|---|---|
| **Site/presença para PME BR** (N2) | 3 | 3 | 1 | 1 | **66,7** | InfinitePay, Levolu, QueroSite, Agência Colors — tabelas 2026, consultadas 24/08/2026 |
| **GEO/AEO BR** (N3) | 3 | 2 | 2 | 2 | **75,0** | Auditoria própria de 17/08/2026 contra mercado: GeoStack R$3.490/R$6.990 público; Promptado R$99–799 |
| **Música/jingle com IA BR** (A1, A2) | 3 | 2 | 1 | 1 | **58,3** | VintePila — jingle com IA a partir de **R$20**, preço público, consultado 24/08/2026 |

**Leitura que os números impõem:**
- **N2 vende abaixo do piso do mercado.** Site institucional simples para PME no Brasil custa **R$1.000–5.000**; freelancer, R$1.500–8.000. A oferta de R$697 (beta) e R$997 (base) entra por baixo do menor preço praticado. Isso não é gap de mercado — é guerra de preço num mercado maduro e fragmentado, contra concorrentes que já operam com escala.
- **A1/A2 competem contra R$20.** Luca DJ pede R$97–197 por música; existe fornecedor público entregando jingle com IA a partir de R$20. A diferenciação não pode ser "faço música com IA" — esse insumo já é commodity precificada.
- **N3 é o único mercado com janela real.** Concorrente puro identificado com preço público (GeoStack, R$3.490–6.990/mês), acima do ticket-alvo; ferramenta de monitoramento sem execução (Promptado). Nichos abertos.

### `PENDENTE_DE_FONTE` — 11 iniciativas
J1, J2, J3, J4, J5, J6, N1, N4, N5, N6, T1, A3, D1.

Consultas a fazer, nomeadas:
- **J3/J4/J6:** volume de processos previdenciários rurais no TRF5 via **Datajud** (classe 72/48); nº de advogados inscritos na Comissão de Seguridade Social **OAB-CE**; lista pública **AAPREC**. Sem tabela de preço pública — a OAB veda; a única prova possível é o primeiro contato.
- **T1:** cotação **CEPEA/ESALQ** de ovinos e existência de abatedouro SIF/SIE no raio de Aquiraz (a própria fonte já registra: *"Abatedouro com SIF/SIE no raio de Aquiraz: pendente de verificação"*).
- **N1:** confirmar se o SDR Aluminacle ainda opera e qual o valor recebido — ver `DADOS_INSUFICIENTES`.

---

## 5. E5 — Matriz, filtro e decisão

### 5.1 Kill switches acionados → `MORTAS`

| Iniciativa | Switch | Registro que aciona |
|---|---|---|
| **Fazenda solar 1 MW (Russega)** | 3 — capital fora da janela, sem parceiro | 1 MW em 2 ha; pré-requisito não verificado: *"consulta de acesso à Enel-CE"* |
| **Canal Dark Ambient/Solfeggio** | 4 + 6 | *"Não iniciado — mesmo território do DeepDrift"*; origem: blueprint LLM do Drive, nunca formalizado |
| **LoFi Samba Carioca / LoFi Calma** | 4 | *"Streaming — ROI baixo sem audiência"*, não iniciado |
| **Nicho Gospel/Worship** | 4 + 6 | blueprint de mercado, pagador nulo, *"atenção a direitos de tradutores"* |
| **AntiStrike / Creator Safe Packs** | 4 + 6 | *"Não iniciado — blueprint de 7 dias desenhado"* |
| **Pacote CAIXA Copilot** | 2 | é automação do trabalho CLT; o escopo do próprio projeto exclui: *"CEOPE / Caixa — automação do trabalho CLT"* |
| **BPC B2B Parecerista** (`RG-JUR-036.1`) | 5 | *"Morta estrutural. Não reabrir: conflito institucional + capital emocional incompatível."* |
| **Vínculo App Uber/iFood** (`RG-JUR-013`) | 5 | *"Morta. Não reabrir sem mudança estrutural nos critérios operacionais."* |
| **Recuperação Judicial B2B** (`RG-JUR-011`) | 5 | descartada — *"Mercado consolidado FIDCs"* |
| **PrevIA Escala · Oráculo Peças Agro** | 5 | dormentes/descartados — *"Reativar se IAN/CCR não engatar"* |
| **Recuperação Tripla Futebol** (`RG-JUR-012`) | 5 | Onda 5, *"🔴 Standby — revisão nov/2026"* |
| **J4 — B7 Atendimento direto** | 3 | *"travada — falta parceiro judicial fechado"* — congela até a parceria fechar, não é morte definitiva |
| **~55 cards em `hipotese`/`exploratorio`** | 5 (Portão T6) | *"tese nova fora de Onda 1 ou 2 vai para backlog automático — sem análise, sem discussão, sem exceção"* |

### 5.2 `DADOS_INSUFICIENTES`

| Iniciativa | Evidência que falta |
|---|---|
| **N1 — Nexum Opera / SDR** | Prontidão bruta seria a mais alta do portfólio (**83,3%**), mas aciona o **switch 1**: a última evidência é de **11/04/2026** e a base que a sustenta (RAG Pessoal local) é inacessível. Falta: (a) o agente ainda roda? (b) valor efetivamente recebido — a própria auditoria diz *"falta valor, forma de pagamento e comprovante"*; (c) houve receita após 28/03? Sem isso, o score é sobre um registro de 4 meses atrás. |
| **J6 — FUNDEF** | Motor quebrado com N=50: *"nenhum tinha rubrica identificável"*. A tese jurídica segue de pé, o motor de dados não. Falta: causa do falso negativo no Bloco 3 e fonte de óbito no Bloco 5. Prazo real: prescrição da parcela 1 ~set/2026. |
| **J5 · J2 · J1** | Todas dependem da Dra. Irmã, declarada como *"Bloqueio crítico"* não resolvido. Falta: quais teses ela assina, capacidade mensal, comarcas, percentual. |
| **D1 — Produtos de prompts** | Ativo documentado, mas arquivos em caminho Windows/OneDrive não recuperado nesta sessão. Falta: localizar os arquivos. |

### 5.3 `SEM_LASTRO` — citados, sem artefato localizável

Todos vêm da classificação Classe B da sua própria wiki de 20/08 (*"há evidência forte de existência/compra, mas o arquivo final ainda não foi localizado"*):
Pack +1000 Templates Typebot · Agente de Vendas IA Avançado · Rodnei Labs + Instalação do Agente · Pack de automações de vendas/atendimento · `Prompt Lovable - Agente CRM` · `prompt-landing-advocacia.md` · `PROPOSTA-COMERCIAL-VALIDADE-ZERO-IA.md`.

Não são iniciativas — são insumos comprados sem entregável recuperável. Nenhum passa no teste do objeto enquanto o arquivo não aparecer.

### 5.4 Tabela-mapa

Ordenada por Prontidão desc, depois Maturidade desc.

| Iniciativa | Quadrante | Prontidão | Maturidade | Pagador | Gargalo #1 | Próximo passo verificável | Fontes |
|---|---|---|---|---|---|---|---|
| **J3 B9 — Parecerista Previdenciário Rural B2B** | — (eixo externo pendente) | **66,7** | PENDENTE | Advogados previdenciários NE via Comissão Seguridade OAB-CE + AAPREC | Contato nunca feito — decidido "Avançar" em 16/08, 8 dias parado | 1 telefonema à Comissão de Seguridade Social OAB-CE | CARDS `RG-JUR-011`; EstadoAtual §17 |
| **N3 GEO** | **EXECUTAR** | 61,1 | **75,0** | PME/profissional liberal Fortaleza | Zero prova de demanda; base de preço já invalidada uma vez | Gate 1 do repo: teste dos 30 min + 5 conversas na rua | repo `06`,`07`; card GEO |
| **N2 Nexum Local** | **EXECUTAR** | 61,1 | **66,7** | Negócio local CE — vertical não escolhida | Preço abaixo do piso de mercado; template não existe | Sprint 0/1: escolher vertical e avaliar 40 empresas | Notion wiki v0.4/v0.5 |
| **N6 Governança de IA** | — | 61,1 | PENDENTE | Escritório de advocacia 1–10 advogados | Sem preço definido | Precificar e rodar 1 diagnóstico gratuito | ESTADO ATUAL 10/07 |
| **A1 Arquibancada Studio** | **APOSTA** | 61,1 | 58,3 | NULO — *"Sem comprador nominal identificado"* | Concorrência a R$20 | 1 briefing real, como já decidido | Notion 15–16/08 |
| **D1 Prompts** | — | 61,1 | PENDENTE | NULO | Arquivo não localizado | Localizar os arquivos antes de qualquer coisa | Auditoria 13/08 |
| **N4 NBS** | — | 55,6 | PENDENTE | PME — case zero é a própria Nexum | Depende da executora júnior | Executar case zero | card NBS |
| **A2 Luca DJ** | **ARQUIVAR** | 55,6 | 58,3 | NULO | Preço não fechado desde 19/07; mercado a R$20 | Decisão binária pendente há 36 dias | Notion 19/07 |
| **A3 DeepDrift** | **ARQUIVAR** | 50,0 | PENDENTE | AdSense — plataforma, não pagador | Gatilho declarado (BPC caso #1) nunca ocorreu | Nenhum — congelado por decisão própria | RADAR 16/06 |
| **J2 Q7 · J5 Bureau CCR** | — | 44,4 | PENDENTE | Mutuários MCMV / escritórios bancário-agro | Dra. Irmã não confirmada + Flag CEF | Fechar formalmente o polo ativo judicial | CARDS |
| **J1 FAR T3** *(único wip-ativo)* | — | 38,9 | PENDENTE | Mutuário FAR 2011–2018 | Flag CEF **estrutural** + parceiro não confirmado | idem | CARDS `RG-JUR-028` |
| **N5 Microprojetos Python** | — | 38,9 | PENDENTE | PME genérica | Risco legal não resolvido; origem CEF | Escolher 1 das 10 peças e nomear 1 cliente | card 08/07 |
| **T1 Ovinocultura** | — | 33,3 | PENDENTE | NULO | Nada implantado; exige equipe | CAR + visita EMATERCE (R$0) | card Russega 17/05 |

### 5.5 O achado que o mapa produziu

Três coisas que só aparecem cruzando as fontes:

1. **P4 = 0 em todo o portfólio.** Catorze iniciativas, nenhuma com prova externa de demanda. Isso não é um problema de priorização — é um problema de evidência. O portfólio inteiro está do lado esquerdo da primeira venda.
2. **A frente mais adiantada é a mais arriscada para o seu emprego.** O único card `wip-ativo/producao` de 94 é o cluster FAR/MCMV, e todo ele é **Flag CEF = SIM** — litígio contra o seu empregador. O próprio card registra a consequência: *"Erro aqui = PAD"*. A frente com maior Prontidão jurídica formal (J3, P6=3) é justamente a que **não** toca a CEF.
3. **Um gargalo único trava seis iniciativas.** J1, J2, J4, J5, J6 e boa parte dos 94 cards dependem de uma pessoa cuja adesão está declarada como não confirmada desde 16/08. Não são seis problemas; é um.

---

## 6. Contradições entre fontes — listadas, não resolvidas

1. **Três "frentes ativas" simultâneas e mutuamente incompatíveis.** O database de cards diz que o `wip-ativo` é `RG-JUR-028` (FAR/MCMV). As Instruções SP&ADV §12.1 registram a contradição **BPC × FUNDEF** como aberta desde 08/07. O EstadoAtual §17 (16/08) decide **B9/B7 previdenciário**. Nenhuma das três revoga as outras. Pela regra de leitura do próprio projeto ("vale a data mais recente"), venceria B9 — mas o database não foi atualizado para refletir isso.
2. **Colisão de IDs no database.** `RG-JUR-011` identifica ao mesmo tempo "Parecerista Previdenciário Rural" e "Recuperação Judicial B2B". O mesmo ocorre com `RG-JUR-013`, `023`, `025`, `026`, `027`, `028`, `029`, `030`, `031`. A regra "1 card por tese, sempre" está mantida; a unicidade do ID, não. Rastreabilidade por ID está quebrada.
3. **Hub desatualizado em 3 meses.** O Hub de Teses (06/05) lista 11 teses. O database tem **94**. Nenhum documento avisa que o Hub é parcial.
4. **Score do MCR 2.6.4:** 94 (Manual, 06/05) × 88 (ranking, 08/05) × 82 (catálogo, 16/06) × 88 (database, hoje). Já registrado como pendência 7 e ainda não reconciliado.
5. **Preço do produto GEO:** R$4.900 (repo `07-gate1`) × R$2.500–4.500 (card GEO Sprint) × R$3.490/mês do concorrente com preço público. Três âncoras de preço para o mesmo comprador.
6. **N2 abaixo do piso de mercado:** oferta de R$697–997 contra mercado verificado de R$1.000–5.000 para o mesmo entregável.
7. **A1 × Agência de Áudio B2B:** overlap declarado na fonte, fusão nunca decidida.

---

## 7. Decisão

> **DECISÃO: a próxima iniciativa a receber horas é o B9 — Parecerista Previdenciário Rural B2B, porque é a única com a maior Prontidão do portfólio (66,7%) sem trava de vínculo (P6=3, amparada pela autorização formal CEF/OAB-CE para atuação extrajudicial) e sem dependência de terceiro — condição registrada por você mesmo em 16/08 como "Avançar · Bloqueio: Nenhum — pode operar" e parada desde então. Todas as demais ficam congeladas até o primeiro parecer pago ou até D+14 sem contato enviado, o que ocorrer primeiro — gatilho que já é a sua própria regra de stop-loss.**

**Por que não N3/GEO,** que é o único par de eixos completo e cai em EXECUTAR: porque N3 e N2 estão em colisão declarada de comprador e preço (§2, POSSÍVEL_DUPLICATA 1), e destinar horas a qualquer uma antes de resolver a colisão financia as duas pontas de uma guerra de preço contra você mesmo. Resolvida a colisão, N3 é a segunda na fila — o Gate 1 do repo já está escrito e custa 30 minutos.

**Por que não N1/Nexum Opera,** que teria a maior Prontidão bruta (83,3%): porque a evidência que sustenta esse número tem 4 meses e vem de uma base que não pude abrir. Antes de qualquer hora nova, uma pergunta de dois minutos: *o SDR ainda roda e quanto ele pagou?* A resposta pode reordenar o mapa inteiro.

---

## 8. Três decisões que são suas, não minhas

1. **N2 × N3** — mesmo comprador, três preços. São uma iniciativa com dois SKUs ou duas frentes? Não fundi.
2. **Frente ativa** — CARDS diz FAR/MCMV, Instruções dizem BPC×FUNDEF em aberto, EstadoAtual diz B9. Qual vale?
3. **A1 × Agência de Áudio B2B** — fundir ou manter separadas?
