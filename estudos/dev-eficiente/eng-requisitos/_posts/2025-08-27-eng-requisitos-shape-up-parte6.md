---
layout: post
title: "Engenharia de Requisitos: Shape Up parte final"
date: 2025-08-27 23:27:00 +0000
image: /assets/images/estudos/dev-eficiente/eng-requisitos/eng-requisitos-shape-up-parte6-cover.jpg
---
Em menos de seis horas, divididas em seis dias, terminamos a leitura do livro Shape Up! Isto mostra o poder da rotina e da constância da qual falei na *Máquina de Aprender* (ver os posts de 10 dias começando [aqui]({% post_url /estudos/dev-eficiente/maquina-aprender/2025-08-04-dev-eficiente-dia2 %})).

### Decida quando parar (continuação)

#### QA serve para os casos excepcionais

A qualidade do projeto é de responsabilidade do time de execução e portanto não há testadores especializados. No caso da Basecamp, uma empresa com 50 funcionários na altura da escrita do livro, tem 1 QA para criar tarefas para casos excepcionais dentro dos projetos. Então o QA só age quando o time entende que seu trabalho pode ser importante e é o próprio time que faz esses testes, preferencialmente de forma automatizada.

#### Extensão do tempo de execução

Há raros casos em que o tempo de execução pode ser expandido para dentro do tempo de resfriamento, mas as condições necessárias para que isso ocorra são: as tarefas que não conseguiram ser concluídas são todas obrigatórias para solução do problema e não há escopos dentro da subida da colina, ou seja, ainda com dúvidas a sanar. Mesmo nesses casos, é preferível que essa aposta seja descartada e só retomada se ela vier como nova aposta em ciclos seguintes. Essas apostas não concluídas podem indicar falha de performance do time ou do processo de modelagem dela.

#### Feedbacks precisam de modelagem

Após a entrega da solução, é possível que cheguem feedbacks de clientes sobre novos problemas ou sobre insatisfação. É essencial que o time não haja sob pressão e receba os feedbacks como novos itens a modelar. Assim, o time de modelagem consegue entender se as reclamações fazem sentido ou não e se merecem ser apostadas nos próximos ciclos.

### Apêndices

O primeiro apêndice do livro explica como implementar o método usando a ferramenta Basecamp, e não farei nenhum resumo aqui por se tratar de algo muito específico e direto. Você pode consultar o livro caso queria aplicar o método no seu time. Os outros dois apêndices tem algumas informações que podem ser relevantes de forma geral ao tentar aplicar o método, então os apresento aqui.

#### Ajuste para o seu tamanho

Ao aplicar o Shape Up, algumas coisas dependem de como a empresa funciona, do tipo de software desenvolvido e de qual o tamanho da empresa. Nesse caso, é importante diferenciar aquilo que é crucial ao método e aquilo que pode ser adaptado. Os itens importantes são:
- O time de execução deve trabalhar exclusivamente no projeto durante o tempo do ciclo. Nesse caso, a forma de isolamento do time pode variar, por exemplo a empresa tendo times de operação e infraestrutura para atender ao funcionamento do produto em produção. Também pode variar o tamanho do ciclo e se ele é fixo. Numa empresa muito pequena onde os fundadores ainda colocam a mão na massa, pode-se trabalhar em projetos com tamanho de ciclo diferentes. O importante é que se ajuste e se cumpra o apetite acordado.
- É preciso trabalhar apenas em soluções modeladas. Não necessariamente é preciso ter times trabalhando de forma paralela em modelagem e execução. Numa empresa pequena, é bem possível que o mesmo time alterne entre essas fases.
- É preciso ter um time multidisciplinar e responsável pela entrega da solução completa. Nem sempre uma pessoa faz cada coisa dentro de um time, mas ele precisa ter todas as competências necessárias para a entrega contempladas pelas pessoas do time.

#### Como começar a aplicar o Shape Up

O livro indica três opções para começar a trabalhar usando esse modelo, de forma que o entendimento de um ou alguns dos aspectos essenciais dele instigue o time a aplicar os outros.
1. Fazer um experimento de seis semanas, isolando o time para que trabalhe sem interrupções e de forma autônoma em apenas um problema modelado.
1. Começar com a modelagem, aplicando todo o método dessa fase do Shape Up e entregando para o time trabalhar usando o método que já usa hoje, como por exemplo *Scrum*.
1. Fixar o ciclo do time em seis semanas evitando reuniões de planejamento (3 se o time usa scrum) e permitindo que o time acerte o passo de produção de código.

---

Espero que tenham gostado tanto quanto eu da leitura do livro. Ele nos dá insights bem interessantes de como é possível aplicar processos de desenvolvimento que fogem um pouco do lugar comum. 

Ao mesmo tempo, o livro deixa espaço para dúvidas quanto à gestão dessas pessoas, uma vez que assume um compromisso total com as apostas feitas, algo que tem suas falhas de aplicabilidade na vida real. Acredito que o fato dos criadores e donos do Basecamp estarem até hoje dentro do processo de modelagem, permite que alguns erros não sejam cometidos, prejudicando o processo de execução. Eles também são pessoas sênior que podem ajudar sempre que necessário para desimpedir escopos que estejam subindo a colina por muito tempo.

Amanhã retomarei os estudos da plataforma Dev+Eficiente e blogarei aqui. Até amanhã!