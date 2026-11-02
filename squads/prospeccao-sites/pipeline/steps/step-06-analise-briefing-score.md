---
execution: inline
agent: andre-analise
inputFile: squads/prospeccao-sites/output/{run_id}/investigacao.md
outputFile: squads/prospeccao-sites/output/{run_id}/briefings.md
---

# Step 06: Análise — Briefing e Score

## Context Loading

Load these files before executing:
- `squads/prospeccao-sites/output/{run_id}/investigacao.md` — dados da investigação do Roberto Rastro
- `squads/prospeccao-sites/output/{run_id}/lista-negocios.md` — dados originais do Pablo (notas, avaliações)
- `squads/prospeccao-sites/agents/andre-analise.agent.md` — persona e princípios do analista
- `squads/prospeccao-sites/agents/andre-analise/tasks/criar-briefing.md` — processo de criação do briefing
- `squads/prospeccao-sites/agents/andre-analise/tasks/calcular-score.md` — processo de cálculo do score
- `squads/prospeccao-sites/pipeline/data/domain-framework.md` — framework dos 8 pontos

## Instructions

### Process
1. Executar a tarefa `criar-briefing.md` para cada negócio (preencher os 8 pontos)
2. Executar a tarefa `calcular-score.md` para cada negócio (calcular score 0-10)
3. Salvar briefing individual em `output/{run_id}/{slug-negocio}/briefing.md` para cada negócio
4. Compilar todos os briefings + scores em `output/{run_id}/briefings.md`
5. Verificar limite de 5 minutos: se atingir, avisar e perguntar
6. Apresentar tabela comparativa de scores para decisão do usuário

## Output Format

```markdown
# Briefings e Scores — [Cidade] — [Data]

## Tabela Comparativa de Scores

| Negócio | Avaliações | Nota | Sem Site | Redes | Ticket | TOTAL |
|---------|-----------|------|----------|-------|--------|-------|
[...]

## Briefings Completos

### [Nome Negócio 1] — Score: [N]/10
[Briefing completo com 8 pontos]

[...]
```

## Output Example

Ver `pipeline/data/output-examples.md` para exemplo completo de briefing.

## Veto Conditions

Reject and redo if ANY are true:
1. Algum dos 8 pontos ausente em algum briefing
2. Score calculado incorretamente (verificar a soma dos critérios)
3. Algum negócio omitido da tabela comparativa

## Quality Criteria

- [ ] Briefings com 8 pontos para todos os negócios
- [ ] Scores com justificativa para todos os negócios
- [ ] Tabela comparativa apresentada
- [ ] Avaliações reais no ponto 8 de cada briefing
- [ ] Briefings individuais salvos por negócio
- [ ] Compilação salva em `output/{run_id}/briefings.md`
