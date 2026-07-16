# Política de segurança

## Escopo

Esta política se aplica aos códigos, automações, pipelines, infraestrutura como código, imagens, pacotes e documentos técnicos mantidos na organização Ouro Safra.

## Como reportar

Não publique vulnerabilidades ativas, credenciais, chaves, tokens ou dados sensíveis em Issues comuns.

Reporte pelo canal interno definido pela Segurança da Informação:

`<canal-interno-de-seguranca>`

Inclua, quando possível:

- repositório e componente;
- ambiente afetado;
- descrição objetiva;
- impacto observado ou potencial;
- evidências sem expor segredos;
- passos de reprodução;
- versão ou commit;
- ação emergencial já executada.

## Tratamento de segredos

Quando um segredo entrar no Git, ele deve ser considerado comprometido.

A ordem de resposta é:

1. revogar ou rotacionar;
2. restringir impacto;
3. verificar uso indevido;
4. remover do código;
5. limpar o histórico, quando necessário;
6. registrar o incidente e as ações preventivas.

Somente apagar o arquivo ou o commit não é suficiente.

## Severidades

| Severidade | Exemplo | Tratamento |
|---|---|---|
| Critical | RCE, segredo ativo de produção, bypass de autenticação | Bloquear release e tratar imediatamente |
| High | Escalada de privilégio, injeção relevante, dependência explorável | Bloquear produção, salvo exceção formal |
| Medium | Risco condicionado ou impacto moderado | Planejar correção com prazo definido |
| Low | Hardening ou risco residual baixo | Manter no backlog com revisão periódica |

## Requisitos mínimos

- dependências verificadas;
- secrets ausentes do Git;
- Actions externas revisadas e fixadas por SHA;
- permissões mínimas do `GITHUB_TOKEN`;
- código não confiável sem acesso a secrets;
- runners privados protegidos;
- vulnerabilidades com owner, severidade e prazo;
- imagens e artefatos críticos verificados.

## Divulgação

Achados internos não devem ser divulgados externamente sem autorização formal da Segurança da Informação e das áreas responsáveis.
