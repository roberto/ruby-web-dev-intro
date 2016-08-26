# Sinatra

Agora que já aprendemos um pouco sobre Ruby, vamos colocar em prática. O Sinatra
é uma forma de criar aplicações web que utilizaremos neste capítulo.

## Instalação

Para instalar o Sinatra precisamos executar o seguinte comando no terminal:

```sh
$ gem install sinatra
```

## Nosso primeiro exemplo, Olá Mundo!

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

## Segundo exemplo, Minha Lista de Desejos

Crie um arquivo (por exemplo: `lista_de_desejos.rb`) com o seguite conteúdo:

```ruby
require 'sinatra'

lista_de_desejos = [
  'Unicórnio Fofinho',
  'Livro com cheiro de novo',
  'Nova temporada da minha séria favorita'
]

get '/' do
  erb(:lista, locals: { desejos: lista_de_desejos })
end
```

Agora crie uma pasta chamada `views`, no terminal execute os seguintes comandos:

```sh
mkdir views
```

Após isso, entre na pasta com `cd views` e crie o arquivo `lista.erb` com o
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

# (...)

erb(:lista, locals: { desejos: lista_de_desejos })
```

Diferente do exemplo anterior, neste utilizamos primeiras linhas para criar uma
variável chamada de `lista_de_desejos` e armazenamos nossos desejos.
Para em seguida utilizar o método `erb` e passar para ele dois paramêtros.

O primeiro paramêtro identifica qual o modelo representa a página que o usuário
irá ver no navegador.

O segundo paramêtro é responsável por indicar para o modelo quais são os desejos
que iremos mostrar na página.

## Terceiro exemplo, adicionando um formulário

Agora vamos utilizar um formulário para adicionar novos desejos. Adicione na
pasta `views` um arquivo chamado `formulario.erb` com o código do formulário
que criamos no capítulo sobre HTML:

```html
<html>
  <body>
    <form method="post" action="/novo">
      <input type="text" name="desejo" />
      <button type="submit">Enviar</button>
    </form>
  </body>
</html>
```

E no arquivo `lista_de_desejos.rb` vamos tratar o envio do formulário da
seguinte forma:

```ruby
get '/novo' do
  erb :formulario
end

post '/novo' do
  lista_de_desejos << params[:desejo]
  redirect '/desejos'
end
```

Adicione um link no arquivo `lista.erb` para o formulário utilizando o seguinte
código:

```html
<a href="/novo">Novo Desejo</a>
```

Ao reiniciar nossa aplicação, podemos acessar
"[http://localhost:4567/](http://localhost:4567/novo)" para abrir o formulário
e adicionarmos outros desejos na lista.

## Entendendo nosso terceiro exemplo

Ao acessar o caminho `/novo` será executado o bloco de código que carrega o
modelo para a página do formulário:

```ruby
get '/novo' do
  erb :formulario
end
```

Já o formulário, ao ser submetido, indica à nossa aplicação qual o método da
solicitação e o caminho, no caso a ação:

```html
<form method="post" action="/novo">
```

Fazendo com que o seguinte bloco seja executado:

```ruby
post '/novo' do
```

O `get`, que utilizamos nos exemplos anteriores, serve para visualizar algum
recurso, como a lista de desejos ou o formulário. Já o `post` utilizamos para
adicionarmos um novo recurso, no nosso caso um novo desejo. Para conhecer outros
métodos de solicitação, acesse:
[https://pt.wikipedia.org/wiki/HTTP](https://pt.wikipedia.org/wiki/Hypertext_Transfer_Protocol#M.C3.A9todos_de_solicita.C3.A7.C3.A3o)

O bloco executado realiza duas ações, adiciona o novo desejo na nossa lista de
desejos e redireciona o navegador para o caminho `/desejos`. O novo desejo é
recebido como um parâmetro da solicitação, utilizando o mesmo nome que foi
utilizado na campo do formulário, no caso `desejo`.

```ruby
  lista_de_desejos << params[:desejo]
  redirect '/desejos'
```

## Onde aprender mais sobre Sinatra?

* [http://www.sinatrarb.com/intro-pt-br.html](http://www.sinatrarb.com/intro-pt-br.html)
