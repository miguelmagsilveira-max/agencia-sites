---
task: "Escrever Email de Proposta"
order: 1
input:
  - briefing: Briefing completo do negócio com avaliações reais
output:
  - email: Arquivo email.md com assunto, corpo e notas de envio
---

# Escrever Email de Proposta

Redige o **conteúdo aprovado** da proposta (`email.md`) que soa como mensagem de pessoa real — seguindo a estrutura de 9 blocos do gold standard em `squads/prospeccao-sites/_references/email-padrao-sabor-do-ipiranga.md`.

> **Tom padrão: INFORMAL e humano (rodada 4).** O conteúdo já deve sair na voz de conversa — caloroso, frases curtas, saudação pela hora, elogio interpretado, pergunta leve. É esse conteúdo que o **Eduardo reorganiza na sequência de etapas** (formato de envio padrão): **Blocos 1-2 → ETAPA 1 (abertura)**, **Blocos 4-5-8 → ETAPA 3 (contexto + dor + permissão)**, **Blocos 6-7 → ETAPA 5 (entrega do link + telas)**. Escrever os 9 blocos de forma que se quebrem limpo nessas três etapas. A mensagem única em 9 blocos é o **formato legado** (canal e-mail, quando fizer sentido mandar tudo de uma vez).

## Process

### Passo 0 — Ler o gold standard (SEMPRE PRIMEIRO)

Antes de qualquer outra coisa:
- Ler `squads/prospeccao-sites/_references/email-padrao-sabor-do-ipiranga.md`
- Internalizar o tom, o ritmo e a estrutura do email do Sabor do Ipiranga
- Só então avançar

### Passo 1 — Capturar screenshots reais via Playwright

a. Verificar que `squads/prospeccao-sites/output/{run_id}/{slug}/site.html` existe  
b. Iniciar servidor HTTP local: `cd squads/prospeccao-sites/output/{run_id} && python3 -m http.server 8765`  
c. Redimensionar viewport: `mcp__playwright__browser_resize` → width: 375, height: 812  
d. Navegar: `mcp__playwright__browser_navigate` → `http://localhost:8765/{slug}/site.html`  
e. Screenshot 1 — Hero (viewport inicial):
   - `mcp__playwright__browser_take_screenshot` → filename: `squads/prospeccao-sites/output/{run_id}/{slug}/screenshots/01-hero.png`  
f. Screenshot 2 — Seção de destaque (avaliações, cardápio ou serviços):
   - `mcp__playwright__browser_evaluate` → `() => { document.querySelector('#avaliacoes, #cardapio, #servicos, #modalidades').scrollIntoView(); }`
   - `mcp__playwright__browser_take_screenshot` → filename: `...screenshots/02-destaque.png`  
g. Screenshot 3 — Contato/localização:
   - `mcp__playwright__browser_evaluate` → `() => { document.querySelector('#localizacao, footer').scrollIntoView(); }`
   - `mcp__playwright__browser_take_screenshot` → filename: `...screenshots/03-contato.png`  
h. Se qualquer etapa falhar: **PAUSAR e avisar o usuário** — nunca prosseguir sem screenshots reais

### Passo 2 — Ler o briefing e identificar

- Nome exato do negócio
- Dado mais expressivo (nota + número de avaliações, ou seguidores, ou check-ins)
- Nicho e diferencial principal
- Canal de contato disponível (email / WhatsApp / telefone)
- Elementos reais do site criado pelo Diego (cardápio? modalidades? serviços? horários? fotos?)
- URL ao vivo do site: ler `squads/prospeccao-sites/output/{run_id}/{slug}/link-ao-vivo.txt` (gerado pelo Diego no deploy Vercel) — usada no Bloco 7

### Passo 3 — Construir o email nos 9 blocos

**Bloco 1 — Abertura humana** (1 linha)
```
Olá, tudo bem? Meu nome é Miguel, sou desenvolvedor web aqui de São Paulo.
```
Variações permitidas: "aqui de São José dos Campos" se fizer sentido contextual. Nunca abrir com dado, nunca abrir com nome do negócio.

**Bloco 2 — Como conheceu + elogio interpretado** (2-3 linhas)
```
Encontrei [o/a NEGÓCIO] pesquisando [NICHO] no Google e fiquei impressionado com [DADO REAL]. [INTERPRETAÇÃO: "é coisa séria" / "trabalho fala por si só" / "isso não é à toa" / "raro ver alguém com esse nível".]
```
- SEMPRE conta como encontrou (pesquisando no Google, no Maps, buscando [nicho])
- SEMPRE cita o dado real mas o interpreta — nunca só recita
- A interpretação deve soar como pensamento genuíno, não como template

**Bloco 3 — Transição** (1 linha curta)
```
Justamente por isso resolvi entrar em contato.
```
Variações: "E é justamente por isso que cheguei até vocês." / "Foi isso que me fez querer falar com vocês."

**Bloco 4 — Problema como história** (3-5 linhas)
```
Hoje, quando alguém pesquisa "[BUSCA DO CLIENTE POTENCIAL]" no Google, a primeira coisa que aparece é [O QUE JÁ EXISTE] — e vocês aparecem bem [ou: vocês já têm boa presença]. Mas o segundo passo que quase todo cliente dá é [COMPORTAMENTO REAL: procurar o site pra ver o cardápio / ver fotos antes de decidir / checar horários / comparar opções]. Sem um site, uma parte dessas pessoas simplesmente vai para o concorrente que tem.
```
- Sempre reconhecer o que já funciona ANTES de mostrar a falha
- Construir cena com o cliente potencial em ação — não dizer apenas "vocês não aparecem"
- Adaptar ao nicho: restaurante ≠ academia ≠ salão ≠ borracharia no que o cliente busca e faz

**Bloco 5 — Ponte emocional** (1 linha)
```
Pensei: um(a) [TIPO DE NEGÓCIO] com esse nível de qualidade merece uma presença digital à altura.
```
Adaptar o complemento ao negócio: "uma padaria com essa clientela fiel", "uma academia com essa nota", "um salão com tantos anos de carinho", "uma borracharia que atende 24h".

**Bloco 6 — Iniciativa concreta** (2-3 linhas)
```
Aí fui em frente e já deixei no ar uma versão do site pra vocês verem como ficaria — com [ELEMENTO 1], [ELEMENTO 2], [ELEMENTO 3] e tudo mais. Ficou bonito de verdade.
```
- Verbos no passado: "fui em frente", "já montei", "já deixei no ar", "preparei" — NUNCA futuro
- O site agora está DE FATO publicado e no ar (deploy do Diego no Vercel), então a linguagem pode refletir isso com naturalidade: "já deixei no ar", "já coloquei pra rodar", "já está no ar pra você ver". Continua sendo verdade literal — o site existe online.
- Listar 3-5 elementos REAIS do site daquele negócio (usar o que Diego realmente construiu)
- Fechar com auto-elogio casual: "ficou bonito de verdade" / "ficou muito bom" / "gostei do resultado"

**Bloco 7 — Referência aos anexos + link ao vivo** (1-2 linhas)
```
Anexei algumas telas aqui 👇 e, se quiser ver funcionando no seu próprio celular, é só abrir esse link: [URL_AO_VIVO]
```
- A [URL_AO_VIVO] é lida de `squads/prospeccao-sites/output/{run_id}/{slug}/link-ao-vivo.txt` (gerado pelo Diego no deploy)
- O link e os screenshots CONVIVEM — não substituir um pelo outro. As telas dão o primeiro impacto; o link deixa explorar de verdade.
- Este é o único lugar onde 👇 é aceito. Nunca antes, nunca depois.
- Se o `link-ao-vivo.txt` não existir, PAUSAR e avisar o usuário — não inventar URL nem omitir o link silenciosamente.

**Bloco 8 — Convite sem pressão, terminando em pergunta fechada** (2-3 linhas)
```
Se fizer sentido, posso te explicar como funciona pra deixar isso no ar de vez — é rápido e sem compromisso nenhum. Quer que eu te mande os detalhes?
```
- Modelo de referência acima — Carlos adapta levemente por negócio, mantendo o espírito.
- TERMINA SEMPRE com uma **pergunta fechada (sim/não)**, fácil de responder no celular em segundos: "Quer que eu te mande os detalhes?" / "Posso te explicar como funciona?" / "Quer ver como fica no ar de vez?"
- A pergunta pede **permissão para continuar a conversa** — NUNCA pede decisão de compra ("vamos fechar?", "topa contratar?", "fechamos?").
- SEMPRE manter "sem compromisso" na frase ("sem compromisso nenhum").
- PROIBIDO pergunta aberta ("o que achou?", "o que você acha?") — dão trabalho de responder e não convertem.
- PROIBIDO tom de vendedor ("não perca essa oportunidade", "última chance", "promoção").
- Adaptar o canal de resposta ao disponível quando fizer sentido (responder o email / chamar no WhatsApp), mas o fecho é sempre a pergunta fechada de permissão.

**Bloco 9 — Assinatura humana**
```
Abraço,
Miguel Magalhães Silveira
12974062797
```
SEMPRE esta forma. NUNCA "Miguel Silveira — Sites para comércios locais — São José dos Campos/SP". NUNCA só "Miguel". NUNCA "Agência de Sites".

### Passo 4 — Escrever o assunto

Formato novo — curto, como um amigo escreveria:
- "Fiz um site para a Padaria Casa Doce"
- "Algo que pensei pra Big Skull"
- "Site pro Salão Adriana — dá uma olhada"
- "Lembrei da Pizzaria dos Amigos"
- "Algo pra Borracharia A Shalom"

Proibido:
- Assunto com dois pontos + provocação: "Big Skull: 4.81★ invisível no Google" ❌
- Caixa alta ❌
- Emoji no assunto ❌

### Passo 5 — Revisar antes de salvar

Checar mentalmente:
- [ ] Gold standard foi lido antes de escrever?
- [ ] Os 9 blocos estão na ordem correta?
- [ ] 180-240 palavras?
- [ ] Bloco 1 apresenta Miguel antes de qualquer dado?
- [ ] Bloco 2 interpreta o dado (não só recita)?
- [ ] Bloco 4 reconhece o que já funciona antes de mostrar a falha?
- [ ] Bloco 6 usa verbos no passado?
- [ ] Bloco 7 inclui o link ao vivo (de link-ao-vivo.txt) ALÉM dos screenshots?
- [ ] Bloco 8 termina em pergunta fechada de permissão (sim/não) e mantém "sem compromisso"?
- [ ] Bloco 8 NÃO pede decisão de compra nem usa pergunta aberta?
- [ ] Bloco 9 usa "Abraço, / Miguel Magalhães Silveira / 12974062797"?
- [ ] Nenhuma frase dos anti-padrões proibidos?
- [ ] Screenshots capturados e referenciados?

### Passo 6 — Salvar

Salvar em `squads/prospeccao-sites/output/{run_id}/{slug-negocio}/email.md`

## Output Format

```markdown
## Assunto
[assunto no formato novo]

## Corpo
Olá, tudo bem? Meu nome é Miguel, sou desenvolvedor web aqui de São Paulo.

[Bloco 2 — elogio interpretado]

[Bloco 3 — transição]

[Bloco 4 — problema como história]

[Bloco 5 — ponte emocional]

[Bloco 6 — iniciativa concreta]

Anexei algumas telas aqui 👇 e, se quiser ver funcionando no seu próprio celular, é só abrir esse link: [URL_AO_VIVO]

[Bloco 8 — convite sem pressão terminando em pergunta fechada de permissão]

Abraço,
Miguel Magalhães Silveira
12974062797

📎 Anexos: `01-hero.png` · `02-destaque.png` · `03-contato.png`
📁 `squads/prospeccao-sites/output/{run_id}/{slug}/screenshots/`
🔗 Link ao vivo: [URL_AO_VIVO]

## Notas de Envio
- Destinatário: [email, WhatsApp ou canal disponível]
- Dado real usado no elogio: [qual dado + qual interpretação]
- Elementos do site listados no Bloco 6: [lista]
- Screenshots capturados: [lista dos PNGs]
- Link ao vivo usado no Bloco 7: [URL de link-ao-vivo.txt]
- Pergunta fechada do Bloco 8: [qual pergunta de permissão]
- Palavras no corpo: [contagem]
- Horário sugerido: terça/quarta/quinta às 9h (email) | fim de tarde (WhatsApp)
- Follow-up: após 3 dias sem resposta
```

## Anti-Padrões Proibidos (veto imediato)

NUNCA usar estas frases ou variações próximas:
- "Vi que vocês têm X estrelas..."
- "O problema: sem site..."
- "Você perde clientes ativamente..."
- "O que achou?" / "O que você acha?" — pergunta aberta que dá trabalho de responder
- "Vamos fechar?" / "Topa contratar?" / "Fechamos?" — pergunta de decisão de compra (o Bloco 8 pede permissão pra continuar, não decisão)
- "Não perca essa oportunidade" / "Última chance" / "Promoção" — tom de vendedor
- "Modelo especialmente pra [Negócio]"
- Qualquer assunto com dois pontos + provocação

Nota: o Bloco 8 PODE e DEVE usar uma pergunta fechada de permissão como "Quer que eu te mande os detalhes?" ou "Posso te explicar como funciona pra deixar isso no ar de vez?". Isso não é pressão — é convite a continuar a conversa. O que está proibido é a pergunta aberta, a pergunta de compra e o tom de vendedor acima.

## Veto Conditions

Reject and redo if ANY are true:
1. Gold standard não foi lido antes de escrever
2. Qualquer dos 9 blocos ausente ou fora de ordem
3. Menos de 150 ou mais de 260 palavras no corpo
4. Bloco 1 ausente ou abre com dado ao invés de apresentação
5. Bloco 2 recita dado sem interpretar
6. Bloco 4 acusa sem reconhecer o que funciona
7. Bloco 6 usa verbos no futuro ("posso montar", "vou criar")
8. Frase do anti-padrão proibido presente no corpo
9. Screenshots ausentes — arquivos PNG não existem em `screenshots/`
10. Screenshots gerados por IA ou descritos como texto
11. Assinatura não é "Abraço, / Miguel Magalhães Silveira / 12974062797"
12. Bloco 7 não inclui o link ao vivo (de link-ao-vivo.txt) junto dos screenshots
13. Bloco 8 não termina em pergunta fechada de permissão, OU usa pergunta aberta / pergunta de decisão de compra / tom de vendedor
