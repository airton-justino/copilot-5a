# Regras de Negócio

## Convenções

- Cada regra possui um identificador único no formato **RN-XXX**.
- Regras ainda não confirmadas ou em discussão são marcadas com **"Ponto em aberto"**.
- Quando uma regra tiver exceções conhecidas, elas são listadas logo abaixo da regra.

---

## Gestão de Casos / Tickets

### RN-001 – Vinculação de Caso a Cliente

Todo caso aberto no Salesforce deve ser obrigatoriamente vinculado a uma **Conta** e a um **Contato** cadastrados no sistema.

- **Exceção:** **Ponto em aberto** — definir o comportamento quando o cliente não está cadastrado no momento da abertura do caso.

### RN-002 – Categorização de Casos

Todo caso deve ser classificado com pelo menos:

- **Tipo de caso** (ex.: dúvida, reclamação, solicitação, incidente)
- **Prioridade** (ex.: baixa, média, alta, crítica)

**Ponto em aberto:** Validar e confirmar a lista definitiva de tipos e prioridades com as áreas de negócio.

### RN-003 – Prazo de Resposta Inicial

**Ponto em aberto:** Definir os SLAs (tempos máximos de resposta e resolução) por prioridade de caso.

### RN-004 – Encerramento de Caso

Um caso só pode ser encerrado quando:

1. A solução tiver sido registrada no campo de resolução.
2. **Ponto em aberto:** Definir se é necessária confirmação do cliente para encerrar o caso.

### RN-005 – Reabertura de Caso

**Ponto em aberto:** Definir as condições sob as quais um caso encerrado pode ser reaberto e quem tem permissão para fazê-lo.

---

## Escalada

### RN-006 – Critérios de Escalada

**Ponto em aberto:** Definir os critérios que disparam a escalada de um caso (ex.: tempo sem resposta, tipo de problema, solicitação do cliente).

### RN-007 – Responsável pela Escalada

**Ponto em aberto:** Definir quem pode realizar a escalada e para quais grupos ou pessoas.

---

## Dados do Cliente

### RN-008 – Unicidade de Conta

Não devem existir duas contas no Salesforce para o mesmo cliente (mesma empresa ou mesmo CPF/CNPJ).

- **Exceção:** **Ponto em aberto** — definir o processo de deduplicação para registros legados migrados do Zendesk.

### RN-009 – Dados Obrigatórios no Cadastro de Contato

**Ponto em aberto:** Definir quais campos são obrigatórios no cadastro de um Contato no Salesforce (ex.: nome, e-mail, telefone, empresa).

---

## Integração Zendesk–Salesforce

### RN-010 – Sincronização de Tickets Existentes

**Ponto em aberto:** Definir se os tickets históricos do Zendesk serão migrados como casos no Salesforce e qual o recorte de data (ex.: últimos 12 meses, todos os tickets abertos, etc.).

### RN-011 – Conflito de Dados na Integração

**Ponto em aberto:** Definir qual sistema é a fonte oficial de verdade em caso de divergência de dados durante o período de coexistência dos dois sistemas.

---

## Visibilidade e Acesso

### RN-012 – Acesso do Time Comercial aos Casos

O time comercial deve ter acesso de **leitura** aos casos de suporte vinculados às contas que gerenciam, sem poder editar ou encerrar casos.

**Ponto em aberto:** Confirmar se há exceções ou perfis comerciais com acesso mais amplo.

### RN-013 – Restrição de Acesso a Dados Sensíveis

**Ponto em aberto:** Identificar se há campos ou informações nos casos de suporte que não devem ser visíveis para determinados perfis de usuário.
