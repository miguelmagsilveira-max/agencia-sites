# Revisão — Salão de Beleza Adriana
Data: 2026-05-18
Revisora: Vera Veredito — Especialista em Qualidade

---

## Checklist de 15 Itens

### Autenticidade

- [1] ✅ Cards de avaliação real: **Exceção aplicada.** Roberto Rastro marcou ⚠️ AVALIAÇÕES INSUFICIENTES (0 avaliações textuais públicas encontradas). O site usa seção "Nossa Comunidade" com prova social alternativa de dados reais verificáveis: 665 curtidas Facebook, 103 check-ins, @sdbelezaadriana ativo. Não há reviews inventadas — substituição justificada e documentada.

- [2] ❌ Estrutura dos cards: Não existem cards de depoimento textual no site. A exceção do Item 1 autoriza a ausência de reviews textuais, mas o Item 2 exige que, quando cards existem, tenham os 4 elementos obrigatórios. Como os cards de prova social alternativa são puramente numéricos (sem texto entre aspas, sem avatar circular com inicial, sem nome de cliente, sem estrelas), o item não é atendido. Nenhum dos 3 cards da seção "Nossa Comunidade" tem os 4 elementos: estrelas + texto entre aspas + avatar com inicial + nome.

- [3] ✅ WhatsApp real: `wa.me/5512997946928` encontrado no botão flutuante e em todos os CTAs. Bate com o número do briefing: (12) 99794-6928 → 55 + 12 + 997946928 = `5512997946928`. Número completo e verificado.

- [4] ✅ Todos os links completos: 8 ocorrências de `wa.me/5512997946928` no site (hero, 3 cards de serviço, banner noivas, CTA final, footer, botão flutuante). Todos com número completo.

- [5] ✅ Horário específico: "Segunda a Sexta: 09h00–18h00 / Sábado: 09h00–12h00 / Domingo: Fechado" — específico e bate com o briefing (Seg–Sex 09h00–18h00 | Sáb 09h00–12h00). Também exibido no footer e no Schema LD+JSON.

- [6] ✅ Email: Não aparece no site. Ausência intencional — o agente registrou "email não encontrado" no briefing e Carlos Carta indicou entrega via DM Instagram ou WhatsApp. Nenhum placeholder visível como "email@email.com".

---

### Qualidade Visual

- [7] ❌ Imagens Unsplash: **Apenas 2 URLs distintas encontradas.** Mínimo exigido: 5.
  - `photo-1560066984-138dadb4c035` — usada 6× (hero background, sobre img, serviço card 1, serviço card 3, mosaico-img1, schema JSON)
  - `photo-1522337360788-8b13dee7a37e` — usada 4× (banner noivas background, sobre img — duplicada no card, serviço card 2, mosaico-img2)
  - Total de fotos distintas no domínio unsplash.com: **2** (muito abaixo do mínimo de 5)

- [8] ✅ SVG em feature-icons: Todos os ícones usam `<svg>` inline com `<path>` e atributos adequados. Seção "Nosso Compromisso": 4 ícones SVG (ouvido, estrela, coração, escudo). Seção "Por que nos escolher" (features-list): 3 ícones SVG (câmera/Instagram, pin de localização, bússola). Nenhum emoji usado como ícone de feature-icon.

- [9] ✅ Badge de destaque: Card "Noivas & Madrinhas" tem `<span class="servico-badge">👰 Especialidade</span>` — badge visível e diferenciado dos demais cards.

- [10] ✅ Seção "Nosso Compromisso": Seção `.compromisso` presente entre "Sobre" e "Serviços", com 4 bullets sobre valores do nicho: (1) escuta o cliente antes de começar, (2) produtos de qualidade comprovada, (3) resultado que dura, (4) ambiente acolhedor. Conteúdo específico para salão de beleza.

- [11] ✅ Variação de CTAs: CTAs ao longo do site com linguagem e intenção distintas:
  - "Agendar pelo WhatsApp →" (hero, CTA final)
  - "Ver serviços" (hero secundário)
  - "Ver mais →" (link em cada card)
  - "Sou noiva — quero agendar 💍" (banner noivas)
  - "Ver nossos trabalhos →" (seção Instagram)
  - "Agendar: (12) 99794-6928" (nav)
  Não há repetição monótona do mesmo texto em todos os pontos.

---

### Estrutura

- [12] ✅ Stats no hero: 3 stats no bloco `.hero-stats-box` (canto inferior direito): **665** (Fãs Facebook), **103** (Check-ins no local), **👰** (Especialista noivas). Dois stats com números reais verificáveis do briefing.

- [13] ✅ Animações: 
  - `slowZoom`: presente — `animation: slowZoom 22s ease-in-out infinite alternate` no `.hero-bg` ✅
  - `fadeUp` com delays escalonados: presente — hero-tag (0.2s), h1 (0.4s), hero-sub (0.6s), hero-ctas (0.8s), hero-stats-box (1s) ✅
  - Hover com `translateY`/`transform`: presente — `.btn-primary:hover { transform: translateY(-2px) }`, `.servico-card:hover { transform: translateY(-8px) }`, `.comunidade-card:hover { transform: translateY(-8px) }` ✅

- [14] ✅ Paleta de cores: 9 variáveis de cor definidas no `:root`: `--primary`, `--secondary`, `--accent`, `--dark`, `--text`, `--bg`, `--bg-alt`, `--gray`, `--border`. Muito acima do mínimo de 5.

- [15] ✅ Tipografia: Fonte display é **Cormorant Garamond** — serif elegante, adequada para salão de beleza/noivas (mesma categoria de Playfair Display). Não é Poppins. Carregada via Google Fonts com pesos 400, 600, 700 e itálico.

---

## Revisão do Email

Seção: "Email 3 — Salão de Beleza Adriana" em `emails.md`

- Nome correto: ✅ — "Salão de Beleza Adriana" (idêntico ao briefing)
- Dado real citado: ❌ — O email menciona "vi seus trabalhos no Instagram" de forma genérica, mas não cita nenhum dado numérico verificável (ex: "665 curtidas no Facebook", "103 check-ins", nota Google). A frase "os penteados de noiva são lindos" é subjetiva, não é dado real.
- Palavras: ~85 palavras — ✅ (dentro do intervalo 60–150)
- CTA é pergunta: ✅ — "Posso te mostrar como ficaria sem compromisso?"
- Assunto OK: ❌ — "Noivas que buscam cabeleireira em SJC não estão encontrando o Salão Adriana" tem **13 palavras** (máximo: 7)
- Sem preço: ✅ — Nenhuma menção a valor ou proposta comercial

---

Ponto positivo: A solução de prova social alternativa para o Salão Adriana é elegante e honesta — a seção "Nossa Comunidade" deixa explícito que não há depoimentos fabricados e apresenta os 3 dados reais (665 curtidas, 103 check-ins, @sdbelezaadriana) com SVG e visual coerente com o restante do site. A tipografia Cormorant Garamond e a paleta rosé/dourado criam identidade visual sofisticada, adequada para noivas.

---

## CORREÇÕES OBRIGATÓRIAS

1. **[Item 2]** — Ausência dos 4 elementos obrigatórios nos cards de prova social — Os 3 cards da seção "Nossa Comunidade" exibem apenas número + título + texto descritivo, sem: (a) estrelas de avaliação, (b) texto entre aspas de depoimento, (c) avatar circular com inicial do cliente, (d) nome do cliente/fonte. Mesmo com a exceção do Item 1, o formato dos cards deve incluir os elementos de estrutura quando cards são usados como prova social. Alternativa aceitável: transformar os cards em painéis puramente estatísticos (sem a estrutura de depoimento) ou adicionar uma nota de rodapé identificando a fonte ("Fonte: Facebook · facebook.com/sdbelezaadriana"). — **Agente: Diego Digital**

2. **[Item 7]** — Apenas 2 URLs de imagem Unsplash distintas (mínimo: 5) — `photo-1560066984-138dadb4c035` e `photo-1522337360788-8b13dee7a37e` são repetidas em 10 ocorrências no total. O site parece visualmente monótono com as mesmas duas fotos. Adicionar pelo menos 3 URLs Unsplash adicionais e distintas, preferencialmente relacionadas ao nicho de salão de beleza (ex: photo de tratamento capilar, manicure, ambiente de salão, coloração diferente). — **Agente: Diego Digital**

3. **[Email — Dado real]** — O email não cita nenhum dado numérico verificável do Salão Adriana — Substituir a frase genérica "Vi seus trabalhos no Instagram" por dado concreto: ex. "Vi que você tem 665 fãs no Facebook e 103 check-ins — uma comunidade local que claramente gosta do seu trabalho." — **Agente: Carlos Carta**

4. **[Email — Assunto]** — Assunto com 13 palavras (máximo: 7) — "Noivas que buscam cabeleireira em SJC não estão encontrando o Salão Adriana" excede o limite. Sugestão de assunto dentro do limite: "Noivas em SJC não estão achando o Adriana" (8 palavras — ainda levemente acima) ou "Penteado de noiva: o Google não te mostra" (7 palavras). — **Agente: Carlos Carta**

---

## VEREDICTO: REJEITADO

4 falhas: Item 2 (estrutura de cards ausente), Item 7 (apenas 2 imagens Unsplash distintas, mínimo 5), Email sem dado real verificável, Assunto do email com 13 palavras (máximo 7).
