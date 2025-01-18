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


