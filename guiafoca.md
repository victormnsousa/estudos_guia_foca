# Guia Foca GNU/Linux - Versão Iniciante

Gleydson Mazioli da Silva <gleydson@guiafoca.org> 

Versão 3.99 - Julho de 2005

# Introdução 

Foca sinfica _FOnte de Consulta e Aprendizado_ e é dividido em três níveis de aprendizado; 

Neste guia encontraremos:
* textos explicativos sobre o GNU/Linux, seus comandos, arquivos, diretórios, etc;
* Explicações iniciais sobre as partes básicas do computador e periféricos; 
* Comandos e programas equivalentes entre DOS/Windows e GNU/Linux; 
* Material para quem está em primeiro contato com computadores e/ou GNU/Linux; 

Página oficial: <http://www.guifoca.org>  

## 1.1 - Antes de começar 

Os capitúlos _introdução_ e _básico_ contém explicações teóricas sobre o computador e GNU/LInux; 

Dicas: pratique imediatamente o que aprendeu; tenha interesse; não decore; seja curiosa; não desanime; ninguém aprende tudo da noite para o dia; considere atualizações/tempo; você conhecerá mais sobre computadores; existe interface gráfica, mas os melhores recursos estão na linha de comando; peça ajuda a outros usuários GNU/Linux; 

# 1.2 Pré-requisitos

Ter um sistema GNU/Linux instalado; 

# 1.3 Sistema Operacional 

O _sistema operacional_ é o conjunto de programa que fazem a itnerface do usuário e seus programas com o computador; 

# 1.4 O Linux

Criado em 1991, por _Linux Torvalds_ na universidade de Helsink, Finlândia. É um sistema operacional de código aberto distruído gratuitamente pela internet; é mantido e desenvolvido por milhares de pessoas espalhadas pelo mundo; 

## 1.4.1 Algumas caracteristícas do Linux

* É livre e desenvolvido voluntariamente; 
* Convivem sem nenhum tipo de conflito com outros sistemas operacionais; 
* Multitarefa real
* Multiusário
* Suporte a nomes extensos de arquivos e diretórios
* Conecitividade com outros tipos de plataformas; 
* Proteção entre processos executados na memória RAM; 
* Suporte a mais de 63 terminais virtuais; 
* Modularização
* Drivers dos perifiéricos e recursos do sistema podem ser carregados e removidos completamente da memória RAM e ocupam pouco espaço; 
* Não há necessidade de reiniciar o sistema após modificações; somente em casa de instalação de novo hardware; 
* Não precisa de um processador potente para funcionar; 
* Novas versões do sistema não provocam lentidão, pelo contrário;
* Não é requerida licença; 
* Acessa corretamente discos formatados em outras extensões;
* Utiliza permissões de acessos a arquivos, diretórios e programas; 
* Não é vulnerável a vírus; 
* Rede TCP/IP melhorada; 
* Pode rodar aplicações DOS (DOSEMU) ou Windows (wine):
* Suporte a dispostivos infravermelho
* Suporte a rede via rádio amador; 
* Suporte a dispostivos plug-and-play;
* USB, FIrewire, Wirelles, firewwals;
* Roteamento estático e dinâmico de pacotes; 
* Ponte entre redes; 
* Proxy tradicional e transparente; 
* Pode atender mais de um indereço IP na mesma placa de rede;
* Sistema de arquivos organiza-os de maneira inteligente, permitindo multiusuários e gravações intensivas; 
* Permite montagem de servidor web, email e news de baixo custo e alta performance; 
* é possível ver e adaptar o código para sua necessidade; 
* Suporte a dispostivos novos e obsoletos; 
* Utilizado em 10 arquiteturas diferentes; 
* Consultores técnicos especializados ao redor do mundo; 
* Entre outras caracteristícas; 

# 1.5 Distribuições Linux

Só o kernel GNU/Linux não é suficiente para um sistema funcional; existem grupos de pessoas, empresas e organizações que distribuem o Linux junto a outros programas essenciais; este é os significado básico de _distribuição_;

Cada distribuição tem sua caracteristíca própia, como sistema de instalação, objetivo, localização de programas nomes de arquivo de configuração, etc. 

A escolha depende das necessidades de cada um; a escolha não deve ser feita a das suas necessidades; 

# 1.6 Software Livre 

Tradução do t exto Linux e o Sistema GNU de Richard Stallman

O coração do projeto GNU é uma ideia: que o software deve ser livre e que a liberdade do usuário vale a pena ser defendida; 

# 1.7 Processamento de Dados

É o envio de dados ao computador que serão processados e terão um resultado de saída útil; 

# 1.8 O computador 

É uma máquina eletrônica que processa e armazena os dados e pode executar diversos programas para executar uma série de tarefas e atender a necessidade do utilizador; 

O computador não é uma máquina inteligente, apenas executa instruções dos programsa escritos pelo programador; 

# 1.9 Conhecendo o computador

Explicação de gabinete e monitor, será pulado; 

# 1.10 Placa mãe 

É a placa principal do sistema onde estão localizados o processador, memória RAM, Memória Cache, BIOS, CMOS, RTC. Possuí encaixes onde são inseridas placas de extensão; 

## 1.10.1 Alguns componentes da placa mãe

* RAM - Memória de Acesso Aleatório (Randomic Acess Memory) Memória de armazenamento temporário dos programas e depende de uma fonte de energia; 
* Processador: responsável pelo processamento das instruções matemáticas/lógicas e programas carregados na memória RAM; 
* CACHE: Memória de Armazenamento Auxiliar do Processador; Aumenta o desempenho de processamento; 
* BIOS: É a memória _ROM_ que contém as instruções básicas para a inicialização do computador; reconhecimento e ativação dos períféricos conectados a placa mãe; 

# 1.11 Memória do Computador 

A memória é a parte do computador que permite o armazenamento de dados; 

## 1.11.1 Memória Principal

Depende de fonte de energia, tendo a RAM como principal exemplo

## 1.11.2 Memória AUxiliar

São dispostivos que não dependem de fonte de energia para manter dados armazenados, como discos rígidos; 

# 1.16 - Desligando o computador

**shutdown -h**
**halt**
**poweroff" 

# 1.17 - Reiniciando o computador

**reboot** 
**shutdown -r now**

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

# Capítulo 3

O capítulo 3 é dedicado a usuários MS-DOS e Windows que desejam migrar de sistema operacional; por uma questão de desatualização, será ignorado neste estudo; 

# 4. Discos e Partições

## 4.1 Partições

São divisões existentes no disco rígido que marcam onde começa e onde termina um sistema de arquivos; por isso, podemos usar mais de um sistema operacional no mesmo computador; ou dividir o disco rígido em uma ou mais partes no mesmo sistema opercional; 

## 4.4 Identificação de discos e partições em sistemas Linux

No GNU/Linux, os dispostivos existentes em seu computador são identificados por um arquivo referente a este dispostivo no diretório **/dev**; 

A identificação é feita da seguinte maneira: 

**/dev/hda1**

Por ordem:
* diretório onde são armazenados os dispostivos
* sigla que identifica o tipo de disco rígido (hd=ide, sd = scsi)
* letra que identifica o disco rígido (a=primeiro, b=segundo, etc)
* Número que identifica o qual a partição do disco rígido

## 4.5 Montando (acessando) uma partição de  disco

Você pode acessar uma partição de disco usando o comando **mount**; 

**mount[_dispostivo_][_ponto de montagem_][_opções]; 

* _dispostivo_ é a identificação da unidade de disco/partição que deseja usar **/dev/hda1**, por exemplo
* _ponto de montagem_ é o diretório de onde _a unidade de disco/partição_ será acessado; ele deve estar vazio; normalmente é utilizado o diretório **/mnt**
* **-t** [_tipo_] é o tipo de sistema de arquivos usados pelo _dispostivo_
* **-r** especificada monta a partição somente para leitura
* **-w** especificada monta a partição como leitura/gravação; é o padrão

Existem outras opções que podem ser encontradas no manual de mount **man mount**; 

O comando **mount** sem parâmetros mostra os sistemas de arquivos montados no sistema; 

### 4.5.1 fstab

O arquivo **/etc/fstab** permite que as partições do sistema sejam montadas facilmente especificando somente o dispostivo ou ponto de montagem; 

Ele contém parâmetros sobre as partições que são lidas pelo comando **mount**; Cada linha deste arquivo, contém a partição que desejamos montar, o pontp de montagem, o sistema de arquivos e outras opções;

Tem o seguinte formato:

_Sistema de arquivos_ _Ponto de montagem_ _Tipo_ _Opções_ dump ordem
/dev/hda1               /                   ext2   defaults  0   1

* _Sistema de arquivos_ é a partição qeu deseja montar;
* _Ponto de montagem_ é o diretório do GNU/Linux onde a partição montada será acessada; 
* _Tipo_ é o tipo de sistema de arquivos usado na partição que será montada; 
* _Opções_ especifica as opções usadas com o sistema de arquivo
    * defaults (valor padrão; 
    * noauto não monta o sistema de arquivos
    * ro - monta somente leitura
    * user - Permite que usuários montem o sistema de aruivos
    * sync - para discos removivéis
* _dump_ especifica a frequência de backup com o programa dump; 0 desativa
* _Ordem_ define a ordem que os sistemas de arquivo serão verificados; se usar 0 não é verificado; 

Depois é só digitar o comando **mount/dev/hdg**

## 4.6 Desmontando partição

Para desmontar um sistema de arquivo utilize o comando **umount** com permissões de root; 

**umount[_dispostivo_/_pontodemontagem_]** 

Vocẽ pode usar **umount /dev/hda1** ou **umount/mnt** para desmontar um sistema de arquivos **/dev/hda1** montado em **/mnt**; 

# 5. Execução de programas 

## 5.1 Executando um comando/programa

Para executar o comando, é necessário permissões de execução e que esteja no caminho de procura de arquivos; 

No aviso de comando **#/root** ou **$/usuário** digite o nome do comando e tecle Enter; O programa/comando é executado e recebe um número de identificação **PID**; 

## 5.2 path

Path é o caminho de procura dos arquivos/comandos executáveis e é armazenado na variável de ambiente **PATH**; 

para ver o conteúdo: **echo $PATH**; 

O caminho dos arquivos vem configurado na instalação, mas pode ser alterado em **/etc/profile**; 

## 5.3 Tipos de execução de comandos/programas 

Um programa pode ser executado de duas formas:

1- Primeiro plano, também chamado de _foreground_; quando você deve esperar o término da execução para dar um novo comando; 

2- Segundo plano ou _background_; quando você não precisa esperar o término da execução para dar um novo comando; para ele é apresentado um processo PID; 

## 5.4 Executando programas em sequência

Os comandos podem ser executados em sequência, separados por **;**

# 5.5 ps 

É útil saber quais processos estão sendo executados no computador; 

O comando **ps** mostra os processos, usuários e hora inicial, etc; 

**ps [opções]**

* a 
mostra os processos criados por você e de outros usuários
* x 
mostra processos que não são controlados pelo terminal 
* u 
mostra o nome do usuário que iniciou o processo e a hora que o processo foi iniciado
* m
mostra a memória ocupada porcada processo
* f 
mostra a árvore de execução dos comandos
* e 
mostra as variáveis de ambiente no momento da inicialização do processo
* w 
mostra a continuação da linha atual na próxima linha 

O **ps** não precisa de **- hífen**; não utiliza opções longas e não tem parâmetros; 

## 5.6 top

Mostra os programas usados ativos, parados, tempo na CPU, detalhes da Memória, disponibilidade, etc. 

**top[opções] **

* -d[tempo] 
atualiza a tela após o tempo em segundos
* -s 
Diz ao top para ser executado no modo seguro
* -i
inicia o top ignorando o tempo de processos zumbis
* -c 
mostra a linha de comando ao invés do nome do programa
* 'espaço' 
atualiza a tela imediatamente
* 'ctrl + l
apaga e atualiza a tela
* k 
finaliza um processo
* n 
muda o número de linhas mostrado na tela

## 5.7 Controle de execução de processos

### 5.7.1 Interrompendo a execução de um processo

Pressionar Ctrl+c ou **kill**

### 5.7.2 Parando momentaneamente a execução de um processo

Pressionar Ctrl+z; ele será pausado e será mostrado o número de seu processo; 

Para retornar, consulte **fg** ou **bg**; 

### 5.7.3 jobs

Mostra os processos que estão parados ou rodando em _segundo plano_; eles são iniciados usando **&** no final do comando ou por **bg**

### 5.7.4 fg

Permite que um programa em segundo plano ou parado, rode em primeiro plano; É necessário usar o comando **jobs** para ter o número do processo;

**fg[número]**  

### 5.7.5 bg 

Permite um programa em primeiro plano ou parado rodar em segundo pĺano; é necessário primeiro interromper a execução do comando com ctrl+z; com o número da tarefa interrompida, é possível rodar **bg[número]** em segundo plano; 

### 5.7.6 kill

Sinal de término ao processo sendo executado; 

**kill[_opções_][_sinal_][_número_]** 

* número é a identificação do processo que pode ser obtida com **ps**; também aceita o **%** de **jobs**
* sinal que será enviado ao processo; -15 omitido padrão 
* opções, -9 destruição, terminado sem chances de salvar ou apagar arquivos temporários

Exemplos: 

**kill 500**
**kill -9 500**
**kill %1**

### 5.7.7 killall

Permite finalizar processos pelo nome; 

**killall[_opções_][_sinal_][_processo_]

* processo é o nome do processo que deseja finalizar
* sinal que será enviado ao processo (pode ser obtido usando a opção -i
* opções
    * - i pede confirmação sobre a finalização do processo
    * -l lista o nome de todos os sinais conhecidos
    * -q ignora a existência do processo
    * -v retorna se o sinal foi enviado com sucesso ao processo
    * -w finaliza a execução do killall somente após finalizar todos os processos

### 5.7.8 killall5

Sinal de finalização para todos os processos executados; 

**kill all[_sinal_]** 

### 5.7.9 Sinais do sistema 

conferir man signal

## 6.1 ls

**ls[opções][caminho/arquivo]** 

opções

consultar man ls para todas as funções

## 6.2 cd

Entra em um diretório

**cd[_diretório_]**

* cd sem parâmetros ou **cd ~** retorna ao diretório home
* **cd/** retorna ao diretório raiz
* **cd-** retorna ao diretório anteriormente acessado
* **cd..** sobe um diretório
* **cd../[diretório]** sobe um e entra no especificado

## 6.3 pwd 

Mostra o nome e caminho do diretório atual 

## 6.4 mkdir

Cria um diretório nmo sistema; 

**mkdir[_opções_][_caminho/diretório_][_caminho1/diretório1_]**

## 6.5 rmdir

Remove um diretório do sistema 

**rmdir[_caminho/diretório_][_caminho1/diretório1]

(em ambos é possível criar/remover mais de um diretório) 

* é necessário estar um nível acima do diretório que será removido
* é necessário usar **-r** para remover diretórios com arquivos

# 7 Comandos para manipulação de arquivos 

## 7.1 cat 

Mostra o conteúdo de um arquivo binário ou texto

**cat[_opções_][_diretório/arquivo_][_diretório/arquivo_]**

* **-n, --number** mostra o número das linhas
* **-s, --squeeze-blank** não mostra mais que uma linha em branco entre parágrafos
* **zcat** para ver arquivos compactados como gzip

## 7.2 tac 

Mostra o conteúdo de um arquivo binário ou texto, só que com a ordem inversa

**tac[_opções_][_diretório/arquivo_]**

* **-s [string]** Usa _string_ como separador de registros

## 7.3 rm

Apaga arquivos, também pode ser usado para apagar diretórios e sub (vazios e com arquivos)

**rm[_opções_][_caminho_][_arquivo/diretório_]**

* se omitido o caminho, assume o diretório atual
* **-i,--interactive** pergunta antes de remover
* **-v,--verbose** mostra os arquivos na medida que são removidos
* **-r,--recursive** é usado para remover arquivos em sub-diretórios ou subdiretórios
* **-f, --force** remove os arquivos sem perguntar
* **--arquivo** remove os arquivos que contém caracteres especiais; funciona com todos os comandos do shell e permite caracteres especiais como *, **?**, **-** sejam interpretados; 

## 7.4 cp

Copia arquivos 

**cp[_opções_][_origem_][_destino_]**

* **i, --interactive** pergunta antes de substituir um arquivo existente
* **-f,--force** não pergunta e substitui
* **-r** copia arquivos dos diretórios e subdiretórios da origem para destino; é recomendado usar **-R**
* **-R,--recursive** copia arquivos e subdiretórios, mas também os arquivos especiais FIFO e dispositivos
* **-v,--verbose** mostra os arquivos enquanto estão sendo copiados
* **cp* /tmp** copia todos os arquivos do diretório atual para **/tmp**

## 7.5 mv

Move ou renomeia arquivos e diretórios; o arquivo de origem é apagado

**mv[_opções_][_origem_][_destino_]**

* **-f,--force** substitui o arquivo de destino sem perguntar
* **-i,--interactive** pergunta antes de substituir (é o padrão)
* **-v,--verbose** mostra os arquivos que estão sendo movidos

# 8 comandos diversos

## 8.1 clear

Limpa a tela e posiciona o cursor

**clear**

## 8.2 date

Permite ver/modificar a data e hora do sistema

**man date**

## 8.3 df

Mostra o espaço livre e ocupado de cada partição

**df[_opções_]

* **-a** inclui sistemas de arquivos com 0 blocos
* **-h** mostra o espaço livre ocupado em MB,KB,GB ao invés de blocos
* **-H** usa 1000 ao invés de 1024 como unidade de medida
* **-k** lista em kbytes
* **-l** somente lista sistema de arquivos locais
* **-m** lista em mbytes

## 8.4 ln

Cria links para arquivos e diretórios no sistema. Trata-se de um mecanismo quei faz referência a outro arquivo ou diretório em outra localização; ele cria referências reais, possibilitando cópia do link(arquivo alvo), entrar em diretório, etc; 

**ln[_opções_][_origem_][_link]

* _link_ é o nome do link que será criado
* **-s** cria um link simbólico; usado para criar ligações com o arquivo/diretório de destino
* **-v** mostra o nome de cada arquivo antes de fazer o link
* **-d** cria um hardlink para diretórios; somente para root

Existem dois tipos de links:

Os links _simbólicos_ criam um arquivo especial no disco (do tipo link) que tem como conteúdo o caminho para chegar até o arquivo alvo; 
Já os _hardlink_ fazem referência ao mesmo inodo do arquivo original, ele será idêntico ao original, inclusive nas permissões; 
Não é possível fazer um hardlink para um diretório ou fazer referência a arquivos que estejam em partições diferentes; 

Observações: Se for usado o comando **rm** com um link, somente o link será removido; no comando **cp**, somente o arquivo original será copiado; no comando **mv** com um link, a modificação será feita no link;; se for usado um comando de visualização, como **cat**, o arquivo original será visualizado; 

Exemplos: **ln -s /dev/ttyS1i /dev/modem** cria o link **/dev/modem** para o arquivo **/dev/ttyS1
**ln -s /tmp ~/tmp** cria um link **~/tmp** para o diretório **/tmp**

## 8.5 du

Mostra o espaço ocupado por arquivos e sub-diretórios do diretório atual

**du[_opções_]

* **-a,--all** mostra o espaço ocupado por todos os arquivos
* **-b,--bytes** mostra o espaço ocupado em bytes
* **-c,--total** faz uma totalização de todo espaço listado
* **-D** não conta links simbólicos
* **-h, --human** mostra em formato legível ao invés de blocos
* **-H** usa 1000 e não 1024 como unidade
* **-k** mostra o esppaço ocupado em kbytes 
* **-m** mostra o espaço ocupado em mbytes
* **-S,--separate-dirs** não calcula o espaço ocupado por sub-diretórios

## 8.6 find

Procura por arquivos/diretórios no disco; a busca pode ser realizado por data de modificação, tamanho, etc; o programa utiliza _opções_ longas; 

**find[_diretório_][_opção/expressão_]**

* **-name [expressão]** procura pelo nome _expressão_ nos arquivos e diretórios processados
* **-depth** processa subdiretórios primeiro antes do diretório principal
* **-maxdepth[num]** faz procura de até _num_ sub diretórios dentro diretório pesquisado
* **mindepth[num]** não faz nenhum procura em diretórios menores que o _num_ de níveis
* **mount,-xdev** não faz pesquisa em sistemas de arquivos diferentes daquele onde o comando foi executado
* **size[num]** procura por arquivos que tiverem o tamanho _num_; _num_ pode ser antecedido de + ou - para especificar um arquivo maior ou menor que _num_; a opção size ainda pode ser seguida de:
    * **b** especifica o tamanho em blocos de 512 bytes(padrão do comando)
    * **c** especifica o tamanho em bytes
    * **k** especifíca o tamanho em kbytes
* **-type[_tipo_]** procura por arquivos do _tipo_ especificado, são aceitos:**b-bloco**, **c-caractere**, **d- diretório**, **p-pipe**, **f-arquivo regular**, **l-linksimbólico** e **s-sockete**; 
* a maior parte dos arquivos númericos pode ser precedido por + ou -;

Exemplos:
~~~bash
find / -name grep
~~~
Procura no diretório raiz e subdiretórios um arquivo/diretório chamado **grep**; 

~~~bash
find / -name grep -maxdepth 3
~~~
Procura no diretório raiz e subdiretórios até o terceiro nível um arquivo chamado **grep**

~~~bash
find . -size +100k
~~~
Procura no diretório 

## 8.7 free

Mostra detalhes sobre a utilização da memória RAM do sistema

**free[opções]**

* **-b** mostra os resultados em bytes
* **-k** mostra os resultados em kbytes
* **-m** mostra os resultados em mbytes
* **-o** oculta a linha de buffers
* **-t** mostra uma linha contendo o total
* **-s[num]** mostra a utilização de memória a cada _num_ segundos
* o **free** é uma interface do arquivo **/proc/meminfo**

# 8.8 grep

Procura por um texto dentro de um arquivo(s) ou no dispostivo de entrada padrão 

**grep[_expressão_][_arquivo_][_opções_]**

* _expressão_ é a palavra ou frase que será procurada no texto; é possível identificá-la com aspas
* **-A[num]** mostra o _número_ de linhas após a linha encontrada pelo grep
* **-B[num]** mostra o _num_ de linhas antes da expressão encontrada
* **-f[arquivo]** especifica o arquivo que o texto será procurado
* **-h,--no-filename** não mostra os nomes dos arquivos durante a procura
* **-i,--ignore-case** ignora as diferenças entre maiúsculas e minúsculas na busca
* **-n,--line-number** mostra o nome de cada linha encontrada pelo grep
* **-U,--bynary** trata o arquivo que será procurado como binário
* se um arquivo não for especificado ou se for usado uma hífen, **grep** faz sua pesquisa no dispositivo de entrada padrão

## 8.9 head

Mostra as linhas iniciais de um arquivo de texto

**head [_opções_]**

* **-c[número]** mostra o _número_ de bytes do inicio do arquivo
* **-n[_num_]** mostra o _número_ de linhas do inicio do código
* se não for especificado, **head** mostra as 10 primeiras linhas

## 8.10 nl

Mostra o número de linhas junto com o conteúdo de um arquivo

**nl [_opções_] [_arquivo_]

* **-f[opc]** faz a filtragem de saída de acordo com a opção
    * **a** número todas as linhas
    * **t** não númera as linhas
    * **n** numera as linhas vazias
    * **texto** numera somente linhas que contém o _texto_
* **-v[num]** número inicial (o padrão é 1)
* **-i[num]** número de linhas adcionadas a cada linha do arquivo (o padrão é 1) 
* exemplos: **nl /etc/passwd** , **nl -i 2 /etc/passwd**

# 8.11 more

Permite fazer a páginação de arquivos ou da entrada padrão; O comando pode ser utilizado para leitura de arquivos que ocupem mais de uma tela; Permite o uso de **enter** ou **espaço** para continuar avançando no arquivo; pressione **q** para sair; 

**more [_arquivo_]**

# 8.12 less

Permite fazer a páginação de arquivos ou da entrada padrão; Também usado para leitura de arquivos que ocupem mais de uma tela; Permite a utilização de setas ou **pgup/pgdown** para rolamento de página; 

**less [_arquivo_] 

# 8.13 sort

Organiza as linhas de um arquivo texto ou da entrada padrão;

**sort [_opções_] [_arquivo_]

* **-b** ignora as linhas em branco
* **-d** somente usa letras, digitos e espaços durante a organização
* **-f** ignora as diferenças entre maiúsculas e minúsculas
* **-r** inverte o resultado da comparação
* **-n** organiza os números na ordem aritmética
* se o **-n** não for utilizado o arquivo será organizado por listagem alfabética e númerica, sequencialmente
* **-c** verifica se o arquivo já está organizado
* **-o _arquivo_** grava a saída de sort no _arquivo_ 

Exemplos:

* **sort texto.txt** organiza o texto em ordem crescente
* **sort texto.txt -r** organiza o conteúdo do arquivo em ordem decrescente
* **cat texto.txt | sort** faz a mesma coisa que o primeiro, mas a saída do comando **cat** é redirecionada a entrada padrão de **sort**
* **sort -f texto.txt** ignora as diferenças entre letras maiúsculas e minúsculas durante a organização

## 8.14 tail

mostra as linhas finais de um arquivo de texto;

**tail [_opções_] 

* **-c [número]** mostra o _número_ de bytes do final do arquivo 
* **-n [número]** mostra o _número_ de linhas de final de arquivo

## 8.15 time

Mede o tempo gasto para executar um processo/programa;

**time [_comando_]**

## 8.16 touch

Muda a data e hora que um arquivo foi criado; também pode ser usado para criar arquivos vazios; quando usado em arquivos que não existem, cria um novo; 

**touch [_opções_] [_arquivos_] 

* **-t MMDDhhmm[Ano.Segundos]** usa minutos _MM_, dias _DD_, horas _hh_, minutos _mm_ e,opcionalmente, o ano e segundos para modificação dos arquivos ao invés da data e hora atual
* **-a,--time=atime** faz o **touch** mudar somente a data e hora do acesso ao arquivo
* **-c,--no-create** não cria arquivos vazios, caso os arquivos não existam
* **-m.--time=mtime** faz o **touch** mudar somente a data e hora da modificação
* **-r [arquivo]** usa as horas no _arquivo_ como referências ao invés da hora atual

## 8.17 uptime

Mostra o tempo de execução do sistema; 

**uptime**

## 8.18 dmesg

Mostra as mensagens de inicialização do kernel. São mostradas as mensagens da última inicialização do sistema;

**dmesg | less**

## 8.19 mesg

Permite ou não recebimentos de requisições de **talk** de outros usuários; 

**mesg[_y/n_]**

* **y** permite que você recebe **talks** de outros usuários
* **n** permite envio mas recusa recebimento

## 8.20 echo

Mostra mensagens; utilizado para construção de scripts para mostrar mensagens na tela para o usuário acompanhar;

**echo [mensagem]**

A opção **-n** pode ser usada para que não ocorra o salto de linha após a mensagem ser mostrada;

## 8.21 su

Permite o usuário mudar sua identidade para outro usuário sem fazer o logout; útil para executar programas ou comandos como root;

**su [usuário]**

Se não for digitado, é assumido o usuário root; será exigida senha; **exit** para sair; 

## 8.22 sync

Grava os dados do cache de disco na memória RAM para todos os discos rígidos e flexíveis do sistema; O cache é um mecanismo de aceleração que permite que um arquivo seja armazenado na memória e não imediatamente gravado no disco; e assim utilizar toda memória RAM disponível acelerando o desempenho de leitura e gravação; 

**sync** 

## 8.23 uname

Retorno o nome e versão do kernel atual;

**uname**

## 8.24 reboot

reinicia o computador; 

**reboot**

## 8.25 shutdown

Desliga/reinicia o computador imediatamente ou de maneira programável de forma segura; todos os usuários do sistema são avisados; só pode ser executado pelo root ou quando é usada a opção **-a** pelos usuários cadastrados em **/etc/shutdown.allow**; 

**shutdown [_opções_] [_hora_] [_mensagem_]**

* **-h** inicia o processo para desligamento do computador
* **-r** reinicia o sistema
* **-c** cancela a execução de shutdown, é possível acrescentar mensagem
* o shutdown envia uma mensagem a todos usuários alerta sobre 15 minutos para o desligamento
* é recomendado utilizar o símbolo **&** no final da linha de comando para execução em segundo plano
* em 5 minutos, o **login** é desativado

## 8.26 wc 

Conta o número de palavras, bytes e linhas em um arquivo ou entrada padrão; se as opções forem omitidas, o **wc** mostra a quantidade de linhas, palavras e bytes; 

* **-c,--bytes** mostra os bytes do arquivo
* **-w,--words** mostra a quantidade de palavras do arquivo
* **-l,--lines** mostra a quantidade de linhas do arquivo
* a ordem da listagem dos parâmetros é única; modificar a posição das opções não modifica a ordem da listagem

## 8.27 seq

Imprime um sequência de números começando em _primeiro_ e terminando em _último_, com _imcremento_ para avançar 

**seq [_opções_] [_primeiro_] [_incremento_] [_ultimo_] 

* _primeiro_ é o número inicial da sequência 
* _incremento_ é o número utilizado para avançar na sequência
* _último_ é o número final da sequência
* **-f,--format [formato]** formato de saída dos números da sequência; utilizar o estilo do printf para ponto flutuante %g padrão
* **-s, --separator [string]** usa _string_ para separar a sequência de números, padrão /n
* **-w, --equal-width** insere zeros na frente dos números, mantendo a sequência alinhada; 

# 9 comandos de rede

## 9.1 who 

Mostra quem está atualmente conectado no computador; lista o nome de usuários, terminal e data da conexão; 

**who [_opções_]** 

* **-H,--heading** mostra o cabeçalho das colunas
* **-i, -u,--idle** mostra o tempo que o usuário está parado em Horas:Minutos
* **-m, i am** mostra o nome do computador e usuário associado ao nome
* **-q, --count** mostra o total de usuários conectados aos terminais
* **-T, -w,, --mesg** mostra se o usuário pode receber mensagens via **talk**
    * **+** o usurio recebe; **-**osuário não recebe; **?** não é possível determinal

## 9.2 Telnet

Permite acesso a um computador remoto; é mostrada uma tela de acesso correspondente ao local onde deve ser feita a autenticação do usuário; 

**telnet [_opções] [_ip/dns_] [_porta_]

* **-8** requisita uma operação binária de 8 bits; por padrão, **telnet** não usa 8 bits
* **-a** tenta um login automático a partir do ambiente user
* **-d** ativa o modo de debug
* **-r** ativa a emulação de rlogin
* **-l [usuário]** faz a conexão usando _usuário_ como nome de usuário

## 9.3 finger 

Mostra detalhes sobre os usários de um sistema;

**finger [usuário] [usuário@host]

* **-l** mostra os detalhes de todos os usuários conectados no momento
* **-p** Não exibe o conteúdo dos arquivos **.plan** e **.project**
* sem parâmetros, mostra os dados de todos usuários conectados

## 9.4 ftp 

Permite a transferência de arquivos do computador remoto/local e vice versa; requer autenticação do usuário; uma vez conectado pode usar a maioria dos comandos GNU/Linux; 

**ftp [ip/dns]**

* **ls** lista arquivos do diretório atual
* **cd _diretório_** entra em diretório
* **get _arquivo_** copia um arquivo do servidor ftp para o computador local; é gravado no diretório onde o programa foi executado; 
* **hash _on/off_** quando ligada faz com que o caractere **#** mostre o progresso do download
* **mget _arquivos_** semelhante ao get, mas copia diversos arquivos e permite o uso de coringas
* **send _arquivo_** envia arquivo para o diretório atual do servidor FTP(é necessário permissão de gravação); 
* **prompt _on/off_** ativa ou desativa pergunta para a cópia de arquivo; _off_ pressupõe sim

## 9.5 whoami

Mostra o nome que usou para conectar-se ao sistema

**whoami**

## 9.6 dnsdomainname

Mostra o nome do domínio de seu sistema

## 9.7 hostname

Mostra ou muda o nome de seu computador na rede

## 9.8 talk

Inicia conversa com outro usuário em uma rede local ou Internet

PÁGINA 90
  




















 
