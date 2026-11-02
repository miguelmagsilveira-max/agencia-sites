# Revisão — Lanchonete e Pizzaria dos Amigos
Data: 2026-05-18
Revisora: Vera Veredito
Run: 2026-05-17-114447

---

## Checklist de 15 Itens

### Autenticidade

- [1] ✅ Cards de avaliação real: Roberto Rastro marcou ⚠️ AVALIAÇÕES INSUFICIENTES (0 avaliações textuais públicas encontradas). O site implementou corretamente a "Prova Social Alternativa" com dados reais verificáveis: 10 anos de operação (desde maio de 2015 — confirmado no briefing), 0% taxa delivery (confirmado via Anota.ai), Instagram ativo (@pizzariaelanchonetedosamigos — confirmado no briefing). Seção "Por que pedir dos Amigos?" usa dados numéricos reais (10 anos, 0%, cardápio completo). Exceção documentada aplicada corretamente.

- [2] ✅ Estrutura dos cards de avaliação: N/A — Item 1 aprovado por exceção documentada (prova social alternativa). Os 3 cards da seção "Por que pedir dos Amigos?" contêm número destacado, título, descrição e link CTA. A estrutura é consistente e adequada para o modelo alternativo.

- [3] ❌ WhatsApp real: Link no botão flutuante é `https://wa.me/55?text=...` — número incompleto, sem DDD e sem número de celular. O briefing confirma que o telefone NÃO foi encontrado na investigação. O site deveria ter pausado e solicitado o número ao usuário antes de publicar. Placeholder funcional (`wa.me/55`) que leva a destino inválido.

- [4] ❌ Todos os links completos: Único link `wa.me` encontrado no site (`wa.me/55`) está incompleto. Não há outro link WhatsApp além do botão flutuante. Falha idêntica ao Item 3.

- [5] ❌ Horário específico: Linha 1539 do HTML exibe `"Horário: consulte pelo Instagram"` — texto explicitamente proibido pelo checklist ("Nunca aceitar 'consulte por telefone' ou 'horário a confirmar'"). O horário não foi confirmado na investigação, mas o site deveria ter omitido o campo conscientemente em vez de usar texto de consulta.

- [6] ✅ Email: Email real `viniciuscarvalhosjc1515@gmail.com` aparece visivelmente no site em dois locais: seção de localização (linha 1511) e rodapé (linha 1586), além do schema JSON-LD. Bate exatamente com o email confirmado no briefing (Solutudo). Sem placeholder.

### Qualidade Visual

- [7] ✅ Imagens Unsplash: 4 IDs únicos encontrados (`photo-1513104890138`, `photo-1504674900247`, `photo-1568901346375`, `photo-1546069901`) mais 2 background-images CSS (`photo-1513104890138` no hero, `photo-1504674900247` no banner), totalizando 8 ocorrências com 4 fotos distintas. Verificação mais rigorosa: 4 fotos únicas distintas do Unsplash — abaixo do mínimo de 5 URLs distintas. PORÉM, na contagem de `<img>` + `background-image` são 8 instâncias. Reavaliando pela letra do checklist ("5 ou mais URLs Unsplash distintas"): apenas 4 IDs únicos. ❌ se contagem for por URLs distintas (4 < 5). ✅ se contagem for por ocorrências (8 ≥ 5). Decisão: o checklist diz "5 ou mais URLs Unsplash distintas" — com 4 IDs únicos, a condição não é atendida.

  **Reavaliação:** 4 URLs distintas < 5 mínimo exigido.

- [7] ❌ Imagens Unsplash: 4 URLs distintas encontradas (photo-1513104890138, photo-1504674900247, photo-1568901346375, photo-1546069901). Mínimo exigido: 5 URLs distintas. Deficit de 1 imagem.

- [8] ✅ SVG em feature-icons: Seção "Como trabalhamos" (Experiência) usa `.feature-icon-box` com `<svg>` + `<path>`/`<line>`/`<rect>` inline para todos os 3 ícones (calendário/tradição, seta/delivery, grid/cardápio). Seção "Nosso Compromisso" usa `.compromisso-icon` com `<svg>` + `<polygon>`/`<path>`/`<rect>`/`<circle>` para todos os 4 itens. Nenhum emoji usado como ícone funcional nessas seções.

- [9] ✅ Badge de destaque: Card 1 do cardápio tem badge `⭐ Mais Pedido` (classe `card-badge`, linha 1273). Card 3 tem badge `🚫 Sem taxa extra` (classe `card-badge card-badge-accent`, linha 1306). Dois cards diferenciados com badges distintos.

- [10] ✅ Seção "Nosso Compromisso": Seção presente com ID `compromisso`, título "Nosso compromisso com o bairro", contendo 4 bullets específicos do nicho gastronômico: "Ingredientes selecionados", "Entrega direta", "10 anos de consistência", "Pedido pelo Instagram". Posicionada entre Sobre e Cardápio. Totalmente adequada ao contexto.

- [11] ✅ Variação de CTAs: CTAs encontrados variam em linguagem e intenção: "Pedir agora" (nav), "🛵 Pedir pelo Instagram →" (hero primário), "Ver cardápio" (hero secundário), "Ver sabores →" (card 1), "Montar pedido →" (card 2), "Pedir agora →" (card 3), "Ir para o Instagram →" (banner delivery), "Conhecer mais →" (porque card 1), "Fazer pedido →" (porque card 2), "Ver cardápio →" (porque card 3), "Bora pedir? 🍕" (CTA final). Nenhum CTA repetido identicamente ao longo do site. Excelente variação.

### Estrutura

- [12] ✅ Stats no hero: Hero contém 3 stats reais no canto inferior direito (`.hero-stats-box`): "10 / Anos no bairro", "2015 / Fundação", "0% / Taxa delivery". Todos os números são verificáveis e confirmados no briefing. Stats com glassmorphism e posicionamento correto.

- [13] ✅ Animações: `slowZoom` aplicado no `.hero-bg` (linha 261 — `animation: slowZoom 20s ease-in-out infinite alternate`). `fadeUp` com delays escalonados no hero: hero-badge 0.2s, h1 0.4s, hero-sub 0.6s, hero-ctas 0.8s, hero-stats-box 1s. Hover com `translateY(-8px)` nos cards de cardápio (linha 541) e porque-cards (linha 801). Todos os 3 critérios presentes.

- [14] ✅ Paleta de cores: CSS define 9 variáveis de cor em `:root`: `--primary`, `--secondary`, `--accent`, `--dark`, `--text`, `--bg`, `--bg-alt`, `--gray`, `--border`. Supera amplamente o mínimo de 5 variáveis exigido.

- [15] ✅ Tipografia por nicho: Fonte display `Playfair Display` (serif) usada em títulos, headings, stats e logo. Adequada para nicho gastronômico/alimentação (categoria Playfair/Cormorant para gastronomia). Não é Poppins. Font body: Inter. Combinação correta para o nicho.

---

## Resumo dos Itens ❌

| Item | Status | Problema |
|------|--------|---------|
| 3 | ❌ | `wa.me/55` — número incompleto, sem DDD |
| 4 | ❌ | Único link wa.me no site também incompleto |
| 5 | ❌ | "Horário: consulte pelo Instagram" — texto proibido |
| 7 | ❌ | Apenas 4 URLs Unsplash distintas (mínimo: 5) |

---

## Revisão do Email

Email para: viniciuscarvalhosjc1515@gmail.com
Assunto: "Pizzaria dos Amigos: delivery ativo, Instagram ativo — só falta o site"

- Nome correto: ✅ — "Lanchonete e Pizzaria dos Amigos" mencionado no corpo (linha 1)
- Dado real citado: ✅ — "delivery próprio pelo Anota.ai" e "presença ativa no Instagram" (dados confirmados no briefing)
- Palavras: 77 — ✅ (dentro do range 60–150)
- CTA é pergunta: ✅ — "Posso mostrar um modelo?" (última linha do corpo)
- Assunto OK: ❌ — 12 palavras ("Pizzaria dos Amigos: delivery ativo, Instagram ativo — só falta o site"). Limite: 4–7 palavras. Excede em 5 palavras.
- Sem preço: ✅ — nenhuma menção a valores, pacotes ou proposta comercial

---

Ponto positivo: A seção de Prova Social Alternativa é muito bem executada — transforma a ausência de avaliações textuais em um diferencial positivo com dados concretos e verificáveis (10 anos, 0% taxa, delivery próprio). O uso de números reais em vez de depoimentos inventados demonstra integridade e criatividade do conteúdo.

## CORREÇÕES OBRIGATÓRIAS

1. **[Item 3/4] — WhatsApp incompleto** — O botão flutuante e único link wa.me usa `https://wa.me/55` sem DDD e número. O site deveria ter pausado a execução e solicitado ao usuário o número de WhatsApp/celular antes de publicar. **Correção:** Solicitar ao cliente o número completo (formato: 55 + DDD + número, ex: `5512999999999`) e substituir em `href="https://wa.me/55?text=..."`. — **Agente: Diego Digital**

2. **[Item 5] — Horário proibido** — Linha 1539 exibe "Horário: consulte pelo Instagram" — texto explicitamente proibido pelo checklist. O horário não foi confirmado na investigação, mas a solução correta é omitir o campo completamente (sem placeholder visível) ou usar o Instagram como referência sem a fórmula "consulte". **Correção:** Remover o `<span>` com o texto "Horário: consulte pelo Instagram" ou substituir por "Pedidos via Instagram" sem menção a "consulte". — **Agente: Diego Digital**

3. **[Item 7] — Imagens Unsplash insuficientes** — Apenas 4 URLs distintas do Unsplash (photo-1513104890138, photo-1504674900247, photo-1568901346375, photo-1546069901). Falta 1 imagem adicional com URL única. **Correção:** Adicionar pelo menos 1 imagem Unsplash nova (sugestão: foto de lanche/hambúrguer ou ambiente de lanchonete) em uma nova seção ou substituindo uma imagem repetida. — **Agente: Diego Digital**

4. **[Assunto do Email] — Assunto muito longo** — "Pizzaria dos Amigos: delivery ativo, Instagram ativo — só falta o site" tem 12 palavras (limite: 4–7). **Correção:** Encurtar para algo como "Pizzaria dos Amigos: só falta o site" (7 palavras) ou "Delivery ativo — só falta o site" (6 palavras). — **Agente: Carlos Carta**

---

## VEREDICTO: REJEITADO

4 itens reprovados: WhatsApp incompleto (Items 3 e 4 — falha crítica de dado real), horário com texto proibido "consulte" (Item 5), imagens Unsplash insuficientes (Item 7 — 4 de 5 mínimos), e assunto do email com 12 palavras (acima do limite de 7).
