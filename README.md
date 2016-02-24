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
<!-- Não Recomendado -->
<title>Test </ title>

<!-- Recomendado -->

```

