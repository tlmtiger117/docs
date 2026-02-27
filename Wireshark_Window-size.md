# 27/02/26
# Window-size Wireshark

- O que é :É basicamente a quantidade de dados que um host pode receber(bytes),armazenar(RAM) e processar(CPU)
- Função: Serve para Detectar scanners,SOs ou comportamentos suspeitos em geral na rede com base em:
          - Timesstamp: Tempo preciso entre cada pacote.
          - Window-size: Quantidade de dados que podem ser armazenados e processados.

- Como funciona: Window-size funciona basicamente confirmando recebimento de dados(bytes) e seguindo o fluxo da conexão TCP
     ex:
      - HOST1 -> Manda dados para o alvo -> HOSTALVO armazena e processa os dados com base no seu Window-size(limite dinâmico).
      - [ACK]: Quando o host confirma a conexão, ele modifica o window-size(libera espaço na RAM e CPU) para novas conexões,
               assim seguindo a conexão até o fim(tem [ACK] =  Window-size muda).

- Wireshark: Sniffer de rede("caçador de pacotes/analista"), observa tudo na rede em que está(sua interface).
      - Onde olhar o window-size: Window-size só funciona no protocolo TCP, pois esse é o protocolo de transmissão segura de dados.
      - Olhar na camada 4 do Wireshark.


- [aprendizado] Aprendi sobre como tudo que tem relação a rede tem um padrão, só basta conhecer a linha de base e ir testando e
                simulando os comportamentos suspeitos(entendendo o lado do atacante pra poder defender).


  
        
  
