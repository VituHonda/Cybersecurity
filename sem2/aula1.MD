# Configurações

CLIENTE:
nat - dhcp
bridge - dhcp
interna - static 192.168.100.10/24

SERVIDOR:
nat - dhcp
bridge - dhcp
interna - static 192.168.100.20/24

###

host-only - depois

###

Depois de configurar as 3 placas das 2 maquinas

desligar bridge e interna - das duas maquinas
criar quarta placa host-only - atualizar mac

verificar se esta ok em tools - network
properties -> dhcp server

abrir maquina owasp - só abrir

kali linux - host-only

# NETDISCORD

no kali - netdiscover --help

descobriu ips dentro da rede dentro do adapter eth0

-i eth0 -P -r 192.168.56.0/24

no navegador do kali colocar o ip 192.168.56.103

OBS: na maquina do owasp se tentar bater no ip pode ser que o firewall bloqueie caso isso aconteça reiniciar a maquina da owasp

no site clicar em "bWAPP"

CP01 - é esse desafio


