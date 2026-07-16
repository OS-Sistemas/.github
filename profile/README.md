# Tecnologia Ouro Safra

Este espaço concentra os repositórios corporativos utilizados pelos times de Desenvolvimento, RPA, Dados e Plataforma.

## Núcleos lógicos

- **SGI-Frontend:** aplicações web, componentes e pacotes de frontend.
- **SGI-Backend:** APIs, serviços Python e componentes de backend.
- **JOBS:** automações, RPAs, pipelines de dados e rotinas agendadas.
- **Platform:** templates, workflows, infraestrutura como código e padrões corporativos.

## Times

- `@ouro-safra/dev`
- `@ouro-safra/rpa`
- `@ouro-safra/dados`
- `@ouro-safra/platform-admins`
- `@ouro-safra/security-reviewers`
- `@ouro-safra/production-approvers`

## Fluxo de trabalho

Toda mudança relevante deve seguir esta trilha:

```text
Issue → branch → Pull Request → CI e revisão → release → deploy → evidência
```

As branches protegidas não recebem push direto. Alterações são integradas por Pull Request e devem passar pelos checks definidos para cada repositório.

## Segurança

Não armazene senhas, tokens, chaves privadas, wallets, arquivos `.env` reais ou dados pessoais desnecessários no Git.

Consulte a política corporativa em `SECURITY.md`.
