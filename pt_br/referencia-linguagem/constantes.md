[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | [Variáveis](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/variaveis.md) - **Constantes** - [Expressões](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/expressoes.md)


Constantes
==========

Perguntas
---------

<a name="back60">060</a> – Quais os tipos de dados que podem ser atribuidos a constantes ?

<a href="#060">Resposta</a>
***


<a name="back61">061</a> – Qual função é usada para resgatar todas as constantes definidas ?

<a href="#061">Resposta</a>
***


<a name="back62">062</a> – Está correto esse tipo de criação de constante fora de classes ? E a definição de constantes usando a 
palavra-chave "const" está disponivel a partir de qual versão ?

```php
const constante = "ola mundo"";
```

<a href="#062">Resposta</a>
***


<a name="back63">063</a> – Porque não podemos definir constantes com a palavra-chave `const` dentro de funções, laços e ifs ?

<a href="#063">Resposta</a>
***


<a name="back64">064</a> – Quantas constantes mágicas existem, defina cada uma delas !

<a href="#064">Resposta</a>
***


<a name="back65">065</a> – A constante mágica `__CLASS__` funcionara também para traits ?

<a href="#065">Resposta</a>
***






Respostas
---------

<a href="#back060">voltar a pergunta</a><br/>
<a name="060">060</a> - **Resposta:** _Somente dados escalares, boolean, int, float, string, ou em alguns casos com dados resource 
que deve ser evitado para evitar problemas inesperados_

***


<a href="#back061">voltar a pergunta</a><br/>
<a name="061">061</a> - **Resposta:** _get_defined_constants(true), Retorna uma matriz associativa com os nomes de todas as 
constantes e seus valores, "true" referesse ao modelo (categorize) como ele vem formatado o vetor, no caso por categoria_

***


<a href="#back062">voltar a pergunta</a><br/>
<a name="062">062</a> - **Resposta:** _sim, está correto, const pode ser usado fora de um escopo de classe a partir do PHP 5.3.0_

***


<a href="#back063">voltar a pergunta</a><br/>
<a name="063">063</a> - **Resposta:** _Devem ser declaradas no escopo de topo (principal) pois são definidas no tempo de compilação, 
por isso que não podem ser definidas dentro de funções, laços ou ifs_

***


<a href="#back064">voltar a pergunta</a><br/>
<a name="064">064</a> - **Resposta:** _8 Constantes_

    __LINE__
    A linha atual do script
    
    __FILE__
    O caminho completo e nome do arquivo
    
    __DIR__
    O diretório do arquivo
    equivalente a dirname(__FILE__)
    
    __FUNCTION__
    O nome da função
    
    __CLASS__
    O nome da classe, a partir do PHP 5.4 funciona também em traits
    
    __TRAIT__
    O nome da trait
    
    __METHOD__
    O nome do método de classe
    
    __NAMESPACE__
    O nome do namespace atual

***


<a href="#back065">voltar a pergunta</a><br/>
<a name="065">065</a> - **Resposta:** _Sim, a partir do PHP 5.4_

***

