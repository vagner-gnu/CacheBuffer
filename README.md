# CacheBuffer

Objetivo é criar script para fazer a limpeza da memória cache automaticamente.

Acesse o diretório /home/user,

Depois crie o arquivo CacheBuffer.sh

#nano CacheBuffer.sh

Adicione o conteudo do arquivo CacheBuffer.sh

Salve Ctrl+x

Permissão 
#chmod +x CacheBuffer.sh

Adicione o agendamento de execução a cada 12 horas.

#nano /etc/crontab

0 */12 * * * root /home/user/./CacheBuffer.sh

Salve Ctrl+x
