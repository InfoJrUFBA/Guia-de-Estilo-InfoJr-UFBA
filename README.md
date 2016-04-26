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
 
 2.4.1 [Orientação a Objetos](#241-orientação-a-objetos)
   
    - [Classes e Objetos](#classes-e-objetos)
   
    - [Atriibutos e Métodos](#atributos-e-métodos)
   
    - [Herança](#herança)
   
    - [Classes Abstratas](classes-abstratas)
   
    - [Métodos Abstratos](métodos-abstratos)
   
    - [Classes Finais](#classes-finais)
   
    - [Métodos Finais](#métodos-finais)
   
    - [Traits](#traits)
   
   
 2.4.2 [PHP Data Objects(PDO)](#242-php-data-objectspdo)
 
    - [Executando comandos](#executando-comandos)
    
    - [Fazendo consultas](#fazendo-consultas)
    
    - [Transações](#transações)
    
    - [Prepared Statements](#prepared-statements)
 
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
#### 2.1 - HTML
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
Este guia utiliza as [recomendações](http://framework.zend.com/manual/1.10/en/coding-standard.html) definidas pela Zend Technologies para descrever o estilo a ser utilizado ao se escrever PHP. E [orientações](http://www.devmedia.com.br/) defindas pelo DevMedia para induzir conhecimentos sobre Orientação a Objetos e PDO no PHP.
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

##### 2.4.1 Orientação a Objetos
A orientação a objetos (OO) é um padrão de programação em que um software não é composto por um grande bloco de códigos específicos, e sim de vários blocos de códigos distantes e independentes, que juntos montam um sistema. O PHP faz parte de um grupo de linguagens que possuem suporte a OO, mas não é preso a ela. Esse padrão não possui um objetivo único e tem como objetivo:

- Reutilização de código (tempo economizado);
- Escalabilidade (código adicionado mais facilmente);
- Manutenbilidade (manutenção mais fácil);
- Desenvolvimento mais rápido.

A POO possui alguns conceitos fundamentais para seu desenvolvimento:

- Abstração: são tipos abstratos de dados;
- Objetos: um objeto é uma entidade do mundo real, concreta ou abstrata, que seja aplicável ao sistema;
- Classes: uma classe é a representação de vários objetos que possuem as mesmas características e comportamentos;
- Atributos / Propriedades: são as características de um determinado objeto.

##### Classes e Objetos
Algo que confunde bastante novos estudantes de Orientação a Objetos é a diferença entre Classes e Objetos. 
As classes definem as características e o comportamento dos seus objetos. Cada característica é representada por um atributo e cada comportamento é definido por um método, logo uma classe não é um objeto e sim uma abstração de sua estrutura, no qual podemos definir quantos objetos desejamos ter.
Para podermos entender melhor o funcionamento, vamos criar a nossa primeira classe e alguns objetos a partir dela, conforme o exemplo a seguir:
```PHP
 <?php
 Class Conta {
 }
     $conta  = new Conta();
     $conta2 = new Conta();
     $conta3 = new Conta();
 ?>
```
Criamos uma classe vazia de uma conta junto com três objetos que são dessa conta criada. Podemos dizer então que os três objetos são do tipo conta. E é dessa maneira que funciona todo objeto, seu tipo será sempre a classe a partir do qual ele é criado.

##### Atributos e Métodos
Uma classe é composta por atributos e métodos, que juntos dão funcionalidade a um objeto. Podemos ver no próximo exemplo, uma classe composta por dois atributos e três métodos.
```PHP
<?php 
  Class Conta { 
    public $saldo = 500; 
    public $titular; 
    
    function sacar($valor) { 
    } 
    
    function depositar($valor) { 
    } 
    
    function verSaldo() { 
    } 
  } 
    $conta1 = new Conta(); 
    $conta1 ->depositar(500); 
    $conta1->sacar(20); 
  
    $conta2 = new Conta(); 
    $conta2->depositar(250); 
    $conta2->verSaldo(); ?>
?>
```
A classe Conta tem como atributos o saldo da conta e o titular. E como métodos possui depositar(), sacar() e verSaldo(). Para acessarmos o método depositar() do nosso objeto $conta1 precisamos utilizar uma seta(->). Seu nome é Operador de Acesso a Objetos e é através dessa seta que indicamos que estamos acessando um atributo ou método de tal objeto. Faremos agora uma codificação mais completa em cima de nossa classe Conta, como podemos observar no exemplo a segur:
```PHP
<?php 
  Class Conta{ 
    public $saldo = 0; 
    public $titular; 
    
    function depositar($valor) { 
        $this->depositar += $valor; 
    } 
    
    function sacar($valor) { 
        if(($this->saldo > 0) && ($this->saldo >= $valor)) { 
            $this->saldo -= $valor; 
        }else { 
            echo "Saldo insuficiente"; 
         } 
      } 
      
    function verSaldo() { 
        echo "Saldo Atual:".$this->saldo. "<br>"; 
    } 
  } 
  
  $novaConta = new Conta(); 
  $novaConta->verSaldo(); 
  $novaConta->depositar(500); 
  $novaConta->verSaldo(); 
  $novaConta->sacar(150);
  $novaConta->verSaldo(); ?>
?>
```
Note que para acessarmos nossos atributos dentro dos métodos utilizamos a variável reservada $this. Se fosse preciso chamar algum método da própria classe dentro de um outro método teríamos de usar $this, que é usado para acessar atributos e métodos da própria classe e só existe dentro deste escopo. No PHP ele é fundamental e obrigatório, já em algumas outras linguagens de programação $this é opcional.

##### Herança
Um dos conceitos fundamentais da OO é a herança de classes, pois permite que uma classe estenda outra e a classe filha vai herdar todos os atributos e métodos da classe pai. Ela pode então tanto possuir novos métodos e atributos, quanto reescrever métodos já existentes, como mostra o próximo exemplo:
```PHP
<?php 
    class Conta{ 
        public $saldo = 0; 
        function depositar($valor) { 
        } 
        
        function sacar() {
        } 
        
        class ContaCorrente extends Conta { 
            function transferir($contaDestino, $valor) {
                $this->saldo -= $valor; 
            } 
        }
    } 
 
     $novaConta = new ContaCorrente(); 
     $novaConta->transferir('xxx-xxx', 500); 
     echo "Saldo:".$novaConta->saldo; 
 ?>
```

##### Classes abstratas
Uma classe abstrata é uma classe que não pode ser instanciada como um objeto diretamente. Ela tem que ser estendida por alguma classe concreta, e quando um objeto desta classe for criado, ele herdará métodos e atributos da classe abstrata. Veja o próximo exemplo:
```PHP
<?php abstract 
 class Conta{ 
     public $saldo =0; 
     public function sacar() { 
     } 
     
     public function depositar($valor) { 
     }
     
     class ContaPoupanca extends Conta{ 
         public function resgatar($valor) {
         } 
     } 
     
     $conta1 = new ContaPoupanca(); 
     $conta1->depositar(500); 
     $conta1->resgatar(250); ?>
?>
Note que a classe estendida faz uso dos métodos declarados na classe abstrata, ou seja, em classes abstratas e concretas o conceito de herança é o mesmo. Mas, para que serve uma classe abstrata? Vamos pensar no funcionamento de um banco, onde os clientes podem ter uma conta corrente e poupança: o funcionamento de uma conta segue um determinado padrão, o que difere uma da outra são as ações (métodos) que podemos executar.
```
##### Métodos Abstratos
odemos ter também métodos abstratos em nossas classes, como mostra o próximo exemplo:
```PHP
 <?php 
  abstract class Conta { 
      public $saldo = 0; 
      public function sacar() { 
      } 
      
      public function depositar($valor) { 
      } 
  } 
  class ContaPoupanca extends Conta { 
      public function resgatar($valor) { 
      } 
  } 
  $conta1 = new ContaPoupanca(); 
  $conta1->depositar(500); 
  $conta1->resgatar(250); ?>
?>
```
Todo método abstrato precisa, obrigatoriamente, ser implementado na classe filha, ou seja, todas as contas, independentemente do tipo devem possuir as operações básicas de saque, depósito, transferência e consulta. Porém, contas de tipos diferentes podem tratar estas ações de formas diferentes. Por exemplo: um depósito em uma conta poupança gera um certo rendimento ao saldo aplicado - para este caso um método abstrato é uma forma de garantir que este método seja implementado na classe ContaPoupança e em todas as outras classes que estende–lás.

##### Classes Finais
Uma classe final é uma classe que não pode ser estendida por nenhuma outra classe, ou seja, a classe final não tem herdeiros, pois ela é a última de sua hierarquia. Em nosso exemplo temos uma conta do tipo poupança que, pela regra de negócio de um banco, não possui uma derivação, ou seja, não deve ser estendida. Para estes casos definimos a classe como final, ou seja, somente existirão objetos da classe poupança e não filhos da mesma, pois o correto é que todas as contas estendam a nossa classe pai Conta e mais nenhuma outra, como mostra o próximo exemplo:
```PHP
<?php 
final class ContaPoupanca { 
     public function resgatar($valor){ 
     } 
     public function verSaldo(){ 
     } 
 } 
 $poupanca = new ContaPoupanca(); 
 $poupanca->resgatar(250); 
?>
```
##### Métodos Finais
Também podemos ter métodos finais que jamais podem ser reescritos nas classes filhas. Em nosso exemplo de agência bancária, podemos concluir que o método sacar de uma Conta é padrão para todas as Contas, independentemente de seu tipo. Quando temos uma situação como esta podemos definir estes métodos como final, impedindo assim que eles sejam reescritos e saiam do padrão estabelecido na classe pai, como mostra o exemplo a seguir:
```PHP
<?php 
 class Conta { 
     public function depositar($valor){ 
     } 
     
     final public function sacar($valor){ #método final, não pode ser reescrito 
     } 
 } 
 class ContaCorrente extends Conta{ public function depositar(){ 
      public function depositar(){
      } 
 } 
?>
```
##### Traits
Traits, a partir do PHP 5.4, nos proporcionam uma maneira simples e objetiva de reaproveitamento de código, pois são como classes onde usamos a palavra reservada trait, então escrevemos os métodos que queremos. E para usarmos um trait em uma classe usamos a palavra USE, como podemos observar no próximop exemplo:
```PHP
<?php 
 class Conta { 
     public $saldo = 0; 
     public function getSaldo() {
         echo "Saldo Atual: {$this->saldo}"; 
     } 
 } 
 trait Acoes { 
     public function getSaldo(){ 
         echo "Saldo Disponivel: {$this->saldo}"; 
     } 
     
     public function depositar($valor){ 
         $this->saldo += $valor; 
     } 
     
     public function sacar($valor){ 
         if($this->saldo >= $valor) { 
             $this->saldo -= $valor; 
         } 
     } 
 } 
 
 class ContaCorrente extends Conta { 
     use Acoes; 
 } 
 $o = new ContaCorrente(); 
     $o->depositar(500); 
     $o->sacar(200); 
     $o->getSaldo(); 
     // Saldo Disponivel: 300 
 ?>
 ```
Note que o método getSaldo() foi reescrito dentro do Trait, ou seja, irá sobrescrever os métodos da classe base (pai). Podemos ainda usar múltiplos traits em nossas classes, como no próximo exemplo.
```PHP
<?php 
 class Conta { 
     public $saldo = 0; 
     public function getSaldo() { 
         echo "Saldo Atual: {$this->saldo}"; 
     } 
 } 
 trait Acoes { 
     public function depositar($valor) { 
         $this->saldo += $valor; 
     } 
     public function sacar($valor) { 
         if($this->saldo >= $valor) {
             $this->saldo -= $valor; 
         } 
     } 
 } 
 trait consultaExtrato { 
     public function getSaldo() { 
         echo "Saldo Disponivel para saque:{$this->saldo}<br>"; 
     } 
     public function gerarExtrato($periodo) { 
         echo "Gerando extrato período $periodo aguarde..."; 
     } 
 } 
 class ContaCorrente extends Conta { 
     use Acoes, consultaExtrato; 
 } 
 $o = new ContaCorrente(); 
 $o->depositar(500); 
 $o->sacar(200); 
 $o->getSaldo(); 
 $o->gerarExtrato('20/01/2013'); 
?>
```
Desta vez temos dois traits com nomes diferentes, e note que sobrescrevemos o método getSaldo() novamente no trait consultaExtrato.

#### 2.4.2 PHP Data Objects(PDO)
O PDO veio para solucionar a migração de um banco de dados para outro, do MySQL para o PostgreSQL, por exemplo. O PDO é uma camada de abstração de acesso a dados, onde os métodos de manipulação de dados são independentes do SGDB que você está utilizando, ou seja, podemos usar as mesmas funções para executar queries e consultar dados.
O PDO veio no PHP 5.1 e dá suporte a vários sistemas gerenciadores de banco de dados, como MySQL, PostgreSQL, SQlite, Informix, Oracle, SQL Server, IBM e etc.
A conexão com um banco de dados através do PDO se dá durante a criação de um objeto da classe PDO, passando informações de conexão com o banco na forma de um DSN (Data Source Name), além das credencias de acesso, como mostra o próximo exemplo.
```PHP
<?php 
 // MySQL $db = new PDO("mysql:host=localhost;dbname=banco", "root", "senha"); 
 
 // PostgreSQL 
 
 $db = new PDO("pgsql:host=localhost;dbname=banco", "root", "senha"); 
 
 // SQLite 
 
 $db = new PDO("sqlite:banco.sqlite"); 
?>
```
Veja que criamos a $db que guarda um objeto da classe PDO e entre parênteses passamos o host, nome do banco, usuário e senha. Uma vez que o objeto da classe PDO tenha sido instanciado, conectamos em nosso banco. Para desconectar, basta "matarmos" o objeto ou aguardar que ele seja morto automaticamente ao final de nosso script, como podemos ver a seguir:
```PHP
<?php 
 $db = new PDO("mysql:host=localhost;dbname=banco", "root", ""); 
 unset($db); 
?>
```
Veja que utilizamos o unset para encerrar a conexão.

##### Executando Comandos
Depois de conectados temos a nossa disposição uma série de métodos para lidar com o banco. Utilizando a linguagem SQL, vamos fazer o uso do método exec, de acordo com o código do próximo exemplo.
```PHP
<?php  
  $db = new PDO("mysql:host=localhost;dbname=banco", "root", "");
   
  $db->exec("CREATE TABLE clientes(id INT AUTO_INCREMENT, nome VARCHAR(255), email VARCHAR(255)) ");
  ?>
```
Veja que acessamos o método exec através de nossa conexão com o “->” e criamos uma tabela chamada clientes com os campos id, nome e email.

##### Fazendo Consultas
Para fazer consultas usamos o método query, que executa um comando SQL e traz para nós linhas de um banco de dados. Veja o próximo exemplo.
```PHP
<?php 
     $db = new PDO("mysql:host=localhost;dbname=banco", "root", ""); 
  
     $dados = $db->query("SELECT * FROM clientes"); 
?>
```
Veja que dentro da $dados é executada uma query que traz todos os dados da tabela clientes. Podemos ainda acessar nossos dados através dos métodos fetch e fetchAll.
O método fetch retorna apenas um resultado para nós, enquanto o fetchAll irá retornar todos os resultados. Estes métodos retornam tanto um array quando um objeto, dependendo dos parâmetros especificados, como exemplo a seguir.
```PHP
<?php 
    $db = new PDO("mysql:host=localhost;dbname=banco", "root",""); 
    $dados = $db->query("SELECT * FROM clientes"); 
    $todos = $dados->fetchAll(); 
    $um = $dados->fetch(); 
    
    print_r($todos); 
    print_r($um); 
?>
```
Note que, por padrão, os métodos retornam índices associativos e numéricos. Podemos fazer com que somente índices associativos sejam mostrados ou apenas numéricos, como mostra o código a seguir
```PHP
<?php $db = new PDO("mysql:host=localhost;dbname=banco", "root",""); 
    $dados = $db->query("SELECT * FROM clientes"); 
    $assoc = $dados->fetchAll(PDO::FETCH_ASSOC); 
    $num = $dados->fetchAll(PDO::FETCH_NUM); 
    
    print_r($assoc); 
    print_r($num); 
?>
```
Veja que na $assoc queremos que seja retornado resultados em índices associativos, enquanto que na $num retorna apenas índices numéricos.

##### Transações
Transações são uma sequência de operações feitas em um sistema gerenciador de banco de dados. As transações têm o objetivo de proporcionar uma maneira de recuperar informações a partir de um desastre. Uma transação de banco de dados deve possuir atomicidade, consistência, isolamento e durabilidade (ACID).

Imagine um sistema onde temos que inserir dados em tabelas de estoque, pedido, cliente e logística. O cliente pagou e tudo foi inserido aparentemente bem no sistema, mas não foi inserido o pedido de entrega na tabela de logística. Temos um problema agora, certo?!

As transações evitam esse tipo de problema através do método beginTransaction do PDO. Após chamarmos o método, todos os comandos feitos não serão automaticamente executados. O PDO irá esperar pelo método commit para efetivar os comandos no banco de dados, ou pelo comando rollback para anular os comandos e desfazer tudo que foi feito. Veja o próximo exemplo.
```PHP
<?php 
    $db = new PDO("mysql:host=localhost;dbname=banco", "root", ""); 
    $db->beginTransaction(); 
    $db->exec("UPDATE pedidos SET compra = 5641"); 
    $db->exec("UPDATE clientes SET compra = 5641 "); 
    $db->exec("INSERT INTO logística(compra) VALUES (5641)"); 
    // Caso tudo tenha dado certo 
    $db->commit(); 
    
    // Caso não deu certo $db->rollback();
```
##### Prepared Statements
Statements são comandos SQL pré-construídos e garantem que nenhuma query que foi preparada sofra um ataque SQL injection, ou seja, um ataque baseado na manipulação do código SQL pela inserção de informações em uma query.

Imagine a inserção de vários dados em uma tabela. As únicas coisas que mudam são as informações de cada registro, a tabela e as colunas não mudam. Um statement então cria um INSERT onde vai inserir em tabela e colunas pré-determinadas, já que apenas as informações mudarão.

O PDO possui um método chamado prepare que, ao utilizá-lo, o comando não será executado, apenas preparado para ser executado depois. O método prepare retorna um objeto da classe PDOStatement para que, quando utilizamos esse método, precisamos criar placeholders que serão substituídos pelos valores que queremos que estejam naquela query. Veja o próximo exemplo.
```PHP
<?php
    $db = new PDO("mysql:host=localhost;dbname=banco", "root", "");
   
    $statement = $db->prepare("INSERT INTO posts (titulo, conteudo) VALUES
     (?, ?)");
```
Note que as interrogações são nossos placeholders, que serão substituídos por variáveis. Para executarmos as statements usamos o método execute, passando como parâmetro um array de variáveis que substituirão os placeholders, como mostra o exemplo a seguir.
```PHP
<?php 
    $db = new PDO("mysql:host=localhost;dbname=banco", "root", ""); 
    $statement = $db->prepare("INSERT INTO posts (titulo, conteudo) VALUES (?, ?)"); 
    $statement->execute(array("Arroz", "Meu primeiro item!")); 
    $statement->execute(array("Feijão", "Meu segundo item!")); 
    $statement->execute(array("Tomate", "Meu terceito item!"));
```
Note que temos apenas uma query, mas iremos executar três vezes com três valores diferentes. Estamos passando um array de informações para o método execute, que pegará essas informações e colocará no lugar das interrogações, ou seja, os placeholders.

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
