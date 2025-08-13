# Garantir que todas as dependencias estão instaladas
apt update

apt install ssh
apt install netcat
apt install net-tools
apt install apache2

## Criar segunda página no caminho

/var/www/nomeDaPastaDaPagina

### dentro dela criar o index.html

/var/www/nomeDaPastaDaPagina/index.html

- Exemplo:

![image](https://github.com/user-attachments/assets/01e60eea-3be7-4c98-8008-ae3f561a581d)


## Fazer o apache escutar a outra porta, no caso 7070

/etc/apache2/ports.conf

Para escutar a porta 7070

Listen 7070

Para escutar a porta 7070 vindo do localhost

Listen 127.0.0.1:7070

- Exemplo:

![image](https://github.com/user-attachments/assets/32a9be3a-ca2b-408e-9807-6c0b5481abdd)

## Criar uma configuração para que o apache carregue o novo site

/etc/apache2/sites-avaiable/nomeDaPagina.conf

- Exemplo:

![image](https://github.com/user-attachments/assets/4758dbab-e570-4f95-bcbe-95f5fa574b18)

## Após toda a configuração habilitar a nova pagina no apache2

a2ensite nomeDaPagina.conf

Esse arquivo irá para 

/etc/apache2/sites-enabled/nomeDaPagina.conf

## Dê restart no servidor apache

service apache2 restart

# Resultado exemplo:

### Padrão

![image](https://github.com/user-attachments/assets/7591fead-1ce7-4005-850e-7c79d54fcdcb)

### Deslogado

![image](https://github.com/user-attachments/assets/d62c3735-e073-4a49-a048-daf2a0efe625)

### Logado

![image](https://github.com/user-attachments/assets/3fcd05e3-5509-4d01-b0c6-9f3d6d8fcbea)
