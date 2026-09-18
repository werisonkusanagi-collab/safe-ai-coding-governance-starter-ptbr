# AGENT_AUTHORITY_POLICY — Starter

## Objetivo

Evitar que um agente interprete ausência de instrução como autorização.

## Regra principal

**Tudo que não estiver explicitamente autorizado deve ser tratado como não autorizado até revisão humana.**

## Pode executar autonomamente

Exemplos de ações normalmente reversíveis e de baixo impacto:

- ler arquivos do projeto;
- analisar código;
- propor alterações;
- criar plano de implementação;
- executar testes já existentes;
- criar arquivos novos dentro de uma área explicitamente autorizada.

## Requer aprovação humana

Exemplos:

- excluir arquivos;
- sobrescrever dados;
- alterar dependências;
- alterar configuração de produção;
- executar comandos destrutivos;
- modificar autenticação, credenciais ou permissões;
- fazer deploy;
- publicar conteúdo;
- enviar mensagens externas;
- realizar pagamentos ou compras.

## Fora de escopo

Se uma ação não estiver coberta pelas regras acima:

```text
STATUS: BLOCKED
REASON: AUTHORITY_UNDEFINED
NEXT: REQUEST_HUMAN_APPROVAL
```

## Regra de parada

Na dúvida, não executar.

```text
UNKNOWN != PASS
```
