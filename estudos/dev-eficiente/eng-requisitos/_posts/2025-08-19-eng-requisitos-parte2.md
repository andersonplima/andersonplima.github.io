---
layout: post
title:  "Dev + Eficiente: Engenharia de Requisitos para Devs parte 2"
date:   2025-08-19 23:24:00 +0000
image: /assets/images/estudos/dev-eficiente/eng-requisitos/eng-requisitos-parte2-cover.jpg
---
Hoje conclui o curso de *Engenharia de Requisitos para Devs* ao estudar a definição de requisitos funcionais e não funcionais, 
além de passos práticos para o entendimento e refinamento de requisitos.

# Tipos de requisitos {#tipos-requisitos}

As definições abaixo foram retiradas do [livro](https://www.amazon.com.br/Software-Engineering-Global-Ian-Sommerville/dp/1292096136) de Engenharia de Software do Ian Sommerville 
em adaptação livre minha. Acredito serem definições bem claras e de fácil entendimento, por isso achei por bem trazê-las aqui 
sem muitas modificações.

Os requisitos funcionais definem os serviços que o sistema deve prover, como o sistema deve reagir a determinadas entradas e como o sistema deve se comportar em determinadas situações. Também pode incluir o que o sistema **não** deve fazer.

Os requisitos não funcionais, também conhecidos como atributos de qualidade, são limitações às quais os serviços e funções 
que o sistema fornece estão submetidos. Podem ser limitações de tempo, padrões, processos, custo, etc.

# 5 passos para refinar um requisito

O curso nos apresenta 5 passos práticos para refinar um requisito, de forma a minimizar as chances de termos surpresas na entrega de uma funcionalidade 
ou correção de software. São eles:

1. Busque acesso a quem idealizou o requisito.
    A fonte mais confiável possível deve ser encontrada para sanar qualquer dúvida. 
    Se não tem acesso a essa pessoa, busque a segunda mais confiável e assim por diante.
1. Entreviste quem solicitou o requisito.
    Não deve haver dúvidas sobre o que está sendo pedido, portanto esgote as possibilidades com a pessoa de referência, 
    preenchendo as lacunas e mantendo o canal aberto para eventuais reencontros.
    Uma boa técnica para encontrar motivações é a dos 5 porquês. Esse número 5 é só um *número mágico*, mas o importante é 
    que se entenda o objetivo real do requisito para melhorar seu refinamento.
1. Confira o entendimento do requisito.
    Uma vez que você entreviste a pessoa e tenha suas respostas, escreva com suas palavras o que entendeu e retorne à pessoa
    para conferir se você entendeu corretamente o requisito. Nesse momento, também é importante trazer representações do
    funcionamento do requisito rabiscado em um desenho. Assim, fica mais fácil para a pessoa validar o seu entendimento.
1. Especifique cenários de testes.
    Escreva um conjunto de especificações de testes contemplando os cenários de como o sistema deve se comportar diante
    desse novo requisito (e também de como ele não deve se comportar). Acrescente os cenários que verifiquem atributos de 
    qualidade, caso existam.
1. Descreva como você implementaria o requisito.
    Antes de começar a codificar o requisito, escreva como faria essa implementação, passo-a-passo, para que fique
    claro para você mesmo que você entendeu o requisito e que não esteja faltando nenhuma informação necessária. 
    Adicionalmente, submeta essa descrição aos cenários de teste especificados.

Executando esses passos, você estará pronto para abrir o editor de código e entregar o requisito com muito mais confiança de
estar resolvendo o problema do seu cliente.

Amanhã começarei a leitura do livro Shape Up, principal referência para esse método de refinamento de requisitos. Tchau!
