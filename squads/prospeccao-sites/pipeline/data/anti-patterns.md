# Anti-Patterns — Prospecção de Sites

## Anti-Patterns de Prospecção

### 1. Inventar dados
**O que é:** Preencher campos vazios com informações não encontradas publicamente.
**Por que é prejudicial:** Envia email para endereço errado, menciona avaliações falsas, perde credibilidade imediatamente.
**Como evitar:** Se não encontrou o email, registrar como "email não encontrado". Nunca inferir.

### 2. Incluir negócios com site ativo
**O que é:** Incluir na lista negócios que já têm site funcional.
**Por que é prejudicial:** Perde tempo com leads que não têm a necessidade que resolve.
**Como evitar:** Verificar campo "site" no Google Maps. Sites em construção ou redirect count como "sem site".

### 3. Ignorar o contatados.md
**O que é:** Não verificar a lista de negócios já contatados antes de prospectar.
**Por que é prejudicial:** Contato repetido em menos de 30 dias parece spam e queima o relacionamento.
**Como evitar:** Sempre ler contatados.md como primeira ação do Prospector.

---

## Anti-Patterns de Investigação

### 4. Parafrasear avaliações
**O que é:** Reescrever as avaliações coletadas em vez de copiá-las literalmente.
**Por que é prejudicial:** O poder do email está em usar as palavras EXATAS do cliente. Parafrasear dilui a autenticidade.
**Como evitar:** Copiar avaliação com aspas, nome do avaliador e data. Verificar no HTML que é idêntico ao briefing.

### 5. Confundir negócios com nomes similares
**O que é:** Coletar dados da "Barbearia do João" de outra cidade que não a pesquisada.
**Por que é prejudicial:** Email com dados errados destrói credibilidade na primeira linha.
**Como evitar:** Sempre verificar cidade + nome + endereço antes de confirmar o perfil.

---

## Anti-Patterns de Email

### 6. Vender no primeiro email
**O que é:** Mencionar preços, pacotes, contratos ou pedir uma decisão de compra.
**Por que é prejudicial:** Primeiro email frio que tenta vender é deletado. O objetivo é iniciar conversa.
**Como evitar:** Finalizar sempre com pergunta aberta. Nunca com CTA de "compre" ou "contrate".

### 7. "Prezado empreendedor" sem personalização
**O que é:** Começar o email com saudação genérica ou sem o nome do negócio.
**Por que é prejudicial:** Sinaliza instantaneamente que é template em massa. Taxa de resposta cai para zero.
**Como evitar:** Sempre usar o nome do negócio. Se disponível, usar o nome do dono.

### 8. Email longo (mais de 150 palavras)
**O que é:** Escrever parágrafos longos explicando o serviço, benefícios, diferenciais.
**Por que é prejudicial:** Emails longos de cold outreach são escaneados e deletados no mobile.
**Como evitar:** Target: 60-100 palavras. Máximo: 150 palavras. Uma ideia por parágrafo.

### 9. Múltiplos CTAs
**O que é:** Pedir que o destinatário faça várias ações ("veja o site, me liga, se inscreve").
**Por que é prejudicial:** Paralisia de decisão. Nenhuma ação é tomada.
**Como evitar:** Exatamente 1 CTA. Sempre no formato de pergunta.

### 10. Urgência falsa
**O que é:** "Últimas vagas", "Promoção só até sexta", "Responda hoje".
**Por que é prejudicial:** Destruição de credibilidade. Pequenos empresários identificam pressão fake imediatamente.
**Como evitar:** Zero urgência no primeiro email. Oferta direta e sem pressão.

---

## Anti-Patterns de Design

### 11. Site não mobile
**O que é:** HTML sem meta viewport, layout fixo em pixels, fontes pequenas.
**Por que é prejudicial:** 80%+ dos acessos a sites de comércio local são mobile. Site não mobile parece amador.
**Como evitar:** `<meta name="viewport" content="width=device-width, initial-scale=1.0">` é obrigatório.

### 12. Sem botão WhatsApp
**O que é:** Site sem link/botão para WhatsApp do negócio.
**Por que é prejudicial:** WhatsApp é o canal de conversão principal para comércio local no Brasil. Sem WhatsApp = sem conversão.
**Como evitar:** Botão flutuante + botão nas seções de CTA. Número real do negócio.

### 13. Design genérico (não adaptado ao nicho)
**O que é:** Usar o mesmo template visual para barbearia, clínica e restaurante.
**Por que é prejudicial:** O dono do negócio vê um site genérico e não se identifica. "Isso não é pra mim."
**Como evitar:** Adaptar cores, seções, CTAs e copy ao nicho específico de cada negócio.

### 14. Avaliações inventadas no site
**O que é:** Criar avaliações fictícias no HTML quando não foram coletadas avaliações reais suficientes.
**Por que é prejudicial:** Se o dono reconhecer que as avaliações são falsas, queima a credibilidade da agência.
**Como evitar:** Usar APENAS avaliações reais do briefing. Se não há avaliações, usar seção diferente (sobre o negócio, etc.).

---

## Anti-Patterns de Revisão

### 15. Aprovar sem verificar avaliações reais
**O que é:** Vera Veredito aprova o site sem verificar que as avaliações no HTML são literalmente as do briefing.
**Por que é prejudicial:** Se avaliações foram inventadas pelo Diego, o email que as menciona vai gerar desconfiança.
**Como evitar:** Comparação obrigatória HTML vs briefing.md para cada avaliação no site.

---

## Anti-Patterns de Envio

### 16. Atualizar contatados.md antes da confirmação do usuário
**O que é:** Eduardo Envio marca o negócio como contatado ao gerar o kit de envio.
**Por que é prejudicial:** Se o usuário nunca enviou, o negócio fica bloqueado por 30 dias sem motivo.
**Como evitar:** contatados.md só é atualizado após confirmação EXPLÍCITA do usuário de que enviou.
