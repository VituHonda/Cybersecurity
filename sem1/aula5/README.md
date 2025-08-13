Atualizar pacotes do linux

apt update

Verificar portas abertas

netstat -nltp

ss -nltp

Instalar apache

apt install apache2

Ligando, parando e restartando servidor apache

service apache2 start

service apache2 stop

service apache2 restart

Remover index.html de um servidor apache no python também mostra todos os arquivos

Servidor apache sem index.html mostra muita informação
- ip
- porta
- versão
- SO

Pasta de configuração do servidor

no caso do apache2

cd /etc/apache2/

Pasta de segurança do apache

cd conf-enabled/security.conf

Desligar

ServerTokens Prod

ServerSignature off

Log do servidor
cd /var/log/apache2
access.log

Pegar pedaços do log
head/tail -n numeroDeLinhas nomeDoArquivo
head -n 3 access.log
