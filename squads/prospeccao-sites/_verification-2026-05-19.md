# Verificação de Conformidade — Squad Prospecção Sites
**Data:** 2026-05-19 (sessão), gerado 2026-05-20
**Verificado por:** Claude Code (inspeção direta de todos os arquivos .agent.md e tasks/)

---

## PABLO PROSPECÇÃO

### Status: ✅ Corrigido
| Regra | Status | Ação |
|-------|--------|------|
| Busca 5 negócios via Google Maps | ✅ OK | — |
| Prioriza negócios sem site | ✅ OK | — |
| Busca além de 5 se descartes forem altos | ❌ → ✅ | Adicionado como Princípio 5 |
| Consulta contatados.md (bloqueio 30 dias) | ✅ OK | — |
| NÃO bloqueia por descartados.md | ❌ → ✅ | Adicionado como Princípio 4 |

---

## ROBERTO RASTRO

### Status: ✅ OK
| Regra | Status | Ação |
|-------|--------|------|
| NUNCA desistir antes de 14 fontes | ✅ OK | Adicionado nesta sessão |
| 14 fontes listadas em ordem | ✅ OK | Adicionado nesta sessão |
| Registra resultado de cada fonte | ✅ OK | Adicionado nesta sessão |
| 3 avaliações textuais reais (ou exceção) | ✅ OK | Princípio original |
| Coleta: telefone, email, horário, endereço, dono | ✅ OK | Princípio 3 + task Fase 3 |
| NUNCA inventa dados | ✅ OK | Anti-Pattern original |

---

## ANDRÉ ANÁLISE

### Status: ✅ OK
| Regra | Status | Ação |
|-------|--------|------|
| Critério bloqueante: email/telefone/WhatsApp público | ✅ OK | Adicionado nesta sessão |
| Instagram DM / formulários não contam | ✅ OK | Adicionado nesta sessão |
| Verifica 14 fontes antes de aceitar REPROVADO | ✅ OK | Adicionado nesta sessão |
| Reprovados → descartados.md (nunca contatados.md) | ✅ OK | Adicionado nesta sessão |
| Reprovados sem bloqueio de 30 dias | ✅ OK | Adicionado nesta sessão |
| Score 0-10 + briefing 8 pontos para aprovados | ✅ OK | Princípio original + task calcular-score.md |
| Usuário decide ordem de execução | ✅ OK | Coberto pelo checkpoint pipeline |

---

## DIEGO DIGITAL

### Status: ✅ Corrigido
| Regra | Status | Ação |
|-------|--------|------|
| Tipografia por nicho (tabela completa) | ✅ OK | Princípio 2 + task Step 2 |
| NUNCA Poppins | ✅ OK | Anti-Pattern 1 |
| Unsplash sintaxe source.unsplash.com/?keywords | ❌ → ✅ | Adicionado em Princípio 1 + task Step 4 reescrito |
| onerror fallback para Picsum em toda `<img>` | ❌ → ✅ | Adicionado em Princípio 1 + task Step 4 + Anti-Patterns 16-17 |
| Mínimo 5 imagens distintas (sem reuso) | ❌ → ✅ | Explicitado em Princípio 1 + task Step 4 |
| Paleta 3 cores + 2 neutras | ✅ OK | Princípio 5 |
| 8-10 seções obrigatórias | ✅ OK | Princípio 4 + task Step 5 |
| SVG line-style nos feature-icons (nunca emoji) | ✅ OK | Princípio 13 |
| Badge de destaque em 1 card | ✅ OK | Princípio 14 |
| Seção "Nosso Compromisso" obrigatória | ✅ OK | Princípio 15 |
| CTAs variados (proibido repetir) | ✅ OK | Princípio 16 |
| Zero placeholders (wa.me/55?, "consulte", etc.) | ✅ OK | Princípio 12 |
| Animações: slowZoom, fadeUp, hover | ✅ OK | Princípio 3 |
| PAUSAR se dado crítico faltar | ✅ OK | Princípio 12 + Anti-Pattern 11 |

---

## CARLOS CARTA

### Status: ✅ OK (reescrito nesta sessão)
| Regra | Status | Ação |
|-------|--------|------|
| Gold standard salvo em _references/ | ✅ OK | Criado nesta sessão |
| Lê gold standard antes de cada email | ✅ OK | Princípio 1 + task Passo 0 |
| Estrutura 9 blocos obrigatória | ✅ OK | Princípio 2 + task Passo 3 |
| 180-240 palavras | ✅ OK | Princípio 3 |
| Tom: pessoa, não marketer | ✅ OK | Tone Rules |
| Anti-padrões proibidos (lista de frases) | ✅ OK | Anti-Patterns + task |
| Assuntos no novo padrão (sem dois pontos) | ✅ OK | Princípio implícito + task Passo 4 |
| Screenshots via Playwright (375x812) | ✅ OK | Princípio 7-8 |
| Salvar em screenshots/ como 01/02/03 | ✅ OK | task Passo 1 |
| NUNCA gerar screenshot com IA | ✅ OK | Anti-Pattern 8 |
| PAUSAR se Playwright falhar | ✅ OK | Princípio 7 |
| Assinatura: "Abraço, / Miguel Magalhães Silveira / 12974062797" | ✅ OK | Princípio 9 + Bloco 9 |

---

## VERA VEREDITO

### Status: ✅ Corrigido
| Regra | Status | Ação |
|-------|--------|------|
| Checklist 15 itens obrigatório | ✅ OK | Agente original |
| Item 1 condicional (prova social alternativa) | ✅ OK | Exceção documentada no task |
| Verifica Unsplash sintaxe source.unsplash.com | ❌ → ✅ | Item 7 reescrito no checklist do agente + task |
| Verifica onerror fallback Picsum | ❌ → ✅ | Item 7 reescrito no checklist do agente + task |
| Verifica 9 blocos do email (gold standard) | ✅ OK | Adicionado nesta sessão |
| Verifica anti-padrões do Carlos | ✅ OK | Adicionado nesta sessão |
| Rejeição automática se qualquer item falhar | ✅ OK | Agente original |
| Feedback acionável item por item | ✅ OK | Agente original |

---

## EDUARDO ENVIO

### Status: ✅ OK (reescrito nesta sessão)
| Regra | Status | Ação |
|-------|--------|------|
| Gmail MCP desativado | ✅ OK | Reescrito nesta sessão |
| Gera apenas kit-envio.md por negócio | ✅ OK | Reescrito nesta sessão |
| Kit contém: para, canal, assunto, corpo, screenshots, horário | ✅ OK | task gerar-kit-envio.md |
| contatados.md só após confirmação manual | ✅ OK | Princípio 2 |
| criar-rascunho-gmail.md marcado DEPRECATED | ✅ OK | Arquivo sobrescrito nesta sessão |

---

## ARQUIVOS DE MEMÓRIA

| Arquivo | Status |
|---------|--------|
| `_memory/contatados.md` | ✅ Existe — 5 negócios bloqueados até 2026-06-18 |
| `_memory/descartados.md` | ✅ Existe — vazio (criado nesta sessão) |
| `_references/email-padrao-sabor-do-ipiranga.md` | ✅ Existe — gold standard integral com análise |

---

## PIPELINE COMPLETO

| Etapa | Agente | Status |
|-------|--------|--------|
| 1. Busca 5 negócios | Pablo Prospecção | ✅ |
| 2. Investiga 14 fontes + 3 reviews | Roberto Rastro | ✅ |
| 3. Filtra por contato direto + score | André Análise | ✅ |
| 4. Cria site HTML (Unsplash source + Picsum fallback) | Diego Digital | ✅ |
| 5. Escreve email 9 blocos + screenshots | Carlos Carta | ✅ |
| 6. Revisa 15 itens + gold standard | Vera Veredito | ✅ |
| 7. Gera kit-envio.md (NÃO envia) | Eduardo Envio | ✅ |
| 8. Usuário envia → confirma → Eduardo registra | — | ✅ |

---

## RESUMO DE MUDANÇAS DESTA VERIFICAÇÃO

### Corrigidos agora (4 itens):
1. **Pablo** — Adicionados Princípios 4 e 5: não bloquear por descartados.md + buscar mais se descartes forem altos
2. **Diego agent.md** — Princípio 1 expandido: sintaxe source.unsplash.com + onerror Picsum + Anti-Patterns 16-17
3. **Diego task** — Step 4 reescrito: tabela de keywords por nicho, exemplos de URL, instrução onerror com seed único
4. **Vera** — Item 7 do checklist atualizado para verificar sintaxe e fallback; task revisar.md idem

### Já estavam corretos (sem mudança):
- Roberto Rastro (atualizado anteriormente nesta sessão)
- André Análise (atualizado anteriormente nesta sessão)
- Carlos Carta (reescrito completamente nesta sessão)
- Eduardo Envio (reescrito completamente nesta sessão)
- Todos os arquivos de memória

---

*Verificação concluída. Squad pronto para próxima rodada quando o usuário confirmar.*
