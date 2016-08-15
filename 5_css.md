# CSS

Neste capítulo veremos como trabalhar com cores, fontes, margens no HTML e
aplicaremos na nossa lista de desejos.

## O que é CSS?

Quando tags como e atributos de cor foram adicionados ao HTML, começou um
pesadelo para os desenvolvedores web. Desenvolvimento de grandes sites, onde
fontes e cores informações tinham que ser adicionadas a cada página, tornou o
processo longo e caro. Para resolver este problema, a World Wide Web Consortium
(W3C) criou o CSS.

O CSS (Cascading Style Sheets, em português, Folha de Estilos em Cascata)
controla fontes, cores, margens, linhas, alturas, larguras, imagens de fundo,
posicionamentos e muito mais. Com o CSS é possível criar diversos estilos
diferentes para uma mesma estrutura em HTML.

## Seletores CSS

Os seletores são a forma de indicar em quais elementos estaremos aplicando as
propriedades declaradas.

### Estrutura de um seletor

A estrutura inclui o seletor, nome da propriedade CSS e um valor.

A propriedade e o valor são separados por dois pontos ":" e são cercados por
chaves "{}":

```css
seletor { propriedade: valor; }
```

### Tipos de seletores

**Elemento**: Usa o nome da tag HTML.

```css
elemento { propriedade: valor; }
```

Dessa forma aplicaremos as propriedades em todos os elementos que utilizam a
tag indicada. Exemplo, todos itens de lista terão a cor azul:

```css
li { color: blue; }
```

**Identificador**: Usa o atributo `id` de um elemento HTML para selecionar um
elemento específico. O `id` de um elemento deve ser único dentro de uma página.
No CSS identificamos o tipo `id` com o caracter "#" (hashtag).

```css
#id-do-elemento { propriedade: valor; }
```

Assim podemos indicar pelo atributo `id` qual elemento deve receber tal
propriedade. Exemplo, elemento com `id` "nome" terá o tamanho de fonte 13px:

```css
#nome { font-size: 13px; }
```

**Classe**: Usa o atributo "class" das tags HTML. A mesma classe pode ser
utilizada várias vezes na mesma página. No CSS identificamos o tipo classe com
o caracter "." (ponto).

```css
.classe-do-elemento { propriedade: valor;}
```

Assim podemos selecionar vários elementos com a mesma classe. Exemplo, todos os
itens com a classe "favorito" terão a cor amarela como fundo:

```css
.favorito { background-color: yellow; }
```

### Principais propriedades do CSS

O CSS possui diversas propriedades, aqui estão algumas delas:

* `font-family` - Define a família da fonte utilizada.
* `font-style` - Define a propriedades de estilos que podem ser: normal,
  italic ou oblique.
* `font-size` - Define o tamanho da fonte. Tem que utilizar uma unidade de
  medida (px, em, etc)
* `text-align` - Controla o posicionamento do conteúdo de um elemento. Os
  valores possíveis são: left, right, center e justify.
* `color` - Define a cor de um texto. Pode ser em hexa, RGB ou nome em inglês.
* `width` - Define a largura de um elemento. Tem que utilizar uma unidade de
  medida (px, em, etc)
* `height` - Define a altura de um elemento. Tem que utilizar uma unidade de
  medida (px, em, etc)
* `border` - Define bordas para um elemento. Tem que ter a espessura, tipo e a
  cor.
* `background` - Define as propriedades relacionadas ao fundo de exibição:
  `background-color`, `background-image`, `background-repeat`,
  `background-attachment`, `background-position`

## Utilizando CSS no HTML

Agora que já criamos um arquivo HTML e vimos como funciona o CSS, como juntar
os dois? Temos 3 maneis de fazer isso: folha de estilo externa, folha de
estilo interna e estilo em linha.

### Folha de estilo externa

Com uma folha de estilo externa, é possível alterar a aparência de um site
inteiro, alterando apenas um arquivo. O arquivo de folha de estilo externo
deve ser salvo com uma extensão `.css` .

Cada página HTML deve incluir uma referência para o arquivo de folha de
estilo externa no interior do elemento `<link>`. O elemento `<link>` vai
dentro da seção `<head>` (logo acima do `<body>`):

```html
<html>
  <head>
    <link rel="stylesheet" href="site.css" type="text/css">
  </head>
  <body>
    (...)
  </body>
</html>
```

### Folha de estilo interna

Uma folha de estilo interna pode ser usada se uma única página e tem um
estilo único. Estilos internos são definidos dentro do elemento `<style>`,
dentro da seção `<head>` de uma página HTML:

```html
<html>
  <head>
    <style>
      elemento { propriedade: valor; }
    </style>
  </head>
  <body>
    (...)
  </body>
</html>
```

### Estilo em linha

Um estilo em linha pode ser usado para aplicar um modelo exclusivo em um
único elemento.
Para usar estilos em linha, adicione o atributo de estilo `style` ao
elemento relevante. O atributo de estilo pode conter qualquer propriedade CSS.
Este estilo não é muito recomendado, pois pode causar re-trabalho e códigos
confusos.

```html
<h1 style="color: blue; margin-left: 30px;">Título</h1>
```
