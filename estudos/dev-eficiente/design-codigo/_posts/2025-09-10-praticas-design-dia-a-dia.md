---
layout: post
title:  "Dev + Eficiente: Práticas de Design de Código Para Seu Dia a Dia"
date:   2025-09-10 22:56:00 +0000
image: /assets/images/estudos/dev-eficiente/design-codigo/praticas-design-dia-a-dia-cover.jpg
---

Olá! Voltando com o post diário (não é mais diário, igual àquela daily semanal do seu time) vou tratar do curso Práticas de Design de Código Para Seu Dia a Dia. Esse curso está muito ligado ao [anterior]({% post_url /estudos/dev-eficiente/design-codigo/qualidade/2025-09-01-qualidade-software-1 %}) sobre qualidade no design de código, mas aprofunda com exemplos práticos alguns aspectos. Serve como reforço do curso anterior e também dá margem para aplicação imediata se você já trabalha desenvolvendo software.

### Direcionamentos antes da prática

#### Qualidade não é negociável

A qualidade do seu trabalho não é algo que pode ser deixado de lado porque o prazo está apertado. As coisas que podem ter menor qualidade com prazo apertado são aquelas sobre as quais você não tem domínio técnico. Estas você pode negociar e deixar transparente para os stakeholders e gestores. Mas, por exemplo, se você domina testes automatizados, você tem obrigação profissional de fazê-los. Sobre essas obrigações, indico a leitura do livro [O Programador Pragmático](https://www.amazon.com.br/Programador-Pragm%C3%A1tico-Aprendiz-Mestre/dp/8577807002).

#### Tomamos decisões ruins

Tudo que fazemos no nosso código está ligado a um contexto. Então, garanta que a decisão tomada agora é a melhor possível dentro do contexto e lide com as consequências quando vierem, **corrigindo os problemas**.

#### Fazemos o que foi combinado

A prioridade máxima é entregar o caso de uso específico. Comece seu código fazendo apenas o que foi pedido ou combinado com qualidade. Depois, se houver tempo, você pode expandir a flexibilidade do código, se fizer sentido, mas isso deve acontecer apenas em casos excepcionais.

### Práticas

Aqui vou explicar as práticas uma a uma, mas sem mostrar código, pois são exercícios de código Java executados pelo professor durante o curso que faz mais sentido que você mesmo se inscreva para assistir ou procure pesquisar e aplicar de outra forma. Acho que estrapola um pouco o limite do que pode ser compartilhado de um curso pago 😶‍🌫️.

#### Implemente de fora para dentro

É mais fácil entender se você tem todo o conhecimento necessário para implementar uma funcionalidade, se você começa por onde o usuário tem acesso, por exemplo uma API ou uma tela de um sistema. Por mais que sua implementação seja em camadas, comece pela parte mais próxima do usuário, e vá testando passo a passo a aplicação, até que chegue na parte mais interna. Esse princípio é muito parecido com o TDD, onde você inicia escrevendo testes que quebram dos casos de uso a serem implementados.

#### Maximize a coesão

Escreva o código que faz alterações ou cálculos em alguma informação o mais próximo possível de onde aquela informação é armazenada. Assim, fica mais fácil para a próxima pessoa entender onde mexer quando precisa fazer alterações relacionadas a um assunto, contexto, etc. Essa estratégia também diminui o acoplamento de mudança entre arquivos, uma vez que quase tudo que precisa ser mudado para alterar uma funcionalidade estará dentro de poucos arquivos, ou muitas vezes um só.

#### Proteja as bordas do sistema

Todo método público ou interface de entrada, as chamadas bordas, precisa ser protegida, ou seja, não tome como garantido nenhum dado fornecido, valide tudo! Valores nulos, limites de valores, existência de entidades, são exemplos do que deve ser validado.

#### Não retorne nulo

Você deve ser explícito sobre aquilo que seus métodos retornam. Ao retornar nulo, você delega a quem chama, a responsabilidade de verificar se existe algo no retorno. Se sua linguagem de trabalho não possui esse tipo de construção, crie você mesmo os tipos que encapsulem valores opcionais de retorno com métodos para verificação de nulidade. Assim, fica claro pra quem usa sua função que ela **deve** verificar se o retorno contém um valor, permitindo até mesmo que analisadores estáticos de código customizados avaliem se seu código está conferindo tudo.

#### Não ligamos parâmetros de borda externa com entidades

Os tipos que definem o contrato com o mundo externo, não podem ser os mesmos tipos usados para persistência. Se reutilizamos esses tipos, o sistema pode sofrer ataques de injeção de parâmetros que causam inconsistências no seu banco de dados. A boa prática é usar DTOs (Data Transfer Objects) para o contrato, os diferenciando das classes de negócio ou entidades.

#### Informação obrigatória entra pelo construtor

Os seus objetos devem ser sempre válidos, portanto, deve ter suas propriedades obrigatórias inicializadas pelo construtor. Um objeto que tem brechas de inicialização através de propriedades, pode entrar muito facilmente num estado inválido, principalmente se quem criou a classe é diferente de quem vai usar a classe, coisa que é muito fácil de acontecer na manutenção de um sistema. Então, os contratos devem ser explícitos sempre, e o contrato de criação de um objeto é seu construtor.

#### Deixe pistas quando a compilação não resolver

Comentários e metadados são importantes para explicitar algo que não pode ser lido nos contratos, ou seja, que seria tratado como erro de compilação, quando não cumprido.

#### Utilize o que está pronto

Conheça sua linguagem e framework, ou mesmo pacotes externos com boa reputação. Se a funcionalidade não estiver disponível em nenhum desses lugares, você implementa a sua solução. Todo código acaba sendo um compromisso assumido de manutenção - também conhecido como **custo** -, então é importante que ele seja restrito ao caso de uso solicitado.

#### Utilize o Cognitive Driven Design

Para evitar discussões eternas sobre complexidade nas revisões de código, tenha um acordo prévio sobre o assunto para que todos do time sigam. O CDD é uma das formas, criada pelo próprio Alberto Souza, com base na teoria da carga cognitiva, onde valores são atribuídos aos elementos do código e a soma desses valores é calculada para cada função ou classe. O acordo firmado é sobre o valor máximo dessa soma. Pesquisas indicam que o CDD direciona o código para uma melhor legibilidade e manutenibilidade[^1] [^2] [^3].

[^1]: [Cognitive-Driven Development Helps Software Teams to Keep Code Units Under the Limit!](https://arxiv.org/abs/2210.07342)
[^2]: [Toward a Definition of Cognitive-Driven Development](https://ieeexplore.ieee.org/document/9240662)
[^3]: [Assisting Novice Developers Learning in Flutter Through Cognitive-Driven Development](https://arxiv.org/abs/2408.11209)

#### Só altere referências que você criou

Use apenas o bloco de código que criou as referências para um objeto para modificar o conteúdo dele. Isso facilita bastante o rastreamento de modificações de objetos, que é uma atividade bem frequente na correção de bugs ou alterações de comportamento de funcionalidades. Se todo mundo pode mexer em tudo, é fácil seu sistema virar um caos!

#### Derive testes de maneira sistemática

Não teste seus sistemas aleatoriamente de primeira, foque antes nos testes de vão captar casos limites do seu código. Esses casos são bem específicos e variados caso a caso, mas a ideia é que os possíveis caminhos do seu código sejam todos percorridos pelo menos uma vez pelos testes executados.

---

Este post, com conteúdo retirado do curso, dá dicas excelentes de como ter uma qualidade mínima no seu código. Ao praticar essas sugestões no dia-a-dia, o seu time vai ter um código muito mais fácil de manter. Ele não é uma lista extensiva de todas as técnicas possíveis, mas as que estão aqui são muito valiosas 💎.


