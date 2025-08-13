# Kali

funciona ctrl v

## enviando arquivos para o servidor

"scp form_post.html aluno@192.168.10.20:/home/aluno"

possivel especificar o lugar pra onde vai

nao deu pra mandar direto pra /var/www/html por conta de permissao

## movendo arquivos no servidor

mv form_post.html /var/www/html

## proxy

instalar foxyproxy no mozila

## configurando proxy

option
Add
BurpSuite
127.0.0.1
8080

## Criar banco de dados

apt update
apt install mariadb-server mariadb-client

- ligando o banco

systemctl start mariadb

- ativando o banco

systemctl enable mariadb

- acessar mariadb

mysql -u root

- criando banco dentro do sql

CREATE DATABASE loginDB;

- acessando banco BEM IMPORTANTE

USE loginDB

- criando tabela

CREATE TABLE users (
 id INT AUTO_INCREMENT PRIMARY KEY,
 username VARCHAR(50) NOT NULL,
 password VARCHAR(255) NOT NULL
);

INSERT INTO users (username, password) VALUES ('nome_do_usuario', 'senha_segura');

