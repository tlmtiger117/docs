# 20/02/26
# Fluxo da Sub_rede e roteadores:

1- o cliente faz a perunta(você): "esse ip da outra rede está ativo(ICMP request)"?

2- a máscara de rede analisa: "hum.. esse endereço não é da nossa rede, vai ter que mandar pro roteador"

3- roteador: "blz, recebi esses dados, tenho acesso a rede da pergunta(por causa dos meus adptadores),
              vou repassar para o endereço de destino dessa outra rede"

4- host-rede2: recebi um ICMP, estou ativo, mandando resposta(reply) para quem perguntou

5- máscara: "ip não é dessa rede, passando pro roteador"

5- roteador:"resposta recebida, mandado pra quem perguntou"

6- cliente:"certo, host ativo".
