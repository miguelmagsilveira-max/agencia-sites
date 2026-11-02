---
execution: inline
agent: roberto-rastro
inputFile: squads/prospeccao-sites/output/{run_id}/lista-negocios.md
outputFile: squads/prospeccao-sites/output/{run_id}/investigacao.md
---

# Step 04: Investigação Digital Profunda

## Context Loading

Load these files before executing:
- `squads/prospeccao-sites/output/{run_id}/lista-negocios.md` — lista aprovada pelo usuário no checkpoint 3
- `squads/prospeccao-sites/agents/roberto-rastro.agent.md` — persona e princípios do investigador
- `squads/prospeccao-sites/agents/roberto-rastro/tasks/investigar-digital.md` — processo detalhado de investigação

## Instructions

### Process
1. Para cada negócio da lista aprovada, executar o processo completo de investigação da tarefa `investigar-digital.md`
2. Verificar limite de 10 minutos: se atingir, avisar o usuário com o status atual e perguntar se quer mais tempo
3. Salvar todos os resultados em `squads/prospeccao-sites/output/{run_id}/investigacao.md`
4. Apresentar resumo das plataformas encontradas por negócio

## Output Format

```markdown
# Investigação Digital — [Cidade] — [Data]

## [Nome do Negócio 1]
[Relatório completo conforme formato da tarefa investigar-digital.md]

## [Nome do Negócio 2]
[...]

[... para todos os negócios]
```

## Output Example

```markdown
# Investigação Digital — Campinas — 2026-05-17

## Barbearia Premium do Zé

### Status por Plataforma
| Plataforma | Status | URL |
|---|---|---|
| Google Maps | Ativo | maps.google.com/...barbearia-do-ze |
| Facebook | Ativo | facebook.com/barbeariadoze |
| Instagram | Ativo | @barbearia_do_ze |
| TripAdvisor | Não encontrado | - |
| Restaurant Guru | N/A | - |
| Solutudo | Não encontrado | - |

### Avaliações Reais Coletadas
"Melhor barbearia de Campinas. O Zé conhece cada cliente pelo nome e lembra do corte preferido." — Carlos M., 2026-03-15 — Google Maps

[...]
```

## Veto Conditions

Reject and redo if ANY are true:
1. Avaliações parafraseadas ou sem aspas (devem ser texto literal)
2. Plataformas não investigadas sem registro de "Não encontrado"

## Quality Criteria

- [ ] Todos os negócios investigados nas 6 plataformas do checklist
- [ ] Avaliações copiadas literalmente com aspas
- [ ] Status de cada plataforma registrado para cada negócio
- [ ] Identidade visual descrita para cada negócio
- [ ] Arquivo salvo em `output/{run_id}/investigacao.md`
