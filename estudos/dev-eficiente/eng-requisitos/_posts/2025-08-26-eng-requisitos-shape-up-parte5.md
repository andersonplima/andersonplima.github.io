---
layout: post
title: "Engenharia de Requisitos: Shape Up parte 5"
date: 2025-08-26 23:17:00 +0000
image: /assets/images/estudos/dev-eficiente/eng-requisitos/eng-requisitos-shape-up-parte5-cover.jpg
category: shape-up
---
Hoje continuamos o capítulo sobre construção do livro Shape Up. Por favor, leia os posts anteriores em sequência para não se perder aqui.

Ao construir uma primeira parte do software também é importante *começar pelo meio*. As funcionalidades de software tem um fluxo natural de usabilidade onde a parte importante e desafiadora está no meio. Coisas como cadastros básicos e login, por exemplo, não atacam o problema real a ser resolvido e podem ser feitas depois. Os critérios que podem ser usados para decidir por onde começar são:
- A coisa é essencial? Sem ela o problema exposto no pitch ainda pode ser resolvido?
- Ela é pequena? Como é preciso entregar essa primeira parte na primeira semana, não adianta pegar algo complexo demais para fazer.
- Ela é incomum? Ou seja, é uma coisa que não existe ainda no sistema ou que tem algum desafio para ser implementada?

### Mapeie os escopos

Os escopos são conjuntos de tarefas que fazem sentido serem entregues juntas para demonstrar alguma funcionalidade que é parte da solução do problema.

Eles não são mapeados de forma prévia e sim descobertos à medida que as tarefas do projeto vão sendo executadas. Eles também definem a linguagem do projeto e raramente estão ligados a aspectos técnicos, tendo mais a ver com funcionalidades completas que afetam o negócio e podem ser entregues de forma independente.

### Mostre progresso

Como as tarefas dentro de cada escopo podem variar até o fim do ciclo, o processo define uma forma de reportar progresso bem particular. Ele materializa a analogia da construção com uma caminhada por uma colina através de pontos numa curva em formato de sino. Nesse gráfico, cada ponto representa o status de um escopo.

À medida que o escopo está sendo descoberto, e a quantidade de incertezas vai diminuindo, ele é representado como um ponto do lado esquerdo da curva, subindo a colina. Quando não houver mais incertezas, o ponto estará no topo dela. O lado direito da curva, descendo a colina, é reservado para os escopos que já estão sendo codificados até que cheguem à base da colina.

Essa apresentação gráfica e o acompanhamento das mudanças dela ao longo do ciclo de seis semanas, serve para que os gestores foquem na observação dos escopos parados por muito tempo, para que ajudem a desimpedi-los (por exemplo, chamando ajuda de um sênior) ou verifiquem se o mapeamento de escopo está inadequado. Adicionalmente, ela serve para ordenar os escopos para resolver os mais complexos primeiro. Como o tempo é limitado a seis semanas, começar pelos escopos "fáceis" é a pior estratégia, pois surpresas podem aparecer no final do ciclo.

### Decida quando parar

Sempre é possível melhorar o trabalho do software a ser entregue, mas é preciso saber quando parar. A melhor forma é comparar o que se tem construído com o que os usuários já tem acesso e não com algum software ideal platônico.

Como há um limite temporal, o time precisa balancear custos (tempo) e benefícios de melhorar algum aspecto do software que vá além de resolver o problema apostado. Então o trabalho de enxugar escopo é contínuo, até mesmo sendo chamado de *martelar escopo* dentro do livro. Aquilo que não é entregue pelo software tem tanto valor quanto o que é entregue, fazendo parte daquilo que o diferencia dos seus concorrentes. O time deve se perguntar: no que focar para resolver os problemas dos **nossos** clientes? É mais importante esse foco do que fazer algum tipo de cobertura pra um caso de uso excepcional que ninguém usa.

---

Ainda há um restinho de leitura para a seção de quando parar até que cheguemos à conclusão do livro e seus apêndices. Volte amanhã que teremos mais!