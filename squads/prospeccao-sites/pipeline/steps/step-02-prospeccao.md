---
execution: inline
agent: pablo-prospeccao
inputFile: squads/prospeccao-sites/output/{run_id}/cidade.md
outputFile: squads/prospeccao-sites/output/{run_id}/lista-negocios.md
---

# Step 02: Prospecção no Google Maps

## Context Loading

Load these files before executing:
- `squads/prospeccao-sites/output/{run_id}/cidade.md` — cidade informada pelo usuário no checkpoint 1
- `squads/prospeccao-sites/_memory/contatados.md` — lista de negócios já contatados (filtro 30 dias)
- `squads/prospeccao-sites/agents/pablo-prospeccao.agent.md` — persona e princípios do agente
- `squads/prospeccao-sites/agents/pablo-prospeccao/tasks/buscar-negocios.md` — processo detalhado de busca

## Instructions

### Process
1. Ler `contatados.md` e extrair negócios com data nos últimos 30 dias → lista de exclusão
2. Executar a tarefa `buscar-negocios.md` completa para a cidade informada
3. Verificar limite de 15 minutos: se atingir, avisar o usuário e perguntar se quer mais tempo
4. Salvar resultado em `squads/prospeccao-sites/output/{run_id}/lista-negocios.md`
5. Apresentar a lista de forma clara para o checkpoint seguinte

## Output Format

```markdown
# Lista de Negócios — [Cidade] — [Data]

## Negócio 1: [Nome]
- Segmento: [categoria]
- Endereço: [endereço completo]
- Telefone: [telefone com DDD]
- Email: [email] ou "Não encontrado"
- Nota Google: [X.X ⭐] ([N] avaliações)
- Site: Nenhum
- Fonte do email: [origem]

[... até Negócio 5]

---
Nota: [N] negócios encontrados. [N] filtrados por ter site. [N] filtrados por contatados.md.
```

## Output Example

```markdown
# Lista de Negócios — Campinas — 2026-05-17

## Negócio 1: Barbearia Premium do Zé
- Segmento: Barbearia
- Endereço: Rua das Flores, 142 — Centro — Campinas/SP
- Telefone: (19) 99812-3456
- Email: contato@barbeariadoze.com.br
- Nota Google: 4.8 ⭐ (127 avaliações)
- Site: Nenhum
- Fonte do email: Página do Facebook

## Negócio 2: Clínica Odontológica Sorriso Perfeito
- Segmento: Clínica odontológica
- Endereço: Rua Coronel Quirino, 215 — Campinas/SP
- Telefone: (19) 3523-1234
- Email: sorrisoperfeito.cps@gmail.com
- Nota Google: 4.9 ⭐ (68 avaliações)
- Site: Nenhum
- Fonte do email: Google Maps

[mais 3 negócios...]
```

## Veto Conditions

Reject and redo if ANY are true:
1. Algum negócio com site ativo incluído na lista
2. Algum negócio do contatados.md (últimos 30 dias) incluído

## Quality Criteria

- [ ] 5 negócios listados com campos obrigatórios preenchidos
- [ ] Nenhum negócio com site ativo
- [ ] Nenhum negócio dos últimos 30 dias do contatados.md
- [ ] Email coletado para pelo menos 3 dos 5 negócios
- [ ] Arquivo salvo em `output/{run_id}/lista-negocios.md`
