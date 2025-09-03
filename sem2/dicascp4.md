Para verificar REDE
Se precisar configurar o kali, faça o seguinte. Abra as configurações das VMs em Rede e altere para que o adaptador seja Host-Only. Subir a máquina Kali e a máquina servidor que o professor liberou.
No Kali os IPs com ip –br –c a:

NOTA: lembre-se do nome das placas de rede (ex: enp0s3)
Rodar o comando netdiscover para descobrir o IP da máquina servidor do professor:
netdiscover -i eth0 -P -r <IPDaNossaMáquinaComFinal.0>/24
Exemplo:
192.168.56.0

Final 1 é roteador, final 100 é DHCP, então 103 é o IP do server que vamos invadir.
No Kali tentar acessar o IP do servidor do professor no navegador, possivelmente deve ter o retorno da página index dele, exemplo de URL para colocar no navegador:
http://<IPservidor>
Nessa página imagino que tenha a dica de qual o nome do login para o servidor dele.


Vá para a pasta /usr/share/wordlists e descompacte o arquivo rockyou.txt.gz (arquivo com as senhas mais comuns)
Gunzip rockyou.txt.gz
Hydra –l <username> -P rockyou.txt ssh://<IPServidor>
(-l é L minúsculo)

Descobrindo a senha é só entrar com SSH (ssh NomeDoLogin@IPdaMaquina). Provável ter arquivo lá com a flag 1, só dar um ls ou coisa do tipo.
Rodar um netstat -tulpn para descobrir os serviços que estão rodando

22 é o SSH que estamos utilizando, 80 é porta padrão, então a que estiver de diferente é o serviço do servidor.
Sabendo qual é a porta do serviço, ele comentou sobre encaminhamento de porta. Faça o seguinte na máquina kali:
ssh –L 8080:localhost:<portaQueRodaOserviço> –p 22 NomeDoLogin@IPdoServidor
(colocar senha que descobriu antes)
Na máquina do Kali acessar um navegador com a URL: (localhost:8080)
Se pelo navegador não funcionar, pode tentar dar um curl:
curl localhost:8080

Ele disse que chave pública e privada pode cair, se pá que vai ser igual foi na GS.
Pra isso, caso você acesse o navegador após o redirecionamento de porta e ainda dê problema, pode ser que precise dar SSH como root no servidor fazendo o redirecionamento.
No caso da GS tinha um arquivo id_rsa_root, acho que estava na home do usuário que você logou. Pra achar é só rodar um ls -lha e ver se tem esse arquivo, pode ser que esteja dentro da pasta oculta .ssh
Quando você tiver o arquivo da chave privada do root, rodar um SCP para passar o arquivo para sua máquina:
scp <ChavePrivada> kali@<IPdoKali>:/home/kali
na home do kali, se não tiver, crie a pasta .ssh:
cd /home/kali
mkdir .ssh
Mover o arquivo para a pasta .ssh:
mv <ChavePrivada> .ssh/
Agora como usuário kali, tentar fazer o SSH utilizando a chave privada:
ssh -i <ChavePrivada> root@<IPdoServer>

PARTE DO PROXY

4 – Ligar o burpsuite no plugin foxyproxy
5 – abrir o burpsuite no kali e ir dando next até chegar na tela onde você clica em proxy. Clicar em intercept on
6 – ir no site e tentar fazer um login aleatório. O burpsuite deve interceptar a tentativa de login. Clicar em Forward-> para liberar o processo de login e ver o retorno do site


7 – No próprio site fala que o login é bee e a senha é bug, mas para aprendizado vamos colocar o username correto com a senha errada. Ao capturar selecionar a parte da senha e clicar com o botão direito (send to intruder)


8 – Na seção Intruder, clique em Clear, Clear All e depois selecione a senha e clique em Add, você verá que adiciona dois caracteres estranhos ao redor da senha selecionada.
9 – Na direita em payloads, clicar em Load..., navegar para /usr/share/wordlists/metasploit e pegar o arquivo http_default_pass.txt. Neste caso a senha de bee não está aí na lista, então vamos adicionar na lista a palavra “bug” apenas para mostrar funcionando. (ele disse que possivelmente vai estar nesse arquivo a senha)
10 – A página que abrir são os testes de login bruteforce. O que retornou 302 é a senha correta, também podemos saber pelo length menor (já que uma resposta de acesso com sucesso costuma ser menor do que uma mensagem de erro no login)
 
