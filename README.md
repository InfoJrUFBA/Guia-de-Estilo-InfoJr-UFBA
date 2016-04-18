#Guia de estilização de código da InfoJr UFBA

### Motivação
O guia abaixo é um documento em construção que tem como finalidade padronizar o desenvolvimento de códigos nas linguagens de programação e estilização dos projetos, e que facilite o acesso e compreensão dos mesmos pelos seus membros.


1. [REGRAS GERAIS](#1---regras-gerais)

 1.1 [Protocolo para Recursos Externos](#11---protocolo-para-recursos-externos)

 1.2 [Idioma](#12---idioma)

 1.3 [Última Linha](#13---Última-linha)

 1.4 [Identação](#14---identação)
 
 1.5 [Espaços](#15---espaços)
 
 1.6 [Codificação de Caracteres](#16---codificação-de-caracteres)
 
 1.7 [Comentários](#17---comentários)

2. [REGRAS DE ESTILO](#2---regras-de-estilo)

 2.1 [HTML](#21---html)

 2.2 [CSS](#22---css)

 2.3 [JAVA SCRIPT](#23---javascript)

 2.4 [PHP](#24---php)
 
3. [EDITORES DE TEXTO](#3---editores-de-texto)

 3.1 [BRACKETS](#31---brackets)

 3.2 [SUBLIME](#32---sublime)


### 1 - REGRAS GERAIS
As regras descritas nesta seção devem ser aplicadas para qualquer arquivo independente da linguagem a ser utilizada.

#### 1.1 - Protocolo para Recursos Externos
Omitir a parte de protocolo ```(http:, https:)``` de URLs

```html 
<!-- Não Recomendado -->
<script src="https://github.com/InfoJrUFBA/info_style_guide/edit/master/README.md"></script>

<!-- Recomendado -->
<script src="//github.com/InfoJrUFBA/info_style_guide/edit/master/README.md"></script>
```

#### 1.2 - Idioma
Todo o código deve ser escrito em Inglês, com exceção do conteúdo que vai ser apresentado ao usuário final, este último deve ser escrito em português do Brasil.

#### 1.3 - Última linha
Todo o código deve ser escrito em Inglês, com exceção do conteúdo que vai ser apresentado ao usuário final, este último deve ser escrito em português do Brasil.

```php
function createBadge() {
    // ...
}
```

#### 1.4 - Identação
A indentação padrão é de quatro espaços. Não utilize tabs junto com espaços. 

```html
HTML

<ul>
    <li>Diretoria de Projetos</li>
    <li>Diretoria Administrativa Financeira</li>
</ul>
```
_____________________________________________________________________________________________________

```css
CSS

ul{
    color: red;
}
```
_____________________________________________________________________________________________________

```php
PHP

<?php
    function creatUser() {
    }
?>
```

#### 1.5 - Espaços
Remova os espaços existentes no final das linhas.

```html
HTML

<!-- Não Recomendado -->
<p>Infojr</p>___

<!-- Recomendado -->
<p>Infojr</p>
```

#### 1.6 - Codificação de Caracteres
Verifique se o seu editor usa UTF-8 como codificação de caracteres. É importante que especifique a codificação em templates HTML e documentos via ```<meta charset="utf-8">```.

#### 1.7 - Comentários
Utilize os comentários para explicar o código, conforme necessário, sempre que possível. Indicando o que ele cobre, qual a finalidade, para que serve, e etc. Isso facilita a compreensão do mesmo por outras pessoas que tiverem acesso ao seu código. Para fazer um comentário, envolva o exemple desejado entre ```<!-- -->```.

```
<!--Este é um comentário. Comentários não são exibidos no navegador.-->
```

### 2 - REGRAS DE ESTILO
#### 2.1 - Html
As regras de estilo estabelicidas para HTML baseados no [guia de estilo para HTML](https://google.github.io/styleguide/htmlcssguide.xml#HTML_Style_Rules) da Google.
##### Tipo de Documento
Use HTML5. O HTML5 é o preferido para todos os documentos HTML. Recomenda-se utilizar o HTML como text/html. Não use XHTML. XHTML, como application/xhtml+xml, pois carece de suporte ao navegador e infraestrutura, além de oferecer menos espaço para sua otimização. 
Ao definir o tipo de documento utilize a tag que expresse que a versão utilizada será o HTML5.

```html
<!-- Recomendado -->
<!DOCTYPE hmtl>
```

##### Escrita
Utilize sempre letras minúsculas para representar tags e atributos.

```html
<!-- Não recomendado -->
<A HREF="/">Home</A>
<!-- Recomendado -->
<a href="/">Home</a>
```

##### Use o HTML de acordo com sua finalidade
Use os elementos(“tags”) para designar a função que você tem preferência. Por exemplo, **p**, que serve para parágrafos, **a**, para links, e etc. A utilização do HTML de acordo com sua finalidade é importante por razões de acessibilidade, reutilização e eficiência do código.

```html
<!-- Não Recomendado -->
<p><button>Algo</button></p>

<!-- Recomendado -->
<div class="btn-group">
    <button>Algo</button>
</div>
```

##### Aspas
Use aspas duplas para os atributos html.

```html
<!-- Não Recomendado -->
<input type='text' name='user[name]' id='user_name'>

<!-- Recomendado -->
<input type="text" name="user[name]" id="user_name">
```

##### Valide sua página
Sempre que possível verifique se sua página HTML segue os padrões estabelecidos pelo [W3C](http://www.w3schools.com/).

####2.2 - CSS
As regra de estilo estabelicidas para CSS baseados no [guia de estilo para CSS](https://google.github.io/styleguide/htmlcssguide.xml#CSS_Style_Rules) da Google.
##### Escrita
Utilize sempre letras minúsculas para representar tags, propriedades e valores quando possível.

```css
/* Não recomendado */
H1 {
    FONT-SIZE: 20PX;
}
/* Recomendado */
h1 {
    font-size: 20px;
}
```

##### Aspas
Use aspas simples quando necessário.
/* Não recomendado */
p {
    font-family: "Comic Sans MS", sans-serif;
}
/* Recomendado */
p {
    font-family: 'Comic Sans MS', sans-serif;
}
##### Ordem de Declaração
As propriedades devem ser declaradas em ordem alfabética. Contudo, as propriedades de terceiros ```(-moz-, -webkit-)``` devem ser ordenadas juntos às propriedades que estas alteram.

```css
input {
    background: fuchsia;
    border-radius: 4px;
    border: 1px solid;
    -moz-border-radius: 4px;
    -webkit-border-radius: 4px;
    color: black;
    text-align: center;
    text-indent: 2em;
}
```

**Dica:** Com o Sulime Text você pode selecionar as propiedades e pressionar F5 para ordená-las em ordem alfabética.
##### Nomeclatura para classes e IDs
Utilize nomes que refletem a finalidade do elemento em questão.	Nomes que são específicos representam o real objetivo, são compreensíveis e estão menos propensos a serem mudados. Nomes mais simples também podem ser utilizados.

```css
ID

/*Não Recomendado*/
#yee-1901 {}
#navegação {}

/*Recomendado*/
#gallery{}
#navigation{}
__________________________________________________________________________________________________________
CLASS

/*Não Recomendado*/
.claro {}
.atr {}

/*Recomendado*/
.video {}
.auxiliar {}
```

##### Evite nomeação de classes e IDs com o uso de seletores
A menos que necessário (por exemplo, com classes auxiliares), não use nomes de elementos em conjunto com IDs ou classes.

```css
ID

/*Não Recomendado*/
Ul#example {}

/*Recomendado*/
#example {}
___________________________________________________________________________________________________________
CLASS

/*Não Recomendado*/
.div.error {}

/*Recomendado*/
.error {}
```

##### Faça uso da Taquigrafia (escrita rápida)
O CSS oferece uma variedade de taquigrafia, propriedade que permite a escrita do código de maneira mais resumida. É interessante a utilização da mesma sempre que possível, mesmo nos casos em que apenas um valor é definido. 

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
    font: 100%/1.6 Palatino, Georgia, serif;
    padding: 0 1em 2em;
```

##### Notação Hexadecimal
Use 3 caracteres para notação hexadecimal sempre que possível.

```css
/*Não Recomendado*/
    color: #EEBBCC;

/*Recomendado*/
    color: #EBC;
```

##### Utilização de ponto e vírgula
Finalize todas as declarações de propriedades utilizando um ```;```.

```css
/*Não Recomendado*/
div{
    color: blue
    font-family: 'Times New Roman', serif
}

/*Recomendado*/
div{
    color: blue;
    font-family: 'Times New Roman', serif;
}
```

##### Delimitadores de classes e IDs
Busque ao máximo escrever classes e IDs com nomes simples, mas no caso de palavras compostas utilize hifens ```-``` para classes e subtraços ```_``` para IDs.

```css
ID

#new_user {
    /*..*/
}
__________________________________________________________________________________________________________
CLASS

.btn-primary {
    /*..*/
}
```

##### Separação entre propriedades e valores
Sempre utilize um espaço simples parar separar uma propriedade dos seus valores

```css
/*Não Recomendado*/
p {
    color:blue;
}
/*Recomendado*/
p {  
    color: blue;
}
```

##### Valide o seu estilo
Sempre que possível verifique se o seu arquivo CSS segue os padrões propostos pela [W3C](http://www.w3schools.com/).

#### 2.3 - JavaScript
O guia de estilo para JavaScript é baseado no [documento](http://javascript.crockford.com/code.html) escrito por Douglas Crockford. Se alguma regra não estiver escrita aqui tome o documento original como base.
##### Arquivos JavaScript
Use tags ```<script>``` o mais tarde possível (geralmente antes de fechar a tag body). Isso reduz o atraso para carregar uma página. Não é necessário adicionar os atributos tipo ou language.
#####Largura da linha
Evite escrever linhas com mais de 120 caracteres. Em alguns casos será necessário quebrar comandos. Nesse caso quebre a linha depois de um operador.

##### Comentários
Use comentários se somente necessário. Não comente coisas óbvias como:

```
 var i = 0; // Atribui à variável i o valor zero.
```

Você deve comentar funções utilizando o padrão DocBlock:

```
/**
* Descrição do método...
*
* @method myFunction
* @param {String} myVariable
* @return {Array}
*/
function myFunction(myVariable) {
    return [myVariable];
}
```

##### Declaração de váriaveis
Sempre declare variáveis antes de usá-las.

```
 var name;
 var email;
```

##### Declaração de funções
Todas as funções devem ser declaradas antes de serem usadas. Não deve haver espaços entre o nome da função e o parêntese de abertura ```()```, mas deve haver um espaço no fechar de parênteses e abertura de chaves ```{```.

```javascript
function validate(attribute, options) {
    return true;
}
```

##### Nomes
Ao definir variáveis e funções opte por utilizar valores que tenham signicado e que expressem o que será armazenado ou calculado na mesma.

##### Comandos
Todos os comandos devem ser terminados por ponto e vírgula ```;```.

#### 2.4 - PHP
Este guia utiliza as [recomendações](http://framework.zend.com/manual/1.10/en/coding-standard.html) definidas pela Zend Technologies para descrever o estilo a ser utilizado ao se escrever PHP.
##### Regras Gerais
Para arquivos que possuem apenas código PHP é proibido o uso de tags de encerramento (?>). Isso evita a injeção de espaços desnecessários.

Obs.: Nos exemplos de código escritos aqui a tag de fechamento do PHP está sendo utilizada porque este arquivo não é apenas PHP.

##### Largura da linha
Assim como JavaScript, o número máximo de caracteres por linha é de 120.

##### Nomes de arquivos
Todos os arquivos que possuem código PHP devem possuir a extensão .php no final, com a exceção apenas dos scripts de visão que devem terminar com a extensão .phtml.

##### Nomes de classes
Classes devem possuir o namespace com o nome da pasta onde estão hospedados imediatamente após a pasta App. Por exemplo, para a classe User, hospedada em App/Models/User.php o arquivo PHP deve conter:

```PHP
<?php
    namespace Models;
    class User {}
?>
```

##### Funções e Métodos
Nomes de funções sempre começam com letra minúscula e seguem o "camelCase".

```PHP
<?php
    function validateName() {}
    function validateEmail() {}
    function createUser() {}
?>
```

##### Variáveis
Devem possuir apenas caracteres alfanuméricos. Underscores (_) não são permitidos.

### 3 - EDITORES DE TEXTO
A seguir alguns editores de textos que podem ser utilizados no desenvolvimento dos projetos.
#### 3.1 - Brackets
Um editor de textos Open Source que vem crescendo a uma grande velocidade, alcançando alguns editores de texto já consolidados no mercado.
##### 3.1.1 - Atalhos do teclado
O Brackets, assim como outros editores e softwares, tem seus atalhos para agilizar o dia-a-dia de quem trabalha com tais ferramentas. Abaixo alguns atalhos interessantes:

**Crtrl+Shift+A**: Abre um input para você digitar uma tag e teclar “Enter”. Fazendo isso, ele irá inserir a tag completa com seu fechamento e seus atributos no html. Ex.: Digite link e tecle “Enter”, ele vai retornar ```<link rel=”stylesheet” href=””>```. E quando você dá “Enter” o “ponteiro” do mouse vai para dentro das aspas do atributo href. Daí, basta você começar a digitar o endereço que ele vai mostrando as opções em forma de codehint. 

**Crtrl+Shift+D**: Esse atalho de grande utilidade também está presente no Brackets. Serve para duplicar uma linha.

**Crtrl+D**: Atalho utilizado para deletar uma linha.

**Crtrl+E**: Uma das grandes novidades do Brackets. Com esse atalho você pode editar o CSS sem ter que abrir o arquivo .css. Basta ir em um arquivo .html ou .php clicar sobre o elemento que deseja alterar as propriedades e pressionar Ctrl+E para abrir a tela de edição.

##### 3.1.2 - Extensões
Apesar de ser um editor com pouco tempo no mercado já conta com uma grande quantidade de plug-ins para dar aquela incrementada no workflow. Segue alguns deles que podem ser utilizados: 

**Brackets Git**: Bastante completo, disponibiliza uma interface para você usar o controle de versões mais utilizado por todos. Para aqueles que não gostam de usar o git através de interfaces, ele te dá, de fácil acesso, um botão que leva diretamente para o terminal, aberto já na pasta do projeto, sem ter que navegar até o projeto pelo terminal.

**Emmet**: Disponibiliza abreviações para agilizar o desenvolvimento de HTML e CSS.

**Code Folding**: Esse plug-in agiliza a organização do seu código. Ele disponibiliza a função de comprimir um determinado bloco de código em uma linha (e, claro, posteriormente você pode expandir novamente), deixando assim o código mais curto para se navegar entre o arquivo com mais legibilidade.

**Indent Guide**: Muito bom para facilitar a leitura do código e evitar que você deixe tags HTML abertas sem querer. Ele cria uma linha guia ligando a tag de abertura e a tag de fechamento de determinado elemento, assim você pode verificar se está tudo identado e fechado corretamente.

#### 3.2 - Sublime
Um editor de texto simples, limpo, leve e muito customizável.
##### 3.2.1 - Configurações do Sublime parar aplicação das [Regras Gerais](#1---regras-gerais)
O Sublime Text permite que você altere as configurações padrões para realizar certas tarefas. Para alterar as configurações clique em Preferences → Settings – User.

As configurações necessárias para realizar as regras gerais expostas na seção anterior de forma automática estão descritas a seguir:

```
{
    "ensure_newline_at_eof_on_save": true,
    "tab_size": 4,
    "translate_tabs_to_spaces": true,
    "trim_trailing_white_space_on_save": true
}
```

##### 3.2.1 - Atalhos do teclado
O Sublime tem muitos comandos escondidos que podem não estar listados nos menus. Você pode acioná-los pelo teclado acionando os comandos pelo controle de acesso *CMD+SHIFT+P*. A seguir alguns deles:

**Configurando um atalho de comando**: O usuário pode instalar um comando subl no seu terminal para facilitar a abertura de projetos no Sublime via terminal. Você pode conferir o passo a passo da configuração através do seguinte link: Configurandosublime. 

**Mútiplas Seleções**: Você pode selecionar vários lugares ao mesmo tempo do seu código de maneira fácil, para isso segure o *CMD ou CTRL* e use o mouse para selecionar diversas partes do seu código.

**Selecionar Pedaços iguais do código**: Secione a tag desejada para edição e em seguida aperte *CMD+D ou CTRL+D* para selecionar outros blocos de código iguais a este que você selecionou inicialmente.

**Procurar Arquivos**: Você pode encontrar arquivos no seu projeto sem ter que ficar perdendo tempo nas pastas, use o atalho *CMD+T* e em seguida digite o nome dos seus arquivos e edite-os.

**Goto Anythig**: Você pode encontrar funções, classes ou IDs dentro dos seus arquivos, use o atalho *CMD+P*. Esse comando abre o search geral do Sublime. Nesse search você pode procurar arquivos, como no exemplo anterior ou se você iniciar a busca com um *@*, vai possibilitar a procura de funções, classes, IDs e etc. no arquivo aberto.
Se você quiser ir para uma linha específica, você pode começar a busca com : (dois pontos) e aí você coloca o número da linha ou use o atalho *CTRL+G* e número da linha.

**Escondendo a sidebar**: Ideal para quem trabalha com notebook com tela pequena. Basta apertar *CMD+K* ou *CTRL+K* e seguidamente B e isso faz com que o sidebar apareça ou desapareça.

**Apagar linha inteira**: Para apagar todo o conteúdo de uma linha, utilize *CMD+K+K ou CTRL+K+K*. Para excluir a linha completamente, utiliza *CMD+X ou CTRL+X*.

**Clonar Linha**: Para copiar uma linha inteira e duplica-la utilize *CMD+SHIFT+D ou CTRL+SHIFT+D*.

**Seleção em Bloco**: Segure *SHIFT* e aperte a seta do teclado para baixo. Você verá o cursor selecionando as linhas. Depois segure o *CMD+SHIFT* ou *CTRL+SHIFT* e aperte a tecla para direita.

**Aalhos de Seleção**: A tecla SUPER é *CMD* no *MAC* e a mesma é a tecla *CTRL* no Windows e no Linux.

**Outros Comandos que você pode utilizar**:

 - Selecionar conteúdo entre tags: *CTRL+SHIFT+A*
 - Expandir seleção para linha: *CTRL+L*
 - Expandir seleção para ocorrência idêntica: *CTRL +D*
 - Expandir seleção para escopo: *CTRL +SHIFT+SPACE*
 - Mover a linha para cima: *CTRL +SHIFT+UP*
 - Mover a linha para baixo: *CTRL +SHIFT+DOWN*
 - Duplicar linha: *CTRL +SHIFT+D*
 - Juntar linhas: *CTRL +J*
 
##### 3.2.2 - Extensões
Assim como no Brackets o sublime apresenta alguns plug-ins que facilita a vida dos desenvolvedores. Alguns recomendados que você pode utilizar: 

**Package Control**: Antes de instalar qualquer pacote de plug-in, é importante que você já tenha instalado em seu Sublime o Package Control de acordo com a versão do Sublime utilizada. 
O Package Control é um plug-in que gerencia todos os outros plug-ins do Sublime.

**Emmet**: Este plug-in é simplesmente um conjunto de ferramentas de desenvolvimento web que ajudam a codificação de *HTML* e *CSS*. Ele permite que você crie, com mais velocidade, seus elementos através de expressões específicas, seguidas da tecla *TAB*.

**Jqery**: Esse plug-in pode facilitar bastante no momento de criação de bibliotecas em seus projetos. Ele é um pacote que fornece alguns trechos para a maioria do JQuery, muito usados no dia a dia.

**Colorhighliter**: Esse é um plug-in serve para inspecionar discretamente os valores de cores hexadecimais selecionados em diferentes estilos e ícones. Além disso, o plug-in adiciona o seletor de cores em um conversor de formato de cor. Seria um tipo de “inspecionar elemento” para cores em tempo real.

**Aligntab**: Esse plug-in serve para a organização de códigos. Ele vai te auxiliar a permanecer com uma Indentação 100% padronizada. É um plug-in de alinhamento usando expressão regular. Confira abaixo suas características:

```
- Alinha usando expressão regular
- Espaçamento personalizado, preenchimento e justificado
- Detecção inteligente para alinhamentos se linhas são selecionadas
- Suporte a múltiplos cursores
- Modo de mesa e modo de visualização ao vivo
```

**Colorshemeselector**: Esse plug-in permite que você crie uma customização no seu Sublime Text. Resumidamente ele serve para selecionar esquema de cores através do Painel. Infelizmente isso só são adotados cores padrões escolhidas pela ferramenta.

**CSS3**: Esse plug-in serve para manter uma boa organização no CSS. Existem casos onde queremos acabar ir logo embora para casa e acabamos esquecendo um simples ```;```. O CSS3 Syntax ou apenas CSS3 é bem abrangente, pois se baseia nos mais recentes projetos e especificações atuais. Uso: Navegue até View > Syntax > CSS3. 

**Javascriptnext**: Este é um pacote de sintaxe melhorada para Java Script. Baseia-se nos arquivos de linguagem comumente usados ​​e também inclui novos recursos de ECMAScript 6 como módulos, métodos, arrows functions, classes, geradores e assessores (ES5). Se você quiser usá-lo para cada arquivo js, você ​​cria ou abra um arquivo Java Script, e daí clica no nome de sintaxe no canto inferior direito do Sublime, em seguida, clique em “Abrir todos com extensão atual e depois selecione JavascriptNext – ES6 > JavascriptNext.
