---
task: "Criar Briefing de 8 Pontos"
order: 1
input:
  - investigacao: Documento de investigação digital do Roberto Rastro
  - lista_negocios: Lista original com dados do Google Maps do Pablo Prospecção
output:
  - briefing: Briefing estruturado com os 8 pontos para cada negócio
---

# Criar Briefing de 8 Pontos

Transforma os dados brutos da investigação em briefings estruturados e acionáveis para cada negócio.

## Process

0. **Filtro WhatsApp/email — BLOQUEANTE** — Antes de criar o briefing:
   a. Verificar se Roberto encontrou WhatsApp público OU email público. Telefone fixo sozinho NÃO basta e DM de Instagram/Facebook NÃO conta — negócio sem WhatsApp/email não avança.
   b. Verificar que Roberto consultou as 14 fontes (não menos)
   c. Se Roberto listou menos de 14 fontes e não encontrou contato → **devolver a Roberto para continuar busca**
   d. Se Roberto esgotou 14 fontes e não encontrou contato → registrar em `squads/prospeccao-sites/_memory/descartados.md`:
      ```markdown
      | [Nome] | [Cidade] | [Data] | sem contato direto após 14 fontes | [lista das 14 fontes e resultados] |
      ```
      Não criar briefing. Não avançar. Não registrar em contatados.md.
   e. Apenas negócios com contato direto confirmado prosseguem para os 8 pontos abaixo.

1. **Para cada negócio aprovado no filtro, preencher os 8 pontos**:

   **Ponto 1 — Identidade do Negócio**
   Síntese de quem são: nome completo, tipo de negócio, tempo de existência (se inferível), diferencial aparente com base nas avaliações e nas redes sociais.

   **Ponto 2 — Público-Alvo**
   Quem frequenta o negócio, inferido das avaliações (vocabulário, contexto, tipo de comentário) e do nicho. Indicar se confirmado ou inferido.

   **Ponto 3 — Produto/Serviço**
   O que oferecem: produtos/serviços principais, preços (se identificados nas redes), destaques mencionados repetidamente nas avaliações.

   **Ponto 4 — Identidade Visual Existente**
   Cores, logo, fontes, estilo visual — conforme identificado na investigação. Se não identificado, registrar como "Identidade visual não identificada nas plataformas encontradas."

   **Ponto 5 — Concorrência e Posicionamento**
   Como o negócio se posiciona no segmento local. Se houver dados de concorrentes (mencionados em avaliações, localização próxima), incluir.

   **Ponto 6 — Objetivo do Site**
   O que o site precisa fazer para ESTE negócio específico. Inferir do nicho e das avaliações: agendamento online? exibir cardápio? captar leads? gerar confiança para novos clientes?

   **Ponto 7 — Presença Digital Atual**
   Resumo do status em cada plataforma investigada: ativo/inativo/não encontrado + qualidade da presença.

   **Ponto 8 — Conteúdo Disponível**
   Se Roberto coletou texto: avaliações reais copiadas literalmente (copiar do documento do Roberto). Se Roberto marcou ℹ️ SEM TEXTO: registrar a prova social agregada (nota + volume + nomes de avaliadores recentes, se houver) — NUNCA inventar texto. Texto é bônus; a ausência dele não reduz o score nem impede o briefing. Incluir também fotos identificadas e textos das redes que podem ser aproveitados.

2. **Salvar briefing individual por negócio** em `output/{run_id}/{slug-negocio}/briefing.md`

3. **Compilar todos os briefings** no arquivo central `output/{run_id}/briefings.md`

## Output Format

```markdown
# Briefing — [Nome do Negócio]

## 1. Identidade do Negócio
[síntese]

## 2. Público-Alvo
[descrição com indicação: confirmado / inferido das avaliações]

## 3. Produto/Serviço
[lista de serviços/produtos com detalhes]

## 4. Identidade Visual Existente
[cores, logo, estilo ou "não identificada"]

## 5. Concorrência e Posicionamento
[posicionamento no segmento local]

## 6. Objetivo do Site
[o que o site precisa fazer para este negócio]

## 7. Presença Digital Atual
[resumo por plataforma]

## 8. Conteúdo Disponível
### Avaliações Reais
"[avaliação literal]" — [autor], [data]
[...]

### Fotos e Outros Conteúdos
[descrição do que está disponível]
```

## Output Example

```markdown
# Briefing — Barbearia Premium do Zé

## 1. Identidade do Negócio
Barbearia masculina premium no centro de Campinas. Foco em cortes modernos e barba. Destaque pelo atendimento personalizado — o proprietário conhece cada cliente pelo nome (mencionado em múltiplas avaliações). Posicionamento premium: não compete em preço.

## 2. Público-Alvo
Homens de 25-45 anos, profissionais com renda média-alta que valorizam qualidade e experiência acima de preço. (Inferido das avaliações: vocabulário formal, menção a "pontualidade", "profissionalismo", clientela fiel.)

## 3. Produto/Serviço
- Corte masculino (R$55 — identificado em avaliação)
- Barba completa (R$40)
- Combo corte + barba (R$80)
- Ambiente: café na chegada mencionado em avaliação

## 4. Identidade Visual Existente
Cores: marrom escuro e dourado/bege. Estilo premium e masculino com referências clássicas. Logo: tesoura estilizada em dourado. Tipografia bold moderna. Fotos profissionais dos cortes.

## 5. Concorrência e Posicionamento
3 barbearias identificadas no mesmo bairro (verificado no Maps). Zé tem 127 avaliações vs. 34 e 22 dos concorrentes principais. Posicionado como opção premium da região.

## 6. Objetivo do Site
Exibir serviços com preços para novos clientes, mostrar avaliações como prova social, gerar agendamentos via WhatsApp. Site de conversão direta.

## 7. Presença Digital Atual
- Google Maps: ativo, 4.8⭐ (127 avaliações)
- Facebook: ativo (2 posts/mês), 430 curtidas
- Instagram: ativo (3 posts/semana), 1.240 seguidores
- TripAdvisor: não encontrado
- Solutudo: não encontrado

## 8. Conteúdo Disponível
### Avaliações Reais
"Melhor barbearia de Campinas. O Zé conhece cada cliente pelo nome e lembra do corte preferido." — Carlos M., 2026-03-15

"Ambiente incrível, café na chegada e saio sempre perfeito. Não troco por nada. Recomendo!" — Rafael T., 2026-02-28

"Pontual e profissional. Nunca precisei esperar mais de 5 minutos. Preço justo pelo que entrega." — Lucas A., 2026-01-10

"Fui pela primeira vez sem indicação, só pelas avaliações. Não me arrependi. Já é minha barbearia definitiva." — Mateus B., 2025-12-05

### Fotos e Outros Conteúdos
Fotos profissionais dos cortes (Instagram, alta qualidade)
Fotos do ambiente interno e dos profissionais (Facebook)
Logo em dourado disponível no Instagram
```

## Quality Criteria

- [ ] Todos os 8 pontos preenchidos para cada negócio
- [ ] Avaliações copiadas literalmente no ponto 8 (idênticas ao documento do Roberto)
- [ ] Dados confirmados vs. inferidos indicados explicitamente
- [ ] Briefing individual salvo por negócio + compilado no briefings.md central

## Veto Conditions

Reject and redo if ANY are true:
1. Briefing criado para negócio sem WhatsApp/email verificado (telefone fixo sozinho não qualifica)
2. REPROVADO aceito sem Roberto ter consultado as 14 fontes
3. Negócio reprovado registrado em contatados.md (deve ir só para descartados.md)
4. Algum dos 8 pontos ausente sem justificativa
5. Avaliações no ponto 8 diferentes (parafraseadas) das avaliações no documento do Roberto
