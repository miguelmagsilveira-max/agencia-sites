# Research Brief — Prospecção de Sites para Comércio Local

## Domínio 1: Cold Email B2B para Venda de Sites

### Framework Central Validado
**Observação → Problema Plantado → Solução Pronta → Pergunta Aberta**

O objetivo do primeiro email NÃO é fechar venda — é iniciar uma conversa.
Conversas começam com perguntas, não com pitches.

### Estrutura de Email Validada (60-100 palavras)
```
Assunto: [4-7 palavras referenciando o negócio ou cidade]

[Nome ou "Olá [nome do negócio]"],

[Elogio genuíno baseado em dado real — avaliação, produto, destaque]

[Planta o problema: o que eles estão perdendo SEM site, específico ao nicho]

[Mostra solução pronta: "Criei uma versão do site para vocês"]

[CTA de baixo compromisso: "Posso te mandar?"]

[Nome + Agência de Sites]
```

### Dados de Performance (fontes pesquisadas)
- Emails de 60-100 palavras com personalização real: 10-15% de taxa de resposta
- Templates genéricos: 1-3% de taxa de resposta
- 80% das conversões ocorrem no 2º ao 4º contato (follow-up é obrigatório)
- Melhores horários: terça/quarta/quinta entre 9h-11h30
- Assunto ideal: 3-5 palavras, sem caixa alta, sem emoji

### Estratégia "Mostrar Trabalho Pronto"
Criar o site antes do contato e mencioná-lo no email.
"Criei uma versão do site para vocês" > "Ofereço serviço de criação de sites"
Reduz barreira de imaginação. O cliente vê, não imagina.

### Personalização por Nicho no Problema Plantado
- Restaurante/Bar: "Quem busca 'restaurante em [cidade]' no Google não te encontra"
- Salão/Barbearia: "Clientes novos não conseguem agendar sem te ligar"
- Clínica: "Pacientes que buscam online escolhem o concorrente com site"
- Loja: "Sem site, você não aparece no Google Maps com destaque"
- Academia: "Alunos em potencial não conseguem ver seus horários e modalidades"

---

## Domínio 2: Prospecção no Google Maps

### Metodologia de Coleta
1. Google Maps é fonte primária — dados frequentemente atualizados pelo próprio negócio
2. WhatsApp presente em 99% dos perfis (segundo Qualifiquei.com.br)
3. Email: buscar em Facebook/Instagram/Solutudo quando não está no Maps
4. Dados prioritários: nome exato, telefone com DDD, email, nota, nº avaliações, endereço, categoria

### Nichos de Alta Prioridade (ticket médio e motivação digital)
1. Clínicas médicas e odontológicas — credibilidade digital = mais pacientes
2. Hotéis e pousadas — reservas online são padrão do setor
3. Restaurantes temáticos — cardápio digital é demanda crescente
4. Salões de beleza premium — agendamento online reduz ligações perdidas
5. Pet shops e clínicas veterinárias — donos de pets são nativos digitais
6. Academias de dança e artes marciais — informação de turmas é crítica

### Sistema de Score (validado por pesquisa)
| Critério | Pontuação |
|---|---|
| 1-10 avaliações Google | 1 ponto |
| 11-50 avaliações Google | 2 pontos |
| 51+ avaliações Google | 3 pontos |
| Nota 3.0-3.9 estrelas | 1 ponto |
| Nota 4.0+ estrelas | 2 pontos |
| Site básico/ruim | 1 ponto |
| Sem site | 2 pontos |
| Redes sociais ativas | 2 pontos |
| Nicho de ticket alto | 1 ponto |
| **MÁXIMO** | **10 pontos** |

---

## Domínio 3: Design de Sites para Comércio Local

### Estrutura Universal Validada
```
1. Hero Section
   - Foto principal do negócio (high quality)
   - Headline: "[Diferencial] em [Cidade]"
   - Sub: prova social ("Mais de 500 avaliações 5⭐ no Google")
   - CTA primário: botão WhatsApp ou ação principal

2. Diferenciais (3 colunas: ícone + título + 1 frase)

3. Produtos/Serviços em Destaque (grid com fotos + nomes)

4. Avaliações Google (3-5 citações literais com nome do avaliador)

5. Sobre o Negócio (foto + história curta, tom pessoal)

6. Contato
   - Google Maps iframe
   - Telefone clicável (tel:)
   - Horários de funcionamento
   - Endereço completo

Footer + WhatsApp flutuante (botão fixo, sempre visível)
```

### Adaptações por Nicho
| Nicho | Seção Especial | CTA Principal |
|---|---|---|
| Restaurante/Bar | Cardápio com fotos dos pratos | "Ver cardápio" / "Fazer pedido" |
| Salão/Barbearia | Galeria antes/depois + lista de serviços com preço | "Agendar agora" |
| Clínica/Consultório | Credenciais do profissional (foto, formação, CRM/CRO) | "Agendar consulta" |
| Loja/Comércio | Produtos em destaque com preço | "Falar no WhatsApp" |
| Pet Shop | Serviços + preços + galeria de pets atendidos | "Agendar banho/tosa" |
| Academia | Modalidades + grade horária + fotos das aulas | "Conhecer planos" |

### Elementos Técnicos Obrigatórios
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- Botão WhatsApp: `<a href="https://wa.me/55{DDD}{NUMERO}">`
- Maps embed: `<iframe src="https://maps.google.com/maps?q=...">`
- Google Fonts via CDN (Inter, Poppins ou Roboto)
- Schema.org LocalBusiness markup
- CSS em `<style>` interno (HTML autocontido, arquivo único)
