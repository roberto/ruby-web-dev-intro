# HTML

Neste capítulo vamos falar sobre HTML, aprender sobre HTML nos ajudará a criar
a estrutura de uma página que contém uma lista de desejos.

## O que é HTML?

Na base da estrutura de uma página da Web está o HTML (HyperText Markup Language
ou, em português, Linguagem de Marcação de HiperTexto). HTML é o que o
navegador "lê" para apresentar a página ao usuário em frente ao computador.
Para o browser conseguir ler o arquivo, é preciso criá-lo com extensão ".html"
ou “.htm”, caso contrário o browser não irá renderizar o conteúdo corretamente.

## Tags HTML

As tags são rótulos usados para informar ao navegador como deverá apresentar o
site. Ou seja, quando escrevemos HTML estamos escrevendo tags que serão
interpretadas pelo navegador, resultando no visual do site.

Exemplo: A tag "h1" serve para escrever um título, ao inserí-la em um arquivo
HTML o browser irá exibir um texto com a formatação de um título.

![imagem de exemplo da tag h1](images/4_html/exemplo_h1.png)

## Estrutura de uma tag

Todas as tags possuem um formato que deve ser utilizado pelos desenvolvedores
web na hora de codificar.
As tags começam com um sinal de "<" e terminam com um sinal de ">".

## Tags de abertura e de fechamento

Tag de abertura, inicia a marcação do código:

```html
<nomedatag>
```

Tag de fechamento, finaliza com uma barra a marcação do código:

```html
</nomedatag>
```

O conteúdo que deverá ser exibido na página deve estar entre as tags de
abertura e fechamento. Exemplo:

```html
<h1>Título da página</h1>
```

Alguns casos não precisam de duas tags, uma de abertura e outra para
fechamento, pois o fechamento ocorre dentro da própria tag.

Tag para adicionar nova linha em branco:

```html
<br />
```

## Algumas regras das tags HTML

* As tags podem ser escritas tanto em maiúsculas como em minúsculas: `<h1>` ou
  `<H1>` (o mais utilizado é em minúsculo)
* Não pode haver espaços na declaração das tags: `< h1 >`
* Todas as tags devem ser fechadas: `<h1>Sub título</h1>` ou `<br />`

## Tags encadeadas

É possível encadear várias tags para que tenhamos uma estrutura de conteúdos
inseridos um dentro do outro.

Exemplo:

```html
<tag>
  <tag1>conteudo</tag1>
  <tag />
</tag>
```

Dica:

> Para conseguir adicionar estes espaços antes de uma tag, é só apertar a tecla
> `tab` do seu computador que o editor de texto adiciona com o espaçamento
> correto. Estes espaços antes das tags são importantes, pois facilitam a
> leitura do código e deixam clara a hierarquia dos elementos.

## Principais tags HTML

O HTML possui diversas tags, aqui estão algumas e para que servem:

```html
<body></body> corpo da página, onde colocamos outras tags
<p></p> parágrafos
<a></a> links
<h3></h3> títulos, de 1 a 6
<ul> lista não ordenada
  <li></li> itens de listas
</ul>
<div></div> para dividir a página em seções
<table></table> tabelas
<td></td> colunas de tabelas
<tr></tr> linha na tabela
<form> para agrupar entradas de um formulário
  <input /> campos de formulário
  <select> para agrupar opções para seleção
    <option></option> opções
  </select>
</form>
```

Exemplo:

```html
<div>
  <p>Sou um parágrafo dentro de uma div</p>
  <table>
    <tr>
      <td>Coluna 1 - Linha 1</td>
      <td>Coluna 2 - Linha 1</td>
    </tr>
    <tr>
      <td>Coluna 1 - Linha 2</td>
      <td>Coluna 2 - Linha 2</td>
    </tr>
  </table>
</div>
```

Resultado:
<!-- markdownlint-disable MD033 -->

---
<div>
  <p>Sou um parágrafo dentro de uma div</p>
  <table>
    <tr>
      <td>Coluna 1 - Linha 1</td>
      <td>Coluna 2 - Linha 1</td>
    </tr>
    <tr>
      <td>Coluna 1 - Linha 2</td>
      <td>Coluna 2 - Linha 2</td>
    </tr>
  </table>
</div>

---
<!-- markdownlint-enable MD033 -->

## Criando nosso primeiro arquivo HTML

Vamos agora criar uma lista de desejos, podem ser presentes, utilizando HTML.

### Passo a passo

* Crie um arquivo chamado `lista.html` no seu editor em alguma pasta do seu
  computador
* Abra o arquivo e digite:

```html
<html>
  <body>
    <h1>Minha Lista de Desejos!</h1>
  </body>
</html>
```

* Salve o arquivo
* Abra o arquivo em algum navegador (Firefox, Chrome, Safari, etc.)
* Voilà! \o/

Agora vamos adicionar uma lista logo após nosso título:

```html
<html>
  <body>
    <h1>Minha Lista de Desejos!</h1>
    <ul>
      <li>Mais uma temporada do meu seriado favorito</li>
      <li><b>Unicórnio</b> de pelúcia</li>
    </ul>
  </body>
</html>
```

Experimente também utilizar a tag `ol` em vez de `ul` ou até mesmo `table`.
Escreva seu nome, seu aniversário ou a data de uma festa. Tente utilizar as
tags da sessão "Principais tags HTML" para ver o resultado na página.

## Atributos de tags

As tags podem ter atributos. Um atributo possui um nome e um valor, e é
utilizado para adicionar informações extras ao elemento. Esta informação
pode ser algo que indique como o conteúdo deve ser renderizado, que
identifique a ocorrência única do elemento, entre outras possibilidades.

O atributo de um elemento é sempre escrito dentro da tag de abertura logo após
o nome e tem o padrão nomedoatributo + sinal de igual + valor entre aspas.

```html
<tag nomedoatributo="valor"></tag>
```

Exemplo:

```html
<a href="http://www.facebook.com/">Facebook</a>
a - tag de link
href - atributo com a url do link
```

Resultado:

---
[Facebook](http://www.facebook.com/)

---

### Atributos de algumas tags

Tag `<input>`:

* type – Tipo de dado: text, file, radio, checkbox, hidden, password, submit,
  reset, button, image
* name – Identificação do campo
* maxlength – Número máximo de caracteres permitidos
* value – Texto que aparece dentro da caixa ou nome do botão

Tag `<img>`:

* src - Localização da imagem (caminho no computador, url, etc)
* alt - Descrição da imagem
* width - Largura da imagem
* height - Altura da imagem

Tag `<a>`:

* href - URL da página destino
* target - Especifica onde é para o link abrir: \_blank (nova página),
  \_parent, \_self (mesma página), \_top

## Adicionando links

Agora que abordamos atributos de tags, vamos experimentar adicionar links nos
itens da lista adicionando a tag `<a>` em volta dos textos e utilizando o
atributo `href` para indicar a página destino:

```html
<li>
  <a href="http://disneyxd.disney.com.br/gravity-falls/">
    Mais uma temporada do meu seriado favorito
  </a>
</li>
```

## Cabeçalho

Algumas tags fazem parte do cabeçalho e alteram algum comportamento da página
sem aparecerem como conteúdo visível na página, sendo meta informações.

Devem ser adicionadas dentro da tag `head`:

```html
<html>
  <head>
    <!-- adicione as tags aqui -->
  </head>
  <body>
  </body>
</html>
```

Por exemplo, podemos utilizar a seguinte tag abaixo para acentuar palavras sem
ter problemas:

```html
<meta charset="utf-8">
```

E com a tag `title` podemos alterar o título da janela (ou aba) no navegador:

```html
<title>Lista de Desejos</title>
```

## Criando um formulário

Vamos experimentar criar um formulário. Crie um arquivo chamado
`formulario.html` com o seguinte conteúdo:

```html
<html>
  <body>
    <form action="/novo" method="post">
      <label>Desejo:</label>
      <input type="text" name="desejo" />
      <button type="submit">Enviar</button>
    </form>
  </body>
</html>
```

Na definição da tag `form` indicamos como e para onde os dados dos campos serão
enviados:

```html
<form action="/novo" method="post">
```

Usamos `label` para termos um rótulo para nosso campo de entrada:

```html
<label>Desejo:</label>
```

A tag `input` indica o tipo de entrada e o nome que será utilizado para
representar a informação ao submeter ao conteúdo:

```html
<input type="text" name="desejo" />
```

E por fim, adicionamos o botão para o envio do formulário:

```html
<button type="submit">Enviar</button>
```

Faremos este formulário funcionar no capítulo sobre Sinatra, por enquanto
experimente alterações como:

* `textarea` em vez de `input`
* renomeie o botão de envio
* adicione outro campo com outro `label`

## Onde aprender mais sobre HTML?

Abaixo, alguns links que podem ajudar a ver mais sobre HTML:

* [https://developer.mozilla.org/pt-BR/docs/HTML/Introduction](https://developer.mozilla.org/pt-BR/docs/HTML/Introduction)
* [https://www.codecademy.com/pt-BR/learn/web](https://www.codecademy.com/pt-BR/learn/web)
