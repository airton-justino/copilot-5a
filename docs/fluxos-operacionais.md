# Fluxos Operacionais

## Convenções

- **AS-IS:** Fluxo atual, como o processo funciona hoje.
- **TO-BE:** Fluxo futuro, como o processo deverá funcionar após a migração/integração.
- **Ponto em aberto:** Etapa ou decisão ainda não definida.

---

## Fluxo 1 – Abertura de Ticket de Suporte

### AS-IS (Situação Atual)

1. Cliente entra em contato pelo canal de atendimento (e-mail, chat ou telefone).
2. O atendente abre um ticket manualmente no **Zendesk**.
3. O ticket é categorizado por tipo de problema e prioridade.
4. O atendente resolve o ticket ou o escala para o nível técnico.
5. Após resolução, o ticket é fechado no Zendesk.
6. **Não há sincronização automática** com o Salesforce — o time comercial não tem visibilidade dos tickets de suporte.

### TO-BE (Situação Futura)

1. Cliente entra em contato pelo canal de atendimento.
2. O atendente registra o caso no **Salesforce Service Cloud** (ou o caso é criado automaticamente via integração).
3. O caso é categorizado e vinculado à **Conta** e ao **Contato** correspondentes no Salesforce.
4. O time comercial passa a ter visibilidade dos casos de suporte do cliente diretamente no Salesforce.
5. Após resolução, o caso é encerrado e o histórico fica consolidado no perfil do cliente.

**Ponto em aberto:** Definir se o Zendesk continuará recebendo novos tickets em paralelo durante o período de transição.

---

## Fluxo 2 – Escalada de Ticket

### AS-IS (Situação Atual)

1. O atendente identifica que o ticket requer atenção especializada.
2. O ticket é reatribuído manualmente para outro grupo ou agente no Zendesk.
3. **Ponto em aberto:** Descrever o processo de comunicação durante a escalada.
4. O agente escalado resolve o ticket e registra a solução no Zendesk.

### TO-BE (Situação Futura)

**Ponto em aberto:** Mapear como o processo de escalada funcionará no Salesforce e se haverá regras de atribuição automática.

---

## Fluxo 3 – Consulta de Histórico do Cliente

### AS-IS (Situação Atual)

1. O time comercial precisa consultar o histórico de atendimento de um cliente.
2. É necessário acessar o Zendesk separadamente e buscar os tickets pelo e-mail do cliente.
3. O cruzamento de informações com o CRM (Salesforce) é feito manualmente.

### TO-BE (Situação Futura)

1. O time comercial acessa o perfil da **Conta** no Salesforce.
2. Todos os casos de suporte do cliente aparecem diretamente no perfil, sem necessidade de acessar outro sistema.

---

## Fluxo 4 – Criação de Conta/Contato a partir de Novo Ticket

### AS-IS (Situação Atual)

**Ponto em aberto:** Descrever como novos clientes são cadastrados no Zendesk e se há algum processo de sincronização com o Salesforce.

### TO-BE (Situação Futura)

**Ponto em aberto:** Definir se a criação de um novo caso no Salesforce deverá criar automaticamente uma Conta/Contato inexistente, ou se isso será feito manualmente pelo atendente.

---

## Fluxo 5 – Relatórios e Indicadores de Atendimento

### AS-IS (Situação Atual)

- Relatórios de atendimento são extraídos do Zendesk.
- **Ponto em aberto:** Descrever quais relatórios são gerados hoje e qual a frequência.

### TO-BE (Situação Futura)

**Ponto em aberto:** Definir quais dashboards e relatórios serão construídos no Salesforce para substituir os relatórios atuais do Zendesk.
