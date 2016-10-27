# Workshop AO VIVO sobre Socket.io

![socket.io logo](http://www.cnydev.org/wp-content/uploads/2015/03/socketio2.png)

Nesse workshop sobre [Socket.io](http://socket.io/) você irá aprender a criar um sistema de Chat em tempo real, com salas, mensagens privadas e etc.

Hoje em dia o [Socket.io](http://socket.io/) é amplamente utilizado em sistemas web que fazem o uso de informações em tempo real onde o servidor irá enviar os dados sem que o cliente necessite requisita-las, tornando a experiência do usuario mais atrativa.

Com mais de 3,479,533 downloads, e aumentando, no último mês é um dos módulos completos mais utilizados atualmente.

Esse workshop será pago, porém apenas até alcançar a meta dele que é: **R$2000**!

Após alcançarmos essa meta, que deve dar no máximo 3 turmas de 9 alunos, irei liberar **GRATUITAMENTE PARA TODOS**, porém só os alunos doadores terão acesso à um grupo, do Telegram, especial para tirar suas dúvidas de forma mais direta e rápida.

## Ementa

As funcionalidades a serem desenvolvidas nesse módulo são:

- criação de grupos com várias pessoas
- criação de chat individual
- envio de mensagem para algumas pessoas escolhidas
- mostrar quando a pessoa estiver digitando
- mostrar ícone de envio de mensagem
- mostrar ícone de recebimento de mensagem
- mostrar ícone de leitura de mensagem

## Aulas

Teremos 2 tipos de turmas:

- dia de semana: 5 dias de 1 hora cada
- final de semana: 2 dias de 2.5 horas cada

Todas serão **AO VIVO** via Hangouts.

*ps: caso eu ache uma ferramenta melhor e que comporte mais de 10 pessoas poderá ser trocada.*

### Início

O início de cada turma se dará na semana após o fechamento dela que deve ser com 8, mínimo, ou 9 alunos, máximo. Por exemplo:

Estou iniciando a divulgação agora 26 de Setembro de 2016, caso feche até 30 de Stemebro de 2016 esse módulo iniciará em 3 de Outubro de 2016.

## Custo

O custo por aluno será de: **R$120** via Eventick/Pagseguro/Paypal ou com **DESCONTO à vista ficando R$100**.

*ps: à vista apenas via depósito ou transferência bancária para minha conta na Caixa.*

## Pré-requisitos

Os pré-requisitos para esse worksho são bem básicos, caso você já tenha visto os módulos de [Node.js](https://www.youtube.com/playlist?list=PL77JVjKTJT2hP_lxL88oDo2rJvOskpGfJ) e [Angular](https://www.youtube.com/playlist?list=PL77JVjKTJT2hfviaP9JV_ZyJWSD4je7Df) do [Be MEAN](https://www.youtube.com/channel/UCKdo1RaF8gzfhvkOdZv_ojg/playlists?sort=dd&shelf_id=0&view=1) **você já está mais que apto para fazer esse workshop**.

Caso ainda não tenha feito basta saber:

- ler
- escrever
- pensar
- perguntar
- Node.js básico
- AngularJs básico

## Client

Nosso cliente será baseado no Atomic Design e o mesmo *frontend* será feito em:

- Angular 1
- Angular 2
- React
- Vue

### Atomic Design

Primeiramente precisamos definir quais são nossos átomos!

- input para digitar mensagem
- input para digitar nome da sala
- input para digitar seu nome
- botão de enviar mensagem
- botão de criar sala
- título da sala atual
- texto com as mensagens
- texto com nome das salas
- texto com o nome dos usuários

#### Átomos

Antes de tudo definimos os átomos básicos que precisamos para utilizar de base para os átomos anteriormente definidos, então eles serão:

- input/text: .atom-input-text
- button/submit: .atom-button-submit
- h1: .atom-title-primary
- span: .atom-text-line
- p: .atom-text-paragraph


Exemplo em Stylus:

```stylus
.atom-input-text 
  @extend $atom-text-base

```

##### Átomo: input para digitar mensagem

Nesse átomo usaremos o átomo base: `.atom-input-text`. Porém seu identificador será: `.atom-message-text`


```stylus
.atom-message-text
  @extend .atom-input-text
  padding: 0.5rem
```

## Server
