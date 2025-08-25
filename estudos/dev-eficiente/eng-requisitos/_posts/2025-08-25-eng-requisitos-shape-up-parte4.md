---
layout: post
title: "Engenharia de Requisitos: Shape Up parte 4"
date: 2025-08-25 22:24:00 +0000
image: /assets/images/estudos/dev-eficiente/eng-requisitos/eng-requisitos-shape-up-parte4-cover.jpg
---

Olá! Este post é continuação direta do post anterior. Se você não leu, ~~volte uma casa~~ acesse [aqui]({% post_url 2025-08-22-eng-requisitos-shape-up-parte3 %}).

Continuando a fase de apostas, o livro destaca que é importante iniciar cada ciclo com a mesa de trabalho vazia, ou seja, os times de projeto só trabalharão nos pitchs aprovados no ciclo de resfriamento precedente. O objetivo é manter o foco no que é importante e foi validado pela mesa de apostas, que lembre, é composta pelos principais stakeholders do produto.

### Faça suas apostas

Há formas diferentes de fazer apostas dependendo da fase do produto. Para produtos existentes, o processo já foi explicado até aqui e não há novidades. Mas e se estivermos trabalhando um produto novo?

Novos produtos são construídos em três fases ou modos.
1. Modo de pesquisa e desenvolvimento: as apostas são feitas sobre o tempo a ser investido em *spikes*, que são pesquisas de possíveis soluções técnicas para o problema ou ideia.
    Esses ciclos, também de seis semanas, se repetem até que o time que está pesquisando, formado por pessoas sênior, tenha confiança que chegou em uma solução que faz sentido e as decisões fundamentais de interface e código já foram tomadas.
1. Modo de produção: apesar do nome, ainda não é nesse modo que o produto é exposto a público. O que ocorre aqui é a passagem de bastão para os times menos sênior continuarem o desenvolvimento em ciclos de &ndash; adivinha? &ndash; seis semanas.
    Durante esse modo, outras features podem ser adicionadas ao produto, até que se decida que ele está pronto para lançamento.
1. Modo de limpeza: após decisão de lançamento do produto, um ou dois ciclos são dedicados à resolução de bugs e polimentos de interface e funcionalidades. Também é possível decidir pela remoção de funcionalidades que não são adequadas ao produto.

Por fim, ao debater apostas as perguntas a se fazer para validar os pitchs são:
- Esse problema realmente importa?
- O apetite está correto?
- A solução é atrativa?
- É a hora certa de trabalhar nisso?
- As pessoas certas estão disponíveis?

Uma vez validada, uma mensagem pode ser postada para fazer o kick-off de projeto e iniciar o ciclo de construção.

## Construindo o projeto

Agora é hora de construir os projetos validados. Na reunião de kick-off o defensor do pitch explica o projeto para os responsáveis técnicos que definirão durante o ciclo o design final e implementarão o código **em produção**. Os testes também devem ser realizados dentro do ciclo e portanto o design e codificação não podem consumir todo o apetite.

Não há definição formal de tarefas no kick-off, pois isso fica a cargo do time executor. Ainda mais, as tarefas são livremente modificadas durante a execução, pois as tarefas imaginadas no início são diferentes das tarefas que surgem durante a investigação do estado atual do software e a codificação efetiva.

O método indica que seja construída uma peça de software de fim a fim já na primeira semana, para que fique claro desde cedo dentro do ciclo, tanto para o próprio time quanto para os seus líderes, quais serão as dificuldades de execução do projeto. Isso traz materialidade para as tarefas a serem executadas e diminui a margem de erro quanto ao consumo do apetite. Essa primeira versão, interna, não precisa estar visualmente perfeita, nem com o melhor código possível, mas precisa funcionar em ambiente de teste.

---

Hoje começamos a entender como é a construção de software dentro do processo Shape Up. Amanhã entraremos no mapeamento de escopo 🤔.




