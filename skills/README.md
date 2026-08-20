# skills (próprias)

Skills originais, criadas do zero por mim. Cada pasta abaixo é uma skill completa (com `SKILL.md`, `references/` e `evals/`).

## Instalar

```bash
# uma skill específica
npx skills add carlosferreirareis/skills --skill <nome-da-skill>

# todas de uma vez
npx skills add carlosferreirareis/skills --all
```

## Skills

| Skill | Descrição | Instalar |
|---|---|---|
| [`copywriter-brasileiro`](copywriter-brasileiro/) | Copywriting baseado em "O Livro de Ouro do Copywriter Brasileiro" (Junior WM): psicologia da persuasão, persona, benefícios, headline, banco de palavras e estrutura de carta de vendas. | `npx skills add carlosferreirareis/skills --skill copywriter-brasileiro` |
| [`carta-de-vendas-16-palavras`](carta-de-vendas-16-palavras/) | Framework "One Belief + Ten Questions" de "A Carta de Vendas de 16 Palavras" (Evaldo Albuquerque), para planejar e estruturar cartas de vendas/VSLs do zero e diagnosticar peças que não convertem. | `npx skills add carlosferreirareis/skills --skill carta-de-vendas-16-palavras` |
| [`headlines-lendarias`](headlines-lendarias/) | Swipe file de 101 headlines reais (Ogilvy, Schwartz, Caples, Halbert, Hopkins), organizadas em 15 padrões estruturais reutilizáveis. | `npx skills add carlosferreirareis/skills --skill headlines-lendarias` |

## Como criar uma skill nova

1. Copie `templates/skill-template/` (na raiz do repo) para uma pasta nova aqui dentro.
2. Preencha o `SKILL.md` (frontmatter + instruções) e adicione um `README.md` curto (nome, descrição, comando `npx skills add`).
3. Use a skill `skill-creator` do Claude Code pra testar antes de finalizar — guarde o relatório de avaliação em `evals/review-iteration-1.html`.
4. Adicione a skill à tabela acima e ao README raiz do repo.

## Documentos de apoio

- [`exemplo-prompt-anuncios.md`](exemplo-prompt-anuncios.md) — prompt genérico com placeholders para gerar anúncios combinando as três skills.
- [`mapeamento-skills-copywriting.md`](mapeamento-skills-copywriting.md) — qual skill usar para gancho, desenvolvimento, CTA e fechamento por WhatsApp.
