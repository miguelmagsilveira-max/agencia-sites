# Output Examples — Prospecção de Sites

## Exemplo 1: Barbearia (Score 8/10)

### briefing.md
```markdown
# Briefing — Barbearia Premium do Zé

## 1. Identidade do Negócio
Barbearia masculina premium fundada há 3 anos no centro de Campinas.
Especializada em cortes modernos, barba e tratamentos capilares.
Tom casual mas profissional nas redes sociais.

## 2. Público-Alvo
Homens de 25-45 anos, profissionais com renda média-alta.
Valorizam qualidade e experiência acima do preço.
Inferido das avaliações: clientes fiéis que retornam quinzenalmente.

## 3. Produto/Serviço
- Corte masculino (R$55)
- Barba completa (R$40)
- Combo corte + barba (R$80)
- Progressiva masculina (R$120)
Destaques nas avaliações: atendimento personalizado, ambiente relaxante, pontualidade.

## 4. Identidade Visual Existente
Instagram (@barbearia_do_ze): feed marrom escuro + bege, tipografia bold moderna.
Logo: tesoura estilizada em dourado. Fotos profissionais dos cortes.

## 5. Concorrência e Posicionamento
3 barbearias no mesmo bairro. Zé tem mais avaliações (127 vs 34 e 22 dos concorrentes).
Posicionamento premium — não compete em preço.

## 6. Objetivo do Site
Exibir serviços e preços, receber agendamentos via WhatsApp, mostrar avaliações para novos clientes.

## 7. Presença Digital Atual
- Instagram: 1.240 seguidores, 3 posts/semana, boa interação
- Facebook: página com 430 curtidas, menos ativo
- Google Maps: 4.8⭐ (127 avaliações)
- TripAdvisor: não encontrado
- Solutudo: não encontrado
- Site: nenhum

## 8. Conteúdo Disponível
Avaliações reais coletadas:
- "Melhor barbearia de Campinas. O Zé conhece cada cliente pelo nome." — Carlos M., 2026-03-15
- "Ambiente incrível, café na chegada e saio sempre perfeito. Recomendo!" — Rafael T., 2026-02-28
- "Pontual e profissional. Nunca precisei esperar mais de 5 minutos." — Lucas A., 2026-01-10
```

### site.html (trecho estrutural)
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Barbearia Premium do Zé — Campinas</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    :root { --brown: #4a2c17; --gold: #c9a84c; --beige: #f5f0e8; }
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: 'Poppins', sans-serif; background: #fff; }
    /* ... 300+ linhas de CSS ... */
  </style>
</head>
<body>
  <!-- Hero -->
  <section class="hero">
    <h1>A melhor barbearia de Campinas</h1>
    <p>Mais de 127 avaliações 5⭐ no Google</p>
    <a href="https://wa.me/5519998123456?text=Oi!+Quero+agendar+um+horário" class="btn-primary">
      Agendar pelo WhatsApp
    </a>
  </section>
  <!-- Serviços, Avaliações reais, Sobre, Mapa -->
  <!-- WhatsApp flutuante -->
  <a href="https://wa.me/5519998123456" class="whatsapp-float" aria-label="WhatsApp">📱</a>
</body>
</html>
```

### email.md
```markdown
## Assunto
Site pronto para a Barbearia do Zé

## Corpo
Olá, Barbearia do Zé!

Vi as avaliações de vocês no Google — 127 avaliações com 4.8 estrelas é raro de ver. Parabéns pelo trabalho de verdade.

Com uma reputação dessas, imagina se quem busca "barbearia em Campinas" no Google chegasse direto num site mostrando essas avaliações e já saísse com o horário agendado?

Criei uma versão de como ficaria. Posso te mandar?

Pedro
Agência de Sites

## Notas
- Destinatário: contato@barbeariazecampinas.com.br
- Relacionamento: cold (primeiro contato)
- Follow-up: dia 3 após envio se sem resposta
- Melhor horário de envio: terça 9h
```

---

## Exemplo 2: Restaurante (Score 7/10)

### email.md
```markdown
## Assunto
Cardápio online para o Sabor da Vila

## Corpo
Olá, Sabor da Vila!

Vi o comentário da Dona Marcia: "melhor moqueca de camarão que já comi na vida". São 89 avaliações assim no Google de vocês.

Muita gente que busca "restaurante nordestino em São Paulo" no Google não te encontra porque você não tem site ainda. Essa galera vai pro concorrente — não porque é melhor, mas porque aparece.

Criei um site com o cardápio completo e um botão de reserva pelo WhatsApp. Quer ver como ficou?

Ana
Agência de Sites

## Notas
- Destinatário: sabordavila@gmail.com (via Facebook)
- CTA: pergunta aberta, baixo compromisso
```

---

## Exemplo de Veredicto — Vera Veredito

```
==============================
 REVIEW VERDICT: APROVADO
==============================

Negócio: Barbearia Premium do Zé
Revisão: 1 de 3

SITE HTML:
✅ Avaliações conferidas com briefing.md — textos idênticos
✅ Nome correto em toda a página ("Barbearia Premium do Zé")
✅ WhatsApp: (19) 99812-3456 — número verificado
✅ Meta viewport presente — mobile-first confirmado
✅ Design marrom/dourado coerente com identidade visual do Instagram

EMAIL:
✅ 82 palavras — dentro do limite (60-100)
✅ Elogio baseado em dado real: 4.8⭐ com 127 avaliações (verificado no briefing)
✅ Problema plantado específico ao nicho: busca de barbearia no Google
✅ CTA de pergunta: "Posso te mandar?" — baixo compromisso
✅ Assunto: 5 palavras, sem caixa alta

VEREDICTO: APROVADO
Artefatos prontos para aprovação final do usuário.
```
