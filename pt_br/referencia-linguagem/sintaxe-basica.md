[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | **Sintaxe Básica** - [Tipos](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/tipos.md)


Sintaxe Básica
==============

Perguntas
---------

<a name="back01">01</a> – quantos tipos de tipos de tags de abertura e fechamento o PHP suporta, quantos e quais são tipos especiais sendo 
que para usar eles precisam ativa uma diretiva no arquivo de configuração do php.ini e qual seria essa diretiva ?

<a href="#01">Resposta</a>
***


<a name="back02">02</a> – Qual tipo de tags você vai precisar usar quando for trabalhar com PHP em arquivos XHTML ou XML ?

<a href="#02">Resposta</a>
***


<a name="back03">03</a> – Porque o uso de tags curtas é desencorajado no PHP ?

<a href="#03">Resposta</a>
***


<a name="back04">04</a> – É necessário usar o separador de instruções ? se sim, quando é que não é obrigatório usar-las ?

<a href="#04">Resposta</a>
***


<a name="back05">05</a> – A tag de fechamento de um bloco de PHP é obrigatória ? quando é necessário o uso dela ? Se não Quais 
as vantagens de não usa-la ?

<a href="#05">Resposta</a>
***


<a name="back06">06</a> – Quais estilos de cometário o PHP suporta ?

<a href="#06">Resposta</a>
***



Respostas
---------

<a href="#back01">voltar a pergunta</a><br/>
<a name="01">01</a> - **Resposta:** _Tags suportadas pelo PHP nativamente são :_

```php
Tags sempre disponíveis
<?php ?>
<script language=”php”></script>

Tags ativas com a diretiva shot_open_tags ou quando o PHP é configurado com a opção --enable-short-tags
<? ?>

Tags ativas com a diretiva asp_tags no php.ini
<% %>
```
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
bom manter ele como um padrão_

***


<a href="#back05">voltar a pergunta</a><br/>
<a name="05">05</a> - **Resposta:** _Quando um arquivo contém código PHP e outros códigos, como HTML, Javascript, etc .. 
é necessário a tag de fechamento, quando o arquivo contém somente código PHP não é obrigatório, sendo aconselhavel não usar a tag de 
fechamento, evitando problemas com inclusões, requires, errors de header, buffering, etc ..._

***


<a href="#back06">voltar a pergunta</a><br/>
<a name="06">06</a> - **Resposta:** _O PHP suporta dois três tipos de comentários, no estilo C, C++ e shell (estilo Perl):_

    # comentário 1 estilo shell
    // comentário 2 estilo C++
    /*
    comentário 3, multiplas linhas
    */

***
