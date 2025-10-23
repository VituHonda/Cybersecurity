# Preparando ambiente para usar gobuster

- apt update
- apt install gobuster
- precisa entrar no caminhou ou digitar inteiro

<img width="296" height="43" alt="image" src="https://github.com/user-attachments/assets/360517e8-9c83-436b-883e-7269b2fe1565" />

- Mapeando caminhos de pastas padrão de um ip

<img width="658" height="383" alt="image" src="https://github.com/user-attachments/assets/03d65405-1b54-4532-92e2-477d188dd582" />

- Da pra remapear para pastar terminadas com status code 300

<img width="755" height="476" alt="image" src="https://github.com/user-attachments/assets/b7452202-824d-4d79-8b32-e4e2f37dfea0" />



cp03
sem porta aberta
sem vulnerabilidade

# Dicas GS - KIRA + KALI

- LFI locate file inclusion

<img width="1351" height="543" alt="image" src="https://github.com/user-attachments/assets/743a79b0-e493-4318-ad9c-55b83bfd1830" />

- Encontrar portas abertas com nmap

<img width="272" height="72" alt="Captura de tela 2025-10-23 194236" src="https://github.com/user-attachments/assets/9bae436b-0a16-4e73-b8e3-955d2f8f5dec" />

- RFI -> remote file inclusion

Pegar backdoor (script que abre portas) -> php-reverse-shell.php transformar em uma imagem e jogar no servidor

- Encontrando arquivo backdoor

/usr/share/webshells

<img width="346" height="200" alt="image" src="https://github.com/user-attachments/assets/fe2a935c-158e-4720-8d1c-d893a85820e1" />

<img width="537" height="226" alt="image" src="https://github.com/user-attachments/assets/fc08bf53-a2da-43a5-ae99-4a2b52f1c8b1" />

- Transformando backdoor em imagem

cp php-reverse-shell.php revshell.php.jpg

<img width="530" height="248" alt="image" src="https://github.com/user-attachments/assets/f8aef875-1748-4d0a-a60b-78dea617c51b" />

- Vai fazer o contrário o backdoor vai fazer o servidor conectar no cliente

Alterar aqui com o ip da máquina do cliente

<img width="608" height="381" alt="image" src="https://github.com/user-attachments/assets/d0350389-945d-4131-be91-c7548ce1673d" />

Dar upload no arquivo

Fazer enumeração de pasta

<img width="588" height="202" alt="image" src="https://github.com/user-attachments/assets/70172b18-42d3-48c9-93ec-a0b509a496a4" />

Exemplo

<img width="1279" height="604" alt="image" src="https://github.com/user-attachments/assets/1a6463a4-fcaa-479d-abb9-346a4cc0b47a" />

<img width="901" height="585" alt="image" src="https://github.com/user-attachments/assets/8702534b-694a-43e2-8933-a5a144f5eec3" />

Abrindo porta com netcat

<img width="360" height="194" alt="image" src="https://github.com/user-attachments/assets/82d1c12b-802f-44a7-b52b-bb991958f928" />

Para conseguir executar o backdoor é necessário usar a url falha

<img width="909" height="139" alt="image" src="https://github.com/user-attachments/assets/96405b92-6960-4aa3-8775-d053e40a334d" />

Alternativa colocar depois de = -> /uploads/revshell.php.jpg

- Desabilitar pty -> isso ocultar pty do servidor -> oculta historico 

python3 -c "import pty;pty.spawn('/bin/bash')"

<img width="409" height="89" alt="image" src="https://github.com/user-attachments/assets/8a0d71b3-9486-4b8b-a69b-e36742757e4e" />

Aqui revela 2 usuários -> www-data e bassam

<img width="507" height="282" alt="image" src="https://github.com/user-attachments/assets/e0a857ea-2757-4cfc-b1ff-e87f1df38d9b" />

User.txt possivelmente flag

Em aplicações web normalmente estão dentro de /var/www/html

<img width="527" height="193" alt="image" src="https://github.com/user-attachments/assets/ea41ae96-6ac1-4ed9-bbcf-c57de6826f5f" />

<img width="642" height="77" alt="image" src="https://github.com/user-attachments/assets/0d5f620d-fb1c-43c9-8251-edabe4307990" />

Entrar no usuário bassam

<img width="579" height="101" alt="image" src="https://github.com/user-attachments/assets/5fc4b5e3-6bd8-4509-a6fa-3bfb415a5756" />

# PARABENS ENTROU NO USUARIO NORMAL - FALTA O ROOT

Entrando no usuário root

Tenta entrar no root e usando senha do bassam e ele avisa o comando usado pelo usuário que passa pelo root

<img width="668" height="208" alt="image" src="https://github.com/user-attachments/assets/484e0600-a1e7-4ca0-8833-cf9d6dbe5a14" />

### Falha de segurança

https://gtfobins.github.io/

https://gtfobins.github.io/gtfobins/find/

<img width="670" height="201" alt="image" src="https://github.com/user-attachments/assets/74bdaca3-91a9-4c77-9219-756206b0d266" />

entrar no root e achar a flag

<img width="99" height="106" alt="image" src="https://github.com/user-attachments/assets/d819e1e5-d6a2-462c-be52-64bda4ffa1eb" />

com cat abre a flag
