# Investigação: Design de Landing Pages para Comércio Local

## Fonte 1: Divia Marketing Digital — Landing Pages para Bares e Restaurantes
URL: https://www.divia.com.br/criacao-de-landing-pages-para-bares-e-restaurantes

### Estrutura ideal de site para comércio local
1. **Hero section**: Foto impactante do negócio + headline com o principal benefício + CTA (WhatsApp ou "Ver cardápio")
2. **Sobre**: História curta e autêntica do negócio (1-2 parágrafos), tom pessoal
3. **Produtos/Serviços**: Os 3-6 mais importantes com foto + nome + descrição curta
4. **Avaliações**: Seção com avaliações reais do Google (citações com nome do cliente)
5. **Contato/Localização**: Mapa embed + telefone + WhatsApp button + horários
6. **CTA flutuante**: Botão WhatsApp fixo no canto inferior direito

### Elementos visuais que convertem
- Mobile-first obrigatório (80%+ dos acessos são mobile)
- SSL (cadeado) — transmite credibilidade
- Carregamento rápido (abaixo de 3 segundos)
- Fotos profissionais ou de alta qualidade do negócio
- Botão WhatsApp verde visível em todas as telas
- Cores coerentes com a identidade visual do negócio
- Tipografia legível em tela pequena

### Seções obrigatórias por nicho

**Restaurante/Lanchonete:**
- Hero + tagline + botão "Ver cardápio" / "Fazer pedido"
- Cardápio digital com fotos dos pratos principais
- Avaliações do Google
- Horário de funcionamento + endereço + mapa
- Botão WhatsApp para pedido/reserva

**Salão de Beleza/Barbearia:**
- Hero + headline de benefício + botão "Agendar agora"
- Serviços com preço e duração
- Galeria antes/depois
- Avaliações do Google
- Botão WhatsApp para agendamento

**Clínica/Consultório:**
- Hero + headline de credibilidade + botão "Agendar consulta"
- Especialidades/serviços
- Sobre o profissional (foto, formação, CRM/CRO)
- Avaliações de pacientes
- Formulário ou WhatsApp para agendamento

**Loja/Comércio Geral:**
- Hero + oferta principal + CTA
- Produtos/categorias em destaque
- Diferenciais do negócio
- Avaliações Google
- Contato + localização + horários

---

## Fonte 2: Pesquisa sobre estrutura HTML para comércio local

### Princípios técnicos de desenvolvimento
- HTML semântico (section, article, nav, footer)
- CSS com variáveis de cor para fácil personalização
- Font: Google Fonts (Inter, Roboto ou Poppins — legibilidade mobile)
- Imagens: uso de placeholder ou referência a fotos reais do negócio
- Integração WhatsApp: `https://wa.me/55{telefone}?text={mensagem}`
- Google Maps embed via iframe

### Anti-patterns de design local
1. **Texto demais** na hero section (máx 10 palavras no headline)
2. **Sem botão WhatsApp** — canal principal de conversão no Brasil
3. **Não mobile-optimizado** — mais de 80% dos acessos são mobile
4. **Sem avaliações** — prova social é crucial para comércio local
5. **Cores aleatórias** sem identidade da marca
6. **Formulário de contato** sem alternativa de WhatsApp
7. **Sem horários de funcionamento** — dúvida comum do cliente local

---

## Padrões identificados (síntese)

### Estrutura universal para qualquer comércio local
```
1. Hero (foto + headline curto + CTA primário)
2. Diferenciais (3 ícones + texto curto)
3. Produtos/Serviços (grid com fotos)
4. Avaliações Google (citações reais)
5. Sobre o negócio (foto + texto pessoal)
6. Contato (mapa + telefone + horários)
7. WhatsApp flutuante (sempre visível)
```

### Copy que funciona para comércio local
- Headline: "[Benefício principal] em [Cidade]" — ex: "A melhor pizza artesanal em Campinas"
- Sub-headline: "[Prova social ou diferencial]" — ex: "Mais de 500 avaliações 5 estrelas no Google"
- CTA: "Fazer pedido pelo WhatsApp" / "Agendar agora" / "Ver cardápio"
- Sobre: "Fundado em [ano] por [nome], o [negócio] nasceu com a missão de..."
- Avaliações: usar citações reais extraídas do Google

### Elementos técnicos essenciais
- `<meta viewport>` para responsividade
- `<a href="https://wa.me/...">` botão WhatsApp flutuante
- `<iframe>` Google Maps embed
- Schema.org LocalBusiness markup para SEO local
- Lazy loading nas imagens
