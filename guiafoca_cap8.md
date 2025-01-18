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


