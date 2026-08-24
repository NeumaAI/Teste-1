# E0 — Declaração de cobertura

Mapa de iniciativas por Prontidão × Maturidade · gerado em 24/08/2026 · etapa E0, sem varredura, sem inventário, sem score.

---

## 1. Fontes acessíveis nesta sessão

| Fonte | Método real de acesso | O que devolve | Limitação técnica |
|---|---|---|---|
| **WIKIS** — repositório local `/home/user/Teste-1` | leitura direta de arquivo (`grep`/`cat`) + histórico git | 11 arquivos, 2.760 linhas, 3 commits, branch `claude/mapa-iniciativas-prontidao-re05vz`. Cobre **uma única frente**: produto de sites GEO/AIO | busca literal apenas; cobertura estreita — é uma frente, não o portfólio |
| **DRIVE** — Google Drive (`rodrigosouzap@gmail.com`) | `search_files` com sintaxe estruturada (`fullText contains 'x'`, `title contains 'x'`) | arquivos com id, título, data, pasta-pai; conteúdo lido depois por `read_file_content` | **busca literal, não semântica.** Sem score de similaridade. Exige rodar sinônimos de cada consulta |
| **NOTION** — workspace pessoal | `notion-search`; conteúdo integral por `notion-fetch` | páginas com id, título, URL, timestamp e trecho destacado | o backend respondeu `workspace_search`, **não** `ai_search`: é busca de workspace, **sem score de similaridade exposto** |
| **SKILLS** — `/root/.claude/skills/synced/` (79 skills) | leitura direta | registro de frentes codificado como skill (ex.: `geo-otimizacao-conteudo`, `resolve-estrategia`, `diagnostico-governanca-ia`) | fonte de **intenção declarada**, não de execução. Skill descreve método, raramente prova pagador |

## 2. Fontes inacessíveis

| Fonte | Motivo | O que destrava |
|---|---|---|
| **RAG_VECTOR** — índice vetorial pessoal | **não existe nesta sessão.** Nenhuma ferramenta de embedding ou busca vetorial exposta; nenhum diretório de índice em `/home/user` ou `/root` | (a) caminho de um índice local que eu possa ler; ou (b) endpoint/MCP de busca vetorial; ou (c) sua autorização para **substituir** a E1 por varredura literal+sinônimos em Notion/Drive |
| **CARDS** — base de cards de iniciativas | não identificada. A busca encontrou referência a um database (`📋 RG de Teses`, citado em *⚖️ Teses Jurídicas — Hub do Escritório*), mas **não confirmei** que seja a base de cards de iniciativas, nem se existe outra | URL ou id do database de cards. Sem isso, `CARDS` sai da E2 e o painel de cobertura registra a lacuna |
| **HISTÓRICO DE CONVERSAS** | não é base consultável por API nesta sessão | nada — fica declarado como não varrido |

## 3. Consequência direta sobre o protocolo

1. **A E1 como escrita não roda.** Sem RAG vetorial, "top-k = 12 acima do limiar" não tem referente. Ou você fornece o índice, ou a E1 é substituída pelo procedimento do item 4.
2. **`LIMIAR_SIMILARIDADE` é inaplicável nas fontes disponíveis.** Nenhuma delas expõe score. Fixar 0,75 seria número inventado — o campo fica `NULO`.
3. **Risco de cobertura assimétrica.** O repositório detalha uma frente (GEO/AIO) em 2.760 linhas; as demais frentes vivem em Notion/Drive com granularidade menor. Sem correção, a única frente com wiki tende a dominar o inventário por volume de âncora, não por mérito.

## 4. Parâmetros que vou usar (substituição declarada)

| Parâmetro | Valor | Justificativa |
|---|---|---|
| Limiar de similaridade | `NULO` | nenhuma fonte expõe score |
| Critério de retenção substituto | booleano: o resultado entra se contiver **âncora literal ≤200c** que satisfaça os três testes (objeto / pagador / registro). Sem âncora → `SEM_LASTRO` | mantém a regra 1 sem fabricar métrica |
| Top-k | 12 por consulta e por fonte | conforme anexo |
| Chunk recuperado | Notion: bloco/página inteira via `notion-fetch`. Drive: arquivo inteiro até 5 MiB. Repo: arquivo inteiro | as fontes não fatiam em chunks; o "id do chunk" vira `URL da página` / `id do arquivo Drive` / `caminho:linha` |
| Sinônimos | obrigatórios nas 12 consultas, em PT-BR, por serem buscas literais | compensa a ausência de semântica |

## 5. Variáveis do anexo ainda em branco

- `JANELA_HORAS_SEMANA` = **não informado** — trava a dimensão P5 (Operação) em `NULO` para toda iniciativa
- `RESTRIÇÕES_DE_VÍNCULO` = **não informado** — trava P6 (Risco) e o kill switch nº 2
- `DATA_DO_MAPA_ANTERIOR` = **não informado** — só afeta a E6, opcional

## 6. Decisão que cabe a você

- **(A)** fornecer índice vetorial → E1 roda como escrita
- **(B)** autorizar a substituição do item 4 → a E1 vira varredura literal+sinônimos em Notion, Drive, repo e skills, com a limitação registrada no painel de cobertura da E5
- **(C)** parar aqui

Em qualquer caso, informe `JANELA_HORAS_SEMANA` e `RESTRIÇÕES_DE_VÍNCULO`, ou P5 e P6 nascem `NULO` e toda iniciativa cai em `DADOS_INSUFICIENTES` por acúmulo de dimensões nulas.

**PORTÃO E0 aberto. Aguardando `PORTÃO OK` + escolha entre A, B e C.**
