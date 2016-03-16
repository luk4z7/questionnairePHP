[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | [Estruturas de Controle](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/estrutura-de-controle.md) - **Funções** - [Classes e Objetos](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/classes-objetos.md)


Funções
=======

Perguntas
---------

<a name="back0113">0113</a> – Qual nomeclatura que é dado para a seguinte função:

```php
function volunteer($a)
{
    if ($a <= 30) {
        echo "$a\n";
        volunteer($a + 1);
    }
}

volunteer(1);
```

<a href="#0113">Resposta</a>
***


<a name="back0114">0114</a> – Uma função no PHP é preciso ser criada antes de ser referenciada ?

<a href="#0114">Resposta</a>
***


<a name="back0115">0115</a> – Quais os tipos de passagens de argumentos podem ser passadas para as funções no PHP ?

<a href="#0115">Resposta</a>
***


<a name="back0116">0116</a> – O PHP permite o uso de arrays e do tipo especial NULL como valores pardrões !? De um exemplo:

<a href="#0116">Resposta</a>
***


<a name="back0117">0117</a> – Esse trecho de código nos retornara um erro 
(Warning: Missing argument 2 for iogurtera(), called in), analise o e responda qual o motivo de ter gerado esse erro 

```php
function iogurtera ($tipo = "azeda", $sabor)
{
    return "Fazendo uma taça de $sabor $tipo.\n";
}
echo iogurtera ("framboesa");
```

<a href="#0117">Resposta</a>
***


<a name="back0118">0118</a> – Demonstre um exemplo que retorne uma referência de uma função. 

<a href="#0118">Resposta</a>
***


<a name="back0119">0119</a> – É verdadeiro a seguinte afirmativa que valores escalares não são passados por referência e 
objetos são sempre passados por referência e retornados por referência, demonstre um exemplo ?

<a href="#0119">Resposta</a>
***


<a name="back0120">0120</a> – O que é uma função variável ?

<a href="#0120">Resposta</a>
***


<a name="back0121">0121</a> – Funções variáveis funcionam com construtores de linguagem como echo, print, unset, isset, empty, 
include, require, etc ... ? como podemos acessar esses construtores com funções variáveis, demonstre um exemplo.

<a href="#0121">Resposta</a>
***


<a name="back0122">0122</a> – Um método de objeto pode ser chamado com uma sintaxe de funções variáveis ?

<a href="#0122">Resposta</a>
***


<a name="back0123">0123</a> – Para usar funções `image` como `imagecreatetruecolor()` o PHP deve ser compilado com suporte a
qual extensão ?

<a href="#0123">Resposta</a>
***


<a name="back0124">0124</a> – O que são closures ?

<a href="#0124">Resposta</a>
***


<a name="back0125">0125</a> – Closures estão disponíveis desde qual versão ?

<a href="#0125">Resposta</a>
***


<a name="back0126">0126</a> – Demonstre um exemplo de uma closure

<a href="#0126">Resposta</a>
***


<a name="back0127">0127</a> – PHP 5.6 indroduz um novo recurso chamado de `variadics`, qual sua finalidade ? demonstre um exemplo!

<a href="#0127">Resposta</a>
***


<a name="back0128">0128</a> – `variadics` permite passar valores por referência ?

<a href="#0128">Resposta</a>
***


<a name="back0129">0129</a> – `variadics` permite indução de tipos ?

<a href="#0129">Resposta</a>
***


<a name="back0130">0130</a> – No PHP 5.6 qual a finalidade do operador de `splat` ? qual outro nome ele
é conhecido ? demonstre algum exemplo de seu uso!

<a href="#0130">Resposta</a>
***


<a name="back0131">0131</a> – Analisando o exemplo abaixo será emitido um `Warning`, qual o motivo de um retorno de `Warning`

```php

    var_dump(1, 2, ...null, ...[3, 4]);

```

<a href="#0131">Resposta</a>
***











Respostas
---------

<a href="#back0113">voltar a pergunta</a><br/>
<a name="0113">0113</a> - **Resposta:** _Recursividade, é uma função que a mesma chama-se várias vezes_

***


<a href="#back0114">voltar a pergunta</a><br/>
<a name="0114">0114</a> - **Resposta:** _Sim, é necessário que a função exista para ser referênciada_

***


<a href="#back0115">voltar a pergunta</a><br/>
<a name="0115">0115</a> - **Resposta:** _Passagens por argumento, valores default e passagem de valores por referência_

***


<a href="#back0116">voltar a pergunta</a><br/>
<a name="0116">0116</a> - **Resposta:** _Sim_

```php
function makecoffeeTest($types = array(“cappuccino”), $coffeeMaker = null) {
    $argumentos = func_num_args();
    $device = is_null($coffeeMaker) ? "hands" : $coffeeMaker;

    return "Making a cup of ".join(", ", $types)." with $device | números de argumentos é: $argumentos";
}
echo makecoffeeTest(array("cappuccino", "lavazza"), "teapot");
```

***


<a href="#back0117">voltar a pergunta</a><br/>
<a name="0117">0117</a> - **Resposta:** _argumentos padrões sempre devem ser passados após argumentos sem ser valores defaults_

```php
function  iogurtera ($sabor, $tipo = "azeda"){}
```

***


<a href="#back0118">voltar a pergunta</a><br/>
<a name="0118">0118</a> - **Resposta:**

```php
function &retorna_referencia(&$value)
{
    return $value++;
}

$value = 1;
$nova_referencia =& retorna_referencia($value);
retorna_referencia($value);
retorna_referencia($value);

echo $value . " valores";
```

***


<a href="#back0119">voltar a pergunta</a><br/>
<a name="0119">0119</a> - **Resposta:** _Sim, objetos são sempre passados e retornados por referência, diferente de dados 
escalares que é necessário forçar_

```php
// (1) objetos são sempre passados e retornados por referência
class Obj {
    public $x;
}

function obj_inc_x($obj) {
    $obj->x++;
    return $obj;
}

$obj = new Obj();
$obj->x = 1;

$obj2 = obj_inc_x($obj);
obj_inc_x($obj2);
obj_inc_x($obj2);
print $obj->x . ', ' . $obj2->x . "\n";
echo "\n";

// (2) dados escalares não são passado e retornados por referência
function scalar_inc_x($x) {
    $x++;
    return $x;
}

$x = 1;
$x2 = scalar_inc_x($x);
scalar_inc_x($x2);
print $x . ', ' . $x2 . "\n";
echo "\n";

// (3) Forçando para ser passado por referência e retornando por referência dados escalares
function &scalar_ref_inc_x(&$x) {
    $x++;
    return $x;
}

$x = 1;
$x2 =& scalar_ref_inc_x($x);
scalar_ref_inc_x($x2);
scalar_ref_inc_x($x2);
print $x . ', ' . $x2 . "\n";
echo "\n";
```

***


<a href="#back0120">voltar a pergunta</a><br/>
<a name="0120">0120</a> - **Resposta:** _Funções variáveis é um conceito em que um nome de uma variável
existi parenteses no final, o PHP procurará uma função com o mesmo nome, qualquer que seja a avaliação da variável, e tentará
executá-la_

***


<a href="#back0121">voltar a pergunta</a><br/>
<a name="0121">0121</a> - **Resposta:** _Não funcionam, nesse caso pode ser usar uma função de `wrapper` para usar quaisquer um
destes construtores com uma função variável_

```php
function echoit($string)
{
    echo $string;
}
$func = 'echoit';
$func('test');  // Chama echoit()
```

***


<a href="#back0122">voltar a pergunta</a><br/>
<a name="0122">0122</a> - **Resposta:** _Sim, um método de objeto também pode ser chamado com a sintaxe de funções variáveis:_

```php
class Foo
{
    function MetodoVariavel()
    {
        $name = 'Bar';
        $this->$name(); // Isto chama o método Bar()
    }

    function Bar()
    {
        echo "Bar foi chamada!";
    }
}

$foo = new Foo();
$funcname = "MetodoVariavel";
$foo->$funcname();  // Isto chama $foo->MetodoVariavel()
```

***


<a href="#back0123">voltar a pergunta</a><br/>
<a name="0123">0123</a> - **Resposta:** _Deve ser compilado com suporte a GD_

***


<a href="#back0124">voltar a pergunta</a><br/>
<a name="0124">0124</a> - **Resposta:** _Funções anonimas também conhecidas como closures, permitem a criação de funções que 
não tem o nome especificado_

***


<a href="#back0125">voltar a pergunta</a><br/>
<a name="0125">0125</a> - **Resposta:** _Desde a versão do PHP 5.3_

***


<a href="#back0126">voltar a pergunta</a><br/>
<a name="0126">0126</a> - **Resposta:**

```php
class Cart
{
	const PRICE_BUTTER = 1.00;
	const PRICE_MILK = 3.00;
	const PRICE_EGGS = 6.95;

	protected $products = array();

	public function add($product, $quantity)
	{
		$this->products[$product] = $quantity;
	} 

	public function getQuantity($product)
	{
		return isset($this->products[$product]) ? $this->products[$product] : FALSE;
	}

	public function getTotal($tax)
	{
		$total = 0.00;

		$callback = function ($quantity, $product) use ($tax, &$total)
		{
			$pricePerItem = constant(__CLASS__ . "::PRICE_" . strtoupper($product));
			$total += ($pricePerItem * $quantity) * ($tax + 1.0);
		};

		array_walk($this->products, $callback);
		return round($total, 2);
	}
}

$my_car = new Cart();

$my_car->add('butter', 1);
$my_car->add('milk', 3);
$my_car->add('eggs', 6);

print $my_car->getTotal(0.05) . "\n";
```

***


<a href="#back0127">voltar a pergunta</a><br/>
<a name="0127">0127</a> - **Resposta:** _`variadics` permite que você possa designar explicitamente uma função que aceita uma lista
de variáveis (argumentos)_

ex:

```php

    function fn($reqParam, $optParam = null, ...$params) {
        var_dump($reqParam, $optParam, $params);
    }

    fn(1);             // 1, null, []
    fn(1, 2);          // 1, 2, []
    fn(1, 2, 3);       // 1, 2, [3]
    fn(1, 2, 3, 4);    // 1, 2, [3, 4]
    fn(1, 2, 3, 4, 5); // 1, 2, [3, 4, 5]

```

***


<a href="#back0128">voltar a pergunta</a><br/>
<a name="0128">0128</a> - **Resposta:** _Sim_

ex:

```php

    function foo(&...$args) {
        // each argument is passed by reference
    }

```

***


<a href="#back0129">voltar a pergunta</a><br/>
<a name="0129">0129</a> - **Resposta:** _Sim_

ex:

```php

    function foo(array ...$args) {
        // each argument is an array
    }

```

***


<a href="#back0130">voltar a pergunta</a><br/>
<a name="0130">0130</a> - **Resposta:** _`Operador de Splat` ou mais conhecido como `Unpacking` (desenpacotador), funciona ao
contrário do que `variadics` faz, o que lhe permite descompactar uma estrutura de dados matriz como em uma lista de argumentos_

ex:

```php

    var_dump(1, 2, ...[3, 4]); // int(1) int(2) int(3) int(4)

```

```php

    function test($arg1, $arg2, $arg3 = null) {
        var_dump($arg1, $arg2, $arg3);
    }

    test(...[1, 2]);       // 1, 2, NULL
    test(...[1, 2, 3]);    // 1, 2, 3
    test(...[1, 2, 3, 4]); // 1, 2, 3

```

***


<a href="#back0131">voltar a pergunta</a><br/>
<a name="0131">0131</a> - **Resposta:** _Será gerado um `Warning`, pois quando for tentar descompactar algo que não for uma matriz
ou `Traversable` um aviso será lançado_

***












