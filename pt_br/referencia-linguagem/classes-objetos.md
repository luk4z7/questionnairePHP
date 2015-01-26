[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | [Funções](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/funcoes.md) - **Classes e Objetos** - [Namespaces](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/namespaces.md)


Classes e Objetos
=================

Perguntas
---------

<a name="back0127">0127</a> – Como o PHP trata os objetos ?

<a href="#0127">Resposta</a>
***


<a name="back0128">0128</a> – O que é `$this` ?

<a href="#0128">Resposta</a>
***


<a name="back0129">0129</a> – É possível usar heredocs na atribuição de um membro de uma classe ?

<a href="#0129">Resposta</a>
***


<a name="back0130">0130</a> – Qual é o retorno do trecho de código abaixo:

```php
class A
{
    function foo()
    {
        if (isset($this)) {
            echo '$this está definida (';
            echo get_class($this);
            echo ")\n";
        } else {
            echo "\$this não está definida.\n";
        }
    }
}

A::foo();
```

<a href="#0130">Resposta</a>
***


<a name="back0131">0131</a> – Marque "correto"  ou "incorreto" a atribuição a os membros da classe abaixo:

```php
class simpleClass {
	// EX1:
	public $var8 = array(true, false);
	
	// EX2:
	public $var1 = 'olá '.'mundo';
	
	// EX3:
	public $var2 = <<<EOD
olá mundo
EOD;
	
	// Ex4:
	public $var3 = 1+2;
	
	// Ex5:
	public $var6 = myConstant; 
	
	// Ex6:
	public $var4 = self::myStaticMethod();
	
	// Ex7:
	public $var5 = $myVar;
	R: Incorreto
}
```

<a href="#0131">Resposta</a>
***


<a name="back0132">0132</a> – Analisando o código abaixo qual será o retorno de `$instance`, `$reference` e `$assigned`:

```php
class SimpleClass
{
	public $var = array(true, false);
}

$instance = new SimpleClass();
$assigned   =  $instance;
$reference  =& $instance;

$instance->var = '$assigned terá esse valor';
$instance = null;

var_dump($instance);
var_dump($reference);
var_dump($assigned);
```

<a href="#0132">Resposta</a>
***


<a name="back0133">0133</a> – Qual operador é usado para instânciar uma classe:

<a href="#0133">Resposta</a>
***


<a name="back0134">0134</a> – Quando atribuir uma instância já criada de um objeto a uma variável nova, a variável nova 
irá acessar a mesma instância do objeto ?

<a href="#0134">Resposta</a>
***


<a name="back0135">0135</a> – Como uma classe pode herdar métodos e membros de outra classe ?

<a href="#0135">Resposta</a>
***


<a name="back0136">0136</a> – No PHP é possível herdar múltiplas classes ?

<a href="#0136">Resposta</a>
***


<a name="back0137">0137</a> – É possível sobrescrever um método que a classe pai definiu um método como `final` ?

<a href="#0137">Resposta</a>
***


<a name="back0138">0138</a> – Para que serve o operador `::parent`:

<a href="#0138">Resposta</a>
***


<a name="back0139">0139</a> – Qual a finalidade e da palavra-chave `::class` ?

<a href="#0139">Resposta</a>
***


<a name="back0140">0140</a> – Porque quando criamos uma propriedade(campo, atributo) e inicializamos ela com um valor, 
porque esse valor tem que ser um valor constante ?

<a href="#0140">Resposta</a>
***


<a name="back0141">0141</a> – Se você declarar uma propriedade usando `var`, o PHP irá tratar a propriedade como se estivesse 
declarada como ? `public`, `protected`, `private` ? Porque ainda é mantido o `var` ?

<a href="#0141">Resposta</a>
***


<a name="back0142">0142</a> – Como podemos acessar uma propriedade dentro de um método de classe, onde a propriedade não é 
estática ? E também como podemos acessar uma estática ?

<a href="#0142">Resposta</a>
***


<a name="back0143">0143</a> – É possível atribuir um `nowdoc` a uma propriedade ?

<a href="#0143">Resposta</a>
***


<a name="back0144">0144</a> – Uma interface pode conter uma constante ?

<a href="#0144">Resposta</a>
***


<a name="back0145">0145</a> – Autoloading é disponível usando PHP em modo interativo CLI ?

<a href="#0145">Resposta</a>
***


<a name="back0146">0146</a> – Qual a maneira de chamar um construtor pai a partir de um construtor da classe filha ?

<a href="#0146">Resposta</a>
***


<a name="back0147">0147</a> – Para garantir compatibilidade reversa, se o PHP 5 não conseguir  achar uma `__construct()`
para uma determinada classe, ele procurará pela função construtora a moda-antiga, como seria esse método ?

<a href="#0147">Resposta</a>
***


<a name="back0148">0148</a> – Qual dos dois códigos gerará um erro, explique o motivo do erro:

Ex1:
```php
namespace Foo;
class Bar {
	public function Bar() {
        		echo "Bar \n";
    	}
}

class Foo extends Bar {
	public function __construct()
	{
		parent::__construct();
	}
}

$obj = new Foo();
```

Ex2:
```php
class Bar {
	public function Bar() {
        		echo "Bar \n";
    	}
}

class Foo extends Bar {
	public function __construct()
	{
		parent::__construct();
	}
}

$obj = new Foo();
```

<a href="#0148">Resposta</a>
***


<a name="back0149">0149</a> – A visibilidade de uma propriedade ou método pode ser definida prefixando a declaração com 
quais palavras-chaves ? defina cada uma!

<a href="#0149">Resposta</a>
***


<a name="back0150">0150</a> – Qual é saída do código abaixo, explique o motivo do retorno do código:

```php
abstract class base {
    public function inherited() {
        $this->overridden();
    }
    private function overridden() {
        echo 'base';
    }
}

class child extends base {
    private function overridden() {
        echo 'child';
    }
}

$test = new child();
$test->inherited();
```

<a href="#0150">Resposta</a>
***


<a name="back0151">0151</a> – Qual o significado de Paamayim Nekudotayim ?

<a href="#0151">Resposta</a>
***


<a name="back0152">0152</a> – É possível substituir `self` por `static`, qual o resultado do código abaixo ?

```php
class A {
    const C = 'constA';
    public function m() {
        echo static::C;
    }
} 

class B extends A {
    const C = 'constB';
}

$b = new B();
$b->m();
```

<a href="#0152">Resposta</a>
***


<a name="back0153">0153</a> – Caso um método abstrato é definido como `protected`, a implementação da classe deve ser 
definida ou como `protected` ou `public`, mas não `private`, esta afirmativa está correta ?

<a href="#0153">Resposta</a>
***


<a name="back0154">0154</a> – É possível uma classe implementar mais de uma interface ?

<a href="#0154">Resposta</a>
***


<a name="back0155">0155</a> – Interfaces podem ser extendidas como classes usando o operador `extends` ?

<a href="#0155">Resposta</a>
***


<a name="back0156">0156</a> – Uma interface pode ter métodos privados ou protegidos ?

<a href="#0156">Resposta</a>
***


<a name="back0157">0157</a> – Qual é nome do operador que é usado para implementar uma interface ?

<a href="#0157">Resposta</a>
***


<a name="back0158">0158</a> – Existe herança múltipla em interfaces ? Se sim, demonstre um exemplo.

<a href="#0158">Resposta</a>
***


<a name="back0159">0159</a> – É permitido sobrescrever constantes quando se usa-as em interfaces ?

<a href="#0159">Resposta</a>
***


<a name="back0160">0160</a> – O que são `traits` ?

<a href="#0160">Resposta</a>
***


<a name="back0161">0161</a> – Uma `trait` pode ser instânciada ?

<a href="#0161">Resposta</a>
***


<a name="back0162">0162</a> – Qual é o retorno dos exemplos de código abaixo:

EX1:
```php
class Base {
    public function sayHello() {
        echo 'Hello ';
    }
}

trait SayWorld {
    public function sayHello() {
        parent::sayHello();
        echo 'World!';
    }
}

class MyHelloWorld extends Base {
    use SayWorld;
}

$o = new MyHelloWorld();
$o->sayHello();
```

EX2:
```php
trait HelloWorld {
    public function sayHello() {
        echo 'Hello World!';
    }
}

class TheWorldIsNotEnough {
    use HelloWorld;
     public function sayHello() {
         echo 'Hello Universe!';
     }
}

$o = new TheWorldIsNotEnough();
$o->sayHello();
```

<a href="#0162">Resposta</a>
***


<a name="back0163">0163</a> – Para que serve o operador `insteadof` ?

<a href="#0163">Resposta</a>
***


<a name="back0164">0164</a> – No exemplo abaixo tempos duas `traits` com métodos com nomes iguais, gerando um `fatal error` 
como podemos resolver esse conflito ? demonstre-o em uso!

```php
trait A {
    public function smallTalk() {
        echo 'a';
    }
    public function bigTalk() {
        echo 'A';
    }
}

trait B {
    public function smallTalk() {
        echo 'b';
    }
    public function bigTalk() {
        echo 'B';
    }
}

class Talker {
    use A, B;
}

$talker = new Talker();
$talker->bigTalk();
```

<a href="#0164">Resposta</a>
***


<a name="back0165">0165</a> – É possível alterar/ajustar a visibilidade dos métodos em uma classes usando `traits`, 
demonstre um exemplo, use a `trait` abaixo mudando/ajustando a visibilidade do método `sayHello()`:

```php
trait HelloWorld {
	private function sayHello() {
        		echo 'Hello World!';
    	}
}
```

<a href="#0165">Resposta</a>
***


<a name="back0166">0166</a> – Demonstre o uso de `traits` e métodos estáticos.

<a href="#0166">Resposta</a>
***


<a name="back0167">0167</a> – Qual será o resultado do código abaixo:

```php
trait PropertiesTrait {
    public $x = 1;
}

class PropertiesExample {
    use PropertiesTrait;

    public $x = 10;
}

$example = new PropertiesExample;
echo $example->x;
```

<a href="#0167">Resposta</a>
***


<a name="back0168">0168</a> – Observando os códigos abaixo, qual é o resultado dos exemplos ?

EX1:
```php
class TestClass {
    public static $_bar;
}
class Foo1 extends TestClass { }
class Foo2 extends TestClass { }
Foo1::$_bar = 'Hello';
Foo2::$_bar = 'World';
echo Foo1::$_bar . ' ' . Foo2::$_bar;
```

EX2:
```php
trait TestTrait {
    public static $_bar;
}
class Foo11 {
    use TestTrait;
}
class Foo22 {
    use TestTrait;
}
Foo11::$_bar = 'Hello';
Foo22::$_bar = 'World';
echo Foo11::$_bar . ' ' . Foo22::$_bar;
```

EX3:
```php
trait sayWhere {
    public function whereAmI() {
        echo __CLASS__ . ' ';
    }
}

class Hello {
    use sayWHere;
}

class World {
    use sayWHere;
}

$a = new Hello;
$a->whereAmI();

$b = new World;
$b->whereAmI();
```

<a href="#0168">Resposta</a>
***


<a name="back0169">0169</a> – O que é sobrecarga em PHP ?

<a href="#0169">Resposta</a>
***


<a name="back0170">0170</a> – Um método sobrecarregado pode ser definido como `private`, `protected` ou `public` ?

<a href="#0170">Resposta</a>
***


<a name="back0171">0171</a> – Quais são os métodos mágicos que processam as sobrecargas no PHP ? defina cada um deles !

<a href="#0171">Resposta</a>
***


<a name="back0172">0172</a> – Observando o código abaixo, usando sobrecarga, o último exemplo gera um 
`Notice: (Undefined property via __get())` acessando o membro diretamente, somente que no exemplo acima acessando o método ele 
não gera o erro, explique o que acontece no código abaixo:

```php
class PropertyTest
{
    private $data = array();

    public $declared = 1;

    private $hidden = 2;

    public function __set($name, $value)
    {
        echo "Setting '$name' to '$value'\n";
        $this->data[$name] = $value;
    }

    public function __get($name)
    {
        echo "Getting '$name' ";
        if (array_key_exists($name, $this->data)) {
            return $this->data[$name];
        }

        $trace = debug_backtrace();
        trigger_error(
            'Undefined property via __get(): ' . $name . ' in ' . $trace[0]['file'] . "\n" .
            'on line ' . $trace[0]['line'],
            E_USER_NOTICE);
        return null;
    }
	
    public function __isset($name)
    {
        echo "Is '$name' set?\n";
        return isset($this->data[$name]);
    }

    public function __unset($name)
    {
        echo "Unsetting '$name'\n";
        unset($this->data[$name]);
    }

    public function getHidden()
    {
        return $this->hidden;
    }
}

$obj = new PropertyTest;
$obj->a = 1;
echo $obj->a . "\n";
var_dump(isset($obj->a));
echo “\n”;

echo $obj->declared . ' $obj->declared'." \n";
echo “\n”;

echo $obj->getHidden() . "\n";
echo $obj->hidden . "\n";
```

Retorno do código acima:

    Setting 'a' to '1'
    Getting 'a' 1
    Is 'a' set?
    bool(true)
    
    1 $obj->declared
    
    2
    
    Getting 'hidden'
    Notice: Undefined property via __get()

<a href="#0172">Resposta</a>
***


<a name="back0173">0173</a> – Defina `__call` e `__callStatic`

<a href="#0173">Resposta</a>
***


<a name="back0174">0174</a> – Sobrecarga de método, analisando a sintaxe de `__call` e `__callStatic`:

```php
public mixed __call ( string $name , array $arguments )

public static mixed __callStatic ( string $name , array $arguments )
```

Explique como funcionam os argumentos `$name` e `$arguments`, demonstre um exemplo com o uso de `__call` e `__callStatic`

<a href="#0174">Resposta</a>
***


<a name="back0175">0175</a> – Observando o código abaixo, como podemos iterar os membros da própria classe dentro do método  
`iterateVisible` ? No retorno do código qual será a diferença entre `$class->iterateVisible()` e o `foreach` do objeto `MyClass()`, 
explique o resultado:

```php
class MyClass
{
	public $var1 = 'value 1';
    	public $var2 = 'value 2';
    	public $var3 = 'value 3';

    	protected $protected = 'protected var';
    	private   $private   = 'private var';

    	function iterateVisible() {
       
    	}
}

$class = new MyClass();

foreach($class as $key => $value) {
	print "$key => $value\n";
}
echo "\n";

$class->iterateVisible();
```

<a href="#0175">Resposta</a>
***


<a name="back0176">0176</a> – O que define o padrão de projeto Factory, explique um pouco como ele funciona e demonstre 
algum exemplo de sua ultilização:

<a href="#0176">Resposta</a>
***


<a name="back0177">0177</a> – O que define o padrão de projeto Singleton, explique um pouco como ele funciona e 
demonstre algum exemplo de sua utilização:

<a href="#0177">Resposta</a>
***


<a name="back0178">0178</a> – Descreva os nomes dos métodos mágicos existentes no PHP:

<a href="#0178">Resposta</a>
***


<a name="back0179">0179</a> – Como são chamadas as funções que o PHP reserva que começam com `__ ?

<a href="#0179">Resposta</a>
***


<a name="back0180">0180</a> – Analisando o seguinte código ele gerará um erro, qual o motivo do erro observando o 
código seguinte:

```php
class A
{
  private $a;
 
  public function __construct()
  {
    $this->a = 1;
  }
}

class B extends A
{
  protected $b;
  protected $c;
 
  public function __construct()
  {
    parent::__construct();
    $this->b = 2;
  }
 
  function __sleep()
  {
    return array('b', 'c', 'a');
  }
}

serialize(new B);
var_dump(serialize(new B));
```

    ERRO:
    Notice: serialize(): "a" returned as member variable from __sleep() but does not exist in

<a href="#0180">Resposta</a>
***


<a name="back0181">0181</a> – Quando que `__wakeup()` é executado e qual a finalidade desse método mágico no PHP ?

<a href="#0181">Resposta</a>
***


<a name="back0182">0182</a> – Analisando o exemplo abaixo teremos um erro tipo `E_RECOVERABLE_ERROR`, como podemos 
resolver esse problema usando um método mágico, qual seria esse método ?

```php
class TestClass
{
    public $foo;

    public function __construct($foo)
    {
        $this->foo = $foo;
    }
}

$class = new TestClass('Hello');
echo $class;
```

<a href="#0182">Resposta</a>
***


<a name="back0183">0183</a> – O métogo mágico `__invoke()` está disponivel desde quando no PHP ?

<a href="#0183">Resposta</a>
***


<a name="back0184">0184</a> – Qual a finalidade do método mágico `__invoke()` ?

<a href="#0184">Resposta</a>
***


<a name="back0185">0185</a> – A palavra `final` foi introduzido em qual versão do PHP e qual sua finalidade ?

<a href="#0185">Resposta</a>
***


<a name="back0186">0186</a> – O exemplo abaixo gerará um fatal erro, agora qual o motivo do erro nesta operação de herança:

```php
class ClasseBase {
   public function teste() {
       echo "ClasseBase::teste() chamado\n";
   }
   
   final public function maisTeste() {
       echo "ClasseBase::maisTeste() chamado\n";
   }
}

class ClasseFilha extends ClasseBase {
   public function maisTeste() {
       echo "ClasseFilha::maisTeste() called\n";
   }
}
```

<a href="#0186">Resposta</a>
***


<a name="back0187">0187</a> – Propriedades podem ser definidas como `final` ?

<a href="#0187">Resposta</a>
***


<a name="back0188">0188</a> – Observando o exemplo de código abaixo qual será o resultado, explique:

```php
class Foo
{
    var $that;

	function __clone()
	{
	    $this->that = clone $this->that;
	}
}

$a = new Foo;

$a->that = $a;
print_r($a->that);

$b = clone $a;
var_dump($b);
```

<a href="#0188">Resposta</a>
***


<a name="back0189">0189</a> – Qual o retorno do código abaixo na saída do `echo`:

```php
class Bar{
	public $var;
	function __construct() { $this->var = 'aaa'; }
}
 
$a = new Bar;
$b = clone $a;
$b->var = 'bbb';

echo($a->var);
echo "\n";
echo($b->var);
echo "\n\n";

$c = new Bar;
$d = $c;
$d->var = 'bbb';

echo($c->var);
echo "\n";
echo($d->var);
```

<a href="#0189">Resposta</a>
***


<a name="back0190">0190</a> – Quando há existência de dois objetos, quando que os dois vão ser comparados como idênticos, 
quais os requisitos ?

<a href="#0190">Resposta</a>
***


<a name="back0191">0191</a> – O que é indução de tipos ?

<a href="#0191">Resposta</a>
***


<a name="back0192">0192</a> – Observando o código abaixo nos será retornado um erro `(Catchable fatal error:)`, 
refatore o código para não gerar o erro e explique qual o motivo do erro:

```php
class MinhaClasse
{
    public function teste(OutraClasse $outraclasse) {
        echo $outraclasse->var;
    }
}

class OutraClasse {
    public $var = 'Alô Mundo';
}

$minhaclasse = new MinhaClasse;

$foo = new stdClass;
$minhaclasse->teste($foo);
```

<a href="#0192">Resposta</a>
***


<a name="back0193">0193</a> – A indução de tipos funciona com quais tipo de dados ?

<a href="#0193">Resposta</a>
***


<a name="back0194">0194</a> – Em qual versão do PHP foi implementado o `late static bindings` e o que seria esse termo ?

<a href="#0194">Resposta</a>
***


<a name="back0195">0195</a> – Qual o retorno de `B::test()` nos dois exemplos abaixo, explique o motivo dos retornos:

EX1:
```php
class A {
    public static function who() {
        echo __CLASS__;
    }
    public static function test() {
        static::who(); // Aqui vem Late Static Bindings 
    }  
}  

class B extends A {      
    public static function who() {
         echo __CLASS__;
    }  
}   

B::test();
```

EX2:
```php
class A {
    public static function who() {
        echo __CLASS__;
    }
    public static function test() {
        self::who();      
    }  
}  

class B extends A {      
    public static function who() {
         echo __CLASS__;
    }  
}   

B::test();
```

<a href="#0195">Resposta</a>
***


<a name="back0196">0196</a> – Observando o código abaixo qual será o resultado tendo em mente que chamadas estáticas usando 
palavras-chave como `parent::` ou `self::` somente encaminhão a informação:

```php
class A {
    public static function foo() {
        static::who();
    }
        
    public static function who() {
        echo __CLASS__."\n";
    }
}

class B extends A {
    public static function test() {
        A::foo();
        parent::foo();
        self::foo();
    }

    public static function who() {
        echo __CLASS__."\n";
    }
}

class C extends B {
    public static function who() {
        echo __CLASS__."\n";
    }
}

C::test();
```

<a href="#0196">Resposta</a>
***


<a name="back0197">0197</a> – Objetos são passados por referências por padrão ? Explique como funciona esse processo! 
Se essa afirmativa é completamente verdadeira;

<a href="#0197">Resposta</a>
***


<a name="back0198">0198</a> – `session_register` foi removido em qual versão do PHP ?

<a href="#0198">Resposta</a>
***


<a name="back0199">0199</a> – OOP Changelog, defina as versões e que cada `feature foi implementada:

> 1.  Versão que foi adicionado traits
>
> 2.  Métodos como o mesmo nome que o último elemento de um nome de classe namespaced deixarão de ser tratados como construtor, 
      Esta alteração não afeta as classes não namespaced.
>
> 3.  As classes que implementam interfaces com métodos que têm valores padrão no protótipo não 	são mais necessários para 
      coincidir com o valor padrão da interface.
>
> 4.  Agora é possível referênciar a classe usando uma variável (por exemplo: `echo $classname::constante`). O valor da variável 
      não pode ser uma palavra-chave (por exemplo: `self, parent ou static`).
>
> 5.  Um `E_WARNING` é emitido se um método mágico de sobrecarrega são declarados estáticos. Ele também reforça a exigência de 
      visibilidade pública.
>
> 6.  Exceções lançadas na função `__autoload()` não poderiam ser pegas no bloco `catch`, e 	resultariam em um erro fatal. 
      Exceções agora jogadas na função `__autoload()` podem ser capturadas no bloco `catch`, com um provison. Se jogar uma exceção 
      personalizada, então a classe de exceção personalizada deve estar disponível. A função `__autoload()` pode ser usada de 
      forma recursiva para alimentação automática da classe de exceção personalizada.
> 
> 7.  Adicionado método `__callStatic()`
>
> 8.  Adicionado `heredocs` e apoio `nowdoc` para definições `const`
>
> 9.  Adicionado `Late Static Bindings`
>
> 10. Adicionado método `__invoke()`
>
> 11. O método `__toString()` só era chamado quando diretamente combinado com `echo ou print`. Mas agora, ele é chamado no 
      contexto de string ( ex: `printf()` com modificador %s), mas não em outros contextos tipo: (ex: com modificador %d). 
      Desde o PHP *.*.0, convertendo objetos sem um método `__toString` emitia um erro de nível `E_RECOVERABLE_ERROR`.
>
> 12. Nas versões anteriores do PHP 5, o uso de `var` foi considerado obsoleto e emitiria um erro nível `E_STRICT`. Não é mais 
      obsoleto, pois não emite o erro.
>
> 13. O método estático `__set_state()` é agora chamado para classes exportadas por `var_export()`
>
> 14. Adicionado métodos `__isset()` e `__unset()`

<a href="#0199">Resposta</a>
***



Respostas
---------

<a href="#back0127">voltar a pergunta</a><br/>
<a name="0127">0127</a> - **Resposta:** _O PHP trata objetos da mesma maneira que referências ou manipuladores, significando que 
cada variável contém uma referência a um objeto ao invés de uma cópia de todo o objeto._

***


<a href="#back0128">voltar a pergunta</a><br/>
<a name="0128">0128</a> - **Resposta:** _$this é uma referência para o objeto chamador do método (normalmente o objeto ao qual o 
método pertence, mas pode ser outro objeto, se o método é chamado estaticamente no contexto de um objeto secundário)_

```php
class A
{
    function foo()
    {
        if (isset($this)) {
            echo '$this está definida (';
            echo get_class($this);
            echo ")\n";
        } else {
            echo "\$this não está definida.\n";
        }
    }
}

class B
{
    function bar()
    {
        A::foo();
    }
}

$a = new A();
$a->foo();
A::foo();
$b = new B();
$b->bar();
B::bar();
```

Impressão do exemplo assima:

    $this está definida (A)
    $this não está definida.
    $this está definida (B)
    $this não está definida.

***


<a href="#back0129">voltar a pergunta</a><br/>
<a name="0129">0129</a> - **Resposta:** _Declaração inválida, somente nowdocs podem ser usados no contexto de dado estático, 
na atribuição ao um membro de uma classe, apartir do PHP 5.3.0_

***


<a href="#back0130">voltar a pergunta</a><br/>
<a name="0130">0130</a> - **Resposta:** _$this não está definida_

***


<a href="#back0131">voltar a pergunta</a><br/>
<a name="0131">0131</a> -

Ex1 - **Resposta:** Correto<br/>
Ex2 - **Resposta:** Incorreto<br/>
Ex3 - **Resposta:** Incorreto<br/>
Ex4 - **Resposta:** Incorreto<br/>
Ex5 - **Resposta:** Correto<br/>
Ex6 - **Resposta:** Incorreto<br/>
Ex7 - **Resposta:** Incorreto<br/>

***


<a href="#back0132">voltar a pergunta</a><br/>
<a name="0132">0132</a> - **Resposta:**

    NULL
    NULL
    object(SimpleClass)#1 (1) {
      ["var"]=>
      string(26) "$assigned terá esse valor"
    }
    
`$assigned` não tem valor `null`, sendo somente `$reference` uma referência a `$instance`, ou seja no PHP um alias.
Quando atribuir uma instância de um objeto a uma variável nova, a variável nova irá acessar a mesma instância do objeto que 
foi atribuido, a partir do PHP5, uma variável objeto não contém mais o próprio objeto valor. Ela contém um identificador do 
objeto que permite que os acessadores do objeto encontrem o objeto real. Quando um objeto é enviado por argumento. Retornado 
ou atribuido para outra variável, as variáveis diferentes não são aliases: elas armazenam uma cópia do identificador, 
que aponta para o mesmo objeto.

***


<a href="#back0133">voltar a pergunta</a><br/>
<a name="0133">0133</a> - **Resposta:** _Para criar uma instância é usado o operador `new`_

```php
$test = new myClass();
```

***


<a href="#back0134">voltar a pergunta</a><br/>
<a name="0134">0134</a> - **Resposta:** _Sim, criando um identificador apontando para o mesma instância_

***


<a href="#back0135">voltar a pergunta</a><br/>
<a name="0135">0135</a> - **Resposta:** _Uma classe pode herdar métodos e membros de outra classe usando a palavra-chave 
`extends` na sua declaração_

***


<a href="#back0136">voltar a pergunta</a><br/>
<a name="0136">0136</a> - **Resposta:** _O PHP não possui herança múltipla, uma classe só pode herdar uma classe base_

***


<a href="#back0137">voltar a pergunta</a><br/>
<a name="0137">0137</a> - **Resposta:** _Os métodos e membros herdados podem ser sobrescritos, a não ser que a classe pai 
definiu um método como `final`_

***


<a href="#back0138">voltar a pergunta</a><br/>
<a name="0138">0138</a> - **Resposta:** _Operador para acessar os métodos ou membros da classe pai_

***


<a href="#back0139">voltar a pergunta</a><br/>
<a name="0139">0139</a> - **Resposta:** _Obter o nome completo da classe, inclusive o namespace, desde o PHP 5.5._

```php
namespace NS {
    class ClassName {
    }
    
    echo ClassName::class;
    echo "\n";
}
```

Retorno:

    NS\ClassName

***


<a href="#back0140">voltar a pergunta</a><br/>
<a name="0140">0140</a> - **Resposta:** _Pois tem que ser um valor que possa ser avaliado em tempo de compilação e não deve 
depender de informações de tempo de execução, a fim de ser avaliada_

***


<a href="#back0141">voltar a pergunta</a><br/>
<a name="0141">0141</a> - **Resposta:** _Será tratado como `public` quando é usado o `var`, afim de manter 
compatibilidade com PHP 4 e PHP 5, ainda é aceito o uso da palavra-chave `var` em declarações de propriedades_

***


<a href="#back0142">voltar a pergunta</a><br/>
<a name="0142">0142</a> - **Resposta:**

não estáticos

    ($this->property)
    
estático

    (self::property)

***


<a href="#back0143">voltar a pergunta</a><br/>
<a name="0143">0143</a> - **Resposta:** _Sim, a partir do PHP 5.3.0 pode se atribuir `nowdocs` a propriedades_

***


<a href="#back0144">voltar a pergunta</a><br/>
<a name="0144">0144</a> - **Resposta:** _Sim, é possível também uma interface terem constantes_

***


<a href="#back0145">voltar a pergunta</a><br/>
<a name="0145">0145</a> - **Resposta:** _Não, autoloading não é disponível usando PHP em modo interativo CLI_

***


<a href="#back0146">voltar a pergunta</a><br/>
<a name="0146">0146</a> - **Resposta:** _Construtores pais não são chamados implicitamente se a classe filha define um 
construtor. Para executar o construtor da classe pai, uma chamada a `parent::__construct()` dentro do construtor da classe 
filha é necessária_

***


<a href="#back0147">voltar a pergunta</a><br/>
<a name="0147">0147</a> - **Resposta:** _Ele procurar por um método que tenha o mesmo nome da classe_

***


<a href="#back0148">voltar a pergunta</a><br/>
<a name="0148">0148</a> - **Resposta:** _Exemplo 1 vai gerar um erro, pois a partir do PHP 5.3.3, métodos com o mesmo nome 
como último elemento de uma classe dentro de namespace não será mais tratado como construtor, lembrando que essa mundaça não 
afeta classes fora de namespace_

***


<a href="#back0149">voltar a pergunta</a><br/>
<a name="0149">0149</a> - **Resposta:** _`public` (pode ser acessado dentro de fora da classe), `private` 
(visibilidade somente dentro da própria classe que o define), `protected` (visibilidade dentro da própria classe que o define
e nas classes filhas)_

***


<a href="#back0150">voltar a pergunta</a><br/>
<a name="0150">0150</a> - **Resposta:** _retorno: `base`, Isso acontece pois métodos privados são visiveis apenas para 
classe que o define, a classe filha não vê métodos privados do pai, se os filhos não podem ver métodos privados dos pais não 
pode se substituir-los_

***


<a href="#back0151">voltar a pergunta</a><br/>
<a name="0151">0151</a> - **Resposta:** _Paamayim Nekudotayim é hebraico é significa `double colon`, as palavras foram 
utilizadas pelos dois desenvolvedores israelenses originais de PHP, Andi Gutmans e Zeev Suraski, para o operador de resolução 
de escopo `::`, é um token que permite acesso a métodos ou membros estáticos, constantes e sobrecarregados de uma classe_

***


<a href="#back0152">voltar a pergunta</a><br/>
<a name="0152">0152</a> - **Resposta:** _Retorno será `constB`, A partir do PHP 5.3.0 você pode usar `static`, nesse caso 
`static` nós retornará o valor da constante C `constB`, usando o `self` nos traria `constA` pois `self::` somente nos retorna 
o valor_

***


<a href="#back0153">voltar a pergunta</a><br/>
<a name="0153">0153</a> - **Resposta:** _Sim, está correto, os métodos devem ser definidos com a mesma (ou menos restrita) visibilidade_

***


<a href="#back0154">voltar a pergunta</a><br/>
<a name="0154">0154</a> - **Resposta:** _Sim, classes podem implementar mais de uma interface, separando cada interface com uma virgula_

***


<a href="#back0155">voltar a pergunta</a><br/>
<a name="0155">0155</a> - **Resposta:** _Sim, uma interface pode extender de outra interface_

***


<a href="#back0156">voltar a pergunta</a><br/>
<a name="0156">0156</a> - **Resposta:** _Não, todos os métodos declarados em uma interface devem ser `public`, essa é a 
natureza de uma interface_

***


<a href="#back0157">voltar a pergunta</a><br/>
<a name="0157">0157</a> - **Resposta:** _Para implementar uma interface, o operador `implements` é usado_

***


<a href="#back0158">voltar a pergunta</a><br/>
<a name="0158">0158</a> - **Resposta:** _Sim_

```php
interface a
{
	public function foo();
}

interface b
{
	public function bar();
}

interface c extends a, b
{
	public function baz();
}

class d implements c
{
	public function foo() {
    	}

    	public function bar() {
    	}

    	public function baz() {
    	}
}
```

***


<a href="#back0159">voltar a pergunta</a><br/>
<a name="0159">0159</a> - **Resposta:** _Não é permitido sobreescrever constantes, segue o mesmo conceito como constantes 
de classes_

***


<a href="#back0160">voltar a pergunta</a><br/>
<a name="0160">0160</a> - **Resposta:** _São um mecanismo para reutilização de código em linguagens de herança simples, 
como PHP, traits são destinadas a reduzir algumas limitações de herança simples, permitindo reutilizar conjuntos de métodos 
livremente em várias classes independentemente que vivem em diferentes hierarquias de classes_

***


<a href="#back0161">voltar a pergunta</a><br/>
<a name="0161">0161</a> - **Resposta:** _Não é possível instanciar uma trait por conta própria._

***


<a href="#back0162">voltar a pergunta</a><br/>
<a name="0162">0162</a> - **Resposta:** 

EX1: 

    Hello World
    
EX2: 

    Hello Universe!
                                         
O segundo exemplo não é retornado igualmente ao primeiro pois a ordem de precedência é que o método da classe atual substitua 
o método da trait

***


<a href="#back0163">voltar a pergunta</a><br/>
<a name="0163">0163</a> - **Resposta:** _Para resolver conflitos de nomes entre as caracteristicas utilizadas na mesma classe, 
o operador `insteadof` é usado para escolher exatamente um dos métodos conflitantes_

***


<a href="#back0164">voltar a pergunta</a><br/>
<a name="0164">0164</a> - **Resposta:** _Na `class Talker` resumiriamos da seguinte maneira:_

```php
class Talker {
	use A, B {
		B::smallTalk insteadof A;
		A::bigTalk insteadof B;	
	}
}
```

***


<a href="#back0165">voltar a pergunta</a><br/>
<a name="0165">0165</a> - **Resposta:**

```php
class myClass {
	use HelloWorld { sayHello as public; }
}
```

***


<a href="#back0166">voltar a pergunta</a><br/>
<a name="0166">0166</a> - **Resposta:**

```php
trait StaticExample {
	public static function doSomething() {
        		echo 'Doing something';
    	}
}

class Example {
	use StaticExample;
}

Example::doSomething();
```

***


<a href="#back0167">voltar a pergunta</a><br/>
<a name="0167">0167</a> - **Resposta:** _Será retornado um erro de incopatibilidade, quando uma `trait` define uma 
propriedade, então uma classe não pode definir uma propriedade com o mesmo nome, caso contrário, um erro será emitido, 
É um `E_STRICT se a definição de classe é compativel (mesma visibilidade e valor inicial) ou erro fatal do contrário_

***


<a href="#back0168">voltar a pergunta</a><br/>
<a name="0168">0168</a> - **Resposta:**

EX1:

    World World
    
EX2:

    Hello World
    
Ao contrário de herança se uma `trait` tem propriedades estáticas, cada classe usando essa `trait` tem instâncias 
independentes dessas propriedades. 


EX3:

    Hello World
    
vale apena notar que o `__CLASS__` constante mágica se torna ainda mais mágico, irá retornar o nome da classe em que a 
`trait` está sendo usada.

***


<a href="#back0169">voltar a pergunta</a><br/>
<a name="0169">0169</a> - **Resposta:** _Sobrecarga em PHP provê recursos para 'criar' dinamicamente membros e métodos. 
Estas entidades dinâmicas são processadas via métodos mágicos que podem estabelecer em uma classe para vários tipos de ações_

***


<a href="#back0170">voltar a pergunta</a><br/>
<a name="0170">0170</a> - **Resposta:** _Incorreto, Todos os métodos sobrecarregados devem ser definidos como públicos_

***


<a href="#back0171">voltar a pergunta</a><br/>
<a name="0171">0171</a> - **Resposta:**

É executado ao se escrever dados para membros inacessíveis 
```php
__set ( string $name , mixed $value ) 
```
OBS: O argumento `$name` é o nome do membro com o qual se está interagindo. O argumento `$value` do método `__set()` 
especifica o valor para o qual o membro `$name` deveria ser setado


É utilizado para ler dados de membros inacessíveis 
```php
__get ( string $name )
```
   
É disparado para chamar `isset()` ou `empty()` em membros inacessíveis
```php
__isset ( string $name )
```

É invocado quando `unset() é usado em membros inacessíveis
```php
__unset ( string $name )
```

É disparado quando invocado métodos inacessíveis em um contexto de objeto
```php
__call ( string $name , array $arguments )
```

É disparado quando invocado métodos inacessíveis em um contexto estático
```php
__callStatic ( string $name , array $arguments )
```
OBS: O argumento `$arguments` é um array enumerado contendo os parâmetros passados para o método `$name`.

***


<a href="#back0172">voltar a pergunta</a><br/>
<a name="0172">0172</a> - **Resposta:** _Esse erro é obtido por causa do membro ter visibilidade `private` não sendo visivel 
fora da classe, para que `__get()` é usado. Gerando assim um erro_

***


<a href="#back0173">voltar a pergunta</a><br/>
<a name="0173">0173</a> - **Resposta:**

É disparado quando invocado métodos inacessíveis em um contexto de objeto
```php
__call ( string $name , array $arguments )
```   
    
É disparado quando invocado métodos inacessíveis em um contexto estático
```php
__callStatic ( string $name , array $arguments )
```
OBS: O argumento `$arguments` é um array enumerado contendo os parâmetros passados para o método `$name`.

***


<a href="#back0174">voltar a pergunta</a><br/>
<a name="0174">0174</a> - **Resposta:** _O argumento `$name` é o nome do método sendo chamado. O argumento `$arguments` é um 
`array` enumerado contendo os parâmetros passados para o método `$name`_

```php
class MethodTest
{
	public function __call($name, $arguments)
    	{
        		echo "Calling object method '$name' "
             		. implode(', ', $arguments). "\n";
    	}

    	public static function __callStatic($name, $arguments)
    	{
        		echo "Calling static method '$name' "
             		. implode(', ', $arguments). "\n";
    	}
}

$obj = new MethodTest;
$obj->runTest('in object context');
MethodTest::runTest('in static context');
```

Retorno:

    Calling object method 'runTest' in object context
    Calling static method 'runTest' in static context

***


<a href="#back0175">voltar a pergunta</a><br/>
<a name="0175">0175</a> - **Resposta:** 

```php
class MyClass
{
    public $var1 = 'value 1';
        public $var2 = 'value 2';
        public $var3 = 'value 3';

        protected $protected = 'protected var';
        private   $private   = 'private var';

        function iterateVisible() {
            echo "iterateVisible\n";
            foreach ($this as $key => $value) {
            print "$key => $value \n";
        }
        }
}

$class = new MyClass();

foreach($class as $key => $value) {
    print "$key => $value\n";
}
echo "\n";

$class->iterateVisible();
```

Retorno:

    var1 => value 1
    var2 => value 2
    var3 => value 3
    
    iterateVisible
    var1 => value 1 
    var2 => value 2 
    var3 => value 3 
    protected => protected var 
    private => private var
    
OBS: Por padrão todas as propriedades visíveis serão usadas para a iteração, na saída o `foreach` iterou por cada uma 
das variáveis visíveis que podem ser acessadas, diferente do foreach fora da classe que somente tem acesso as propriedades públicas.


***


<a href="#back0176">voltar a pergunta</a><br/>
<a name="0176">0176</a> - **Resposta:** _O padrão Factory permite a instanciação de objetos em tempo de execução. 
É chamado de Factory uma vez que é responsável por "produzir" um objeto. O Factory parametrizado recebe como argumento o 
nome da classe para instanciar. _

```php
class Exemplo
{
    // Método Factory parametrizado
    public static function factory($type)
    {
        if (include_once 'Drivers/' . $type . '.php') {
            $classname = 'Driver_' . $type;
            return new $classname;
        } else {
            throw new Exception ('Driver não encontrado');
        }
    }
}

// Carregar um driver MySQL
$mysql = Exemplo::factory('MySQL');

// Carregar um driver SQLite 
$sqlite = Exemplo::factory('SQLite');
```

***


<a href="#back0177">voltar a pergunta</a><br/>
<a name="0177">0177</a> - **Resposta:** _O padrão Singleton se aplica em situações em que é preciso haver uma só instância de 
uma classe. O exemplo mais comum é uma conexão com um banco de dados. Implementar esse padrão permite ao programador fazer 
essa instância única ser facilmente acessível por muitos outros objetos_

```php
class Exemplo
{
    // Guarda uma instância da classe
    private static $instance;
    
    // Um construtor privado; previne a criação direta do objeto
    private function __construct() 
    {
        echo 'Sou um construtor';
    }

    // O método singleton 
    public static function singleton()
    {
        if (!isset(self::$instance)) {
            $c = __CLASS__;
            self::$instance = new $c;
        }

        return self::$instance;
    }
    
    // Método exemplo
    public function latir()
    {
        echo 'Au!';
    }

    // Previne que o usuário clone a instância
    public function __clone()
    {
        trigger_error('Clone is not allowed.', E_USER_ERROR);
    }

}

// Isso falharia porque o construtor é privado
$test = new Exemplo;

// Isso sempre vai recuperar uma instância da classe
$test = Exemplo::singleton();
$test->latir();

// Isso irá emitir um E_USER_ERROR.
$test_clone = clone $test;
```

***


<a href="#back0178">voltar a pergunta</a><br/>
<a name="0178">0178</a> - **Resposta:** _Os nomes de funções `__construct`, `__destruct`, `__call`, `__callStatic`, 
`__get`, `__set`, `__isset`, `__unset`, `__sleep`, `__wakeup`, `__toString`, `__invoke`, `__set_state` and `__clone` são 
mágicos nas classes do PHP. Você não pode ter funções com esses nomes em nenhuma de suas classes a não ser que queira que a 
funcionalidade mágica associada com eles_

***


<a href="#back0179">voltar a pergunta</a><br/>
<a name="0179">0179</a> - **Resposta:** _PHP reserva todas as funções com nomes começando com `__` como mágicas_

***


<a href="#back0180">voltar a pergunta</a><br/>
<a name="0180">0180</a> - **Resposta:** _É importante notar sobre `__sleep()` e a variável de membro privada `a`, a 
serialização é executada a partir do escopo da visibilidade da subclasse, em uma determinada hierarquia de classes em 
que as classes pai podem conter variáveis de membro privadas, essas variáveis são serializadas quando `__sleep()` não está 
definido. No entanto, umas vez que `__sleep()` é definido, não há nenhuma maneira de fazer essas variáveis de membro privadas 
serem serializadas também_

***


<a href="#back0181">voltar a pergunta</a><br/>
<a name="0181">0181</a> - **Resposta:** _O intuito do método `__wakeup()` é reestabelecer qualquer conexão com banco de dados 
que podem ter sido perdidas durante a serialização e realizar tarefas de reinicialização. _

```php
class Connection
{
 	protected $link;
    	private $server, $username, $password, $db;
    	
	public function __construct($server, $username, $password, $db)
    	{
        		$this->server = $server;
        		$this->username = $username;
        		$this->password = $password;
        		$this->db = $db;
        		$this->connect();
    	}
    
    	private function connect()
    	{
        		$this->link = mysql_connect($this->server, $this->username, $this->password);
        		mysql_select_db($this->db, $this->link);
    	}
    
    	public function __sleep()
    	{
        		return array('server', 'username', 'password', 'db');
    	}
    
    	public function __wakeup()
    	{
        		$this->connect();
    	}
}

$connection = new Connection('localhost', 'root', '12345', 'mybase');

$teste = serialize($connection);
var_dump($teste);

$teste = unserialize($teste);
var_dump($teste);
```

***


<a href="#back0182">voltar a pergunta</a><br/>
<a name="0182">0182</a> - **Resposta:** 

```php
class TestClass
{
    public $foo;

    public function __construct($foo)
    {
        $this->foo = $foo;
    }

    public function __toString()
    {
        return $this->foo;
    }
}

$class = new TestClass('Hello');
echo $class;
```

Retorno:

    Hello

OBS: O método `__toString()` permite que uma classe decida como se comportar quando for convertida para uma string.
Vale lembrar que antes do PHP 5.2.0 o método `__toString()` só era chamado quando diretamente combinado com `echo` ou `print`. 
Desde o PHP 5.2.0, ele é chamado no contexto de string (ex: em printf() com modificador %s) mas não em outros tipos de 
contextos (ex: com modificadores %d). Desde o PHP 5.2.0, convertendo objetos sem o método `__toString()` para string 
causa `E_RECOVERABLE_ERROR`

***


<a href="#back0183">voltar a pergunta</a><br/>
<a name="0183">0183</a> - **Resposta:** _Disponível desde o PHP 5.3.0_

***


<a href="#back0184">voltar a pergunta</a><br/>
<a name="0184">0184</a> - **Resposta:** _O método `__invoke()` é chamado quando um script tenta chamar um objeto como uma 
função_

```php
class CallableClass
{
	public function __invoke($x)
    	{
        		var_dump($x);
    	}
}
$obj = new CallableClass;
$obj(5);
var_dump(is_callable($obj));
```

Retorno:

    int(5)
    bool(true)

***


<a href="#back0185">voltar a pergunta</a><br/>
<a name="0185">0185</a> - **Resposta:** _PHP 5 introduz a palavra-chave `final`, que previne que classes filhas 
sobrecarreguem um método. Basta prefixar a definição com `final`_

***


<a href="#back0186">voltar a pergunta</a><br/>
<a name="0186">0186</a> - **Resposta:** _Resulta em erro Fatal: Não pode sobrescrever método final `ClasseBase::maisTeste()`_

***


<a href="#back0187">voltar a pergunta</a><br/>
<a name="0187">0187</a> - **Resposta:** _Propriedades não podem ser definidas como `final`, apenas classes e métodos 
podem ser declarados como `final`_

***


<a href="#back0188">voltar a pergunta</a><br/>
<a name="0188">0188</a> - **Resposta:** _Será encadeado uma recursividade, `clone` será executado até gerar um fatal error:
`Maximum function nesting level of '100' reached, aborting`_

    Foo Object
    (
        [that] => Foo Object
        *RECURSION*
    )

***


<a href="#back0189">voltar a pergunta</a><br/>
<a name="0189">0189</a> - **Resposta:** _Esse exemplo mostra o simples conceito do `clone`, quando um objeto é clonado,
PHP 5 fará uma cópia superficial de todas as propriedades do objeto_

Retorno:

    aaa
    bbb
    
    bbb
    bbb

***


<a href="#back0190">voltar a pergunta</a><br/>
<a name="0190">0190</a> - **Resposta:** _Quando usar o operador de comparação (==), variáveis objeto são comparadas de 
maneira simples, nominalmente. Duas instâncias de objetos são iguais (idênticas) se tem os mesmos atributos e valores, e 
são instâncias da mesma classe, usamos o operador de identidade (===) para ser feito essa comparação_

***


<a href="#back0191">voltar a pergunta</a><br/>
<a name="0191">0191</a> - **Resposta:** _É a habilidade de forçar um parâmetro para que seja um objeto (especificado o nome 
da classe no protótipo da função) ou `array` (a partir do PHP 5.1). Contudo, se `NULL` é usado como o valor padrão do 
parâmetro, ele será permitido como um argumento nas chamadas á função_

***


<a href="#back0192">voltar a pergunta</a><br/>
<a name="0192">0192</a> - **Resposta:** _Somente o objeto da classe `OutraClasse será passado por parametro na hora da `
instânciação da classe `MinhaClasse`_

```php
class MinhaClasse
{
    public function teste(OutraClasse $outraclasse) {
        echo $outraclasse->var;
    }
}

class OutraClasse {
    public $var = 'Alô Mundo';
}

$minhaclasse = new MinhaClasse;

$foo = new OutraClasse;
$minhaclasse->teste($foo);
```

***


<a href="#back0193">voltar a pergunta</a><br/>
<a name="0193">0193</a> - **Resposta:** _`objeto` e `array` (a partir do PHP 5.1) e `NULL` quando é passado como valor
padrão do parâmetro_

***


<a href="#back0194">voltar a pergunta</a><br/>
<a name="0194">0194</a> - **Resposta:** _Implementado no PHP 5.3.0, recurso chamado `late static bindings` que pode ser usado 
para referênciar a classe chamada no contexto de herança estática_

***


<a href="#back0195">voltar a pergunta</a><br/>
<a name="0195">0195</a> - **Resposta:** _Referências estáticas para a atual classe como `self::` ou `__CLASS__` são resolvidas 
usando a classe na qual a função pertence, como onde ele foi definida_

EX1:

    retorno B
    
EX2:

    retorno A

***


<a href="#back0196">voltar a pergunta</a><br/>
<a name="0196">0196</a> - **Resposta:**

Retorno:
    
    A
    C
    C
    
A resolução do `late static bindings` termina em uma chamada estática inteiramente resolvida sem volta. Por outro lado, 
chamadas estáticas usando palavras-chave como `parent::` ou `self::` encaminharão a informação, se fosse removido o método 
`who` da classe `C` seria retornado `A B B`

***


<a href="#back0197">voltar a pergunta</a><br/>
<a name="0197">0197</a> - **Resposta:** _Não necessáriamente são passados sempre por referência,  Uma referência PHP é um alias, 
que permite duas variáveis diferentes escreverem para o mesmo valor. A partir do PHP5, uma variável objeto não contém mais o 
próprio objeto como valor. Ela contém um identificador do objeto que permite que os acessadores do objeto encontrem o objeto real.
Quando um objeto é enviado por argumento, retornado ou atribuído para outra variável, as variáveis diferentes não são aliases: 
elas armazenam uma cópia do identificador, que aponta para o mesmo objeto_

***


<a href="#back0198">voltar a pergunta</a><br/>
<a name="0198">0198</a> - **Resposta:** _Desde a versão do PHP 5.4.0_

***


<a href="#back0199">voltar a pergunta</a><br/>
<a name="0199">0199</a> - **Resposta:**


> 1.  PHP 5.4.0
>
> 2.  PHP 5.3.3
>
> 3.  PHP 5.3.0
>
> 4.  PHP 5.3.0
>
> 5.  PHP 5.3.0
>
> 6.  PHP 5.3.0
> 
> 7.  PHP 5.3.0
>
> 8.  PHP 5.3.0
>
> 9.  PHP 5.3.0
>
> 10. PHP 5.3.0
>
> 11. PHP 5.2.0
>
> 12. PHP 5.1.3
>
> 13. PHP 5.1.0
>
> 14. PHP 5.1.0

***
