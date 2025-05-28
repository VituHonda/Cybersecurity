# configurar placas de rede - nomes iguais entre servidor e cliente

- INTERNA

allow-hotplug eth0
iface eth0 inet static
address 192.168.10.10/24

- BRIDGE

allow-hotplug eth1
iface eth1 inet dhcp

# SSH

- ssh normal

ssh user@ip
ssh aluno@192.168.10.10

- ssh mandando chave publica
  
ssh-copy-id aluno@192.168.10.10
Salva a sua chave publica no servidor que esta fazendo ssh ai n precisa mais colocar senha

- ssh para portas diferentes

ssh aluno@192.168.10.10 -p numeroDaPorta
adicionar -p caso a porta seja diferente de 22

- ssh com redirecionamento de porta local

ssh -L porta:localhost:portaRemota aluno@192.168.10.10
  
# HYDRA

hydra -L user.txt -P pass.txt ssh://192.168.10.10

provavel usar rockyou.txt

L minusculo para quando usar o proprio user, maiusculo para uma wordlist
mesma coisa para senhas
  
# CURL

- GET 

curl ip

- HEAD

curl -I ip

