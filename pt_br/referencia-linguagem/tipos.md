[Sintaxe Básica]( ) - **Tipos** - [Variáveis]( )


Tipos
=====

Perguntas
---------

<a name="back07">07</a> – Quantos tipos de dados o PHP suporta, e quais são eles ?

<a href="#07">Resposta</a>
***


<a name="back08">08</a> – Qual a diferença entre float e double ?

<a href="#08">Resposta</a>
***


<a name="back09">09</a> – Qual função pode ser usada para checar um tipo de uma variável / expressão ?

<a href="#09">Resposta</a>
***


<a name="back010">010</a> – Qual a maneira de forçar a conversão de uma variável ?

<a href="#010">Resposta</a>
***


<a name="back011">011</a> – Tipos booleanos foram introduzidos em qual versão do PHP ?

<a href="#011">Resposta</a>
***


<a name="back012">012</a> – Quais palavras-chaves são usadas para especificar um booleano ?

<a href="#012">Resposta</a>
***


<a name="back013">013</a> – Quais tipos de valores podem ser considerados com FALSE ?

<a href="#013">Resposta</a>
***


<a name="back014">014</a> – -1" é considerado FALSE, explique !?

<a href="#014">Resposta</a>
***


<a name="back015">015</a> – Responda com o valor correto para a saída do var_dump:

<a href="#015">Resposta</a>

```php
a) var_dump((bool) "");
```

```php
b) var_dump((bool) 1);
```

```php
c) var_dump((bool) -2);
```

```php
d) var_dump((bool) "foo");
```

```php
e) var_dump((bool) 2.3e5);
```

```php
f) var_dump((bool) array(12));
```

```php
g) var_dump((bool) array());
```

```php
h) var_dump((bool) "false");
```

***


<a name="back016">016</a> – Defina alguns tipos de notação que os inteiros podem ser especificados ?

<a href="#016">Resposta</a>
***


<a name="back017">017</a> – Qual função pode converter o valor de um inteiro ?

<a href="#017">Resposta</a>
***


<a name="back018">018</a> – Quando se trabalha com tipos ponto flutuantes quais as recomendações para tratamento desses tipos 
de dados, quais funções relacionadas a esse tipo de feature são muito últeis !?

<a href="#018">Resposta</a>
***


<a name="back019">019</a> – Porque não é recomendado testar números ponto flutuante com igualdade ?

<a href="#019">Resposta</a>
***


<a name="back020">020</a> – O que é o NAN em PHP ?

<a href="#020">Resposta</a>
***


<a name="back021">021</a> – Um caracter no PHP é equivalente a quantos bytes ?

<a href="#021">Resposta</a>
***


<a name="back022">022</a> – Quais as formas que uma string literal pode ser especificada ?

<a href="#022">Resposta</a>
***


<a name="back023">023</a> – A partir de qual versão foi incrementado o hererdoc ?

<a href="#023">Resposta</a>
***


<a name="back024">024</a> – É possível inicializar membros de classes ou constantes com nowdoc ?

<a href="#024">Resposta</a>
***


<a name="back025">025</a> – Qual versão foi adicionado o nowdoc ?

<a href="#025">Resposta</a>
***


<a name="back026">026</a> – Para escapar array multidimensionais dentro de strings literais especificadas com aspas 
duplas como é a maneira correta ? De um exemplo!

<a href="#026">Resposta</a>
***


<a name="back027">027</a> – Chamada de funções e métodos dentro de {$} está definido desde qual versão do PHP ?

<a href="#027">Resposta</a>
***


<a name="back028">028</a> – É possível acessar um caracter de uma string da seguinte maneira !?

```php
$str = "Pegando o primeiro caracter";
echo $str[0];
```

<a href="#028">Resposta</a>
***


<a name="back029">029</a> – Na conversão de string para números quando uma string será avaliada como um ponto fluante ? 
O que há define como um ponto flutuante na hora da conversão?

<a href="#029">Resposta</a>
***


<a name="back030">030</a> – Tendo como exemplo o seguinte trecho de código:

```php
$arr = array(5 => 1, 12 => 2);
```

logo em seguida for adicionado outro valor ao array, exemplo:

```php
$arr[] = 248;
```

Qual seria o valor do próximo indíce !?

<a href="#030">Resposta</a>
***


<a name="back031">031</a> – Com o exemplo abaixo qual seria o valor do índice no final do script quando é executado o print_r !?

```php
// Criando um array normal
$array = array(1, 2, 3, 4, 5);
print_r($array);

// Agora apagando todos os itens, mas deixando o array intacto:
foreach ($array as $i => $value) {
    unset($array[$i]);
}
print_r($array);

// Acrescentando um item
$array[] = 6;
print_r($array);
```

<a href="#031">Resposta</a>
***


<a name="back032">032</a> – Temos o seguinte exemplo a baixo, então podemos afirmar que esse trecho de código vai gerar um 
E-NOTICE !?

```php
$arr = array('fruta' => 'maçã');
print "Olá $arr[fruta]";
```

<a href="#032">Resposta</a>
***


<a name="back033">033</a> – Porque é errado a declaração de indices de arrays da seguinte maneira:

```php
$error_descriptions[E_ERROR] = “Um erro fatal ocorreu”;
```

<a href="#033">Resposta</a>
***


<a name="back034">034</a> – Qual será o valor do indíce criado para o valor 4 !?

```php
$array = array('cor' => 'vermelha',
    'sabor' => 'doce',
    'forma' => 'redonda',
    'nome' => 'maçã',
    4,
);
```

<a href="#034">Resposta</a>
***


<a name="back035">035</a> – Nesse exemplo usamos o print_r() para ter o resultado do array abaixo, está correto? Exemplifique!

```php
$array = array(10, 5 => 7, 3 => 6, 0 => 15);
```

resultado do print_r()

    array(
        [0] => 10
    	[5] => 7,
    	[3] => 6,
    	[0] => 15
    );

<a href="#035">Resposta</a>
***


<a name="back036">036</a> – Quando convertemos um valor em um objeto qual nome podemos usar no objeto para resgata-lo ?

```php
$obj = (object) 'String';
echo $obj-> ?
```

<a href="#036">Resposta</a>
***


<a name="back037">037</a> – A partir de qual versão o tipo resource foi incluído no PHP ?

<a href="#037">Resposta</a>
***


<a name="back038">038</a> – De um exemplo de um tipo de dado resource e seu retorno com a função get_resource_type()

<a href="#038">Resposta</a>
***


<a name="back039">039</a> – É necessário liberar manualmente memória  utilizando alguma função free_result nas aplicações ou 
somente é responsabilidade do coletor de lixo? Explique um pouco.

<a href="#039">Resposta</a>
***


<a name="back040">040</a> – A partir que qual versão php tipo null foi introduzino no PHP ?

<a href="#040">Resposta</a>
***


<a name="back041">041</a> – Quando uma variável pode ser considerada com null ?

<a href="#041">Resposta</a>
***


<a name="back042">042</a> – Um exemplo de uma função que é denominada como pseudo-tipo mixed e um number!

<a href="#042">Resposta</a>
***


<a name="back043">043</a> – Demonstre o uso de uma função call-back!

<a href="#043">Resposta</a>
***


<a name="back044">044</a> – Quando uma função retorna tipo void, o que significa isso no PHP ?

<a href="#044">Resposta</a>
***


<a name="back045">045</a> – Comente um pouco sobre a pseudo-variável ($....):

<a href="#045">Resposta</a>
***


<a name="back046">046</a> – Quais os tipos de moldagens permitidas no PHP (conversão de tipos) ?

<a href="#046">Resposta</a>
***


Respostas
---------

<a href="#back07">voltar a pergunta</a><br/>
<a name="07">07</a> - **Resposta:** _O PHP suporta oito tipos primitivos:_

* 1 boolean
* 2 integer
* 3 float (double)
* 4 string
* Compostos
    * 5 array
    * 6 object
* Tipos especiais
    * 7 resource
    * 8 NULL
* pseudo-tipo
    * mixed
    * number
    * callback
    * e a pseudo-variável $...

***


<a href="#back08">voltar a pergunta</a><br/>
<a name="08">08</a> - **Resposta:** _Ambos tem o mesmo papel, considerando o double como um float, os dois nomes existem por 
razões históricas_

***


<a href="#back09">voltar a pergunta</a><br/>
<a name="09">09</a> - **Resposta:** _var_dump() ou gettype(), ou as funções para checagem de cada tipo especifico:
is_int(), is_string(), is_null(), is_bool(), is_object(), is_array(), is_resource, is_callable, is_long, is_numeric, is_real etc ..._

***


<a href="#back010">voltar a pergunta</a><br/>
<a name="010">010</a> - **Resposta:** _Realizando um processo chamado de (casting), inserindo o tipo a ser convertido na frente da 
variável, forçando a conversão_

```php
$a = "1String"; 
var_dump($a); // string
$b = (int) $a; 
var_dump($b); // int
```

***


<a href="#back011">voltar a pergunta</a><br/>
<a name="011">011</a> - **Resposta:** _O tipo booleano foi introduzido ao PHP na versão 4_

***


<a href="#back012">voltar a pergunta</a><br/>
<a name="012">012</a> - **Resposta:** _true ou false_

***


<a href="#back013">voltar a pergunta</a><br/>
<a name="013">013</a> - **Resposta:**

* o próprio booleano FALSE
* o inteiro 0 (zero)
* o ponto flutuante 0.0 (zero)
* uma string vazia e a string “0”
* um array sem elementos
* um objeto sem elementos membros (somente PHP 4)
* o tipo especial NULL (incluindo variáveis não definida)
* o objeto SimpleXML criado de tags vazias

Qualquer outro valor é considerado como TRUE (incluindo tipo resource)

***


<a href="#back014">voltar a pergunta</a><br/>
<a name="014">014</a> - **Resposta:** _Não, é considerado como TRUE, assim como qualquer valor não zero (negativos ou positivos)_

***


<a href="#back015">voltar a pergunta</a><br/>
<a name="015">015</a> - 

a) **Resposta:** false<br/>
b) **Resposta:** true<br/>
c) **Resposta:** true<br/>
d) **Resposta:** true<br/>
e) **Resposta:** true<br/>
f) **Resposta:** true<br/>
g) **Resposta:** false<br/>
h) **Resposta:** true<br/>

***


<a href="#back016">voltar a pergunta</a><br/>
<a name="016">016</a> - **Resposta:**

* notação decimal (base 10)
* hexadecimal (base 16) ou 
* octal (base 8)

***


<a href="#back017">voltar a pergunta</a><br/>
<a name="017">017</a> - **Resposta:** _Na conversão explicita, pode se usar o próprio operador (int) na frente da variável ou 
a função intval()_

***


<a href="#back018">voltar a pergunta</a><br/>
<a name="018">018</a> - **Resposta:** _Para maior precisão é recomendados usar funções matemáticas de precisão arbitrária ou 
as funções relacionadas ao gmp_

***


<a href="#back019">voltar a pergunta</a><br/>
<a name="019">019</a> - **Resposta:** _porque não existe conversão para formato interno sem uma pequena perda de precisão, 
isso pode ocasionar resultados confusos: por exemplo floor((01.+0.7)*10) normalmente retornará 7, em vez de 8, porque a 
representação interna final será algo como  7.9999999999999991118...., então nunca confie em resultados com números de ponto 
flutuante até a última casa e nunca compare números de ponto flutuante em igualdade_

***


<a href="#back020">voltar a pergunta</a><br/>
<a name="020">020</a> - **Resposta:** _Constante que representa valor indefinido ou não representável nos cálculos de ponto flutuante_

***


<a href="#back021">voltar a pergunta</a><br/>
<a name="021">021</a> - **Resposta:** _Antes do PHP 6, um caracter é o mesmo que um byte_

***


<a href="#back022">voltar a pergunta</a><br/>
<a name="022">022</a> - **Resposta:**

* apóstofro
* aspas
* sintaxe heredoc
* sintaxe nowdoc

***


<a href="#back023">voltar a pergunta</a><br/>
<a name="023">023</a> - **Resposta:** _PHP 4_

***


<a href="#back024">voltar a pergunta</a><br/>
<a name="024">024</a> - **Resposta:** _Sim, diferente de heredocs, nowdocs pode ser usado no contexto de dado estático_

```php
class foo {
    public $bar = <<<'EOT'
bar
EOT;
}
```

***


<a href="#back025">voltar a pergunta</a><br/>
<a name="025">025</a> - **Resposta:** _PHP 5.3.0_

***


<a href="#back026">voltar a pergunta</a><br/>
<a name="026">026</a> - **Resposta:**

```php
$a = array("a", "b");
echo "escapando o array {$a[1]}";
```

***


<a href="#back027">voltar a pergunta</a><br/>
<a name="027">027</a> - **Resposta:** _Desde o PHP 5_

***


<a href="#back028">voltar a pergunta</a><br/>
<a name="028">028</a> - **Resposta:** _Sim. corretamente_

***


<a href="#back029">voltar a pergunta</a><br/>
<a name="029">029</a> - **Resposta:** _Será avaliada como ponto flutuante quando no inicio da string conter qualquer um dos caracteres 
'.', 'e' ou 'E' em outros casos será avaliado como inteiro_

***


<a href="#back030">voltar a pergunta</a><br/>
<a name="030">030</a> - **Resposta:** _13_

***


<a href="#back031">voltar a pergunta</a><br/>
<a name="031">031</a> - **Resposta:** _5, a maior chave inteira utilizada não precisa necessariamente existir no array, 
Ela pode ter existido no array desde a última vez que o array foi indexado_

***


<a href="#back032">voltar a pergunta</a><br/>
<a name="032">032</a> - **Resposta:** _Neste caso não será lançado pois está dentro das aspas duplas, e constantes não 
são observadas dentros de strings e por isso nenhum E-NOTICE será lançado aqui_

***


<a href="#back033">voltar a pergunta</a><br/>
<a name="033">033</a> - **Resposta:** _Errado pois o PHP vai interpretar como uma constante gerando um erro, uma constante 
indefinida_

***


<a href="#back034">voltar a pergunta</a><br/>
<a name="034">034</a> - **Resposta:** _0_

***


<a href="#back035">voltar a pergunta</a><br/>
<a name="035">035</a> - **Resposta:** _O indice é sobrescrito pelo segundo valor, então o exemplo acima é falso_

    array (
        [0] => 15,
        [5] => 7,
        [3] => 6
    )

***


<a href="#back036">voltar a pergunta</a><br/>
<a name="036">036</a> - **Resposta:**

```php
echo $obj->scalar;
```

***


<a href="#back037">voltar a pergunta</a><br/>
<a name="037">037</a> - **Resposta:** _PHP 4_

***


<a href="#back038">voltar a pergunta</a><br/>
<a name="038">038</a> - **Resposta:** _PHP 4_

```php
$fp = fopen("arrays.php", "w");
echo get_resource_type($fp)."\n";
```

***


<a href="#back039">voltar a pergunta</a><br/>
<a name="039">039</a> - **Resposta:** _Normalmente não é necessário, pois através do sistema de contagem de referência 
introduzido com a engine da Zend no PHP 4, quando um recurso não é mais referenciado, ele é automaticamente detectado 
(assim como no java). Quando isso acontece, todos os recursos em uso por esse recurso são liberados pelo coletor de lixo. 
Por essa razão, é raramente necessário liberar memória manualmente utilizando alguma função free_result_

***


<a href="#back040">voltar a pergunta</a><br/>
<a name="040">040</a> - **Resposta:** _PHP 4_

***


<a href="#back041">voltar a pergunta</a><br/>
<a name="041">041</a> - **Resposta:**

* Quando ela for assimilada com a constante NULL
* ela não recebeu nenhum valor ainda.
* ela foi apagada com unset()

***


<a href="#back042">voltar a pergunta</a><br/>
<a name="042">042</a> - **Resposta:** _str_replace(), usado tanto para string como para arrays, gettype() aceita todos os tipos do PHP_

***


<a href="#back043">voltar a pergunta</a><br/>
<a name="043">043</a> - **Resposta:**

```php
function my_callback_function() {
    echo 'Olá Mundo!';
}
call_user_func('my_callback_function');
```

***


<a href="#back044">voltar a pergunta</a><br/>
<a name="044">044</a> - **Resposta:** _void no tipo de retorno indica que não há valor a ser retornado. 
void na lista de parâmetros indica que a função não aceita parâmetros_

***


<a href="#back045">voltar a pergunta</a><br/>
<a name="045">045</a> - **Resposta:** _No protótipo de uma função significa e assim por diante. O nome desta variável é 
usada quando a função suporta infinito número de argumentos_

***


<a href="#back046">voltar a pergunta</a><br/>
<a name="046">046</a> - **Resposta:**

* (int) – molde para inteiro
* (bool) (boolean) – convete para booleano
* (float) (double) (real) – converte para número de ponto flutuante
* (string) – converte para string
* (binary) – converte para string binária (PHP 6)
* (array) – converte para array
* (object) – converte para objeto
* (unset) – converte para NULL (PHP 5)

***