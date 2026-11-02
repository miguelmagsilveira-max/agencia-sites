# Documento Vivo — Negócios-Sites

Documento vivo da agência de sites: registro contínuo de status, decisões e aprendizados do projeto de prospecção.

## Quem é Miguel
- Miguel Magalhães Silveira, de São José dos Campos/SP
- Iniciante em tecnologia (não programa, usa Claude Code + Claude.ai)
- Telefone: 12974062797 · Email: miguel.silveira@redealumni.com

## O Negócio
Agência de landing pages para pequenos comércios locais em São José dos Campos.
- Entrega única R$600-800 por site, sem mensalidade
- Hospedagem Vercel (grátis) + domínio Registro.br (~R$40/ano no nome do cliente)

## Squad prospeccao-sites — 7 agentes inline
1. Pablo Prospecção — busca 5 negócios sem site via Google Maps, consulta contatados.md
2. Roberto Rastro — investiga 14 fontes pra achar email/telefone + 3 reviews textuais
3. André Análise — filtro bloqueante de contato direto (email/tel/WhatsApp; DM não conta), score 0-10
4. Diego Digital — site HTML premium (API oficial da Unsplash com chave no `.env`; foto real do Instagram do alvo via `imagens-insta/` SÓ quando passa o gate de 2 condições: nicho visual-autoral E trabalho próprio usável — fora disso, Unsplash + Picsum; 8-10 seções, SVG icons)
5. Carlos Carta — conteúdo da proposta (`email.md`) no tom INFORMAL padrão (rodada 4), em 9 blocos que alimentam a sequência de etapas do Eduardo; Sabor do Ipiranga vira fonte de tom + formato legado de mensagem única; + 3 screenshots Playwright
6. Vera Veredito — revisa 15 itens, rejeição automática
7. Eduardo Envio — gera **kit-envio.txt** (texto puro) na **sequência de etapas informal** (abertura → [aguarda] → contexto+permissão → [aguarda] → link), um follow-up por etapa (NÃO envia; Miguel envia manual)

Pipeline: Pablo → Roberto → André → (filtro) → Diego → Carlos → Vera → Eduardo → Miguel envia

## Gold standard de email
Sabor do Ipiranga (primeira venda manual). Salvo em _references/email-padrao-sabor-do-ipiranga.md. Serve como **fonte de tom** e **formato legado de mensagem única** (canal e-mail quando fizer sentido mandar tudo de uma vez). Os 9 blocos — abertura humana, elogio interpretado, transição, problema como história, ponte emocional, iniciativa concreta (passado), referência aos anexos, convite sem pressão, assinatura "Abraço, Miguel Magalhães Silveira, 12974062797" — continuam sendo a estrutura do conteúdo que o Carlos escreve, mas o **formato de envio padrão agora é a sequência de etapas informal** (ver "Padrões do squad vigentes" abaixo).

## Padrões do squad vigentes (ajustes estruturais 2026-10-15)

Valem daqui pra frente (não são de uma rodada específica):

1. **Kit de envio em .txt, sequência de etapas informal (Eduardo).** O Eduardo gera `kit-envio.txt` (texto puro, sem markdown pesado: nada de `#`, `**`, tabelas — texto corrido + separadores de hífens, pra copiar/colar fácil no celular). O formato padrão é a **sequência de etapas informal da rodada 4**: ETAPA 1 (abertura morna curta) → [AGUARDE] → ETAPA 3 (contexto + dor + permissão) → [AGUARDE] → ETAPA 5 (entrega do link + telas), com **um follow-up por etapa**. O Eduardo monta as etapas reorganizando o conteúdo aprovado do Carlos, sem inventar fato/dado. Mantém tudo o que já valia: não envia nada, link ao vivo e screenshots obrigatórios, contatados.md só após confirmação.
2. **Copy informal como tom padrão (Carlos + Eduardo).** O tom padrão das mensagens é o **informal/humano** (como na rodada 4), em sequência de etapas — não mais o registro longo e formal. O Carlos escreve o conteúdo (`email.md`) já nessa voz, em 9 blocos que mapeiam nas etapas (Blocos 1-2 → ETAPA 1; 4-5-8 → ETAPA 3; 6-7 → ETAPA 5). O email longo de 9 blocos (Sabor do Ipiranga) passa a ser **legado** (mensagem única, canal e-mail) e **fonte de tom/guardrails** — não o default.
3. **Foto do Instagram do alvo com gate de 2 condições (Diego).** Usar foto real do Instagram do alvo (`imagens-insta/`) **SÓ quando as duas valerem**: (a) nicho **visual-autoral** — o trabalho das mãos é o produto: confeitaria, tatuagem, pintura/marmorato, cestas, convites, unhas e similares; E (b) o alvo **publicou os próprios trabalhos de forma usável**. Fora disso (prestador de serviço, ou sem trabalho próprio usável) → **Unsplash oficial + Picsum fallback** com keyword específica do nicho. Isso governa a prioridade de imagem dos Princípios 1/22/30 e do Step 4.0; no tratamento SÓBRIO (prestadores) o gate normalmente fecha → Unsplash.

## Status atual

**Rodada 1 (enviada — resultados coletados em 30/05/2026):**
- 5 sites criados: Padaria Casa Doce, Big Skull Fitness, Salão Adriana, Lanchonete dos Amigos, Borracharia A Shalom
- 3 de 5 enviados: Lanchonete (email), 2 por WhatsApp
- Imagens enviadas junto, canais diretos (sem DM Instagram) — execução correta
- Resultado: 0 respostas após 2 semanas
- Problema de medição: Miguel não consegue ver se WhatsApp foi visualizado nem se email foi aberto
- Bug do Diego corrigido: IDs inventados do Unsplash → source.unsplash.com + Picsum fallback (esse padrão depois evoluiu — ver Aprendizados)
- Bloqueio dos 5 até 18/06/2026

**Rodada 2 (enviada — resultados):**
- 4 negócios enviados, com follow-up (2º toque) em todos
- Respostas: A Família respondeu "sem interesse" (recusou); Classe A, Equilibre-se e Cris = silêncio
- Falha de detecção de site: Equilibre-se (site institucional próprio equilibresectp.com.br) e A Família (página de delivery delivery.sistemapallas.com.br) passaram indevidamente por falha na detecção de presença web — corrigido no Roberto/André/Pablo (ver Aprendizados)
- contatados.md atualizado: A Família → recusou; Classe A, Equilibre-se, Cris → enviado sem resposta

**Rodada 3 (2026-07-11 — 5 sites, foco em nichos de serviço/ateliê):**
- 5 alvos: MIDOG (adestramento), Vinícius (personal), JACI (salgados), Casa dos Salgados, Dona Costura. 3 RICO com fotos reais + 2 SÓBRIOS.
- Resultado registrado no rodada2/aprendizados: A Família recusou (rodada 2); follow-up destravou a única resposta. Detecção de site em 3 categorias corrigida.

**Rodada 4 (2026-09-14 — MIX comércio × prestador, variável = identidade do remetente):**
- Variável isolada desta rodada: **identidade do remetente** (novo WhatsApp Business profissional, mudança feita FORA do Code). No Code, nada mudou em copy/site/lógica.
- Público MIX deliberado, etiquetado por tipo para comparar abertura: **3 COMÉRCIOS** — Blue House Banho e Tosa (pet, 4,9), Pavoli Sorvetes e Açaí (4,6), Saint Joe Burgerhouse (hamburgueria, 4,3) — **3 PRESTADORES** — André Pintor (marmorato, RICO com fotos reais do Insta), Meseque Montador (SÓBRIO), Araci Personal Organizer (SÓBRIO).
- Todos verificados: WhatsApp público, sem site institucional próprio (Saint Joe e Araci = 🟡 plataforma). Nenhum repete rodadas anteriores.
- 6 sites criados + deployados no Vercel (aliases públicos), screenshots, emails no gold standard, revisão Vera (6 APROVADOS), 6 kits etiquetados. **NÃO enviados** — envio manual do Miguel; contatados.md NÃO atualizado até confirmação.
- Links ao vivo (públicos): blue-house-three.vercel.app · pavoli.vercel.app · saint-joe.vercel.app · andre-pintor.vercel.app · meseque-montador.vercel.app · araci-organizer.vercel.app
- **Atualização Saint Joe (2026-10-04) — refino sobre material real do cliente (só este alvo):**
  - Site redesenhado na identidade P&B REAL da marca (cardápio oficial deles é todo P&B, sofisticado): preto predominante, tipografia display itálica pesada, selo circular, traços geométricos no espírito do cardápio. Objetivo: "parecer o site deles".
  - Botões reais estilo Linktree dentro de um site próprio (seção "Peça do seu jeito"): **iFood** (link real) · **Cardápio** (abre PDF real deles, servido em `/cardapio.pdf`, 200 `application/pdf`) · **Pedir para retirada** (WhatsApp (12) 97616-0016 com texto pré-preenchido) · **Contato/WhatsApp** (mesmo número). Retirada e contato apontam pro mesmo número, como no Linktree deles.
  - Selo **liberado**: "5ª melhor hamburgueria do Brasil — Guia do Hambúrguer (2016/17)", SEMPRE com fonte + ano (auto-declaração pública no Linktree oficial, confirmada pelo Miguel). Reverte a trava anti-"5ª melhor" dos briefings (que barrava por não-verificável): com a fonte confirmada, usar com atribuição.
  - Kit reescrito no ângulo **"casa própria que REÚNE tudo"** (iFood + cardápio + retirada + WhatsApp num lugar só, aparece no Google, à altura do tamanho da marca). REMOVIDO o ângulo "sem comissão / substituir/tirar o iFood" — era falso e arriscado: eles usam iFood/Linktree de propósito. É só-ganho, nada é tirado.
  - **Correção de refino (mesmo dia):** o P&B foi longe demais — identidade da marca (logo/tipografia/fundos/botões/selo) fica P&B, mas **fotos e mapa NÃO**. Removido todo filtro `grayscale` das imagens (comida em P&B tira o apetite) e do mapa; mapa voltou a ser Google Maps colorido e interativo (zoom/arrastar/rota) no endereço real. Aprendizado: aplicar P&B só na identidade, nunca em foto de comida nem em mapa.
  - Screenshots do kit regeneradas em cor (01-hero, 02-links, 03-cardapio). Vera aprovou site + kit. **Eduardo NÃO enviou** — envio manual do Miguel; contatados.md NÃO atualizado.

**Rodada 5 (2026-10-27 — em andamento):**

*Fase 0 — Migração Vercel + Web Analytics (concluída):*
- Os 17 sites da agência migrados da conta de TRABALHO (`miguelsilveira-prog` / miguel.silveira@redealumni.com) para a conta PESSOAL (`miguelmagsilveira-3897` / miguelmag.silveira@gmail.com), via transferência oficial da Vercel (API create/accept transfer-request). **Transferir (não recriar) preservou o link `.vercel.app` exato de cada site** — recriar mudaria o sufixo (ex.: `blue-house-three`, `casa-dos-salgados-olive`, `vinicius-personal-gamma`) e quebraria links já enviados. Piloto: dulce (nunca enviado). Verificado: todos HTTP 200, conteúdo idêntico byte-a-byte, dono = pessoal. `gestao-ativos` (não é da agência; único projeto com GitHub conectado, `github:miguelsilveira-prog/gestao-ativos`) ficou na conta de trabalho.
- CLI agora logado na conta pessoal (padrão daqui pra frente). Tokens de migração (expiração 1 dia) revogados pelo Miguel; arquivos temporários apagados.
- **Web Analytics** (plano Hobby, grátis: 50 mil eventos/mês somados, janela de relatório 1 mês, rastreia visitas/visitantes) ativado em **6 sites** — os em andamento / reservados pra repescagem: **poli-pinturas** (piloto), **blue-house**, **jaci-salgados**, **midog-adestramento**, **saint-joe**, **andre-pintor**. Rotina por site: comparar HTML local × ar (parar se divergir além do script) → religar `.vercel/` à conta pessoal → inserir snippet `/_vercel/insights/script.js` no HTML → Enable no painel (único passo só-painel) → redeploy pela conta pessoal → conferir link igual + `script.js` 200. Objetivo: saber se o alvo ABRIU o link (dado agregado, não identifica quem; para link enviado a 1 alvo ~ equivale a "abriu"; aberturas do próprio Miguel também contam). Os outros 11 sites ficaram SEM Analytics por decisão do Miguel.
- Status de envio real das rodadas 3-4 registrado no `contatados.md`: `reservado-repescagem` (Pablo NÃO prospecta): MIDOG, JACI, Saint Joe, Blue House; `em-andamento`: André Pintor, Poli; Araci `saiu-do-ramo`; Dona Costura e Dulce nunca enviados.

**Diagnóstico pendente (resolver antes de mudar copy):**
- Verificar tracinhos do WhatsApp (cinza = não lido / azul = lido)
- Instalar Mailtrack ou Streak no Gmail pra rastrear abertura de email
- Sem saber "não viram" vs "viram e ignoraram", qualquer mudança de copy é chute

**Próximos passos rodada 2:**
1. Resolver medição (read receipts + rastreador de email)
2. Testar follow-up — 2º toque destrava maioria das respostas em cold outreach
3. Testar link ao vivo hospedado no Vercel em vez de só screenshots
4. Reduzir atrito da resposta (pergunta sim/não fácil no final do email)
5. Rodar /opensquad run prospeccao-sites

## Aprendizados

- Imagens do Diego (padrão atual): API oficial da Unsplash com chave no `.env` + fotos reais do Instagram via `imagens-insta/` quando o negócio tem Instagram bom. (Histórico: IA inventava IDs do Unsplash → migrou-se para source.unsplash.com + Picsum → hoje descontinuado em favor da API oficial + fotos do insta.)
- Emails formulaicos não convertem → seguir gold standard humano (Sabor do Ipiranga)
- DM Instagram não rastreável + algoritmo limita alcance → priorizar email/WhatsApp/telefone
- Sites são demos comerciais, não finais → review negativa fica de fora
- Sem dado real (resultados), iteração é palpite — sempre medir antes de mudar
- Cold outreach tem taxa de resposta baixa por natureza — 3 contatos sem resposta é amostra pequena, não fracasso
- Follow-up (2º/3º toque) traz mais respostas que o 1º contato — não parar no primeiro envio
- Medição é pré-requisito: sem saber se viram, não dá pra saber se o problema é canal ou mensagem
- Detecção de site é crítica no critério "comércios SEM site" → o Roberto agora detecta e classifica presença web em 3 categorias: **site institucional próprio** (domínio próprio com sobre/serviços/contato) = DESQUALIFICA; **página de plataforma/delivery** (ex.: sistemapallas, iFood, cardápio online) = PASSA com ângulo de venda ("tem ferramenta de pedido, mas falta site institucional que apresente o negócio e apareça no Google"); **sem presença web própria** = QUALIFICA. Contexto: na rodada 2, Equilibre-se e A Família passaram com site/página existente por falha de detecção — proposta chegou a ser enviada pra quem já tinha site
- Follow-up confirmado: na rodada 2, o 2º toque destravou a ÚNICA resposta (A Família) — reforça que follow-up vale e o 1º contato sozinho não basta
- Rodada 4 isola a variável **identidade do remetente** (novo WhatsApp Business profissional) mantendo copy/site/lógica idênticos — desenho de teste correto para atribuir qualquer mudança de abertura ao remetente, não à mensagem. O MIX etiquetado [COMÉRCIO]/[PRESTADOR] permite comparar abertura por tipo de público na mesma rodada.
- **Vercel Deployment Protection:** projetos novos nascem com "Vercel Authentication" ligada → a URL de deployment (com hash, `projeto-hash-team.vercel.app`) redireciona pra login (inútil pro cliente). MAS o **alias de produção limpo** (`projeto.vercel.app`, ou `projeto-three` quando o nome está tomado) fica **público**. Solução: sempre usar o alias limpo no kit (testar com `curl` que retorna 200 e serve o conteúdo certo — cuidado com colisão de nome com projeto de terceiros). Desligar a proteção via API é ação de "enfraquecer segurança" e é barrada pelo classificador — não force; use o alias limpo.
- **Fork de si mesmo para tarefas paralelas é arriscado:** ao paralelizar a construção dos 6 sites com `subagent_type: fork`, os forks herdam o contexto de orquestrador e um deles "virou o Claude pai" (tentou parar os irmãos; outro alucinou "todos no ar"). Os arquivos foram escritos corretamente ANTES do descarrilamento, então o dano foi nulo, mas a lição é: para autoria paralela de artefatos, verificar SEMPRE o disco (não confiar no `result` do fork) e considerar subagentes `general-purpose` (contexto limpo) em vez de `fork` quando a tarefa não precisa do meu contexto inteiro.
- **Screenshot de site com scroll-reveal:** sites que usam `opacity:0` + IntersectionObserver só revelam no scroll — um screenshot full-page (sem rolar) sai com seções em branco. Antes de capturar, forçar visível via `evaluate` (opacity:1/transform:none) OU recortar de um full-page com os blocos já revelados. E blindar o site com rede de segurança (revelar após timeout + fallback `<noscript>`) pra nunca ficar em branco pro cliente.
