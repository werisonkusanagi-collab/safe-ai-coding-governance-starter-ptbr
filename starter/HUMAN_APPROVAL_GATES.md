# HUMAN_APPROVAL_GATES — Starter

Use gates antes de ações com impacto relevante.

## GATE 1 — Escopo

Antes da implementação:

- [ ] objetivo entendido;
- [ ] arquivos/áreas afetadas identificados;
- [ ] ações fora do escopo bloqueadas.

## GATE 2 — Ação destrutiva

Antes de excluir, sobrescrever ou executar ação difícil de reverter:

- [ ] impacto descrito;
- [ ] alternativa reversível considerada;
- [ ] rollback disponível;
- [ ] aprovação humana explícita recebida.

Sem aprovação:

```text
STOP
```

## GATE 3 — Mudança externa

Antes de qualquer ação que produza efeito fora do ambiente local:

- [ ] destino identificado;
- [ ] conteúdo/alteração revisado;
- [ ] autoridade confirmada;
- [ ] aprovação humana obtida.

## GATE 4 — Release

Antes de declarar pronto:

- [ ] testes relevantes executados;
- [ ] resultado observado;
- [ ] regressões críticas verificadas;
- [ ] evidência registrada;
- [ ] rollback conhecido.
