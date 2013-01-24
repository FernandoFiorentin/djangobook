======================
Cap�tulo 2: Come�ando
======================

Instalar o Django � um processo de v�rios passos, em fun��o das m�ltiplas partes que
envolve os cen�rios de desenvolvimento web hoje em dia. Neste cap�tulo, vamos leva-los atrav�s de 
como se instalar o framework e as suas dependencias.

Como o Django � "apenas" c�digo Python, ele � executado em qualquer lugar que rode Python -- incluindo
alguns telefones celulares! Mas este cap�tulo abrange apenas os cen�rios comums para se 
instalar o Django. Vamos assumir que voc� esteje instalando em uma m�quina desktop/laptop ou um servidor.

Depois, no Cap�tulo 12, n�s iremos cobrir como fazer o deploy do Django para um site em produ��o.

Instalando o Django
====================

Django � puramente escrito em Python, ent�o o primeiro passo para instalar o 
framework � ter certeza de que voc� tem o Python instalado.

Vers�es do Python
------------------

O n�cleo do framework Django (vers�o 1.4) trabalha com qualquer vers�o do Python da 2.5
at� a 2.7. O GIS(Geographic Information Systems) do Django exige o Python 2.5 at� o 2.7.

Se voc� n�o tem certeza da vers�o do Python que que tem instalada e voc� tem
completa liberdade para tomar essa decis�o, escolha a �ltima vers�o da s�rie 2.x: vers�o 2.7.
Embora Django funcione igualmente bem com qualquer vers�o 2.5 at� 2.7, a ultima 
vers�o do Python tem boa performace de desempenho e idiomas adicionais
caracter�sticas que talvez voc� deseje ultilizar em suas aplica��es. Al�m disso, 
add-ons de terceiros que voc� possa querer ultilizar talvez nescessite da mais recente que 
o Python 2.5, ent�o ultilize a ultima versnao do Python mantendo o leque de op��es em aberto.

.. admonition:: Django and Python 3.0

    No momento em que este livro estava sendo escrito, o Python 3.0 estava sendo lan�ado, mas Django
    foi testado apenas de experimentalmente. Python 3.0 intruduziu a 
    um n�mero substancial de incompatibilidades com as vers�es anteriores, mundando 
    a si mesmo, e, como resultado, muita das principais bibliotecas Python e
    frameworks, incluindo Django, ainda n�o tinha pego.

    Django 1.5 dar� suporte para o Python 2.6, 2.7, e 3.2. Entretando,
    suporte para o Python 3.2 � considerado um "preview", o que significa que
    os desenvolvedores Django n�o est�o confiantes o suficiente para prometer
    estabilidade da produ��o. Para isso sugiro que voc� espere at� a vers�o do Django 1.6 

Instala��o
-----------

Se voc� estiver no Linux ou no Mac OS X, voc� provavelmente tem o Python instalado.
Escreva ``python`` no prompt de comando (ou em Applications/Utilities/Terminal, no Mac OS X).
Se voc� v� algo como isso, � porque o Python est� instalado::

    Python 2.7.3rc2 (default, Apr 22 2012, 22:30:17)
    [GCC 4.6.3] on linux2
    Type "help", "copyright", "credits" or "license" for more information.
    >>>

Caso contr�rio, voc� prescisa fazer o download e instalar o Python. Isso � f�cil e r�pido
instru��es detalhadas poder�o ser encontradas em http://www.python.org/download/

Instalando Django
=================

Em um determinado momento, duas dinstintas vers�es dinstintas do Django est�o dispon�veis para voc�:
a �ltima vers�o oficial e a vers�o de desenvolvimento. A vers�o que voc� decidir instalar 
depende das suas prioridades. Se voc� quer uma vers�o testada e est�vel, ou se voc� quer uma
vers�o contendo os recursos mais recentes. Talvez voc� possa contribuir para o Django, � custa de
estabilidade?

N�s recomendamos trabalhar com um lan�amento oficial, mas � importante saber que a vers�o 
de desenvolvimento existe, porque voc� ir� encontrar men��es na documenta��o e pelos 
membros da comunidade.

Instalando um lan�amento oficial
------------------------------

Um lan�amento oficial tem um n�mero de vers�o, como 1.4.2, 1.4.1 ou 1.4, 
um lan�amento n�o oficial tem um n�mero de vers�o, como 1.4.2, 1.4.1 ou 1.4, e a �ltima 
estar� sempre dispon�vel em http://www.djangoproject.com/download/.

Se voc� est� em uma distribui��o Linux que inclui um pacote do Django, � uma boa ideia
usar a vers�o do distribuidor. Dessa forma voc� ter� atualiza��es de seguran�a juntamente com
o resto dos pacotes do seu sistema.

Se voc� n�o tem acesso a uma vers�o pr�-empacotada, voc� pode fazer o download e instalar
o framework manualmente. Para isso, primeiramente fa�a o do tarball, que ser� chamado
de algo como ``Django-1.4.2.tar.gz``. (N�o importa em qual diret�rio local voc� tenha baixado
este arquivo inicial; O processo de instala��o colocar� os arquivos do Django no lugar correto.) 
Ent�o, descompacte-o e e execute ``setup.py install``, como voc� faz com a maioria das bibliotecas
do Python.

Veja como esse processo se parece em sistemas Unix:

#. ``tar xzvf Django-1.4.2.tar.gz``
#. ``cd Django-*``
#. ``sudo python setup.py install``

No Windows, n�s recomendamos o uso do 7-Zip (http://www.djangoproject.com/r/7zip/)
para descomprimir os arquivos ``.tar.gz``. Uma vez com os arquivos descompactados, inicie o DOS
shell (o "Prompt de Comando") com os privil�gios de administrador e execute o comando seguinte 
dentro do diret�rio cujo nome come�a com ``Django-``::

    python setup.py install

No caso de voc� estiver curioso: os arquivos do Django ser�o instalados no local da
instala��o do seu Python no ``site-packages`` diret�rio -- um diret�rio aonde o o Python
procura por biblioteca de terceiros. Normalmente � um lugar como ``/usr/lib/python2.7/site-packages``.

Instalando a vers�o de "Desenvolvimento"
----------------------------------------

Django ultiliza o Git (http://git-scm.com) para o controle de vers�o. A mais
recente e maior vers�o de desenvolvimento do Django se encontra no seu oficial 
reposit�rio do Git (https://github.com/django/django). Voc� deve considerar a 
instala��o dessa vers�o se voc� quer trabalhar on the bleeding edge, ou se voc� quiser 
contribuir com o c�digo do Django.

Git � gratu�to, um uma distribui��o de c�digo live de revis�o de controle de sistema, e o
time do Django usa ele para controlar as mudan�as no c�digo fonte do Django. Voc� pode fazer
o download e instalar o Git no http://git-scm.com/download, mas � mas f�cil instalar com
o controlador de pacots do seu sistema operacional. Voc� pode usar o Git para pegar a mais 
recente vers�o dos c�digos do Django e, a qualquer momento, voc� pode atualizar os c�digos 
da sua vers�o local do Django para obter as �ltimas altera��es feitas pelos os desenvolvedores
Django.

Ao usar a vers�o de desenvolvimento, tenha em mente que n�o h� coisas como garantias de que
n�o ser� quebrada a qualquer momento. Como dito, alguns membros do time do Django executa sites
de produ��o em vers�es de desenvolvimento, para que eles tenham um incentivo de mant�-los est�veis.

Para pegar a �ltima vers�o do Django, siga esses passos:

#. Tenha certeza que voc� tenha o Git instalado. Voc� pode peg�-lo gratuitamente em http://git-scm.com/,
e voc� pode achar a excelente documenta��o em http://git-scm.com/documentation.

#. Clone o reposit�rio usando o seguinte comando ``git clone https://github.com/django/django djmaster``

#. Localize na instala��o do Python o diret�rio ``site-packages``. Normalmente
   fica localizada em um lugar como ``/usr/lib/python2.7/site-packages``. Se voc� n�o faz id�ia,
   escreva isso no prompt de comando::

       python -c 'import sys, pprint; pprint.pprint(sys.path)'

    A sa�da resultante dever� incluir o diret�rio do seu ``site-packages``.

#. Dentro do diret�rio ``site-packages``, crie um arquivo chamado ``djmaster.pth``
  e edite ele para conter o caminho completo para o seu diret�rio ``djmaster``.
  Por exemplo, o arquivo poderia conter essa linha::

       /path/to/djmaster

#. Coloque ``djmaster/django/bin`` em seu PATH do sistema. Este diret�rio inclui
   inclui utilit�rios de administra��o, tais como o ``django-admin.py``.

.. admonition:: Dica:

    Se arquivos ``.pth`` s�o novos para voc�, voc� pode aprender mais sobre eles em
    http://www.djangoproject.com/r/python/site-module/.

Depois de baixar pelo Git e seguir os passos anteriores, n�o h� nescessidade de 
executar ``python setup.py install``-- voc� acabou de fazer o trabalho manualmente!

Como o c�digo do Django muda frequentemente com corre��o de bugs e ad��o de recurso,
voc� provavelmente queira atualiza-lo de vez em quando. Para atualizar o c�digo, 
apenas execute o comando ``git pull origin master`` dentro do diret�rio ``djmaster``.
Quando voc� executar o comando, o Git entrar� em contato com https://github.com/django/django,
determinando se algo c�digo fonte foi mudado, e atualizando a sua vers�o local com as altera��es
que tem sido feitas desde o �ltimo update. It's quite slick.

Finalmente, se voc� usa a vers�o de desenvolvimento do Django, voc� deve saber como 
qual a vers�o do Django est� sendo executada. Conhecer o n�mero da sua vers�o ser� importante
se voc� nescessitar correr at� a comunidade para ajuda, ou se voc� apresentar melhorias 
para o framework. Nestes casos, voc� dever� dizer as pessoas que revisionam, tamb�m conhecido como "commit", 
o que voc� est� usando. Para saber o seu atual "commit", digite "git log -1" de dentro de um diret�rio ``django``, e 
olhe para os identificadores depois de "commit". Este n�mero muda toda vez que o Django � alterado,
seja por meio de uma corre��o de bug, adi��o de funcionalidade, documenta��o ou melhoria de qualquer coisa.

Testando a instala��o do Django
================================

Para um feedback positivo de p�s instala��o, pare um instante para ver se a instala��o
est� funcionando. Em um shell de comando, mude para outro diret�rio (ex., *n�o* o diret�rio que que
cont�m o diret�rio ``django``) e inicie o interpretador interativo Python digitando ``python``. Se a 
instala��o obteve exito, voc� podera importar o m�dulo ``django``:

    >>> import django
    >>> django.VERSION
    (1, 4, 2, 'final', 0)

.. admonition:: Exemplos do Interpretador Interativo

    O interpretador interativo do Python � um programa de linha de comando que permite que voc� escreva
    um programa Python interativamente. Para inicializa-lo, execute o comando ``python`` na linha de comando.

    Ao longo desse livro, apresentamos exemplos em sess�es no interpretador interativo do Python. Voc� poder�
    reconhecer esses exemplos pelos tr�s sinais de maior qu� (``>>>``), que designam o interpretador no prompt. Se
    voc� est� copiando exemplos deste livro, n�o copie estes sinais de maio-qu�.

    Declara��es de v�rias linhas nesse interpretador interativo s�o preenchidos com tr�s pontos (``...``). Por exemplo::

        >>> print """This is a
        ... string that spans
        ... three lines."""
        This is a
        string that spans
        three lines.
        >>> def my_function(value):
        ...     print value
        >>> my_function('hello')
        hello

    Esses tr�s pontos no inicio de linhas adicionais s�o inseridas pelo shell do Python -- eles n�o s�o parte
    daquilo que est� sendo inserido. N�s incluimos aqui para ser fiel a sa�da real do interpretador. Se voc� copiar
    estes exemplos para acompanhar, n�o copie estes pontos.

Configurando um Banco de Dados
===============================

Neste ponto, voc� pode muito bem come�ar a escrever uma aplica��o web com o Django, 
porque os pr�-requisitos r�pidos do Django � apenas estar trabalhando com uma instala��o do Python.
No entanto, as probabilidades de que voc� ir� desenvolver um Web site com um *banco de dados dirigido*, 
neste caso, voc� nescessitar� de configurar um servidor de banco de dados.

Se voc� apenas quer come�ar a jogar com o Django, pule para a se��o "Come�ando um Projeto" --
mas tenha em mente que todos os exemplos desse livro asumme que voc� tenha trabalhado configurado
um banco de dados.

Django suporta quatro tipo de banco de dados

* PostgreSQL (http://www.postgresql.org/)
* SQLite 3 (http://www.sqlite.org/)
* MySQL (http://www.mysql.com/)
* Oracle (http://www.oracle.com/)

Para a maior parte, todos esses bancos de dados trabalham igualmente bem com o n�cleo do Django framework.
(Uma not�vel excess�o � o opcional GIS suporte ao Django, que � muito mais poderoso que o PostgreSQL do que 
com outros bancos de dados.) Se voc� n�o estiver amarrado a nenhum sistema legado e tem a liberdade para 
escolher o banco de dados, n�s recomendamos PostgreSQL, que alcan�a um bom equilibrio entre custo, recurso, 
velocidade e estabilidade.

Configurar o banco de dados � um processo de duas etapas:

* Primeiro, voc� prescisa instalar e configurar servidor de banco de dados em si.
  Este processo est� al�m do escopo desse livro, mas cada um dos quatro banco de dados
  tem uma rica documenta��o em seus pr�prios websites. (Se, voc� est� em um servidor
  de hospedagem compartilhado, provavelmente eles ir�o definiram isso para voc�.)

* Segundo, voc� prescisa instalar a biblioteca Python para o seu banco de dados em particular. 
  Isso � um pouco de c�digo de terceiros que permite ao Python se comunicar com o banco de dados.
  N�s delineamos especificamente, por requerimentos de banco de dados nas se��es seguintes.

Se voc� est� apenas brincando um pouco com o Django e n�o quer instalar um servidor de 
banco de dados, considere ent�o usar o SQLite. SQLite � o unico na lista de banco de dados suportados
� o �nico que n�o requere nenhum dos passos citados acima. Ele se limita em ler e escrever informa��es
em um �nico arquivo em seu sistema, e a vers�o 2.5 do Python ou superior inclui um suporte nativo para ele.

No Windows, a obten��o de drives bin�rios do banco de dados pode ser algo frustante. Se voc� est� ansioso para
saltar, n�s recomendamos o uso do Python 2.7 e seu suporte nativo para o SQLite.

Usando Django com o PostgresSQL
--------------------------------

Se voc� esta usando o PostgreSQL, voc� nescessita instalar o pacote ``psycopg`` ou o ``psycopg2`` 
pelo endere�o http://www.djangoproject.com/r/python-pgsql/. N�s recomendamos ``psycopg2``, como � mais novo, 
mais ativamente desenvolvido e pode ser f�cilmente instalado. De qualquer forma, tome nota da vers�o que 
voc� est� ultilizando, a vers�o 1 ou a 2; voc� ir� nescessitar dessa informa��o posteriormente.

Se voc� est� usando o PostgreSQL no Windows, se pode achar um precompilador de bin�rios do ``psycopg``
no http://www.djangoproject.com/r/python-pgsql/windows/.

Se voc� estiver no Linux, verifique se a sua distribui��o de gerenciamento de pacotes sistemas ofere�e
um pacote chamado "python-psycopg2", "psycopg2-python", "python-postgresql" ou alguma coisa similar.

Usando Django com SQLite 3
--------------------------

Voc� est� com sorte: pois n�o � requerido especificidades de banco de dados, porque o Python vem com suporte
so SQLite. Pule para a pr�xima se��o.

Usando Django com MySQL
-----------------------

Django requer MySQL 4.0 ou acima. A vers�es 3.x n�o suporta subconsultas aninhadas 
e algumas outras declara��es SQL bastante padr�o.

Se voc� nescessita de instalar o pacote ``MySQLdb`` o endere�o �: http://www.djangoproject.com/r/python-mysql/.

Se voc� est� em uma distribui��o Linux, verifique se a sua distribui��o de gerenciamento de pacotes do sistema
oferece um pacote chamado "python-mysql", "python-mysqldb", "mysql-python" ou alguma coisa parecida.

Using Django com Oracle
------------------------

Django trabalha com o Oracle Database Server ver�es 9i ou superior.

Se voc� est� usando Oracle, voc� nescessita instalar a biblioteca ``cx_Oracle``,
no http://cx-oracle.sourceforge.net/. Use a ver�o 4.3.1 ou superior, mas evite a vers�o 5.0
devido a um bug nesta vers�o do driver. A vers�o 5.0.1 resolveu o bug, entretando, voc� pode escolher 
uma vers�o superior tamb�m.

Usando Django sem um Banco de Dados
------------------------------------

Como mencionado anteriormente, o Django atualmente n�o requer o uso de banco de dados. Se voc� quer apenas
usar ele como servidor de p�ginas din�micas que n�o ultilizam o banco de dados, est�
tudo perfeitamente bem.

Como o que disse, tenha em mente que algumas das ferramentas extras juntas com o Django *ultilizam* um banco
de dados, ent�o se voc� escolher n�o usar um banco de dados, voc� n�o poder� usufruir desses recursos.
(Destacamos esses recursos ao longo do livro.)

Come�ando um Projeto
=====================

Uma vez que o Python esteja instalado, Django e (opcionalmente) um servidor/biblioteca de banco de dados,
voc� pode pegar o primeiro passo no desenvolvimento de uma aplica��o Django atrav�z da cria��o de um *projeto*.

Um projeto � uma cole��o de configura��es para uma inst�ncia do Django, incluindo uma configura��o de banco de
dados, op��es espec�ficas do Django e configura��es de aplica��es espec�ficas.

Se esta � a sua primeira vez usando Django, voc� ter� que cuidar de algumas configura��es iniciais.
Criar um novo diret�rio para come�ar a trabalhar nele, talvez alguma coisa parecida como ``/home/username/djcode``.

.. admonition:: Aonde Coloco Esse Diret�rio Vivo?
    
    Se voc� j� tem alguma experi�ncia com PHP, voc� provavelmente est� acostumado a colocar o c�digo sobre a raiz do
    servidor (um lugar como ``/var/www``). Com Django, voc� n�o faz isso. N�o � uma boa id�ia colocar qualquer c�digo
    Python dentro da ra�z do seu servidor web. Porque ao faz�-lo voc� corre o risco das pessoas verem o seu c�digo fonte.
    E isso n�o � bom.

    Coloque o seu c�digo em algum diret�rio **fora** da ra�z do documento.

V� at� o diret�rio que voc� criou, e execute o comando ``django-admin.py startproject mysite``. Isso ir� criar um diret�rio
chamado``mysite`` no seu diret�rio corrente.

.. nota::
    ``django-admin.py`` deve estar no path do sistema se voc� instalou o Django via o utilit�rio ``setup.py``

    Se voc� estiver usando uma vers�o de desenvolvimento, voc� ir� achar ``django-admin.py`` em ``djmaster/django/bin``.
    Por causa que voc� ir� usar ``django-admin.py`` v�rias vezes, considere adicionar ao path do sistema. No Unix, voc� pode
    fazer isso usando links simb�licos de ``/usr/local/bin``, usando um comando como ``sudo ln -s /path/to/django/bin/django-admin.py
    /usr/local/bin/django-admin.py``. No Windows, voc� nescessitar� atualizar o seu vari�vem de ambiente ``PATH``. 

    Se voc� instalou o Django de um pacote de vers�o para o sua distribui��o Linux, ``django-admin.py`` pode ser chamado
    de ``django-admin``.

Se voc� ver uma mensagem de "permission denied" ao executar ``django-admin.py startproject``, voc� nescessitar� mudar as 
permiss�es dos arquivos. Para isso, navegue at� o diret�rio aonde ``django-admin.py`` est� instalado (e.g., ``cd /usr/local/bin``)
e execute o comando ``chmod +x django-admin.py``.

O commando ``startproject``  cria um diret�rio contendo 5 arquivos::

    mysite/
        manage.py
        mysite/
            __init__.py
            settings.py
            urls.py
            wsgi.py

.. nota:: N�o corresponde com voc� v�?
    
    O layout padr�o do projeto recentemente mudado. Se voc� est� vendo um layout "flat" (sem o diret�rio interior
    ``mysite/``), voc� provavelmente est� usando uma vers�o do Django que n�o corresponde a vers�o do livro. Este 
    livro cobre Django 1.4 acima, ent�o se voc� est� usando uma vers�o antiga voc� provavelmente vai querer
    consultar o dacumenta��o oficial do Django.

    A documenta��o das vers�es Django 1.x est� no endere�o  https://docs.djangoproject.com/en/1.X/.

Estes arquivos s�o os seguintes

* ``mysite/``: O exterior do diret�rio ``mysite/`` � apenas um container para o seu projeto. Esse nome
  n�o importa para o Django; voc� pode renomear ele da maneira que desejar.

* ``manage.py``: Um utilit�rio de linha de comando que permite que voc� interaja com o projeto Django de v�rias formas.
  Escreva ``python manage.py help`` para entender o que ele � capaz de fazer. Voc� nunca dever� editar este arquivo;
  ele � criado nesse diret�rio puramente por conveni�ncia.

* ``mysite/mysite/``: O interior do diret�rio ``mysite/`` � o atual pacote Python para o seu projeto. Este nome � o nome 
  do pacote Python que voc� nescessita usar para importar qualquer coisa dentro dele (e.g. ``import mysite.settings``).

*``__init__.py``: Um arquivo necess�rio para o Python tratar o diret�rio ``mysite`` como um pacote (i.e., um grupo de 
m�dulos Python). Ele � um arquivo vazio, e geralmente voc� n�o adiciona nada a ele.

* ``settings.py``: Defini��es/configura��es para este projeto Django. D� uma olhada nele para ter uma id�ia dos tipos
  configura��es avaliadas, juntamente com os seus valores padr�es.

* ``urls.py``: As URLs para este projeto Django. Pense nisso como como uma "tabela de conte�do" para o seu site em Django.  

* ``wsgi.py``: Um ponto de entrada para o WSGI compat�veis com servidores web para servir o seu projeto.
  Veja como fazer deploy com WSGI (https://docs.djangoproject.com/en/1.4/howto/deployment/wsgi/) para maiores detalhes.

Apesar do seu pequeno tamanho, estes arquivos j� constituem uma aplica��o de trabalho Django.

Executando o servidor de desenvolvimento
-----------------------------------------

Para mais alguns feedbacks posit�vos ap�s a instala��o, vamos executar o servidor de desenvolvimento do Django 
para ver a nossa aplica��o em a��o.

O servidor de desenvolvimento do Django (tamb�m chamado de "runserver") � um servidor interno, leve, que 
voc� poder� usar enquanto desenvolve o seu site. Ele � incluso com o Django ent�o voc� pode desenvolver o seu 
seite rapidamente, sem ter que lidar com configurac�o de servidor de produ��o (e.g., Apache) at� que voc� esteja
realmente pronto para o ambiente de produ��o. O servidor de desenvolvimento observa o seu c�digo e autom�ticamente
recarrega autom�ticamente, tornando f�cil para voc� alterar o seu c�digo sem a necessidade de de reiniciar qualquer coisa.

Para iniciar o servidor, mude para o seu diret�rio do container do projeto (``cd mysite``), se voc� n�o estiver, 
execute este commando::

    python manage.py runserver

You'll see something like this::

    Validating models...
    0 errors found.

    Django version 1.4.2, using settings 'mysite.settings'
    Development server is running at http://127.0.0.1:8000/
    Quit the server with CONTROL-C.

Isso inicia o servidor localmente, na porta 8000, acess�vel somente para conec��es do seu pr�prio computador. Agora que 
est� rodando visite http://127.0.0.1:8000/ com o seu web browser. Voc� vai ver um "Welcome to Django" em uma p�gina sombreada 
com agrad�veis tons de azul pastel. Est� funcionando!!

Uma nota final importante sobre o servidor de desenvolvimento que � importante mencionar antes de prosseguir. Embora 
este servidor seja conveniente para o desenvolvimento, resistir a tenta��o de us�-lo em qualquer coisa parecida com um 
ambiente e produ��o. O servidor de desenvolvimento pode lidar com apenas um pedido de cada vez de maneira confi�vel, e 
n�o passou por nenhuma esp�cie de auditoria de seguran�a. Quando chegar a hora de lan�ar o seu site, consulte o Cap�tulo
12 para informa��es sobre como fazer o deploy do Django.

.. admonition:: Mudando o Host ou Porta do Servidor de Desenvolvimento
    Por padr�o, o comando `runserver` inicializa o servidor de desenvolvimento na porta 8000, ouvindo somente para 
    conex�es locais. Se voc� deseja mudar a porta do servidor, passe isso como argumento na linha de comando::

        python manage.py runserver 8080

    Ao especificar um endere�o de IP, voc� pode dizer ao servidor para permitir conex�es n�o locais. Isso � especificamente
    �til se voc� quisesse compartilhar um site de desenvolvimento com outros membros da sua equipe. O endere�o de IP ``0.0.0.0``
    diz ao servidor atender qualquer interface de rede::

        python manage.py runserver 0.0.0.0:8000

    Quando voc� tiver feito isso, outros computadores da sua rede local poder�o visualizar o seu site em Django visitando o seu
    endere�o de IP no Web browser, e.g., http://192.168.1.103:8000/ .(Note que voc� ter� que consutar as suas configura��es de rede
    para determinar o seu endere�o de IP em sua rede local. Usu�rios Unix, tentar�o rodar "ifconfig" no prompt de comando para 
    pegar essa informa��o, usu�rios Windows, tentar�o "ipconfig".)

O que vem em seguida?
=====================

Agora que voc� tem tudo instalado e o servidor de desenvolvimento rodando, voc� est� pronto para o :doc:`aprendendo
o b�sico <c�pitulo03>` de servir p�ginas Web com Django.