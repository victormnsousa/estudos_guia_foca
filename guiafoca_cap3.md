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


