---
task: "Revisão de Qualidade — Checklist Obrigatório (15 itens) + Filtro Visual Fase 1 (itens 16-20)"
order: 1
input:
  - site_html: squads/prospeccao-sites/output/{run_id}/{slug}/site.html
  - email: squads/prospeccao-sites/output/{run_id}/emails.md (seção do negócio)
  - briefing: squads/prospeccao-sites/output/{run_id}/{slug}/briefing.md
output:
  - revisao: Veredicto APROVADO ou REJEITADO com checklist completo e feedback acionável
---

# Revisão de Qualidade — Checklist Obrigatório + Filtro Visual (Fase 1)

Revisa site HTML e email de proposta contra o checklist obrigatório e o filtro visual de fase 1. Um item obrigatório falhando = REJEITADO — mas respeitando a TRAVA DE FASE 1 abaixo.

## 🔒 TRAVA DE FASE 1 (Prospecção) — o que Vera NÃO pode rejeitar

Estamos em **fase de prospecção**: o site é uma amostra criada ANTES do contato, sem acesso ao material privado do negócio (pós-venda). Por isso, Vera **NUNCA rejeita** um site por faltar:
- **Depoimento textual real** — texto de avaliação é bônus. Sem 3 avaliações, o Diego usa prova social agregada (nota + volume) — isso é correto, não é falha.
- **Antes/depois real** — depende de fotos privadas do cliente. Não exigir.
- **Preço / tabela de valores** — não temos os preços reais. Ausência é correta.
- **Feed do Instagram embutido / posts reais** — depende de acesso/integração privada. Uma chamada com link para o perfil basta.

Vera só cobra, na fase 1, o que é **possível sem conteúdo privado**: imagens relevantes ao nicho, hero cheio, prova visual do serviço/produto, layout não-genérico, CTAs variados, WhatsApp na identidade, dados de contato reais. Rejeitar por falta de conteúdo privado é erro da Vera.

## Process

### Step 1 — Carregar artefatos de referência

1. Ler o `briefing.md` do negócio — é a fonte de verdade para dados reais
2. Ler o `site.html` do negócio
3. Ler a seção do negócio em `emails.md`
4. Verificar se há fotos reais em `output/{run_id}/{slug}/imagens-insta/` (se houver, o site deve usá-las; se não, imagens da API Unsplash)

### Step 2 — Executar o checklist (obrigatórios + filtro visual)

Para cada item, marcar ✅ (OK) ou ❌ (FALHA) com observação específica. Aplicar sempre a TRAVA DE FASE 1:

**ITENS DE AUTENTICIDADE (mais críticos)**

**Item 1 — Prova social honesta (depoimento textual é BÔNUS — TRAVA FASE 1)**
- O site tem uma seção de prova social? Ela pode ser de dois tipos, ambos válidos:
  * **Modo texto:** 3 cards de depoimento com texto real (quando o briefing tem 3+ avaliações textuais), OU
  * **Modo agregado:** nota + volume / "% recomendam" / tempo de mercado quando NÃO há 3 avaliações textuais.
- 🔒 **NUNCA rejeitar por falta de depoimento textual** — texto é bônus. A ausência de cards de depoimento, com prova agregada honesta no lugar, é ✅.
- ✅ se: seção de prova social presente (texto OU agregada, honesta) | ❌ se: avaliação/depoimento INVENTADO, ou número/selo inventado, ou divergência do briefing

**Item 2 — Estrutura da prova social conforme o modo**
- Modo texto: cada card tem estrelas + texto entre aspas + avatar com inicial + nome + fonte.
- Modo agregado: a nota/volume/ângulo exibido bate com o briefing (sem número inventado) e segue a regra de força (volume baixo não estampado cru).
- ✅ se: a forma usada está bem montada e fiel ao briefing | ❌ se: card incompleto no modo texto, ou dado agregado inventado/divergente

**Item 3 — Telefone/WhatsApp real**
- O número no botão flutuante WhatsApp tem formato completo? `wa.me/55DDNNNNNNNNN`
- Nunca aceitar `wa.me/55?` ou `wa.me/55` sem DDD e número
- Bate com o número no briefing?
- ✅ se: número completo e verificado | ❌ se: placeholder ou número incompleto

**Item 4 — Links de WhatsApp completos**
- Todos os links `wa.me` no site têm número completo?
- ✅ se: todos completos | ❌ se: qualquer link incompleto

**Item 5 — Horário de funcionamento**
- O horário exibe dias e horas específicas (ex: "Seg-Sex 09h-18h")?
- Nunca aceitar "consulte por telefone" ou "horário a confirmar"
- ✅ se: horário específico OU campo conscientemente omitido | ❌ se: placeholder ou "consulte"

**Item 6 — Email**
- O email aparece corretamente OU foi conscientemente omitido?
- Nunca aceitar "email@email.com" ou "[inserir email]"
- ✅ se: email real OU ausência intencional sem placeholder | ❌ se: placeholder visível

**ITENS DE QUALIDADE VISUAL**

**Item 7 — Imagens reais (5 mínimo): fotos do Instagram OU API oficial da Unsplash**
- Contar imagens distintas em `<img>` e `background-image: url()`. Fontes válidas:
  * **Fotos reais do Instagram** — arquivos locais referenciados de `imagens-insta/` (quando o usuário baixou no checkpoint 8). NÃO precisam de `onerror`.
  * **API oficial da Unsplash** — URLs do domínio `images.unsplash.com/photo-...` (vindas da resposta real da API). Cada `<img>` remota DEVE ter `onerror` para `picsum.photos`.
- 🚫 **`source.unsplash.com` é PROIBIDO** (endpoint descontinuado que serve imagem aleatória) → qualquer ocorrência é ❌.
- ✅ se: 5+ imagens distintas e relevantes ao nicho (Instagram e/ou images.unsplash.com), com onerror nas `<img>` remotas | ❌ se: <5, qualquer `source.unsplash.com`, ou `<img>` remota sem onerror

**Item 8 — SVG em feature-icons**
- Os ícones da seção "Por que nos escolher" / "Nosso Compromisso" / "Diferenciais" são SVG inline?
- Emoji como ícone de feature = ❌
- ✅ se: SVG inline com `<svg>` + `<path>` | ❌ se: emoji no lugar de ícone

**Item 9 — Badge de destaque nos cards**
- Um dos cards de cardápio/serviço/modalidade tem badge visível ("Mais Pedido", "Destaque", "Especialidade da Casa")?
- ✅ se: badge presente em pelo menos 1 card | ❌ se: todos os cards idênticos sem diferenciação

**Item 10 — Seção de diferenciais/processo (posição pelo mapa do nicho)**
- Existe uma seção com 3-4 bullets sobre valores/processo? A posição segue o mapa do nicho (não é fixa entre Sobre e Cardápio).
- Pode ter outros nomes conforme o nicho: "Nosso Compromisso", "Como Trabalhamos", "Processo", "Benefícios", "Diferenciais".
- ✅ se: seção presente com conteúdo específico do nicho | ❌ se: ausente

**Item 11 — Variação de CTAs**
- Os CTAs ao longo do site variam de linguagem e intenção?
- Contar quantos CTAs dizem exatamente "Falar no WhatsApp" — se todos dizem o mesmo, ❌
- ✅ se: CTAs variam (ex: "Agendar", "Ver cardápio", "Conhecer", "Ligar") | ❌ se: todos iguais

**ITENS DE ESTRUTURA**

**Item 12 — Stats no hero**
- O hero tem stats reais no canto inferior direito (nota, avaliações, anos, ticket)?
- ✅ se: 2-3 stats com números reais visíveis | ❌ se: stats ausentes ou com dados fictícios

**Item 13 — Animações**
- `slowZoom` está no hero background (verificar no CSS)?
- `fadeUp` com delays escalonados está no texto do hero?
- Hover nas cards tem `translateY` ou `transform`?
- ✅ se: todos os 3 presentes | ❌ se: qualquer um ausente

**Item 14 — Paleta de cores**
- O CSS define mais de 2 cores principais? (`--primary`, `--secondary`, `--accent` + 2 neutras)
- ✅ se: 5+ variáveis de cor definidas | ❌ se: apenas 2 cores

**Item 15 — Tipografia por nicho**
- A fonte display não é Poppins?
- É adequada para o nicho (Playfair/Cormorant para gastronomia/beleza; Oswald/Bebas para academia/auto)?
- ✅ se: fonte correta para o nicho | ❌ se: Poppins ou inadequada

**ITENS DE REJEIÇÃO VISUAL (fase 1 — só o que é possível sem conteúdo privado)**

**Item 16 — Imagens relevantes ao nicho**
- Toda imagem mostra o produto/serviço do negócio? (prato num restaurante, tatuagem num estúdio, bolo numa doceria)
- ❌ se: qualquer imagem genérica/aleatória sem relação com o nicho (paisagem, prédio, foto de banco fora de contexto)
- ✅ se: todas relevantes ao nicho

**Item 17 — Hero cheio, sem espaço morto**
- O hero tem imagem do nicho preenchendo a tela (full-bleed) ou a coluna direita (split)?
- ❌ se: lado direito vazio/cinza parecendo imagem quebrada; hero só com cor chapada sem imagem carregada
- ✅ se: hero visualmente cheio com imagem real

**Item 18 — Prova visual do serviço/produto cedo**
- Existe uma seção de prova visual (portfólio/galeria/fotos do produto/antes-depois quando houver foto) e ela aparece logo após o hero, não enterrada no fim?
- 🔒 Fase 1: "antes-depois" só é exigível se há foto disponível — a ausência dele NÃO reprova; o que se cobra é existir prova visual do trabalho cedo.
- ❌ se: nenhuma prova visual do trabalho, ou prova visual jogada para o rodapé
- ✅ se: prova visual presente nas primeiras seções de conteúdo

**Item 19 — Não parece template genérico**
- O site tem identidade do nicho (tipografia, paleta, imagens, copy específicos) e não cara de modelo pronto trocado de nome?
- ❌ se: visual genérico de template, sem personalidade do nicho
- ✅ se: claramente desenhado para aquele negócio/nicho

**Item 20 — WhatsApp flutuante na identidade**
- O botão flutuante usa a cor da marca no fundo (verde só no ícone, se houver)?
- ❌ se: botão verde-neon gritante que destoa da paleta
- ✅ se: harmonizado com a paleta do site

### Step 3 — Verificar Email (Gold Standard — 9 blocos)

Comparar o email com o gold standard em `squads/prospeccao-sites/_references/email-padrao-sabor-do-ipiranga.md`.

a. **Bloco 1** presente: email abre com apresentação do Miguel antes de qualquer dado?
b. **Bloco 2** presente: elogio *interpreta* o dado ("é coisa séria" ou similar) — não só recita?
c. **Bloco 3** presente: transição de uma linha ("Justamente por isso..." ou variação)?
d. **Bloco 4** presente: problema construído como história, reconhece o que já funciona?
e. **Bloco 5** presente: ponte emocional com "Pensei:" ou similar?
f. **Bloco 6** presente: iniciativa no passado ("fui em frente", "já montei"), com 3-5 elementos reais?
g. **Bloco 7** presente: linha de referência aos screenshots com 👇?
h. **Bloco 8** presente: convite sem pressão com "Não tem nenhum compromisso"?
i. **Bloco 9** presente: assinatura "Abraço, / Miguel Magalhães Silveira / 12974062797"?
j. Nenhuma frase proibida: "O problema:", "Vi que vocês têm X estrelas", "Posso te mostrar?", "O que achou?", "Sem compromisso" sozinho?
k. Palavras no corpo entre 150 e 260?
l. Assunto no formato novo (sem dois pontos + provocação)?
m. Sem menção a preços ou proposta comercial?

### Step 4 — Calcular Veredicto

- 🔒 **Antes de marcar qualquer ❌, aplicar a TRAVA DE FASE 1**: se a "falha" for ausência de depoimento textual real, antes/depois real, preço ou feed Instagram embutido, NÃO é ❌ — é comportamento correto da fase de prospecção.
- REJEITADO se: qualquer dos 15 itens do checklist OU qualquer item visual (16-20) marcado como ❌
- REJEITADO se: qualquer item de email (a-m) falhar
- APROVADO se: todos os 15 itens ✅, todos os itens visuais (16-20) ✅ E todos os itens de email (a-m) ✅

### Step 5 — Documentar e Salvar

Salvar revisão em `squads/prospeccao-sites/output/{run_id}/revisao.md`

## Output Format

```markdown
# Revisão — [Nome do Negócio]
Data: [data]

## Checklist (15 itens) + Filtro Visual Fase 1 (16-20)

### Autenticidade
- [1] ✅/❌ Prova social honesta (texto OU agregada): [modo usado]
- [2] ✅/❌ Estrutura da prova social conforme o modo: [observação]
- [3] ✅/❌ WhatsApp real: [número encontrado] vs [número no briefing]
- [4] ✅/❌ Todos os links completos: [observação]
- [5] ✅/❌ Horário específico: [horário encontrado]
- [6] ✅/❌ Email: [email encontrado / omitido intencionalmente]

### Qualidade Visual
- [7] ✅/❌ Imagens reais (Instagram OU images.unsplash.com, sem source.unsplash.com): [N] encontradas
- [8] ✅/❌ SVG em feature-icons: [observação]
- [9] ✅/❌ Badge de destaque: [card destacado ou ausente]
- [10] ✅/❌ Seção diferenciais/processo (posição pelo mapa do nicho): [nome da seção]
- [11] ✅/❌ Variação de CTAs: [CTAs encontrados]

### Estrutura
- [12] ✅/❌ Stats no hero: [stats encontrados]
- [13] ✅/❌ Animações: slowZoom [✅/❌] | fadeUp [✅/❌] | hover [✅/❌]
- [14] ✅/❌ Paleta: [N] variáveis de cor
- [15] ✅/❌ Tipografia: [fonte display encontrada]

### Filtro Visual Fase 1 (só o que é possível sem conteúdo privado)
- [16] ✅/❌ Imagens relevantes ao nicho: [observação]
- [17] ✅/❌ Hero cheio, sem espaço morto: [observação]
- [18] ✅/❌ Prova visual do trabalho cedo: [observação]
- [19] ✅/❌ Não parece template genérico: [observação]
- [20] ✅/❌ WhatsApp flutuante na identidade: [observação]

## Revisão do Email

- Nome correto: ✅/❌
- Dado real citado: ✅/❌ ([dado])
- Palavras: [N] — ✅/❌
- CTA é pergunta: ✅/❌
- Assunto OK: ✅/❌
- Sem preço: ✅/❌

---
Ponto positivo: [algo bem feito]

## CORREÇÕES OBRIGATÓRIAS
[Listar apenas itens ❌, numerados]
1. [Item X] — [o que está errado] — [como corrigir] — **Agente: Diego Digital**

## VEREDICTO: [APROVADO / REJEITADO]
[Motivo em 1 linha]
```

## Veto Conditions

Reject (don't produce output) and redo if ANY are true:
1. Veredicto ausente — deve ser APROVADO ou REJEITADO
2. Algum dos 15 itens do checklist OU dos itens visuais (16-20) não verificado
3. Revisão feita sem comparar a prova social do HTML com o briefing
4. Site rejeitado por falta de conteúdo privado (depoimento textual, antes/depois, preço ou feed Instagram) — viola a TRAVA DE FASE 1
