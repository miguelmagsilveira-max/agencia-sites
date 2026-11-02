# Revisão — Vera Veredito — Rodada 4 (2026-09-14)

Método: checagem automatizada (15 itens obrigatórios) + revisão visual dos full-page screenshots mobile (itens 16-20) + verificação dos emails contra os 9 blocos do gold standard. TRAVA DE FASE 1 aplicada (não cobro depoimento textual real, antes/depois, preço ou feed embutido).

## Veredictos

| Site | Etiqueta | Tratamento | Site | Email | Veredicto |
|------|----------|-----------|------|-------|-----------|
| Blue House Banho e Tosa | COMÉRCIO | RICO | ✅ | ✅ | **APROVADO** |
| Pavoli Sorvetes e Açaí | COMÉRCIO | RICO | ✅ (após fix) | ✅ | **APROVADO** |
| Saint Joe Burgerhouse | COMÉRCIO | RICO | ✅ | ✅ | **APROVADO** |
| André Pintor | PRESTADOR | RICO (fotos reais) | ✅ | ✅ | **APROVADO** |
| Meseque Montador | PRESTADOR | SÓBRIO | ✅ | ✅ | **APROVADO** |
| Araci Personal Organizer | PRESTADOR | SÓBRIO | ✅ | ✅ | **APROVADO** |

## Itens verificados (todos os 6)
- [x] Prova social honesta: Blue House 4,9 / Pavoli 4,6 / Saint Joe 4,3 (sem contagem exata) estampadas; André/Meseque/Araci sem número (ângulo qualitativo) — nada inventado, nada divergente do briefing
- [x] WhatsApp real e funcional em todos (formato wa.me/55 + DDD + número), botão flutuante na cor da marca (verde só no ícone)
- [x] Horário nunca fabricado — substituído por CTA de WhatsApp onde não confirmado (sem placeholder)
- [x] Imagens: RICO ≥5 distintas (`images.unsplash.com`, nunca `source.unsplash.com`); André com 7 FOTOS REAIS locais; SÓBRIO 1-2 fotos de nicho relevantes; toda `<img>` remota com `onerror` Picsum
- [x] Feature-icons SVG inline (nunca emoji) — 8 a 14 SVGs por site
- [x] Card com badge de destaque ("Mais Pedido"/"Especialidade"/"Queridinho")
- [x] Seção diferenciais/processo presente (posição pelo mapa do nicho)
- [x] CTAs variam por intenção (não repetem "Falar no WhatsApp")
- [x] Hero-stats reais no canto (nota, ou especialidade/área nos prestadores)
- [x] Animações: slowZoom/fadeUp/hover presentes
- [x] Paleta 3 cores + 2 neutras por nicho; tipografia por nicho (nunca Poppins)
- [x] Schema.org LocalBusiness, meta viewport, nav blur, footer 3 colunas
- [x] Linha "Prévia / demonstração — site amostra, não oficial" no rodapé
- [x] Galeria/portfólio com lightbox inline (RICO)
- [x] Breakpoint 768px
- [x] (16-20) Imagens relevantes ao nicho; hero cheio; prova visual cedo; identidade de nicho; WhatsApp na cor da marca

## Correção aplicada nesta revisão
- **Pavoli:** os blocos com `.rv{opacity:0}` só apareciam via IntersectionObserver no scroll — no carregamento sem rolagem ficavam invisíveis. Adicionada rede de segurança (revela `.rv` após 1,2s + fallback `<noscript>`), preservando a animação. Site re-deployado. Conteúdo (galeria, cardápio, prova 4,6, mapa) confirmado visível.

## Emails (9 blocos do gold standard)
Todos os 6 verificados: [x] Bloco 1 apresentação antes de qualquer dado; [x] Bloco 2 elogio interpretado ("não é à toa", "coisa séria", "fala por si"); [x] Bloco 3 transição "Justamente por isso"; [x] Bloco 4 problema como história reconhecendo o que já funciona; [x] Bloco 5 ponte "Pensei:"; [x] Bloco 6 iniciativa no passado ("fui em frente", "já deixei no ar") com 3-5 elementos reais; [x] Bloco 7 telas 👇 + link ao vivo; [x] Bloco 8 pergunta fechada de permissão ("Quer que eu te mande os detalhes?") + "sem compromisso"; [x] Bloco 9 assinatura "Abraço, / Miguel Magalhães Silveira / 12974062797". Sem frases proibidas (sem "vamos fechar", sem "o que achou", sem tom de vendedor). ~200-230 palavras cada.

## Ponto positivo
Destaque para o André Pintor: galeria montada com fotos REAIS do trabalho dele (marmorato/cimento queimado), triadas para excluir conteúdo de corrida/pessoal — prova visual forte e honesta, sem fabricar nada.

## Observação fora do checklist (não bloqueia a Vera, mas bloqueia o ENVIO)
Os 6 deploys estão com **Vercel Authentication (Deployment Protection)** ligada → os links ao vivo hoje redirecionam para login. Precisa ser desativada por projeto antes de enviar (ver kit e relatório). Os screenshots foram capturados de servidor local e NÃO dependem disso.
