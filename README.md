# skills

Repositório pessoal para concentrar **todas as minhas skills do Claude Code** — as que eu crio do zero e as que eu faço fork de outros autores/repositórios — para reutilizar facilmente nos meus projetos.

Uma *skill*, no formato do Claude Code, é uma pasta com um arquivo `SKILL.md` (frontmatter YAML + instruções em Markdown) e, opcionalmente, scripts, referências e assets auxiliares. Mais detalhes: https://code.claude.com/docs/en/skills

## Estrutura

```
skills/
├── skills/          # Skills criadas por mim, do zero
│   └── <nome-da-skill>/
│       └── SKILL.md
├── forks/           # Skills de terceiros (fork/adaptação), com atribuição
│   └── <nome-da-skill>/
│       ├── SKILL.md
│       └── SOURCE.md    # origem, autor, link, licença, o que foi alterado
└── templates/
    └── skill-template/  # esqueleto para começar uma skill nova
        └── SKILL.md
```

- **`skills/`** — minhas skills originais. Uma pasta por skill.
- **`forks/`** — skills de terceiros trazidas para cá. Cada uma mantém um `SOURCE.md` com a origem (repo/link), autor e licença, além do que foi adaptado em relação ao original.
- **`templates/`** — modelos para criar novas skills rapidamente.

## Convenções

- **Nome da pasta** = `name` da skill em `SKILL.md`, em `kebab-case`.
- Cada skill vive isolada na sua própria pasta (sem dependências cruzadas entre skills).
- `SKILL.md` deve ter frontmatter com `name` e `description` claros — a `description` é o que o Claude usa para decidir quando ativar a skill, então deve ser específica sobre quando (e quando não) usá-la.
- Scripts, referências e exemplos auxiliares de uma skill ficam dentro da própria pasta dela (ex.: `scripts/`, `references/`, `assets/`).

## Como adicionar uma skill nova (criada por mim)

1. Copie `templates/skill-template/` para `skills/<nome-da-skill>/`.
2. Preencha o `SKILL.md` (frontmatter + instruções).
3. Adicione a skill à tabela abaixo.
4. Commit e push.

Dica: use a skill `skill-creator` do Claude Code para gerar, revisar e testar (`eval`) a skill antes de finalizar. Cada skill deste repo guarda em `evals/review-iteration-N.html` o relatório comparativo (com/sem a skill) gerado nesse processo — abra um no navegador para ver um exemplo de como funciona o teste antes de criar o seu.

## Como adicionar um fork

1. Crie `forks/<nome-da-skill>/`.
2. Copie o conteúdo original (respeitando a licença do projeto de origem).
3. Documente em `SOURCE.md`: link do repositório/autor original, licença e um resumo das adaptações feitas.
4. Adicione a skill à tabela abaixo.
5. Commit e push.

## Skills disponíveis

### Próprias

| Skill | Descrição |
|---|---|
| [`copywriter-brasileiro`](skills/copywriter-brasileiro/) | Copywriting baseado em "O Livro de Ouro do Copywriter Brasileiro" (Junior WM): psicologia da persuasão, persona, benefícios, headline, banco de palavras e estrutura de carta de vendas. |
| [`carta-de-vendas-16-palavras`](skills/carta-de-vendas-16-palavras/) | Framework "One Belief + Ten Questions" de "A Carta de Vendas de 16 Palavras" (Evaldo Albuquerque), para planejar e estruturar cartas de vendas/VSLs do zero e diagnosticar peças que não convertem. |
| [`headlines-lendarias`](skills/headlines-lendarias/) | Swipe file de 101 headlines reais (Ogilvy, Schwartz, Caples, Halbert, Hopkins), organizadas em 15 padrões estruturais reutilizáveis, para gerar e variar headlines a partir de fórmulas comprovadas. |

### Forks

| Skill | Origem | Descrição |
|---|---|---|
| _(nenhuma ainda)_ | | |

## Exemplos de prompts

- [`skills/exemplo-prompt-anuncios.md`](skills/exemplo-prompt-anuncios.md) — prompt genérico com placeholders para gerar anúncios de conversão (headlines, carrosséis, texto de anúncio, roteiros) combinando as skills `copywriter-brasileiro`, `carta-de-vendas-16-palavras` e `headlines-lendarias` para qualquer negócio/produto.
- [`skills/mapeamento-skills-copywriting.md`](skills/mapeamento-skills-copywriting.md) — qual dessas três skills é mais forte para escrever o gancho, o desenvolvimento e o CTA de uma peça, e como combiná-las.

## Uso nos projetos

Para usar uma skill de um projeto, copie a pasta da skill (`skills/<nome>/` ou `forks/<nome>/`) para o diretório de skills do projeto de destino (ex.: `.claude/skills/`), ou consulte a documentação do Claude Code sobre como referenciar skills externas.
