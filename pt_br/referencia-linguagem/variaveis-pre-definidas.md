[Referências]( ) - **Variáveis pré-definidas** - [Exceções pré-definidas]( )


Variáveis pré-definidas
=======================

Perguntas
---------

<a name="back0231">0231</a> – O que são variáveis superglobais no PHP ?

<a href="#0231">Resposta</a>
***


<a name="back0232">0232</a> – PHP provê um grande número de variáveis pré-definidas para todos os scripts, defina cada uma sua 
findadade nas seguintes variáveis:

> 1.  $GLOBALS
>
> 2.  $_SERVER
>
> 3.  $_GET
>
> 4.  $_POST
>
> 5.  $_FILES
>
> 6.  $_REQUEST
>
> 7.  $_SESSION
>
> 8.  $_ENV
>
> 9.  $COOKIE
>
> 10. $php_errormsg
>
> 11. $HTTP_RAW_POST_DATA
>
> 12. $http_response_header
>
> 13. $argc
>
> 14. $argv

<a href="#0232">Resposta</a>
***


<a name="back0233">0233</a> – A partir de qual versão foram introduzidas as variáveis globais no PHP ?

<a href="#0233">Resposta</a>
***


<a name="back0234">0234</a> – Sabendo que `$GLOBALS` referência todas variáveis disponíveis no escopo global qual o retorno do
codigo abaixo:

```php
function test() {
    $foo = "local variable";

    echo '$foo in global scope: ' . $GLOBALS["foo"] . "\n";
    echo '$foo in current scope: ' . $foo . "\n";
}

$foo = "Example content";

var_dump($GLOBALS);

test();
```

<a href="#0234">Resposta</a>
***


<a name="back0235">0235</a> – `$_SERVER` é um array contendo informação como cabeçalhos, paths, e localizações do script. Defina
cada um dos elementes listados abaixo:

> 1.  PHP_SELF:
>
> 2.  argv:
>
> 3.  argc:
>
> 4.  GATEWAY_INTERFACE:
>
> 5.  SERVER_ADDR:
>
> 6.  SERVER_NAME:
>
> 7.  SERVER_SOFTWARE:
>
> 8.  SERVER_PROTOCOL:
>
> 9.  REQUEST_METHOD:
>
> 10. REQUEST_TIME:
>
> 11. QUERY_STRING:
>
> 12. DOCUMENT_ROOT:
>
> 13. HTTP_ACCEPT:
>
> 14. HTTP_ACCEPT_CHARSET:
>
> 15. HTTP_ACCEPT_ENCODING:
>
> 16. HTTP_ACCEPT_LANGUAGE:
>
> 17. HTTP_CONNECTION:
>
> 18. HTTP_HOST:
>
> 19. HTTP_REFERER:
>
> 20. HTTP_USER_AGENT:
>
> 21. HTTPS:
>
> 22. REMOTE_ADDR:
>
> 23. REMOTE_HOST:
> 
> 24. REMOTE_PORT:
>
> 25. SCRIPT_FILENAME:
>
> 26. SERVER_ADMIN:
>
> 27. SERVER_PORT:
>
> 28. SERVER_SIGNATURE:
>
> 29. PATH_TRANSLATED:
>
> 30. SCRIPT_NAME:
>
> 31. REQUEST_URI:
>
> 32. PHP_AUTH_DIGEST:
>
> 33. PHP_AUTH_USER:
>
> 34. PHP_AUTH_PW:
>
> 35. AUTH_TYPE:

<a href="#0235">Resposta</a>
***


<a name="back0236">0236</a> – A variável de requisição HTTP `$_REQUEST` é um array associativo que por padrão contém informações 
de quais outras variáveis de requisição HTTP ?

<a href="#0236">Resposta</a>
***


<a name="back0237">0237</a> – Quando foi intruduzido a diretiva que afeta o conteúdo de `$_REQUEST` e qual o nome dessa diretiva?

<a href="#0237">Resposta</a>
***


<a name="back0238">0238</a> – Em qual versão do PHP `$_FILES` foi removido de `$_REQUEST`?

<a href="#0238">Resposta</a>
***


<a name="back0239">0239</a> – `$php_errormsg` é uma variável contendo o texto da última mensagem de erro gerada pelo PHP, mas 
está variável somente estará disponível dentro do escopo no qual o erro ocorreu, e somente se a opção de configuração do php.ini 
estiver habilitada, que por padrão vem 'off' qual seria essa diretiva ?

<a href="#0239">Resposta</a>
***


<a name="back0240">0240</a> – Qual a finalidade da `$http_response_header`?

<a href="#0240">Resposta</a>
***



Respostas
---------

<a href="#back0231">voltar a pergunta</a><br/>
<a name="0231">0231</a> - **Resposta:** _Superglobais são variáveis nativas que estão sempre disponíveis em todos escopos_

***


<a href="#back0232">voltar a pergunta</a><br/>
<a name="0232">0232</a> - **Resposta:**

> 1.  Referência todas as variáveis disponíveis no escopo global
>
> 2.  Informações do servidor e ambiente de execução
>
> 3.  HTTP GET variáveis
>
> 4.  HTTP POST variáveis
>
> 5.  HTTP File Upload variáveis
>
> 6.  Variáveis de requisição HTTP
>
> 7.  Variáveis de sessão
>
> 8.  Variáveis de ambiente
>
> 9.  HTTP Cookie
>
> 10. A Mensagem de erro anterior
>
> 11. Informação não-tratada do POST
>
> 12. Cabeçalho de resposta HTTP
>
> 13. O número de argumentos passados para o script
>
> 14. Array de argumentos passados para o script

***


<a href="#back0233">voltar a pergunta</a><br/>
<a name="0233">0233</a> - **Resposta:** _4.1.0_

***


<a href="#back0234">voltar a pergunta</a><br/>
<a name="0234">0234</a> - **Resposta:**

Retorno:

    $foo in global scope: Example content
    $foo in current scope: local variable
    
A descrição de `$GLOBALS` é um array associativo contendo referências para todas as variáveis que estão definidas no escopo global 
do script, o nome das variáveis são chaves do array.

***


<a href="#back0235">voltar a pergunta</a><br/>
<a name="0235">0235</a> - **Resposta:**

> 1.  O nome do arquivo do script que está executando, relativa à raiz do documento, OBS: se estiver rodando PHP em linha de 
      comando, está variável contém o nome do script desde o PHP 4.3.0, anteriormente ela não estava disponível
>
> 2.  Array de argumentos passado para o script. Quando o script é executado na linha de comando, isto permite um acesso aos 
      parâmetros de linha de comando no estilo do C. Quando chamado via método GET, ele conterá a query string
>
> 3.  Contém o número de parâmetros da linha de comando passados para o script (se executado da linha de comando)
>
> 4.  O número de revisão da especificação CGI que o servidor está utilizando, por exemplo : 'CGI/1.1'
>
> 5.  O endereço IP do servidor onde está o script em execução
>
> 6.  O nome host do servidor onde o script atual é executado. Se o script está rodando em um host virtual, este será o valor 
      definido para aquele host virtual
>
> 7.  A string de identificação do servidor, fornecida nos headers quando respondendo a requests
>
> 8.  Nome e número de revisão do protocolo de informação pelo qual a página foi requerida, por exemplo 'HTTP/1.0'
>
> 9.  Contém o método de request utilizando para acessar a página. Geralmente 'GET', 'HEAD', 'POST' ou 'PUT'
>
> 10. O timestamp do início da requisição. Disponível desde o PHP 5.1.0
>
> 11. A query string (string de solicitação), se houver, pela qual a página foi acessada
>
> 12. O diretório raiz sob onde o script atual é executado, como definido no arquivo de configuração do servidor
>
> 13. O conteúdo do header Accept: da requisição atual, se houver
>
> 14. O conteúdo do header Accept-Charset: da requisição atual, se houver. Exemplo: 'iso-8859-1,*,utf-8'
>
> 15. O conteúdo do header Accept-Encoding: da requisição atual, se houver. Exemplo: 'gzip'
>
> 16. O conteúdo do header Accept-Language: da requisição atual, se houver. Exemplo 'en'
>
> 17. O conteúdo do header Connection: da requisição atual, se houver. Exemplo: 'Keep-Alive'
>
> 18. O conteúdo do header Host: da requisição atual, se houver
>
> 19. O endereço da página (se houver) através da qual o agente do usuário acessou a página atual. Essa diretiva é informada pelo 
      agente do usuário. Nem todos os browsers geram esse header, e alguns ainda possuem a habilidade de modificar o conteúdo do 
      HTTP_REFERER como recurso. Em poucas palavras, não é confiável
>
> 20. O conteúdo do header User-Agent: da requisição atual, se houver. É uma string denotando o agente de usuário pelo qual a página 
      é acessada. Um exemplo típico é: Mozilla/4.5 [en] (X11; U; Linux 2.2.9 i586). Além de outras coisas, você pode utilizar este 
      valor com get_browser() para personalizar a geração de suas páginas para as capacidades do agente do usuário
>
> 21. Define para um valor não vazio se o script foi requisitado através do protocolo HTTPS. Note que quando usando ISAPI com 
      IIS, o valor será off se a requisição não for feita por protocolo HTTPS
>
> 22. O endereço IP de onde o usuário está visualizado a página atual
>
> 23. O nome do host que o usuário utilizou para chamar a página atual. O DNS reverso (lookup) do REMOTE_ADDR do usuário. 
      
      Nota: Seu servidor web precisa estar configurado para criar essa variável. Por exemplo, no Apache você precisa colocar um 
      HostnameLookups On dentro do httpd.conf
> 
> 24. A porta TCP na máquina do usuário utilizada para comunicação com o servidor web
>
> 25. O caminho absoluto o script atualmente em execução.
      
      Nota:
      Se o script for executado pela CLI com um caminho relativo, como file.php ou ../file.php, $_SERVER['SCRIPT_FILENAME'] irá 
      conter o caminho relativo especificado pelo usuário
>
> 26. O valor fornecido pela diretiva SERVER_ADMIN (do Apache) no arquivo de configuração do servidor. Se o script está sendo 
      executado em um host virtual, este será os valores definidos para aquele host virtual
>
> 27. A porta na máquina servidora utilizada pelo servidor web para comunicação. Como default, este valor é '80'. Utilizando SSL, 
      entretanto, mudará esse valor para a porta de comunicação segura HTTP
>
> 28. String contendo a versão do servidor e nome do host virtual que é adicionado às páginas geradas no servidor, se ativo
>
> 29. O caminho real do script relativo ao sistema de arquivos (não o document root), depois realizou todos os mapeamentos de caminhos (virtual-to-real). 
      
      Nota: A partir do PHP 4.3.2, PATH_TRANSLATED não mais existe implicitamente sob a SAPI do Apache 2, ao contrário da mesma 
      situação no Apache 1, onde ela tinha o mesmo valor da variável de servidor SCRIPT_FILENAME, quando a mesma não era 
      configurada pelo Apache. Essa mudança foi realizada para conformidade com a especificação CGI, onde PATH_TRANSLATED deve 
      existir somente se PATH_INFO estiver definida. Apache 2 users may use AcceptPathInfo = On inside httpd.conf to define 
      PATH_INFO
>
> 30. Contém o caminho completo do script atual. Útil para páginas que precisam apontar para elas mesmas (dinamicamente). A 
      constante __FILE__ contém o caminho completo e nome do arquivo (mesmo incluído) atual
>
> 31. O URI fornecido para acessar a página atual, por exemplo, '/index.html'
>
> 32. Quando executando no Apache como módulo fazendo autenticação HTTP esta variável é definida para o cabeçalho 'Authorization' 
      enviado pelo cliente (que você pode então usar para fazer apropriada validação)
>
> 33. Quando executando sob o Apache ou IIS (ISAPI no PHP 5) como módulo e fazendo autenticaçào HTTP, esta variável estará 
      definida com o username fornecido pelo usuário
>
> 34. Quando executando sob o Apache ou IIS (ISAPI no PHP 5) como módulo e fazendo autenticaçào HTTP, esta variável estará 
      definida com a senha fornecida pelo usuário
>
> 35. Quando executando sob o Apache como módulo e fazendo autenticaçào HTTP, esta variável estará definida com o tipo de 
      autenticação utilizado

***


<a href="#back0236">voltar a pergunta</a><br/>
<a name="0236">0236</a> - **Resposta:** _$_GET, $_POST, $_COOKIE_

***


<a href="#back0237">voltar a pergunta</a><br/>
<a name="0237">0237</a> - **Resposta:** _Versão do PHP 5.3.0, nome da diretiva é `request_order`_

***


<a href="#back0238">voltar a pergunta</a><br/>
<a name="0238">0238</a> - **Resposta:** _Versão do PHP 4.3.0_

***


<a href="#back0239">voltar a pergunta</a><br/>
<a name="0239">0239</a> - **Resposta:** _track_errors_

***


<a href="#back0240">voltar a pergunta</a><br/>
<a name="0240">0240</a> - **Resposta:** _Retorna o cabeçalho de responta HTTP_

***
