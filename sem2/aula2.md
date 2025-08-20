Instalar foxy proxy

configurar proxy - man in the middle
name - burp suite

Placa de rede - lo
hostname - 127.0.0.1

# SQL Injection
Para testar se um site está vulnerável a um ataque sql colocar uma aspas simples ao final da url

Lista de sql injections:

https://github.com/payloadbox/sql-injection-payload-list/blob/master/Intruder/exploit/Auth_Bypass.txt

- Para ataque de força bruta

abrir burp suite

- passo a passo
caminho
proxy -> proxy settings

endereço de ip ali deve estar configurado no foxy proxy

colocar algum usuário e senha

ligar foxy proxy

tentar logar

send to intruder

aba intruder

seleciona o campo que quer alterar 

add - para transformar em variavel

dar load na wordlist

/usr/share/wordlists/metasploit

http_default_user.txt

http_default_pass.txt

dar start attack

para identificar o campo certo olhar o campo length/payload - para campo errado vai voltar sempre no mesmo tamanho e provavel um tamanho grande porque a mensagem de falha é grande. Para o campo certo vai ser um length pequeno porque "sucesso" tem poucos caracteres
