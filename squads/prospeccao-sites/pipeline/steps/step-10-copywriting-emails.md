---
execution: inline
agent: carlos-carta
inputFile: squads/prospeccao-sites/output/{run_id}/briefings.md
outputFile: squads/prospeccao-sites/output/{run_id}/emails.md
---

# Step 10: Copywriting — Emails de Proposta

## Context Loading

Load these files before executing:
- `squads/prospeccao-sites/output/{run_id}/briefings.md` — briefings completos com avaliações reais
- `squads/prospeccao-sites/agents/carlos-carta.agent.md` — persona e princípios do copywriter
- `squads/prospeccao-sites/agents/carlos-carta/tasks/escrever-email.md` — processo de criação do email
- `squads/prospeccao-sites/pipeline/data/tone-of-voice.md` — tons disponíveis para seleção
- `squads/prospeccao-sites/pipeline/data/anti-patterns.md` — erros a evitar

## Instructions

### Process
1. Para CADA negócio selecionado no checkpoint 7:
   a. Ler o briefing específico (focar nas avaliações reais e no nicho)
   b. Escrever no **tom padrão informal/humano** (rodada 4), na estrutura de 9 blocos do gold standard — o conteúdo que o Eduardo vai reorganizar na sequência de etapas (Blocos 1-2 → ETAPA 1; 4-5-8 → ETAPA 3; 6-7 → ETAPA 5)
   c. Executar `escrever-email.md` completo
   d. Verificar contagem de palavras do corpo (180-240, conforme o agente do Carlos)
   e. Salvar em `output/{run_id}/{slug-negocio}/email.md`
2. Verificar limite de 5 minutos TOTAL para todos os emails
3. Registrar resumo em `output/{run_id}/emails.md`

## Output Format

```markdown
# Emails de Proposta — [Data]

## Emails Criados

| Negócio | Tom | Palavras | Email disponível | Arquivo |
|---------|-----|---------|-----------------|---------|
| [Nome] | Tom [N] | [N] palavras | ✅/⚠️ | output/.../email.md |
[...]

---
[Conteúdo completo de cada email, conforme formato da tarefa escrever-email.md]
```

## Output Example

Ver o formato completo do conteúdo (9 blocos, tom informal, assinatura do Miguel) em `escrever-email.md`. Exemplo real recente: `output/2026-09-13-rodada4/blue-house/email.md`.

## Veto Conditions

Ver os vetos completos em `escrever-email.md` (gold standard). Resumo:
1. Corpo fora de 180-240 palavras (rejeita abaixo de 150 ou acima de 260)
2. Fecho não é pergunta fechada de permissão (sim/não), ou usa pergunta aberta / decisão de compra / tom de vendedor
3. Elogio não baseado em dado real do briefing (ou recitado sem interpretar)
4. Assinatura não é "Abraço, / Miguel Magalhães Silveira / 12974062797"
5. Tom formal/corporativo em vez do informal/humano padrão (rodada 4)

## Quality Criteria

- [ ] Um email por negócio selecionado
- [ ] Tom informal/humano padrão (rodada 4), 9 blocos que quebram limpo nas etapas do Eduardo
- [ ] 180-240 palavras no corpo
- [ ] Elogio com dado real verificável, interpretado (não recitado)
- [ ] Fecho em pergunta fechada de permissão
- [ ] Assunto curto, sem caixa alta, sem dois pontos provocativos
- [ ] Assinatura "Abraço, / Miguel Magalhães Silveira / 12974062797"
- [ ] Arquivos salvos nos caminhos corretos
