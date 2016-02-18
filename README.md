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
