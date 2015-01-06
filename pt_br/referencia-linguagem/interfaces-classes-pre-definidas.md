[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | [Exceções pré-definidas](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/excecoes-pre-definidas.md) - **Interfaces e Classes pré-definidas** - [Contexto de opções e parâmetros](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/contexto-opcoes-parametros.md)


Interfaces e Classes pré-definidas
==================================

Perguntas
---------

<a name="back0245">0245</a> – Qual o objetivo da interface Traversable ?

<a href="#0245">Resposta</a>
***


<a name="back0246">0246</a> – Traversable pode ser aplicado isoladamente ?

<a href="#0246">Resposta</a>
***


<a name="back0247">0247</a> – Qual a finalidade da interface `Iterator`?

<a href="#0247">Resposta</a>
***


<a name="back0248">0248</a> – Quais os métodos que são necessários serem implementados quando usado `Iterator` ?

<a href="#0248">Resposta</a>
***


<a name="back0249">0249</a> – Executando o código abaixo teremos um exemplo básico da ordem que é executado os métodos 
quando usamos um `foreach` com um `iterator`, como seria essa ordem dos métodos ?

```php
class myIterator implements  Iterator {

    private $position = 0;

    private $array = array(
        "firstelement",
        "secondelement",
        "lastelement",
    );

    public function __construct()
    {
        $this->position = 0;
    }

    public function rewind()
    {
        var_dump(__METHOD__);
        $this->position = 0;
    }

    public function valid()
    {
        var_dump(__METHOD__);
        return isset($this->array[$this->position]);
    }

    public function current()
    {
        var_dump(__METHOD__);
        return $this->array[$this->position];
    }

    public function key()
    {
        var_dump(__METHOD__);
        return $this->position;
    }

    public function next()
    {
        var_dump(__METHOD__);
        ++$this->position;
    }
}

$it = new myIterator;

foreach ($it as $key => $value) {
    var_dump($key, $value);
    echo "\n";
}
```

<a href="#0249">Resposta</a>
***


<a name="back0250">0250</a> – Qual a finalidade da interface `ArrayAccess` ?

<a href="#0250">Resposta</a>
***


<a name="back0251">0251</a> – Quais os método da interface `ArrayAccess` ?

<a href="#0251">Resposta</a>
***


<a name="back0252">0252</a> – Analisando o trecho de código abaixo quais os métodos que seram retornados na sequência:

```php
class obj implements arrayaccess
{
    public function offsetSet($offset, $value)
    {
        var_dump(__METHOD__);
    }

    public function offsetExists($var)
    {
        var_dump(__METHOD__);

        if ($var == "foobar") {
            return true;
        }
        return false;
    }

    public function offsetUnset($var)
    {
        var_dump(__METHOD__);
    }

    public function offsetGet($var)
    {
        var_dump(__METHOD__);
        return "value";
    }
}

$obj = new obj;
echo "\n";

var_dump(isset($obj["foobar"]));
echo "\n";

var_dump(empty($obj["foobar"]));
echo "\n";

var_dump(empty($obj["foobaz"]));
echo "\n";
```

<a href="#0252">Resposta</a>
***


<a name="back0253">0253</a> – Interface para serialização personalizada, as classes que implementam esta interface 
ainda suportam métodos como `__sleep()` e `__wakeup()` ?

<a href="#0253">Resposta</a>
***


<a name="back0254">0254</a> – Qual o significado do termo `Closure` e qual sua finalidade ?

<a href="#0254">Resposta</a>
***


<a name="back0255">0255</a> – Analisando a classe abaixo como podemos "hackear" a classe `hackThursday` para acessar o 
membro privado `$dayOfWeek` fazendo um `bind` com a classe `Closure`

```php
class HackThursday {
	private $dayOfWeek = "Thursday \n";
}
```

<a href="#0255">Resposta</a>
***


<a name="back0256">0256</a> – Vimos a classe `closure` com o método estático `::bind` e o `::bindTo` como podemos usar ele ?

<a href="#0256">Resposta</a>
***







Respostas
---------

<a href="#back0245">voltar a pergunta</a><br/>
<a name="0245">0245</a> - **Resposta:** _Interface para detectar se uma classe é traversable para ser usada em um `forech`_

***


<a href="#back0246">voltar a pergunta</a><br/>
<a name="0246">0246</a> - **Resposta:** _Não, deve ser implementar `IteratorAggregate` ou `Iterator_

***


<a href="#back0247">voltar a pergunta</a><br/>
<a name="0247">0247</a> - **Resposta:** _Interface para `Iterator` externos ou objetos que podem ser iterados internamente, 
ou seja permite que um objeto possa ser percorrido em uma estrutura `foreach_

***


<a href="#back0248">voltar a pergunta</a><br/>
<a name="0248">0248</a> - **Resposta:**

 * current (retorna o elemento atual), 
 * key (retorna a chave do elemento atual), 
 * next(move da posição atual para o próximo elemento), 
 * rewind (Retrocede para o primeiro elemento do iterator), 
 * valid (Verifica se a posição atual é válida)

***


<a href="#back0249">voltar a pergunta</a><br/>
<a name="0249">0249</a> - **Resposta:**

Retorno:

    myIterator::rewind (Retrocede para o primeiro elemento do iterator)
    myIterator::valid (Verifica se a posição atual é válida)
    myIterator::current (retorna o elemento atual)
    myIterator::key (retorna a chave do elemento atual)
    myIterator::next (move da posição atual para o próximo elemento) conforme:
    
```php
public function next()
{
	var_dump(__METHOD__);
	++$this->position;
}
```

Logo em seguida será validado novamente a posição `(myIterator::valid)` sendo executado novamente a mesma sequência a cima 
sem o `rewind` que é executado no ínicio pois este método é chamado quando inicia se o loop `foreach`, não sendo executando 
novamente no decorrer da iteração, seguindo essa ordem iterando o `($this->array[$this->position])` parando em
`(myIterator::valid)` que é sempre chamado após `(myIterator::rewind)` e `(myIterator::next)` para verificar se a posição atual é válida.

***


<a href="#back0250">voltar a pergunta</a><br/>
<a name="0250">0250</a> - **Resposta:** _Interface para fornecer acesso a objetos como array_

***


<a href="#back0251">voltar a pergunta</a><br/>
<a name="0251">0251</a> - **Resposta:**

    abstract public offsetExists() // Se existir um deslocamento
    abstract public offsetGet() // Deslocamento para recuperar
    abstract public offsetSet() // Deslocamento para definir
    abstract public offsetUnset() // Diferença unset

***


<a href="#back0252">voltar a pergunta</a><br/>
<a name="0252">0252</a> - **Resposta:** _Os métods  `offsetExists` e  `offsetGet` são executados ao usar `isset()` e `empty()` 
em objetos de aplicação `ArrayAccess`_

    string(17) "obj::offsetExists"
    bool(true)
    
    string(17) "obj::offsetExists"
    string(14) "obj::offsetGet"
    bool(false)
    
    string(17) "obj::offsetExists"
    bool(true)

***


<a href="#back0253">voltar a pergunta</a><br/>
<a name="0253">0253</a> - **Resposta:** _Não é mais suportado métodos como `__sleep()` e `__wakeup()`_

***


<a href="#back0254">voltar a pergunta</a><br/>
<a name="0254">0254</a> - **Resposta:** _É uma classe para representar funções anônimas_

***


<a href="#back0255">voltar a pergunta</a><br/>
<a name="0255">0255</a> - **Resposta:**

MetaTrait.php
```php
trait MetaTrait
{
    private $methods = array();

    public function addMethod($methodName, $methodCallable)
    {
        if (!is_callable($methodCallable)) {
            throw new InvalidArgumentException('Second param must be callable');
        }
        $this->methods[$methodName] = Closure::bind($methodCallable, $this, get_class());
    }

    public function __call($methodName, array $args)
    {
        if (isset($this->methods[$methodName])) {
            return call_user_func_array($this->methods[$methodName], $args);
        }

        throw RunTimeException('There is no method with the given name to call');
    }
}
```

test.php
```php
require 'MetaTrait.php';

class HackThursday {
    use MetaTrait;

    private $dayOfWeek = "Thursday \n";

}

$test = new HackThursday();
$test->addMethod('when', function () {
    return $this->dayOfWeek;
});

echo $test->when();
```

***


<a href="#back0256">voltar a pergunta</a><br/>
<a name="0256">0256</a> - **Resposta:** _Basicamente serve para duplicar uma closure com um novo objeto vinculado e escopo de classe_

```php
class A {
    function __construct($val) {
        $this->val = $val;
    }
    function getClosure() {
        //returns closure bound to this object and scope
        return function() { return $this->val; };
    }
}

$ob1 = new A(1);
$ob2 = new A(2);

$cl = $ob1->getClosure();
echo $cl(), "\n";
$cl = $cl->bindTo($ob2);
echo $cl(), "\n";
```

***












