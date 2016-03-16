[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | [Classes e Objetos](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/classes-objetos.md) - **Namespaces** - [Exceções](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/excecoes.md)


Namespaces
==========

Perguntas
---------

<a name="back0200">0200</a> – O que são `namespaces`?

<a href="#0200">Resposta</a>
***


<a name="back0201">0201</a> – `namespaces` foram projetados para resolver qual tipo de problema enfrentado pelos desenvolvedores PHP ?

<a href="#0201">Resposta</a>
***

<a name="back0202">0202</a> – Demonstre um exemplo de uso de `namespaces`:

<a href="#0202">Resposta</a>
***


<a name="back0203">0203</a> – Levando em consideração que nenhuma construção de código é permitido antes de uma declaração de 
`namespace` o código abaixo está correto !?

```php
declare(ticks=1);

namespace MyProject;

const CONNECT_OK = 1;
class Connection {

	public function __construct()
	{
		echo CONNECT_OK . "\n";
	}
}

$class  = new Connection();
```

<a href="#0203">Resposta</a>
***


<a name="back0204">0204</a> – Analisando o código, é possível declarar dois namespaces em um único arquivo ? Qual o retorno do 
código abaixo:

```php
namespace MyProject;

const CONNECT_OK = 2;
echo \MyProject\CONNECT_OK . "\n";

namespace AnotherProject;

const CONNECT_OK = 1;
echo \AnotherProject\CONNECT_OK . "\n";
```

<a href="#0204">Resposta</a>
***


<a name="back0205">0205</a> – Analisando o código abaixo o segundo exemplo de sintaxe ele é suportado pelo PHP ? Qual o 
retorno do código:

```php
namespace MyProject;

const CONNECT_OK = 2;
echo \MyProject\CONNECT_OK . "\n";

namespace AnotherProject;

const CONNECT_OK = 1;
echo \AnotherProject\CONNECT_OK . "\n";


namespace MyProject2 {
	const CONNECT_OK = 1;
}

namespace AnotherProject2 {
	const CONNECT_OK = 3;
}
```

<a href="#0205">Resposta</a>
***


<a name="back0206">0206</a> – Demonstre um exemplo de um arquivo PHP onde contém um código namespaced e um código não 
namespaced (código global):

<a href="#0206">Resposta</a>
***


<a name="back0207">0207</a> – Demonstre três formas de acessar uma classe `Nome não qualificado`, `Nome qualificado`,
`Nome completo`:

<a href="#0207">Resposta</a>
***


<a name="back0208">0208</a> – A implementação do PHP de namespace é influênciada pela sua natureza dinâmica, vamos ver um 
exemplo de acesso dinâmico por namespace, observe que não há diferença entre um nome qualificado e um nome completo:

```php
namespace namespacename;
class classname
{
    function __construct()
    {
        echo __METHOD__ . "\n";
    }
}
function funcname()
{
    echo __FUNCTION__ . "\n";
}
const constname = "namespaced";

$a = '\namespacename\classname'; // nome completo
$obj = new $a;
$a = 'namespacename\classname'; // nome qualificado
$obj = new $a;
$b = 'namespacename\funcname'; // nome qualificado
$b();
$b = '\namespacename\funcname'; // nome completo
$b();
echo constant('\namespacename\constname'), "\n"; // nome completo
echo constant('namespacename\constname'), "\n"; // nome qualificado
```

Retorno:

    namespacename\classname::__construct
    namespacename\classname::__construct
    namespacename\funcname
    namespacename\funcname
    namespaced
    namespaced
    
Obervando o exemplo acima, qual será o retorno do código abaixo:

file2.php
```php
class classname
{
    function __construct()
    {
        echo __METHOD__ . ' ' . basename(__FILE__) . " \n";
    }
}
function funcname()
{
    echo __FUNCTION__ . ' ' . basename(__FILE__) . " \n";
}

const constname = "global";
```

basic.php
```php
namespace namespacename;
class classname
{
    function __construct()
    {
        echo __METHOD__ . "\n";
    }
}
function funcname()
{
    echo __FUNCTION__ . "\n";
}
const constname = "namespaced";

include 'file2.php';

$a = 'classname';
$obj = new $a;
$b = 'funcname';
$b();
echo constant('constname'), "\n";

$a = '\namespacename\classname';
$obj = new $a;
$b = 'namespacename\funcname';
$b(); // prints namespacename\funcname
echo constant('namespacename\constname'), "\n";
```

<a href="#0208">Resposta</a>
***


<a name="back0209">0209</a> – Quais as duas maneiras abstratas de acessar elementos dentro de um namespace ?

<a href="#0209">Resposta</a>
***


<a name="back0210">0210</a> – Namespaces PHP suportam três tipos de `aliasing` ou `importing`, quais são eles ?

<a href="#0210">Resposta</a>
***


<a name="back0211">0211</a> – Analisando as regras e convensões de resoluções de namespaces, responda Correto ou Incorreto:

> 1.  Chamadas para funções totalmente qualificadas, classes ou constantes são resolvidas em tempo de compilação, por exemplo: 
      `\A\B` resolve classe `A\B`
>
> 2.  Dentro de um namespace, todos os nomes qualificados não truduzidos de acordo com as regras de importação tem o namespace 
      atual prefixado. Por exemplo: se uma chamada para `C\D\e()` é executada dentro de namespace `A\B` é traduzido para 
      `A\B\C\D\e()`
>
> 3.  Nomes de classes não qualificadas são traduzidos durante a compilação de acordo com as regras de importação atuais 
      (nome completo substituido pelo pequeno nome importado). 
      No exemplo, se o namespace `A\B\C` é importado como `C`, `new C()` é traduzido para o novo `A\B\C()`
>
> 4.  Dentro do namespace atual ex: `A\B`, chamadas para funções não qualificadas são resolvidas em tempo de execução.
      Exemplo de uma chamada para uma função `foo()` 
      É procurado por uma função do atual namespace `A\B\foo()`
      E tenta encontrar e chamar a função global `foo()`
>     
> 5.  Dentro de namespace atual ex: `A\B`, chamadas para nomes de classes não qualificadas ou qualificadas (não nomes de 
      classes totalmente qualificados), são resolvidos em tempo de compilação.
      Exemplo de chamada para `new C()` ou `new D\e()` como é resolvido:
      exemplo com `new C()`
      Ele procura por uma classe do namespace atual `A\B\C`
      Ele tenta autoload `A\B\C`
      exemplo com `D\e()` 
      Ele procura por uma classe, antecedendo o namespace atual `A\B\D\e()`
      Ele tenta autoload `A\B\D\e()`
>

<a href="#0211">Resposta</a>
***


<a name="back0212">0212</a> – FAQ: Coisas que você precisa saber sobre namespaces.

> 1. Se eu não usar namespaces, eu deveria me importar com isso?
>
> 2. Como faço para usar classes internas ou globais em um namespace?
>
> 3. Como faço para usar as classes namespaces, funções ou constantes em meu próprio namespace?
>
> 4. Como é que o seguintes namespaces `\my\name` ou `\name` resolvem?
>
> 5. Como é que o seguinte namespace `my\name` resolve?
>
> 6. Como é que o nome da classe não qualificado como `name` resolve ?
>
> 7. Como é que um nome de uma função não qualificada ou nome de uma constante não qualificada resolve?
>
> 8. Nomes de importação não pode entrar em conflito com as classes definidas no mesmo arquivo.
>
> 9. Namespaces aninhados não são permitidos
>    ```php
>    namespace my\stuff {
>       namespace nested {
>           class foo {}
>       }
>    }
>    ```
>
> 10. Nem funções nem constantes podem ser importados através da declaração `use`
>
> 11. namespaces dinâmicos (identificadores entre aspas) devem escapar barra invertida
>
> 12. Constantes Undefined referenciadas usando qualquer barra invertida morre com um erro fatal
>
> 13. Não pode substituir constantes especiais `NULL, TRUE, FALSE, ZEND_THREAD_SAFE ou ZEND_DEBUG_BUILD`


<a href="#0212">Resposta</a>
***


<a name="back0213">0213</a> – No PHP 5.3 e 5.5 não era possível fazer uma importação de função e constantes, veja abaixo como era
acessado por seu nome completo ou por um `alias`, no PHP 5.6 é possível fazer uma importação de função e constante ? demonstre um exemplo!

```php

    use Unicode\Tools as UT; // alias

    $charset = UT\CHARSET;
    UT\strlen("string");

    // ou totalmente qualificado
    $charset = \Unicode\Tools\CHARSET;

    \Unicode\Tools\strlen(
        "string"
    );

```

<a href="#0213">Resposta</a>
***




Respostas
---------

<a href="#back0200">voltar a pergunta</a><br/>
<a name="0200">0200</a> - **Resposta:** _É um forma de encapsular itens_

***


<a href="#back0201">voltar a pergunta</a><br/>
<a name="0201">0201</a> - **Resposta:** _`namespaces` são projetados para resolver dois problemas que os autores de bibliotecas 
e aplicativos enfrentam na hora de criar elementos de código reutilizáveis, como classes e funções.
 Colisões nos nomes das classes /funções/constantes internas ou de terceiros.
 Reduzir apelidos como (Extra_Long_Names), melhorando a legibilidade do código fonte.
 `namespaces` fornecem uma maneira para agrupar relacionadas classes, interfaces, funções e constantes._

***


<a href="#back0202">voltar a pergunta</a><br/>
<a name="0202">0202</a> - **Resposta:**

```php
namespace my\name;

class MyClass {}
const MYCONST = 1;

$a = new MyClass;
$b = new \my\name\MyClass;
$c = __NAMESPACE__ . '\MYCONST';

var_dump($a, $b, $c);
```

***


<a href="#back0203">voltar a pergunta</a><br/>
<a name="0203">0203</a> - **Resposta:** _Sim, nenhum código PHP pode existir fora dos suportes de namespace, exceto por uma 
instrução `declare()` então o código acima terá como retorno: 1_

***


<a href="#back0204">voltar a pergunta</a><br/>
<a name="0204">0204</a> - **Resposta:** _Sim, é possível declarar vários `namespaces` em um único arquivo, essa sintaxe não é
recomendado para a combinação de `namespaces` em único arquivo_

Retorno do código:

    2
    1

***


<a href="#back0205">voltar a pergunta</a><br/>
<a name="0205">0205</a> - **Resposta:** _Sim, O segundo exemplo é suportado, mas será gerado um erro nesse trecho de código, 
pois não é possível misturar declarações de `namespaces` suportados com declarações de `namespaces` sem colchetes_

***


<a href="#back0206">voltar a pergunta</a><br/>
<a name="0206">0206</a> - **Resposta:**

```php
namespace MyProject {
	const CONNECT_OK = 1;
	class Connection { 
		public function foo()
		{
			echo 'hello' . "\n";
		}
	}
	function connect() { /* ... */  }
}

namespace { // código global
	$a = MyProject\connect();
	$b = new MyProject\Connection();
	$b->foo();
	echo MyProject\CONNECT_OK . "\n";
}
```

***


<a href="#back0207">voltar a pergunta</a><br/>
<a name="0207">0207</a> - **Resposta:**

file.php
```php
namespace Foo\Bar\subnamespace;

const FOO = 1;
function foo() {}
class foo
{
    static function staticmethod() {}
}
```

basic.php
```php
namespace Foo\Bar;
include 'file.php';

const FOO = 2;
function foo() {}
class foo
{
    static function staticmethod() {}
}

// Nome não qualificado
foo(); // resolve a função Foo\Bar\foo
foo::staticmethod(); // resolve a classe Foo\Bar\foo, método staticmethod
echo FOO; // resolve a constante Foo\Bar\FOO
echo "\n";

// Nome qualificado
subnamespace\foo(); // resolve a função Foo\Bar\subnamespace\foo
subnamespace\foo::staticmethod(); // resolve a classe Foo\Bar\subnamespace\foo, método staticmethod
echo subnamespace\FOO; // resolve a constante Foo\Bar\subnamespace\FOO
echo "\n";

// Nome completo
\Foo\Bar\foo(); // resolve a função Foo\Bar\foo
\Foo\Bar\foo::staticmethod(); // resolve a classe Foo\Bar\foo, método staticmethod
echo \Foo\Bar\FOO; // resolve a constante Foo\Bar\FOO
echo "\n";
```

Retorno:

    2
    1
    2

***


<a href="#back0208">voltar a pergunta</a><br/>
<a name="0208">0208</a> - **Resposta:**

Retorno:

    classname::__construct file2.php 
    funcname file2.php 
    global
    namespacename\classname::__construct
    namespacename\funcname
    namespaced

***


<a href="#back0209">voltar a pergunta</a><br/>
<a name="0209">0209</a> - **Resposta:** `__NAMESPACE__` e a palavra-chave namespace

***


<a href="#back0210">voltar a pergunta</a><br/>
<a name="0210">0210</a> - **Resposta:** _aliasing um nome de uma classe, aliasing um nome de uma interface e aliasing um nome namespace_

***


<a href="#back0211">voltar a pergunta</a><br/>
<a name="0211">0211</a> - **Resposta:**

> 1.  Correto
>
> 2.  Correto, para usar sem o prefixo teria que se usar nome completo (totalmente qualificado): `\C\D\e();`
>
> 3.  Correto
>
> 4.  Correto
>     
> 5.  Falso, no ponto de que chamadas para nomes de classes não qualificadas ou qualificadas são resolvidas em tempo de 
      compilação, o correto seria execução.
>

***


<a href="#back0212">voltar a pergunta</a><br/>
<a name="0212">0212</a> - **Resposta:**

> 1.  Não, Namespaces não afetam o código existente de forma alguma, ou qualquer código que ainda venha a ser escrito que não 
>     contém namespaces. Você pode escrever:
>    
>     ```php
>        $a = new \stdClass;
>     
>        // Equivalente a:
>        $a = new stdClass;
>     ```
>
> 2.  Resposta
>
>     ```php
>        namespace foo;
>        $a = new \stdClass;
>        
>        function test(\ArrayObject $typehintexample = null) {}
>         
>        $a = \DirectoryIterator::CURRENT_AS_FILEINFO;
>        
>        // extendendo uma classe interna ou global
>        class MyException extends \Exception {}
>     ```
>
> 3.  Resposta
>
>     ```php
>     namespace foo;
>     
>     class MyClass {}
>     
>     // Usando uma classe do namespace atual como uma indução de tipo
>     function test(MyClass $typehintexample = null) {}
>     // Outra forma de usar uma classe do namespace atual como uma indução de tipo
>     function test(\foo\MyClass $typehintexample = null) {}
>     
>     // Extender uma classe do namespace atual
>     class Extended extends MyClass {}
>     
>     // Acessar uma função global
>     $a = \globalfunc();
>     
>     // Acessar uma constante global
>     $b = \INI_ALL;
>     ```
>
> 4.  Resposta
>    
>     ```php
>     namespace foo;
>     $a = new \my\name(); // instância a classe 'my\name'
>     echo \strlen('hi'); // chama a função 'strlen'
>     $a = \INI_ALL; // atribui a constante 'INI_ALL' a '$a'
>     ```
>
>
> 5.  Resposta
>
>     Nomes que contêm uma barra invertida, mas não começam com uma barra invertida como `my\name`  pode ser resolvido em duas 
>     maneiras diferentes.
>     Se não houver uma declaração de importação que aliases outro nome para `my`, então o pseudônimo de importação é aplicada 
>     ao `my` em `my\name`
>     Caso contrário, o nome do atual namespace é anexado a `my\name`
>
>     ```php
>     namespace foo;
>     use blah\blah as foo;
>
>     $a = new my\name(); // instânciando a classe 'foo\my\name'
>     foo\bar::name(); // chama o método estático 'name' na classe 'blah\blah\bar'
>     my\bar(); // chama a função 'foo\my\bar'
>     $a = my\BAR; // atribui a constante 'foo\my\BAR' a '$a'
>     ```
>
> 6.  Resposta
>
>     Os nomes das classes que não contêm uma barra invertida como o `name` pode ser resolvido em duas maneiras diferentes.
>     Se não houver uma declaração de importação que apelide outro nome a `name`, então o pseudônimo de importação é aplicada.
>     Caso contrário, o nome do atual namespace precederá `name`.
>
>     ```php
>     namespace foo;
>     use blah\blah as foo;
>     
>     $a = new name(); // Instância a classe 'foo\name'
>     foo::name(); // chama o método estático 'name' da classe 'blah\blah'
>     ```
>
> 7.  Resposta
>
>     Função ou nomes de constantes que não contêm uma barra invertida como o nome pode ser resolvido em duas maneiras diferentes.
>     Em primeiro lugar, o nome do namespace atual é prefixado para o nome.
>     Finalmente, se o nome da constante ou função não existir no namespace atual, uma constante ou uma função de nome global 
>     é usado se ela existir.
>
>     ```php
>     namespace foo;
>     use blah\blah as foo;
>    
>     const FOO = 1;
>    
>     function my() {}
>     function foo() {}
>     function sort(&$a)
>     {
>         \sort($a); // chamando uma função global 'sort'
>         $a = array_flip($a);
>         return $a;
>     }
>    
>     my(); // chamando 'foo\my'
>     $a = strlen('hi'); // chamando uma função global 'strlen' porque 'foo\strlen' não existe
>     $arr = array(1,3,2);
>     $b = sort($arr); // chamando função 'foo\sort'
>     $c = foo(); // chamando função 'foo\foo' – Importações não é aplicada
>     
>     $a = FOO; // Atribui a constante 'foo\FOO' a $a - Importações não é aplicada
>     $b = INI_ALL; // Atribui a constante global 'INI_ALL' a $a
>     ```
>
> 8.  Resposta
>
>     file1.php
>     ```php
>     namespace my\stuff;
>     class MyClass {}
>     ``` 
>     
>     another.php
>     ```php
>     namespace another;
>     class thing {}
>     ```
>
>     file1.php
>     ```php
>     namespace my\stuff;
>     include 'file1.php';
>     include 'another.php';
>     
>     use another\thing as MyClass;
>     $a = new MyClass; // instânciando classe "thing" do namespace another
>     ```
>
>     Não há conflito de nome, embora a classe `MyClass` exista dentro do  namespace `my\stuff`, porque a definição `MyClass` 
>     está em um arquivo separado. No entanto, o exemplo a seguir causa um erro fatal de conflito de nomes porque `MyClass` 
>     é definida no mesmo arquivo como a declaração `use`
>
>     ```php
>     namespace my\stuff;
>     use another\thing as MyClass;
>     class MyClass {} // fatal error: MyClass conflitos com declaração de importação
>     $a = new MyClass;
>     ```
>
> 9.  O exemplo demonstrado na pergunta poderia ser resolvido da seguinte maneira:
>     ```php
>     namespace my\stuff\nested {
>        class foo {}
>     }
>     ```
>
> 10. Resposta
>
>     Os únicos elementos que são afetadas por declarações de `use` são namespaces e nomes de classe. A fim de encurtar uma 
>     longa constante ou função, importar sua contendo namespace.
>     
>     ```php
>     namespace mine;
>     use ultra\long\ns\name;
>     
>     $a = name\CONSTANT;
>     name\func();
>     ```
>
> 11. Resposta
>
>     É muito importante perceber que, porque a barra invertida é usado como um caractere de escape dentro de strings, deve 
>     sempre ser dobrado quando usado dentro de uma string. Caso contrário, existe um risco de consequências não intencionais:
>
>     ```php
>     $a = 'dangerous\name'; // \n é uma nova linha dentro de strings entre aspas duplas!
>     $obj = new $a;
>      
>     $a = 'not\at\all\dangerous'; // Não há problema aqui
>     $obj = new $a;
>     ```
>
>     Dentro de um único citado, a seqüência de escape barra invertida é muito mais seguro de usar, mas ainda é uma prática 
>     recomendada para escapar barras invertidas em todas as cadeias de caracteres como uma das melhores práticas.
>
> 12. Resposta
>
>     Qualquer constante indefinida que é inqualificável como FOO produzirá um aviso explicando que o PHP assume FOO foi o 
>     valor da constante. Qualquer constante, qualificado ou totalmente qualificado, que contém uma barra invertida irá 
>     produzir um erro fatal se não for encontrado.
>
>     ```php
>     namespace bar;
>     $a = FOO; // produces notice - undefined constants "FOO" assumed "FOO";
>     $a = \FOO; // fatal error, undefined namespace constant FOO
>     $a = Bar\FOO; // fatal error, undefined namespace constant bar\Bar\FOO
>     $a = \Bar\FOO; // fatal error, undefined namespace constant Bar\FOO
>     ```
>
> 13. Resposta
>
>     Qualquer tentativa de definir uma constante namespaced que é um especial, será retornado um erro fatal
>
>     ```php
>     namespace bar;
>     const NULL = 0; // fatal error;
>     const true = 'stupid'; // also fatal error;
>     ```

***


<a href="#back0213">voltar a pergunta</a><br/>
<a name="0213">0213</a> - **Resposta:** _Com o PHP 5.6 sim, podemos importar funções e constantes, para importar funções é usado
`use function` e para constantes usa-se `use const`_

```php

    use const Unicode\Tools\CHARSET;
    use function Unicode\Tools\strlen;

    $charset = CHARSET; // acessando agora Unicode\Tools\CHARSET
    strlen($string);    // acessando agora Unicode\Tools\strlen(),
                        // e não a funcão global \strlen()

```

***