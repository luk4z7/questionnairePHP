[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | [Tipos](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/tipos.md) - **Variáveis** - [Constantes](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/constantes.md)


Variáveis
=========

Perguntas
---------

<a name="back47">047</a> – A criação de uma variável em PHP segue um padrão, como pode ser válido o nome de uma variável ? 
Quais tipos de caracteres podem contém em uma variável?

<a href="#047">Resposta</a>
***


<a name="back48">048</a> – Como é o processo de atribuição por referência ? Demonstre um exemplo!

<a href="#048">Resposta</a>
***


<a name="back49">049</a> – Como podemos checar se uma variável foi inicializada ?

<a href="#049">Resposta</a>
***


<a name="back50">050</a> – Desde a versão 4.1.0, o PHP fornece um conjunto adicional de arrays predefinidos contendo variáveis do 
servidor web, conhecidas como superglobais, qual é o nome dessa diretiva que é habilitada no php.ini ?

<a href="#050">Resposta</a>
***


<a name="back51">051</a> – Defina a direfença entre variáveis pré-definidas e variáveis superglobais ?

<a href="#051">Resposta</a>
***


<a name="back52">052</a> – Uma variável criada fora de escopo de uma função que é necessário o acesso dela dentro do escopo 
dessa função pode ser acessado com a palavra reservada conhecida como ? De um exemplo !

<a href="#052">Resposta</a>
***


<a name="back53">053</a> – Demonstre um exemplo de uso de variáveis static !

<a href="#053">Resposta</a>
***


<a name="back54">054</a> – Referências são armazenadas estaticamente ?

<a href="#054">Resposta</a>
***


<a name="back55">055</a> – Olhando para o trecho de código abaixo receberemos um
(Fatal error: Cannot use [] for reading in)  como devemos proceder para resolver esse problema ?

```php
$array = array("one", "two", "three");
$a = "array";

$$a[] = "four";

print_r($array);
```

<a href="#055">Resposta</a>
***


<a name="back56">056</a> – Com o exemplo abaixo de código, qual será a saida dele ?

```php
$Bar = "a";
$Foo = "Bar";
$World = "Foo";
$Hello = "World";
$a = "Hello";

echo $a . "\n";
echo $$a . "\n";
echo $$$a . "\n";
echo $$$$a . "\n";
echo $$$$$a . "\n";
```

<a href="#056">Resposta</a>
***


<a name="back57">057</a> – Quais os perigos de register_globals e a partir de qual versão do PHP ele passou a vir desativado ?

<a href="#057">Resposta</a>
***


<a name="back58">058</a> – Supomos que a diretiva de configuração magic_quotes_gpc estiver ativa, qual o efeito de um valor 
sendo resgatado via POST, qual seria o resultado !?

    (It's “PHP!”)

<a href="#058">Resposta</a>
***


<a name="back59">059</a> – Independente de configuração de um ambiente demonstre três possibilidade de resgatar o valor que 
vem via post com o name ="username"!

<a href="#059">Resposta</a>
***



Respostas
---------

<a href="#back047">voltar a pergunta</a><br/>
<a name="047">047</a> - **Resposta:** _Uma variável no PHP é declarada com um simbolo de cifrão ($) seguido pelo nome da variável. 
O nome da variável se inicia como uma letra ou sublinhado, seguido por qualquer número, algarismo ou sublinhados_

***


<a href="#back048">voltar a pergunta</a><br/>
<a name="048">048</a> - **Resposta:** _O processo de referência simplesmente referencia (em outras palavras, 
“torna-se um apelido para” ou “aponta para”) a variável original, alterações na nova variável afetam a original e vice versa, 
para atruibuir por referência simplesmente adicione um e-comercial (&) na frente do nome da variável que estiver sendo atribuida (variável origem)_

```php
$two = 'two';
$one = &$two;
$two = " one - $two";
echo $two; // one - two
echo $one; // one – two
```

***


<a href="#back049">voltar a pergunta</a><br/>
<a name="049">049</a> - **Resposta:** _Atravéz do construtor da linguagem isset()_

***


<a href="#back050">voltar a pergunta</a><br/>
<a name="050">050</a> - **Resposta:** _register_globals, sendo desligada por default desde a versão 4.2.0_

***


<a href="#back051">voltar a pergunta</a><br/>
<a name="051">051</a> - **Resposta:** _Nenhuma, variáveis pré-definidas(nativas) do sitema são conhecidas com superglobais_

***


<a href="#back052">voltar a pergunta</a><br/>
<a name="052">052</a> - **Resposta:** _Palavra reservada para dar acesso a uma variável em vários escopos é (global)_

```php
function product() {
    global $item;
    $item = 'Computer';

    function itemOne() {
        global $item;
        echo "Item One: 40.00 R$ -- $item model one \n";
    }

    function itemTwo() {
        global $item;
        echo "Item Two: 60.00 R$ -- $item model two \n";
    }

    itemOne();
    itemTwo();
    echo "Item normal: 20.00 R$ -- $item model normal";

}

product();
```

***


<a href="#back053">voltar a pergunta</a><br/>
<a name="053">053</a> - **Resposta:** _Variáveis estáticas fornenecem uma solução ideal para funções recursivas, uma 
função recursiva é aquela que chama a si mesma_

```php
class test1{}
class test2{}
class test3{}

function cache($class) {
    static $loaders = array();
    $loaders[$class] = new $class;
    var_dump($loaders);
}

cache('test1');
cache('test2');
cache('test3');
```

Resultado do var_dump:

    array(1) {
        ["test1"]=>
      object(test1)#1 (0) {
      }
    }
    
    array(2) {
        ["test1"]=>
      object(test1)#1 (0) {
      }
      ["test2"]=>
      object(test2)#2 (0) {
      }
    }
    
    array(3) {
        ["test1"]=>
      object(test1)#1 (0) {
      }
      ["test2"]=>
      object(test2)#2 (0) {
      }
      ["test3"]=>
      object(test3)#3 (0) {
      }
    }
    
Usando a mesma função sem a variável static:

```php
class test1{}
class test2{}
class test3{}

function cache($class) {
    $loaders = array(); // sem o uso do static
    $loaders[$class] = new $class;
    var_dump($loaders);
}

cache('test1');
cache('test2');
cache('test3');
```

Resultado do var_dump:

    array(1) {
        ["test1"]=>
      object(test1)#1 (0) {
      }
    }
    array(1) {
        ["test2"]=>
      object(test2)#1 (0) {
      }
    }
    array(1) {
        ["test3"]=>
      object(test3)#1 (0) {
      }
    }

***


<a href="#back054">voltar a pergunta</a><br/>
<a name="054">054</a> - **Resposta:** _Não, Referências não são armazenadas estaticamente, esse exemplo demonstra que quando 
assimilamos uma referência para uma variável estática, ela não se lembra quando você chama a função &get_instance_ref() uma segunda vez_

```php
function &get_instance_ref() {
    static $obj;

    echo 'Objeto estatico: ';
    var_dump($obj);
    if (!isset($obj)) {
        // Assimila uma referencia a variavel estatica
        $obj = &new stdclass;
    }
    $obj->property++;
    return $obj;
}

function &get_instance_noref() {
    static $obj;

    echo "Objeto estatico: ";
    var_dump($obj);
    if (!isset($obj)) {
        // Assimila o objeto para a veriavel estatica
        $obj = new stdclass;
    }
    $obj->property++;
    return $obj;
}

$obj1 = get_instance_ref();
$still_obj1 = get_instance_ref();
echo "\n";
```

Resultado:
    
    Objeto estático: NULL 
    Objeto estático: NULL

```php
$obj2 = get_instance_noref();
$still_obj2 = get_instance_noref();
```

Resultado:

    Objeto estatico: NULL
    Objeto estatico: object(stdClass)(1) {
        ["property"]=>
    int(1)
    }

***


<a href="#back055">voltar a pergunta</a><br/>
<a name="055">055</a> - **Resposta:**

```php
$array = array("one", "two", "three");
$a = "array";

${$a}[] = "four";

print_r($array);
```

***


<a href="#back056">voltar a pergunta</a><br/>
<a name="056">056</a> - **Resposta:**

    hello
    World
    Foo
    Bar
    a

***


<a href="#back057">voltar a pergunta</a><br/>
<a name="057">057</a> - **Resposta:** _A partir do php 4.2.0 passou a ser definido como off, tornou-se obsoleta desde o 
PHP 5.3.0 e removida desde o PHP 5.4.0,  register_globals afeta o conjunto de variáveis pré-definidas disponíveis no escopo 
global, não recomendavel seu uso deixando seu código inseguro com essa diretiva ativada, não por a diretiva ser literalmente
insegura mas o uso incorreto dela é que é, quando habilitada, é possivel usar variáveis sem saber ao certo de onde elas vieram, 
register_globals criará para seus scritps vários tipos de variáveis oriundas de formulários HTML_

***


<a href="#back058">voltar a pergunta</a><br/>
<a name="058">058</a> - **Resposta:**

    It\'s \“PHP!\”

***


<a href="#back059">voltar a pergunta</a><br/>
<a name="059">059</a> - **Resposta:**

```php
$username; (register_global ativado)
$_POST['username'];
$_REQUEST['username'];

$HTTP_POST_VARS['username']; // PHP4
import_request_variables('p', 'p_'); // PHP4
echo $p_username;
```

***
