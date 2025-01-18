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


