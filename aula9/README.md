- lado do servidor
nano /etc/ssh/sshd_config.d
service ssh restart

- lado do cliente
ip do servidor
ssh aluno@192.168.10.20 -p 2244

- lado do servidor

![image](https://github.com/user-attachments/assets/4b51ffd7-8910-4f44-9661-760cda38a01e)

permit root login 

strict mode - tempo para deslogar automaticamente
max auth - quantidade maxima de tentativas de login
max sessions - maximo de usuarios conectados

- permitir logar como root
- 
![image](https://github.com/user-attachments/assets/64047867-34ee-44e6-a0af-2485a976203c)

service ssh restart

- lado do cliente
trocar para aluno com
su aluno
cd /home
cd

![image](https://github.com/user-attachments/assets/3f39b20b-0119-4fdc-9388-a70ee0a50b57)

criando chave publica 
ssh-keygen -t rsa

![image](https://github.com/user-attachments/assets/2e6e0148-e6cb-4c58-8d86-0713fe124890)

chaves
entrar
cd .ssh

![image](https://github.com/user-attachments/assets/eaadb680-ded3-4018-b1ec-1b9789163e0e)

abrir chaves
cat nome do arquivo
  
- lado do servidor

criar chave ssh

- lado do cliente

ssh-copy-id aluno@192.168.10.20

![image](https://github.com/user-attachments/assets/5ead0134-37a1-4aab-abfe-73ff3f6d4301)

- lado do servidor
  
verficar se a chave chegou

![image](https://github.com/user-attachments/assets/d79d65ee-41cd-4ac9-9833-e99f1cc16f2f)


- lado do cliente

logar no servidor

![image](https://github.com/user-attachments/assets/1c34aaf0-858b-47e3-b218-b253698b6426)

vai logar sem pedir senha por conta da chave ssh

# Ataque força bruta

criar dois wordlists 1 para user 1 para password

nano nomedoarquivo

precisar instalar dependencia, no cali linux n precisa
apt install hydra -y

cd /home/aluno

![image](https://github.com/user-attachments/assets/a5772638-8676-4131-a01d-27012275e6ba)

![image](https://github.com/user-attachments/assets/7ab8c3c5-fdca-4fa4-b8d8-de3990ffca9b)

# Trabalho

- redirecionamento de porta com ssh

como cliente normalmente acessa a porta 80 que é internet e ve o site
objetivo - usando ssh para acessar a porta 8080 que é a intranet

pesquisar como fazer de forma local

ssh -L 1234:localhost:7070 aluno@192.168.10.50

prints
porta 80 
porta do servidor logado e deslogado

# Maldades

shodan.io - mostra portas abertas ao redor do mundo
