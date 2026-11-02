# Análise Consolidada — Investigação de Referências

## Perfis Investigados
- **Cold email / Copywriting B2B**: protagnst.com, eesier.com.br, blog.umbler.com (estratégias de agências digitais)
- **Design landing pages comércio local**: divia.com.br, templatemonster.com, mobirise.com

---

## DOMÍNIO 1: Cold Email para Venda de Sites

### Framework Recomendado (Observação → Problema → Pergunta)
1. **Observação personalizada**: Mencione algo específico e real do negócio (avaliações, localização, produto)
2. **Planta o problema suavemente**: Sugira o que eles estão perdendo SEM site (clientes que buscam online, avaliações que não convertem)
3. **Mostre a solução pronta**: Diga que já criou uma versão — não fale de serviço abstrato
4. **Pergunta aberta de baixo compromisso**: "Posso te mandar?" ou "Vale dar uma olhada?"

### Estrutura de email validada (60-100 palavras)
```
Assunto: Site para [Nome do negócio] (ou "Vi você no Google Maps")

[Nome],

Vi as avaliações do [negócio] no Google — [elogio genuíno específico].

[Planta o problema]: Imagina se quem busca por [nicho] em [cidade] chegasse direto no seu site com essas avaliações na página inicial?

Criei uma versão de como ficaria. Posso te mandar?

[Seu nome]
Agência de Sites
```

### Melhores práticas validadas
- Email enviado terça, quarta ou quinta entre 9h-11h30
- Assunto: 3-5 palavras, sem caixa alta, sem emoji
- Nome correto do estabelecimento (verificado antes)
- Elogio genuíno baseado em avaliações reais lidas
- CTA único por email
- Follow-up no 2º dia (sem resposta): variar o ângulo

### Anti-patterns (nunca fazer)
1. Vender no primeiro email
2. Email com mais de 3 parágrafos
3. "Prezado empreendedor" sem nome
4. Listar preços ou pacotes no primeiro contato
5. CTA com urgência falsa ("Vagas limitadas!", "Só até sexta!")
6. CC para outros destinatários

---

## DOMÍNIO 2: Design de Sites para Comércio Local

### Framework Recomendado — Estrutura Universal
```
Seção 1 — Hero
  - Foto principal do negócio (high quality ou placeholder)
  - Headline: "[Diferencial] em [Cidade]"
  - Sub: prova social ou 2ª linha de benefício
  - CTA: botão WhatsApp ou ação principal

Seção 2 — Diferenciais (3 colunas com ícone + texto)

Seção 3 — Produtos/Serviços em destaque (grid com foto)

Seção 4 — Avaliações reais do Google (3-5 citações)

Seção 5 — Sobre o negócio (foto + história curta)

Seção 6 — Contato
  - Google Maps embed
  - Telefone clicável (tel:)
  - Horários de funcionamento
  - Endereço

Footer + WhatsApp flutuante (sempre visível)
```

### Elementos técnicos obrigatórios
- Mobile-first (`<meta viewport>`)
- Botão WhatsApp flutuante: `https://wa.me/55{DDDtelefone}`
- Google Maps embed via `<iframe>`
- Cores da identidade visual do negócio (extraídas de redes sociais)
- CSS inline ou único arquivo (para entrega em HTML único)
- Avaliações reais do Google citadas literalmente no HTML

### Diferenciação por nicho
| Nicho | CTA principal | Seção especial |
|---|---|---|
| Restaurante/Bar | "Ver cardápio" / "Fazer pedido" | Cardápio digital com fotos |
| Salão/Barbearia | "Agendar agora" | Galeria antes/depois |
| Clínica/Consultório | "Agendar consulta" | Credenciais do profissional |
| Loja/Comércio | "Falar no WhatsApp" | Produtos em destaque |
| Pet shop | "Agendar banho/tosa" | Serviços + preços |
| Academia | "Conhecer planos" | Modalidades + horários |

---

## DOMÍNIO 3: Prospecção no Google Maps

### Metodologia de prospecção validada
1. Buscar categoria + cidade no Google Maps
2. Filtrar negócios: sem site OU site inativo/mal feito
3. Priorizar: 4+ estrelas, 20+ avaliações, perfil ativo
4. Coletar: nome, telefone, email (via FB/Instagram), avaliações, segmento, endereço
5. Verificar em: Facebook, Instagram, TripAdvisor, Restaurant Guru, Solutudo

### Score de priorização (0-10)
- **Avaliações Google** (0-3 pts): 1-10 avaliações=1, 11-50=2, 51+=3
- **Nota média** (0-2 pts): abaixo de 3=0, 3-3.9=1, 4+=2
- **Ausência de site** (0-2 pts): tem site=0, site ruim=1, sem site=2
- **Presença ativa em redes** (0-2 pts): sem redes=0, ativa=2
- **Ticket médio do nicho** (0-1 pt): nichos de ticket alto=1

### Nichos de alta prioridade
- Clínicas médicas e odontológicas
- Hotéis e pousadas
- Restaurantes e bares temáticos
- Salões de beleza e barbearias premium
- Academias de dança, artes marciais
- Pet shops e clínicas veterinárias

---

## Recomendações para os Agentes do Squad

### Para o Copywriter
- Usar avaliações reais coletadas pelo Pesquisador como elogio genuíno
- Adaptar o "problema plantado" ao nicho (restaurante = sem pedido online, clínica = sem agendamento digital)
- Assunto do email mencionar o nome do negócio ou cidade
- Email: 60-100 palavras, finalizar com pergunta, nunca com pitch

### Para o Dev/Designer
- Usar HTML único autocontido (CSS inline + no `<style>`)
- Incorporar avaliações reais do Google coletadas pelo Pesquisador
- Adaptar seções por nicho (ver tabela acima)
- WhatsApp flutuante obrigatório em todos os sites
- Mobile-first sempre

### Para o Prospector
- WhatsApp em 99% dos perfis Google Maps — coletar sempre
- Email: buscar no Facebook/Instagram/Solutudo se não estiver no Maps
- Priorizar negócios com 20+ avaliações e nota 4+
- Evitar negócios já contatados nos últimos 30 dias (verificar contatados.md)
