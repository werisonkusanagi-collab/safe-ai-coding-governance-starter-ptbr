# PRE_CHANGE_CHECKLIST — Starter

Execute antes de qualquer alteração relevante.

## Contexto

- [ ] Qual é o objetivo?
- [ ] Qual é o estado atual?
- [ ] Quais arquivos/serviços serão afetados?
- [ ] Existe dependência oculta conhecida?

## Autoridade

- [ ] A ação está explicitamente autorizada?
- [ ] Há necessidade de aprovação humana?
- [ ] O agente está dentro do escopo definido?

## Reversibilidade

- [ ] Existe backup, branch, snapshot ou outro mecanismo de rollback?
- [ ] O estado anterior pode ser restaurado?
- [ ] A mudança pode ser aplicada incrementalmente?

## Validação

- [ ] Existe um teste ou evidência que confirme o resultado?
- [ ] O critério de sucesso está definido antes da mudança?
- [ ] Falha ou resultado desconhecido será tratado como falha?

## Regra

Se qualquer item crítico permanecer desconhecido:

```text
DO_NOT_PROCEED
STATUS: BLOCKED
```
