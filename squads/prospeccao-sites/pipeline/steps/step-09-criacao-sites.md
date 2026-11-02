---
execution: inline
agent: diego-digital
inputFile: squads/prospeccao-sites/output/{run_id}/briefings.md
outputFile: squads/prospeccao-sites/output/{run_id}/sites-criados.md
---

# Step 09: Criação de Sites HTML

## Context Loading

Load these files before executing:
- `squads/prospeccao-sites/output/{run_id}/briefings.md` — briefings completos dos negócios selecionados
- `squads/prospeccao-sites/agents/diego-digital.agent.md` — persona e princípios do designer
- `squads/prospeccao-sites/agents/diego-digital/tasks/criar-site-html.md` — processo completo de criação
- `squads/prospeccao-sites/pipeline/data/research-brief.md` — estruturas validadas por nicho

## Instructions

### Process
1. Ler a lista de negócios selecionados no checkpoint 7
2. Para CADA negócio selecionado, executar `criar-site-html.md` completo:
   a. Ler o briefing específico do negócio
   b. **Verificar `output/{run_id}/{slug-negocio}/imagens-insta/`** — se o usuário baixou fotos reais do Instagram no checkpoint 8, usar essas fotos no site (Diego decide a distribuição: hero, galeria, cards). Se a pasta estiver vazia ou não existir, buscar imagens na API oficial da Unsplash (Step 4 da tarefa).
   c. Decidir estrutura baseada no nicho
   d. Definir paleta de cores pela identidade visual
   e. Criar HTML completo e autocontido
   f. Salvar em `output/{run_id}/{slug-negocio}/site.html`
3. Verificar limite de 15 minutos TOTAL para todos os sites:
   - Se atingir no meio de um site: completar o site atual antes de parar
   - Avisar usuário: "Atingi 15 minutos. Criei sites para [N] negócios. Quer mais tempo para os restantes?"
4. Registrar resumo em `output/{run_id}/sites-criados.md`

## Output Format

```markdown
# Sites Criados — [Data]

## Sites Gerados

| Negócio | Arquivo | Nicho | Avaliações incluídas | WhatsApp |
|---------|---------|-------|---------------------|---------|
| [Nome] | output/{run_id}/{slug}/site.html | [nicho] | [N] avaliações reais | ✅ |
[...]

## Resumo de Decisões de Design

### [Nome do Negócio]
- Estrutura escolhida: [seções] — Motivo: [nicho específico]
- Cores: [cores usadas] — Fonte: [identidade visual do Instagram]
- Avaliações incluídas: [N] (todas reais do briefing)
- CTA principal: "[texto do botão]"
```

## Output Example

```markdown
# Sites Criados — 2026-05-17

## Sites Gerados

| Negócio | Arquivo | Nicho | Avaliações | WhatsApp |
|---------|---------|-------|-----------|---------|
| Barbearia do Zé | output/.../barbearia-do-ze/site.html | Barbearia | 4 reais | ✅ |
| Clínica Sorriso | output/.../clinica-sorriso/site.html | Clínica | 3 reais | ✅ |

## Resumo de Decisões de Design

### Barbearia Premium do Zé
- Estrutura: Hero + Serviços (preços) + Avaliações + Sobre + Mapa
- Cores: marrom escuro (#4a2c17) + dourado (#c9a84c) — extraído do Instagram
- 4 avaliações reais do briefing incluídas literalmente
- CTA principal: "Agendar pelo WhatsApp"
```

## Veto Conditions

Reject and redo if ANY are true:
1. Site sem `<meta viewport>` (quebra mobile)
2. Site com avaliações diferentes das do briefing
3. Site sem botão WhatsApp flutuante

## Quality Criteria

- [ ] Um site criado para cada negócio selecionado
- [ ] HTML autocontido (sem CSS externo)
- [ ] Meta viewport em todos os sites
- [ ] Avaliações reais do briefing em todos os sites
- [ ] Botão WhatsApp flutuante em todos os sites
- [ ] Arquivos salvos nos caminhos corretos
- [ ] Resumo salvo em `output/{run_id}/sites-criados.md`
