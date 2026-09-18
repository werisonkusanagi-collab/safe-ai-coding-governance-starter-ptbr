---
title: "Como impedir que um agente de programação faça mudanças destrutivas sem aprovação humana"
published: false
description: "Uma estrutura mínima de autoridade, gates humanos, rollback e evidência para projetos com agentes de programação."
tags: ai, programming, agents, safety
---

# Como impedir que um agente de programação faça mudanças destrutivas sem aprovação humana

Agentes de programação reduzem drasticamente o tempo entre uma intenção e uma alteração real no projeto.

Esse ganho também muda o tipo de risco.

Quando um agente consegue editar dezenas de arquivos, executar comandos, instalar dependências ou alterar configuração em poucos segundos, a pergunta deixa de ser apenas:

> “Ele consegue fazer?”

e passa a ser:

> “Ele tinha autoridade para fazer isso?”

Uma estrutura mínima de governança pode reduzir essa ambiguidade sem transformar cada alteração em burocracia.

## 1. Autoridade deve ser explícita

Uma regra útil é:

```text
Ausência de proibição não significa autorização.
```

Separe as ações em três grupos:

### Autônomas

Ações reversíveis e de baixo impacto, como:

- ler código;
- analisar erros;
- elaborar planos;
- executar testes existentes;
- propor patches.

### Com aprovação humana

Ações como:

- excluir arquivos;
- alterar dependências;
- modificar produção;
- fazer deploy;
- publicar conteúdo;
- alterar permissões;
- executar operações destrutivas.

### Fora de escopo

Quando a autoridade não está definida:

```text
STATUS: BLOCKED
REASON: AUTHORITY_UNDEFINED
NEXT: REQUEST_HUMAN_APPROVAL
```

## 2. Ações destrutivas precisam de um gate

Antes de uma ação difícil de reverter, o agente deve demonstrar quatro coisas:

1. qual é o impacto;
2. qual é o caminho de rollback;
3. por que a ação é necessária;
4. que recebeu aprovação humana explícita.

Sem esses quatro elementos, a execução para.

Isso é diferente de simplesmente pedir “tenha cuidado”.

O gate transforma cuidado em uma condição verificável.

## 3. Rollback vem antes da mudança

Uma mudança segura não começa pelo patch.

Ela começa respondendo:

> “Como voltamos ao estado anterior se isso der errado?”

Dependendo do projeto, rollback pode significar:

- branch;
- commit;
- snapshot;
- backup;
- arquivo de configuração anterior;
- migration reversível;
- feature flag.

Se não existe rollback e o impacto é relevante, o risco precisa subir de nível antes da execução.

## 4. “Concluído” exige evidência

Um dos erros mais comuns em fluxos com agentes é transformar ausência de erro visível em sucesso.

Uma regra simples:

```text
UNKNOWN != PASS
```

O agente só deve declarar uma alteração como concluída quando houver evidência observável.

Por exemplo:

```text
CLAIM: bug corrigido
EVIDENCE: teste X passou + reprodução original não ocorre
RESULT: PASS
LIMITATIONS: não validado em produção
```

Isso força a separação entre:

- implementação;
- validação;
- declaração de sucesso.

## 5. Use um ciclo previsível

Um fluxo pequeno já ajuda bastante:

```text
PLAN → IMPLEMENT → VALIDATE → RELEASE
```

**PLAN** define escopo, autoridade e risco.

**IMPLEMENT** executa apenas o que foi autorizado.

**VALIDATE** procura evidência e regressões.

**RELEASE** só ocorre quando os gates relevantes foram satisfeitos.

## Starter gratuito

Preparei um starter PT-BR com quatro arquivos pequenos:

- `AGENT_AUTHORITY_POLICY.md`
- `HUMAN_APPROVAL_GATES.md`
- `PRE_CHANGE_CHECKLIST.md`
- `EVIDENCE_BEFORE_CLAIMS_MINI.md`

Link do repositório: **[ADICIONAR_URL_DO_GITHUB_APÓS_PUBLICAÇÃO]**

## Kit completo

Para quem precisa de uma estrutura reutilizável mais ampla, o **Kit de Codificação Segura com IA — Governança de Agentes** inclui manual, guia rápido, policies, templates, workflows, checklists, exemplos, `AGENTS.md`, `CLAUDE.md`, rollback, regression validation e multi-agent review.

**Página do produto:** https://kit-codificacao-segura-ia-governanca.lovable.app

Preço atual: **R$ 39,90**, pagamento único.

---

Este material é uma camada de governança operacional. Ele não substitui permissões, sandboxing, backups, branch protection, gestão de credenciais, testes ou revisão técnica adequados ao risco do ambiente.
