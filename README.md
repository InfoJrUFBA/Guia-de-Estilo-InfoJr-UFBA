# info_style_guide
Guia de estilização de código da InfoJr UFBA

### Motivação
A necessidade de dispor de uma sistema que unifique a forma com que são feitos códigos das linguagens de programação e estilização dos projetos para que facilite o armazenamento e acesso dos mesmos pelos seus membros, assim como a falta de maturidade e de preparo dos trainees em interagir com a estrutura dos códigos dos projetos já finalizados, acaba por interferir de forma direta no seu aprendizado e em tudo aquilo que foi produzido pela empresa, e mediante a isso temos como intuito desse texto a criação de um documento ainda em construção, com ajuda de todos os membros da InfoJr UFBA, com uma orientação disposta de regras de formatação para as tecnologias utilizadas no desenvolvimento dos projetos da Empresa dos próximos anos.

###1 - Regras Gerais
As regras descritas nesta seção devem ser aplicadas para qualquer arquivo independente da linguagem a ser utilizada.

####1.1 - Protocolo para recursos externos
Omitir a parte de protocolo (http:, https:) de URLs
```html 
<!-- Não Recomendado -->
<script src="https://github.com/InfoJrUFBA/info_style_guide/edit/master/README.md"></script>

<!-- Recomendado -->
<script src="//github.com/InfoJrUFBA/info_style_guide/edit/master/README.md"></script>
```
####1.2 - Idioma
Todo o código deve ser escrito em inglês, com exceção do conteúdo que vai ser apresentado ao usuário final, este último deve ser escrito em português do Brasil. 

####1.2 - Identação
A indentação padrão é de quatro espaços. Não utilize tabs junto com espaços. 
```html
HTML

<ul>
  <li>Diretoria de Projetos</li>
  <li>Diretoria Administrativa Financeira</li>
</ul>
```
__________________________________________________________________________________________________________________________
```css
CSS

ul{
  color: red;
}
```
__________________________________________________________________________________________________________________________
```php
PHP

<?php
  function creatUser(){
  }
?>
```

####1.3 - Espaços
Remova os espaços existentes no final das linhas.
```html
HTML

<!-- Não Recomendado -->
<p>Infojr</p>___

<!-- Recomendado -->
<p>Infojr</p>
```

####1.3 - Codificação de Caracteres
Verifique se o seu editor usa UTF-8 como codificação de caracteres. É importante que especifique a codificação em templates HTML e documentos via <meta charset="utf-8">.

####1.3 - Comentários
Utilize os comentários para explicar o código, conforme necessário, sempre que possível. Indicando o que ele cobre, qual a finalidade, para que serve, e etc. Isso facilita a compreensão do mesmo por outras pessoas que tiverem acesso ao seu código. 

###2 - Regras de Estilos
####2.1 - HTML
#####Tipo de Documento
Use HTML5. O HTML5 é o preferido para todos os documentos HTML. Recomenda-se utilizar o HTML como text/html. Não use XHTML. XHTML, como application/xhtml+xml, pois carece de suporte ao navegador e infraestrutura, além de oferecer menos espaço para sua otimização. 
Ao definir o tipo de documento utilize a tag que expresse que a versão utilizada será o HTML5.
```
<!-- Recomendado -->
<!DOCTYPE hmtl>
<meta charset = "utf-8"
<title>Test</title>
<article>Este é apenas um teste.</article>
```

#####Use o HTML de acordo com sua finalidade
Use os elementos(“tags”) para designar a função cuja a qual você tem preferência. Por exemplo, **p** que serve para parágrafos, **a** para links, e etc. A utilização do HTML de acordo com sua finalidade é importante por razões de acessibilidade, reutilização e eficiência do código.
```html
<!-- Não Recomendado -->
<div onclick = "goToRecommendations ();">Todas as recomendações</div>

<!-- Recomendado -->
<a href="recomendations">Todas as recomendações</a>
```

#####Aspas
Use aspas duplas para os atributos html.
```html
<!-- Não Recomendado -->
<inpút type ='text' name='user[name]' id='user_name'>

<!-- Recomendado -->
<inpút type ="text" name="user[name]" id="user_name">
```

#####Valide sua página
Sempre que possível verifique se sua página HTML segue os padrões estabelecidos pelo W3C.

####2.2 - CSS
#####Nomeclatura para classes e IDS
Utilize nomes que refletem a finalidade do elemento em questão.	Nomes que são específicos apresentam o real objetivo, são compreensíveis e estão menos propensos a serem mudados. Nomes mais simples também podem ser utilizados.
```css
ID

/*Não Recomendado*/
#yee-1901{}
#navegação

/*Recomendado*/
#gallery{}
#nav{}
______________________________________________________________________________________________________________________________
CLASS

/*Não Recomendado*/
.button-verde{}
.claro{}
.atr{}

/*Recomendado*/
.button{}
.video{}
.aux{}
```

#####Evite nomeação de classes e IDs com o uso de seletores
A menos que necessário (por exemplo, com classes auxiliares), não use nomes de elementos em conjunto com IDs ou classes.
```css
ID

/*Não Recomendado*/
Ul#example{}

/*Recomendado*/
#example{}
______________________________________________________________________________________________________________________________
CLASS

/*Não Recomendado*/
.div.error{}

/*Recomendado*/
.erro{}
```

#####Faça uso da Taquigrafia (escrita rápida)
O CSS oferece uma variedade de taquigrafia, propriedade que permite a escrita do código de maneira mais resumida. É interessante a utilização da mesma sempre que possível, mesmo nos casos em que apenas um valor é definido. 
```css
/*Não Recomendado*/
-top border-style: none;
font-family: Palatino, geórgia, serif;
font-size: 100%;
line-height: 1.6;
padding-bottom: 2em;
padding-left: 1em;
padding-right: 1em;
padding-top: 0;

/*Recomendado*/
border-top: 0;
font: 100%/1.6 palatino, geórgia, serif;
padding: 0 1em 2em;
```

#####Notação Hexadecimal
Use 3 caracteres para notação hexadecimal sempre que possível. 
```css
/*Não Recomendado*/
color: #EEBBCC;

/*Recomendado*/
color: #EBC;
```
