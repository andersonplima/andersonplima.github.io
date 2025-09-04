---
layout: post
title:  "Qualidade de Software em Aplicações Modernas parte final"
date:   2025-09-04 22:23:00 +0000
image: /assets/images/estudos/dev-eficiente/design-codigo/qualidade/qualidade-software-3-cover.jpg
---
As aulas de hoje foram focadas na última indicação do autor do curso sobre como podemos obter
um código de boa qualidade. 
Ele indica que devamos ter uma linha guia (*guideline*) de codificação que deve ser seguido 
por todo time. 
Ele também fala que ter essa linha guia é mais importante do que o conteúdo dela em si.
De qualquer forma, há uma sugestão de alguns itens que podem estar contidos na linha guia.

### Métrica CDD

A métrica CDD consiste em dar pesos para determinadas características do código para computar um peso total. Por exemplo:
- Condicionais e loops valem 1 unidade.
- Tratamento de erros valem 2 unidades.
- Uso de classes internas do projeto vale 1 unidade.
- *Efeitos colaterais*[^1] valem 1 unidade.
Tanto os valores exatos, quanto o que o time considera como complexo pode variar a gosto do freguês. O importante é que 
isso seja somado para dar uma complexidade total e que a linha guia qual valor máximo aceitável.

### Testes automatizados

Sobre testes automatizados, o seu guia pode definir:
- O percentual de cobertura mínimo.
- Os testes devem ser de comportamento e não de implementação.
- Mantenha o tempo de execução o menor possível.
- Teste valores limite (null, infinito, valores negativos, etc).

### Log

Os logs devem ser feitos de maneira sistemática e uniforme dentro do sistema. De preferência deixe uma função de log 
pronta para ser usada em todo o projeto, já prevendo os níveis de criticidade (erro, alerta e debug) e quais informações
são obrigatórias no log. Defina no seu guia em que situações são usados cada nível de criticidade.

### Coesão

- Mantenha os arquivos que trabalham no mesmo contexto próximos uns dos outros para facilitar a leitura do código do projeto.
- Mantenha os métodos que validam atributos de uma classe dentro da própria classe. Isso também vale para DTOs com classes mapeadoras: prefira utilizar métodos de conversão dentro do próprio DTO.
- Se você está trabalhando numa arquitetura MVC ou numa API com controllers, mantenha esses controllers coesos, ou seja, 
mantenha no mesmo controller, apenas as rotas que são executadas por funções que têm as mesmas dependências. Isso evita que você tenha controllers muito grandes e de difícil leitura para atender telas complexas de um sistema.

### Generalização

Analise sempre se seu código está fazendo generalizações precoces, sem que haja naquele momento cenários de uso diferentes. O risco que se quer evitar é que a generalização esteja fraca o suficiente, por falta de conhecimento dos possíveis cenários futuros, pra que uma vez que o cenário chegue, seja necessário mudar completamente a generalização. Isso é muito comum de acontecer e o custo de generalizar na hora certa é mínimo. Isso é muito alinhado com o princípio KISS! (Keep It Simple, Sucker!) que você pode chamar de forma mais educada de *Complique Apenas Quando Realmente Necessário*.

[^1]: Efeitos colaterais são ações que afetam o mundo externo, como leitura e escrita de arquivos, chamadas HTTP, etc.

---

A linha de raciocínio de Alberto no que diz respeito a como agir diante da sua codebase é muito em linha com o que eu penso:
o de não ter padrões de estimação, de entender e atender o negócio acima de tudo e começar simples sempre. 

Até o próximo passo da jornada! ☕