[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | [Namespaces](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/namespaces.md) - **Exceções** - [Generators](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/generators.md)


Exceções
========

Perguntas
---------

<a name="back0213">0213</a> – Como podemos disparar uma exceção no PHP e como podemos pegala, demonstre um exemplo!?

<a href="#0213">Resposta</a>
***


<a name="back0214">0214</a> – Levando em consideração que quando uma exceção é disparada, código logo após á instrução não será 
executado, e o PHP tentará achar o primeiro bloco `catch` correspondente a exceção disparada, Se não for pego, um erro fatal do 
PHP será lançado com uma mensagem `Uncaught Exception …`, a não ser que um tratador tenha sido definido com …. ? complete a frase 
e demonstre um exemplo!

<a href="#0214">Resposta</a>
***


Respostas
---------

<a href="#back0213">voltar a pergunta</a><br/>
<a name="0213">0213</a> - **Resposta:** _Uma exceção pode ser disparada `thrown`, ou pega `caught ou catched` no PHP_

```php
function inverse($x) {
	if (!$x) {
        		throw new Exception('Division by zero.');
    	}
    	else return 1/$x;
}

try {
	echo inverse(5) . "\n";
    	echo inverse(0) . "\n";
} catch (Exception $e) {
  	echo "Exceção pega: ",  $e->getMessage(), "\n";
}
```

***


<a href="#back0214">voltar a pergunta</a><br/>
<a name="0214">0214</a> - **Resposta:** _set_exception_handler()_

```php
function inverse($x) {
	if (!$x) {
        		throw new Exception('Division by zero.');
    	}
    	else return 1/$x;
}

try {
	echo inverse(5) . "\n";
    	echo inverse(0) . "\n";
} catch (Exception $e) {
  	echo "Exceção pega: ",  $e->getMessage(), "\n";
}
```

***

