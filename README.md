# Repositório de Apoio Funcional – Projetos Salesforce (5A)

Base de contexto funcional e instruções para uso do GitHub Copilot em projetos Salesforce e migração de processos do Zendesk para Salesforce no 5A.

## Objetivo

Este repositório centraliza o conhecimento de negócio necessário para:

- Armazenar e preservar o contexto funcional dos projetos Salesforce
- Documentar os fluxos operacionais (AS-IS e TO-BE)
- Registrar e manter as regras de negócio vigentes
- Documentar as integrações entre Zendesk e Salesforce
- Orientar o GitHub Copilot com instruções claras e objetivas

## Estrutura do Repositório

```
.
├── .github/
│   └── copilot-instructions.md   # Instruções de comportamento para o GitHub Copilot
├── docs/
│   ├── contexto-negocio.md       # Contexto geral do negócio e dos projetos
│   ├── fluxos-operacionais.md    # Fluxos AS-IS e TO-BE dos processos
│   ├── regras-negocio.md         # Regras de negócio documentadas
│   ├── integracoes.md            # Integrações entre Zendesk e Salesforce
│   └── glossario.md              # Glossário de termos e siglas
└── README.md                     # Este arquivo
```

## Como Usar

1. Consulte `docs/contexto-negocio.md` para entender o cenário geral do projeto.
2. Consulte `docs/fluxos-operacionais.md` para visualizar os processos atuais e futuros.
3. Consulte `docs/regras-negocio.md` antes de implementar qualquer lógica funcional.
4. Consulte `docs/integracoes.md` para entender as trocas de dados entre sistemas.
5. As instruções ao Copilot estão em `.github/copilot-instructions.md`.

## Convenções

- Todo ponto ainda não definido é marcado como **"Ponto em aberto"**.
- Todo o conteúdo está em **português do Brasil**.
- O foco é **funcional e de negócio** — detalhes técnicos só aparecem quando indispensáveis.

