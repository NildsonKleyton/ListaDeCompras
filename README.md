# Sumário 
[HTML Conceitos](#html-conceitos)
1. [O que é HTML](#o-que-é-html) 
2. [Comentário no HTML](#comentário-no-html)
3. [Anatomia das Tags](#anatomia-das-tags)
4. [Atributos Globais mais utilizados](#atributos-globais-mais-utilizados)
   - [class](#classe)
   - [contenteditable](#contenteditable)
   - [data](#data)
   - [hidden](#hidden)
   - [id](#id)
   - [style](#style)
   - [tabindex](#tabindex)
   - [title](#title)
5. [Aninhamento de tags](#aninhamento-de-tags)
   -  [Hierarquia](#hierarquia)
   -  [Fluxo](#fluxo)
   -  [Posicionamento dos elementos](#posicionamento)
6. [Conteúdo do Texto e Caracteres Reservado](#conteúdo-do-texto-e-caracteres-reservado)
   - [Caracteres Reservado](#caracteres-reservado)
7. [Anatomia do Documento HTML](#anatomia-do-documento-html)
8. [Semântica](#semântica)
   1. [Títulos ou Cabeçalhos](#títulos-ou-cabeçalhos)
   2. [Listas](#listas)
   3. [Citações](#citações)
   4. [Abreviação](#abreviação)
   5. [Detalhe de contato](#detalhe-de-contato)
   6. [Lista de Descrição](#lista-de-descrição)
      - [Múltiplos termos e definições](#mtd)
      - [Termo e definição única](#tdu)
      - [Múltiplos termos, definição única](#m-u)
      - [Termo único, múltiplas definições](#u-m)
   7. [Representação de Código](#representação-de-código)

<br><hr>
<h1 align="center">HTML Conceitos</h1>

## **O que é HTML**
&emsp;**HTML->** Hypertext Markup Language ( _Linguagem de Marcação de Hipertexto_ )
 
## **Comentário no HTML**
&emsp;Para usar comentário no _HTML_ utilizamos assim _"\<!-- Comentário -->"_.
Tudo que estiver dentro do espaço para comentário não aparecerá na página.

## **Anatomia das Tags**
- **Abertura de tag**<br>
  &emsp;_\<h1>_
- **Fechamento de tag**<br>
  &emsp;_\</h1>_
- **Conteúdo**<br>
  &emsp;_\<h1> Conteúdo aqui \</h1> <br>_
  &emsp;O conteúdo de uma Elemento pode ser outro Elemento.
- **Elementos**<br>
  &emsp;O _\<h1>_ é um elemento com com abertura, conteúdo e fechamento.
- **Elementos Vazios**<br>
  &emsp;O _\<img>_ é um elemento apenas com a abertura e contem atributos
- **Atributos**<br>
  &emsp;Atributos em um elemento serve para por **informações extras** ou como **configurações**.<br>
  **Ex.:** \<img src="" alt=""> onde **src** e **alt** são os atributos.
  - **Anatomia do Atributo**<br>
    nome=_"conteúdo"_
  - **Atributos boolean**<br>
    São os atributos que não precisam de conteúdo.<br>
    **Ex.:**
    ```html
    <input type="text" disabled /> <br />
    ```
    O _"disabled"_ significa desabilitado, o input é visível, mas nao pode ser usado.

## **Atributos Globais mais utilizados**
<id id="classe">

- **class:**<br>
  &emsp;Usado para classificar o elemento, utilizando no CSS e no JavaScript
  **Ex.:**
  ```html
  <div class="nome-da-class">conteúdo\</div>
  ```
  **Resultado** <div class="nome-da-class">conteúdo</div><br>
<id id="contenteditable">

- **contenteditable:**<br>
  &emsp;Permite editar o conteúdo de um elemento na página, sempre que atualizar a página o conteúdo volta a origem.<br>
  **Ex.:**
  ```html
  <div contenteditable="true">Modifique esta frase.</div>
  ```
  **Resultado:** <div contenteditable="true">Modifique esta frase.</div><br>
<id id="data">

- **data- \*:**<br>
  &emsp;Utilizado no JavaScript e também no CSS.<br>
  ```html
  <div data-id="">conteúdo\</div>
  ```
<id id="hidden">

- **hidden:**<br>
  &emsp;Esconde o elemento na página. Tipo boolean.<br>
  **Ex.:**
  ```html
  <div hidden>conteúdo\</div>
  ```
<id id="id">

- **id:**<br>
  &emsp; _"id"_ só pode ter um por página, ou seja, o valor do id="valor" não pode repetir, podendo ter problemas no CSS ou JavaScript por esta repetindo.
  **Usamos assim:**
  ```html
  <div id="car">conteúdo de carro</div>
  <div id="moto">conteúdo de moto</div>
  ```
<id id="style">

- **style:**<br>
  &emsp;Utilizada para da estilo a um elemento, usando o CSS, geralmente é usado em arquivos esternos.
  **Ex.:**
  ```html
  <div style="color:red ; width: 300px; border: 1px solid">conteúdo\</div>
  ```
  **Resultado**
  <div style="color:red ; width: 300px; border: 1px solid"> conteúdo</div><br>
<id id="tabindex">

- **tabindex:**<br>
  &emsp;Conforme é pressionado a tecla **_Tab_** no teclado, o curso move de acordo ao valor da tabindex<br>
  **Ex.:**<br>
  ```html
  <input type="text" tabindex="1" /><br />
  <input type="text" tabindex="3" /><br />
  <input type="text" tabindex="2" /><br />
  <input type="text" tabindex="4" /><br />
  ```
  **Resultado:**<br>
  \<input type="text" tabindex="1"><input type="text" tabindex="1"><br>
  \<input type="text" tabindex="3"><input type="text" tabindex="3"><br>
  \<input type="text" tabindex="2"><input type="text" tabindex="2"><br>
  \<input type="text" tabindex="4"><input type="text" tabindex="4"><br>
<br>
<id id="title">

- **title:**
  &emsp;Define um título da tag, não muda na visualização na página, e mostra o título quando o mouse esta sob a tag.<br>
  **Ex.:**
  ```html
  <div title="Define um título">Deixe o mouse sobre a esta frase.</div>
  ```
  **Resultado:**<br>
  <div title="Define um título">Deixe o mouse sobre a esta frase.</div>

## **Aninhamento de tags**
<id id="hierarquia">

- **Hierarquia** <br>
  &emsp;Podemos ter um elemento dentro de outro, gerando uma hierarquia.<br>
  Abaixo temos a tag _"div"_ que é pai da tag _"p"_.

  ```HTML
  <div>
    <p>Um texto aqui</p>
  </div>
  ```
<id id="fluxo">

- **Fluxo**<br>
  Abaixo temos um erro de fluxo

  ```HTML
  <div>
    <p>Um texto aqui
  </div>
  Outro texto
      </p>
  ```

  Fluxo correto

  ```HTML
  <div>
    <p>Um texto aqui</p>
    <p>Outro texto aqui</p>
  </div>
  ```
<id id="posicionamento">

- **Posicionamento dos elementos**
  &emsp;No HTML os elementos ficam sempre uma abaixo do outro na página

  - **tag que quebra linha**

    ```HTML
    <p>Um texto aqui</p>
    <p>Conteúdo do elemento div</p>
    ```

    **Resultado:**
    <p>Um texto aqui</p>
    <p>Conteúdo do elemento div</p>

  - **tag em linha**

    ```HMTL
    <p> Texto com <strong>Negrito</strong> e <em>Itálico</em>
    ```

    **Resultado:**
    <p> Texto com <strong>Negrito</strong> e <em>Itálico</em>, sem quebra se linha.</p>

## **Conteúdo do Texto e Caracteres Reservado**

&emsp;A tag **_"\<p>"_** é usada como uma tag de parágrafo, e a tag **_\<br>_** para finalizar uma linha e inicia outra.<br>

&emsp;Com o estilo **_text-indent_** é possível definir um comprimento antes vazio antes do inicio do parágrafo.

```HTML
<p style="text-indent: t1em">Era &nbsp;uma vez, um pastosinho quê se chamava Davi,<br> era tão pequenino, mas orava a Deus.</p>
```

**Resultado:**

<p style="text-indent: 1em">Era &nbsp; uma vez, um pastosinho quê se chamava Davi,<br> era tão pequenino, mas orava a Deus.</p>

<id id="caracteres-reservado">

**Caracteres Reservado:**

&emsp;Caracteres reservado são caracteres usados no próprio HTML, como < > & " ', não podendo usar nas tags, porão da erros.<br>
&emsp;Para usarmos precisamos troca-los por outra forma de escrever.

| Entidade HTML | Caracteres |
| :-----------: | :--------: |
|    \&nbsp;    |   espaço   |
|     \&lt;     |     <      |
|     \&gt;     |     >      |
|    \&amp;     |     &      |
|    \&quot;    |     "      |
|    \&apos;    |     '      |
|    \&emsp;    |    Tab     |

## **Anatomia do Documento HTML**

**_\<!DOCTYPE html>_** Serve para identifica a alguns navegadores que estamos trabalhando com **_HTML5_**.<br>
\<html> É a tag _root_ que contem dois importantes Elementos o **\<head>** e **\<body>** cada um tem suas particularidades.<br>
\<head> Esta tag contem informações para a página.

- Título da página <br>
  O titulo aprece na aba da pagina do navegador<br>

  ```html
  <title>Anatomia do Documento\</title>
  ```

- \<meta><br>
  Define qualquer informação de metadados que não podem ser definidos por outros elementos HTML. (\<base>, \<link>, \<script>, \<style> ou \<title>).

&emsp;O atributo **"lang"** identifica a linguagem do Documento

```HTML
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="utf-8">
    <title> Anatomia do Documento</title>
  </head>
  <body>

  </body>
</html>
```

## **Semântica** 

&emsp;Um dos principais objetivos é dar uma estruturação para o texto, para que haja significado e também uma melhor leitura e para isso usamos elementos semânticos, são mais de 100, mas todos muito importantes, são apenas benefícios.

### **Títulos ou Cabeçalhos**

&emsp;Para marcação de Título, usamos as tag **_\<hx>\</hx>_** — indo de **1 à 6** é a tag para título, 1 sendo o maior e 6 sendo o menor, a hierarquia indo de título, subtítulo e etc, que são orem de importância visual.<br>
&emsp;A tag **_\<h1>_** é considerado a principal da página, de preferencia usamos a penas um por página. Caso precise de mais de um, provavelmente se cria outra pagina.<br>
&emsp;A tag **\<hr>** cria uma linha<br>

**Ex.:**

```html
<h1>Titulo h1</h1>
<h2>Titulo h2</h2>
<h3>Titulo h3</h3>
<h4>Titulo h4</h4>
<h5>Titulo h5</h5>
<h6>Titulo h6</h6>
<hr />
```

**Resultado:**

<h1>Titulo h1</h1>
<h2>Titulo h2</h2>
<h3>Titulo h3</h3>
<h4>Titulo h4</h4>
<h5>Titulo h5</h5>
<h6>Titulo h6</h6>
<hr>

<br>&emsp;Não precisa ter mais de três tipos de **_"\<h>"_** por página, apenas se tiver a necessidade de uma estrutura diferente. Pense em ciar uma outra página, caso necessário.

**EX.:**

```html
<h1>Sobre mim</h1>
<p style="text-indent: 1em">
  Lorem ipsum dolor sit amet, consectetur adipisicing elit.
</p>
<p style="text-indent: 1em">
  Voluptates tempora iusto at provident soluta distinctio fugit ratione
  consectetur deleniti vel quisquam deserunt architecto quas, possimus quos
  molestias maiores iste officia?
</p>

<h2>Nascimento</h2>
<h3>Infância</h3>
<p style="text-indent: 1em">
  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui officiis
  consequuntur corrupti nisi cumque esse dolorum fugit, rem suscipit cum
  laudantium expedita itaque odio a explicabo ex illo illum libero?
</p>
<h3>Adolescência</h3>
<p style="text-indent: 1em">
  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui officiis
  consequuntur corrupti nisi cumque esse dolorum fugit, rem suscipit cum
  laudantium expedita itaque odio a explicabo ex illo illum libero?
</p>

<h2>Trabalho</h2>
<p style="text-indent: 1em">
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus ad vel
  explicabo consequatur, ut magni doloremque sapiente, perspiciatis excepturi
  esse ea neque sed! Blanditiis mollitia assumenda ipsum harum consequuntur.
  Veritatis.
</p>
```

**Resultado:**

<h1>Sobre mim</h1>
<p style="text-indent: 1em">Lorem ipsum dolor sit amet, consectetur adipisicing elit. </p>
<p style="text-indent: 1em">Voluptates tempora iusto at provident soluta distinctio fugit ratione consectetur deleniti vel quisquam deserunt architecto quas, possimus quos molestias maiores iste officia?
</p>

<h2>Nascimento</h2>
<h3>Infância</h3>
<p style="text-indent: 1em">
    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui officiis consequuntur corrupti nisi cumque esse dolorum fugit, rem suscipit cum laudantium expedita itaque odio a explicabo ex illo illum libero?
</p>
<h3>Adolescência</h3>
<p style="text-indent: 1em">
Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui officiis consequuntur corrupti nisi cumque esse dolorum fugit, rem suscipit cum laudantium expedita itaque odio a explicabo ex illo illum libero?
</p>

<h2>Trabalho</h2>
<p style="text-indent: 1em">Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus ad vel explicabo consequatur, ut magni doloremque sapiente, perspiciatis excepturi esse ea neque sed! Blanditiis mollitia assumenda ipsum harum consequuntur. Veritatis.</p>

### **Listas**

&emsp;Existe dois tipos de listas, Ordenada e Não ordenada.<br>
&emsp;Usa a tag **_\<ol>\</ol>_** para _lista Ordenada_ e **_\<ul>\<ul>lista_** para _Não ordenada_ e a tag **_\<li>\<li>_** para os _itens_ da lista.

```html
<h3>Lita ordenada</h3>
<ol>
  <li>casa</li>
  <li>cabana</li>
  <li>apartamento</li>
</ol>
<h3>Lista não ordenada</h3>
<ul>
  <li>casa</li>
  <li>apartamento</li>
  <li>cabana</li>
</ul>
```
**Resultado:**
<h3>Lita ordenada</h3>
<ol>
  <li>casa</li>
  <li>cabana</li>
  <li>apartamento</li>
</ol>
<h3>Lista não ordenada</h3>
<ul>
  <li>casa</li>
  <li>apartamento</li>
  <li>cabana</li>
</ul>

### **Citações**
&emsp;É um recuso para informa, que o texto usado é de outra página, palavras de alguém ou de uma documentação.<br>

**Utilizamos os elementos**:
- **\<blockquote>\<blockquote>** — para uma citação que você queira deixa maior, tendo uma estilização mais diferente.
- **cite** — atributo usado para citar a url.
- **\<code>\</code>** — mostra que é um código em uma cor diferente
- **\<cite>\</cite>** — tag usada para colocar o citar link direto no texto.
  ```html
  <blockquote
    cite="https://developer.mozilla.org/en-us/docs/Web/html/Element/blockquote"
  >
    <p style="text-indent: 1em">
      O <strong>Elemento HTML <code>&lt;blockquote&gt;</code></strong> (ou
      <em>HMTL Block Quotation Elemento</em> indica um texto é uma citação
      externa.)
    </p>
    <p>
      De acordo com
      <a
        href="https://developer.mozilla.org/en-us/docs/Web/html/Element/blockquote"
        target="_blank"
      >
        <cite>página MDN blockquote</cite> </a
      >:
    </p>
  </blockquote>
  ```
  **Resultado:**
  <blockquote cite="https://developer.mozilla.org/en-us/docs/Web/html/Element/blockquote">
    <p style="text-indent: 1em">O <strong>Elemento HTML <code>&lt;blockquote&gt;</code></strong> (ou <em>HMTL Block Quotation Elemento</em> indica um texto é uma citação externa.)</p>
    <p>De acordo com <a href="https://developer.mozilla.org/en-us/docs/Web/html/Element/blockquote" target="_blank">
      <cite>página MDN blockquote</cite> </a>:
    </p>
  </blockquote>

- **\<q>\</q>** — citação curtas com aspas.
  ```html
  <p>
    O elemento quote <code>&lt;q&gt;</code> é
    <q cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">
      Usado para citações curtas que não precisam de parágrafos ou quebras de
      linha.</q
    >
    --
    <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">
      <cite>MDN q page</cite></a
    >.
  </p>
  ```
  **Resultado:**

  <p>O elemento quote <code>&lt;q&gt;</code> é <q cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">usado para citações curtas que não precisam de parágrafos ou quebras de linha.</q> -- <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">
  <cite>MDN q page</cite></a>.</p>

### **Abreviação**
&emsp;Usamos o elemento **_\<abbr title="">\</abbr>_** para abreviação de palavras, mostra uma palavra sublinhada inteira, ao colocamos o mouse em cima da abreviação, mostrando o conteúdo do **"title"**.
```html
<p stylo="text-indent: 1em">
  Usamos <abbr title="Hypertext Markup Language">HTML</abbr> para estruturar
  nossos documentos da web.
</p>
```
**Resultado:**
<p stylo="text-indent: 1em">
  Usamos <abbr title="Hypertext Markup Language">HTML</abbr> para estruturar
  nossos documentos da web.
</p>

### **Detalhe de contato**

&emsp;A tag _\<address>\</address>_ é usada para apenas colocar detalhes de **contato**, _não endereço em si_, mas por como localizar o **autor** da página.
```html
<address>
  <p>Nildson Kleyton</p>
  <strong>nildsonkleyton@hotmail.com</strong>
</address>
```
**Resultado:**
<address>
  <p>Nildson Kleyton</p>
  <strong>nildsonkleyton@hotmail.com</strong>
</address>
<br>

### **Lista de Descrição**
&emsp;Usado para marcar uma lista de itens e suas descrição.<br>
- _Definition List_ (Lista de Descrição) **\<dl>\</dl>** uma lista de pares de termos e descrições.<br>
- _Description Term_ (Termo da Descrição) **\<dt>\</dt>** identifica um termo na lista de definição.<br>
- _Description Details_ (Detalhes da Descrição) **\<dd>\</dd>** fornece detalhes ou uma definição mais completa do termo precedente.<br>
&emsp;Um uso comum para estes elementos é para implementar um glossário ou exibir metadados (uma lista de pares chave e valor).<br>
**Exemplos:**<br>
<span id="mtd">

- **Múltiplos termos e definições**
  ```html
  <h3>Glossário</h3>
  <dl>
    <dt>Hypertext</dt>
    <dd>É um hiper texto com possibilidades...</dd>

    <dt>Markup</dt>
    <dd>Marcação do texto</dd>

    <dt>Languague</dt>
    <dd>Linguagem com sua semântica e sintaxe....</dd>
  </dl>
  ```
  **Resultado:**
  <h3>Glossário</h3>
  <dl>
      <dt>Hypertext</dt>
      <dd>É um hiper texto com possibilidades...</dd>
      <dt>Markup</dt>
      <dd>Marcação do texto</dd>
      <dt>Languague</dt>
      <dd>Linguagem com sua semântica e sintaxe....</dd>
  </dl>
<span id="tdu">

- **Termo e definição única**
  ```html
  <dl>
    <dt>Firefox</dt>
    <dd>
      Um navegador gráfico gratuito, de código aberto, multiplataforma
      desenvolvido pela Mozilla Corporation e centenas de voluntários.
    </dd>
  </dl>
  ```
  **Resultado:**
  <dl>
    <dt>Firefox</dt>
    <dd>
      Um navegador gráfico gratuito, de código aberto, multiplataforma
      desenvolvido pela Mozilla Corporation e centenas de voluntários.
    </dd>
  </dl>
<span id="m-u">

- **Múltiplos termos, definição única**
  ```html
  <dl>
    <dt>Firefox</dt>
    <dt>Mozilla Firefox</dt>
    <dt>Fx</dt>
    <dd>
      Um navegador gráfico gratuito, de código aberto, multiplataforma
      desenvolvido pela Mozilla Corporation e centenas de voluntários.
    </dd>
  </dl>
  ```
  **Resultado:**
  <dl>
    <dt>Firefox</dt>
    <dt>Mozilla Firefox</dt>
    <dt>Fx</dt>
    <dd>
      Um navegador gráfico gratuito, de código aberto, multiplataforma
        desenvolvido pela Mozilla Corporation e centenas de voluntários.
    </dd>
  </dl>
<span id="u-m" >

- **Termo único, múltiplas definições** 
  ```html
  <dl>
    <dt>Firefox</dt>
    <dd>
      Um navegador gráfico gratuito, de código aberto, multiplataforma
      desenvolvido pela Mozilla Corporation e centenas de voluntários.
    </dd>
    <dd>
      O Panda Vermelho também conhecido como Panda Menor, Wah, Bear Cat ou
      Firefox, é um mamífero principalmente herbívoro, ligeiramente maior que um
      gato doméstico (60 cm de comprimento).
    </dd>
  </dl>
  ```
  **Resultado:**
  <dl>
    <dt>Firefox</dt>
    <dd>
      Um navegador gráfico gratuito, de código aberto, multiplataforma
      desenvolvido pela Mozilla Corporation e centenas de voluntários.
    </dd>
    <dd>
      O Panda Vermelho também conhecido como Panda Menor, Wah, Bear Cat ou
      Firefox, é um mamífero principalmente herbívoro, ligeiramente maior que um gato doméstico (60 cm de comprimento).
    </dd>
  </dl> 
### **Representação de Código**
&emsp;Para representar códigos ou blocos de códigos no HTML, podemos usar a tags:
- \<code> Para mostra um ou mais código.

- \<pre> Mostra blocos de código ou texto pre-formatodo,Se você precisar exibir caracteres reservados como **<  >  &  "** dentro da \<pre> tag, os caracteres devem ser escapados usando sua respectiva _entidade HTML_ .
- \<xmp> (n)
