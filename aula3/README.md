
# Cursos alura

- Formação LPI

#  Fundamentos

- 1
Slide 7 relação client e server side com protocolos no meio

porta dos protocolos 
https - 443
http - 80

dns - 53

- Protocolos https
como funciona:
3 handshake
syn ack
ack syn
syn

chave publica e privada

Flags: 
rst
push
fyn

- 2
stateless server
baseado nos cookies

- 3
métodos http
get
post
put
delete
patch
head

connect
options
trace

# Funcionamento
códigos da cinco categorias de resposta http

1. Informativo (100-199)
2. Sucesso (200-299)
3. Redirecionamento (300-399)
4. Erro de cliente (400-499)
5. Erro do servidor (500-599)

Esses códigos são definidos na
RFC 9110 (mais de 200 páginas)

# Cabeçalho http

Host
User-Agent
Accept
Accept-Language
Authorization
Content-Type
Content-Length
Status-Line
Content-Type
Content-Length
Set-Cookie
Cache-Control
Location

# Dica CP segundo semestre

- troca de chave publica e privada ssh

# Maldade

## Mesmo em modo anônimo por conta dos cookies as páginas ficam salvas na memória do sistema operacional

Navegador para privacidade - Firefox
abrir opções avançadas no firefox:
``` about.config ```

informações salvas pelos navegadores ficam salvas 180 dias

## User-Agent 
Os user agents dos cabeçalhos são usados para aumentar os preços com base nas informações que o user agent salva

Exemplo: modelo de celular, quantidade de bateria, quantidade de acessos

## Storm-Breaker 
github
ve do celular: 
geolocalização
imagem
audio

# LINUX

Quando o --help for muito grande digitar
``` comando | less ```
para aparecer o scroll

mudar senha
``` passwd ```

adicionar usuário oculto 
``` useradd ```

adicionar usuário
``` adduser ```

ao usar ls -la ou ls -lha
drwxr-xr-x

permissoes
d - dentro do hd
rwx - usuario
r-x - grupo
r-x - outros

r = read
w = write
x = execute

criar arquivo
cat > nomeDoArquivo

escrever no arquivo
echo "texto" > nomeDoArquivo
