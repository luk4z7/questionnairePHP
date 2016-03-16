[home](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/home.md) | [Contexto de opções e parâmetros](https://github.com/luk4z7/questionnairePHP/blob/master/pt_br/referencia-linguagem/contexto-opcoes-parametros.md) - **Protocolo e wrappers suportados**


Protocolo e wrappers suportados
===============================

Perguntas
---------

<a name="back0257">0257</a> – Qual a definição para `streams` ?

<a href="#0257">Resposta</a>
***


<a name="back0258">0258</a> – Destaque alguns `streams` padrões que o PHP possui e descreva o objetivo especifico de cada:

<a href="#0258">Resposta</a>
***


Respostas
---------

<a href="#back0247">voltar a pergunta</a><br/>
<a name="0247">0247</a> - **Resposta:** _É uma camada de abstração para acesso a arquivos, O termo `streams` refere-se
ao número de recursos, como diferentes ficheiros, conexões de rede, protocolo de compressão, e assim por diante,
podem ser condiderados como `streams` de dados a lido/escrito que em sequência ou aleatoriamente_

***


<a href="#back0248">voltar a pergunta</a><br/>
<a name="0248">0248</a> - **Resposta:**

    file://              acesso ao arquivo padrão
    http://              acesso a recursos remotos via HTTP
    ftp://               acesso a recursos remotos via FTP
    php://               acessar vários I/O's como STDIN/STDOUT, ou postar dados brutos
    compress.zlib://
    e
    compress.bzip2://    acesso a arquivos compactados (gzip / bzip2), utilizando a biblioteca
                         de compressão zlib.

    zip://               acesso a arquivos zip compactados (requer a extensão zip)
    data://              RFC 2397 o acesso aos dados em strings (adicionado no PHP 5.2)
    glob://              encontrar caminhos por correspondência de padrão (por exemplo, glob ())
    phar://              PHP Arquivos (também conhecidos como PHAR) córrego invólucro (adicionado
                         no PHP 5.3)

***