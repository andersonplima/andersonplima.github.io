---
layout: post
title: "Engenharia de Requisitos: Shape Up parte 2"
date: 2025-08-21 22:45:00 +0000
image: /assets/images/estudos/dev-eficiente/eng-requisitos/eng-requisitos-shape-up-parte2-cover.jpg
category: shape-up
---
Continuando a leitura da definição de limites, foi mostrado um estudo de caso com a inclusão de um calendário na ferramenta de cadastro de eventos do Basecamp. Uma ferramenta de calendário completa pode ser muito complexa e levar pelo menos seis meses para uma primeira versão. Mas ao modelar a funcionalidade, entrevistando o cliente, o time viu que o problema a ser resolvido era a falta de visibilidade de espaços na agenda para marcar novos compromissos. Então a ideia desenvolvida foi um *calendário de pontos*, onde dois meses são exibidos por vez e as datas ocupadas são marcadas com pontinhos pretos. Logo, uma data livre seria facilmente identificável.

O livro também alerta para funcionalidades sem propósito claro, como refatorações completas, iniciativas chamadas *Função 2.0* ou *Redesign da Funcionalidade Y*. Esse tipo de ideia gera um alerta vermelho sobre o que não fazer, pois dificilmente encaixaria em qualquer apetite definido. 

### Encontrar os elementos

Essa sessão trata do segundo passo da modelagem onde os elementos da solução são descobertos pelo time. São discutidas duas formas de fazer isso, as *placas de ensaio* e os *rascunhos em pincel marcador*.

As placas de ensaio são uma inspiração das homônimas da área de engenharia elétrica, e consistem em definir os elementos da solução usando:
- Lugares: apresentados como nomes sublinhados, representam coisas para onde você pode navegar no sistema, como telas e menus.
- Recursos: apresentados como nomes abaixo dos lugares, representam coisas sobre as quais o usuário pode agir, como botões e campos.
- Linhas de conexão: são linhas que conectam recursos a lugares, movendo o usuário.

Já os rascunhos são ditos como feitos com pincel marcador para que seja difícil desenhar detalhes. A intenção é que seja um desenho em alto nível, destacando apenas os elementos importantes para a solução, deixando espaço para que os designers do time de construção trabalhem na versão final.

### Riscos

De posse dos elementos da solução, é hora de pensar nos riscos de não entregar dentro do apetite definido. As possíveis questões a serem respondidas são:
- A solução requer um trabalho técnico que nunca foi feito antes?
- Não temos certeza sobre como as partes se conectam?
- Estamos assumindo que existe uma solução de design que não somos capazes de pensar?
- Existe alguma decisão forte pendente que devemos tomar nessa fase?

Também é importante nesse passo definir quais casos a solução não suporta para que o time de construção não perca tempo tentando resolver. Além disso, se um especialista técnico ainda não viu essa solução, é hora de discutir com um para que ele dê sua visão sobre se essa solução cabe no apetite definido.

### Pitch

O pitch é o texto que vai ser usado para defender essa solução na fase de aposta. Os primeiros três ingredientes do pitch são:
1. O problema: a ideia, o caso de uso, algo que estamos motivados a resolver. O problema! Você entendeu.
1. O apetite: mesmo nessa fase, podem haver discussões sobre a solução e o apetite serve para limitar o tipo de alteração que pode haver nela, ou mesmo o quanto o time está disposto a discutir. 
1. A proposta de solução: por mais que seja óbvio, muitas vezes há pitches em que apenas o problema é descrito. Isso quer dizer que a modelagem não foi feita e não é produtivo fazer outro time investir tempo nessa atividade.

---

Vejo nesse segundo dia de leitura do Shape Up, que há bastante aprendizado que podemos levar
para qualquer refinamento de requisitos, independente de qual é o processo de upstream como um todo.

Amanhã, finalizo a leitura sobre modelagem com os dois últimos elementos do pitch e inicio a leitura da fase de aposta. Até lá!