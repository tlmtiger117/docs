# 20/02/26
# Fluxo da Sub_rede e roteadores:

1- o cliente faz a perunta(você): "esse ip da outra rede está ativo(ICMP request)"?

2- a máscara de rede analisa: "hum.. esse endereço não é da nossa rede, vai ter que mandar pro roteador"

3- roteador: "blz, recebi esses dados, tenho acesso a rede da pergunta(por causa dos meus adptadores),
              vou repassar para o endereço de destino dessa outra rede"
              
  - [!] sempre ative o forward(repasse no roteador, sem isso, não tem como acessar outra rede/repassar dados). 
        comando do forward(ubuntu server):sudo sysctl -w net.ipv4.ip_forward=1
        sempre que fechar a VM/resetar ela, tem que ativar o repasse de novo(sei que tem confg permanente, mas não encontrei).
                  
                  
4- host-rede2: recebi um ICMP, estou ativo, mandando resposta(reply) para quem perguntou

5- máscara: "ip não é dessa rede, passando pro roteador"

5- roteador:"resposta recebida, mandado pra quem perguntou"

6- cliente:"certo, host ativo".

- [!] link para o projeto finalizado de "sub-redes": https://github.com/tlmtiger117/projetos/blob/main/Projeto-Sub_Redes.txt
