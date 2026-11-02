# Domain Framework — Pipeline de Prospecção e Venda de Sites

## Metodologia do Pipeline

### Fase 1: Descoberta e Qualificação (Passos 1-3)
**Objetivo:** Identificar 5 negócios locais sem site que são bons candidatos para comprar

**Processo:**
1. Receber a cidade-alvo do usuário
2. Buscar negócios no Google Maps usando Apify (diversificar nichos)
3. Filtrar: sem site + verificar contatados.md (excluir últimos 30 dias)
4. Coletar dados públicos de cada negócio
5. Apresentar a lista para aprovação do usuário

**Critério de sucesso:** 5 negócios com dados completos (nome, telefone, segmento, avaliações)

---

### Fase 2: Investigação Digital (Passo 4)
**Objetivo:** Coletar todo o conteúdo público disponível sobre cada negócio para personalização

**Processo:**
1. Para cada negócio: buscar em Facebook, Instagram, TripAdvisor, Restaurant Guru, Solutudo
2. Copiar avaliações reais literalmente (NUNCA parafrasear ou inventar)
3. Identificar identidade visual (cores, logo, estilo)
4. Mapear presença digital atual

**Critério de sucesso:** Dados suficientes para criar site e email personalizados

---

### Fase 3: Análise e Briefing (Passo 6)
**Objetivo:** Transformar dados brutos em briefing estruturado + score de prioridade

**Os 8 pontos do briefing:**
1. Identidade do negócio — quem são, o que fazem, diferencial aparente
2. Público-alvo — quem frequenta, inferido das avaliações e nicho
3. Produto/serviço — o que oferecem, destaques mencionados nas avaliações
4. Identidade visual existente — cores, logo, estilo identificado nas redes
5. Concorrência e posicionamento — como se posicionam no segmento local
6. Objetivo do site — o que o site precisa fazer (agendar, exibir cardápio, gerar leads)
7. Presença digital atual — resumo de tudo encontrado pelo Pesquisador
8. Conteúdo disponível — avaliações reais, fotos, textos coletados

**Critério de sucesso:** Todos os 8 pontos preenchidos, score calculado, todos os negócios apresentados

---

### Fase 4: Produção de Conteúdo (Passos 8-9)
**Objetivo:** Criar site HTML e email de proposta personalizados para cada negócio aprovado

**Site (Diego Digital):**
- HTML único autocontido
- Estrutura adaptada ao nicho
- Avaliações reais integradas
- WhatsApp funcional
- Mobile-first

**Email (Carlos Carta):**
- 60-100 palavras
- Elogio genuíno baseado em dado real
- Problema plantado específico ao nicho
- CTA de baixo compromisso

**Critério de sucesso:** Site funcional + email personalizado para cada negócio selecionado

---

### Fase 5: Revisão e Aprovação (Passos 11-12)
**Objetivo:** Garantir que os artefatos são precisos, personalizados e adequados para envio

**Checklist de revisão:**
- Avaliações no HTML são literalmente as do briefing?
- Nome do negócio correto em todos os artefatos?
- Email tem o formato e tamanho corretos?
- Site é mobile-responsive?
- Dados de contato (WhatsApp, endereço) são os reais?

**Critério de sucesso:** APROVADO pela Vera Veredito + aprovação final do usuário

---

### Fase 6: Preparação do Kit de Envio (Passo 13)
**Objetivo:** Gerar um kit de envio completo para o usuário enviar manualmente

**Processo:**
1. Gerar kit-envio.txt (texto puro) para cada negócio aprovado, na sequência de etapas informal (abertura → [aguarda] → contexto+permissão → [aguarda] → link + telas), com follow-up por etapa
2. Informar usuário para enviar manualmente (terça/quarta às 9h para email)
3. Aguardar confirmação do usuário
4. Atualizar contatados.md

**Critério de sucesso:** Kits gerados + contatados.md atualizado após confirmação

---

## Regras Transversais do Pipeline

### Regra da Autenticidade
Nenhum agente inventa dados. Avaliações são sempre reais e copiadas literalmente. Nomes são sempre verificados. O poder do email está na personalização real — inventar destrói a credibilidade.

### Regra dos Checkpoints
O usuário tem controle total. Nenhuma etapa passa sem aprovação. O pipeline para e espera em cada checkpoint.

### Regra do Limite de Tempo
Todo agente monitora seu próprio tempo. Ao atingir o limite, para, avisa, e pergunta: "Atingi meu limite de tempo. Quer me dar mais tempo ou sigo com o que tenho?"

### Regra da Memória
contatados.md é atualizado SOMENTE após confirmação explícita do usuário de que agendou o envio. Isso garante que nenhum negócio seja marcado como contatado sem realmente ter sido.

### Regra da Saída por Negócio
Cada negócio tem sua própria pasta em output/{run_id}/{slug-do-negocio}/:
- briefing.md — briefing completo dos 8 pontos
- site.html — site HTML autocontido
- email.md — email de proposta com assunto, corpo e notas
