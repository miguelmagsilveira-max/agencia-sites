# Quality Criteria — Prospecção de Sites

## Critérios por Agente

### Pablo Prospecção — Coleta de Negócios
- [ ] 5 negócios coletados (ou menos se não houver suficientes sem site)
- [ ] Nenhum negócio com site ativo na lista
- [ ] Nenhum negócio do contatados.md (últimos 30 dias) na lista
- [ ] Todos os campos preenchidos: nome, telefone, segmento, nota, nº avaliações, endereço
- [ ] Email coletado para pelo menos 3 dos 5 negócios
- [ ] Dados de fonte pública verificável (Google Maps, Facebook, etc.)

### Roberto Rastro — Investigação Digital
- [ ] Todos os 5 negócios investigados em pelo menos 1 plataforma além do Maps
- [ ] Avaliações copiadas literalmente (texto exato, nome do avaliador se disponível)
- [ ] Ausência de dados registrada explicitamente ("sem Instagram encontrado")
- [ ] Identidade visual mapeada para cada negócio (cores, estilo)
- [ ] Plataformas verificadas: Facebook, Instagram, TripAdvisor, Restaurant Guru, Solutudo

### André Análise — Briefing e Score
- [ ] Todos os 8 pontos do briefing preenchidos para cada negócio
- [ ] Score de 0-10 calculado com justificativa por critério
- [ ] Todos os 5 negócios apresentados ao usuário (sem descarte automático)
- [ ] Avaliações reais do Pesquisador integradas no ponto 8
- [ ] Score baseado apenas nos critérios objetivos definidos (não em opinião)

### Diego Digital — Site HTML
- [ ] HTML único autocontido (CSS em `<style>` interno)
- [ ] `<meta viewport>` presente (mobile-first)
- [ ] Avaliações reais do briefing incluídas literalmente no HTML
- [ ] Botão WhatsApp flutuante com número real do negócio
- [ ] Google Maps embed com endereço real
- [ ] Design adaptado ao nicho (não genérico)
- [ ] Arquivo salvo em output/{run_id}/{negocio}/site.html
- [ ] Carregamento esperado < 3 segundos (sem recursos externos além de Google Fonts + Maps)

### Carlos Carta — Email de Proposta
- [ ] 60-100 palavras no corpo do email
- [ ] Elogio genuíno baseado em avaliação ou característica real do briefing
- [ ] Problema plantado específico ao nicho do negócio
- [ ] Exatamente 1 CTA de baixo compromisso (pergunta)
- [ ] Assunto de 4-7 palavras, sem caixa alta, sem emoji
- [ ] Formato plain text (sem HTML)
- [ ] Arquivo salvo em output/{run_id}/{negocio}/email.md

### Vera Veredito — Revisão
- [ ] Verificação explícita de avaliações reais (HTML == briefing)
- [ ] Nome do negócio correto em HTML e email
- [ ] WhatsApp com número real verificado
- [ ] Email dentro do limite de palavras (60-100)
- [ ] CTA do email é pergunta (não afirmação ou comando)
- [ ] Veredicto claro: APROVADO ou REJEITADO
- [ ] Feedback acionável em caso de rejeição

### Eduardo Envio — Kit de Envio
- [ ] kit-envio.txt (texto puro) gerado com canal e destino corretos
- [ ] Kit na sequência de etapas informal (ETAPA 1 → [AGUARDE] → ETAPA 3 → [AGUARDE] → ETAPA 5), sem markdown pesado
- [ ] Etapas reorganizam o conteúdo do email.md aprovado, sem inventar fato/dado
- [ ] Link ao vivo e caminhos dos screenshots incluídos na ETAPA 5
- [ ] Follow-up de até 3 toques (LEU/NÃO LEU), seção de fechamento/objeções e pergunta pós-visualização incluídos no kit
- [ ] contatados.md atualizado SÓ após confirmação do usuário

---

## Critérios do Pipeline

### Checkpoints
- [ ] Cada checkpoint apresenta todos os dados do passo anterior
- [ ] Nenhum passo avança sem confirmação explícita do usuário
- [ ] Checkpoint final mostra: briefing + site (preview) + email para todos os negócios

### Memória
- [ ] contatados.md atualizado após cada rodada completada
- [ ] Negócios do contatados.md (últimos 30 dias) filtrados na próxima rodada
- [ ] Campos registrados: negócio, cidade, data_contato, email_enviado, resultado

### Output Structure
- [ ] Pasta output/{run_id}/ criada para cada rodada
- [ ] Subpasta por negócio com: briefing.md, site.html, email.md
- [ ] relatorio-rodada.md com resumo dos 5 negócios processados

---

## Thresholds de Aprovação (Vera Veredito)

| Score | Veredicto |
|---|---|
| Todos os critérios atendidos | APROVADO |
| 1 critério crítico falhou (avaliação inventada, nome errado, sem WhatsApp) | REJEITADO |
| Critérios menores falharam (design poderia ser melhor, email um pouco longo) | APROVADO com sugestões |
| Múltiplos critérios falharam | REJEITADO com lista de correções |
