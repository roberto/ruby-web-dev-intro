# Sinatra

Agora que já aprendemos um pouco sobre Ruby, vamos colocar em prática. O Sinatra
é uma forma de criar aplicações web que utilizaremos neste capítulo.

## Instalação

Para instalar o Sinatra precisamos executar o seguinte comando no terminal:

```sh
$ gem install sinatra
```

## Nosso primeiro exemplo

Crie um arquivo (por exemplo: `ola.rb`) com o seguite conteúdo:

```ruby
require 'sinatra'

get '/' do
  'Olá Mundo!'
end
```

Execute no terminal:

```sh
ruby ola.rb
```

Então acesse "[http://localhost:4567/](http://localhost:4567/)" no seu navegador.

Para finalizar a execução da sua aplicação, aperte *Control + C*.

## Entendendo nosso exemplo

Vamos agora destrinchar nosso exemplo.

```ruby
require 'sinatra'
```

Primeiramente estamos carregando o Sinatra, disponibilizando assim componentes
do mesmo na nossa aplicação:

```ruby
get '/' #(...)
```

O `get` é um método do Sinatra, que serve para indicarmos como responder a
solicitação de uma página, no caso a página raiz do nosso site, o `/`, que por
sua vez é o primeiro parâmetro.

```ruby
do
  "Olá Mundo"
end
```

O bloco de código passado para o `get` indica como responderemos a solicitação,
no caso retornando a frase `"Olá Mundo!"`.

## Nosso segundo exemplo, Minha Lista de Desejos

Crie um arquivo (por exemplo: `lista_de_desejos.rb`) com o seguite conteúdo:

```ruby
require 'sinatra'

get '/' do
  lista_de_desejos = [
    'Unicórnio Fofinho',
    'Livro com cheiro de novo',
    'Nova temporada da minha séria favorita'
  ]

  erb(:inicio, locals: { desejos: lista_de_desejos })
end
```

Agora crie uma pasta chamada `views`, no terminal execute os seguintes comandos:

```sh
mkdir views
```

Após isso, entre na pasta com `cd views` e crie o arquivo `inicio.erb` com o
seguinte conteúdo:

```erb
<html>
  <body>
    <h1>Minha Lista de Desejos!</h1>
    <ul>
    <% for desejo in desejos %>
      <li><%= desejo %></li>
    <% end %>
    </ul>
  </body>
</html>
```

Execute no terminal:

```sh
ruby lista_de_desejos.rb
```

Então acesse "[http://localhost:4567/](http://localhost:4567/)" no seu navegador.

Para finalizar a execução da sua aplicação, aperte *Control + C*.

## Entendendo nosso segundo exemplo

Assim como no exemplo anterior, criamos um bloco de código que passamos para o
método `get`. Como podemos ver à seguir:

```ruby
  lista_de_desejos = [
    'Unicórnio Fofinho',
    'Livro com cheiro de novo',
    'Nova temporada da minha séria favorita'
  ]

  erb(:inicio, locals: { desejos: lista_de_desejos })
```

Diferente do exemplo anterior, neste utilizamos primeiras linhas para criar uma
variável chamada de `lista_de_desejos` e armazenamos nossos desejos.
Para em seguida utilizar o método `erb` e passar para ele dois paramêtros.

O primeiro paramêtro identifica qual o modelo representa a página que o usuário
irá ver no navegador.

O segundo paramêtro é responsável por indicar para o modelo quais são os desejos
que iremos mostrar na página.

### Onde aprender mais sobre Sinatra?

* [http://www.sinatrarb.com/intro-pt-br.html](http://www.sinatrarb.com/intro-pt-br.html)
