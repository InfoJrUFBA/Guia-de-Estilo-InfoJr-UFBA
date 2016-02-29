# info_style_guide
Guia de estilização de código da InfoJr UFBA

### Motivação
A necessidade de dispor de uma sistema que unifique a forma com que são feitos códigos das linguagens de programação e estilização dos projetos para que facilite o armazenamento e acesso dos mesmos pelos seus membros, assim como a falta de maturidade e de preparo dos trainees em interagir com a estrutura dos códigos dos projetos já finalizados, acaba por interferir de forma direta no seu aprendizado e em tudo aquilo que foi produzido pela empresa, e mediante a isso temos como intuito desse texto a criação de um documento ainda em construção, com ajuda de todos os membros da InfoJr UFBA, com uma orientação disposta de regras de formatação para as tecnologias utilizadas no desenvolvimento dos projetos da Empresa dos próximos anos.

###1 - REGRAS GERAIS
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

###2 - REGRAS DE ESTILO
####2.1 - HTML
#####Tipo de Documento
Use HTML5. O HTML5 é o preferido para todos os documentos HTML. Recomenda-se utilizar o HTML como text/html. Não use XHTML. XHTML, como application/xhtml+xml, pois carece de suporte ao navegador e infraestrutura, além de oferecer menos espaço para sua otimização. 
Ao definir o tipo de documento utilize a tag que expresse que a versão utilizada será o HTML5.
```
<!-- Recomendado -->
<!DOCTYPE hmtl>
<meta charset = "utf-8">
<title>Test</title>
<h1>Este é apenas um teste.</h1>
```

#####Use o HTML de acordo com sua finalidade
Use os elementos(“tags”) para designar a função cuja a qual você tem preferência. Por exemplo, **p** que serve para parágrafos, **a** para links, e etc. A utilização do HTML de acordo com sua finalidade é importante por razões de acessibilidade, reutilização e eficiência do código.
```html
<!-- Não Recomendado -->
<p><button>Algo</button></p>

<!-- Recomendado -->
<div class="btn-group">
  <button>Algo</button>
</div>
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
__________________________________________________________________________________________________________
CLASS

/*Não Recomendado*/
.claro{}
.atr{}

/*Recomendado*/
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
___________________________________________________________________________________________________________
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

#####Utilização de ponto e vírgula
Finalize todas as declarações de propriedades utilizando um *;*
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

#####Delimitadores de Classe e Ids
Busque ao máximo escrever classes e ids com nomes simples, mas no caso de palavras compostas utilize hifens (-) para classes e subtraços (_) para ids.
```css
ID

#new_user{
  /*..*/
}
__________________________________________________________________________________________________________
CLASS

.btn-primary{
   /*..*/
}
```

#####Separação entre propriedades e valores
Sempre utilize um espaço simples parar separar uma propriedade dos seus valores
```css
/*Não Recomendado*/
p{
  color:blue;
}
/*Recomendado*/
p{  
  color: blue;
}
```

###3 - EDITORES DE TEXTO
A seguir alguns editores de textos que podem ser utilizados no desenvolvimento dos projetos.
####3.1 - Brackets
Um editor de textos Open Source que vem crescendo a uma grande velocidade, alcançando alguns editores de texto já consolidados no mercado.
#####3.1.1 - Atalhos do teclado
O Brackets, assim como outros editores e softwares, tem seus atalhos para agilizar o dia-a-dia de quem trabalha com tais ferramentas. Abaixo alguns atalhos interessantes:

**Crtrl+Shift+A**: Abre um input para você digitar uma tag e teclar “Enter”. Fazendo isso, ele irá inserir a tag completa com seu fechamento e seus atributos no html. Ex.: Digite link e tecle “Enter”, ele vai retornar <link rel=”stylesheet” href=””>. E quando você dá “Enter” o “ponteiro” do mouse vai para dentro das aspas do atributo href. Daí, basta você começar a digitar o endereço que ele vai mostrando as opções em forma de codehint. 

**Crtrl+Shift+D**: Esse atalho de grande utilidade também está presente no Brackets. Serve para duplicar uma linha.

**Crtrl+D**: Atalho utilizado para deletar uma linha.

**Crtrl+E**: Uma das grandes novidades do Brackets. Com esse atalho você pode editar o CSS sem ter que abrir o arquivo .css. Basta ir em um arquivo .html ou .php clicar sobre o elemento que deseja alterar as propriedades e pressionar Ctrl+E para abrir a tela de edição.

#####3.1.2 - Extensões
Apesar de ser um editor com pouco tempo no mercado já conta com uma grande quantidade de plug-ins para dar aquela incrementada no workflow. Segue alguns deles que podem ser utilizados: 

**Brackets Git**: Bastante completo, disponibiliza uma interface para você usar o controle de versões mais utilizado por todos. Para aqueles que não gostam de usar o git através de interfaces, ele te dá, de fácil acesso, um botão que leva diretamente para o terminal, aberto já na pasta do projeto, sem ter que navegar até o projeto pelo terminal.

**Emmet**: Disponibiliza abreviações para agilizar o desenvolvimento de HTML e CSS.

**Code Folding**: Esse plug-in agiliza a organização do seu código. Ele disponibiliza a função de comprimir um determinado bloco de código em uma linha (e, claro, posteriormente você pode expandir novamente), deixando assim o código mais curto para se navegar entre o arquivo com mais legibilidade.

**Indent Guide**: Muito bom para facilitar a leitura do código e evitar que você deixe tags HTML abertas sem querer. Ele cria uma linha guia ligando a tag de abertura e a tag de fechamento de determinado elemento, assim você pode verificar se está tudo identado e fechado corretamente.

####3.2 - Sublime
Um editor de texto simples, limpo, leve e muito customizável.
#####3.2.1 - Atalhos do teclado
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
 
#####3.2.2 - Extensões
Assim como no Brackets o sublime apresenta alguns plug-ins que facilita a vida dos desenvolvedores. Alguns recomendados que você pode utilizar: 

**Package Control**: Antes de instalar qualquer pacote de plug-in, é importante que você já tenha instalado em seu Sublime o Package Control de acordo com a versão do Sublime utilizada. 
O Package Control é um plug-in que gerencia todos os outros plug-ins do Sublime.

**Emmet**: Este plug-in é simplesmente um conjunto de ferramentas de desenvolvimento web que ajudam a codificação de *HTML* e *CSS*. Ele permite que você crie, com mais velocidade, seus elementos através de expressões específicas, seguidas da tecla *TAB*.

**Jqery**: Esse plug-in pode facilitar bastante no momento de criação de bibliotecas em seus projetos. Ele é um pacote que fornece alguns trechos para a maioria do JQuery, muito usados no dia a dia.

**Colorhighliter**: Esse é um plug-in serve para inspecionar discretamente os valores de cores hexadecimais selecionados em diferentes estilos e ícones. Além disso, o plug-in adiciona o seletor de cores em um conversor de formato de cor. Seria um tipo de “inspecionar elemento” para cores em tempo real.

**Aligntab**: Esse plug-in serve para a organização de códigos. Ele vai te auxiliar a permanecer com uma Indentação 100% padronizada. É um plug-in de alinhamento usando expressão regular. Confira abaixo suas características:

- Alinha usando expressão regular
- Espaçamento personalizado, preenchimento e justificado
- Detecção inteligente para alinhamentos se linhas são selecionadas
- Suporte a múltiplos cursores
- Modo de mesa e modo de visualização ao vivo

**Colorshemeselector**: Esse plug-in permite que você crie uma customização no seu Sublime Text. Resumidamente ele serve para selecionar esquema de cores através do Painel. Infelizmente isso só são adotados cores padrões escolhidas pela ferramenta.

**CSS3**: Esse plug-in serve para manter uma boa organização no CSS. Existem casos onde queremos acabar ir logo embora para casa e acabamos esquecendo um simples “;“. O CSS3 Syntax ou apenas CSS3 é bem abrangente, pois se baseia nos mais recentes projetos e especificações atuais. Uso: Navegue até View > Syntax > CSS3. 

**Javascriptnext**: Este é um pacote de sintaxe melhorada para Java Script. Baseia-se nos arquivos de linguagem comumente usados ​​e também inclui novos recursos de ECMAScript 6 como módulos, métodos, arrows functions, classes, geradores e assessores (ES5). Se você quiser usá-lo para cada arquivo js, você ​​cria ou abra um arquivo Java Script, e daí clica no nome de sintaxe no canto inferior direito do Sublime, em seguida, clique em “Abrir todos com extensão atual e depois selecione JavascriptNext – ES6 > JavascriptNext.
 


 






