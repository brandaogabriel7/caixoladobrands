---
{"dg-publish":true,"dg-path":"Tecnologia/Event Storming.md","permalink":"/tecnologia/event-storming/","tags":["fleeting"],"created":"2024-02-21T16:20:58.365-03:00","updated":"2026-01-23T14:24:56.762-03:00"}
---

- É uma técnica que entra na parte estratégica/conceitual do DDD.
- Com o Event Storming é possível ter um entendimento muito mais profundo do domínio.
- É uma técnica para entender de forma mais clara o domínio das aplicações através dos eventos gerados por elas.
- Geralmente ocorre em formato de workshop entre a área técnica e os domain experts. É comum que se use post-its e faça presencialmente mas existem alternativas para que seja realizada remotamente.
- O Event Storming não é a única forma de buscar essa clareza mas ele busca ser mais dinâmico.
## Mapeamento dos eventos
- A ideia é entender o que o sistema faz com base em seus eventos.
- Domain Events
    - Verbo no passado, algo que já aconteceu
    - Relevante para os domain experts
    - Todo evento pode ter um post-it de uma cor específica.
### Eventos de finalização de eventos
- Destacar mais os eventos que indicam finalização de uma parte relevante da aplicação. Dessa forma fica fácil distinguir entre eventos pequenos e grandes
## Comandos
- Todo evento gerado é feito através de um comando.
- Quais são as operações do meu sistema e quem as realizou?
## Atores
- Entender quem são os atores ajuda a saber quem deve participar do Event Storming, quais Domain experts devem ser envolvidos
## Pontos de decisão e policies
### Pontos de decisão
- Há momentos em que decisões precisam ser tomadas com base em algum dado.
    - Onde e como esse dado é obtido não é importante nesse momento. Essa é uma complexidade acidental, não de negócio.
### Políticas
- A chave para pensar em políticas é "Sempre que" (Whenever). A política (policy) descreve algo que deve acontecer com base em um gatilho.
- Pode ser automatizada ou manual.
## Cronologia
- Serve para definir a ordem em que os eventos ocorrem
- Alguns eventos podem, inclusive, ocorrer de forma paralela
## Origens dos eventos
- Os eventos podem ter diversas origens:
    - A ação de um usuário
    - Gerado por sistema externo
    - Por tempo
    - Consequência de outro evento (por meio de uma policy)
## Formação de agregados
- Entre um comando e um domain event, sempre tem um agregado
- As regras de negócio desse agregado participam desses eventos e comandos
- Então, nesse ponto do Event Storming, podemos começar a perceber os agregados
## Definindo contextos delimitados
- Alguns eventos podem conectar áreas diferentes. Esses são eventos pivô, servem de transição entre as áreas.
- Isso pode nos ajudar a perceber contextos delimitados.
- Não existe fórmula mágica para delimitação dos contextos, mas algumas coisas podem ser observadas como indicação de mudança de contexto:
    - Palavras diferentes sendo usadas com o mesmo significado
    - Palavras iguais sendo usadas com significados diferentes
    - Quando sistemas diferentes estão "observando" o mesmo evento.
- Mesmo seguindo várias técnicas, sempre podemos encontrar áreas cinzentas, onde não há clareza de qual área é responsável pelo quê e nem todos estão na mesma página.
- Essas áreas cinzentas podem trazer muita discussão até que os impasses sejam resolvidos. Mas é importante observar que tudo isso acontece antes que qualquer código seja desenvolvido para que esses problemas não sejam encontrados no meio do processo de desenvolvimento.
- É importante observar, também, as novas ideias e oportunidades, além dos possíveis riscos e pontos que precisam ser revisados.
## Arrow voting
- Às vezes, nem todos vão chegar num consenso nas tomadas de decisão. Nesses momentos, uma possibilidade para resolver o impasse é utilizar votação.
- Quem está conduzindo o workshop deve ter muito cuidado para fazer a votação de forma a manter o clima leve.
## Contextos e microsserviços
- A divisão de contextos pode ser um ponto de partida para divisão em microsserviços