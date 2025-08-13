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

