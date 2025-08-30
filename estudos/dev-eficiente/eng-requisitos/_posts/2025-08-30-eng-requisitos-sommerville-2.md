---
layout: post
title: "Engenharia de Requisitos: Sommerville"
date: 2025-08-30 13:21:00 +0000
image: /assets/images/estudos/dev-eficiente/eng-requisitos/eng-requisitos-sommerville-1-cover.jpg
---
O [manifesto ágil](https://agilemanifesto.org/iso/ptbr/manifesto.html) tem como seus segundo e quarto valor, respectivamente:
> Software em funcionamento mais que documentação abrangente

> Responder a mudanças mais que seguir um plano

E como explicação sobre os valores:

> Ou seja, mesmo havendo valor nos itens à **direita**, valorizamos mais os itens à **esquerda**.

Isso quer dizer que **podemos** ter um plano e documentação, mesmo em processos ágeis, que representam o suposto[^1] estado da arte em desenvolvimento de software. Os valores ágeis como colocados no manifesto nos dizem que priorizamos os itens à esquerda em momentos de escolha, mas não desvalorizamos os itens à direita. Há situações em que é desejável ter algum nível de documentação e planejamento, como quando precisamos de maior previsibilidade, redução de riscos, adequação a protocolos mais rígidos de segurança, etc. Imagine criar um software para controle de máquinas hospitalares sem um planejamento detalhado! Me avisem antes, pra que eu nunca entre nesse hospital!

Dito isso, a *Engenharia de Requisitos*, como descrita no capítulo 4 do Sommerville, embora pareça enferrujada, nos dá alguns direcionamentos sobre a importância de algum tipo de estrutura documental que informe quais são os aspectos imutáveis (ou quase) do software que estamos criando.

A Engenharia de Requisitos é dividida em quatro partes, elicitação, especificação, validação e mudança. Se eu puder reduzir os métodos ágeis a qualquer método que seja iterativo e incremental, é possível fazer engenharia de requisitos com nível menor de detalhe, com maior frequência, e de forma simultânea e/ou intercalada com a implementação do software.

[^1]: Usei a palavra *suposto* aqui por entender que as metodologias ágeis são muito flexíveis em sua implementação e as empresas tendem a trabalhar com um misto de processos para se adequar à sua cultura, tipo de software entregue, exigência regulamentar, tipo de cliente atendido, dentre outros limites. Como não há rigidez na verificação do método, geralmente entende-se que uma empresa é ágil, para todos os efeitos, quando ela diz que é. Como reforço, também trago que a palavra *suposto* não é colocada de maneira pejorativa, pois reconheço a importância e a vantagem de se trabalhar seguindo os valores e princípios ágeis, como especificados no manifesto, inclusive sem estar preso a métodos mais ou menos prescritivos, como o Scrum. Cada time que entrega software está sujeito a condições de funcionamento diferentes, e por isso uma estrutura de valores e princípios como a do manifesto ágil é um ótimo ponto de partida.

## Elicitação
Nessa fase as pessoas responsáveis por documentar o que software precisa fazer, trabalha na definição de requisitos de usuário e requisitos de sistema. Os requisitos de usuário definem como usuário interage com o sistema e são descritos em alto nível, sem termos técnicos, de forma que um usuário ou stakeholder consiga entender. Os requisitos de sistema são mais detalhados e descrevem o que deve ser implementado no sistema e quais restrições de aplicam. É geralmente dentre os requisitos de sistema que os requisitos não funcionais são descritos. 
Ver [Dev + Eficiente: Engenharia de Requisitos para Devs parte 2]({% post_url /estudos/dev-eficiente/eng-requisitos/2025-08-19-eng-requisitos-parte2 %}#tipos-requisitos).

A elicitação de requisitos envolve duas técnicas principais, a entrevista e a etnografia. As duas devem ser feitas em conjunto para que a elicitação seja mais assertiva. 

É possível utilizar na entrevista alguns esboços ou protótipos para ajudar a coletar informações e perguntas mais diretas sobre como o sistema deve funcionar devem ser evitadas. O usuário final raramente sabe o que precisa e é trabalho do analista descobrir isso. Estórias e cenários também podem ser utilizados nas entrevistas para dar mais materialidade às discussões. As estórias são descrições narrativas do funcionamento do sistema do ponto de vista dos usuários, enquanto os cenários são mais detalhados e tratam de fluxos normais, possibilidades de erro e como sistema e usuários devem reagir diante deles. Em futuras etapas, o cenário é um boa entrada para elaboração de casos de teste para validar tanto os requisitos quanto sua implementação.

A etnografia é o processo de observar o fluxo de trabalho atual, a relação entre as pessoas, os aspectos políticos da organização, ou seja, como as pessoas se relacionam em torno da execução do seu trabalho, o qual está sujeito à otimização através de software. Ao elicitar requisitos, é possível que haja conflitos de interesse ou de funcionalidades do sistema que as entrevistas não conseguem captar. Também é possível que a forma com que os processos são definidos dentro da empresa não seja como as pessoas trabalham de fato, e só a observação, via etnografia, permite mapear essa distorção.

## Especificação
A especificação em si é a documentação do que foi elicitado em linguagem natural, de uma forma mais estruturada ainda que textual, ou com a utilização de métodos mais formais como UML. Também é possível combinar livremente esses formatos para manter o equilíbrio entre o que é entendível pelos stakeholders e pelas pessoas que irão fazer a implementação. Muitas vezes o documento de especificação é construído em camadas, focando em requisitos mais gerais e não funcionais, para depois aprofundar para o nível de arquitetura e implementação. 

Nesse ponto é que, ao trabalhar com processos ágeis, o(a) analista tem o papel de identificar o que precisa ser essencialmente especificado, como as principais restrições do sistema e atributos de qualidade geral, além da definição de funcionalidades em formato de User Stories e alguns poucos diagramas como os de sequência e casos de uso. Isso permite que a mudança seja facilmente acomodada dentro da iteração atual ou nas próximas.

## Validação
A validação de requisitos é feita tanto de maneira contínua dentro do processo de elicitação &ndash; à medida que entrevistas recorrentes com uso de protótipos, por exemplo, são feitas &ndash;, quanto após conclusão da elaboração da proposta de documento final na etapa de especificação. Aspectos importantes como custo, verificabilidade dos requisitos, consistência, etc, são validados em reuniões com stakeholders internos e externos. 

## Mudança
Enquanto métodos ágeis aceitam a mudança de forma mais natural, com artefatos documentais que facilitam essa mudança, nos métodos mais tradicionais em cascata, um controle de mudança mais rígido é tomado. Isso é importante quando o desenvolvimento de software está sujeito a um contrato com especificações detalhadas do que deve ser entregue e quando o orçamento ou prazo associado é limitado.

Basicamente são analisadas as mudanças propostas e registradas em log como histórico. As validações de mudanças de escopo, custo e prazo (escolha duas[^2]) são feitas com muita atenção e os contratos podem ser mudados de acordo. Determinadas mudanças, dependendo do tipo de contrato, podem inviabilizar a sua execução.

[^2]: [Project Management Triangle](https://en.wikipedia.org/wiki/Project_management_triangle)

---

😮‍💨 Ufa! Este foi o resumo do capítulo 4 do Sommerville junto com algumas colaborações minhas. Espero que gostem! Até semana que vem!