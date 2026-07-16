# Guia de contribuição

## 1. Antes de iniciar

Toda mudança relevante deve estar vinculada a uma Issue.

A Issue deve conter:

- problema ou objetivo;
- resultado esperado;
- critérios de aceite;
- sistema ou componente;
- time responsável;
- prioridade;
- risco, quando aplicável;
- ticket interno relacionado durante a transição.

Não inicie desenvolvimento relevante somente por mensagem, reunião ou solicitação verbal.

## 2. Branches

Modelo transitório:

- `main`: versão liberável e produção;
- `develop`: integração, DEV/N2 e preparação de release.

Padrões de nome:

```text
feature/<issue>-<descricao-curta>
fix/<issue>-<descricao-curta>
hotfix/<issue>-<descricao-curta>
infra/<issue>-<descricao-curta>
docs/<issue>-<descricao-curta>
spike/<issue>-<descricao-curta>
```

Exemplos:

```text
feature/123-aprovacao-contrato
fix/456-validacao-token
docs/789-runbook-rollback
```

## 3. Commits

Utilize Conventional Commits.

Exemplos:

```text
feat(api): adicionar consulta de contratos
fix(auth): impedir refresh com token expirado
test(documents): cobrir inscrição estadual vazia
chore(deps): atualizar dependência vulnerável
docs(runbook): documentar rollback do serviço
```

Evite mensagens genéricas como `update`, `ajuste`, `teste` ou `correções diversas`.

## 4. Pull Requests

O Pull Request deve:

- referenciar a Issue;
- explicar contexto e alterações;
- informar como validar;
- descrever riscos e ambientes afetados;
- avaliar migração, configuração e rollback;
- apresentar evidências;
- permanecer com escopo revisável.

Abra Draft PR quando a mudança exigir colaboração antecipada.

## 5. Revisão

O autor não substitui a revisão independente.

Antes do merge:

- todos os checks obrigatórios devem estar aprovados;
- todos os comentários devem estar resolvidos;
- a aprovação de CODEOWNERS deve ser obtida quando exigida;
- novos commits podem invalidar aprovações anteriores;
- mudanças sensíveis podem exigir dois revisores.

## 6. Segurança

É proibido versionar:

- arquivos `.env` reais;
- senhas e tokens;
- chaves privadas;
- wallets;
- certificados com chave privada;
- credenciais de banco;
- dados pessoais desnecessários;
- dumps produtivos não mascarados.

Ao identificar segredo exposto:

1. revogue ou rotacione a credencial;
2. comunique Segurança;
3. investigue possível uso indevido;
4. remova o conteúdo;
5. limpe o histórico quando necessário.

## 7. Merge

O padrão para feature e correção é squash merge.

Branches temporárias devem ser excluídas após o merge.

Push direto, force push e exclusão de `develop` e `main` são proibidos fora do procedimento formal de exceção.

## 8. Exceções

Toda exceção deve possuir:

- Issue;
- justificativa;
- risco;
- aprovador;
- controle compensatório;
- data de expiração;
- ação corretiva.

Bypass emergencial exige revisão no próximo dia útil.
