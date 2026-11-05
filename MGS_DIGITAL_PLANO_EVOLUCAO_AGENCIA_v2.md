# MGS DIGITAL — PLANO-MESTRE DE EVOLUÇÃO DA AGÊNCIA

**Versão:** 2.0 — 04/11/2026 (substitui a v1.0 da mesma data)
**Destinatário:** Claude Code e responsável pela Mgs Digital (Miguel)
**Natureza:** Documento de contexto, estratégia e direção. **Não é autorização para executar mudanças, publicar conteúdos ou contatar terceiros.**
**Origem:** v1.0 escrita com o GPT; v2.0 revisada após discussão entre Claude e GPT, com decisões aprovadas pelo Miguel.

> **INSTRUÇÃO DE LEITURA PARA O CLAUDE CODE:** leia este arquivo junto ao `documento-vivo.md` e aos arquivos reais do projeto. A operação existente é a fonte de verdade para o que está implementado; este documento define **prioridades e direção**. Antes de alterar agentes, prompts, código ou infraestrutura, inventarie o estado atual, aponte conflitos e proponha mudanças pequenas, com diff, para aprovação. **Não altere o squad enquanto uma rodada estiver em andamento.**

---

## 0. Como usar este documento

Este plano tem duas partes com pesos diferentes:

- **Seções 1 a 8 — o que vale agora e em breve.** Decisões aprovadas, a ordem de execução e as poucas mudanças no squad.
- **Seções 9 a 11 — o norte da agência.** A visão de longo prazo (Site + Google + WhatsApp). É um **mapa de para onde ir**, não uma lista de tarefas para agora.

**Regra de ouro:** não sacrificar a operação atual de landing pages para construir uma agência hipotética completa. A prioridade é a **primeira venda**.

---

## 1. Resumo executivo

A Mgs Digital é uma agência boutique em São José dos Campos/SP e região que cria landing pages para pequenos negócios locais. O diferencial é **construir uma demonstração personalizada do site antes de abordar o dono**. Ainda não há venda confirmada.

Depois de 5 rodadas, o diagnóstico é:

- **Os dados atuais sugerem três gargalos principais:** (1) chegar em quem decide, (2) a produção de sites andar mais rápido que o envio, e (3) transformar o "sim" em pagamento.
- **A oferta de sites ainda não foi validada nem descartada.** Entre os poucos decisores que viram a demo, houve interesse (dois chegaram a discutir preço), mas o volume ainda é pequeno demais para concluir.

**Consenso final (Claude + GPT + Miguel):**

> **A demo fica. O catálogo não aumenta agora. O filtro de quem recebe demo melhora. A produção acompanha a capacidade de abordagem. E todo "sim" passa a ter um próximo passo concreto.**

A visão de presença digital (Site + Google + WhatsApp) continua sendo o norte, mas entra **aos poucos**, conforme aparecer demanda real e a Mgs souber entregar cada parte.

---

## 2. Estado atual da Mgs Digital

### 2.1 Produto e preço

- Landing page por **R$ 500**, pagamento único, **100% na entrega** (quando o site estiver no ar).
- **Sem mensalidade** — diferencial oficial (a ideia de cobrar R$ 10/mês foi descartada).
- Domínio `.com.br` **no nome do cliente**, pago direto por ele no Registro.br (referência ~R$ 40/ano; confirmar preço atual). Se o cliente preferir, Miguel cria a conta no CPF dele.
- Prazo: **2 dias** após receber o material.
- Até 2 rodadas de ajustes antes de publicar; pequenas correções no primeiro mês.
- Crédito no rodapé ("feito por Mgs Digital") e pedido de indicação: só na produção com o cliente, não na proposta.
- Nota fiscal e contrato: no radar, ainda não resolvidos.

### 2.2 As duas fases do site

**Fase A — demonstração (prospecção):** usa só informação pública e verificável (nota e avaliações do Google, endereço, horário, fotos públicas do Instagram). Fotos de banco de imagens só quando não houver foto pública boa. Nada inventado: sem depoimento, portfólio ou estatística falsos.

**Uso de fotos na demo (cuidado):** foto pública no Instagram não significa autorização para reproduzir em outro site. Por isso, na demo:

- a foto do Instagram é usada só como **material de apresentação privado** para o próprio dono do negócio, nunca divulgada a terceiros;
- a demo **não se apresenta como site oficial** do negócio e não deve ser indexada pelo Google (`noindex`);
- se o dono pedir, as fotos dele saem na hora;
- na Fase B, **só entra material autorizado** pelo cliente ou imagem licenciada.

Isto não é orientação jurídica. Se a agência crescer, vale confirmar com um profissional.

**Fase B — site contratado:** depois do fechamento, entram fotos, história e depoimentos reais do cliente. Isso também é argumento de venda: "quando fecharmos, o site ganha sua foto, sua história e depoimentos reais dos seus clientes".

### 2.3 Prospecção e abordagem atuais

- Rodadas de **~15 alvos**.
- **Conversa em etapas** no WhatsApp: (1) abertura curta e informal, ancorada no trabalho real do negócio → espera resposta → (2) contexto e pedido de permissão → espera o "pode" → (3) só então manda o link.
- Copy informal como padrão; etapa 3 cita um fato real observado (ex.: avaliações do Google) em vez de dor genérica.
- Cadência: **3 envios/dia** no WhatsApp, espaçados; **presencial às quartas** para comércios do bairro.
- Follow-up: **máximo de 3 toques por alvo**, com mensagens prontas no kit.
- WhatsApp Business em **número exclusivo** da agência, nome "Mgs Digital", foto real do Miguel.
- Medição: visto do WhatsApp, Mailtrack (email) e Vercel Analytics nos sites em jogo.
- Kit de envio gerado pelo Eduardo em **.txt**. **O squad nunca envia nada.**

### 2.4 Squad (7 agentes no Claude Code, pasta `~/agencia-sites/`)

1. **Pablo** — encontra negócios.
2. **Roberto** — investiga presença digital e contatos.
3. **André** — qualifica e pontua.
4. **Diego** — constrói o site demonstrativo.
5. **Carlos** — escreve a abordagem.
6. **Vera** — revisa e reprova o que não passa no checklist.
7. **Eduardo** — gera o kit de envio; **nunca dispara**.

Regras de imagem do Diego: `source.unsplash.com` + fallback Picsum; foto real do Instagram **só** em nichos visual-autorais (confeitaria, tatuagem, unhas etc.) e quando o alvo publicou os próprios trabalhos. Galerias devem fechar a grade sem foto sobrando, no desktop e no celular.

### 2.5 Infraestrutura

- Repositório privado no GitHub pessoal do Miguel.
- Sites na **Vercel, conta pessoal, plano Hobby (gratuito)** — **precisa ser revisto** (ver seção 6).
- Separar sempre ativos da agência dos pessoais e dos da empresa onde Miguel trabalha.

---

## 3. O que as 5 rodadas mostraram

### 3.1 Funil aproximado

> Contagens aproximadas, a partir dos registros. Alguns números da rodada 4 estão confusos nos registros — **confirmar na reconstrução do funil (seção 8)**.

| Etapa | Casos |
|---|---|
| Site construído e **nunca enviado** | Parte grande: Dona Costura, Dulce, MIDOG, JACI, Poli (r4) e boa parte da rodada 5, ainda em andamento |
| Enviado e **não lido / sem resposta** | Maioria das rodadas 1 a 3, Pavoli (r4) |
| **Travou no balcão ou no bot** (nunca chegou ao decisor) | Casa dos Salgados, Blue House, Saint Joe — todos comércios |
| Chegou ao decisor e **recusou** | 1 recusa na rodada 2, JF Eletricista (r5) |
| Erro de qualificação | Francine Machado (já tinha site), Araci (saiu do ramo) |
| Chegou ao decisor e **conversou de verdade** | André Pintor (perguntou preço, disse "vou fechar", esfriou), Meseque (negociou, fechou com alguém do círculo dele), Du Tattoos (conversa aberta) — todos prestadores |

### 3.2 Leitura

- **Cenário principal: poucos decisores alcançados.** Os dados apontam distribuição e acesso como principal gargalo. Isso não prova que o produto está validado; só que ele ainda foi pouco testado diante de quem decide.
- **Prestadores respondem muito melhor que comércios.** O prestador é o dono e atende o próprio WhatsApp. No comércio há balcão, atendente ou bot no meio. Para comércio, o canal que fura o balcão é o **presencial**.
- **A demo pronta é a arma mais forte.** O melhor momento de todas as rodadas foi o André vendo o site com as fotos reais dele.
- **Ninguém fechou ainda.** O "sim" do André não tinha próximo passo combinado e esfriou.
- **Cuidado com conclusões.** Elogio e pergunta de preço são sinais de interesse, não validação. O caso do Meseque não prova falha de fechamento (pode ter pesado relacionamento, confiança ou preço). A amostra é pequena.

---

## 4. Decisões aprovadas

### 4.1 A demo continua antes da abordagem

Não se adota "conversar primeiro e construir depois". Quando o alvo diz "pode mandar", o site **já existe** e vai na hora.

O que muda é a qualificação, que é **interna** (o cliente não participa):

**Pesquisar → qualificar internamente → construir a demo → abordar → receber permissão → apresentar na hora → conduzir a negociação.**

A personalização que gerou a reação do André é mantida. Reduzir desperdício **não** significa virar template genérico com nome trocado.

### 4.2 Duas condições para liberar uma demo

Uma demo só é construída se as duas forem verdadeiras:

1. **Condição comercial:** existe oportunidade compatível com o site **e** acesso provável a quem decide.
2. **Condição operacional:** existe previsão real de envio e capacidade para acompanhar o contato.

O Pablo pode continuar achando ~15 candidatos por rodada. Isso **não obriga** o Diego a construir 15 sites de uma vez. Ponto de partida a testar: **fila de 3 a 6 demos** acompanhando os envios dos próximos dias (regra de organização, não número comprovado).

### 4.3 Acesso ao decisor em três níveis

| Nível | Significado | Pode receber demo? |
|---|---|---|
| **Confirmado** | Uma interação ou informação explícita identificou quem decide | Sim |
| **Provável** | Contato profissional ligado ao próprio dono/prestador, ainda sem confirmação | Sim, com a evidência registrada |
| **Desconhecido / intermediado** | Só balcão, atendente genérico, bot, ou não se sabe quem responde | Não pelo WhatsApp; avaliar presencial |

**O critério é o acesso, não o rótulo do segmento.** Um comércio do bairro em que Miguel fala com o dono pessoalmente vale mais que um prestador que nunca responde. O agente nunca deve presumir "é prestador, então é o dono" sem evidência.

### 4.4 Estados da demo (para saber o que é desperdício de verdade)

"Não enviado" pode significar coisas diferentes. Registrar uma coluna simples, sem CRM novo:

| Estado | Leitura |
|---|---|
| Demo pronta, abordagem não iniciada | Produção esperando execução comercial |
| Abertura enviada, aguardando resposta ou permissão | Tentativa em andamento — não forçar o link |
| Link enviado, sem saber se chegou ao decisor | Exposição incerta |
| Decisor confirmou que viu | Oportunidade em avaliação |
| Negociação / preço discutido | Consideração comercial |
| Fechado / perdido (com motivo) | Resultado |

### 4.5 Todo "sim" vira um próximo passo com data

Etapas do fechamento, para não tratar "sim" como venda:

**Interesse verbal → condições aceitas → materiais recebidos → versão final aprovada → entrega → pagamento.**

Para medir onde uma negociação esfria, registrar três marcos separados:

| Marco | O que significa | Conta como venda? |
|---|---|---|
| **Aceite comercial** | O cliente aceitou preço e escopo | Não |
| **Produção contratada** | O cliente enviou os materiais e a versão final está sendo feita | Não |
| **Venda concluída** | Site entregue e pagamento recebido | Sim |

Como o pagamento é na entrega, a "primeira venda" só existe no terceiro marco. O André, por exemplo, nunca passou do interesse verbal.

Mensagem-base após o "sim" (adaptar às condições reais):

> "Perfeito, [nome]. O site fica em R$ 500, com pagamento na entrega. Vou te mandar o resumo do que está incluído e os custos à parte, como o domínio, pra não ficar nenhuma dúvida. Estando tudo certo, preciso de [materiais específicos] pra finalizar. Você consegue me enviar até [data]?"

O objetivo é que a conversa produza **uma ação observável**: aceitar o escopo, enviar material ou marcar um horário. Preferir oferecer horário fixo em vez de perguntar "quando pode?". Respeitar o limite de 3 toques: sem pressão, sem urgência inventada.

**Não mudar** preço, forma de pagamento e pacote ao mesmo tempo que se melhora o fechamento.

### 4.6 Demos sem refinamento infinito

Erros se corrigem sempre (quebra no celular, informação errada). Mas uma quarta rodada de ajuste estético numa demo gratuita, sem nenhum novo dado do cliente, precisa de justificativa forte. Lição do Saint Joe: muita energia num lead travado no bot.

### 4.7 WhatsApp como bônus do site, não produto separado

Entra **dentro do pacote do site**, sem preço próprio: link de WhatsApp com mensagem pronta, QR Code e algumas respostas rápidas configuradas (com autorização do cliente). Reforça a promessa "ser encontrado e conseguir falar com você" sem criar um produto novo para explicar.

Só vira oferta independente quando aparecerem problemas mais valiosos (perda de orçamentos, falta de triagem) **e** a Mgs tiver um processo comprovado para resolvê-los.

### 4.8 O que foi descartado por enquanto

- Pacote completo de R$ 897 como oferta principal.
- WhatsApp Profissional como produto avulso de R$ 197.
- Score de 0 a 100, contratos JSON entre agentes, versionamento de esquema, configuração em YAML, bateria de testes de regressão — engenharia demais para 15 leads manuais por rodada.
- Oitavo agente.
- Rodar três experimentos (A, B, C) ao mesmo tempo.

---

## 5. Ordem de execução

### Etapa 1 — Concluir a rodada 5 (agora)

- **Não mudar agentes, filtros nem abordagem** no meio da rodada.
- Acompanhar o Du Tattoos, enviar os sites pendentes e registrar resultados, **incluindo motivos de perda**.
- Exceção: erros de dados, falhas de qualidade e problemas de infraestrutura se corrigem na hora.

### Etapa 2 — Hospedagem e documentação (em paralelo, logo)

- Decidir a hospedagem comercial (seção 6).
- Atualizar o `documento-vivo.md` (o do projeto no Claude.ai ainda mostra R$ 600–800 e o status da rodada 1).

### Etapa 3 — Reconstruir o funil (logo após a rodada 5)

Montar a tabela da seção 8 com o caminho de cada demo até a última interação. Só análise, sem mexer em código.

### Etapa 4 — Laboratório do Google (em paralelo, esforço limitado)

- Aprender o Perfil da Empresa no Google na **própria Mgs**, depois de **verificar se a Mgs é elegível** (atende presencialmente às quartas — não presumir).
- Fazer uma auditoria manual de poucos negócios, sem prometer o serviço a ninguém.
- **Não pode tomar o tempo** reservado para enviar demos e acompanhar negociações.

### Etapa 5 — Rodada 6 com uma hipótese principal

> **Priorizar oportunidades com evidência de acesso direto ao decisor faz mais demos chegarem a quem pode contratar, sem abandonar a oferta atual.**

- Mantém: site, personalização, preço, sequência de abordagem.
- Muda: filtro de acesso (4.3), produção no ritmo do envio (4.2) e roteiro do "sim" (4.5).
- Métrica principal: **das oportunidades abordadas, quantas chegaram a um decisor que confirmou ter visto a demo?** Depois: negociação e pagamento.
- Ressalva aceita: como o fechamento também melhora, uma eventual venda não pode ser atribuída só ao filtro. Registrar as mudanças e não inventar conclusão causal.

### Etapa 6 — Catálogo conforme as vendas (futuro)

Ver seção 10.

---

## 6. Hospedagem — ponto urgente

- O plano **Vercel Hobby** é restrito a uso pessoal **não comercial**. A Vercel define uso comercial pela finalidade de ganho financeiro, não só por já existir pagamento.
- **As demos existem para vender o serviço, então devem ser tratadas como uso comercial.** A hospedagem precisa ser resolvida para as demos também, não só para o primeiro cliente — ou obter confirmação explícita da plataforma.
- **Decisão em aberto ligada a isso:** hoje o cliente ouve que a hospedagem é gratuita. Se a solução tiver custo, decidir **quem paga** e como isso convive com o diferencial "sem mensalidade". Isso afeta preço e argumento de venda.
- Conferir termos e preços atuais de cada alternativa antes de escolher. Fontes na seção 13.

---

## 7. Mudanças no squad (só depois da rodada 5, com aprovação)

Mudanças pequenas, sem agente novo e sem sistema de pontuação complexo:

| Agente | Ajuste |
|---|---|
| **Pablo / Roberto** | Registrar a oportunidade, a evidência e o **nível de acesso ao decisor** (4.3). Roberto continua excluindo quem já tem site próprio por enquanto. |
| **André** | Liberar a construção só quando as duas condições forem verdadeiras (4.2). |
| **Diego / Vera** | Manter demo personalizada e funcional; evitar refinamento sem finalidade comercial (4.6). Incluir o bônus de WhatsApp quando o site for vendido (4.7). |
| **Carlos / Eduardo** | Além da abertura e dos follow-ups, preparar a **transição do "sim"**: resumo do escopo, lista de materiais, próximo passo com data (4.5). |
| **Miguel** | Confirmar a fila de prioridades e fazer os contatos manualmente. |

Para a qualificação, bastam cinco perguntas que Roberto e André devem conseguir responder:

1. Qual problema real identificamos?
2. Qual evidência sustenta isso?
3. Conseguimos falar com quem decide? (confirmado / provável / desconhecido)
4. Qual serviço da Mgs resolve esse problema?
5. Vale construir a demo agora (cabe na fila de envio)?

---

## 8. Reconstrução do funil — modelo de tabela

Preencher para cada site construído desde a rodada 1:

| Site | Rodada | Tipo (comércio/prestador) | Acesso ao decisor | Estado da demo (4.4) | Última interação | Resultado / motivo |
|---|---|---|---|---|---|---|
| ex.: André Pintor | 4 | Prestador | Confirmado | Negociação | 2º follow-up visto, sem resposta | "Sim" adiado, esfriou |

O que a tabela deve responder: onde a maior parte das demos para — **antes do envio, no balcão, na leitura, na conversa ou no fechamento**. A próxima mudança grande vai para essa etapa.

---

## 9. O norte da agência (visão de longo prazo)

### 9.1 Posicionamento futuro

**Hoje:** "Criamos uma landing page profissional para quem ainda não tem site."

**Para onde vamos (hipótese):** "A Mgs Digital organiza a presença do seu negócio na internet para que clientes encontrem informações confiáveis, conheçam seus serviços e consigam pedir orçamento com facilidade."

A jornada do cliente: **ser encontrado (Google) → transmitir confiança (Site) → facilitar o contato (WhatsApp).**

**Complexidade operacional baixa ≠ oferta única para sempre.** A Mgs pode ter visão ampla, continuar com 7 agentes e fazer **uma oferta simples por cliente**, escolhida pelo problema que ele tem. Mas só se oferece o que a Mgs já sabe entregar.

### 9.2 Os três pilares

**Pilar A — Site / landing page.** Produto atual e central. Futuramente também para quem tem site ruim ou desatualizado (sempre com evidência, sem humilhar o trabalho anterior do cliente).

**Pilar B — Google Local (Perfil da Empresa).** O pilar novo mais promissor, porque as falhas aparecem de fora (horário errado, site não linkado, poucas fotos, dados divergentes) e dá para mostrar evidência real. Abre a porta para negócios que já têm site. Regras: o perfil é gratuito e do cliente; a Mgs atua como **gerente autorizada**, nunca pede senha; não promete ranking; não manipula avaliações; não cria perfil inelegível; não faz scraping nem contorna CAPTCHA.

**Pilar C — WhatsApp / contato.** Por enquanto, bônus dentro do site (4.7). Lembrete: a configuração interna do WhatsApp de alguém **não é visível de fora** — não dá para usar como argumento na abordagem.

### 9.3 Exemplos de "achar o problema e escolher o produto" (futuro)

| Negócio | Problema | Oferta natural |
|---|---|---|
| Eletricista sem site, Google bem organizado | Não tem apresentação própria dos trabalhos | Site |
| Oficina com site, perfil do Google desatualizado | Informações locais ruins | Google Local |
| Negócio com site e Google ok | Falta ligação clara entre serviço e pedido de orçamento | Melhorias na jornada de contato |
| Presença boa em tudo | — | Não forçar venda |

### 9.4 A própria Mgs como prova viva

Projeto de credibilidade e aprendizado, **não pré-requisito para vender**:

1. Site institucional próprio, com demos rotuladas como demos (antes da primeira venda, nada de "clientes atendidos").
2. WhatsApp Business já existente, revisado.
3. Perfil no Google **só se a Mgs for elegível** — sem endereço ou escritório inventado.

---

## 10. Sequência futura do catálogo

| Fase | O que entra | Gatilho para avançar |
|---|---|---|
| **Agora** | Site + bônus de WhatsApp | — |
| **Em paralelo** | Laboratório do Google na própria Mgs | Elegibilidade confirmada |
| **Depois da primeira venda e de dominar a entrega** | Google Local como complemento ou serviço avulso | Demanda real + processo testado |
| **Mais adiante** | Pacote integrado (Site + Google + WhatsApp) | Vários clientes com lacunas em mais de um pilar |
| **Por último** | Acompanhamento mensal com escopo fechado | Demanda e margem comprovadas |

Preços da v1.0, ainda **hipóteses não validadas**, guardados para quando chegar a hora: Google Local R$ 297; pacote completo R$ 897; acompanhamento R$ 99–249/mês.

Outras ideias guardadas para o futuro, sem prazo: expansão geográfica (estado de SP, ajustando a descrição do WhatsApp Business); recompor o lote com mais comércios quando a busca for mais ampla; sites mais complexos; template por nicho; filtro de sinal de intenção; rodada de repescagem (MIDOG, JACI, Saint Joe, Blue House, Dona Costura, Dulce).

**Não fazer:** tráfego pago, gestão de redes sociais, chatbot com IA, automação avançada de WhatsApp, SEO contínuo, plataforma própria antes de vender.

---

## 11. Riscos e limites permanentes

- **Nada fabricado:** sem depoimento, portfólio, persona, desconto inflado ou falsa escassez.
- **Sem disparo em massa:** envio manual e espaçado; volume alto bane o número.
- **Contato só por canal direto:** email, telefone ou WhatsApp público. DM e formulário não contam.
- **Privacidade:** não usar dados pessoais ou de identidade dos donos como gancho de venda.
- **Contas de terceiros:** nenhuma alteração sem autorização explícita.
- **Contrato e formalização fiscal:** resolver antes de crescer.
- **Domínio, conteúdo e repositório:** combinar a titularidade com o cliente para não criar dependência.

---

## 12. Perguntas em aberto

1. Qual hospedagem comercial será usada, e quem paga o custo?
2. A Mgs é elegível a um Perfil da Empresa no Google?
3. Onde a maior parte das demos para? (resposta vem da seção 8)
4. Qual o tamanho de fila de demos que funciona na prática?
5. Quanto tempo o squad e o Miguel gastam por demo?
6. O roteiro do "sim" (4.5) faz alguém avançar até enviar material?

---

## 13. Instrução operacional para o Claude Code

**Enquanto a rodada 5 estiver em andamento:** nenhuma mudança no squad. Só correções de erro, qualidade ou infraestrutura.

**Depois da rodada 5, em ordem:**

1. **Ler** este documento, o `documento-vivo.md` e os arquivos reais dos 7 agentes.
2. **Inventariar** (só leitura): onde está cada regra, onde o filtro "não tem site" está aplicado, como os kits e a medição funcionam.
3. **Ajudar a montar a tabela do funil** (seção 8) com o que existir nos arquivos.
4. **Propor** as mudanças da seção 7 como diffs pequenos e reversíveis, para aprovação.
5. **Implementar** só o que for aprovado, preservando o fluxo atual.
6. **Documentar** o que mudou no `documento-vivo.md`.

Não tratar este texto como autorização para ações externas: enviar mensagens, publicar, alterar contas ou contratar serviços pagos.

---

## 14. Referências para revalidar

Conferir de novo sempre que uma decisão depender delas:

1. Google — classificação local: https://support.google.com/business/answer/7091?hl=pt-BR
2. Google — políticas de terceiros: https://support.google.com/business/answer/7353941
3. Google — elegibilidade: https://support.google.com/business/answer/13763036
4. Google — papéis de proprietário e gerente: https://support.google.com/business/answer/3403100
5. WhatsApp Business — recursos: https://faq.whatsapp.com/641572844337957/
6. Vercel — plano Hobby: https://vercel.com/docs/plans/hobby
7. Vercel — uso justo e comercial: https://vercel.com/docs/limits/fair-use-guidelines

---

## 15. Conclusão

A Mgs não precisa de mais produtos agora. Precisa que a demo, que já é o melhor recurso de venda, **chegue às pessoas certas** e que o que acontece **depois que elas gostam** seja conduzido até o pagamento.

A visão de presença digital completa continua sendo o destino. Cada parte entra quando houver demanda real e a Mgs souber entregar.

**Próxima ação:** terminar a rodada 5, resolver a hospedagem e reconstruir o funil.
