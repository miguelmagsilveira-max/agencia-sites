---
execution: inline
agent: eduardo-envio
inputFile: squads/prospeccao-sites/output/{run_id}/revisao.md
outputFile: squads/prospeccao-sites/output/{run_id}/{slug-negocio}/kit-envio.txt
---

# Step 14: Preparar Kit de Envio

## Context Loading

Load these files before executing:
- `squads/prospeccao-sites/output/{run_id}/{slug-negocio}/email.md` — email de cada negócio aprovado
- `squads/prospeccao-sites/output/{run_id}/{slug-negocio}/link-ao-vivo.txt` — URL pública do site (deploy do Diego)
- `squads/prospeccao-sites/output/{run_id}/revisao.md` — lista dos negócios aprovados pela Vera
- `squads/prospeccao-sites/agents/eduardo-envio.agent.md` — persona e regras do agente de envio
- `squads/prospeccao-sites/agents/eduardo-envio/tasks/gerar-kit-envio.md` — processo de geração do kit
- `squads/prospeccao-sites/_memory/contatados.md` — para atualização após confirmação

## Instructions

### Process
1. Para cada negócio aprovado no checkpoint 13:
   a. Verificar os screenshots em `screenshots/` (mínimo `01-hero.png`) — se faltar, PAUSAR e avisar
   b. Ler o `email.md` para obter destinatário e o conteúdo aprovado (nota, dor, elementos do site, link)
   c. Ler o `link-ao-vivo.txt` para obter a URL pública do site — se faltar, PAUSAR e avisar
   d. Determinar o canal de entrega (WhatsApp / email / DM Instagram / presencial) com destino exato
   e. Gerar `kit-envio.txt` (texto puro) na sequência de etapas informal — ETAPA 1 → [AGUARDE] → ETAPA 3 → [AGUARDE] → ETAPA 5 — montada a partir do conteúdo aprovado (sem inventar), com um follow-up por etapa, link ao vivo e caminhos dos screenshots na ETAPA 5, horário sugerido. Ver `gerar-kit-envio.md`
2. Apresentar ao usuário os kits gerados, com canal e destino de cada um, e as instruções de envio manual
3. AGUARDAR confirmação do usuário de que enviou (Eduardo NÃO envia nada por conta própria)
4. Após confirmação: atualizar `contatados.md` para cada negócio enviado (status "enviado")
5. Verificar limite de 2 minutos

## Output Format

```markdown
# Kits de Envio — [Data]

## Kits Gerados
| Negócio | Canal | Destino | Status |
|---------|-------|---------|--------|
| [Nome] | [Email/WhatsApp/DM/Presencial] | [destino exato] | ✅ Kit gerado |
[...]

## Instruções de Envio Manual
[instruções por canal]

⏳ Confirme quando enviar para eu registrar no histórico.
```

## Output Example

Ver tarefa `gerar-kit-envio.md` para exemplo completo do kit.

## Veto Conditions

Reject and redo if ANY are true:
1. contatados.md atualizado antes da confirmação do usuário
2. Kit gerado como `.md` / com markdown pesado, ou como mensagem única no formato longo por padrão (default é `.txt` em sequência de etapas; email longo é legado para canal e-mail)
3. Fato/dado/promessa inventado nas etapas (deve reorganizar o conteúdo aprovado do email.md, sem criar nada novo)
4. Kit gerado sem screenshots — se `01-hero.png` não existir, parar e alertar
5. Kit gerado sem o link ao vivo — se `link-ao-vivo.txt` não existir, parar e alertar
6. Eduardo enviou, agendou ou criou rascunho por conta própria — o envio é 100% manual

## Quality Criteria

- [ ] kit-envio.txt (texto puro) gerado para cada negócio aprovado
- [ ] Kit na sequência de etapas informal (ETAPA 1 → [AGUARDE] → ETAPA 3 → [AGUARDE] → ETAPA 5), sem markdown pesado
- [ ] Etapas reorganizam o conteúdo do email.md aprovado, sem inventar fato/dado
- [ ] Link ao vivo e caminhos dos screenshots incluídos na ETAPA 5
- [ ] Um follow-up por etapa incluído
- [ ] Instruções de envio manual apresentadas
- [ ] contatados.md atualizado SOMENTE após confirmação
