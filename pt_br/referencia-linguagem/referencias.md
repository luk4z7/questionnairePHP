[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | [Generators](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/generators.md) - **Referências** - [Variáveis pré-definidas](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/variaveis-pre-definidas.md)


Referências
===========

Perguntas
---------

<a name="back0222">0222</a> – O que são referências em PHP ?

<a href="#0222">Resposta</a>
***


<a name="back0223">0223</a> – Quando é atribuido, passado ou retornado uma variável indefinida por referência o que acontece ? 
Qual o retorno do exemplo abaixo ?

```php
function foo(&$var) { }

$b = array();
foo($b['b']);
var_dump(array_key_exists('b', $b));
```

<a href="#0223">Resposta</a>
***


<a name="back0224">0224</a> – A partir de qual versão foi introduzido no PHP a possibilidade de retornar referência com o operador `new`?

<a href="#0224">Resposta</a>
***


<a name="back0225">0225</a> – A partir de qual versão que o `new` retorna referência automaticamente e o uso de `=&` passou a ser obsoleto ?

```php
$bar =& new fooclass();
$foo =& find_var ($bar);
```

<a href="#0225">Resposta</a>
***


<a name="back0226">0226</a> – Se você atruibuir uma referência para uma variável declarada `global` dentro da função, a 
referência irá ser visível somente dentro da função, como podemos evitar isso ?

```php
$var1 = "Example variable";
$var2 = "";

function global_references()
{
    global $var1, $var2;
    $var2 =& $var1;
}

global_references();
echo "var2 is set to '$var2'\n";
```

Retorno:

    var2 is set to ''

<a href="#0226">Resposta</a>
***


<a name="back0227">0227</a> – Analisando o código abaixo, diga se é possível atribuir um valor para uma variável com referência 
no comando `foreach`, qual o seu retorno do código ?

```php
$ref = 0;
$row =& $ref;
foreach (array(1, 2, 3, 4, 5) as $row) {
    // faz alguma coisa
}
echo $ref;
```

<a href="#0227">Resposta</a>
***


<a name="back0228">0228</a> – Partindo do pressuposto que é possível passar um variável por referência, qual será o retorno do 
código abaixo ?

```php
function foo (&$var)
{
    $var++;
}

$a = 5;
foo ($a);

echo $a;
```

<a href="#0228">Resposta</a>
***


<a name="back0229">0229</a> – Destruindo referências, analisando o código abaixo, qual será o valor de `$b` sendo que `$a` foi destruida !?

```php
$a = 1;
$b =& $a;
unset ($a);
echo $b;
```

<a href="#0229">Resposta</a>
***


<a name="back0230">0230</a> – Temos dois casos de referências `(global, $this)` explique porque são casos de refências:

<a href="#0230">Resposta</a>
***



Respostas
---------

<a href="#back0222">voltar a pergunta</a><br/>
<a name="0222">0222</a> - **Resposta:** _Referências em PHP, significa acessar o mesmo conteúdo de variável através de vários nomes_

***


<a href="#back0223">voltar a pergunta</a><br/>
<a name="0223">0223</a> - **Resposta:** _bool(true), quando removido a referência de foo ($var) o valor é retornado como false_

***


<a href="#back0224">voltar a pergunta</a><br/>
<a name="0224">0224</a> - **Resposta:** _A partir do PHP 4.0.4_

***


<a href="#back0225">voltar a pergunta</a><br/>
<a name="0225">0225</a> - **Resposta:** _Desde o PHP 5 `new`, retorna referência automaticamente, então  usar `=&` neste contexto 
é obsoleto e produz mensagem de nível `E_STRICT`_

***


<a href="#back0226">voltar a pergunta</a><br/>
<a name="0226">0226</a> - **Resposta:** _Usando o array `$GLOBALS["var2"] =& $var1`_

***


<a href="#back0227">voltar a pergunta</a><br/>
<a name="0227">0227</a> - **Resposta:** _Sim, é possível, o retorno é 5_

***


<a href="#back0228">voltar a pergunta</a><br/>
<a name="0228">0228</a> - **Resposta:** _6, pois `$var` está acessando o mesmo contéudo que `$a`_

***


<a href="#back0229">voltar a pergunta</a><br/>
<a name="0229">0229</a> - **Resposta:** _1, A variável `$a` foi removida mas `$b` não, nesse caso removendo `$a` ela somente 
quebra uma referência ou seja para somente de fazer o apontamento entre o nome da variável e o conteúdo, mas não significa que o 
conteúdo da variável será destruido_

***


<a href="#back0230">voltar a pergunta</a><br/>
<a name="0230">0230</a> - **Resposta:** _`global`, pois quando declaramos uma variável como `global` está sendo de fato criado 
uma referência para a variável global. Isto significa que isto é o mesmo que:_

```php
$var =& $GLOBALS["var"];
```

O que significa também que destruir $var não apaga a variável global.
`$this`, é sempre uma referência à instância atual.

***


