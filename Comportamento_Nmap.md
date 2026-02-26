# 26/02/26
# Analisando Comportamento Nmap

- Nmap(Networke mapper):ferramenta utilisada para análises de rede(hosts,portas,firewall...) e dispositivos em regral da rede.
- Telnet: Cliente TCP padrãom utilisado para estabelecer conexões com servidores(rápido e fácil)
- Wireshark: Sniffer de rede("captuador"), captura todo tráfego da sua interface de rede(precisa estar presente nela).
- FTP: Protocólo de tranfêrencia de dados Remoto em uma rede. Atua somente em uma pasta especificada pelo dono(server) FTP.


- Fluxo:
        .1°- Telnet: Usado para simular tráfego de cliente padrão
        .2°- Nmap: Utilisado para simular scanner de rede(atacante/testador de segurança).
        .3°- Wireshark: Utilisado para simular um ADM de rede vendo tráfego em tempo real.


- Telnet(SERVER): Recebe um pedido(SYN), aceita o pedido (SYN-ACK) e o cliente confirma a conexão(ACK)
        .Após o estebelecer conexão o FTP retorna "response"(reposta) ao cleinte, mandando a versão do serviço FTP
        .[!]Fingersprint: técnica de descoberta de versões de serviços. Elas normalemnte chegam nessa fase e resetam a conexão(RST)
  
- Nmap: Faz toda a parte de iniciar uma conexão, mas na hora de confirmar(ACK final), ele manda um RST, encerrando imediatamente
        a conexão com o servidor FTP(-sS)
  
    .[!] O Nmap manda pacotes com tamanhos idênticos, Isso pode ser usado por ADMs de rede para detectar comportamentos conhecidos
         de scanners de rede(pois a maioria dos scanners que existem, se inspiram no Nmap).
  
- Wireshark: Tem total visão da rede(em tempo real) de tudo que acontece. Ela que observou esses comportamentos do Telnet e do Nmap
         .Como todo comportamento numa rede pode ser detectado, ele desenpenha o paple da "análise ativa", sempre buscando
         comportamentos fora do padrão.
  
- [!] Aviso, essas ferramentas não funcionam sozinhas. Elas podem ser utilisadas tanto para proteger quanto para atacar
      (pentest autorizado ou cibercriminoso), por isso, sempre use esses conehciemntos para o bem dos outros Nunca para prejudicar
      alguem.
       




       
       

  
   
