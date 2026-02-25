# 25/02/26
# Firewall, INPUT,OUTPUT e FORWARD

- O que é um firewall: Firewall é um programa que atua diretaemnte no kernel do pc(o kernel que decide as regras do pc) por isso
                     ele é fundamental quando se trata em protejer dispositivos(principalmente contra scanners).
  
- O que são chains: CHAINS ou camadas, são os nomes das etapas que um pacote pode fazer para chegar num destino
                    (OUTPUT,INPUT e FORWARD).


- OUTPUT: Tráfego gerado pelo seu dispositivo, cuja função é criar pacotes, sair para a rede e de lá para o endpoit.
  ex:
     . Você(cria pacotes) -> rede(switch) -> endpoint(dispositivo final,recebe ou rejeita os pacotes).
     .Switch: repassa os dados em redes LAN, manda os dados para todos, mas só o expecificado pelo cliente é quem pode responder.


- INPUT: É todo tráfego cujo o destino final é você(sem repasse, o pacote chega e fica com você).
     . É uma camada muito protegida por justamente ser o trafego externo chegando em você(tráfego de outro pc).
  ex:
     . Tráfego externo(pacotes chgando) -> sua rede(sai para sua interface) -> você(firewall filtrando pacotes).
  

- FORWARD: Camada de repasse de dados, ele não é um endpoint, mas sim, um "repassador de informações/dados"
  ex:
     .Você(pacotes) -> sua rede -> roteador -> internet -> rede do endpoint -> endpoint(depois faz o porcesso inverso).
     .Percebeu que ele não fica com os dados? ele simplemente repassa.


  [Aprendizado]: Refocei conceitos que já utilizei antigamente. Sempre útil revisar conteúdos anteriores.
  
    





                
            
