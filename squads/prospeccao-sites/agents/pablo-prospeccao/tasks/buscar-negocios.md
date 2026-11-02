---
task: "Buscar Negócios no Google Maps"
order: 1
input:
  - cidade: Nome da cidade informada pelo usuário no checkpoint 1
  - contatados_recentes: Lista de negócios contatados nos últimos 30 dias (de contatados.md)
output:
  - lista_negocios: Lista de 5 negócios com todos os dados de contato coletados
---

# Buscar Negócios no Google Maps

Encontra 5 negócios locais sem site na cidade informada, coletando todos os dados públicos disponíveis. Filtra negócios já contatados nos últimos 30 dias.

## Process

1. **Ler contatados.md** — Extrair nomes de negócios com data nos últimos 30 dias. Criar lista de exclusão.

2. **Buscar no Google Maps via Apify ou web_search** — Pesquisar múltiplas categorias de negócios na cidade. Estratégia de busca:
   - "[categoria] em [cidade] sem site"
   - "[categoria] [cidade]" e verificar campo "site" no Maps manualmente
   - Categorias a variar: barbearia, restaurante, salão de beleza, clínica, academia, pet shop, lanchonete, padaria, hotel, farmácia, loja de roupas, cabeleireiro

3. **Filtrar negócios com site ativo** — Qualquer negócio que tenha URL preenchida no Maps é excluído. Sites em construção ou redirect para redes sociais contam como "sem site".

4. **Coletar dados de cada candidato**:
   - Nome completo do negócio (exatamente como aparece no Maps)
   - Telefone com DDD
   - Endereço completo
   - Nota média (ex: 4.7)
   - Número de avaliações (ex: 127)
   - Categoria/segmento

5. **Buscar email em fontes secundárias** para cada negócio sem email no Maps:
   - web_search: "[nome do negócio] [cidade] email contato"
   - web_fetch na página do Facebook se encontrado
   - web_search: "[nome do negócio] site:instagram.com" para bio com email
   - web_search: "[nome do negócio] solutudo.com.br"

6. **Aplicar filtro de exclusão** — Remover da lista qualquer negócio que esteja no contatados.md com data nos últimos 30 dias.

7. **Verificar canal de contato válido (WhatsApp OU email)** — Cada negócio precisa de WhatsApp público OU email público. Telefone fixo sozinho NÃO basta. DM de Instagram/Facebook, formulários web e "fale conosco" NÃO contam. Priorizar quem tem os DOIS (WhatsApp + email).
   - Negócio SEM WhatsApp/email mas promissor (boa nota, bom volume, nicho de ticket interessante) → registrar em `output/{run_id}/promissores-sem-contato.md`. NÃO entra na lista final, NÃO conta para a meta, NÃO é descartado. Buscar outro no lugar.
   - Negócio sem WhatsApp/email e sem destaque → simplesmente fora da lista, repor com outro candidato.

8. **Buscar com folga e repor até fechar a meta** — Buscar sempre mais candidatos do que 5 (7, 8, 9) porque parte cai no filtro de canal. Conforme candidatos caem, repor com novos até ter 5 qualificados com WhatsApp/email. Selecionar os 5 melhores priorizando: sem site + tem WhatsApp/email (idealmente os dois) + nota 4+ + mais avaliações. Diversificar nichos se possível.

## Output Format

```markdown
# Lista de Negócios — [Cidade] — [Data]

## Negócio 1: [Nome]
- Segmento: [categoria]
- Endereço: [endereço completo]
- Telefone: [telefone com DDD]
- Email: [email encontrado] OU "Não encontrado"
- WhatsApp: [número confirmado] OU "Não encontrado"
- Canal válido: [WhatsApp / email — qual(is) confirmado(s)]  (telefone fixo e DM não contam)
- Nota Google: [X.X ⭐] ([N] avaliações)
- Site: Nenhum
- Fonte do email: [Google Maps / Facebook / Instagram / Não encontrado]

## Negócio 2: [Nome]
[mesmos campos]

[... até negócio 5]

---
Nota: [N] negócios encontrados inicialmente. [N] excluídos por ter site ativo. [N] excluídos por contatados.md. [N] promissores sem WhatsApp/email → promissores-sem-contato.md.
```

## Promissores sem Contato (arquivo separado)

Salvar em `output/{run_id}/promissores-sem-contato.md`:

```markdown
# Promissores sem Contato — [Cidade] — [Data]

Negócios que valeriam a pena mas não têm WhatsApp/email público. Não foram descartados — você decide se quer perseguir o contato manualmente.

## [Nome do Negócio]
- Segmento: [categoria]
- Nota Google: [X.X ⭐] ([N] avaliações)
- Por que é promissor: [boa nota / bom volume / nicho de ticket alto]
- Canais tentados: [Maps, Facebook, Instagram, Solutudo... — todos sem WhatsApp/email]
- O que existe: [só telefone fixo / só DM / só formulário]
```

## Output Example

```markdown
# Lista de Negócios — Campinas — 2026-05-17

## Negócio 1: Barbearia Premium do Zé
- Segmento: Barbearia
- Endereço: Rua das Flores, 142 — Centro — Campinas/SP
- Telefone: (19) 99812-3456
- Email: contato@barbeariadoze.com.br (via Facebook)
- Nota Google: 4.8 ⭐ (127 avaliações)
- Site: Nenhum
- Fonte do email: Página do Facebook (localizada via web_search)

## Negócio 2: Restaurante Sabor da Vila
- Segmento: Restaurante nordestino
- Endereço: Av. Brasil, 890 — Cambui — Campinas/SP
- Telefone: (19) 3245-6789
- Email: Não encontrado
- Nota Google: 4.6 ⭐ (89 avaliações)
- Site: Nenhum
- Fonte do email: Não encontrado (tentadas: Maps, Facebook, Instagram, Solutudo)

## Negócio 3: Clínica Odontológica Sorriso Perfeito
- Segmento: Clínica odontológica
- Endereço: Rua Coronel Quirino, 215 — Cambuí — Campinas/SP
- Telefone: (19) 3523-1234
- Email: sorrisoperfeito.cps@gmail.com (via Google Maps)
- Nota Google: 4.9 ⭐ (68 avaliações)
- Site: Nenhum
- Fonte do email: Google Maps (campo email preenchido)

## Negócio 4: Academia Arte Marcial Centro
- Segmento: Academia de artes marciais
- Endereço: Rua Culto à Ciência, 78 — Centro — Campinas/SP
- Telefone: (19) 98765-4321
- Email: Não encontrado
- Nota Google: 4.7 ⭐ (43 avaliações)
- Site: Nenhum

## Negócio 5: Pet Shop Quatro Patas
- Segmento: Pet shop e clínica veterinária
- Endereço: Rua José Paulino, 1200 — Bonfim — Campinas/SP
- Telefone: (19) 99234-5678
- Email: quatropatas.camp@gmail.com (via Instagram bio)
- Nota Google: 4.5 ⭐ (56 avaliações)
- Site: Nenhum
- Fonte do email: Bio do Instagram @quatropatas_campinas

---
Nota: 23 negócios encontrados inicialmente. 18 excluídos por ter site ativo. 0 excluídos por contatados.md.
```

## Quality Criteria

- [ ] 5 negócios qualificados entregues (buscou com folga e repôs quem caiu)
- [ ] Nenhum negócio com site ativo na lista
- [ ] Nenhum negócio do contatados.md (últimos 30 dias)
- [ ] Todos os 5 têm WhatsApp OU email público — nenhum só-DM, só-formulário ou só-telefone-fixo
- [ ] Promissores sem WhatsApp/email registrados em promissores-sem-contato.md (não descartados)
- [ ] Email coletado para pelo menos 3 dos 5 negócios
- [ ] Fonte de cada dado registrada (de onde veio cada informação)
- [ ] Nota de quantos foram encontrados e filtrados incluída

## Veto Conditions

Reject and redo if ANY are true:
1. Algum negócio da lista tem site ativo funcionando
2. Algum negócio foi contatado nos últimos 30 dias e está no contatados.md
3. Algum negócio da lista NÃO tem WhatsApp nem email público (só telefone fixo, só DM ou só formulário)
4. Negócio promissor sem WhatsApp/email descartado em vez de registrado em promissores-sem-contato.md
