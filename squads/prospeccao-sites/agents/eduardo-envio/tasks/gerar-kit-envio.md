---
task: "Gerar Kit de Envio Manual"
order: 1
input:
  - emails_aprovados: Lista de email.md de todos os negócios que passaram pela revisão e foram aprovados pelo usuário no checkpoint 13
output:
  - kits_gerados: kit-envio.txt (texto puro) em cada pasta de negócio aprovado
  - contatados_atualizados: contatados.md atualizado após confirmação do usuário
---

# Gerar Kit de Envio Manual

Gera um arquivo `kit-envio.txt` (**texto puro**, não `.md`) para cada negócio aprovado. O **formato padrão é a sequência de etapas informal** (rodada 4): uma conversa em etapas montada a partir do conteúdo aprovado do Carlos, no tom humano, pronta para o Miguel copiar e colar etapa por etapa no celular. O usuário recebe o kit pronto e envia manualmente pelo canal correto (WhatsApp, email, DM, presencial). Eduardo não envia, não cria rascunhos e não agenda nada.

## Formato padrão: sequência de etapas (default)

O kit NÃO é mais uma mensagem única. É uma conversa em etapas, no tom informal/humano da rodada 4:

- **ETAPA 1 — Abertura morna curta** (a única que o Miguel manda primeiro): saudação pela hora + "aqui é o Miguel, sou de São José" + elogio interpretado do dado real (nota/anos) + uma pergunta leve que convida resposta.
- **[AGUARDE a resposta do lead]** — não mandar mais nada até ele responder.
- **ETAPA 3 — Contexto + dor + permissão**: o que o Miguel faz (cria site pra comércio daqui) + a dor específica do nicho (aparece no Maps mas não tem site pro cliente ver serviço/preço/agendar) + pedido de permissão ("posso te mandar pra dar uma olhada?").
- **[AGUARDE o "pode mandar"]**.
- **ETAPA 5 — Entrega do link (com as telas)**: entrega o link ao vivo + descreve o que tem no site (elementos reais) + avisa que as fotos são de exemplo quando for o caso + fecho leve ("o que achou?"). As 3 telas vão anexadas logo após o texto.

**Regra de montagem — reusar, não inventar:** Eduardo REORGANIZA o conteúdo aprovado do `email.md` nas etapas (encurtando e adaptando a voz para conversa). A nota, a dor, os elementos do site e o link são os MESMOS do email aprovado — só muda a forma. Nenhum fato, número, elogio ou promessa novo.

**Texto puro:** o conteúdo que o Miguel cola não leva `#`, `**`, `|` tabelas nem markdown. Usar texto corrido e separadores simples (linha de hífens `------`, rótulos em MAIÚSCULAS).

> O email longo de mensagem única (9 blocos, gold standard Sabor do Ipiranga) é **legado**: só usar quando o canal for e-mail e fizer sentido mandar tudo de uma vez. O default é a sequência de etapas acima.

## Process

1. **Para cada negócio aprovado no checkpoint 13**:

   a. **Verificar screenshots** — Checar se existem arquivos PNG em `squads/prospeccao-sites/output/{run_id}/{slug}/screenshots/`:
      - Se `01-hero.png` não existir: **PAUSAR e avisar o usuário** — não gerar kit sem screenshots
      - Se existir: listar os arquivos disponíveis com tamanho

   b. **Ler o arquivo `email.md`** do negócio para obter:
      - Destinatário (email, WhatsApp ou canal anotado pelo Roberto)
      - Assunto e corpo aprovados

   b2. **Ler o `link-ao-vivo.txt`** do negócio (`squads/prospeccao-sites/output/{run_id}/{slug}/link-ao-vivo.txt`) para obter a URL pública do site gerada no deploy do Diego. Essa URL entra no kit junto com o texto e os screenshots, para o usuário copiar junto.
      - Se o arquivo não existir: **PAUSAR e avisar o usuário** — o link ao vivo faz parte do kit.

   c. **Determinar canal de entrega**:
      - Email disponível → canal: Email
      - Telefone/WhatsApp disponível → canal: WhatsApp
      - Só Instagram → canal: DM Instagram
      - Sem contato digital → canal: Presencial / Ligação

   d. **Montar as etapas** a partir do `email.md` aprovado, reorganizando o conteúdo (sem inventar):
      - ETAPA 1 (abertura morna), ETAPA 3 (contexto + dor + permissão), ETAPA 5 (entrega do link + telas), com os marcadores `[AGUARDE]` entre elas.
      - Tom humano do Carlos: leve, pessoal, não corporativo, não vendedor. Texto puro, sem markdown.

   e. **Escrever um follow-up por etapa** adaptado ao negócio (mesmo tom humano, leve, sem pressão):
      - **Follow-up da ETAPA 1** (lead não respondeu a abertura — ~2 dias depois): reforça o elogio e antecipa que tem algo rápido pra mostrar.
      - **Follow-up da ETAPA 3** (respondeu a abertura mas sumiu no pedido — ~3 dias depois): "é só me dar um 'pode mandar' que te envio".
      - **Follow-up da ETAPA 5** (recebeu o link e não reagiu — ~3 dias depois): "conseguiu abrir aquele link? queria saber o que achou".

   f. **Gerar `kit-envio.txt`** (texto puro) em `squads/prospeccao-sites/output/{run_id}/{slug}/`:
      - Cabeçalho curto: negócio, status (kit gerado, NÃO enviado), canal + destino exato, link ao vivo, horário sugerido, âncora da abertura
      - As ETAPAS 1/3/5 com `[AGUARDE]` entre elas, cada uma pronta para copiar e colar
      - Os follow-ups por etapa, em seção separada e marcada ("só se ficar sem resposta")
      - Caminhos dos 3 screenshots para anexar junto da ETAPA 5
      - Instruções de envio (mandar uma etapa por vez, esperar resposta, conferir que o link abre sem login)

   g. Confirmar ao usuário que o kit foi gerado, informando o canal e destino exato

2. **Após gerar todos os kits**, informar o usuário:
   - Quantos kits foram gerados
   - Para quais negócios (com canal e destino de cada um)
   - Que cada kit é uma sequência de etapas (mandar uma por vez, esperar resposta) e traz um follow-up por etapa, para reenviar se o lead ficar sem responder
   - Instruções de envio por canal:
     - WhatsApp (canal principal): "Ajuste a saudação pela hora → mande a ETAPA 1 e PARE → depois da resposta, mande a ETAPA 3 e espere o 'pode mandar' → aí mande a ETAPA 5 + as 3 fotos → confira que o link abre sem login → horário ideal: fim de tarde"
     - Email: "Abra seu cliente de email → as etapas viram a sequência de mensagens (ou, se preferir mandar tudo de uma vez, use o email longo legado) → cole o texto com o link ao vivo → anexe os 3 PNGs → terça/quarta às 9h"
     - DM Instagram: "Abra o Instagram → DM para [@handle] → mande a ETAPA 1 e espere → siga as etapas → envie as 3 fotos junto da ETAPA 5"
     - Presencial: "Mostre as 3 fotos no celular ou leve impresso; deixe o link ao vivo para o cliente acessar depois"

3. **AGUARDAR confirmação do usuário** — Após as instruções, PAUSAR e aguardar o usuário confirmar que enviou.

4. **Somente após confirmação**, atualizar `contatados.md`:
   ```markdown
   | [Nome do negócio] | [Cidade] | [Data de hoje] | [Canal usado + destino] | enviado |
   ```

5. **Informar conclusão** da rodada:
   - "[N] kits gerados. [N] negócios registrados no contatados.md. Rodada concluída!"
   - Perguntar se quer sugestões de ajuste na abordagem baseadas nesta rodada

## Output Format (kit-envio.txt — TEXTO PURO)

O arquivo é `.txt`. Nada de `#`, `**`, `|` tabelas nem markdown — texto corrido com separadores de hífens e rótulos em MAIÚSCULAS. Modelo (adaptar por negócio; as etapas saem do `email.md` aprovado):

```text
KIT DE ENVIO — [Nome do Negócio]  ·  [COMÉRCIO] ou [PRESTADOR]

Status: kit gerado (sequência de conversa) — pronto, NÃO enviado. Aguardando sua confirmação de envio.
Canal recomendado: WhatsApp → (12) XXXXX-XXXX
Link ao vivo: https://[projeto].vercel.app
Horário sugerido: fim de tarde (17h–19h).
Âncora da abertura: [dado forte e verificável — ex.: nota 4,9 no Google].

ATENÇÃO: formato em etapas. Mande UMA etapa por vez e espere a resposta antes da próxima.
Onde estiver [AGUARDE], pare e espere.

------------------------------------------------------------
ETAPA 1 — ABERTURA (a única que você manda primeiro) · copiar e colar

[saudação pela hora]! Tudo bem? Aqui é o Miguel, sou de São José também.
[elogio interpretado do dado real — ex.: achei a [negócio] pesquisando [nicho] e reparei no 4,9 no Google, nota assim é raríssima. Parabéns!]
[pergunta leve que convida resposta — ex.: vocês atendem só o [bairro] ou a cidade toda?]

------------------------------------------------------------
ETAPA 2 — [AGUARDE a resposta do lead]

Não mande mais nada aqui. Espere ele responder.

------------------------------------------------------------
ETAPA 3 — CONTEXTO + DOR + PERMISSÃO (manda depois que ele responder) · copiar e colar

[o que o Miguel faz — ex.: além de ter curtido a nota de vocês, eu mexo com criação de site pra comércio daqui de SJC.]
[a dor do nicho — ex.: com 4,9, quando alguém pesquisa "[busca]" vocês aparecem no mapa, mas aí procuram um site pra ver serviço/preço/agendar e não acham — e vão pro concorrente que tem.]
[pedido de permissão — ex.: fiz uma coisa aqui pensando na [negócio]. Posso te mandar pra você dar uma olhada?]

------------------------------------------------------------
ETAPA 4 — [AGUARDE o "pode mandar"]

Só siga pra ETAPA 5 depois que ele topar ver.

------------------------------------------------------------
ETAPA 5 — ENTREGA DO LINK (manda com as telas) · copiar e colar

Show! Então dá uma olhada: é uma prévia que montei do site de vocês, só pra ver como ficaria no ar.
[elementos reais do site — ex.: botei a nota 4,9, os serviços, o endereço no [bairro] e um botão que já abre o WhatsApp pra agendar.]
[quando as fotos forem de banco: as fotos são de exemplo só pra dar o clima — no site de verdade entram as de vocês.]
https://[projeto].vercel.app
Abre direto no seu celular. O que você achou?

------------------------------------------------------------
FOLLOW-UPS (só se ficar sem resposta)

Follow-up da ETAPA 1 (não respondeu a abertura — ~2 dias depois):
[1-2 linhas reforçando o elogio e antecipando algo rápido pra mostrar]

Follow-up da ETAPA 3 (respondeu a abertura mas sumiu no pedido — ~3 dias depois):
[1-2 linhas: "é só me dar um 'pode mandar' que te envio aquilo que comentei. Se não for a hora, sem problema."]

Follow-up da ETAPA 5 (recebeu o link e não reagiu — ~3 dias depois):
[1-2 linhas: "conseguiu abrir aquele link da prévia? queria saber o que você achou."]

------------------------------------------------------------
ANEXOS — TELAS (enviar JUNTO com a ETAPA 5, logo após o texto)
squads/prospeccao-sites/output/[run_id]/[slug]/screenshots/01-hero.png
squads/prospeccao-sites/output/[run_id]/[slug]/screenshots/02-destaque.png
squads/prospeccao-sites/output/[run_id]/[slug]/screenshots/03-contato.png

------------------------------------------------------------
INSTRUÇÕES
1. Ajuste a saudação conforme a hora (bom dia / boa tarde / boa noite).
2. Mande a ETAPA 1 e PARE. Espere ele responder.
3. Só depois da resposta, mande a ETAPA 3. Espere o "pode mandar".
4. Aí sim mande a ETAPA 5 + as 3 telas. Confira que o link abre sem pedir login.
5. Me confirme como foi cada etapa, pra eu registrar no contatados.md.
```

## Quality Criteria

- [ ] Screenshots verificados antes de gerar kit (01-hero.png obrigatório)
- [ ] kit-envio.txt (texto puro) gerado na pasta correta para cada negócio aprovado
- [ ] Kit montado na sequência de etapas (ETAPA 1 → [AGUARDE] → ETAPA 3 → [AGUARDE] → ETAPA 5)
- [ ] Texto das etapas sem markdown pesado (sem `#`, `**`, tabelas) — limpo para colar no celular
- [ ] Conteúdo das etapas reorganiza o email.md aprovado, sem inventar fato/dado novo
- [ ] Canal de entrega correto com destino exato (não genérico)
- [ ] Link ao vivo (de link-ao-vivo.txt) incluído na ETAPA 5
- [ ] Caminhos dos screenshots listados com clareza
- [ ] Horário sugerido incluído
- [ ] Um follow-up por etapa (ETAPA 1, 3 e 5), tom do Carlos, adaptado ao negócio, em seção separada e marcada
- [ ] contatados.md atualizado SOMENTE após confirmação explícita do usuário
- [ ] Registro no contatados.md com todos os campos obrigatórios

## Veto Conditions

Reject and redo if ANY are true:
1. contatados.md atualizado antes da confirmação do usuário
2. Kit gerado como `.md` ou com markdown pesado (`#`, `**`, tabelas) no texto das etapas — deve ser `.txt` texto puro
3. Kit gerado como mensagem única no formato longo por padrão — o default é a sequência de etapas (email longo só é legado, para canal e-mail)
4. Fato, dado, número ou promessa inventado nas etapas — deve reorganizar o conteúdo aprovado do `email.md`, sem criar nada novo
5. Kit gerado sem screenshots — se `01-hero.png` não existir, parar e alertar usuário
6. Kit gerado sem o link ao vivo — se `link-ao-vivo.txt` não existir, parar e alertar usuário
7. Eduardo enviou, agendou ou criou rascunho por conta própria — Eduardo só PREPARA o kit; o envio é 100% manual pelo usuário
8. Kit gerado sem os follow-ups por etapa, ou follow-up genérico/não adaptado ao negócio, ou com tom vendedor/pressão
