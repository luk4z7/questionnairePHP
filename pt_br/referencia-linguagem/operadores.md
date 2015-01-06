[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | [Expressões](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/expressoes.md) - **Operadores** - [Estrutura de Controle](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/estrutura-de-controle.md)


Operadores
==========

Perguntas
---------

<a name="back67">067</a> – Qual a ordem como as atribuições são analisadas ?

<a href="#067">Resposta</a>
***


<a name="back68">068</a> – Qual a diferença entre os pré-incremento e o pós-incremento ?

<a href="#068">Resposta</a>
***


<a name="back69">069</a> – O que é um operador ?

<a href="#069">Resposta</a>
***


<a name="back70">070</a> – Quais tipos de operadores existem no PHP ?

<a href="#070">Resposta</a>
***


<a name="back71">071</a> – Identifique todas as precedências dos operadores a baixo:

Tabela de associação

<table>
    <tr>
        <td>
            ID
        </td>
        <td>
            Operador
        </td>
        <td>
            Resposta
        </td>
    </tr>
    <tr>
        <td>1</td>
        <td>clone new</td>
        <td>?</td>
    </tr>
    <tr>
        <td>2</td>
        <td>[</td>
        <td>?</td>
    </tr>
    <tr>
        <td>3</td>
        <td>++ --</td>
        <td>?</td>
    </tr>
    <tr>
        <td>4</td>
        <td>~ - (int) (float) (string) (array) (object) (bool) @</td>
        <td>?</td>
    </tr>
    <tr>
        <td>5</td>
        <td>Instanceof</td>
        <td>?</td>
    </tr>
    <tr>
        <td>6</td>
        <td>!</td>
        <td>?</td>
    </tr>
    <tr>
        <td>7</td>
        <td>* / %</td>
        <td>?</td>
    </tr>
    <tr>
        <td>8</td>
        <td>+ - .</td>
        <td>?</td>
    </tr>
    <tr>
        <td>9</td>
        <td> &lt;&lt; &gt;&gt; </td>
        <td>?</td>
    </tr>
    <tr>
        <td>10</td>
        <td>&lt; &lt;= >= &lt;&gt;</td>
        <td>?</td>
    </tr>
    <tr>
        <td>11</td>
        <td>== != === !==</td>
        <td>?</td>
    </tr>
    <tr>
        <td>12</td>
        <td>&</td>
        <td>?</td>
    </tr>
    <tr>
        <td>13</td>
        <td>^</td>
        <td>?</td>
    </tr>
    <tr>
        <td>14</td>
        <td>|</td>
        <td>?</td>
    </tr>
    <tr>
        <td>15</td>
        <td>&&</td>
        <td>?</td>
    </tr>
    <tr>
        <td>16</td>
        <td>| |</td>
        <td>?</td>
    </tr>
    <tr>
        <td>17</td>
        <td>Sd= += -= *= /= .= %= &= |= ^= &lt;&lt;= >>=</td>
        <td>?</td>
    </tr>
    <tr>
        <td>18</td>
        <td>and</td>
        <td>?</td>
    </tr>
    <tr>
        <td>19</td>
        <td>xor</td>
        <td>?</td>
    </tr>
    <tr>
        <td>20</td>
        <td>or</td>
        <td>?</td>
    </tr>
    <tr>
        <td>21</td>
        <td>,</td>
        <td>?</td>
    </tr>
    <tr>
        <td>22</td>
        <td>?:</td>
        <td>?</td>
    </tr>
</table>

<a href="#071">Resposta</a>
***


<a name="back72">072</a> – Qual é o nome desse operador:

```php
-$a;
```

<a href="#072">Resposta</a>
***


<a name="back73">073</a> – Em quais momentos que o operador de divisão ("/") não retorna um valor como ponto flutuante ?

<a href="#073">Resposta</a>
***


<a name="back74">074</a> – Trabalhando um pouco com operadores de bit a bit qual seria o resultado da expressão abaixo:

```php
$a = 45;
// 00101101

$b = $a >> 3;

var_dump($b);
```

<a href="#074">Resposta</a>
***


<a name="back75">075</a> – Trabalhando com operadores de bitwase quando os operandos forem string como eles serão tratados ?

<a href="#075">Resposta</a>
***


<a name="back76">076</a> – Quando estamos usando o operador de bitwase & (Bitwise AND), tendo dois valores 
como exemplo: $a = 10, $b = 5, se comparase-mos os dois valores utilizando suas representações binárias, retornando um 
novo valor, como é feito o processo para formar esse novo valor ?

<a href="#076">Resposta</a>
***


<a name="back77">077</a> – Qual será o valor de retorno em sistema binário das seguintes expressões:

```php
a) 00000101 | 00000011
```

```php
b) 00000101 & 00000001
```

```php
c) 00000101 ^ 00000011
```
   
```php  
d) ~ 00000000000000000000000000000010
```

```php
e) 10000111 << 2
```
  
```php  
f) 10000111 >> 3
```

<a href="#077">Resposta</a>
***


<a name="back78">078</a> – Defina os nomes dos comparadores seguintes:

```php
a) $a == $b
```

```php
b) $a === $b
```

```php
c) $a != $b
```

```php
d) $a <> $b
```

```php
e) $a !== $b
```

```php
f) $a < $b
```

```php
g) $a > $b
```

```php
h) $a <= $b
```

```php
i) $a >= $b
```

<a href="#078">Resposta</a>
***


<a name="back79">079</a> – Seguindo a regra, quando é comparado um inteiro com uma string ela é convertida para um número, 
qual o rentorno da seguinte expressão:

```php
var_dump(0 == "a");
```

<a href="#079">Resposta</a>
***


<a name="back80">080</a> – O que é um "staking" de expressões ternárias ?

<a href="#080">Resposta</a>
***


<a name="back81">081</a> – Qual é o retorno do comando abaixo:

```php
echo ( true ? 'true' : false ? 't' : 'f' );
```

<a href="#081">Resposta</a>
***


<a name="back82">082</a> – Qual o retorno da seguinte expressão usando um type casting:

```php
if ((string) '0123' == (string) '123')
    print 'equals';
else
    print 'doesn\'t equal';
```

<a href="#082">Resposta</a>
***


<a name="back83">083</a> – Uma comparação de um array com um array quais são as convenções que são seguidas ?

<a href="#083">Resposta</a>
***


<a name="back84">084</a> – Descreva as convesões para comparações de tipos:

<table>
    <tr>
        <td>
            ID
        </td>
        <td>
            Tipo do 1º operando
        </td>
        <td>
            Tipo do 2º operando
        </td>
        <td>
            Resultado
        </td>
    </tr>
    <tr>
        <td>1</td>
        <td>null ou string</td>
        <td>string</td>
        <td>?</td>
    </tr>
    <tr>
        <td>2</td>
        <td>bool ou null</td>
        <td>qualquer</td>
        <td>?</td>
    </tr>
    <tr>
        <td>3</td>
        <td>object</td>
        <td>object</td>
        <td>?</td>
    </tr>
    <tr>
        <td>4</td>
        <td>string, resource ou number</td>
        <td>string, resource ou number</td>
        <td>?</td>
    </tr>
    <tr>
        <td>5</td>
        <td>Array</td>
        <td>array</td>
        <td>?</td>
    </tr>
    <tr>
        <td>6</td>
        <td>array</td>
        <td>qualquer</td>
        <td>?</td>
    </tr>
    <tr>
        <td>7</td>
        <td>object</td>
        <td>qualquer</td>
        <td>?</td>
    </tr>
</table>

<a href="#084">Resposta</a>
***


<a name="back85">085</a> – Qual é o operador de controle de erro no PHP ?

<a href="#085">Resposta</a>
***


<a name="back86">086</a> – O que é um operador de execução !?

<a href="#086">Resposta</a>
***


<a name="back87">087</a> – Como o operador de execução pode ser desativado ?

<a href="#087">Resposta</a>
***


<a name="back88">088</a> – Quais os tipos de incremetos que o PHP suporta ?

<a href="#088">Resposta</a>
***


<a name="back89">089</a> – Descreva os operadores de Incremento/Decremento abaixo:

```php
a) ++$a
```

```php
b) $a++
```

```php
c) --$a
```

```php
d) $a--
```

<a href="#089">Resposta</a>
***


<a name="back90">090</a> – Qual será o retorno do seguinte trecho de código ?

```php
$i = 'A';
for ($j = 0; $j < 6; $j++) {
    echo ++$i . "\n";
}
```

<a href="#090">Resposta</a>
***


<a name="back91">091</a> – Descreva os operadores abaixo:

```php
a) $a AND $b
```

```php
b) $a OR $b
```

```php
c) $a XOR $b
```

```php
d) !$a
```

```php
e) $a && $b
```

```php
f) $a || $b
```

<a href="#091">Resposta</a>
***


<a name="back92">092</a> – Qual a razão de possuir dois operadores "and" e "or" ?

<a href="#092">Resposta</a>
***


<a name="back93">093</a> – Quantos operadores de strings existem ?

<a href="#093">Resposta</a>
***


<a name="back94">094</a> – Qual é o retorno das seguintes expressões e se elas serão identicas ?

```php
$a = array(1,2,3,4) + array(5,6,7,8);
print_r($a);

$b = array_merge(array(1,2,3,4), array(5,6,7,8));
print_r($b);
```

<a href="#094">Resposta</a>
***


<a name="back95">095</a> – Qual é nome e como é usado o operador de tipo ?

<a href="#095">Resposta</a>
***


<a name="back96">096</a> – Em qual versão is_a() virou a ser obsoleto e quem os substitui ?

<a href="#096">Resposta</a>
***


Respostas
---------

<a href="#back067">voltar a pergunta</a><br/>
<a name="067">067</a> - **Resposta:** _As atribuições são analisadas da direita para a esquerda_

***


<a href="#back068">voltar a pergunta</a><br/>
<a name="068">068</a> - **Resposta:** _pré-incremento o PHP incrementa a variável antes de ler seu valor,
pós-incremento o PHP incrementa a variável depois de ler seu valor_

***


<a href="#back069">voltar a pergunta</a><br/>
<a name="069">069</a> - **Resposta:** _Um operador é algo que você alimenta com um ou mais valores (expressões) e que devolve 
outro valor (e por isso os próprios construtores se tornam expressões)_

***


<a href="#back070">voltar a pergunta</a><br/>
<a name="070">070</a> - **Resposta:** _Operadores unários, que operam em apenas um valor, (! ++)
Operadores binários_

***


<a href="#back071">voltar a pergunta</a><br/>
<a name="071">071</a> - **Resposta:** 

<table>
    <tr>
        <td>
            ID
        </td>
        <td>
            Operador
        </td>
        <td>
            Resposta
        </td>
    </tr>
    <tr>
        <td>1</td>
        <td>clone new</td>
        <td>Não associativo (clone e new)</td>
    </tr>
    <tr>
        <td>2</td>
        <td>[</td>
        <td>Esquerda (array)</td>
    </tr>
    <tr>
        <td>3</td>
        <td>++ --</td>
        <td>Não associativo (incremento/decremento)</td>
    </tr>
    <tr>
        <td>4</td>
        <td>~ - (int) (float) (string) (array) (object) (bool) @</td>
        <td>Não associativo (tipos)</td>
    </tr>
    <tr>
        <td>5</td>
        <td>Instanceof</td>
        <td>Não associativo (tipos)</td>
    </tr>
    <tr>
        <td>6</td>
        <td>!</td>
        <td>Direita (lógico)</td>
    </tr>
    <tr>
        <td>7</td>
        <td>* / %</td>
        <td>Esquerda (aritmético)</td>
    </tr>
    <tr>
        <td>8</td>
        <td>+ - .</td>
        <td>Esquerda (artimético and string)</td>
    </tr>
    <tr>
        <td>9</td>
        <td> &lt;&lt; &gt;&gt; </td>
        <td>Esquerda (Bit-a-bit)</td>
    </tr>
    <tr>
        <td>10</td>
        <td>&lt; &lt;= >= &lt;&gt;</td>
        <td>Não associativo (comparação)</td>
    </tr>
    <tr>
        <td>11</td>
        <td>== != === !==</td>
        <td>Não associativo (comparação)</td>
    </tr>
    <tr>
        <td>12</td>
        <td>&</td>
        <td>Esquerda (Bit-a-bit and referências)</td>
    </tr>
    <tr>
        <td>13</td>
        <td>^</td>
        <td>Esquerda (Bit-a-bit)</td>
    </tr>
    <tr>
        <td>14</td>
        <td>|</td>
        <td>Esquerda (Bit-a-bit)</td>
    </tr>
    <tr>
        <td>15</td>
        <td>&&</td>
        <td>Esquerda (lógico)</td>
    </tr>
    <tr>
        <td>16</td>
        <td>| |</td>
        <td>Esquerda (lógico)</td>
    </tr>
    <tr>
        <td>17</td>
        <td>Sd= += -= *= /= .= %= &= |= ^= &lt;&lt;= >>=</td>
        <td>Direita (atribuição)</td>
    </tr>
    <tr>
        <td>18</td>
        <td>and</td>
        <td>Esquerda (lógico)</td>
    </tr>
    <tr>
        <td>19</td>
        <td>xor</td>
        <td>Esquerda (lógico)</td>
    </tr>
    <tr>
        <td>20</td>
        <td>or</td>
        <td>Esquerda (lógico)</td>
    </tr>
    <tr>
        <td>21</td>
        <td>,</td>
        <td>Esquerda (muitos usos)</td>
    </tr>
    <tr>
        <td>22</td>
        <td>?:</td>
        <td>Esquerda (ternário)</td>
    </tr>
</table>

***


<a href="#back072">voltar a pergunta</a><br/>
<a name="072">072</a> - **Resposta:** _Negação, oposto_

***


<a href="#back073">voltar a pergunta</a><br/>
<a name="073">073</a> - **Resposta:** _O operador de divisão ("/") sempre retorna um valor com ponto flutuante, a não ser que 
os dois operandos seja inteiros (ou strings que são convertidas para inteiros) e números inteiramente divisíveis,
em outro caso um ponto flutuante é retornado_

***


<a href="#back074">voltar a pergunta</a><br/>
<a name="074">074</a> - **Resposta:** _Representação binária: 00000101 valor: 5_

***


<a href="#back075">voltar a pergunta</a><br/>
<a name="075">075</a> - **Resposta:** _Se ambos os parâmetros da esquerda e da direita forem strings, esses operadores irão 
trabalhar nos valores ASCII dos caracteres_

***


<a href="#back076">voltar a pergunta</a><br/>
<a name="076">076</a> - **Resposta:** _É comparado bit a bit se ambos estão ativos tanto em $a quanto em $b é retornado 
ativo (1) caso contrário e retornado desativado (0)_

convertendo da base 10 (decimal) para base 2 (binario)

    10 \ 2 = 5
    0
    
    5 \ 2 = 2.5
    1
    
    2 \ 2 = 1
    0
    
    1 \ 2 = 0.5
    1
    
    10 = 00001010
    
    5 \ 2 = 2.5
    1
    2 \ 2 = 1
    0
    1 \ 2 = 0.5
    1
    
    5 = 00000101
    
    10 =   00001010
    5  =   00000101
         ------------
           00000000

***


<a href="#back077">voltar a pergunta</a><br/>
<a name="077">077</a> - 

a) **Resposta:** 00000111<br/>
b) **Resposta:** 00000001<br/>
c) **Resposta:** 00000110<br/>
d) **Resposta:** 1111111111111111111111111111111101<br/>
e) **Resposta:** 00011100<br/>
f) **Resposta:** 00010000<br/>

***


<a href="#back078">voltar a pergunta</a><br/>
<a name="078">078</a> -

a) **Resposta:** Igual<br/>
b) **Resposta:** Idêntico<br/>
c) **Resposta:** Diferente<br/>
d) **Resposta:** Diferente<br/>
e) **Resposta:** Não idêntico<br/>
f) **Resposta:** Menor que<br/>
g) **Resposta:** Maior que<br/>
h) **Resposta:** Menor ou igual<br/>
i) **Resposta:** Maior ou igual<br/>

***


<a href="#back079">voltar a pergunta</a><br/>
<a name="079">079</a> - **Resposta:** _bool(true), pois string "a" é convertida para zero pois não começa com um dado númerico válido_

***


<a href="#back080">voltar a pergunta</a><br/>
<a name="080">080</a> - **Resposta:** _São expressões ternárias encadeadas uma dentro da outra_

***


<a href="#back081">voltar a pergunta</a><br/>
<a name="081">081</a> - **Resposta:** _t_

***


<a href="#back082">voltar a pergunta</a><br/>
<a name="082">082</a> - **Resposta:** _equals", quando comparado duas strings númericas serão comparadas como inteiras_

***


<a href="#back083">voltar a pergunta</a><br/>
<a name="083">083</a> - **Resposta:** _array com menos membros é menor, se a chave do operando 1 não é encontrada no operando 2, então os 
arrays são incomparáveis, caso contrário – compara valor por valor_

***


<a href="#back084">voltar a pergunta</a><br/>
<a name="084">084</a> - **Resposta:** 

* 1 – converte null para “”, númerico ou  comparação léxica
* 2 – converte para bool, FALSE < TRUE
* 3 – Quando usado operador de comparação (==), variáveis objetos são comparadas de maneira simples , nominalmente, quando usado operador de identidade (===), variáveis objetos são identicas se e somente se elas se referem a mesma instância da mesma classe.
* 4 – Transforma strings e resources para números
* 5 - array com menos membros é menor, se a chave do operando 1 não é encontrada no operando 2, então os arrays são incomparáveis, caso contrário – compara valor por valor
* 6 – é sempre maior
* 7 – é sempre maior

***


<a href="#back085">voltar a pergunta</a><br/>
<a name="085">085</a> - **Resposta:** _"@", Quando ele precede uma expressão em PHP, qualquer mensagem de erro que possa ser 
gerada por aquela expressão será ignorada_

***


<a href="#back086">voltar a pergunta</a><br/>
<a name="086">086</a> - **Resposta:** _São acentos graves, por sua vez o PHP irá interpretar e executar o conteúdo dos 
acentos graves como um comando do shell_

***


<a href="#back087">voltar a pergunta</a><br/>
<a name="087">087</a> - **Resposta:** _Quando a diretiva safe mode está ativa ou shell_exec() está desabilitada_

***


<a href="#back088">voltar a pergunta</a><br/>
<a name="088">088</a> - **Resposta:** _pré e pós-incremento e decremento no estilo C_

***


<a href="#back089">voltar a pergunta</a><br/>
<a name="089">089</a> -

a) **Resposta:** pré-incremento, incrementa $a em um, e então retorna $a<br/>
b) **Resposta:** pós-incremento, retorna $a, e então incrementa $a em um<br/>
c) **Resposta:** pré-decremento, decrementa $a em um, e então retorna $a<br/>
d) **Resposta:** pós-decremento, retorna $a, e então decrementa $a em um<br/>

***


<a href="#back090">voltar a pergunta</a><br/>
<a name="090">090</a> - **Resposta:**

    B
    C
    D
    E
    F
    G
    
Usando o pré-incremento, sendo incrementado depois rentornando o valor, caso fosse usado o pós-incremento teria começado com a 
letra 'A' e prosseguido

***


<a href="#back091">voltar a pergunta</a><br/>
<a name="091">091</a> -

a) **Resposta:** Operador lógico, Verdadeiro se tanto $a quanto $b são verdadeiros<br/>
b) **Resposta:** Operador lógico, Verdadeiro se $a ou $b são verdadeiros<br/>
c) **Resposta:** Operador lógico, Verdadeiro se $a ou $b são verdadeiros, mas não ambos<br/>
d) **Resposta:** Operador lógico, Verdadeiro se $a é verdadeiro<br/>
e) **Resposta:** Operador lógico, Verdadeiro se tanto $a quanto $b são verdadeiros<br/>
f) **Resposta:** Operador lógico, Verdadeiro se $a ou $b são verdadeiros<br/>

***


<a href="#back092">voltar a pergunta</a><br/>
<a name="092">092</a> - **Resposta:** _A razão para as duas variantes dos operandos "and" e "or" é que eles operam com 
precedências diferentes_

***


<a href="#back093">voltar a pergunta</a><br/>
<a name="093">093</a> - **Resposta:** _Há dois operadores, ('.') concatenação e atribuição de concatenação ('.=')_

***


<a href="#back094">voltar a pergunta</a><br/>
<a name="094">094</a> - **Resposta:** _Não serão identicas, pois a função merge_array zera os indices, já o exemplo de cima 
permaneçe com os mesmos valores 1,2,3,4 pois o segundo array tem os mesmos indices do primeiro, se somente  for atribuido o 
indice 5 => 5 será adicionado os demais automaticamente_

    Array
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
    )
    
    Array
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
        [4] => 5
        [5] => 6
        [6] => 7
        [7] => 8
    )

***


<a href="#back095">voltar a pergunta</a><br/>
<a name="095">095</a> - **Resposta:** _O nome é instanceof, usado para verificar se uma determinada variável é um objeto 
instânciado de uma certa classe_

***


<a href="#back096">voltar a pergunta</a><br/>
<a name="096">096</a> - **Resposta:** _O operador instanceof foi introduzido a apartir do PHP 5, antes disso is_a() era usado 
mas se tornou obsoleto pelo instanceof_

***





