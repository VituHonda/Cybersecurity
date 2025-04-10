# ips das vms interna

  192.168.100.10
  
  192.168.100.20

# instalar pacotes

apt install curl

apt install netcat

apt install net-tools

apt install apache2

# comando para ver as info de um pacote
- Netcat - precisa abrir a porta e ver se tem conexao
  man nc | less
-ascii
  man ascii
  -curl - ele so envia a requisição
  man curl | less

- Abrir porta na porta 80
nc -v 127.0.0.1 80

Fazer requisição get
GET / HTTP/1.0

Fazer requisição com HEAD

- printar string
printf "HEAD / HTTP/1.0\r\n\r\n"
HEAD / HTTP/1.1

- Enviando string para o servidor
- printf "HEAD / HTTP/1.0\r\n\r\n" | nc -v 127.0.0.1 80

- chamar um site
curl https://www.fiap.com.br/

curl ifconfig.me

cp02
ip da maquina
print da flag
sao 7 flags

1 - GET 

![image](https://github.com/user-attachments/assets/90076200-5ad5-410e-8715-b2fe16729e3f)

2 - HEAD 

![image](https://github.com/user-attachments/assets/42ffd6a5-b3c7-449b-b0de-f0901a1e5a0d)

![image](https://github.com/user-attachments/assets/c3977271-019f-4653-8f42-75bff5e5e4f8)


3 - UserAgent

![image](https://github.com/user-attachments/assets/698fa428-6f53-45df-886f-21230cbeed50)

4 - POST

![image](https://github.com/user-attachments/assets/c09147f3-8f02-4227-809c-75e5f706eee6)

5 - Authorization

![image](https://github.com/user-attachments/assets/6288169c-f4a9-48ec-a156-02dcaa6cfdb6)

6 - Arquivos ocultos

começar o nome do arquivo com '.' -> ``` mkdir .pasta ``` 

![image](https://github.com/user-attachments/assets/b1174258-a99a-4cb7-a09c-28d777d64e0c)

7 - Revisão
