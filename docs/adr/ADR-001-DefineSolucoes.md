# ADR001 — Escolha da Solução de Arquitetura e Stack Tecnológica para o Connexa

- **Situação:** proposta
- **Data:** 2026-11-01
- **Participantes:** corarruda

## Contexto

Necessidade de definir a solução de arquitetura e as stacks tecnológicas a serem utilizadas no projeto Connexa, considerando os recursos disponíveis.

## Decisão

Decidido adotar o template em Java como base para a arquitetura do Connexa, estruturado em uma arquitetura monolítica modular (Modular Monolith) com fronteiras claras entre os territórios de domínio e suíte de testes automatizados integrada no pipeline de CI.

## Alternativas consideradas

| Alternativa | Por que não foi escolhida |
| template em Node | Menor domínio da equipe |
| template em .NET  | Não familiaridade com a linguagem |
| Arquitetura de Microsserviços  | Desnecessariamente complexo para o projeto |

## Consequências

- **Positivas:** Aproveitamento completo da infraestrutura fornecida no template connexa-modelo-java (scripts de verificação de fronteiras entre módulos e pipeline de CI).
- **Negativas:** Maior verbosidade de código em comparação com staks dinâmicas, exigindo disciplina no cumprimento das regras do AGENTS.md para manter as classes e módulos coesos.
- **Como verificar:** Validação obrigatória dos checks de CI (testes automatizados e análise de fronteiras entre módulos) em todos os Pull Requests direcionados ao branch main.
