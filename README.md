# CacheBuffer

Objetivo é criar script para fazer a limpeza da memória cache automaticamente.

Acesse o diretório /home/user,

Depois crie o arquivo CacheBuffer.sh

#nano CacheBuffer.sh

Adicione:

############################################
#  Objetivo: Limpeza Cache/Buffer e SWAP   #
#  Autor: Vagner Carvalho                  #
#  Data Criacao: 08/09/2019                #
#  Ultima Alteração: 08/09/2019            #
############################################

#!/bin/bash

############################################
echo "Limpeza Cache/Buffer e SWAP"

#Para limpar tudo: Cache/Buffer, Dentries e Inodes:
sudo -i
sync; echo 3 > /proc/sys/vm/drop_caches

#Para limpar o espaço, SWAP:
sudo -i
swapoff -a && swapon -a

echo "Finalizado Limpeza Cache/Buffer e SWAP"
############################################

Salve Ctrl+x

Permissão 
#chmod +x CacheBuffer.sh

Adicione o agendamento de execução a cada 12 horas.

#nano /etc/crontab

0 */12 * * * root /home/user/./CacheBuffer.sh

Salve Ctrl+x
