# Integrações

## Visão Geral

Este documento descreve as integrações existentes e planejadas entre o **Zendesk** e o **Salesforce** no contexto dos projetos da empresa 5A.

---

## Integração 1 – Zendesk → Salesforce (Migração de Tickets)

### Objetivo

Migrar os tickets históricos do Zendesk para o Salesforce como **Casos** (Cases), preservando o histórico de atendimento dos clientes.

### Dados Migrados

| Campo no Zendesk         | Campo no Salesforce       | Observação                         |
|--------------------------|---------------------------|------------------------------------|
| Ticket ID                | Número do Caso / Campo externo | Manter referência cruzada     |
| Assunto                  | Assunto do Caso           |                                    |
| Descrição                | Descrição do Caso         |                                    |
| Status                   | Status do Caso            | **Ponto em aberto:** mapear status |
| Prioridade               | Prioridade do Caso        | **Ponto em aberto:** mapear valores|
| Data de criação          | Data de criação           |                                    |
| Data de encerramento     | Data de encerramento      |                                    |
| Solicitante (e-mail)     | Contato vinculado         | Requer correspondência de e-mail   |
| Organização              | Conta vinculada           | Requer correspondência de nome/CNPJ|
| Comentários/Histórico    | **Ponto em aberto**       | Definir se serão migrados          |
| Anexos                   | **Ponto em aberto**       | Definir política de migração       |

### Critérios de Seleção dos Tickets a Migrar

**Ponto em aberto:** Definir o recorte de dados a ser migrado (ex.: todos os tickets abertos, tickets dos últimos 12 meses, todos os tickets).

### Tratamento de Dados Não Correspondentes

**Ponto em aberto:** Definir o que acontece quando um ticket do Zendesk não encontra um Contato ou Conta correspondente no Salesforce (criar registro novo, ignorar, colocar em quarentena para revisão manual).

---

## Integração 2 – Zendesk ↔ Salesforce (Sincronização em Tempo Real)

### Objetivo

Durante o período de coexistência dos dois sistemas, manter os dados sincronizados para que atendentes no Zendesk e equipe comercial no Salesforce vejam as mesmas informações.

### Direção do Fluxo

**Ponto em aberto:** Definir a direção da sincronização:
- Unidirecional (Zendesk → Salesforce)?
- Bidirecional (ambos os sistemas se atualizam mutuamente)?

### Frequência de Sincronização

**Ponto em aberto:** Definir se a sincronização será em tempo real (via webhooks/eventos), near real-time (a cada X minutos) ou em lotes (batch diário/semanal).

### Eventos que Disparam Sincronização

**Ponto em aberto:** Listar os eventos que deverão disparar a sincronização (ex.: novo ticket criado, ticket atualizado, ticket encerrado, novo cliente cadastrado).

---

## Integração 3 – Salesforce → Zendesk (Dados de Conta e Contato)

### Objetivo

**Ponto em aberto:** Avaliar se os dados de Conta e Contato do Salesforce devem ser enviados ao Zendesk para enriquecer o cadastro de usuários e organizações no sistema de atendimento.

---

## Considerações Gerais

### Autenticação e Segurança

**Ponto em aberto:** Definir o mecanismo de autenticação utilizado nas integrações (OAuth 2.0, API Keys, etc.) e as políticas de segurança para tráfego de dados entre os sistemas.

### Tratamento de Erros

**Ponto em aberto:** Definir como serão tratados erros de integração (ex.: registro de logs, notificação para a equipe, retentativas automáticas).

### Ambiente de Homologação

**Ponto em aberto:** Confirmar se haverá ambientes de sandbox/homologação para testar as integrações antes de ir para produção.
