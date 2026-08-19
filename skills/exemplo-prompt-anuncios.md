# Exemplo de prompt: anúncios de conversão com as skills de copywriting

Este arquivo é um **exemplo de prompt reutilizável** — não é uma skill, é um template que mostra como combinar três skills deste repositório para produzir anúncios de conversão (headlines, carrosséis, texto de anúncio, roteiros de vídeo) para qualquer negócio:

- [`copywriter-brasileiro`](copywriter-brasileiro/) — mapeia persona e núcleo emocional de compra.
- [`carta-de-vendas-16-palavras`](carta-de-vendas-16-palavras/) — define o One Belief e as 10 perguntas que estruturam o argumento de venda.
- [`headlines-lendarias`](headlines-lendarias/) — gera headlines/ganchos a partir de padrões comprovados.

O prompt abaixo foi generalizado a partir de um caso real (venda de sites institucionais, oferta com upsell e order bumps, dois mercados diferentes). Copie o bloco, preencha os placeholders `[ENTRE_COLCHETES]` com as informações do seu negócio e cole numa sessão do Claude Code com acesso a essas três skills. Se você não tiver alguma informação na hora, **deixe o placeholder como está ou apague a linha** — o próprio prompt instrui o Claude a perguntar antes de inventar qualquer coisa sobre o seu negócio.

---

## O prompt

```
Preciso que você atue como meu copywriter, combinando as três skills de copywriting disponíveis: `copywriter-brasileiro`, `carta-de-vendas-16-palavras` e `headlines-lendarias`. Use as três em conjunto, nesta ordem de raciocínio:

1. Primeiro, mapeie a persona e o núcleo emocional de compra (skill copywriter-brasileiro) para o(s) público(s)-alvo descrito(s) abaixo.
2. Depois, defina o One Belief e mapeie as 10 perguntas (skill carta-de-vendas-16-palavras) para esta oferta, adaptando o processo ao(s) formato(s) de anúncio pedido(s) — não é uma carta de vendas longa, é a estrutura por trás de peças curtas.
3. Use esse mapeamento como base para gerar as headlines/ganchos (skill headlines-lendarias), indicando qual padrão do swipe file cada uma usa.
4. Só então escreva o copy final de cada peça.

Antes de escrever qualquer copy, revise as informações abaixo. **Se alguma informação estiver faltando, incompleta, ambígua, ou parecer insuficiente para escrever um anúncio forte, pare e me faça perguntas objetivas primeiro** — não invente detalhes sobre o negócio, a oferta, o público ou a prova social. Peça exemplos concretos quando precisar (números reais, depoimentos, preços, diferenciais) em vez de aceitar respostas vagas.

## Sobre o negócio
- Nome do negócio/marca: [NOME_DO_NEGOCIO]
- O que você vende (produto/serviço, em poucas frases): [DESCRICAO_DO_PRODUTO_OU_SERVICO]
- O que torna essa oferta diferente da concorrência (se souber): [DIFERENCIAL / USP]
- Site ou link institucional (se houver): [LINK_DO_SITE]

## A oferta
- Oferta principal (o que inclui, preço): [OFERTA_PRINCIPAL_E_PRECO]
- Upsell(s), se houver (o que inclui, preço): [UPSELL_E_PRECO]
- Order bump(s), se houver (o que inclui, preço): [ORDER_BUMPS]
- Garantia, se houver: [GARANTIA]
- Prazo/urgência real, se houver (não invente um se não existir): [URGENCIA_REAL]

## Público(s)-alvo e mercado(s)
- Descreva quem compra isso hoje, ou quem você quer atingir: [DESCRICAO_DO_PUBLICO]
- Se houver mais de um mercado/idioma/região, liste cada um separadamente — eles devem receber anúncios **adaptados culturalmente**, não apenas traduzidos: [MERCADO_1], [MERCADO_2]...

## Prova social disponível
- O que existe (depoimentos, cases, números, portfólio, prêmios etc.): [PROVA_SOCIAL_DISPONIVEL]
- Como ela deve ser usada: a prova entra dentro do próprio anúncio (ex.: "já atendi X clientes", print de depoimento), ou é material reservado para depois — enviado manualmente na conversa de venda (WhatsApp, e-mail, DM) após o clique? [ONDE_A_PROVA_DEVE_APARECER]

## Formatos de anúncio pedidos
Liste cada formato que você precisa, com a quantidade/variações desejadas (ex.: "2 carrosséis de 6 telas para teste A/B", "1 roteiro de vídeo de 30s", "3 versões de anúncio estático com headline + texto curto", "1 sequência de 3 e-mails"): [LISTA_DE_FORMATOS]

## Regras e restrições
- Nunca prometa nada que não esteja descrito na oferta acima.
- Tom de voz desejado (se houver preferência — formal, descontraído, técnico etc.): [TOM_DE_VOZ]
- Qualquer coisa que NÃO deva aparecer no anúncio (ex.: preço, nome de cliente específico, comparação direta com concorrente): [RESTRICOES]

## O que preciso que você entregue
1. Persona + núcleo emocional (resumido, por mercado se houver mais de um).
2. One Belief + mapeamento das 10 perguntas (por mercado se houver mais de um).
3. 6 a 10 headlines/ganchos candidatos, indicando o padrão do swipe file usado em cada uma.
4. O copy final de cada formato de anúncio pedido, organizado por seção para eu revisar por partes.
```

---

## Por que este prompt funciona

- **Ordem importa**: pedir para o Claude planejar (persona → one belief/10 perguntas → headlines) antes de escrever o texto final evita que ele pule direto para frases soltas sem fundamento — é o mesmo motivo pelo qual as três skills, sozinhas, já instruem esse sequenciamento.
- **Placeholders em vez de exemplos fixos**: forçam você a preencher com fatos reais do seu negócio (a skill `headlines-lendarias`, por exemplo, é explícita que headlines fortes precisam de um fato concreto por trás — número real, prazo real, diferencial real).
- **A instrução de perguntar antes de inventar** é o que evita o erro mais comum ao usar IA para copy: preencher lacunas de informação com clichês genéricos que soam a "anúncio de IA" em vez de vender de verdade.
- **Separar "prova social no anúncio" de "prova social pós-clique"** veio de um caso real: nem toda prova precisa (ou deve) aparecer no criativo pago — às vezes ela funciona melhor reservada para o momento em que o lead já demonstrou interesse.
