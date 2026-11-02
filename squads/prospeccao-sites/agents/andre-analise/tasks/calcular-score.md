---
task: "Calcular Score de Prioridade"
order: 2
input:
  - briefings: Briefings completos de todos os negócios
  - lista_negocios: Lista original com dados do Google Maps
output:
  - scores: Tabela comparativa de scores com justificativa por critério
---

# Calcular Score de Prioridade

Calcula o score de prioridade (0-10) para cada negócio usando critérios objetivos. Apresenta TODOS os negócios ao usuário para que ele decida quais avançam.

## Process

1. **Para cada negócio, calcular cada critério**:

   **Avaliações Google (0-3 pontos):**
   - 1-10 avaliações = 1 ponto
   - 11-50 avaliações = 2 pontos
   - 51+ avaliações = 3 pontos
   - **Volume baixo = "não pontua neste item", NUNCA "reprovado".** Pontuação menor aqui (1 ou 2) é aceitável e não derruba o negócio. O negócio segue normalmente desde que tenha canal válido (WhatsApp/email) — quem reprova um negócio é a falta de contato, não a falta de volume. Ex.: Classe A com 18 avaliações recebe 2/3 neste critério e segue normalmente, apoiada nos outros sinais (nota alta, % de recomendação, canal válido).

   **Nota média Google (0-2 pontos):**
   - Abaixo de 3.0 estrelas = 0 pontos
   - 3.0 a 3.9 estrelas = 1 ponto
   - 4.0 ou mais = 2 pontos

   **Ausência de site (0-2 pontos):**
   - Tem site funcional = 0 pontos (não deveria estar na lista)
   - Site básico/precário/redirect para rede social = 1 ponto
   - Completamente sem site = 2 pontos

   **Presença ativa em redes sociais (0-2 pontos):**
   - Sem redes encontradas = 0 pontos
   - Redes encontradas mas inativas (último post há mais de 3 meses) = 1 ponto
   - Redes ativas (posts regulares) = 2 pontos

   **Ticket médio do nicho (0-1 ponto):**
   - Nicho de ticket alto (clínica, hotel, consultório, academia premium) = 1 ponto
   - Nicho de ticket médio/baixo (lanchonete, mercadinho, papelaria) = 0 pontos

   **Nota — texto de avaliação não afeta o score:** o critério Avaliações usa o VOLUME (número de avaliações), não o texto literal. Um negócio com 807 avaliações e sem texto acessível ainda recebe 3/3 em Avaliações. A falta de depoimentos textuais NUNCA reduz nem zera o score.

   **Nota — score baixo em um critério não reprova o negócio:** o score é indicativo de oportunidade, não um filtro de aprovação. Pontuar pouco em um item (volume baixo, sem redes, ticket baixo) é normal e aceitável — o negócio continua na lista e é apresentado ao usuário. O único filtro que reprova um negócio é a falta de canal válido (WhatsApp/email), aplicado antes do score no `criar-briefing.md`. Nenhum critério de score, isolado, descarta um negócio.

2. **Somar os pontos de cada critério** para obter o score total (0-10)

3. **Documentar justificativa por critério** para cada negócio

4. **Apresentar tabela comparativa** com TODOS os negócios

## Output Format

```markdown
# Scores de Prioridade — [Cidade] — [Data]

## Tabela Comparativa

| Negócio | Avaliações | Nota | Sem Site | Redes | Ticket | TOTAL |
|---------|-----------|------|----------|-------|--------|-------|
| [Nome] | X/3 | X/2 | X/2 | X/2 | X/1 | X/10 |
[...]

## Detalhamento por Negócio

### [Nome do Negócio] — Score: [N]/10
- Avaliações: [N] pts — [N avaliações encontradas]
- Nota: [N] pts — [nota] ⭐
- Sem site: [N] pts — [status]
- Redes ativas: [N] pts — [status das redes]
- Ticket: [N] pts — [justificativa]

[...]

---
⚠️ Todos os negócios acima estão disponíveis para avançar. O score é indicativo de oportunidade — a decisão final é sua.
```

## Output Example

```markdown
# Scores de Prioridade — Campinas — 2026-05-17

## Tabela Comparativa

| Negócio | Avaliações | Nota | Sem Site | Redes | Ticket | TOTAL |
|---------|-----------|------|----------|-------|--------|-------|
| Barbearia Premium do Zé | 3/3 | 2/2 | 2/2 | 2/2 | 0/1 | **9/10** |
| Clínica Odontológica Sorriso Perfeito | 2/3 | 2/2 | 2/2 | 1/2 | 1/1 | **8/10** |
| Pet Shop Quatro Patas | 2/3 | 2/2 | 2/2 | 2/2 | 0/1 | **8/10** |
| Restaurante Sabor da Vila | 2/3 | 2/2 | 2/2 | 0/2 | 0/1 | **6/10** |
| Academia Arte Marcial Centro | 1/3 | 2/2 | 2/2 | 1/2 | 1/1 | **7/10** |

## Detalhamento por Negócio

### Barbearia Premium do Zé — Score: 9/10
- Avaliações: 3/3 pts — 127 avaliações (51+)
- Nota: 2/2 pts — 4.8 ⭐ (4.0+)
- Sem site: 2/2 pts — Completamente sem site
- Redes ativas: 2/2 pts — Instagram ativo (3 posts/semana) + Facebook ativo
- Ticket: 0/1 pts — Barbearia, ticket médio

### Clínica Odontológica Sorriso Perfeito — Score: 8/10
- Avaliações: 2/3 pts — 68 avaliações (11-50)
- Nota: 2/2 pts — 4.9 ⭐ (4.0+)
- Sem site: 2/2 pts — Completamente sem site
- Redes ativas: 1/2 pts — Instagram encontrado mas inativo (último post há 4 meses)
- Ticket: 1/1 pts — Clínica odontológica, ticket alto

---
⚠️ Todos os 5 negócios acima estão disponíveis para avançar. O score é indicativo de oportunidade — a decisão final é sua. Quais você quer levar para a criação do site e email?
```

## Quality Criteria

- [ ] Todos os 5 critérios calculados para cada negócio
- [ ] Justificativa por critério documentada
- [ ] Tabela comparativa apresentada com todos os negócios
- [ ] Score total correto (soma dos critérios)
- [ ] Mensagem final deixa claro que a decisão é do usuário

## Veto Conditions

Reject and redo if ANY are true:
1. Score calculado errado (verificar: avaliações + nota + sem site + redes + ticket = total)
2. Algum negócio omitido da tabela comparativa
