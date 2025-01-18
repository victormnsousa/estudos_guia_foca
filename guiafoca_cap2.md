# 2 Explicações Básicas 

## 2.2 Arquivos

Onde gravamos nossos dados; cada arquivo é identificado por um nome; 

O GNU/Linux é case sensitive, diferencia letras maiúsculas de minúsculas; 

Um arquivo oculto no GNU/Linux é identificado por um **./ponto** no início de seu nome/ eles não aparecem em listagens normais; para listar:

~~~bash
ls -a 
~~~

### 2.2.1 Extensão de arquivos 

As extensões identificam os tipos de arquivo:

* **.txt**: arquivo de texto
* **script.sh**: arquivo de script
* **system_.log**: registro de algum programa do sistema
* **arquivo_.gz**: arquivo compacto pelo utilitário 'gzip'
* **index_.html**: página de internet no formato Hypertexto

A extensão de um arquivo também ajuda a saber o que precisamos saber para abri-lo; Na maioria dos casos, a extensão não é requerida pelo sistema GNU/Linux, mas é conveniente seu uso; 

### 2.2.2 Tamanho de Arquivos

A unidade padrão é o bit; um conjunto de 8 bits recebe o nome de byte; Os prefixos K (quilo), M (mega), G(giga), T(tera) são oriundos da matemática; o "K" significa multiplicar por 10^3, o "M" por 10^6 e assim sucessivamente; 

**1 Mb** é igual a **1024k** ou **1.048.676 bytes**; 

### 2.2.3 Arquivo texto e binário

texto pode ter seu conteúdo compreendido pór pessoas; binário só pode ser entendido por computadores e é formado pela compilação: a conversão de linguagem humana para linguagem da máquina; 

## 2.3 Diretório

Local utilizado para armazenar um conjunto de arquivos para melhor organização e localização; Também é case sensitive; Nos sistema Unix/Linux são especificados por uma **/ barra**; 

### 2.3.1 Diretório raiz

Principal diretório do sistema; É representado por uma **/**; ao digitar o comando **cd** acessará este diretório; 

A estrutura de subdiretórios pode ser identificada da seguinte maneira

* **/**
* **/bin**
* **/sbin**
* **/usr**
* **/usr/local**
* **/mnt
* **/tmp 
* **/mnt**
* **/mnt**
* **/tmp**
* **/var**
* **/home**

A estrutura de diretórios também é chamada de _árvore de diretórios_; Eles são armazenados conforme regras definidas pelo _FHS (File System Hierarchy Standard);_ ele define o tipo de arquivo que deve ser armazenado em cada diretório; 

### 2.3.2 Diretório atual 

É o diretório que nos encontramos no momento

~~~bash
pwd
~~~

### 2.3.3 Diretório home

Também conhecido como diretório do usuário; Em sistemas GNU/Linux cada usuário (inclusive o root) possui seu próprio diretório onde poderá armazenar seus programas e arquivos; 

está locallizado em **home/nomedelogin**; Ele também pode ser identificado por um **~**; 

Normalmente, o diretório root está localizado em **/root**; 

A depender do número de usuários do sistema pode ter o seguinte formato: **/home/[1letra_do_nome]/[login];**

### 2.3.4 Diretório superior 

O diretório superior pe identificado por **..**; 

Em **/usr/local**:
~~~bash}
ls ..
~~~
listaria **/usr**;

# 2.3.4 Diretório anterior

O diretório anterior é identificado por **-**; e retorna ao último diretório usado; 

# 2.3.6 Caminho na estrutura de diretórios 

Os diretórios que temos que percorrer para chegar no arquivo ou diretório que procuramos; 

para ver o arquivo **/usr/doc/copyright/GPL** você pode:

~~~bash
cd /usr/doc/copyright
cat GPL
~~~

~~~bash
cat /usr/doc/copyright/GPL
~~~

Na primeira você muda o diretório padrão; na segunda, você continua no diretório atual; 

### 2.3.7 Exemplo de diretório 

Um diretório pode conter outros diretórios; 

### 2.3.8 Estruturas básicas de diretórios do Sistema Linux

O sistema GNU/Linux possui

* **/bin**: com arquivos programas do sistema que são usados com frequência pelo usuário
* **/boot** com arquivos necessários para inicialização do sistema
* **/cdrom** com arquivos pde montagem da unidade CD-ROM
* **/dev** arquivos usados para acessar dispositvos
* **/etc** arquivos de configuração do seu computador local
* **/floppy** montagem de disquetes (saudades) 
* **/home** diretórios contendo arquivos dos usuários
* **/lib** bibliotecas compartilhadas pelos programas do sistema e módulos do kernel
* **/lost+found** gravação de arquivos/diretórios recuperados
* **/mnt** ponto de montagem temporário
* **/proc** sistema de arquivos kernel (não existe em seu disco rigído)
* **/root** diretório do usuário root
* **/sbin** diretórios de programas usados pelo superusuário root para administração
* **/tmp** armazenamento de arquivos temporários criados pelos programas
* **/usr** contém a maior parte dos programas
* **/var** conmtém maior parte dos arquivos que são gravados com frequência pelos programas do sistema

## 2.4 Nomeando arquivos e diretórios

Os arquivos podem ter até 255 letras; 

Os programas executáveis não utilizam extensão **.exe, .com ou .bat**; O GNU/Linux utiliza a _permissão de execução_ para identificar se pode ou não ser executado; 

Evite espaços; 

## 2.5 Comandos

Comandos são ordens que passamos ao sistema operacional para executar uma determinada tarefa; 

É sempre utilizado um espaço depois do comando para uma opção ou paramêtro que será passado ao processamento; 

Um comando pode receber _opções_ e _paramêtros_; 

As opções são utilizadas para controlar como o comando será executado;

Os paramêtros identificam o _caminho, origem, entrada padrão_ ou _saída padrão_ que será passada ao comando; 

* Opção:
~~~bash
ls -a 
~~~

* Paramêtro
~~~bash
ls /usr/doc/copyright
~~~

Comando com opção e paramêtro
~~~bash
ls -a /usr/doc
~~~

### 2.5.1 Comandos internos 

São comandos que estão localizados dentro do interpretador de comandos e não no disco; eles são carregados na memória RAM do computador junto com o interpretador de comandos; 

Exemplos: **cd, exit, echo, bg, fg, source, help**; 

## 2.6 Comandos Externos 

São comandos que estão localizados no disco; eles são procurados no disco usand o **path** e executados assim que encontrados; 

## 2.7 Aviso de comando (prompt) 

Aviso de comando ou prompt é a linha mostrada na tela para a _digitação de comandos_; eles serão passados ao 'interpretador de comandos' para sua execução; 

A posição é marcada com um **-/traço** piscante; O aviso de comando root é identificado com **#**; aviso de comando usuário com **$**; 

Retornar a comandos com digitados com seta para cima ou baixo; 

É possível rolar a tela para baixo ou para cima com **Shift+PGUP** ou **Shift+PGDN**; 

* Backspace e del; 
* **Ctrl+a** move o cursos para o início da linha de comando;   
* **Ctrl+3** move para o final; 
* **Ctrl+u** apaga o conteúdo à esquerda e move para **Ctlr+y**; 
* **Ctrl+k++ apaga o da direita e também copia para **Ctlr+y**; 
* **Ctrl+l** limpa a tela e mantém o texto digitado na linha de comando

## 2.8 Interpretador de comandos

Também conhecido como shell; É o programa responsável em interpretar as instruções enviadas pelo usuário e seus programas ao sistema operacional (o kernel); 

os comandos podem ser 'interativos'; quando passados diretamente ao interpretador e dependem do usuário; 

e também podem ser 'não interativos'; quando são usados arquivos de comandos criados pelo usuário (scripts) para o computador executar; 

os nomes podem ser completados com a tecla **TAB**; 

## 2.9 Terminal Virtual (console) 

Terminal ou console é o teclado e tela conectados em seu computador; O GNU/Linux faz uso de sua caracteristíca multiusuária utilizando terminais virtuais;

Um terminal virtual é a segunda seção de trabalho, independe das outras; podem ser acessadas por computador local ou remoto; 
No GNU/Linux, em modo texto ou gráfico, você pode acessar múltipolos terminais virtuais; 

## 2.12 Curingas 

Curingas ou referência global é um recurso usado para especificar um ou mais arquivos ou diretórios do sistema de uma só vez; 

Ele permite a filtragem do que será listado, copiado, apagado, etc; 

* * Faz referência a um nome completo/restante de diretório 
* **?** Faz referência a uma letra naquela posição 
* **[padrão]** Faz referência a uma faixa de caracteres de um arquivo ou diretório; **[a-z][0-9]** para caracteres de a até z, seguido de 0 até 9, por exemplo; ou, **[a-z][AZ]** para caracteres a até z em caixa alta e baixa
* **[padrão]** também permite a precedência de **^** que faz referência a qualquer caractere, exceto o da expressão; **[âbc]** refere-se a qualqeur caractere menos a,b e c
* **{padrões}** Expande a regra e gera strings para pesquisa de padrões 
* **X{ab,01}** Faz referência a respectiva sequência de caracteres 
* **X{a-z,10}** Faz referência a sequência 'a-z' e X10; 

Estamos em **/usr/teste**; 

Ele contém: **teste1.txt, teste2.txt, teste3;txt, teste4.new e teste5.new** 

Para listar somente a extensão .txt, podemos: 

~~~bash
ls * .txt
~~~

~~~bash
ls teste?.txt
~~~

~~~bash
ls teste [1-3].txt
~~~

Sendo o último o mais eficaz; 

Para listar somente a extensão .new, podemos seguir o mesmo raciocínio: **ls * .new**; **ls teste?.new** e **ls teste[4,5]**; 

Existem outras formas de resolver a questão; a mesma coisa pode ser feita com liberdade de várias maneiras diferentes; 


