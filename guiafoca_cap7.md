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


