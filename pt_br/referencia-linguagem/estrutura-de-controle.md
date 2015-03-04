[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | [Operadores](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/operadores.md) - **Estruturas de Controle** - [Funções](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/funcoes.md)


Estruturas de Controle
======================

Perguntas
---------

<a name="back097">097</a> – Avalidando o trecho de código abaixo quando usamos (':') para definir uma condição if / elseif 
podemos separar (else if ) em duas palavras ?

```php
if($a > $b):
    echo $a." message ".$b;
else if($a == $b): // Will not compile.
    echo "message";
endif;
```

<a href="#097">Resposta</a>
***


<a name="back098">098</a> – Qual seria a sintaxe alternativa para algumas estruturas de controle, demonstre para if, for, while !?

<a href="#098">Resposta</a>
***


<a name="back099">099</a> – A seguinte alternativa está correta ?

```php
isset( $value ) AND print( $value );
```

<a href="#099">Resposta</a>
***


<a name="back0100">0100</a> – Tendo em mente que o for é estrutura de controle mais complexa do PHP demonstre 4 exemplos que 
contam até 10 com for:

<a href="#0100">Resposta</a>
***


<a name="back0101">0101</a> – É possivel usar referência em um foreach como seria sua aplicação ?

<a href="#0101">Resposta</a>
***


<a name="back0102">0102</a> – A partir do PHP 5.5 é possível interagir sobre uma matriz de matrizes e descompactar o array 
aninhado, demonstre um exemplo:

<a href="#0102">Resposta</a>
***


<a name="back0103">0103</a> – A partir do PHP 5.4 houve uma mudanção na estrutura de controle break qual foi essa mudança?

<a href="#0103">Resposta</a>
***


<a name="back0104">0104</a> – Qual o resultado da seguinte estrutura de controle switch ?

```php
$i = 0;
switch ($i) {
    case 0:
        echo "i equals 0";
    case 1:
        echo "i equals 1";
    case 2:
        echo "i equals 2";
}
```

<a href="#0104">Resposta</a>
***


<a name="back0105">0105</a> – Essa estrutura de controle está correta usando (;) ponto e virgula no lugar da (,):

```php
$i = 0;
switch ($i) {
    case 0:
        echo "i equals 0";
    case 1:
        echo "i equals 1";
    case 2:
        echo "i equals 2";
}
```

<a href="#0105">Resposta</a>
***


<a name="back0106">0106</a> – Quando falamos sobre as estrutura de controle "declare" o que seria um "tick" ?

<a href="#0106">Resposta</a>
***


<a name="back0107">0107</a> – Registre o declare globalmente, e registre uma function tick, depois demonstre um exemplo de 
uso de declare e ticks:

<a href="#0107">Resposta</a>
***


<a name="back0108">0108</a> – O seguinte exemplo de código, qual será o resultado dele ?

```php
function retur($b) {

	if ((int)$b === 1)
		return print_r(array(1,2,3,4,5));

	echo "la la";
}
retur(1);
```

<a href="#0108">Resposta</a>
***


<a name="back0109">0109</a> – Qual a diferença entre require, require_once, include e include_once ?

<a href="#0109">Resposta</a>
***


<a name="back0110">0110</a> – Qual será o retorno abaixo analisando o trecho de código seguinte:

```php
goto a;
echo 'Foo';
 
a:
echo 'Bar' . "\n";
```

<a href="#0110">Resposta</a>
***


<a name="back0111">0111</a> – Explique como funcionar a estrutura de controle goto

<a href="#0111">Resposta</a>
***


<a name="back0112">0112</a> – goto está disponivel apartir de qual versão do PHP ?

<a href="#0112">Resposta</a>
***


<a name="back0113">0113</a> – O que representa a constante `PHP_EOL` ?

<a href="#0113">Resposta</a>
***





Respostas
---------

<a href="#back097">voltar a pergunta</a><br/>
<a name="097">097</a> - **Resposta:** _Não pode usar o (else if) separado nesse contexto, o PHP vai falhar com um erro de analise, 
para usar o (else if) separado use chaves_

***


<a href="#back098">voltar a pergunta</a><br/>
<a name="098">098</a> - **Resposta:**

```php
if ($a == 8):
    echo "value 8";
endif;

for ($i = 0; $i < 10; $i++):
    echo $i;
endfor;

$i = 1;
while($i < 10):
    echo $i;
    $i++;
endwhile;
```

***


<a href="#back099">voltar a pergunta</a><br/>
<a name="099">099</a> - **Resposta:** _sim está correta, seria o mesmo que:_

```php
if (isset($value)) {
    print($value);
}
```

***


<a href="#back0100">voltar a pergunta</a><br/>
<a name="0100">0100</a> - **Resposta:**

```php
for ($i = 1; $i <= 10; $i++) {
    echo $i;
}

for ($i = 1; ; $i++) {
    if ($i < 10) {
        break;
    }
    echo $i;
}

$i = 1;
for (; ; ) {
    if ($i < 10) {
        break;
    }
    echo $i;
    $i++;
}

for ($i = 1, $j = 0; $i <= 10; $j += $i, print "ola" . "\n", $i++);
```

***


<a href="#back0101">voltar a pergunta</a><br/>
<a name="0101">0101</a> - **Resposta:** _Sim_

```php
$arr = array(1, 2, 3 ,4);
foreach ($arr as &$value) {
    $value = $value * 2;
    echo $value . "\n";
}

var_dump($arr);
```

variável $arr tem seu valor alterado:

    array(4) {
      [0]=>
      int(2)
      [1]=>
      int(4)
      [2]=>
      int(6)
      [3]=>
      &int(8)
    }

***


<a href="#back0102">voltar a pergunta</a><br/>
<a name="0102">0102</a> - **Resposta:** _Sim_

```php
$array = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9],
    [10, 11, 12],
];

foreach ($array as list($a, $b, $c)) {
    echo "A: $a; B: $b; C: $c \n";
}
```

***


<a href="#back0103">voltar a pergunta</a><br/>
<a name="0103">0103</a> - **Resposta:** _Removido a capacidade de passar em variáveis valores númericos como argumento_

```php
$num = 2; break $num;
```

***


<a href="#back0104">voltar a pergunta</a><br/>
<a name="0104">0104</a> - **Resposta:** _A instrução switch executa linha por linha até uma instrução case ser encontrada, 
quando não é usado a instrução break o PHP continuará executando as declarações_

    i equals 0
    i equals 1
    i equals 2
    
***


<a href="#back0105">voltar a pergunta</a><br/>
<a name="0105">0105</a> - **Resposta:** _Sim, é possivel usas ponto e virgula nessa situação_

***


<a href="#back0106">voltar a pergunta</a><br/>
<a name="0106">0106</a> - **Resposta:** _Um tick é um evento especial que ocorre internamente no PHP cada vez que ele foi 
executado um determinado número de declarações_

***


<a href="#back0107">voltar a pergunta</a><br/>
<a name="0107">0107</a> - **Resposta:**

```php
declare(ticks=1);

function myfunc() {
    echo "ticks exemplo \n";
}
register_tick_function('myfunc');
$a = "";
$a = "";
$a = "";
```

Saída

    ticks exemplo
    ticks exemplo
    ticks exemplo
    ticks exemplo

***


<a href="#back0108">voltar a pergunta</a><br/>
<a name="0108">0108</a> - **Resposta:**

Saída

    Array
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
        [4] => 5
    )

***


<a href="#back0109">voltar a pergunta</a><br/>
<a name="0109">0109</a> - **Resposta:** _require é idêntico a include, exeto em caso de falha que tambem ira produzir um erro 
a nível de E_COMPILER_ERROR. Em outras palavras o script será abortado enquanto que include emite um E_WARNING que permite 
que o script continue, o once serve para verificar se o arquivo foi incluido mais de uma vez_

***


<a href="#back0110">voltar a pergunta</a><br/>
<a name="0110">0110</a> - **Resposta:** _Bar_

***


<a href="#back0111">voltar a pergunta</a><br/>
<a name="0111">0111</a> - **Resposta:** _operador goto é usado para saltar para outro ponto no programa, o ponto de destino é 
especificado por um rótulo seguido por dois pontos e a instrução é dada como goto seguido pelo rótulo de destino desejado_

***


<a href="#back0112">voltar a pergunta</a><br/>
<a name="0112">0112</a> - **Resposta:** _O operador goto está disponível apartir do PHP 5.3_

***


<a href="#back0113">voltar a pergunta</a><br/>
<a name="0113">0113</a> - **Resposta:** _Representa `end of line` (fim da linha), marcador para seu sistema operacional atual_

***