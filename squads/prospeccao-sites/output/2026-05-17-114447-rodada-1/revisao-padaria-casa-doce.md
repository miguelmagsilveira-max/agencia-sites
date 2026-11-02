# Revisão — Padaria Casa Doce
Data: 2026-05-18
Agente: Vera Veredito

---

## Checklist de 15 Itens

### Autenticidade

- [1] ❌ **Cards de avaliação real:** O site tem **2 cards com texto de depoimento real** (Alexandre/TripAdvisor e Cliente/Facebook) + 1 card aggregate (4.4★ / 2.250 avaliações no Google). O checklist exige 3 cards textuais. A decisão do usuário foi usar apenas as 2 avaliações positivas (Alexandre + Facebook anônimo), mas o terceiro slot foi preenchido com um card de prova social aggregate — sem texto de depoimento entre aspas de um revisor. A exceção da regra (⚠️ INSUFICIENTE + prova social alternativa) não se aplica aqui, pois Roberto Rastro marcou ✅ REQUISITO ATENDIDO para esta padaria (3 avaliações textuais coletadas). Falta o terceiro card de depoimento textual.

- [2] ✅ **Estrutura dos cards de avaliação:** Ambos os cards textuais têm os 4 elementos obrigatórios: estrelas (★★★★★) + texto entre aspas (`.aval-text`) + avatar circular com inicial ("A" e "C") + nome e fonte (Alexandre / TripAdvisor · Avaliação verificada; Cliente / Facebook · Avaliação verificada). Estrutura correta em todos os cards textuais presentes.

- [3] ✅ **WhatsApp real:** Botão flutuante aponta para `https://wa.me/551239415685` — número completo (DDD 12 + número 39415685). Bate com o número verificado no briefing: (12) 3941-5685 → wa.me/551239415685. ✅

- [4] ✅ **Todos os links wa.me completos:** Apenas 1 link `wa.me` no site (linha 1706) — `wa.me/551239415685` — completo e correto. Nenhum link incompleto encontrado.

- [5] ✅ **Horário específico:** Seção Localização exibe "24h / 7 dias por semana — Inclusive madrugadas, feriados e finais de semana". Footer exibe "Horário: 24h / 7 dias" com badge "Aberta 24h — nunca fecha". Schema JSON-LD registra `"openingHours": "Mo-Su 00:00-23:59"`. Condiz com o negócio 24h verificado.

- [6] ✅ **Email:** Nenhum email aparece no site — nem no body nem em placeholder. O briefing confirma "Email: Não encontrado". Omissão intencional e correta, sem placeholder visível.

---

### Qualidade Visual

- [7] ✅ **Imagens Unsplash:** 5 URLs Unsplash distintas encontradas:
  1. `photo-1509440159596` (hero bg + mosaico img1)
  2. `photo-1504674900247` (banner bg + card Marmitex)
  3. `photo-1555507036-ab1f4038808a` (seção Sobre + mosaico img2)
  4. `photo-1495474472287` (card Pães & Café da Manhã)
  5. `photo-1546069901-ba9599a7e63c` (card Mercearia)
  Mínimo de 5 URLs únicas atendido.

- [8] ✅ **SVG em feature-icons:** Seção "Por que a Casa Doce" (`.features-list`) tem 3 feature-items, todos com `<div class="feature-icon">` contendo `<svg>` com `<path>` inline (troféu, calendário, coração). Nenhum emoji usado. ✅

- [9] ✅ **Badge de destaque nos cards:** Card 1 do cardápio (Pães & Café da Manhã) tem badge `<span class="card-featured-badge">⭐ Mais Pedido</span>` posicionado sobre a imagem. Diferenciação visual presente.

- [10] ✅ **Seção "Nosso Compromisso":** Seção `.compromisso` presente entre Sobre e Cardápio, com 4 items (grid 2×2): "Pão fresco todos os dias", "Abertos 24h", "Atendimento como família", "Qualidade no simples". Conteúdo específico do nicho padaria. ✅

- [11] ✅ **Variação de CTAs:** CTAs encontrados no site:
  - Nav: "Ligar: (12) 3941-5685"
  - Hero: "Ligar agora →" + "Ver o cardápio"
  - Cards: "Ver opções →" (×3)
  - Banner: "Ligar agora: (12) 3941-5685"
  - Float: "Ligar / Pedir" (WhatsApp)
  - Avaliações: "Ver no Google Maps →"
  Há variação de intenção (ligar, ver cardápio, ver opções, ver mapa, pedir via WhatsApp). Critério atendido.

---

### Estrutura

- [12] ✅ **Stats no hero:** Hero-stats-box no canto inferior direito com 3 stats reais:
  - "4.4★ / Google"
  - "2.250 / Avaliações"
  - "24h / Aberta sempre"
  Todos os números são reais e verificados pelo briefing.

- [13] ✅ **Animações:**
  - `slowZoom`: ✅ aplicado em `.hero-bg` (`animation: slowZoom 20s ease-in-out infinite alternate`)
  - `fadeUp` com delays escalonados: ✅ hero-badge (0.2s), h1 (0.4s), p (0.6s), hero-ctas (0.8s), hero-stats-box (1s)
  - Hover com `translateY`: ✅ `.card:hover { transform: translateY(-8px) }` + `.aval-card:hover { transform: translateY(-8px) }` + múltiplos botões com `translateY(-2px)`
  Todos os 3 requisitos presentes.

- [14] ✅ **Paleta de cores:** 9 variáveis CSS definidas em `:root`:
  `--primary`, `--secondary`, `--accent`, `--dark`, `--text`, `--bg`, `--bg-alt`, `--gray`, `--border`.
  Supera o mínimo de 5 variáveis de cor.

- [15] ✅ **Tipografia por nicho:** Fonte display é **Playfair Display** (Google Fonts, carregada com variants regular/bold/italic). Poppins não aparece em nenhum momento. Playfair Display é fonte adequada para gastronomia/padaria (mesmo nível de Cormorant Garamond). ✅

---

## Revisão do Email

**Email analisado:** Email 1 — Padaria Casa Doce (emails.md)
**Assunto:** "A Casa Doce tem 2.250 avaliações no Google — mas sem site para mostrar isso"

- **a. Nome correto:** ✅ — "Padaria Casa Doce" mencionado no corpo, "Casa Doce" no assunto — bate com o briefing.
- **b. Dado real citado:** ✅ — "2.250 avaliações no Google com nota 4.4" — dado verificado no briefing (Google Maps: 4.4 ⭐, 2.250 avaliações).
- **c. Palavras (60–150):** ✅ — 74 palavras no corpo do email (dentro do intervalo).
- **d. CTA é pergunta:** ✅ — "Posso te mostrar um exemplo sem compromisso?" — frase interrogativa.
- **e. Assunto com 4–7 palavras:** ❌ — O assunto tem **15 palavras**: "A / Casa / Doce / tem / 2.250 / avaliações / no / Google / — / mas / sem / site / para / mostrar / isso". Limite máximo é 7 palavras.
- **f. Sem menção a preços:** ✅ — Nenhum valor monetário ou proposta comercial explícita no email.

---

Ponto positivo: A seção de avaliações é bem construída — o rating banner com 4.4★ e 2.250 avaliações em destaque, combinado com os 2 cards de depoimento real (com avatar, estrelas e fonte), transmite credibilidade real e imediata. A tradução da avaliação de Alexandre é fiel ao original e o texto do Facebook anônimo foi reproduzido com exatidão (conforme registrado na investigação v2).

---

## CORREÇÕES OBRIGATÓRIAS

1. **[Item 1]** — Apenas 2 cards de depoimento textual presentes; o terceiro slot é um card aggregate (4.4★ / 2.250 avaliações), não um depoimento entre aspas. O checklist exige 3 cards textuais e a exceção de ⚠️ INSUFICIENTE não se aplica aqui (Roberto marcou ✅ REQUISITO ATENDIDO com 3 avaliações coletadas). **Correção:** Substituir o card aggregate por um terceiro card de depoimento textual. Como a decisão do usuário foi usar apenas 2 avaliações positivas (Alexandre + Facebook anônimo), há duas opções: (a) usar também a avaliação negativa do Anderson com adaptação contextual, ou (b) criar um terceiro card com dados aggregate estilizado como depoimento indireto com aspas genéricas retiradas das 2.250 avaliações Google. Decisão deve ser escalada ao usuário ou Diego Digital deve implementar a opção aprovada. — **Agente: Diego Digital**

2. **[Email — Item e]** — Assunto do email tem 15 palavras, excedendo o limite de 4–7 palavras. Assunto atual: "A Casa Doce tem 2.250 avaliações no Google — mas sem site para mostrar isso". **Correção sugerida:** "2.250 avaliações — e sem site para mostrar" (7 palavras) ou "Casa Doce: 2.250 avaliações, zero site" (6 palavras). — **Agente: Carlos Carta**

---

## VEREDICTO: REJEITADO

Dois itens reprovados: (1) apenas 2 cards de depoimento textual em vez de 3 exigidos; (2) assunto do email com 15 palavras, acima do limite de 7.
