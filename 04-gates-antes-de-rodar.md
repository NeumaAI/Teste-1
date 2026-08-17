# Parte 4 — O que precisa acontecer antes de vender a primeira unidade

Cinco gates. Os dois primeiros são bloqueantes: se falharem, o produto não existe na forma desenhada. Custo total: **cerca de 5 horas.**

---

## 🔴 Gate 1 — O teste dos 30 minutos (BLOQUEANTE)

**Origem:** sua própria Terceira Camada, escrita hoje. É o único gate que você mesmo já mandou fazer e não foi feito.

**O que fazer:** escolher **um** bairro e **uma** categoria (ex.: clínicas odontológicas na Aldeota). Montar 15–20 perguntas que um cliente real faria. Rodar em ChatGPT, Gemini, Perplexity e Claude. Registrar quem é citado.

**Como ler o resultado:**

| Resultado | Leitura | Decisão |
|---|---|---|
| As IAs citam **nomes de negócios locais** e sempre os mesmos 3–5 | Janela **aberta e disputada** | ✅ **GO.** Este é o melhor cenário: existe o "concorrente aparecendo" que faz o pitch funcionar |
| As IAs citam nomes locais, mas variam muito entre si | Janela **aberta e frouxa** | ✅ **GO**, com pitch ajustado — o argumento vira consistência, não substituição |
| As IAs respondem com **agregadores** (TripAdvisor, Doctoralia, iFood, Google Maps genérico) e nenhum nome próprio | **O pitch morre** — não há concorrente a mostrar | 🔄 **REDESENHAR.** Produto vira "aparecer no agregador que a IA cita", que é outro produto |
| As IAs se recusam a recomendar ou dizem "não posso indicar" | Categoria fora do jogo | ❌ trocar de categoria e repetir |

**Custo:** 30 minutos. **Sem isto, nada mais deve ser feito.**

---

## 🔴 Gate 2 — Confirmar se o motor Python existe (BLOQUEANTE para o planejamento)

`[V]` Verifiquei: **não está neste ambiente.** Nem no repositório, nem nas skills, nem em lugar nenhum do sistema de arquivos.

**Três possibilidades, e você é o único que sabe qual é:**
1. Está em outra máquina ou outro repositório → me aponte, eu integro
2. Existe como conversa/rascunho, nunca virou código → é escopo de trabalho, ~8–12h `[I]`
3. Você está se lembrando da skill (que *declara* dependência de Python no frontmatter mas não tem código) → o motor não existe

**Por que importa:** muda a estimativa de tempo do Raio-X de 20 min para ~2 min por alvo. Com 40 alvos por bairro, é a diferença entre 13 horas e 1 hora e meia. Não bloqueia a venda das 3 primeiras unidades — bloqueia a escala.

---

## 🟡 Gate 3 — Construir o template do site

A única peça de engenharia real que falta. Sem ela, "10 dias úteis" é promessa, não capacidade.

**Escopo:** HTML estático, 5–7 páginas, blocos de schema JSON-LD parametrizados, `llms.txt` e `robots.txt` gerados, LCP < 2,5s, sem dependência de JS para conteúdo.
**Estimativa:** 12–16h `[I]` para a v1.
**Quando:** pode acontecer **junto** com a unidade #1 — o caso zero é o que valida o template.

---

## 🟡 Gate 4 — Resolver as duas contradições internas

Duas decisões suas, ambas de 5 minutos, ambas com consequência real:

1. **O piso de R$ 2.000/mês.** A Nexum Visible registra como anti-padrão vender retainer abaixo disso. Este SKU propõe R$ 690/mês. Ou a regra passa a ser específica da Nexum Visible (recomendado), ou o recorrente daqui morre. Escolha uma e **atualize o documento perdedor** — senão vira negociação toda vez.

2. **Site sim ou não.** Três documentos seus vedam criação de site. Este produto a inclui. Se você aceitar a inversão (recomendado, com a ressalva de vender como veículo e não como entregável), **a Nexum Visible §1 precisa ser corrigida** para dizer que a vedação é da unidade Visible, não da casa.

Se não fizer isso, daqui a três meses um documento seu vai contradizer o outro numa reunião com cliente ou na cabeça da pessoa executora.

---

## 🟡 Gate 5 — Fechar o acordo com a pessoa executora antes de treinar

Definir por escrito, antes de qualquer treinamento:
- Modelo de remuneração (§7.3 — recomendado: R$ 800 fixo + 15%)
- Que ela **não vende fora do perfil de aceite**, e o que acontece se vender
- Que **três etapas passam por você** e não podem ser puladas por pressa
- Prazo de teste: 60 dias, 3 unidades, e o que caracteriza sucesso

**Motivo:** o risco documentado neste produto não é falta de demanda — é abandono na virada do mês 2. Acordo escrito no dia 1 é a única coisa barata que reduz isso.

---

## Ordem de execução

```
Gate 1  (30 min)  ──▶  se GO  ──▶  Gate 4  (5 min)  ──▶  Gate 5  (30 min)
   │                                     │
   │ se REDESENHAR                       ▼
   ▼                             Gate 3 + Unidade #1 em paralelo
volta pro desenho                        │
                                         ▼
                                  Gate 2 (quando quiser escalar)
```

**Caminho crítico até a primeira venda:** Gate 1 → Gate 4 → Gate 5 → Unidade #1 (que constrói o template) → Unidade #2 paga.
**Tempo total estimado até a primeira unidade paga `[I]`: 3 a 4 semanas.**

---

## Resumo em uma linha

Antes de montar site nenhum: **abra o ChatGPT, o Gemini, o Perplexity e o Claude, pergunte qual a melhor clínica/pizzaria/pet shop do bairro que você escolher, e veja quem aparece.** Trinta minutos. Se aparecer nome de negócio local, o produto existe e o resto deste pré-projeto vale. Se aparecer só TripAdvisor, a gente redesenha antes de gastar um dia.
