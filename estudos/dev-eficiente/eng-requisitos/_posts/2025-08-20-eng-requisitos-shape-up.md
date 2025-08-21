---
layout: post
title: "Engenharia de Requisitos: Shape Up parte 1"
date: 2025-08-20 22:51:00 +0000
image: /assets/images/estudos/dev-eficiente/eng-requisitos/eng-requisitos-shape-up-parte1-cover.jpg
---
Para aprofundar um pouco mais o que foi estudado no curso anterior, resolvi ler a sua principal referência, o [livro](https://basecamp.com/shapeup) Shape Up, de Ryan Singer. Na sequência deste post, listo os principais pontos abordados até a página 32 da versão em PDF.

## Introdução

Muitos times de software em crescimento se deparam com os seguintes problemas:
- Os membros do time sentem que os projetos só crescem e não terminam nunca.
- Os gestores do produto não encontram tempo para pensar de forma estratégica sobre o produto.
- Os donos das empresas não entendem porque o time não consegue entregar as funcionalidades como antigamente.

Com o time da Basecamp não foi diferente e o produto que nasceu com três pessoas, incluindo o autor do livro, passou a enfrentar esses mesmos desafios à medida que crescia. Ao longo de 15 anos, o processo interno foi desenvolvido e virou o que se chama hoje *Shape Up*.

As principais ideias do processo são:

- Ciclos de seis semanas
    Um tempo grande o suficiente para entregar algo relevante e pequeno o suficiente para que a equipe sinta o prazo (ver aceleradores e sabotadores nos dias 
    [9]({% post_url /estudos/dev-eficiente/maquina-aprender/2025-08-14-dev-eficiente-dia9 %}) e 
    [10]({% post_url /estudos/dev-eficiente/maquina-aprender/2025-08-15-dev-eficiente-dia10 %}) da *Máquina de Aprender*).
    da *Máquina de Aprender*.
- Moldar o trabalho
    Antes de ser executado, o trabalho passa por um processo em que um time sênior define os principais pontos de uma solução, no nível de abstração correto para que haja espaço para o time executor entender o que deve ser feito, mas ainda assim tenha liberdade para encontrar a melhor forma de implementar a solução.
- Tornar os times responsáveis
    Os times executores formados por designers e desenvolvedores(as) tem autonomia para refinar e entregar a solução, partindo do que foi moldado.
- Adereçar riscos
    Em todas as etapas do processo o risco de não entregar a tempo é abordado e minimizado.

O livro é separado em três grandes partes:
1. Modelagem, onde a primeira etapa do processo é explicada.
1. Aposta, a segunda etapa, onde as soluções modeladas são selecionadas e priorizadas.
1. Construção, a última etapa, onde as soluções são refinadas e construídas.

## Parte 1: Modelagem

A modelagem é baseada na criação de uma solução que nem de tão alta fidelidade como um wireframe, nem tão baixa como um conjunto de explicações simples em texto. As propriedades da modelagem são:

1. É grosseira, no sentido de que é visível que não está pronta e que há espaço para designers e programadores colaborarem na definição da solução.
1. Está resolvida, no sentido de que não há buracos de entendimento e estão claros os principais elementos da solução em alto nível.
1. É limitada, uma vez que mostra o que a solução não faz ou não entrega. Também há a limitação de tempo, que no Shape Up é chamado de *apetite*.

Para o trabalho de modelagem é necessário conhecimento estratégico, de design e de programação, para assim ter a definição do que a funcionalidade faz, como funciona e como ela se encaixa no que já existe no sistema. A modelagem então pode ser feita por uma ou mais pessoas que possuam esses conhecimentos. 

A modelagem ocorre em paralelo com a execução e não interfere nela. Enquanto o time de construção está trabalhando nos itens já modelados, novos itens estão sendo modelados para os próximos ciclos.

Os passos para a modelagem são:
1. Ajustar limites: definir o apetite para aquele projeto ou funcionalidade e definir o problema a ser resolvido.
1. Fazer o rascunho de uma solução que se adapte aos limites.
1. Adereçar riscos: encontrar e resolver lacunas ou detalhes que podem fazer o time ficar impedido de trabalhar durante a fase de construção.
1. Escrever o *pitch*: ele resume o problema, as restrições, a solução, as armadilhas e as limitações. Junto com o rascunho, compõe o que é necessário para começar o trabalho de execução, uma vez que esse pitch é aprovado na etapa de aposta.

### Ajustar limites

Nesse passo, é definido o apetite, que em geral consegue ter dois tamanhos: pequeno (factível em 1-2 semanas) ou grande (factível em um ciclo de 6 semanas). O apetite exprime a vontade de aplicar esforço naquela funcionalidade.

Uma vez definido o apetite, a funcionalidade é melhor entendida. Nessa hora é muito importante o acesso ao solicitante. Um exemplo interessante que o livro dá é o de um cliente que pediu um sistema complexo de permissões, para que a pessoa não pudesse arquivar facilmente um arquivo no sistema. Ao entrevistar o cliente, o time de modelagem entendeu que um usuário arquivou um arquivo, achando que esse arquivamento só seria notado por ele, quando na verdade o sistema arquivava para todos os usuários. A proposta de solução aprovada foi mostrar um aviso ao usuário explicando o cenário e deixando a decisão a cargo dele. Com isso uma solução que poderia ter ocupado um ciclo inteiro, foi resolvido em um dia.

<br />

---

<br />

Amanhã continuarei a leitura da sessão *Ajustar limites* e volto por aqui para compartilhar com vocês. Até!