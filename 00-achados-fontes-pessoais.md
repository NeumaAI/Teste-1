# Parte 0 — O que já existe nas suas fontes

Varredura feita em 17/08/2026 sobre: repositório local, Notion, Google Drive e skills sincronizadas.

---

## 0.1 Onde busquei e o que cada fonte devolveu

| Fonte | Acesso | Resultado |
|---|---|---|
| Repositório local (`/home/user/Teste-1`) | ✅ | **Vazio.** Branch `claude/geo-aio-site-product-u9wyhr` sem commits. Nada de código aqui. `[V]` |
| Notion | ✅ | 4 páginas diretamente relevantes + 3 de contexto estratégico |
| Google Drive | ✅ | 7 documentos relevantes, o mais completo de maio/2026 |
| Skills sincronizadas (`/root/.claude/skills/synced/`) | ✅ | `geo-otimizacao-conteudo` e `geo-juridico` — ambas existem |
| Memory-compiler (histórico de conversas) | ⚠️ | Não varrido nesta sessão — é uma skill que roda sobre histórico de chat, não uma base consultável por API. Se quiser, rodo separado. |

---

## 0.2 Os três produtos GEO que você já tem escritos

Este é o achado central. **Você não tem uma ideia nova — tem três versões da mesma ideia, com escadas de preço que não conversam entre si.**

### A) 🟡 Nexum Visible — Framework Operacional v1.0 (GEO + AEO)
[Notion](https://app.notion.com/p/36528fecb91281a9a552ff0e91ee2301) · 18/05/2026, atualizado 20/05 · `[V]`

- Posicionamento: advogados, escritórios, consultores e marcas **B2B**
- **O que explicitamente NÃO vende: "criação de sites"** — está na seção 1, "O que NÃO vendemos"
- Preços: Auditoria R$ 5–8k one-shot · Setup R$ 8k + retainer R$ 3k/mês · Projeto 90 dias R$ 12–18k
- Anti-padrão registrado: **"❌ Vender retainer abaixo de R$ 2.000/mês"**
- Método em 5 fases (V1 Diagnóstico → V5 Iteração)
- Ferramenta de monitoramento decidida: **Promptado (R$ 199/mês, brasileira)**
- Canal prioritário decidido: **agências de marketing jurídico sem GEO, white-label a 70% da tabela**
- Restrição societária: empresa **não pode ter a CEF como cliente**; objeto social nunca "advocacia"

### B) 🔍 GEO — Nexum Brand Intelligence
[Notion](https://app.notion.com/p/34428fecb912818bb331e070f508879a) · 16/04/2026 · `[V]`

- Posicionamento: **PME brasileira** — "único serviço de GEO acessível para PME"
- Escada de preço **completamente diferente da A**: Diagnóstico R$ 300–500 (48h) · Sprint R$ 2.500–4.500 (7–10 dias) · Recorrente R$ 800–1.500/mês
- Funil documentado: Diagnóstico → 80% converte → Sprint → 60% converte → Recorrente. LTV R$ 12–25k/ano `[E]`
- **Tem SOP escrito e delegável** — Etapa 1 Coleta (15 min) / Etapa 2 Análise (20 min) / Etapa 3 Relatório (30 min)
- **Tem os 3 prompts do produto prontos**, coláveis: teste de visibilidade, relatório Gamma, análise de conteúdo em 5 camadas
- Status: "GO confirmado (CRIVO 16/04/2026), produtizado, **aguardando slot WIP**"
- Benchmark de preço confirmado: Promptado R$99 · Profound R$2.300+ · Conversion/Wyse/Bloomin R$9.000+

### C) PLANO COMPLETO — Agência GEO + Agentic AEO (método NUCLEO™)
[Drive](https://docs.google.com/document/d/171ULAn83LeXQ__KOxZ-ZQ9DbpE0J2365YiAJuyo9Jy4/edit) · maio/2026 · 25 KB · `[V]`

- O documento mais completo dos três. Mapeia **8 concorrentes brasileiros nominalmente** (WebShare, Conversion, Wyse, Upsend, Bloomin, Triplo SP, Agência Web Marketing, LondrinaSEO) — todos em SP/Florianópolis/Londrina, **nenhum no Nordeste**
- Método proprietário **NUCLEO™** em 6 etapas: Node mapping → Unified entity → Citation engineering → LLM-readiness audit → Engine-by-engine deployment → Ongoing observation
- **Recomendação explícita de posicionamento: "especialização pura, SEM criação de site"** — está na tabela de diferenciação, linha Upsend e linha Wyse
- Terceira escada de preço: Diagnóstico R$ 4.500 · Essencial R$ 2.800/mês · Completo R$ 5.500/mês · Premium R$ 9.800/mês · Enterprise R$ 18k+/mês
- 5 dores com Mom Test aplicado e score FI (a Dor 1 tem score 22, crítica)
- Dados de eficácia GEO citados de pesquisa: citações inline +30% · estatísticas +30% · **quotes de especialista +41%** · GEO Score ≥0,70 → 78% de citação cross-engine
- Gap de preço documentado: **"buraco enorme entre ferramenta self-service (R$99) e agência enterprise (R$5–10k/mês). Território de R$1k–5k/mês para PME está aberto"**
- Riscos com probabilidade: **"Padrão de abandono em 80-90% — Alta (46% projetos auto-gerados Rodrigo)"**

---

## 0.3 Documentos de contexto que mudam a leitura

### 🎯 Terceira Camada — Critérios de Captura e Releitura de Concorrência v1.0
[Notion](https://app.notion.com/p/3bf28fecb91281ed9c93d3f04f2d05f5) · **17/08/2026 — de hoje** · `[V]`

O documento mais recente e o mais duro contra este produto. Três achados que atingem diretamente o pedido:

1. **Critério C3 — assimetria de diagnóstico.** Três estados: *sabe e busca* / *sente mas não nomeia* / *não sabe de nada*. Corolário textual: **"GEO só rende nos estados 1 e 2. No estado 3 é dinheiro jogado fora — o cliente nunca vai fazer a pergunta."**
2. **A tese de GEO ainda é hipótese.** Texto literal: *"Isso é hipótese, não dado. **Teste antes de investir:** 15-20 perguntas reais de cliente em ChatGPT, Claude, Gemini e Perplexity, registrando quem é citado. Sempre os mesmos cinco escritórios = janela fechada. Respostas genéricas sem atribuição = aberta. **Meia hora de trabalho.**"* — **não há registro de que esse teste tenha sido feito** `[?]`
3. **C0 — Razão de escolha.** *"Qualquer tese cuja razão de escolha seja 'eu apareço no Google' ou 'eu cobro mais barato' está competindo em terreno onde ele não tem vantagem nenhuma."*
4. **Meia-vida da vantagem (C4):** conteúdo/GEO bem posicionado = **12–24 meses** até o incumbente reagir. Não é ativo permanente.

### matriz-renda-extra.pdf
[Drive](https://drive.google.com/file/d/1FXaqAB1zqdmrR_C_8YjSTsR2DAGmup9e/view) · 16/07/2026 · `[V]`

Já tinha detectado exatamente este padrão, um mês atrás. Texto literal:

> *"4 dos seus 11 itens são o mesmo conceito de coisas que você já validou e pontuou como GO, só reformuladas. […] Isso não é coincidência de nicho parecido — é a mesma ideia central, com preço e stack já definidos, esperando você abrir o slot. Isso muda a pergunta real. Não é 'qual side job escolher entre 11 opções novas'. É: **'por que estou regerando ideias que já pontuei como GO em vez de ativar uma delas?'**"*

"Sites GEO/AEO (busca generativa)" aparece nessa matriz em **2º lugar de 11**, com nota baixíssima em "conflito com WIP" (nota 1 de 10).

### Outros documentos de apoio no Drive `[V]`

| Documento | Data | Valor para este produto |
|---|---|---|
| [Otimização de Conteúdo para IA — GEMINI](https://docs.google.com/document/d/1SuyYaVNdXekjemxOH7Q_nNJkZv0mI-G-cz-P_BnT65I/edit) | 23/06/2026 | Referencial técnico denso: SAGEO, **query fan-out (5–20 sub-consultas)**, escada de autoridade de marca (marca global 73% de citação, médio porte 44%, **nicho 11%**) |
| [Prompt de Pesquisa GEO Estratégica](https://docs.google.com/document/d/151Rpzh1prgVtTKVHif0abMSv5mhvR98a6SdYz3d6qec/edit) | 04/03/2026 | Tabela SEO vs AEO vs GEO vs AI Discovery. Zero-click: 60% desktop, **77% mobile** |
| [GEO - SEO - Inputs](https://docs.google.com/document/d/1PhpwlwTckQ1lTVoLI0FFWKPFrpnQNX_2hOZYH4Q64LI/edit) | 10/05/2026 | Prompt do "Filtro do Adversário Cruel" |
| Referencias mundiais GEO / Roadmap de Estudo GEO | 04/03/2026 | Base bibliográfica |
| `2026-04-20-automao-e-ia-para-criao-de-sites.txt` | 20/04/2026 | Anotação sobre automação de criação de sites |

---

## 0.4 As ferramentas que você disse que tem — verificação

Você mencionou dois ativos técnicos. Verifiquei os dois.

### ✅ A skill de GEO — **existe**
`/root/.claude/skills/synced/geo-otimizacao-conteudo/SKILL.md` · 327 linhas · `[V]`

Pipeline de 5 camadas: Auditoria SEO base → Otimização GEO → Filtragem e reenriquecimento → Scoring gamificado → Entrega. Produz metadata YAML, chunking de 100–300 tokens, e scoring ponderado (Findability 25% · Estrutura 20% · Acionabilidade 20% · Credibilidade 15% · Completude 20%).

Existe também `geo-juridico`, com gate de compliance OAB — relevante se algum cliente for advogado.

### ❌ O motor em Python — **não existe neste ambiente**
`[V]` — verificação direta

Você disse *"pegar o motor que eu já fiz em Python aqui. Já tá calepau."* Procurei em todo o sistema de arquivos:

- `geo-otimizacao-conteudo/` contém **apenas** `SKILL.md`. Sem `scripts/`, sem `.py`, sem nada executável.
- O frontmatter da skill **declara** `Dependências: Python 3.8+, requests, beautifulsoup4` — mas o código correspondente não está aqui.
- Os únicos `.py` no ambiente pertencem a skills da Anthropic (`docx`, `xlsx`, `pptx`, `skill-creator`, `mcp-builder`). Nenhum é seu, nenhum é de GEO.
- O repositório deste projeto está vazio.

**Consequência prática:** hoje o produto roda 100% em prompt (a skill), com pessoa no meio. Não há automação executável. Ou o motor está em outra máquina/repositório que preciso que você aponte, ou ele precisa ser construído — e isso é escopo de trabalho, não ativo pronto.

Isso não invalida o produto. **A skill sozinha já entrega o Diagnóstico e o Sprint** — o SOP do documento B prova isso, com tempo cronometrado de 65 minutos por diagnóstico. Só não vale planejar capacidade assumindo automação que não existe.
