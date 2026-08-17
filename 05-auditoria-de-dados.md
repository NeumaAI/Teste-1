# Parte 5 — Auditoria de dados: o que é fato, o que era alucinação

Verificação feita contra o mercado real em **17/08/2026**. Motivo: os dados que sustentavam o pré-projeto vieram dos seus documentos de março–maio/2026, que por sua vez foram **gerados por LLM e nunca verificados contra fonte primária**. Uma alucinação num deles se propaga por todos os documentos seguintes — e por mim.

**Resultado da auditoria: 4 dados falsos ou desatualizados, 5 confirmados com correção de precisão, e 3 achados novos que mudam o produto.**

---

## 5.1 O que estava ERRADO nos seus documentos

### ❌ E1 — Preço da Promptado: você registrou R$ 199/mês. É falso.

**No seu Notion (Nexum Visible §13, 20/05):** *"Ferramenta-núcleo de monitoramento: Promptado (R$ 199/mês, brasileira, PT-BR) — adotar desde o cliente 1."*

**Real, hoje `[V]`:** Starter **R$ 99/mês** · Essential **R$ 399/mês** · Growth **R$ 799/mês** · Enterprise e Agência sob consulta. Trial de 7 dias. Monitora ChatGPT, Gemini, Copilot, Grok e Google AI Mode.

**Impacto:** direto na margem. Um retainer de R$ 690/mês com custo de ferramenta de R$ 399 deixa R$ 291 antes de qualquer hora de trabalho — **inviável**. O plano de custo operacional da Nexum Visible ("~R$ 1.500-2.000/mês") também precisa ser refeito.

> **Correção operacional:** nos clientes 1–3, **não comprar ferramenta nenhuma.** O monitoramento é o mesmo teste do Laudo, roda com a skill, leva ~1h/mês. Promptado (ou o plano Agência) só entra quando houver 4+ clientes para amortizar.

### ❌ E2 — "Nenhuma agência especializada-pura em GEO no Brasil". Falso desde ~junho.

**No seu Drive (plano_agencia_geo, maio):** *"não há agência ESPECIALIZADA-PURA em GEO+Agentic. Gap de posicionamento."*

**Real, hoje `[V]`:** a **GeoStack** se posiciona publicamente como *"a primeira agência do Brasil 100% dedicada a Generative Engine Optimization"*, com preço **público** — GEO Starter **R$ 3.490/mês** (profissionais liberais, marcas pessoais e pequenos negócios) e GEO Growth **R$ 6.990/mês** (PMEs, e-commerces, startups). Mantêm inclusive um "Mapa das Agências de GEO" como ativo de conteúdo.

**Impacto:** o gap que seu plano de maio identificou **foi ocupado em ~3 meses**, exatamente como o critério C4 da sua Terceira Camada previa (meia-vida de vantagem de conteúdo/GEO: 12–24 meses, e menos ainda para posicionamento). Isso não mata o produto — muda o argumento. Ver §5.3.

### ❌ E3 — "Preços opacos, nenhuma agência brasileira mostra preço público". Falso hoje.

GeoStack publica tabela. Há artigos brasileiros de 2026 com faixas abertas: consultoria GEO de **R$ 5.000 (sprint)** a **R$ 80.000/mês (retainer enterprise)** `[V]`.

**Impacto:** seu diferencial "preço público" deixou de ser diferencial. Precisa de outro — e ele existe (§5.3).

### ❌ E4 — Zero-click "60% desktop, 77% mobile". Números certos, rótulos trocados, e defasados.

**Real `[V]`, SparkToro/Similarweb, primeiros 4 meses de 2026, EUA:**
- **68,01% geral** (era 60,45% em 2024 — o "60%" do seu doc era o número **geral de 2024**, não desktop)
- **~50% desktop · ~77% mobile**
- Buscas que geram ao menos um clique caíram 9,51 pontos entre 2024 e 2026 (queda relativa de 22,9%)
- AI Overviews aparecem em **mais de 20%** das buscas do Google

⚠️ **Dado dos EUA.** Não existe estudo equivalente para o Brasil que eu tenha encontrado `[?]`. Usar como referência de tendência, **nunca** como "no Brasil é assim".

---

## 5.2 O que estava CERTO (com a precisão corrigida)

### ✅ V1 — Queda de CTR por AI Overviews: 58% é real, mas exige data

**Ahrefs, dois estudos `[V]`:**
- Abril/2025, 300 mil palavras-chave: **−34,5%** de CTR no 1º colocado quando há AI Overview
- Dezembro/2025: **−58%** — CTR do 1º colocado caiu de 0,073% para 0,016% em keywords com AIO

**Como citar corretamente:** *"Segundo a Ahrefs, com dado de dezembro de 2025, quando aparece o resumo de IA o primeiro colocado do Google perde 58% dos cliques."* Citar sem a data é o tipo de imprecisão que derruba a credibilidade se o cliente procurar.

### ✅ V2 — Paper de Princeton: existe, mas o número é mais fraco do que você anotou

**Real `[V]`:** *"GEO: Generative Engine Optimization"* — Aggarwal, Murahari, Rajpurohit, Kalyan, Narasimhan, Deshpande. ACM SIGKDD 2024, arXiv 2311.09735. 17 páginas, **9 táticas testadas em 10.000 queries**.

**Correção importante:** os três métodos mais fortes atingiram **30–40% de melhora relativa** na métrica *Position-Adjusted Word Count* — e **40% é o valor máximo, não a média**. Além disso, análises do paper apontam que **"Information Gain" (trazer informação que não existe nas outras fontes) é o driver principal de citação**, e que os achados **contrariam as premissas da maioria das agências que hoje vendem visibilidade em IA**.

**Impacto no pitch:** o "+41% com quotes de especialista" do seu documento é derivado desse paper, mas apresentá-lo como ganho garantido é exagero. A forma honesta: *"há pesquisa acadêmica mostrando ganho de até 40% em citação com técnicas específicas — e o fator mais forte é dizer algo que ninguém mais diz."*

### ✅ V3 — Faixa de preço de site no Brasil

`[V]` 2026: site institucional simples R$ 1.000–5.000 · até 5 páginas R$ 2.500–4.500 · site profissional geral R$ 3.000–12.000 · landing page R$ 1.500–4.000. Hospedagem R$ 100–1.500/mês, domínio R$ 40–80/ano.

### ✅ V4 — Nordeste ainda sem agência GEO identificada

`[I]` Busca dirigida a Fortaleza/Ceará/Nordeste não retornou nenhuma agência GEO local. **Ausência de evidência, não evidência de ausência** — mas consistente com o mapeamento de maio.

### ✅ V5 — Mercado brasileiro subpenetrado

`[I]` — **atenção: dado de marketing de agência, não estudo independente.** Alega-se que apenas **1,2% das empresas brasileiras** têm alguma otimização para IA generativa, contra 23% nos EUA. Plausível na ordem de grandeza, mas a fonte tem interesse comercial em inflar a lacuna. **Não usar em proposta** sem uma segunda fonte.

---

## 5.3 Os TRÊS achados novos — e o que eles mudam

### 🔥 N1 — 83% dos restaurantes são invisíveis no ChatGPT. Contra 14% no Google.

`[V]` **Corroborado por 4 fontes independentes** (Local Falcon, TechNewsWorld, MapAtlas, e relatório separado da Uberall). Estudo de **189.905 resultados de busca do ChatGPT** para queries de restaurantes — um dos maiores já feitos sobre visibilidade local em IA.

Três números que vêm junto e que valem mais que o titular:

| Dado | Número | Por que importa |
|---|---|---|
| Invisibilidade | **83% no ChatGPT vs 14% no Google** | O problema é 6× maior em IA do que em busca tradicional |
| Concentração | **Top 10% capturam 74,5% da visibilidade em IA** (vs 54% no Google Maps) | IA é mais "vencedor leva tudo" que o Maps. Estar no pelotão de trás vale ainda menos |
| Avaliações não salvam | Restaurantes com **+1.000 avaliações no Google ficaram de fora 70,9% das vezes** | Mata a objeção *"mas eu tenho 5 estrelas e 800 avaliações"* |

**E o contexto que fecha o argumento:** a OpenAI lançou publicidade no ChatGPT em **fevereiro/2026, com compra mínima de US$ 200.000** `[V]`. Ou seja: a porta paga **está fechada** para negócio local. Orgânico é o único caminho — por enquanto.

**O que muda:** este é o dado mais forte do produto inteiro, e ele não estava em nenhum documento seu. Ele substitui metade dos argumentos que eu tinha proposto. Ressalva obrigatória: **é estudo americano, de restaurantes.** Não é prova de que o mesmo ocorre em Fortaleza — é exatamente por isso que o Gate 1 existe.

### 🔥 N2 — 45% dos consumidores já usam IA para achar negócio local. Era 6% um ano atrás.

`[V]` Salto de 7,5× em doze meses. É o dado que responde *"mas isso é coisa de nerd, meu cliente não usa ChatGPT"* — a objeção mais provável de um dono de padaria.

### 🔥 N3 — O ChatGPT não sabe onde você está.

`[V]` Diferente do Google e do Apple Maps, o ChatGPT **não interpreta "perto de mim"** sem contexto adicional. Ele responde a partir de páginas, avaliações, diretórios e dados estruturados que consegue ler e confiar. Consistência de nome, endereço, telefone e horário **entre site, Google Business Profile e diretórios** é fator determinante.

**Três consequências operacionais diretas:**
1. **O Bloco C (Identidade Canônica) sobe de importância** — deixa de ser higiene e vira mecanismo central
2. **As perguntas do Laudo têm que nomear o bairro/cidade explicitamente** — "melhor pizzaria perto de mim" não testa nada
3. Confirma o que já estava certo: a primeira posição orgânica do Google é citada **3,5× mais** que as seguintes dentro das respostas do ChatGPT `[I]`, e negócios com **20+ avaliações novas em 3 meses** têm **2,5× mais chance** de aparecer `[I]` — ou seja, o produto precisa incluir uma orientação de avaliações, que hoje não está no escopo

---

## 5.4 Preço — refeito sobre âncora real

O R$ 4.900 que propus foi derivado de raciocínio, não de mercado. Agora com mercado:

| Âncora real `[V]` | Valor |
|---|---|
| Site institucional até 5 páginas (BR, 2026) | R$ 2.500 – 4.500 |
| Site profissional geral (BR, 2026) | R$ 3.000 – 12.000 |
| **GeoStack GEO Starter** (pequeno negócio, **sem site**) | **R$ 3.490/mês** |
| GeoStack GEO Growth (PME) | R$ 6.990/mês |
| Consultoria GEO BR — sprint básica | a partir de R$ 5.000 |
| Ferramenta Promptado | R$ 99 / R$ 399 / R$ 799 por mês |

### O veredito sobre o preço

**R$ 4.900 está correto, mas o argumento que eu tinha construído estava errado.** A comparação certa não é com freelancer de site — é com a GeoStack:

| | GeoStack Starter | **PRIMEIRA RESPOSTA** |
|---|---|---|
| Site incluso | ❌ | ✅ |
| Modelo | R$ 3.490/**mês** | R$ 4.900 uma vez |
| **Custo no ano 1** | **R$ 41.880** | **R$ 13.180** (4.900 + 12 × 690) |
| Medição antes/depois | não publicada | ✅ contratual |

**Isso é 3,2× mais barato no primeiro ano, com o site incluído.** É um argumento de venda muito mais forte do que qualquer coisa que eu tinha escrito antes — e é verificável pelo cliente, o que o torna quase impossível de contestar.

### Correções de preço necessárias

| Item | Antes | Agora | Motivo |
|---|---|---|---|
| Projeto | R$ 4.900 | **R$ 4.900 — mantido** | Confirmado pela âncora GeoStack |
| Recorrente | R$ 690/mês | **R$ 890/mês** | R$ 690 não cobre nem a ferramenta se ela for comprada cedo |
| Custo de ferramenta | R$ 199/mês desde o cliente 1 | **R$ 0 até o cliente 4** | Monitoramento manual com a skill, ~1h/mês |
| Laudo avulso | R$ 690 | **R$ 890** | Alinha com o recorrente e evita canibalização |

---

## 5.5 O que continua sem verificação — e não dá para verificar daqui

| # | Pergunta em aberto | Quem responde | Custo |
|---|---|---|---|
| 1 | O ChatGPT/Gemini/Perplexity/Claude citam **negócios locais nomeados em Fortaleza**, ou devolvem agregador? | Só você, rodando | 30 min |
| 2 | Os 83% dos EUA se reproduzem no Brasil? | Só o Gate 1, na sua categoria | incluso acima |
| 3 | Existe agência GEO em Fortaleza que a busca não pegou? | Busca local + LinkedIn | 30 min |
| 4 | O comerciante de bairro **aceita** R$ 4.900? | Só a rua. 5 conversas. | 2h |
| 5 | O motor Python existe em algum lugar? | Só você | 5 min |

**Nenhum documento resolve os itens 1, 2 e 4. Só contato com a realidade.**

---

## Fontes

- [SparkToro — Less than One Third of Google Searches Still Send a Click (2026)](https://sparktoro.com/blog/in-2026-less-than-one-third-of-google-searches-still-send-a-click/) · [Search Engine Land — zero-click 68%](https://searchengineland.com/google-zero-click-searches-2026-study-479717)
- [Ahrefs — AI Overviews Reduce Clicks by 34.5%](https://ahrefs.com/blog/ai-overviews-reduce-clicks/) · [Medianama — AI Overviews reduce clicks by 58%](https://www.medianama.com/2026/02/223-google-ai-overviews-click-through-rates-58-study/)
- [Local Falcon — The AI Visibility Crisis: 83% of Restaurants](https://www.localfalcon.com/blog/the-ai-visibility-crisis-why-83-percent-of-restaurants-dont-exist-in-chatgpt) · [TechNewsWorld](https://www.technewsworld.com/story/study-finds-most-restaurants-missing-from-ai-recommendations-180396.html) · [MapAtlas](https://mapatlas.eu/blog/83-percent-of-restaurants-dont-exist-in-chatgpt) · [Uberall via Las Vegas Sun](https://lasvegassun.com/news/2026/may/07/83-of-restaurants-are-invisible-in-ai-search-new-u/)
- [Promptado — Planos e Preços](https://promptado.com/planos)
- [GeoStack — Agência de GEO](https://geostack.com.br/agencia-de-geo-especialistas-em-otimizacao-para-ia-generativa/) · [Mapa das Agências de GEO](https://geostack.com.br/mapa-das-agencias-de-geo/)
- [Alexandre Caramaschi — Quanto custa consultoria GEO no Brasil em 2026](https://alexandrecaramaschi.com/artigos/quanto-custa-consultoria-geo)
- [Levolu — Quanto custa criar site profissional 2026](https://levolu.com.br/blog/quanto-custa-criar-site-profissional-2026) · [SEO Criação](https://seocriacao.com.br/quanto-custa-criar-um-site-profissional-em-2026/)
- Paper: Aggarwal et al., *GEO: Generative Engine Optimization*, ACM SIGKDD 2024, [arXiv:2311.09735](https://arxiv.org/abs/2311.09735)
