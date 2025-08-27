### Dicas:

- Hydra
- SSH -> redirecionamento de porta, chave pública e privada
- Burp

OBS: Maquina tem firewall - vai bloquear ip -> necessário resetar a VM

Só não vai funcionar não tem um erro específico.

### passo a passo

- prova credencial e porta aberta

- usar hydra

- entrar dentro do server

- as portas abertas

- redirecionamento de porta

- chega no burp

### Dica prova:

1 - verificar placas de rede host-only

2 - verificar ips

3 - netdiscover

<img width="626" height="360" alt="image" src="https://github.com/user-attachments/assets/d41236f5-20a8-4172-a9c1-87218c891f17" />

4 - jogar o ip encontrado no navegador

5 - abrir bwapp no owasp

6 - ligar foxy proxy e burp suite

7 - no burpsuite ligar interceptor

8 - tentar logar

9 - no burp send to intruder a requisição

10 - na aba intruder selecionar as variaveis que deseja fazer o ataque e clicar em add

11 - carregar lista e possiveis senhas

12 - selecionar tipo de ataque - > sniper attack

13 - dar start attack

14 - fechar aba de attack

15 - em settings la em grep match -> dar clear e colocar invalid




### Exemplo de grep

gunzip no rockyou

cat rockyou.txt | grep "brazil"
