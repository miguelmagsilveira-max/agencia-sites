---
task: "Criar Site HTML Completo — Padrão Premium"
order: 1
input:
  - briefing: Briefing completo do negócio (8 pontos + avaliações reais)
  - negocio_selecionado: Nome e dados do negócio aprovado pelo usuário no checkpoint 7
output:
  - site_html: Arquivo site.html autocontido, visualmente premium, pronto para prospecção
  - link_ao_vivo: Arquivo link-ao-vivo.txt com a URL pública do deploy no Vercel
---

# Criar Site HTML Completo — Padrão Premium

Cria um site HTML único, autocontido, de alta qualidade visual, com imagens reais buscadas na API oficial da Unsplash (nunca source.unsplash.com), animações CSS, tipografia por nicho e copy de conversão. O arquivo deve parecer um site profissional de R$3.000+ ao ser aberto no navegador.

## Pré-requisito: Material de Prova Social (texto é bônus)

**ANTES de criar o site, verificar o que existe — sem travar por falta de texto:**
- O briefing contém 3+ avaliações textuais reais?
  - Se SIM: montar a seção de prova social com cards de depoimento (Seção 7 — modo texto).
  - Se NÃO: NÃO rejeitar nem pausar. Montar a seção com prova social agregada escolhida pela força (Seção 7 — modo agregado, regra de força abaixo). Texto de avaliação é bônus, não requisito.
- Único motivo de pausa antes de criar o site: dado de contato crítico ausente (telefone/WhatsApp inutilizável) — ver Step 1. Falta de texto de avaliação NUNCA pausa.

**Regra de força da prova social (vale para o modo agregado):**
- **Volume ALTO (centenas)** → destacar o número grande ("807 avaliações", "+2.000 atendimentos").
- **Volume BAIXO (poucas dezenas)** → NÃO mostrar o número cru. Usar ângulo verdadeiro melhor: "96% recomendam", a nota em estrelas sem volume ("5,0 ⭐"), tempo de mercado ("desde 2015"), ou diferencial de serviço.
- **Nota ALTA (4.5+/5.0)** → pode sempre aparecer, com ou sem volume.
- **SEM prova verificável e boa** → NÃO inventar e NÃO estampar número fraco/duvidoso. A seção de prova social **pode não existir**; substituir por um **ângulo qualitativo honesto** ("orçamento sem compromisso", "atendimento rápido", "resposta no mesmo dia", "atende toda a cidade"). Comum em nichos de serviço — estatística fraca é pior que ausência.
- **Regra de ouro**: omitir o que é fraco é permitido; inventar número, selo ou depoimento é proibido. Dar confiança ao cliente final E deixar o dono orgulhoso — nunca diminuído por um número baixo.

## Trava de Fase 1 vs Fase 2 (o que NÃO entra no site de prospecção)

Este site é de **fase 1 (prospecção)**: montado só com o que existe ANTES da venda. Há conteúdo que só existe pós-venda (fase 2) — quando o dono fornece acesso e material. **PROIBIDO incluir, inventar ou encenar na fase 1:**
- Foto do dono/profissional trabalhando (não temos essa foto antes de fechar).
- Seção "Conheça a [pessoa]" com foto real da pessoa.
- Depoimento de cliente encenado/fabricado.
- Print/screenshot de avaliação.

Na fase 1: **nem inventar, nem deixar buraco/placeholder** no lugar. Montar a seção com o que é honesto e disponível — prova social agregada (Pré-requisito acima), portfólio real do Instagram (`imagens-insta/`), ângulo verdadeiro do diferencial.

> Ressalva: texto de avaliação **real e público** já coletado pelo Roberto continua valendo como bônus (modo texto da Seção 7). A trava barra **fabricar/encenar** depoimento e barra qualquer elemento que exija ativo que só o dono entrega depois de fechar.

## Process

### Step 0 — Escolher o tratamento visual (RICO × SÓBRIO/FUNCIONAL)

Antes de tudo, decidir o tratamento pelo material real do negócio:

- **RICO (padrão)** — nicho visual e/ou com bom material (Instagram bom OU imagem de nicho forte: restaurante, doceria, tatuagem, salão, estética com portfólio). Seguir todos os Steps abaixo à risca (hero com foto, mínimo 5 imagens, cards com foto, prova visual cedo).
- **SÓBRIO/FUNCIONAL** — nicho de **prestação de serviço com material visual escasso** (eletricista, encanador, chaveiro, personal, esteticista sem portfólio, contador, diarista, montador, técnico), **sem Instagram bom nem imagem de nicho forte**. Priorizar **clareza e confiança**:
  - Hero **tipográfico** (headline forte + proposta clara), **não** dependente de foto de banco genérica.
  - Em destaque e repetido no site: **telefone/WhatsApp**, **o que faz** (serviços em lista limpa), **área de atendimento** (bairros/cidade), **"orçamento rápido no WhatsApp"**, **horários**.
  - Layout limpo, muito respiro, com **1-2 imagens de nicho bem escolhidas e relevantes** para dar respiro visual (ex.: costura/tecido/máquina para ateliê; cachorro/adestramento para adestrador) — SVG/ícones e tipografia continuam carregando o visual. Origem da imagem pelo gate do Princípio 31 / Step 4.0: no SÓBRIO (prestador de serviço) o gate normalmente fecha → as 1-2 fotos vêm da API oficial da Unsplash com **keyword ESPECÍFICA do nicho** (Step 4); foto do Instagram do alvo só se ele for visual-autoral e tiver trabalho próprio usável. **Nunca** encher de foto de banco (mosaico/galeria) nem usar imagem sem relação — e **nunca** deixar o site totalmente sem imagem, árido: 1-2 imagens propositais são o padrão.
  - **Relaxado no SÓBRIO:** exigência de hero com background-image full-bleed, mínimo de 5 imagens e cards-com-foto (Steps 4, 6 e vetos correspondentes) NÃO se aplicam — mas **1-2 imagens de nicho relevantes são esperadas** (ex.: hero split com foto na coluna lateral e/ou 1 foto acompanhando uma seção). Continuam valendo: tipografia por nicho, paleta, CTAs por intenção, WhatsApp flutuante, prova social honesta, dados reais, Schema.org, deploy.

Regra: material bom → RICO; serviço + material escasso → SÓBRIO. Na dúvida, honestidade visual — nunca encher de foto de banco que não é do negócio.

### Step 1 — Ler o briefing e extrair dados essenciais

- Nicho → define tipografia, paleta e estrutura de seções
- Endereço, telefone, WhatsApp → para CTA e Maps
- Avaliações reais → incluídas nos cards (parafraseadas, máx 15 palavras verbatim)
- Redes sociais → mencionar na seção Sobre e Footer
- Horários → seção Horários
- Dados de prova social → stats do hero (nota Google, número de avaliações, anos de fundação, etc.)
- **Especialidade/diferencial** → o gancho que o cliente lembra (ver Step 1.5)

### Step 1.5 — Definir o gancho de especialidade (com TRAVA anti-invenção)

Antes de escrever a copy, escolher **um** diferencial concreto e memorável que posiciona o negócio — o que faz alguém lembrar dele. Exemplos: tatuagem → "fine line autoral"; doceria → "bolos de casamento"; restaurante → "comida caseira da região"; salão → "especialista em loiros"; pilates → "studio com aulas individuais".

Esse gancho entra no `hero-tag`, reforça a `<h1>`/subheadline e dá nome à seção de diferenciais. É a "memória" do site.

**Headline e copy CONCRETAS e HUMANAS — não institucionais (regra de especificidade):**
A `<h1>` do hero e os textos de processo/seções devem comunicar algo concreto do nicho/diferencial real — nunca uma frase que serviria para qualquer negócio do mesmo tipo.
- ✅ Concreto/humano (tatuagem autoral): "Sua tattoo nasce da *sua ideia*, não de um catálogo."
- ❌ Institucional/vazio: "Qualidade e profissionalismo em tatuagem." / "O melhor atendimento da cidade."
- Teste rápido: se a headline cabe igualzinha no site de um concorrente do mesmo nicho, ela é genérica demais — reescrever até dizer algo que só este negócio diria.
- Textos de "processo / como funciona" e seções de apoio soam como uma pessoa explicando ao cliente, não como folheto corporativo.

🔒 **A especificidade não afrouxa a trava anti-invenção.** Concreto ≠ inventado: a frase só pode afirmar o que está comprovado no briefing/investigação (Step 1.5, trava abaixo). Ser específico é escolher um ângulo verdadeiro e dizê-lo com voz humana — nunca criar um diferencial que o dono não pode sustentar.

> 🔒 **TRAVA — só destacar o que está COMPROVADO.** O diferencial só pode ser afirmado se aparece de forma verificável no briefing OU na investigação do Roberto. Fontes válidas de comprovação:
> - O próprio briefing/serviços descritos pelo negócio
> - Bio, posts ou destaques do Instagram (registrados pelo Roberto)
> - Avaliações reais que mencionam o diferencial ("o melhor bolo de casamento que já comi")
> - Lista de serviços/cardápio do negócio
>
> **PROIBIDO inventar.** Nunca escrever "especialista em X", "referência em Y", "premiado", "o melhor da cidade" se a fonte não confirma. Frase específica não comprovada = invenção = veto.
>
> **Se não houver diferencial comprovável:** NÃO inventar um. Usar um ângulo verdadeiro mais genérico porém honesto (qualidade, atendimento, tempo de mercado real, nota alta) e seguir. Melhor um gancho honesto e simples do que uma especialidade falsa que o dono não pode sustentar.

### Step 2 — Escolher tipografia por nicho

| Nicho | Display / Títulos | Body / UI |
|-------|-------------------|-----------|
| Restaurante / Bar / Pizzaria | Playfair Display | Inter |
| Padaria / Café / Confeitaria | Playfair Display | Inter |
| Salão / Estética / Spa | Cormorant Garamond | Jost |
| Academia / CrossFit / Artes Marciais | Oswald | Inter |
| Oficina / Borracharia / Auto | Oswald | Inter |
| Clínica / Consultório | Manrope | Lora |
| Barbearia Premium | Playfair Display | Inter |
| Pet Shop / Veterinário | Nunito | Inter |
| Serviço técnico (eletricista/encanador/chaveiro/montador/TI) | Manrope ou Archivo | Inter |
| Serviço pessoal (personal/esteticista sem portfólio/diarista) | Sora ou Manrope | Inter |
| Contador / Serviço administrativo | Manrope | Inter |

**Nunca usar Poppins como fonte principal.** No tratamento SÓBRIO (Step 0), a força vem da tipografia — usar pares limpos e legíveis (grotescas/humanistas), com boa hierarquia de tamanho e peso.

### Step 3 — Definir paleta de cores por nicho

| Nicho | Primary | Secondary | Accent | Neutrals |
|-------|---------|-----------|--------|----------|
| Restaurante clássico | #1a3a2a (verde escuro) | #c9a96e (dourado) | #f8f3ea (creme) | #0d1f16, #2a4a38 |
| Padaria / Café | #3d5a3e (verde-musgo) | #c8942a (caramelo) | #f5ede0 (bege) | #1a1208, #f9f4ec |
| Salão feminino | #8b5e52 (rosa-terroso/mauve) | #c9a96e (dourado fosco) | #f0e6de (off-white) | #2d1a14, #faf6f3 |
| Academia / Luta | #0f0f0f (preto) | #f5d800 (amarelo neon) | #1a1a1a (grafite) | #2a2a2a, #f0f0f0 |
| Borracharia / Auto | #0f1f3d (azul-noite) | #e85c0a (laranja) | #2d3748 (grafite) | #080f1e, #f4f6f9 |
| Clínica | #1e3a5f (azul-marinho) | #4a9e8a (verde-agua) | #f0f7f4 (mint claro) | #0d2035, #f8faf9 |

Sempre definir como variáveis CSS: `--primary`, `--secondary`, `--accent`, `--dark`, `--text`, `--bg`, `--bg-alt`, `--gray`.

### Step 4 — Imagens reais: fotos do Instagram primeiro, Unsplash como fallback

Mínimo 5 imagens DISTINTAS (proibido reusar a mesma imagem em seções diferentes).

**Ordem de prioridade das imagens:**
1. **Fotos reais do Instagram do negócio** (quando o Miguel baixou no checkpoint 8) — sempre preferir estas. São o produto/serviço de verdade e vendem muito mais que banco de imagem.
2. **API oficial da Unsplash** (quando não há fotos do Instagram) — fotos relevantes ao nicho.

#### 4.0 — Gate da foto do Instagram do alvo (decidir ANTES de olhar a pasta)

🔒 **Gate de 2 condições (Princípio 31) — só usar foto do Instagram do alvo se as DUAS valerem:**
- **(a) Nicho visual-autoral** — o trabalho das mãos É o produto: confeitaria/bolos, tatuagem, pintura/marmorato, cestas, convites/papelaria, unhas/nail art **e similares** (restaurante/doceria/salão contam quando a foto própria mostra o prato/bolo/resultado real).
- **(b) O alvo publicou trabalho próprio usável** — fotos próprias, nítidas, do trabalho (não repost, não meme, não flyer, não banco, não borrada).

**Se o gate FECHA** (nicho de prestação de serviço — personal, montador, organizer, eletricista, chaveiro, TI, contador, etc. — OU sem trabalho próprio usável): **NÃO usar a pasta `imagens-insta/`**. Ir direto para 4a e buscar tudo na **API oficial da Unsplash** (keyword específica do nicho) + Picsum fallback. Isso vale para o tratamento SÓBRIO (Step 0), que é o caso típico desses nichos: as 1-2 imagens de respiro vêm da Unsplash.

**Se o gate ABRE** (nicho visual-autoral COM trabalho próprio usável): seguir abaixo e preferir as fotos reais do Instagram.

#### 4.0.1 — Verificar a pasta `imagens-insta/` (quando o gate abre)

Olhar a pasta `squads/prospeccao-sites/output/{run_id}/{slug-negocio}/imagens-insta/`:
```bash
ls -la squads/prospeccao-sites/output/{run_id}/{slug-negocio}/imagens-insta/ 2>/dev/null
```
- **Se tem fotos** (1 ou mais arquivos de imagem): USAR essas fotos no site. Diego decide a melhor distribuição olhando cada foto — a mais forte vai no hero/banner, as demais em galeria, cards e mosaico. Referenciar por caminho relativo a partir da pasta do negócio (o `site.html` fica na mesma pasta), ex.: `<img src="imagens-insta/1.jpg" ...>` e `background-image: url('imagens-insta/2.jpg')`.
  - Se houver fotos do Instagram mas menos de 5, completar o restante com a API da Unsplash (4a–4g) para chegar ao mínimo — mas as fotos reais ficam nas posições de maior destaque (hero, galeria).
  - Fotos do Instagram são arquivos locais: NÃO precisam de `onerror`/Picsum.
- **Se a pasta está vazia ou não existe**: seguir para 4a e buscar tudo na API oficial da Unsplash.

> ⚠️ **`source.unsplash.com` está PROIBIDO.** O endpoint foi descontinuado e passou a servir imagem aleatória (montanha/prédio no lugar do produto). Quando não há foto do Instagram, toda imagem vem da API oficial da Unsplash, com URLs reais e relevantes ao nicho.

#### 4a. Carregar a chave da API
A chave está em `.env` na raiz do projeto (`agencia-sites/.env`), variável `UNSPLASH_ACCESS_KEY`. Carregar antes de buscar:
```bash
export UNSPLASH_ACCESS_KEY=$(grep -E '^UNSPLASH_ACCESS_KEY=' /caminho/para/agencia-sites/.env | cut -d= -f2-)
```

#### 4b. Buscar fotos por keyword do nicho (1 chamada por nicho)
Fazer UMA busca por negócio (a chave demo tem limite de ~50 req/hora — não desperdiçar). Pedir várias fotos de uma vez e distribuir entre as seções:
```bash
curl -s "https://api.unsplash.com/search/photos?query=KEYWORD_DO_NICHO&per_page=20&orientation=landscape&content_filter=high" \
     -H "Authorization: Client-ID $UNSPLASH_ACCESS_KEY"
```
A keyword é específica do nicho (ver tabela em 4d). Da resposta JSON, usar o array `results[]` e pegar, para cada foto escolhida, o campo **`urls.raw`** (que aceita parâmetros de tamanho/qualidade do Imgix).

#### 4c. Montar a URL final de cada imagem
Pegar `urls.raw` de fotos DISTINTAS do `results[]` (uma para hero, uma para sobre, uma por card, uma para banner, duas para o mosaico) e anexar os parâmetros de dimensão/qualidade:
```
{urls.raw}&w=1400&h=900&fit=crop&q=80   ← hero / banner (grande)
{urls.raw}&w=800&h=600&fit=crop&q=80    ← sobre
{urls.raw}&w=600&h=400&fit=crop&q=80    ← cards / mosaico
```
O domínio dessas URLs é `images.unsplash.com/photo-...` — isso é o esperado AGORA (vem da API real, é válido e relevante). Não confundir com "ID chutado de cabeça", que continua proibido.

**Curadoria obrigatória:** olhar o campo `alt_description`/`description` de cada resultado e escolher fotos que realmente mostrem o produto/serviço. Se os primeiros resultados não baterem com o nicho, escolher outros do mesmo `results[]` ou refinar a keyword. PROIBIDO usar imagem sem relação com o negócio.

#### 4d. Em `<img>` — sempre com onerror fallback
```html
<img src="https://images.unsplash.com/photo-XXXX?w=600&h=400&fit=crop&q=80"
     onerror="this.src='https://picsum.photos/seed/rest1/600/400'"
     alt="..." loading="lazy">
```
O seed do Picsum é único por imagem (rest1, rest2, bakery1, etc.). O Picsum é só rede de segurança caso a URL da Unsplash falhe — o caminho principal é a foto real da API.

#### 4e. Em `background-image` (CSS, não suporta onerror)
Usar a URL real da Unsplash diretamente:
```css
background-image: url('https://images.unsplash.com/photo-XXXX?w=1400&h=900&fit=crop&q=80');
```

#### 4f. Se a API falhar (sem rede, 401, limite estourado)
PAUSAR e avisar o usuário (provável chave inválida ou limite de hora atingido). Como contorno temporário, pode usar Picsum com seed por nicho — mas registrar claramente que as imagens são placeholder e o site precisa ser regerado quando a API voltar. NUNCA voltar a usar `source.unsplash.com`.

#### 4g. Keywords (campo `query`) recomendadas por nicho
| Nicho | query principal | alternativas p/ curadoria |
|-------|-----------------|----------------------------|
| Padaria/Café | `bakery bread artisan` | `croissant`, `coffee shop`, `pastry` |
| Restaurante/Marmitaria | `brazilian food lunch` | `home cooked meal`, `restaurant dish`, `rice beans` |
| Doceria/Confeitaria | `cake dessert` | `birthday cake`, `sweets`, `cupcake` |
| Salão/Beleza | `hair salon beauty` | `hairstyle`, `manicure`, `makeup` |
| Pilates/Saúde | `pilates studio` | `pilates reformer`, `physiotherapy`, `stretching` |
| Tatuagem | `tattoo` | `tattoo studio`, `tattoo artist`, `fine line tattoo` |
| Academia | `gym fitness workout` | `weight training`, `crossfit` |
| Borracharia/Auto | `tire mechanic garage` | `auto repair`, `car workshop` |
| Clínica | `clinic medical care` | `dentist`, `healthcare` |

### Step 5 — Mapa de seções por nicho (define a ORDEM)

A ordem das seções **não é fixa** — muda conforme o nicho. A biblioteca de seções do Step 6 é a caixa de ferramentas; **este mapa decide quais entram e em que ordem**.

**Regra de ouro — prova visual cedo:** a prova do trabalho (portfólio, galeria, antes/depois, fotos dos pratos/bolos/tatuagens) aparece **logo depois do hero**, nas duas primeiras seções de conteúdo — **nunca enterrada no fim**. O cliente decide nos primeiros segundos olhando o trabalho, não lendo texto. Em fase de prospecção, com fotos reais do Instagram (checkpoint 8), essa seção é o que mais vende.

Nav fixo no topo, footer e botão WhatsApp flutuante estão **sempre** presentes (não entram no mapa, são fixos).

| Nicho | Ordem das seções (depois do Nav) |
|-------|----------------------------------|
| **Tatuagem** | Hero → **Portfólio (galeria de tattoos)** → Estilos (cards) → Processo (como funciona) → Depoimentos/Prova social → Instagram (chamada pro feed) → Contato (horário + mapa) |
| **Restaurante / Marmitaria** | Hero → **Pratos (cards com foto)** → Ambiente (mosaico) → Avaliações → Cardápio (banner + CTA) → Mapa → Contato |
| **Doceria / Confeitaria** | Hero → **Galeria (mosaico de doces)** → Sabores/Produtos (cards) → Depoimentos → Instagram → WhatsApp / Contato |
| **Salão / Beleza** | Hero → **Antes/depois ou Portfólio (galeria)** → Serviços (cards, com preço se houver) → Equipe (sobre) → Avaliações → Contato |
| **Pilates / Saúde / Bem-estar** | Hero → A profissional (sobre, breve) → **Aula experimental (banner + CTA)** → Benefícios (diferenciais) → Galeria (mosaico) → Depoimentos → Contato |
| **Genérico / outros nichos** | Hero → Diferenciais → Serviços/Produtos (cards) → **Prova visual (galeria/mosaico)** → Avaliações → Contato |
| **Serviço / SÓBRIO (Step 0)** | Hero tipográfico (proposta + telefone/WhatsApp) → **O que faço (serviços em lista/cards limpos)** → Área de atendimento (bairros/cidade + Maps) → Como funciona (peça o orçamento) → Por que confiar (diferenciais honestos, SVG) → Horários + Contato (WhatsApp em destaque) |

**Mapa SÓBRIO — regra:** aqui a "prova visual cedo" NÃO se aplica (não há portfólio forte). A prioridade acima da dobra é **o que faz + como falar com você (telefone/WhatsApp) + área de atendimento**. Sem galeria/mosaico de fotos de banco — mas **1-2 imagens de nicho relevantes** dão respiro (origem pelo gate do Princípio 31 / Step 4.0: no SÓBRIO quase sempre Unsplash com keyword específica do nicho; foto do Instagram do alvo só se ele for visual-autoral e tiver trabalho próprio usável): tipicamente 1 no hero split e/ou 1 acompanhando uma seção. Mínimo de 6 seções de conteúdo continua valendo (as da linha acima já somam 6).

**Como aplicar:**
- Montar as seções do Step 6 **nesta ordem**, não na ordem em que o código aparece no Step 6.
- A seção em **negrito** é a prova visual do nicho — é a primeira coisa de conteúdo depois do hero.
- Se um nicho não está na tabela, usar o mapa **Genérico** e adaptar pela lógica (prova visual cedo).
- Se a prova social é texto (3+ avaliações), os "Depoimentos/Avaliações" usam cards de review; se é agregada, usam o modo agregado (ver Pré-requisito e Seção 7 do Step 6).
- A seção "Instagram" (quando no mapa) é uma chamada curta com link para o perfil — só incluir se o negócio tem Instagram ativo.

### Step 6 — Biblioteca de seções (montar na ORDEM do mapa do Step 5)

As seções abaixo são a caixa de ferramentas (CSS + HTML de referência). **A ordem em que aparecem aqui não é a ordem do site** — montar conforme o mapa do nicho (Step 5). Mínimo de seções de conteúdo: 6 (além de Nav e Footer). Nav, Footer e WhatsApp flutuante são sempre incluídos.

#### Seção 1: Nav fixo com blur
```css
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 100;
  background: rgba(DARK_COLOR, 0.92);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  padding: 16px 32px;
  display: flex; align-items: center; justify-content: space-between;
  transition: background 0.3s;
}
```
Nav deve ter: logo à esquerda, links de navegação no centro (desktop), botão WhatsApp/telefone à direita.

#### Seção 2: Hero com imagem + animação + stats
```css
@keyframes slowZoom {
  from { transform: scale(1); }
  to { transform: scale(1.08); }
}
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(24px); }
  to { opacity: 1; transform: translateY(0); }
}

.hero {
  position: relative;
  min-height: 100vh;
  display: flex;
  align-items: center;
  overflow: hidden;
}
.hero-bg {
  position: absolute; inset: 0;
  background: url('UNSPLASH_URL') center/cover no-repeat;
  animation: slowZoom 20s ease-in-out infinite alternate;
}
.hero-overlay {
  position: absolute; inset: 0;
  background: linear-gradient(to right, rgba(0,0,0,0.82) 0%, rgba(0,0,0,0.35) 100%);
}
.hero-content {
  position: relative; z-index: 1;
  padding: 140px 48px 80px;
  max-width: 1100px; margin: 0 auto; width: 100%;
}
.hero-tag { animation: fadeUp 0.6s ease both; animation-delay: 0.2s; }
.hero h1  { animation: fadeUp 0.6s ease both; animation-delay: 0.4s; }
.hero p   { animation: fadeUp 0.6s ease both; animation-delay: 0.6s; }
.hero-ctas { animation: fadeUp 0.6s ease both; animation-delay: 0.8s; }
.hero-stats-box { animation: fadeUp 0.6s ease both; animation-delay: 1s; }

/* Stats no canto inferior direito */
.hero-stats-box {
  position: absolute;
  bottom: 40px; right: 48px;
  display: flex; gap: 32px;
}
.hero-stat { text-align: center; color: #fff; }
.hero-stat-num { font-size: 1.8rem; font-weight: 800; display: block; color: VAR_SECONDARY; }
.hero-stat-label { font-size: 0.72rem; text-transform: uppercase; letter-spacing: 1px; opacity: 0.75; }
```

Estrutura de HTML do hero:
```html
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-overlay"></div>
  <div class="hero-content">
    <span class="hero-tag">TAG DO NICHO</span>
    <h1>Headline em duas<br><em style="color:var(--secondary)">linhas com itálico</em></h1>
    <p>Subheadline convincente, 1-2 linhas.</p>
    <div class="hero-ctas">
      <a href="WHATSAPP_URL" class="btn-primary">CTA Principal →</a>
      <a href="#sobre" class="btn-outline">Conheça a história</a>
    </div>
  </div>
  <div class="hero-stats-box">
    <div class="hero-stat"><span class="hero-stat-num">DADO</span><span class="hero-stat-label">LABEL</span></div>
    <div class="hero-stat"><span class="hero-stat-num">DADO</span><span class="hero-stat-label">LABEL</span></div>
    <div class="hero-stat"><span class="hero-stat-num">DADO</span><span class="hero-stat-label">LABEL</span></div>
  </div>
</section>
```

#### Seção 3: Sobre — grid 2 colunas
```css
.sobre-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: center;
}
.sobre-img-wrap {
  position: relative;
  border-radius: 16px;
  overflow: hidden;
  aspect-ratio: 4/5;
}
.sobre-img-wrap img {
  width: 100%; height: 100%; object-fit: cover;
  transition: transform 0.8s ease;
}
.sobre-img-wrap:hover img { transform: scale(1.06); }
.bullet-list { list-style: none; }
.bullet-list li { padding: 10px 0; border-bottom: 1px solid rgba(0,0,0,0.08); display: flex; gap: 12px; align-items: center; }
.bullet-list li::before { content: "—"; color: var(--secondary); font-weight: 700; }
```

#### Seção 3.5: Nosso Compromisso / Processo / Benefícios (obrigatória — posição definida pelo mapa do nicho)

Seção curta com 3-4 bullets sobre valores e processo. Adaptar copy **e título** ao nicho (no mapa do Step 5 ela aparece como "Processo" em tatuagem, "Benefícios" em pilates, "Diferenciais" no genérico). A posição segue o mapa do nicho, não é fixa. Ícones são SVG inline, nunca emoji.

```html
<section class="compromisso">
  <div class="container">
    <p class="section-tag">COMO TRABALHAMOS</p>
    <h2 class="section-title">Nosso <em>compromisso</em> com você</h2>
    <div class="compromisso-grid">
      <div class="compromisso-item">
        <div class="compromisso-icon">
          <!-- SVG inline: ex. checkmark -->
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg>
        </div>
        <div>
          <h4>Título do valor</h4>
          <p>Descrição breve e específica do nicho — não genérica.</p>
        </div>
      </div>
      <!-- repetir para 3-4 bullets -->
    </div>
  </div>
</section>
```

```css
.compromisso { padding: 60px 48px; background: var(--primary); color: #fff; }
.compromisso .section-tag { color: var(--secondary); }
.compromisso .section-title { color: #fff; }
.compromisso-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 32px; margin-top: 32px; }
.compromisso-item { display: flex; gap: 16px; align-items: flex-start; }
.compromisso-icon {
  width: 48px; height: 48px; border-radius: 12px;
  background: rgba(255,255,255,0.12); border: 1px solid rgba(255,255,255,0.2);
  display: flex; align-items: center; justify-content: center;
  color: var(--secondary); flex-shrink: 0;
}
.compromisso-item h4 { font-size: 0.95rem; font-weight: 700; margin-bottom: 4px; }
.compromisso-item p { font-size: 0.85rem; opacity: 0.8; line-height: 1.55; }
```

**Copy por nicho:**
- Restaurante/padaria: "Ingredientes selecionados diariamente · Preparados na hora · Atendimento como família"
- Salão: "Escutamos antes de começar · Produtos de qualidade · Resultado que você leva pra casa"
- Academia: "Avaliação física na entrada · Treino adaptado ao seu nível · Acompanhamento constante"
- Borracharia: "Diagnóstico transparente · Preço fechado antes do serviço · Garantia em todo trabalho"

---

#### Seção 4: Cards de produtos/serviços com imagem

**ATENÇÃO — FOTO REAL EM CADA CARD (nicho visual):** Em nichos visuais (tatuagem, doceria/confeitaria, beleza/salão, restaurante), CADA card de estilo/serviço/produto DEVE ter uma **imagem real no topo** ilustrando aquele item específico. PROIBIDO card só com texto ou só com ícone SVG (como no exemplo antigo "Pontilhismo / Fine Line / Autoral" em texto puro). Ordem de prioridade da imagem de cada card:
1. **Foto da pasta `imagens-insta/`** do próprio negócio que represente aquele estilo/serviço — escolher, item por item, a foto que melhor mostra aquele estilo (ex.: a foto de pontilhismo no card "Pontilhismo", a de traço fino no "Fine Line"). É o que mais vende.
2. **API oficial da Unsplash com a keyword do estilo ESPECÍFICO** — só quando não há foto adequada do Instagram para aquele item. Buscar pela keyword do estilo, não a genérica do nicho: `dotwork tattoo`, `fine line tattoo`, `wedding cake`, `nail art`, etc. (reaproveitar o `results[]` da busca do Step 4 quando possível, para não gastar nova chamada).

O ícone SVG pode permanecer como detalhe decorativo dentro do card, mas **não substitui a foto**. Estrutura: `.card-img` no topo (foto), depois `.card-body` (título + texto). Mantém o hover `scale(1.06)` na imagem.

**ATENÇÃO — REGRA DE DESTAQUE:** Um dos 3 cards SEMPRE tem badge de destaque visível. Não deixar 3 cards idênticos.

```html
<!-- Card com badge de destaque -->
<div class="card card-featured">
  <div class="card-badge">⭐ Mais Pedido</div>
  <!-- resto do card -->
</div>
```

```css
.card-featured { border: 2px solid var(--secondary); box-shadow: 0 8px 32px rgba(0,0,0,0.15); }
.card-badge {
  position: absolute; top: 12px; right: 12px;
  background: var(--secondary); color: var(--dark);
  font-size: 0.72rem; font-weight: 800;
  padding: 4px 12px; border-radius: 50px;
  letter-spacing: 0.5px; text-transform: uppercase;
}
.card-img { position: relative; } /* para badge funcionar com position absolute */
```
```css
.cards-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}
.card {
  background: var(--bg-alt);
  border-radius: 16px;
  overflow: hidden;
  transition: transform 0.3s, box-shadow 0.3s;
}
.card:hover { transform: translateY(-8px); box-shadow: 0 20px 40px rgba(0,0,0,0.12); }
.card-img {
  height: 200px; overflow: hidden;
}
.card-img img {
  width: 100%; height: 100%; object-fit: cover;
  transition: transform 0.8s ease;
}
.card:hover .card-img img { transform: scale(1.06); }
.card-body { padding: 24px; }
.card-body h3 { font-family: DISPLAY_FONT; font-size: 1.2rem; margin-bottom: 8px; }
.card-body p { font-size: 0.9rem; color: var(--gray); line-height: 1.6; }
```

#### Seção 5: Banner de persuasão
```css
.banner {
  position: relative;
  padding: 100px 48px;
  text-align: center;
  overflow: hidden;
}
.banner-bg {
  position: absolute; inset: 0;
  background: url('UNSPLASH_URL') center/cover no-repeat;
}
.banner-overlay {
  position: absolute; inset: 0;
  background: rgba(0,0,0,0.72);
}
.banner-content {
  position: relative; z-index: 1; color: #fff;
}
```

#### Seção 6: Experiência com mosaico
```css
.experiencia-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: center;
}
.mosaic {
  position: relative;
  height: 480px;
}
.mosaic-img1 {
  position: absolute;
  top: 0; left: 0;
  width: 75%; height: 80%;
  border-radius: 16px;
  overflow: hidden;
}
.mosaic-img2 {
  position: absolute;
  bottom: 0; right: 0;
  width: 55%; height: 55%;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 20px 60px rgba(0,0,0,0.2);
}
.mosaic-img1 img, .mosaic-img2 img {
  width: 100%; height: 100%; object-fit: cover;
  transition: transform 0.8s;
}
.mosaic:hover .mosaic-img1 img { transform: scale(1.06); }
.mosaic:hover .mosaic-img2 img { transform: scale(1.06); }
.features-list { display: flex; flex-direction: column; gap: 28px; }
.feature-item { display: flex; gap: 16px; align-items: flex-start; }
.feature-icon { width: 48px; height: 48px; border-radius: 12px; background: var(--secondary); display: flex; align-items: center; justify-content: center; font-size: 1.4rem; flex-shrink: 0; }
```

#### Seção 7: Prova Social / Avaliações
**Se o briefing tem 3+ avaliações textuais reais:**
```css
.reviews-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}
.review-card {
  background: var(--bg-alt);
  border-radius: 16px;
  padding: 28px;
  border-top: 3px solid var(--secondary);
}
.review-stars { color: var(--secondary); font-size: 1rem; margin-bottom: 16px; }
.review-text { font-style: italic; color: #555; line-height: 1.7; margin-bottom: 20px; font-size: 0.95rem; }
.review-author { display: flex; align-items: center; gap: 12px; }
.review-avatar {
  width: 44px; height: 44px; border-radius: 50%;
  background: var(--secondary); color: var(--dark);
  display: flex; align-items: center; justify-content: center;
  font-weight: 800; font-size: 1.1rem;
}
.review-name { font-weight: 600; font-size: 0.9rem; }
.review-source { font-size: 0.78rem; color: var(--gray); }
```

**Se o briefing NÃO tem 3 avaliações textuais reais — modo agregado (não pausar):**
Montar a seção escolhendo o ângulo pela FORÇA (regra de força no Pré-requisito). Nunca inventar texto, número ou selo.
- **Volume ALTO** → estampar o número grande em destaque ("807 avaliações no Google", "+2.000 clientes"). Acompanhar da nota.
- **Volume BAIXO** → NÃO mostrar o número cru de avaliações. Trocar por: "96% recomendam", nota em estrelas grande sem volume ("5,0 ⭐"), tempo de mercado, ou diferencial. Um número pequeno diminui o dono e não convence — omitir e usar o ângulo verdadeiro mais forte.
- **Nota ALTA (4.5+)** sempre pode aparecer destacada.
- Pode empilhar provas fortes (nota + % recomendam + tempo de mercado).
- Estruturar como "Números que falam", "Nossa reputação" ou "Quem nos conhece, recomenda".
- Não criar cards de depoimento com texto inventado.

#### Seção 8: Horários + Mapa em grid 2 colunas
```css
.horario-mapa-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 48px;
  align-items: start;
}
.mapa iframe { width: 100%; height: 320px; border: 0; border-radius: 16px; }
```

#### Seção 9: Footer com 3 colunas
```css
footer {
  background: var(--dark);
  color: rgba(255,255,255,0.55);
  padding: 60px 48px 32px;
}
.footer-grid {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  gap: 48px;
  margin-bottom: 40px;
}
.footer-brand h3 { color: #fff; font-size: 1.2rem; margin-bottom: 12px; }
.footer-brand p { font-size: 0.88rem; line-height: 1.7; }
.footer-nav h4, .footer-contact h4 { color: rgba(255,255,255,0.75); font-size: 0.75rem; text-transform: uppercase; letter-spacing: 2px; margin-bottom: 16px; }
.footer-nav ul { list-style: none; }
.footer-nav ul li { margin-bottom: 8px; }
.footer-nav ul li a { color: rgba(255,255,255,0.55); text-decoration: none; font-size: 0.9rem; transition: color 0.2s; }
.footer-nav ul li a:hover { color: var(--secondary); }
.footer-bottom { border-top: 1px solid rgba(255,255,255,0.1); padding-top: 24px; text-align: center; font-size: 0.8rem; }
.footer-disclaimer { margin-top: 8px; font-size: 0.72rem; opacity: 0.5; letter-spacing: 0.3px; }
```

**Linha de prévia obrigatória no footer:** dentro de `.footer-bottom`, logo abaixo do copyright, incluir uma linha discreta sinalizando que o site é uma amostra:
```html
<p class="footer-disclaimer">Prévia / demonstração — site amostra, não oficial</p>
```
Esta linha deve estar presente em TODOS os sites gerados. É discreta (opacidade baixa, fonte pequena) mas honesta: o site é uma demonstração de prospecção, não a versão final contratada.

### Step 6.5 — Ajustes de layout (polimento obrigatório)

Quatro correções que separam um site "quase bom" de um site premium. Aplicar em todos.

#### 1. Hero sem espaço morto — o lado direito SEMPRE tem imagem
O hero nunca pode ter uma área vazia/cinza que pareça imagem quebrada. Duas formas válidas:
- **Hero full-bleed (padrão):** `.hero-bg` cobre 100% da tela (`inset:0; center/cover`) com overlay em gradiente. O conteúdo fica à esquerda; o lado direito mostra a imagem através do overlay mais claro. Garantir que a imagem real (foto do Instagram ou Unsplash) está carregada — nunca cor chapada sozinha.
- **Hero split (2 colunas):** se optar por texto à esquerda + imagem à direita, a coluna direita PRECISA conter uma `<img>` do nicho ocupando toda a coluna (`width:100%; height:100%; object-fit:cover`). Nunca deixar a coluna direita vazia ou só com cor de fundo.
```css
/* Se usar hero split, a coluna da imagem nunca fica vazia */
.hero-split { display: grid; grid-template-columns: 1.1fr 0.9fr; min-height: 100vh; }
.hero-split-img { position: relative; overflow: hidden; }
.hero-split-img img { width: 100%; height: 100%; object-fit: cover; }
```
Veto: hero com metade direita vazia/cinza parecendo imagem quebrada.

#### 2. Compactar seções altas demais
Seções com muito respiro vertical fazem o site parecer vazio e obrigam scroll infinito. Limites de padding vertical:
```css
section { padding-top: 72px; padding-bottom: 72px; }     /* padrão — não passar muito disso */
.compromisso, .banner-compacto { padding-top: 56px; padding-bottom: 56px; }  /* seções de apoio mais enxutas */
```
- Evitar `min-height: 100vh` em qualquer seção que não seja o hero.
- Se uma seção tem pouco conteúdo (3 bullets, um CTA), usar padding menor — não esticar para preencher tela.
- Mosaico/galeria: altura controlada (`max-height` em telas grandes), não deixar imagens gigantes.

#### 3. Hierarquia de CTAs — primário forte, secundário discreto
Em cada par de botões, o primário domina visualmente e o secundário recua. Nunca dois botões com o mesmo peso.
```css
.btn-primary {
  background: var(--secondary);     /* cor de marca de destaque — sólido, preenchido */
  color: var(--dark);
  padding: 16px 32px; border-radius: 8px;
  font-weight: 700; font-size: 1rem;
  box-shadow: 0 8px 24px rgba(0,0,0,0.18);
  transition: transform 0.2s, box-shadow 0.2s;
}
.btn-primary:hover { transform: translateY(-2px); box-shadow: 0 12px 32px rgba(0,0,0,0.24); }

.btn-outline {                       /* secundário — discreto, vazado, sem sombra */
  background: transparent;
  color: #fff; border: 1px solid rgba(255,255,255,0.5);
  padding: 15px 28px; border-radius: 8px;
  font-weight: 500; font-size: 0.95rem;
}
.btn-outline:hover { border-color: #fff; background: rgba(255,255,255,0.08); }
```
Regra: 1 primário por bloco de decisão. O secundário é menor, sem preenchimento e sem sombra. (A variação de texto dos CTAs continua valendo — ver tabela "Variação de CTAs por Intenção".)

#### 4. Botão WhatsApp flutuante harmonizado com a paleta
O botão fixo não pode ser verde-neon gritante que briga com a identidade. O **fundo do botão usa a cor da marca**; o verde pode aparecer só no ícone do WhatsApp.
```css
.whatsapp-float {
  position: fixed; bottom: 24px; right: 24px; z-index: 200;
  width: 56px; height: 56px; border-radius: 50%;
  background: var(--primary);          /* cor de marca, NÃO verde-neon */
  display: flex; align-items: center; justify-content: center;
  box-shadow: 0 6px 20px rgba(0,0,0,0.25);
  transition: transform 0.2s;
}
.whatsapp-float:hover { transform: scale(1.08); }
.whatsapp-float svg { width: 30px; height: 30px; fill: #fff; }  /* ícone branco ou verde discreto */
```
```html
<a href="WHATSAPP_URL" class="whatsapp-float" aria-label="Falar no WhatsApp" target="_blank">
  <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.434 9.889-9.885.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884-.001 2.225.651 3.891 1.746 5.634l-.999 3.648 3.742-.981z"/></svg>
</a>
```
Veto: botão WhatsApp em verde-neon que destoa da paleta. O fundo segue a marca (`--primary` ou `--secondary`); o verde fica restrito ao ícone, se usado.

### Step 6.6 — Engajamento e fechamento (4 ajustes obrigatórios)

Quatro ajustes de fase 1 (só código/design, sem conteúdo novo) validados em auditoria externa. Aplicar em todos os sites.

#### 1. Lightbox no portfólio — toda foto de trabalho é clicável
Cada imagem de galeria/portfólio amplia ao clique num modal/lightbox simples, 100% inline (sem biblioteca externa): fundo escurecido, foto ampliada, fechamento por X ou clique fora.
```css
.lightbox{position:fixed;inset:0;z-index:300;background:rgba(0,0,0,.9);display:none;align-items:center;justify-content:center;padding:28px;cursor:zoom-out;}
.lightbox.open{display:flex;}
.lightbox img{max-width:92vw;max-height:86vh;border-radius:10px;box-shadow:0 24px 80px rgba(0,0,0,.6);cursor:default;}
.lightbox-close{position:absolute;top:16px;right:24px;background:none;border:none;color:#fff;font-size:2.4rem;line-height:1;cursor:pointer;opacity:.8;}
.lightbox-close:hover{opacity:1;}
.gallery-item{cursor:zoom-in;}
```
```html
<!-- antes de </body> -->
<div class="lightbox" id="lightbox" role="dialog" aria-label="Foto ampliada">
  <button class="lightbox-close" aria-label="Fechar">&times;</button>
  <img src="" alt="">
</div>
<script>
(function(){
  var lb=document.getElementById('lightbox'),img=lb.querySelector('img');
  document.querySelectorAll('.gallery-item img').forEach(function(t){
    t.addEventListener('click',function(){img.src=t.src;img.alt=t.alt;lb.classList.add('open');});
  });
  lb.addEventListener('click',function(e){if(e.target!==img)lb.classList.remove('open');});
})();
</script>
```
Adaptar o seletor (`.gallery-item img`) à classe real da galeria do site. Vale para qualquer galeria de fotos do trabalho (tatuagens, bolos, pratos, antes/depois).

#### 1.1. Galeria / Portfólio — grade pela quantidade (fecha no desktop E no mobile)

A galeria pode ter quantas fotos boas o negócio tiver, desde que a grade **feche sem foto sobrando** nos dois tamanhos. Montar a grade pela QUANTIDADE de fotos boas:

| Fotos | Grade desktop |
|---|---|
| 4 | 2×2 |
| 5 | 1 destaque 2×2 + 4 (grade de 4 colunas) |
| 6 | 3 colunas — 1 destaque 2×2 + 5 |
| 8 | 2 linhas de 4 |
| 9 | 3×3 |

Se a contagem não fecha numa grade limpa, **remover a foto mais fraca** até fechar. Fotos boas que sobrarem vão para outras seções (hero, sobre, banner, cards) — nunca numa linha solta. A fonte das imagens NÃO muda (gate do Princípio 31 / Step 4.0).

**Mobile (2 colunas): nenhuma foto pode ficar sozinha numa linha** — se a contagem der ímpar no mobile, promover 1 foto a largura total (`span 2`) ou cortar a mais fraca.

```css
/* exemplo: 5 fotos = 1 destaque 2x2 + 4 */
.galeria-grid{display:grid;gap:12px;grid-template-columns:repeat(4,1fr);grid-auto-rows:1fr;}
.galeria-grid .g-destaque{grid-column:span 2;grid-row:span 2;}
.galeria-grid img{width:100%;height:100%;object-fit:cover;border-radius:10px;display:block;}
@media(max-width:768px){
  .galeria-grid{grid-template-columns:1fr 1fr;}          /* 2 colunas */
  .galeria-grid .g-destaque{grid-column:span 2;grid-row:auto;} /* destaque vira linha cheia; nunca foto sozinha */
}
```
Veto: grade com buraco/foto sobrando no desktop ou no mobile, ou foto sozinha numa linha de 2 colunas no celular.

#### 2. Seção "Como funciona" visual — cards numerados grandes ou linha do tempo
A seção de processo NÃO usa o formato "texto + ícone pequeno". Duas formas válidas (escolher uma):
- **Cards numerados:** cada passo é um card com o número em destaque tipográfico grande (fonte display, ~3rem, cor `--secondary`), título curto e 1-2 linhas de texto.
- **Linha do tempo:** passos conectados por uma linha visual (vertical ou horizontal), com marcadores numerados na cor de marca.

O conteúdo continua enxuto (3-4 passos, frases curtas e humanas) — o que muda é a apresentação.
```css
/* exemplo: cards numerados */
.processo-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:20px;}
.processo-step{background:var(--bg-alt);border:1px solid rgba(255,255,255,.06);border-radius:14px;padding:28px 24px;transition:transform .3s,border-color .3s;}
.processo-step:hover{transform:translateY(-6px);border-color:var(--secondary);}
.processo-num{font-family:var(--display);font-size:3rem;font-weight:700;color:var(--secondary);line-height:1;display:block;margin-bottom:14px;}
```
Veto: processo em lista "ícone pequeno + parágrafo" sem número grande nem linha do tempo.

#### 3. Rodapé aproveitado — fechamento útil
O rodapé não fecha o site vazio: além de navegação e contato, reaproveitar **2-3 itens úteis do material que o site JÁ tem** (sem inventar nada):
- Miniaturas de 2-3 fotos do trabalho, linkando para a galeria (`href="#portfolio"`);
- Selo/menção curta do diferencial real (ex.: "Agenda aberta", "Estúdio privativo", "Desde 2015");
- Link do Instagram do negócio.
```css
.footer-thumbs{display:flex;gap:10px;margin-top:16px;}
.footer-thumbs a{display:block;width:64px;height:64px;border-radius:8px;overflow:hidden;opacity:.85;transition:opacity .2s,transform .2s;}
.footer-thumbs a:hover{opacity:1;transform:translateY(-2px);}
.footer-thumbs img{width:100%;height:100%;object-fit:cover;}
```
Veto: footer só com navegação repetida + copyright, sem nenhum item reaproveitado.

#### 4. Não repetir a mesma prova social em destaque
Um mesmo número de prova social (ex.: "+27 mil seguidores", "807 avaliações") aparece **UMA vez em destaque** no site — na posição de maior impacto (geralmente a seção de prova social). Nas demais posições onde ele apareceria (hero-stats, banner), usar outro ângulo verdadeiro: diferencial ("100% autoral"), especialidade ("fine line"), condição real ("agenda aberta"). Repetir o número dilui o impacto e parece falta de conteúdo.
Veto: o mesmo número estampado em destaque duas vezes no mesmo site.

### Step 7 — Responsividade (768px)
```css
@media (max-width: 768px) {
  .sobre-grid, .experiencia-grid, .horario-mapa-grid, .footer-grid { grid-template-columns: 1fr; gap: 32px; }
  .cards-grid { grid-template-columns: 1fr; }
  .reviews-grid { grid-template-columns: 1fr; }
  .hero-stats-box { position: static; flex-direction: row; justify-content: center; padding: 24px 0 0; }
  .hero-content { padding: 100px 24px 60px; }
  .mosaic { height: 300px; }
  nav .nav-links { display: none; }
}
```

### Step 8 — Salvar o arquivo
Salvar em: `squads/prospeccao-sites/output/{run_id}/{slug-negocio}/site.html`

### Step 8.5 — Inserir o snippet do Vercel Analytics (antes do deploy)

Todo site novo recebe o Vercel Web Analytics **ANTES do deploy**, para medir se o alvo abriu o link (dado agregado — ver documento-vivo → "Analytics em sites novos"). Inserir, logo antes de `</body>`:
```html
<script defer src="/_vercel/insights/script.js"></script>
```
O `script.js` é servido pela própria Vercel após o deploy (responde 200 quando o projeto está na conta e o Analytics está ligado). Não há chave nem config no HTML além dessa linha — nada de segredo no arquivo.

### Step 9 — Deploy ao vivo no Vercel (conta pessoal)

Depois de salvar o `site.html` (já com o snippet do Step 8.5), publicar o site no Vercel para gerar uma URL pública que o cliente possa abrir no celular. O deploy é feito na **conta PESSOAL** (`miguelmagsilveira-3897`), nunca na de trabalho. Os screenshots continuam sendo capturados normalmente (Carlos depende deles) — o deploy é um complemento, não substitui as imagens.

**Comando (sempre com prefixo `npx vercel`):** a partir da pasta do negócio (`squads/prospeccao-sites/output/{run_id}/{slug-negocio}/`), rodar:
```bash
npx vercel deploy --prod
```
O Vercel publica o conteúdo da pasta e retorna a URL pública de produção (ex.: `https://nome-do-projeto.vercel.app`).

**⚠️ PRIMEIRO DEPLOY — PARAR e perguntar ao usuário:** na primeiríssima vez que o deploy roda, o Vercel faz perguntas interativas no terminal que definem como os projetos ficam organizados na conta. Exemplos:
- `Set up and deploy "..."?`
- `Which scope do you want to deploy to?`
- `Link to existing project?`
- `What's your project's name?`
- `In which directory is your code located?`

**NÃO responder sozinho.** Capturar as perguntas exatas, PAUSAR e mostrar ao usuário para ele decidir. Uma resposta automática errada cria projeto bagunçado no Vercel que dá trabalho pra reorganizar depois. A partir do segundo deploy, quando a pasta já estiver linkada (existe `.vercel/`), o comando roda sem perguntas e pode prosseguir normalmente.

**Salvar a URL retornada:** gravar a URL pública de produção num arquivo `link-ao-vivo.txt` na pasta do negócio:
```
squads/prospeccao-sites/output/{run_id}/{slug-negocio}/link-ao-vivo.txt
```
O arquivo contém apenas a URL (uma linha). Carlos e Eduardo leem esse arquivo para incluir o link no email e no kit.

**Ao final do lote — lista de Analytics para o Miguel:** o "Enable" do Web Analytics é um passo só-painel. Depois de deployar todos os sites do lote, entregar ao Miguel a lista de links `https://vercel.com/miguelmagsilveira-3897/<projeto>/analytics` (um por site) para ele clicar **Enable** em todos de uma vez.

**Se o deploy falhar** (erro de rede, autenticação, etc.): PAUSAR, mostrar a mensagem de erro exata ao usuário e não inventar uma URL. O `link-ao-vivo.txt` só é criado com uma URL real retornada pelo Vercel.

## Referência: SVG Line-Style Icons (Lucide/Feather)

Usar em feature-icons, Nosso Compromisso, e Diferenciais. Nunca emoji nesses contextos.

```html
<!-- Relógio / horário / 24h -->
<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"></circle><polyline points="12 6 12 12 16 14"></polyline></svg>

<!-- Estrela / qualidade -->
<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>

<!-- Mapa-pin / localização -->
<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"></path><circle cx="12" cy="10" r="3"></circle></svg>

<!-- Checkmark / garantia -->
<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg>

<!-- Escudo / segurança / confiança -->
<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"></path></svg>

<!-- Coração / cuidado -->
<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"></path></svg>

<!-- Troféu / prêmio / experiência -->
<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="6 9 6 2 18 2 18 9"></polyline><path d="M6 18H4a2 2 0 0 1-2-2v-1a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v1a2 2 0 0 1-2 2h-2"></path><rect x="6" y="18" width="12" height="4"></rect></svg>

<!-- Calendário / agendamento -->
<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect><line x1="16" y1="2" x2="16" y2="6"></line><line x1="8" y1="2" x2="8" y2="6"></line><line x1="3" y1="10" x2="21" y2="10"></line></svg>
```

## Referência: Variação de CTAs por Intenção

Nunca repetir o mesmo CTA em todos os botões do site. Cada posição tem uma intenção diferente:

| Posição | Intenção do visitante | CTA sugerido |
|---------|----------------------|--------------|
| Hero CTA primário | Pronto para agir agora | "Reservar mesa →" / "Agendar agora" / "Ligar: (XX) XXXXX" |
| Hero CTA secundário | Quer conhecer antes | "Ver o cardápio" / "Conheça a história" / "Ver serviços" |
| Nosso Compromisso | Comparando opções | "Por que somos diferentes?" / "Ver depoimentos" |
| Banner de persuasão | Quase convencido | "Falar agora" / "Tirar minha dúvida" / "Estou interessado" |
| Cards de destaque | Quer mais detalhes | "Ver opções →" / "Saber mais" / "Quero esse" |
| Seção de avaliações | Precisando de validação | "Ver todas as avaliações" / "Conhecer no Maps" |
| CTA Final | Tomando a decisão | "Estamos esperando você" / "Vamos conversar?" / "Começar agora" |

## Veto Conditions

> **Escopo por tratamento (Step 0):** os vetos 1, 3, 3c, 4, 5, 7b, 20 e 24 pressupõem o tratamento **RICO** (dependente de foto). No tratamento **SÓBRIO/FUNCIONAL** eles NÃO se aplicam — lá o hero é tipográfico, há poucas/nenhuma imagem de banco, e não há prova visual de portfólio. No SÓBRIO valem, em vez disso, os vetos sóbrios abaixo (S1–S3). Todos os demais vetos valem para os dois tratamentos.
>
> **Vetos do tratamento SÓBRIO:**
> - **S1.** Hero sem proposta clara do serviço OU sem telefone/WhatsApp visível.
> - **S2.** Faltar qualquer um: o que faz (serviços), área de atendimento, "orçamento no WhatsApp", horários.
> - **S3.** **Encher** de foto de banco (mosaico/galeria) OU usar imagem **sem relação** com o nicho. 1-2 imagens de nicho bem escolhidas e relevantes são ESPERADAS — o veto é contra excesso ou irrelevância, não contra ter imagem.
> - **S4.** Site sóbrio **totalmente sem imagem**, árido, quando havia imagem de nicho relevante disponível (Instagram ou Unsplash com keyword específica). O padrão sóbrio é 1-2 imagens propositais, não zero.

Reject and redo if ANY are true:
1. Hero usa gradiente chapado sem background-image real (foto da API da Unsplash) — *tratamento RICO*
2. Fontes são Poppins como display principal
3. Menos de 5 imagens reais no total
3b. Qualquer URL `source.unsplash.com` no HTML (endpoint descontinuado/proibido — usar a API oficial do Step 4)
3c. Imagem sem relação com o nicho (ex.: paisagem/prédio num site de tatuagem ou doceria)
4. Sem animação slowZoom no hero
5. Sem fadeUp escalonado no texto do hero
6. Seção Sobre sem grid 2 colunas (imagem | texto)
7. Menos de 6 seções de conteúdo (além de Nav e Footer), ou ordem que não segue o mapa de seções do nicho (Step 5)
7b. Prova visual do nicho (portfólio/galeria/antes-depois/fotos do produto) enterrada no fim — deve aparecer logo após o hero (Step 5, regra de ouro)
8. Cards de avaliação com texto inventado
9. Sem botão WhatsApp flutuante
10. Paleta com apenas 2 cores
11. Qualquer CTA com placeholder (`wa.me/55?`, "consulte horários", "em breve")
12. Feature-icons com emoji (devem ser SVG inline)
13. 3 cards de serviço/cardápio idênticos sem badge de destaque
14. Ausência da seção de diferenciais/processo (Nosso Compromisso ou o equivalente do nicho: "Processo", "Benefícios", "Diferenciais")
15. Todos os botões do site com CTA idêntico
16. Site rejeitado ou pausado por falta de texto de avaliação (texto é bônus — usar prova social agregada)
17. Volume baixo de avaliações estampado cru no site (ex: "12 avaliações") em vez de um ângulo verdadeiro mais forte
18. Qualquer número, selo ou depoimento inventado na prova social
19. Especialidade/diferencial afirmado sem comprovação no briefing ou na investigação (ex.: "especialista em X", "premiado", "o melhor da cidade" sem fonte) — ver Step 1.5
20. Hero com espaço morto/coluna direita vazia parecendo imagem quebrada (Step 6.5.1)
21. Seção que não é o hero usando `min-height: 100vh` ou padding vertical excessivo que deixa o site vazio (Step 6.5.2)
22. CTA primário e secundário com o mesmo peso visual (devem ter hierarquia — Step 6.5.3)
23. Botão WhatsApp flutuante em verde-neon que destoa da paleta (fundo deve ser cor de marca; verde só no ícone — Step 6.5.4)
24. Card de estilo/serviço/produto só com texto ou só com ícone SVG (sem foto real) em nicho visual — tatuagem, doceria, beleza, restaurante (Step 6, Seção 4 — foto do Instagram primeiro, Unsplash do estilo específico como fallback)
25. Headline do hero institucional/genérica que serviria para qualquer negócio do mesmo nicho, sem nada concreto do diferencial real (Step 1.5 — regra de especificidade)
26. Conteúdo de fase 2 fabricado ou com buraco no lugar — foto do dono trabalhando, "Conheça a [pessoa]" com foto real, depoimento de cliente encenado, print de avaliação inventado (Trava de Fase 1 vs Fase 2)
27. Galeria/portfólio sem lightbox — foto de trabalho que não amplia ao clique (Step 6.6.1)
28. Seção de processo/"Como funciona" em formato "texto + ícone pequeno", sem cards numerados grandes nem linha do tempo (Step 6.6.2)
29. Rodapé vazio/genérico, sem nenhum item útil reaproveitado (miniaturas do trabalho, selo do diferencial, Instagram) (Step 6.6.3)
30. O mesmo número de prova social em destaque duas vezes no site (Step 6.6.4)
31. Foto do Instagram do alvo usada fora do gate de 2 condições — nicho não visual-autoral (prestador de serviço) ou sem trabalho próprio usável (Step 4.0 / Princípio 31). Fora do gate, a imagem vem da Unsplash oficial + Picsum
32. Galeria com grade que não fecha (buraco/foto sobrando) no desktop ou no mobile, ou foto sozinha numa linha de 2 colunas no celular (Step 6.6.1.1 / Princípio 32)
33. Site deployado sem o snippet do Vercel Analytics (`/_vercel/insights/script.js`), ou deployado na conta de trabalho em vez da pessoal (Step 8.5 / Step 9 / Princípio 33)
