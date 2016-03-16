[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | **Sintaxe Básica** - [Tipos](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/tipos.md)


Sintaxe Básica
==============

Perguntas
---------

<a name="back01">01</a> – Quantos tipos de tags de abertura e fechamento o PHP suporta, quais são os tipos especiais sendo
que para usá-los é necessário ativar uma diretiva no arquivo de configuração do php.ini e qual seria essa diretiva ?

<a href="#01">Resposta</a>
***


<a name="back02">02</a> – Qual tipo de tags você vai precisar usar quando for trabalhar com PHP em arquivos XHTML ou XML ?

<a href="#02">Resposta</a>
***


<a name="back03">03</a> – Porque o uso de tags curtas é desencorajado no PHP ?

<a href="#03">Resposta</a>
***


<a name="back04">04</a> – É necessário usar o separador de instruções ? se sim, quando é que não é obrigatório usá-las ?

<a href="#04">Resposta</a>
***


<a name="back05">05</a> – A tag de fechamento de um bloco de PHP é obrigatória ? quando é necessário o uso dela ? Se não, Quais
as vantagens de não usá-la ?

<a href="#05">Resposta</a>
***


<a name="back06">06</a> – Quais estilos de comentários o PHP suporta ?

<a href="#06">Resposta</a>
***



Respostas
---------

<a href="#back01">voltar a pergunta</a><br/>
<a name="01">01</a> - **Resposta:** _Existem 5 tipos de Tags suportadas pelo PHP:_


__Standard Tags__

    <?php
        ...code
    ?>

Tags padrão, são a melhor solução para a portabilidade e compatibilidade com versões anteriores, pois possui a garantia
de estar disponível e não pode ser desativada alterando o arquivo de configuração do PHP


__Echo Tags__

    <?= $variableToEcho; ?>

Antes do PHP 5.4, permitindo as `shorts tags`, também foi disponibilizado as `short-form <?= $variable; ?>`
também conhecida como `echo tags` que permite imprimir o resultado de uma expressão diretamente na saída do
script, com o lançamento do PHP 5.4, `shots-tags` e `echo tags` foram divididas e as `echo tags` agora são
sempre habilitadas.


__Short Tags__

    <?
        ...code
    ?>

As `short tags` foram durante algum tempo o padrão no mundo PHP, no entanto elas tem a grande desvantagem de entrar
em conflito com as instruções de processamento XML `ex: <?xml` e, portanto, já não são recomendadas, atualmente sendo
obsoletas, são ativadas com a diretiva `short_open_tags` ou quando o PHP é configurado com a opção `--enable-short-tags`


__Script Tags__

    <script language=”php”>
        ...code
    </script>

Scripts tags foram introduzidas de modo que os editores HTML que foram capazes de ignorar Javascript, mas eram incapazes
de lidar com as tags padrão do PHP também poderia ignorar código PHP.


__ASP Tags__

    <%
        ...code
    %>

Ninguém entende por que as ASP tags foram introduzidas. No entanto, se você quiser ativar essa opção é possível com a
diretiva `asp_tags` no php.ini.

Short Tags, Script Tags e ASP Tags são todas consideradas obsoletas e seu uso é fortemente desencorajado.

***


<a href="#back02">voltar a pergunta</a><br/>
<a name="02">02</a> - **Resposta:** _Para embutir código PHP em arquivos como XHTML é necessário cumprir com os padrões, usando a tag_

```php
<?php ?>
```
***


<a href="#back03">voltar a pergunta</a><br/>
<a name="03">03</a> - **Resposta:** _O uso de tags curtas deve ser evitado ao desenvolver aplicações ou bibliotecas que serão 
redistribuidas, ou serão usadas em servidores PHP que não estão sobre seu controle, evitando assim conflitos_

***


<a href="#back04">voltar a pergunta</a><br/>
<a name="04">04</a> - **Resposta:** _Para cada final de linha é usado o separador de instruções, nesses casos são obrigatórios, 
mas quando no final de linha que será a ultima linha do arquivo não é necessário, mas para maior legibilidade do código sempre é 
bom manter ele com um padrão_

***


<a href="#back05">voltar a pergunta</a><br/>
<a name="05">05</a> - **Resposta:** _Quando um arquivo contém código PHP e outros códigos, como HTML, Javascript, etc .. 
é necessário a tag de fechamento, quando o arquivo contém somente código PHP não é obrigatório.
É importante lembrar que todos os personagens fora de tags PHP são copiados como estão pelo intérprete do script de saída e
isso inclui caracteres de nova linha.
Novas linhas são normalmente ignoradas pelos navegadores, como eles são caracteres não-semânticas em HTML, no entanto, eles
também são usados como separadores entre a parte de cabeçalho de resposta HTTP de um servidor web e os dados reais;
por isso, a emissão de um caractere de nova linha antes de todos os cabeçalhos pode causar consequências bastantes
desagradáveis, para mitigar esse problema, a primeira nova linha logo após uma tag de fechamento (`?>`) é desencorajado
pelo analisador, isso também resolve um problema introduzido pelo fato de que um número de editores de texto populares
anexará automaticamente uma nova linha ao final do seu arquivo,
evitando problemas com inclusões, requires, errors de header, buffering, etc ..._

***


<a href="#back06">voltar a pergunta</a><br/>
<a name="06">06</a> - **Resposta:** _O PHP suporta três tipos de comentários, no estilo C, C++ e shell (estilo Perl):_

    # comentários de uma linha
    // comentários de uma linha

    /*
     * comentário de multiplas linhas
    */

    /**
     *  Documentação de API exemplo
     *
     *  @param string $bar
     */

***
