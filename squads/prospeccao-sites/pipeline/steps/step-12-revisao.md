---
execution: inline
agent: vera-veredito
inputFile: squads/prospeccao-sites/output/{run_id}/emails.md
outputFile: squads/prospeccao-sites/output/{run_id}/revisao.md
on_reject: 9
---

# Step 12: Revisão de Qualidade

## Context Loading

Load these files before executing:
- `squads/prospeccao-sites/output/{run_id}/{slug-negocio}/site.html` — site de cada negócio
- `squads/prospeccao-sites/output/{run_id}/{slug-negocio}/email.md` — email de cada negócio
- `squads/prospeccao-sites/output/{run_id}/{slug-negocio}/briefing.md` — briefing de referência
- `squads/prospeccao-sites/agents/vera-veredito.agent.md` — persona e critérios da revisora
- `squads/prospeccao-sites/agents/vera-veredito/tasks/revisar.md` — processo de revisão
- `squads/prospeccao-sites/pipeline/data/quality-criteria.md` — critérios de qualidade

## Instructions

### Process
1. Para cada negócio com site + email aprovados no checkpoint 11:
   a. Executar o processo completo da tarefa `revisar.md`
   b. Comparar avaliações no HTML vs. avaliações no briefing (critério mais crítico)
   c. Verificar nome correto em ambos os artefatos
   d. Verificar todos os critérios do checklist
   e. Emitir veredicto APROVADO ou REJEITADO
2. Se REJEITADO:
   - Listar correções obrigatórias com agente responsável
   - Se site rejeitado: retornar ao step-09 (Diego Digital)
   - Se email rejeitado: retornar ao step-10 (Carlos Carta)
3. Verificar limite de 5 minutos
4. Salvar relatório completo em `output/{run_id}/revisao.md`

## Output Format

```markdown
# Revisão de Qualidade — [Data]

## Resultado Geral
| Negócio | Site | Email | Veredicto |
|---------|------|-------|----------|
| [Nome] | ✅/❌ | ✅/❌ | APROVADO/REJEITADO |
[...]

## Revisões Detalhadas

### [Nome do Negócio]
[Revisão completa conforme formato da tarefa revisar.md]
```

## Output Example

Ver `pipeline/data/output-examples.md` para exemplo completo de veredicto.

## Veto Conditions

Reject and redo if ANY are true:
1. Veredicto ausente para qualquer negócio revisado
2. Avaliações não foram comparadas com o briefing

## Quality Criteria

- [ ] Todos os negócios aprovados no checkpoint 11 revisados
- [ ] Comparação literal de avaliações realizada para cada negócio
- [ ] Veredicto explícito (APROVADO ou REJEITADO) para cada negócio
- [ ] Correções obrigatórias listadas em casos de rejeição
- [ ] Relatório salvo em `output/{run_id}/revisao.md`
