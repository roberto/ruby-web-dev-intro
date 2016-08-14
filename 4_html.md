# HTML

Neste capítulo vamos falar sobre HTML e criaremos a estrutura da uma página com
uma lista de desejos.

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

Todas as tags possuem um formato, que deve ser utilizado na hora de codificar
pelos desenvolvedores web.
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

Alguns casos não precisam de tuas tags, uma de abertura e outra para
fechamento, pois o fechamento ocorre dentro da própria tag.

Tag de imagem:

```html
<img />
```

Tag para adicionar nova linha em branco:

```html
<br />
```

## Algumas regras das tags HTML

* As tags podem ser escritas tanto em maiúsculas como em minúsculas: `<h1>` ou
  `<H1>` (o mais utilizado é em minúsculo)
* Não pode haver espaços na declaração das tags: `< h1 >`
* Todas as tags devem ser fechadas: `<h1>Sub título</h1>` ou `<br />`

## Tags aninhadas

É possível aninhar várias tags, para que tenhamos uma estrutura de conteúdos
um dentro do outro.

Exemplo:

```html
<tag>
  <tag1>conteudo</tag1>
  <tag />
</tag>
```

Dica:

> Para conseguir adicionar estes espaços antes da tag, é só apertar a tecla
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
<ul></ul> listas não ordenada
<li></li> itens de listas
<div></div> para dividir a página em seções
<table></table> tabelas
<td></td> colunas de tabelas
<tr></tr> linha na tabela
<input /> campos de formulário
<select> seleção múltipla
  <option></option> opções para seleção
</select>
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

## Onde aprender mais sobre HTML?

Abaixo, alguns links que podem ajudar a ver mais sobre HTML:

* [https://developer.mozilla.org/pt-BR/docs/HTML/Introduction](https://developer.mozilla.org/pt-BR/docs/HTML/Introduction)
* [https://www.codecademy.com/pt-BR/learn/web](https://www.codecademy.com/pt-BR/learn/web)
