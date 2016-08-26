# Ruby

Para programar, usamos uma linguagem de programação, que é um idioma que permite
que a gente dê comandos para o computador, como uma forma de expressar as
instruções que o computador deve seguir. A linguagem que usaremos é Ruby, uma
linguagem criada para ser fácil de usar.

## Instalação

Para instalar Ruby no seu computador, siga as instruções de acordo com seu
sistema operacional:

### Windows

Primeiro, você deve saber se seu computador roda em 32 ou 64 bits. Veja como
descobrir isso nessa página:
[http://windows.microsoft.com/pt-br/windows/32-bit-and-64-bit-windows#1TC=windows-7](http://windows.microsoft.com/pt-br/windows/32-bit-and-64-bit-windows#1TC=windows-7)
Caso seu computador seja 32 bits, clique aqui:
[http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.2.5.exe](http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.2.5.exe)

Caso seu computador seja 64 bits, clique aqui:
[http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.2.5-x64.exe](http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.2.5-x64.exe)

Quando você clicar no link, um download vai começar. Abra o arquivo baixado e
siga as instruções de instalação.

### Mac OS X

Você já possui Ruby instalado no seu computador!

### Linux

Na linha de comando que mencionamos no capítulo sobre terminais, digite o
seguinte comando: `sudo apt-get install` e aperte *Enter*. Você deverá digitar
sua senha (a mesma que você usa para ligar o computador) e apertar *Enter*.

Para verificar se o Ruby está mesmo instalado, digite o comando `ruby -v` na
linha de comando e aperte *Enter*. Você deve ver uma mensagem informando a
versão do Ruby que você instalou, algo do tipo: `ruby 1.9.3p551`. Agora podemos
usar Ruby!

## Agora sim, vamos falar de Ruby?

Vamos entender algumas coisas básicas do Ruby como variáveis, arrays, métodos,
etc. Vamos dar uma olhada em o que são cada um desses nomes e o que podemos
criar com eles :)

Mas antes de continuarmos vamos conhecer o **irb**. O **irb** é um ambiente
interativo para execução de código ruby, nele conseguimos executar código ruby
de maneira instantânea e ver o resultado do nosso código. Todos os exemplos a
seguir podem executados no **irb**.

Para entrar no **irb** você executa o comando:

```sh
$ irb
```

E ele se parece com isso:

```sh
irb(main):001:0>
```

Para sair do **irb** você precisa digitar `exit` e pressionar Enter.

## Tipos básicos no Ruby

Nas variáveis que guardamos nossos dados e eles podem ser de vários tipos:

* Números inteiros: **Integer**
* Palavras ou frases: **String**
* Números decimais: **Float**
* Valores lógicos (verdadeiro ou falso): **True** e **False**
* Lista de valores: **Array**

### Números inteiros e decimais

**Integers** são números inteiros:

```ruby
paginas = 100
```

**Floats** são números decimais:

```ruby
preco = 4.5
```

Sendo `4,5` o valor no exemplo, pois o Ruby representa esses valores com ponto.

**Obs**: Um ponto importante pra citar aqui, é sobre o nome que damos às
variáveis: elas não devem conter espaços, como podemos ver nas variáveis criadas
aqui o espaço foi substituído por *underline* (\_).

Experimente no **irb** algumas operações com números:

```ruby
(irb)> preco + 2      # 6.5
(irb)> 10 - 4 / - 2   # 12
(irb)> (10 - 4) / - 2 # -3
(irb)> 35 % 6         # 5
```

E também alguns métodos:

```ruby
(irb)> 0.zero?         # serious?
(irb)> 2.even?         # true
(irb)> 0.odd?          # false
(irb)> (1+2).next.next # 5
```

Falaremos mais sobre mais métodos ainda neste capítulo.

### Palavras ou frases

Sempre estarão entre aspas, podendo ser duplas:

```ruby
projeto = "Desejos"
```

Ou aspas simples:

```ruby
projeto = 'Desejos'
```

Esse tipo é chamado **String**.

Formas de trabalhar com **Strings**:

```ruby
(irb)> "O resultado é #{5 + 2}"
"O resultado é 7"
(irb)> Meus + projeto
# "Meus Desejos"
(irb)> '1' * 5
# 11111
(irb)> 'Ê!' * 5
# Ê!Ê!Ê!Ê!Ê!
```

```ruby
(irb)> "casa".include? "asa"  # true
(irb)> "casa".length          # 4
(irb)> "casa".gsub("a","A")   # "cAsA"
(irb)> "  casa  ".rstrip      # "  casa"
(irb)> "casa".count("a")      # 2
(irb)> "2".to_i               # 2
(irb)> 2.to_s                 # "2"
(irb)> "2".to_f               # 2.0
(irb)> "2".rjust(5,"0")       # 00002
```

### Lógicos

Os valores lógicos, chamados de Booleanos, representam verdadeiro e falso.

```ruby
tutora_feliz = true
```

‘**True**’ é verdadeiro em inglês, idioma que a linguagem ruby utiliza.

```ruby
tutora_triste = false
```

‘**False**’ é falso em inglês.

```ruby
(irb)> true != false
# true
(irb)> !true
# false
(irb)> tutora_feliz == 1
# false
(irb)> false.to_s
# "false"
```

### Listas de dados

As listas de dados são chamados de `Array` e serve para armazenarmos valores de
vários tipos:

Palvras ou frases:

```ruby
nomes_das_tutoras = ["Carol", "Bárbara"]
```

Números:

```ruby
idades_das_tutoras = [23, 20]
```

E tudo junto:

```ruby
dados = [10, true, "Carol"]
```

Formas para acessar os dados:

```ruby
(irb)> print nomes_das_tutoras[0]
# Carol
(irb)> dados.at(2)
(irb)> dados.fetch(10, "Não encontrado!")
(irb)> dados[-2]
(irb)> dados.values_at(1,3)
```

Inserindo dados:

```ruby
(irb)> dados << "qualquer coisa"
(irb)> dados.insert(-1,3)
(irb)> dados.push 7
```

Removendo dados:

```ruby
(irb)> dados.pop
(irb)> dados.shift
(irb)> dados.delete_at 4
(irb)> dados.delete 4
```

Outros métodos:

```ruby
(irb)> dados + ["abc"]
(irb)> dados * 2
(irb)> dados.join(", ")
```

### Métodos

São uma forma de agrupar um conjunto de instruções, como se fosse uma receita
que podemos executar utilizando seu nome. Podem receber e retornar valores.

```ruby
def escrever_nome(nome)
  "Seu nome é " + nome
end
```

Ok, mas o que significa tudo isso?

* `def` \- estamos dizendo que estamos definindo um método
* `escrever_nome` \- esse é o nome do nosso método. note que nele subtituímos
  os espaços por traços (\_)
* `(nome)` \- é o parâmetro do nosso método, uma variável que mandamos para o
  método, para que ele faça algo com ela. Métodos podem receber nenhum, um ou
  mais paramêtros.
* `“Seu nome é #{nome}”` \- é o que o método vai retornar para a gente,
  note que usamos o paramêtro nome na frase
* `end` \- estamos dizendo que estamos finalizando o método

Agora utilizando nosso método:

```ruby
texto = escrever_nome("Carol")
```

Assim o método retornaria `"Seu nome é Carol"` e `texto` agora tem essa frase
como valor.

Podemos agora utilizar o método `print` já disponibilizado pelo Ruby para
"imprimir" a frase na linha de comando:

```ruby
texto = escrever_nome("Carol")
print(texto)
```

### Controle de fluxo

Até então escrevemos código que é executado sequenciamente e nesta seção
mostraremos uma forma de controlar o fluxo do programa, a partir de alguma
condição. Com isso poderemos realizar decisões durante a execução da nossa
aplicação.

Por exemplo, vamos imprimir no método `escrever_nome` criado na seção anterior
apenas se o nome não estiver em branco.

```ruby
if nome != ''
  "Seu nome é " + nome
end
```

Outra forma de implementar seria utilizando o método `empty?`

```ruby
if !nome.empty?
  "Seu nome é " + nome
end
```

E nosso método ficaria assim:

```ruby
def escrever_nome(nome)
  if !nome.empty?
    "Seu nome é " + nome
  end
end
```

### Laço de repetição

Em algumas situações precisamos repetir um operação em elementos de um conjunto
de dados e podemos realizar tal tarefa utilizando laços.

Por exemplo, vamos podemos escrever os nomes de uma lista utilizando o `for`:

```ruby
lista_de_nomes = ["Juliana", "Enzo", "Roberto"]

for nome in lista_de_nomes
  escrever_nome(nome)
end

# Note que estamos utilizando o método escrever_nome do exemplo anterior.
```

### Comentários

São partes do código que não serão executados, podem ser usados pra lembrar de
algo naquela parte do código, por exemplo. São muito bons quando estamos
aprendendo, pois podemos comentar o que o código está fazendo:

```ruby
# Este é um comentário que não é executado

def linguagem_de_programacao
  "Ruby"
end
```

Para criarmos um comentário, iniciamos a frase com ‘#’, assim, o ruby sabe que
ali tem um comentário e ele não precisa executar nada.

### Onde aprender mais sobre Ruby?

Abaixo, alguns links que podem ajudar a ver mais sobre ruby, e a treinar um
pouquinho também :)

* [https://www.codecademy.com/pt-BR/courses/ruby-beginner-pt-BR](https://www.codecademy.com/pt-BR/courses/ruby-beginner-pt-BR)
* [http://howtocode.com.br/ebooks/ruby](http://howtocode.com.br/ebooks/ruby)
* [http://tryruby.org/levels/1/challenges/0](http://tryruby.org/levels/1/challenges/0)
  está em inglês, mas é um tutorial muito legal para experimentar a linguagem
