## Placas de rede

ver ip NAT -> ip -br -c a

testar acesso a internet usar -> ping

### Configuração segundo adapter de rede

settings 
selecionar segundo adapter
habilitar o adapter
colocar o tipo de rede como bridge
dar refresh no MAC address
ok

obs: por padrão a placa de rede ver desabilitada tem que ligar

Abrir interface de rede -> nano /etc/network/interfaces

na interface configurar o segundo adapter

"#" coloca comentario na interface
allow-hotplug enp0s8
iface enp0s8 inet dhcp
salvar -> ctrl + o
sair -> ctrl + x

ifup nomeDaRede
obs: da pra ver o nome da rede vendo o ip

tentar pingar e apertar ctrl+c para parar

### Configuração terceiro adapter de rede

habilitar o terceiro adapter
dar o nome de fiap
dar refresh no MAC address

allow-hotplug enp0s8
iface enp0s8 inet static
address 192.168.100.10/24

obs: o /24 ao final -> netmask 255.255.255.0 mais facil usar o /24

ifup nomeDaRede

### Clonar vm
settings
trocar o nome para servidor

dentro de cd / -> criar o servidor

python3 -m http.server 1234

## Dica
- conteudo do CP1: Aula4 e permissões
- configurar placa de rede é um requisito pro CP1
- cp01:
Abrir um arquivo txt com uma mensagem no navegador sem mostrar a msg
