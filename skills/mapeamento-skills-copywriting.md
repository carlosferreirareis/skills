# Mapeamento: qual skill usar em cada etapa do anúncio

Este documento mapeia, com justificativa, qual das três skills de copywriting deste repositório é mais forte para cada etapa de uma peça de vendas curta (anúncio, carrossel, VSL) — **gancho**, **desenvolvimento** e **CTA**. É um complemento ao [`exemplo-prompt-anuncios.md`](exemplo-prompt-anuncios.md): aquele arquivo dá o prompt pronto para usar; este explica o "porquê" por trás de como as skills se combinam.

Skills envolvidas:
- [`copywriter-brasileiro`](copywriter-brasileiro/) — caixa de ferramentas geral (persona, benefícios, headline, banco de palavras, estrutura completa de carta de vendas).
- [`carta-de-vendas-16-palavras`](carta-de-vendas-16-palavras/) — framework sequencial de planejamento (One Belief + 10 Perguntas).
- [`headlines-lendarias`](headlines-lendarias/) — swipe file de 101 headlines reais, organizadas em 15 padrões estruturais.

## Resumo — qual skill puxa cada etapa

| Etapa | Skill principal | Skill de apoio | Por quê |
|---|---|---|---|
| **1. Gancho** | `headlines-lendarias` | `carta-de-vendas-16-palavras` (Perguntas 1-2) + `copywriter-brasileiro` (4 U's) | É a única das três construída **só** pra isso — 15 padrões nomeados de headlines reais, com molde e critério de quando usar cada um. |
| **2. Desenvolvimento** | `carta-de-vendas-16-palavras` | `copywriter-brasileiro` (banco de palavras, bullets, benefícios) | É a única com uma **sequência lógica testada** pro corpo da peça (Perguntas 3-8: prova, verdadeiro problema, inimigo comum, urgência, confiança, mecanismo). `copywriter-brasileiro` entra pra "temperar" cada bloco. |
| **3. CTA** | `carta-de-vendas-16-palavras` | `copywriter-brasileiro` (falso fechamento, PS, garantia) | Pergunta 9 (oferta irresistível) + Pergunta 10 (fechamento push-pull) são técnicas específicas e nomeadas — mais precisas que o fechamento genérico da outra skill. |

## Por que essa divisão, em detalhe

### 1. Gancho → `headlines-lendarias` na frente

Ela tem 15 padrões nomeados (pergunta direta, "como eu fiz X", choque de incredulidade, número+lista, prova/autoridade, contraste de preço, exclusividade, "para [persona]", facilidade extrema, entre outros), cada um com molde pronto e exemplo real de anúncio histórico (`references/01-formulas-e-padroes.md`). Nos testes que rodamos para validar essa skill, ela foi a única que nomeou o padrão usado em cada headline gerada e justificou a escolha pela emoção da persona — diferencial de execução, não só de conteúdo.

As outras duas contribuem, mas em segundo plano:
- `carta-de-vendas-16-palavras` define **o que** a headline precisa comunicar (Pergunta 1 = novidade, Pergunta 2 = grande promessa, em `references/02-perguntas-1-a-4.md`) — ótima pra garantir que o gancho tem substância, mas não dá a variedade de formatos.
- `copywriter-brasileiro` tem os 4 U's (Utilidade, Urgência, Exclusividade, Ultra-especificidade) e 40 fórmulas de headline (`references/04-headline.md`) — é redundante com `headlines-lendarias`, só que com menos exemplos reais por trás.

**Na prática:** peça o gancho pra `headlines-lendarias`, mas dê a ela o "core" definido pelas Perguntas 1-2 da outra skill como matéria-prima.

### 2. Desenvolvimento → `carta-de-vendas-16-palavras` na frente

Nenhuma das outras duas tem uma sequência causal pro meio da peça. `carta-de-vendas-16-palavras` tem: prova sempre em formato ABT — E→Mas→Portanto (`references/02-perguntas-1-a-4.md`), o "verdadeiro problema" que tira a culpa do leitor, o inimigo comum ("nós vs eles"), urgência ancorada em fato real, e as três histórias de credibilidade — Já Passei Por Isso / Robin Hood / Especialista (`references/03-perguntas-5-a-7.md`). Isso é estrutura de argumento, o coração do desenvolvimento.

`copywriter-brasileiro` entra como caixa de ferramentas dentro dessa estrutura: os 21 tipos de bullet de Ray Edwards e a fórmula característica→benefício com o teste do "tapa na testa" (`references/03-beneficios-e-caracteristicas.md`), e o banco de 21 categorias de palavras de poder (`references/05-banco-de-palavras.md`) pra dar intensidade ao texto que a outra skill já estruturou.

**Na prática:** deixe `carta-de-vendas-16-palavras` decidir a ordem e o argumento de cada bloco; peça pra `copywriter-brasileiro` escrever os bullets e escolher as palavras dentro de cada bloco.

### 3. CTA → `carta-de-vendas-16-palavras` na frente

Pergunta 9 (oferta irresistível — lacuna de valor, bônus S.I.N., escada de valor, ancoragem) e Pergunta 10 (push-pull: nunca soar desesperado, alternar controle/perda), ambas em `references/04-perguntas-8-a-10.md`, são as técnicas mais específicas e testadas pra fechamento entre as três skills.

`copywriter-brasileiro` também cobre fechamento (falso fechamento, PS, garantia, ancoragem de preço, em `references/06-estrutura-carta-de-vendas.md`) — não é dispensável, principalmente pro PS, que a outra skill trata só de leve.

**Na prática:** estruture a oferta e o fechamento com `carta-de-vendas-16-palavras`, e use `copywriter-brasileiro` pra escrever o PS final e reforçar a garantia.

## Sequência recomendada pra um anúncio completo

1. **Persona + núcleo emocional** → `copywriter-brasileiro`
2. **One Belief + Perguntas 1-10 mapeadas** → `carta-de-vendas-16-palavras` (isso já dá o esqueleto de gancho, desenvolvimento e CTA)
3. **Gancho final** → `headlines-lendarias`, usando a Pergunta 1-2 como matéria-prima, gerando 3-5 variações em padrões diferentes
4. **Desenvolvimento final** → `carta-de-vendas-16-palavras` estrutura, `copywriter-brasileiro` executa (bullets + banco de palavras)
5. **CTA final** → `carta-de-vendas-16-palavras` (oferta + push-pull), `copywriter-brasileiro` pro PS

Essa é a lógica por trás das instruções do [`exemplo-prompt-anuncios.md`](exemplo-prompt-anuncios.md) — use os dois arquivos juntos: este pra entender o raciocínio, aquele pra executar.
