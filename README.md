# Repositório corporativo `.github`

Este repositório centraliza os padrões compartilhados da organização Ouro Safra no GitHub.

## Objetivos

- Padronizar a abertura de Issues e Pull Requests.
- Publicar orientações corporativas de contribuição, segurança e suporte.
- Manter o perfil público ou interno da organização.
- Definir responsáveis pelos arquivos de governança.
- Reduzir duplicação de arquivos entre repositórios.

## Escopo desta entrega

Esta versão contém:

- perfil da organização;
- templates de Issue;
- template de Pull Request;
- política de contribuição;
- política de segurança;
- orientação de suporte;
- conduta de colaboração;
- aviso de propriedade;
- CODEOWNERS do repositório.

Os workflows reutilizáveis de CI/CD não ficam neste repositório. Eles serão mantidos em:

`ouro-safra/platform-github-workflows`

## Estrutura

```text
.github/
├── .github/
│   ├── CODEOWNERS
│   ├── ISSUE_TEMPLATE/
│   │   ├── config.yml
│   │   ├── epic.yml
│   │   ├── feature.yml
│   │   ├── task.yml
│   │   ├── bug.yml
│   │   ├── incident.yml
│   │   ├── problem.yml
│   │   ├── tech-debt.yml
│   │   ├── security.yml
│   │   └── spike.yml
│   └── pull_request_template.md
├── profile/
│   └── README.md
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── NOTICE.md
├── SECURITY.md
└── SUPPORT.md
```

## Aplicação dos arquivos

Os arquivos compartilhados deste repositório são utilizados como padrão pelos repositórios da organização que não possuam uma versão local equivalente.

Um repositório pode manter uma versão própria quando houver necessidade técnica ou operacional específica. A exceção deve preservar os controles mínimos e ser registrada em uma Issue ou ADR.

## Responsáveis

- Manutenção: `@ouro-safra/platform-admins`
- Segurança: `@ouro-safra/security-reviewers`
- Aprovação de mudanças de governança: Organization Owners e fórum de governança do GitHub

## Processo de alteração

1. Abrir uma Issue descrevendo a necessidade.
2. Criar uma branch vinculada à Issue.
3. Abrir Pull Request.
4. Obter revisão dos CODEOWNERS.
5. Validar o impacto nos repositórios da organização.
6. Registrar a mudança no `CHANGELOG.md`.
7. Realizar merge por squash.

## Versionamento

As alterações relevantes deste repositório devem ser identificadas no `CHANGELOG.md`.

Mudanças incompatíveis nos templates devem ser comunicadas antes da ativação.
