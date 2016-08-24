# Sinatra

Agora que já aprendemos um pouco sobre Ruby, vamos colocar em prática. O Sinatra
é uma forma de criar aplicações web que utilizaremos nesta seção.

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

### Onde aprender mais sobre Sinatra?

* [http://www.sinatrarb.com/intro-pt-br.html](http://www.sinatrarb.com/intro-pt-br.html)
