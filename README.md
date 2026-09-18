# Safe AI Coding Governance Starter — PT-BR

Starter gratuito para projetos que usam agentes de programação com IA.

Este repositório demonstra uma estrutura **mínima** para reduzir ambiguidade operacional antes de permitir que um agente altere código, arquivos, configuração ou infraestrutura.

> Produto completo: **Kit de Codificação Segura com IA — Governança de Agentes**  
> Preço atual: **R$ 39,90** — pagamento único  
> Página de vendas: https://kit-codificacao-segura-ia-governanca.lovable.app

## O problema

Agentes de programação podem executar mudanças rapidamente, mas velocidade sem limites explícitos cria riscos:

- alterações destrutivas;
- ações fora do escopo;
- declarações de sucesso sem evidência;
- mudanças difíceis de reverter;
- decisões irreversíveis sem aprovação humana.

Este starter cobre apenas o núcleo mínimo.

## Conteúdo gratuito

```text
starter/
├── AGENT_AUTHORITY_POLICY.md
├── HUMAN_APPROVAL_GATES.md
├── PRE_CHANGE_CHECKLIST.md
└── EVIDENCE_BEFORE_CLAIMS_MINI.md
```

## Ciclo recomendado

```text
PLAN → IMPLEMENT → VALIDATE → RELEASE
```

## Como usar

1. Copie os arquivos de `starter/` para o seu projeto.
2. Adapte nomes, escopo e comandos à sua realidade.
3. Defina explicitamente o que o agente pode fazer sozinho.
4. Defina quais ações exigem aprovação humana.
5. Antes de declarar sucesso, exija evidência observável.
6. Preserve um caminho de rollback antes de mudanças de risco relevante.

## O que este starter NÃO é

- não é uma nova IA;
- não instala nem controla um agente;
- não substitui permissões, sandboxing, backups, branch protection, gestão de credenciais, revisão de código ou testes;
- não oferece garantia absoluta contra falhas;
- não contém o pacote comercial completo.

## Versão completa

O produto completo adiciona uma estrutura mais ampla com:

- manual completo;
- guia rápido;
- policies adicionais;
- templates reutilizáveis;
- workflows;
- checklists;
- exemplos;
- `AGENTS.md`;
- `CLAUDE.md`;
- decision/change/bug/handoff logs;
- rollback e regression validation;
- multi-agent review;
- regras `fail-closed` e `UNKNOWN != PASS`.

**Ver o kit completo:** https://kit-codificacao-segura-ia-governanca.lovable.app

## Compatibilidade

A estrutura é independente de modelo e pode ser adaptada para agentes de programação como Codex, Claude Code, Cursor e equivalentes capazes de seguir instruções de projeto.

Codex, Claude Code e Cursor são marcas de seus respectivos proprietários. Este starter não é afiliado, patrocinado ou endossado por essas empresas.

## Licença do starter

Consulte `LICENSE.md`.
