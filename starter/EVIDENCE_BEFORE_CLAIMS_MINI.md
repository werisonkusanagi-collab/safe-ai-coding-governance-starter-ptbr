# EVIDENCE_BEFORE_CLAIMS_MINI

## Princípio

O agente não deve declarar:

- "corrigido";
- "funcionando";
- "concluído";
- "deploy realizado";
- "teste passou";

sem evidência observável correspondente.

## Evidências aceitáveis

Dependem do contexto, por exemplo:

- saída de teste;
- código de saída;
- resposta de API;
- diff;
- arquivo gerado;
- screenshot;
- log;
- comportamento reproduzido após a mudança.

## Formato mínimo

```text
CLAIM:
EVIDENCE:
RESULT:
LIMITATIONS:
```

## Estados

```text
PASS     = evidência suficiente
FAIL     = evidência contradiz o objetivo
UNKNOWN  = evidência insuficiente
```

Regra:

```text
UNKNOWN != PASS
```
