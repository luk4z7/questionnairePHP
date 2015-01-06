[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | [Exceções](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/excecoes.md) - **Generators** - [Referências](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/referencias.md)


Generators
==========

Perguntas
---------

<a name="back0215">0215</a> – Quais as vantagens de usar um generators ?

<a href="#0215">Resposta</a>
***


<a name="back0216">0216</a> – Generators foram implementados a partir de qual versão do PHP ?

<a href="#0216">Resposta</a>
***


<a name="back0217">0217</a> – Qual a diferença entre uma `function generator` e uma `function` convecional ?

<a href="#0217">Resposta</a>
***


<a name="back0218">0218</a> – Explique como funciona o `generator`, ele retorna um valor ? Ele pode ser iterado ?

<a href="#0218">Resposta</a>
***


<a name="back0219">0219</a> – Qual o significado da palavra-chave `yield`?

<a href="#0219">Resposta</a>
***


<a name="back0220">0220</a> – Analise o código abaixo e confirme a seguinte afirmativa de que `yield` pode ser chamado sem um
argumento para produzir um valor NULL com chave automática:

```php
function gen_three_nulls() {
    foreach (range(1, 3) as $i) {
        yield;
    }
}

var_dump(iterator_to_array(gen_three_nulls()));
```

<a href="#0220">Resposta</a>
***


<a name="back0221">0221</a> – `generators functions` são capazes de dar origem a valores de referência? demonstre abaixo 
refatorando o código! Qual o retorno do código abaixo e como ?

```php
function gen_reference() {
    $value = 3;

    while ($value > 0) {
        yield $value;
    }
}

foreach (gen_reference() as $number) {
    echo ($number).'... ';
}
```

<a href="#0221">Resposta</a>
***



Respostas
---------

<a href="#back0215">voltar a pergunta</a><br/>
<a name="0215">0215</a> - **Resposta:** _Um `generator` permite que você escreva código que usa um `foreach` para iterar sobre um 
conjunto de dados sem a necessidade de construir uma matriz na memória, o que pode fazer com que você ultrapasse um limite de 
memória, ou exigir uma quantidade considerável de tempo de processamento para gerar. Em vez disso, você pode escrever uma 
`function generator`, que é o mesmo com uma função normal, exceto que, em vez de retornar um vez, um `generator` pode gerar 
tantas vezes quanto ele precisa, a fim de proporcionar os valores a ser iterado_

***


<a href="#back0216">voltar a pergunta</a><br/>
<a name="0216">0216</a> - **Resposta:** _A partir do PHP 5.5_

***


<a href="#back0217">voltar a pergunta</a><br/>
<a name="0217">0217</a> - **Resposta:** _A diferença está em que uma função normal retorna um valor, e o generator produz tantos 
valores quanto ele precisa_

***


<a href="#back0218">voltar a pergunta</a><br/>
<a name="0218">0218</a> - **Resposta:** _Quando uma função de `generator` é chamada, ela retorna um objeto que pode ser iterado. 
Quando você iteragir sobre esse objeto (por exemplo, através de um loop foreach), o PHP irá chamar a função do `generator` cada 
vez que precisar de um valor, em seguida, salva o estado do `generator`  para quando precisar de um valor.
Um `generator` não pode retornar um valor: isso irá resultar em um erro de compilação, Uma instrução de retorno vazia é uma
sintaxe válida dentro de um `generator` e vai encerrar o `generator`_

***


<a href="#back0219">voltar a pergunta</a><br/>
<a name="0219">0219</a> - **Resposta:** _O coração de uma função de `generator` é a palavra-chave `yield`, na sua forma mais
simples, uma declaração de `yield` se parece muito com uma instrução de `return`, exceto que em vez de parar a execução da função 
e retornando o valor, em vez disso `yield` fornece um valor para o código de loop para o `generator` e interrompe a execução da
função `generator`_

***


<a href="#back0220">voltar a pergunta</a><br/>
<a name="0220">0220</a> - **Resposta:** _Sim, afirmativo_

retorno:

    array(3) {
      [0]=>
      NULL
      [1]=>
      NULL
      [2]=>
      NULL
    }

***


<a href="#back0221">voltar a pergunta</a><br/>
<a name="0221">0221</a> - **Resposta:** _O retorno será um loop infinito com valor de retorno 3, pois sempre entrará dentro da 
condição, com a referência poderia ser usada para contornar isso e não gerar um código infinito com um pre-decremento:_

```php
function &gen_reference() {
    $value = 3;

    while ($value > 0) {
        yield $value;
    }
}

foreach (gen_reference() as &$number) {
    echo (--$number).'... ';
}
```

***
