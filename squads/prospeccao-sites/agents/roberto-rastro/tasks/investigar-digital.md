---
task: "Investigação Digital Completa — Foco em Avaliações Reais"
order: 1
input:
  - lista_aprovada: Lista de negócios aprovada pelo usuário no checkpoint 3
output:
  - investigacao_completa: Dados completos com mínimo 3 avaliações textuais reais por negócio
---

# Investigação Digital Completa

Para cada negócio da lista, busca sistematicamente avaliações textuais reais, dados de contato verificados e presença digital. Texto de avaliação é **bônus**: Roberto tenta reunir 3+ avaliações textuais, mas se não houver, registra a **prova social agregada** (nota + volume) e o negócio segue. O único bloqueio é falta de WhatsApp/email.

Roberto também **detecta e classifica site existente** (Fase 0). O negócio é "comércio SEM site", então cavar por site já existente antes de qualificar é obrigatório — não achar de primeira não prova ausência.

## Pré-requisito por Negócio

Antes de marcar um negócio como investigado, verificar:
- [ ] Busca ativa por site existente feita e classificação em 3 categorias registrada (Fase 0)
- [ ] Tentativa de 3+ avaliações textuais (bônus); se não houver, flag ℹ️ SEM TEXTO — PROVA SOCIAL AGREGADA (nota + volume) registrado
- [ ] Telefone com DDD verificado (ou "não encontrado")
- [ ] Email verificado (ou "não encontrado")
- [ ] Horário de funcionamento (ou "não confirmado")
- [ ] Endereço completo com CEP

## Process

### Fase 0 — Detecção e Classificação de Site Existente (obrigatória, ANTES de qualificar)

O negócio só qualifica como "sem site" depois de Roberto CAVAR. Não achar de primeira não prova ausência. Para cada negócio, buscar em todas as frentes abaixo e registrar o resultado:

1. **Domínio próprio no Google**
   - `web_search: "[nome do negócio] [cidade]"` — o primeiro resultado pode ser um site próprio
   - `web_search: "[nome do negócio] site oficial"` e `web_search: "[nome do negócio] .com.br"`
   - Procurar domínio do tipo `nomedonegocio.com.br` / `.com` (ex.: `equilibresectp.com.br`)
2. **Link na bio do Instagram** e link-aggregators — abrir o link da bio; pode apontar para site próprio OU para página de plataforma. Checar Linktree, Beacons, Bio.link, Orbit Pages.
3. **Link no perfil do Google Maps** — campo "site" da listagem — e no Facebook (seção Sobre).
4. **Plataformas comuns de presença web**:
   - Delivery/cardápio/pedido: `web_search: "[nome] delivery"`, iFood, Anota.ai, Goomer, Cardápio Web, sistemas tipo `delivery.sistemapallas.com.br`
   - Criadores de site/página: Wix, Google Sites, Orbit Pages, Linktree, Bio.link

Para cada link encontrado, `web_fetch` para inspecionar: é domínio próprio ou subdomínio de plataforma? Tem páginas institucionais (sobre / serviços / contato)? É só uma página de pedido/cardápio?

**Classificar em UMA das 3 categorias:**

```
🚫 SITE INSTITUCIONAL PRÓPRIO — [URL]
   → domínio próprio + páginas institucionais (sobre/serviços/contato). Ex.: equilibresectp.com.br, Dulce.
   → SINALIZAR: André deve DESQUALIFICAR — o negócio já tem o que venderíamos.

🟡 PÁGINA DE PLATAFORMA — [URL]
   → página de delivery/cardápio/pedido ou link em criador de página, SEM site institucional próprio.
     Ex.: A Família (delivery.sistemapallas.com.br/afamiliarestaurante).
   → NÃO desqualifica. Ângulo de venda: "tem ferramenta de pedido, mas falta site institucional
     que apresente o negócio e apareça no Google".

✅ SEM PRESENÇA WEB PRÓPRIA
   → só redes sociais / Google Maps, nenhum site nem página de plataforma. Qualifica normalmente.
```

Critério de desempate próprio × plataforma: **domínio próprio + páginas institucionais = próprio**; subdomínio de plataforma ou página só de pedido/cardápio = plataforma.

### Fase 1 — Identificação do Perfil

Para cada negócio:

1. `web_search: "[nome do negócio] [cidade]"` — identificar perfis online
2. Confirmar identidade: nome + cidade + categoria devem bater antes de usar qualquer dado
3. Coletar URL de cada plataforma identificada

### Fase 2 — Coleta de Avaliações (BÔNUS — tentar, não obrigatório)

Seguir esta sequência tentando completar 3 avaliações textuais. Parar quando tiver 3. Se esgotar as fontes com menos de 3, seguir mesmo assim com prova social agregada — nunca inventar texto.

**1. Google Maps** (sempre tentar primeiro)
- `web_search: "[nome do negócio] [cidade] avaliações"` — snippets de reviews aparecem nos resultados
- `web_search: "[nome do negócio] [cidade] google maps"` — coletar nota e snippets de avaliações
- `web_fetch: [URL do Google Maps do negócio]` — tentar extrair avaliações da página
- Registrar: nota, quantidade total, textos disponíveis nos snippets de busca

**2. TripAdvisor** (restaurantes, padarias, lanchonetes, barbearias, salões)
- `web_search: "[nome] [cidade] site:tripadvisor.com.br"`
- `web_fetch: [URL TripAdvisor]` — coletar nota, ranking, até 5 avaliações textuais

**3. Facebook Reviews**
- `web_search: "[nome] site:facebook.com reviews"`
- `web_fetch: [URL Facebook do negócio]` — coletar nota e avaliações visíveis
- Nota: Facebook muitas vezes requer login — registrar "acesso limitado" se for o caso

**4. iFood / Anota.ai / Rappi** (restaurantes, padarias, pizzarias, lanchonetes)
- `web_search: "[nome] site:ifood.com.br"` ou `web_search: "[nome] ifood avaliações"`
- `web_fetch: [URL iFood]` — avaliações de pedidos são frequentemente públicas e detalhadas
- iFood geralmente tem os textos mais úteis para esse nicho

**5. Reclame Aqui** (todos os nichos — negativo também é útil para contexto)
- `web_search: "[nome] site:reclameaqui.com.br"`
- Se encontrado: anotar reclamações e como foram resolvidas

**6. Foursquare / Yelp**
- `web_search: "[nome] [cidade] site:foursquare.com"`
- `web_fetch: [URL]` se encontrado

**7. Blogs e mídias locais**
- `web_search: "[nome do negócio] São José dos Campos"` — buscar menções em blogs, guias locais, matérias de jornal

### Fase 3 — Busca Exaustiva de Contato Direto (14 fontes obrigatórias)

**Contato qualificado** = WhatsApp público OU email público.
**NÃO qualificam**: telefone fixo sozinho, Instagram DM, Facebook DM, formulários web, "fale conosco".

Consultar TODAS as 14 fontes abaixo, nesta ordem. Registrar resultado de cada uma (encontrou / não encontrou):

1. **Google Maps** — perfil completo: telefone, site, email na listagem
2. **Site próprio** do negócio (Wix, Squarespace, Linktree, etc.) — se existir, raspar contato
3. **Linktree / Beacons** — link-aggregator na bio do Instagram
4. **Bio do Instagram** — texto completo, incluindo números e emails escritos por extenso
5. **Posts fixados do Instagram** — donos costumam fixar post de contato
6. **Stories destacados do Instagram** — buscar destaques com nome "Contato", "Pedidos", "Reservas"
7. **Facebook — seção Sobre / Informações** — telefone e email muitas vezes só aparecem aqui
8. **CNPJ.biz ou ReceitaWS** — `web_fetch: https://www.cnpj.biz/pesquisa/[nome+cidade]` — telefone cadastrado na Receita Federal frequentemente é o número real do dono
9. **Diretórios públicos**: Solutudo, Apontador, Bendito Guia, Polomap, Akademias, Rank Level — `web_search: "[nome negócio] [cidade] solutudo"` etc.
10. **Plataformas do nicho**: Wellhub/Gympass (academias), iFood/Anota.ai (restaurantes), Booksy/Belezamente (salões), Telelistas (qualquer comércio)
11. **Cadastros municipais / Câmara de Comércio** — `web_search: "[nome negócio] [cidade] câmara comércio"` ou prefeitura local
12. **Anúncios pagos**: Google Ads (`web_search: "[nome] anúncio"`) e Meta Ads Library (`web_fetch: https://www.facebook.com/ads/library/?q=[nome]`)
13. **Respostas de donos no Google Maps / TripAdvisor** — `web_search: "[nome negócio] respondeu avaliação google"` — donos frequentemente deixam telefone direto ao responder
14. **OLX / Mercado Livre** — `web_search: "[nome negócio] site:olx.com.br"` (para negócios que vendem produto)

Após consultar as 14 fontes:
- Se encontrou contato direto: registrar e continuar
- Se não encontrou: marcar `⛔ REPROVADO — sem contato direto após busca exaustiva (14 fontes)` com a lista completa de fontes e resultados. André Análise não avança este negócio.

Dados de contato a coletar quando encontrado:
- **Telefone**: formato `(DDD) NNNNN-NNNN` → wa.me: `55DDDDNNNNNNNNN`
- **Email**: verificar validade do endereço
- **Horário**: dias e horas reais (nunca inventar)
- **Endereço + CEP**: verificar consistência entre plataformas

### Fase 4 — Presença Digital e Identidade Visual

- **Instagram**: anotar handle, seguidores, frequência de posts, bio, estilo visual
- **Facebook**: anotar URL, curtidas, check-ins, último post
- **Identidade visual**: cores predominantes, logo, tom de comunicação

- **Instagram como fonte de fotos do site** (alimenta o checkpoint de fotos): avaliar se o Instagram serve para o Diego usar fotos reais no site e classificar explicitamente:
  - `📸 INSTAGRAM BOM — @[handle]` → perfil público com fotos boas do próprio trabalho/produto (pratos reais, tatuagens feitas, bolos entregues, antes/depois), bem iluminadas, não só prints de promoção/texto/repost.
  - `📷 INSTAGRAM FRACO/SEM` → sem perfil público, perfil inativo, ou fotos fracas/genéricas/só texto. Diego usará Unsplash.
  - Critério é a QUALIDADE para vender o negócio, não o número de seguidores. Registrar o @ sempre que existir, mesmo quando classificado como fraco.

### Fase 5 — Conclusão por Negócio

Ao finalizar cada negócio, registrar explicitamente:

Se 3+ avaliações coletadas:
```
✅ TEXTO DISPONÍVEL — [N] avaliações textuais coletadas (bônus para depoimentos)
```

Se menos de 3 após todas as fontes (negócio SEGUE normalmente):
```
ℹ️ SEM TEXTO — USAR PROVA SOCIAL AGREGADA — [N] texto(s) encontrado(s)
Prova social disponível: nota [X.X] ⭐ em [N] avaliações.
Fontes tentadas: [lista]. Diego usará a prova agregada (sem inventar texto).
```

## Output Format

```markdown
# Investigação Digital — Run [run_id]

---

## [Nome do Negócio 1]

### Classificação de Presença Web (Fase 0)
- **Categoria:** 🚫 SITE INSTITUCIONAL PRÓPRIO / 🟡 PÁGINA DE PLATAFORMA / ✅ SEM PRESENÇA WEB PRÓPRIA
- **URL encontrada:** [url] / Nenhuma
- **Frentes buscadas:** domínio no Google [resultado] · bio Instagram [resultado] · site no Google Maps [resultado] · plataformas de delivery/página [resultado]
- **Se 🚫:** sinalizar André → DESQUALIFICAR (já tem site institucional próprio)
- **Se 🟡:** ângulo de venda → "tem ferramenta de pedido, mas falta site institucional que apresente o negócio e apareça no Google"

### Status por Plataforma
| Plataforma | Status | URL / Handle |
|---|---|---|
| Google Maps | Ativo / Não encontrado | [url] |
| TripAdvisor | Ativo / Não encontrado | [url] |
| Facebook | Ativo / Não encontrado | [url] |
| iFood | Ativo / N/A / Não encontrado | [url] |
| Reclame Aqui | Ativo / Não encontrado | [url] |
| Instagram | Ativo / Não encontrado | @handle |
| Solutudo | Ativo / Não encontrado | [url] |

### Dados de Contato Verificados
- Telefone: (12) XXXXX-XXXX → wa.me/5512XXXXXXXXX
- Email: [email@dominio.com] / Não encontrado
- Horário: Seg-Sex XX:00-XX:00 | Sáb XX:00-XX:00 / Não confirmado
- Endereço: [rua, número — bairro — cidade/UF — CEP XXXXX-XXX]
- Dono/contato: [nome se encontrado] / Não identificado

### Avaliações Reais Coletadas
"[texto exato da avaliação]" — [Nome do avaliador], [data] — Fonte: [plataforma] ⭐⭐⭐⭐⭐

"[texto exato]" — [Nome], [data] — Fonte: [plataforma] ⭐⭐⭐⭐⭐

"[texto exato]" — [Nome], [data] — Fonte: [plataforma] ⭐⭐⭐⭐⭐

✅ REQUISITO ATENDIDO — 3 avaliações textuais coletadas

### Dados de Prova Social
- Google Maps: [nota] ⭐ ([N] avaliações)
- [Plataforma]: [nota] ⭐ ([N] avaliações)

### Identidade Visual
- Cores predominantes: [cores observadas]
- Estilo: [moderno/clássico/rústico/etc]
- Logo: [presente/não identificado]
- Tom de comunicação: [formal/descontraído/etc]
- **Fotos do site (Instagram):** 📸 INSTAGRAM BOM — @[handle] / 📷 INSTAGRAM FRACO/SEM [+ @handle se houver]

---

## [Nome do Negócio 2]
[mesmo formato]
```

## Veto Conditions

Reject and redo if ANY are true:
1. Avaliações parafraseadas ou sem aspas (devem ser texto literal da plataforma)
2. Plataforma da sequência pulada sem registro de status
3. Negócio sem 3 avaliações textuais e sem o flag ℹ️ SEM TEXTO — PROVA SOCIAL AGREGADA (com nota + volume) registrado
4. Telefone sem DDD ou em formato incorreto
5. Dados de contato sem verificação de fonte
6. Negócio marcado REPROVADO por falta de contato sem listar as 14 fontes consultadas
7. Menos de 14 fontes consultadas antes de marcar REPROVADO — André devolverá o briefing
8. Negócio sem a classificação de presença web (Fase 0) em 1 das 3 categorias
9. Negócio marcado ✅ SEM PRESENÇA WEB PRÓPRIA sem registrar as frentes buscadas (domínio no Google, bio do Instagram, site no Google Maps, plataformas comuns)
10. Página de plataforma (delivery/cardápio) classificada como 🚫 SITE INSTITUCIONAL PRÓPRIO, ou site institucional próprio classificado como 🟡 PÁGINA DE PLATAFORMA
