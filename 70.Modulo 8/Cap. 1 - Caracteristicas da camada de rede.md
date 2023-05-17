# *A camada de rede*

- Também conhecida como camada OSI 3, forcene serviços para permitir que dispositivos finais troquem dados entre redes. 
- Os principais protocolos de comunicação de camada de rede são IPv4 e IPv6. 
- Protocolos de camada de rede também incluem protocolos de roteamento como OSPF e protocolos de mensagens como ICMP que dá feedback para o dispositivo de origem caso a mensagem tenha chegao com sucesso.
- 4 operações básicas para realizar a comunicação:
	- <mark style="background: #ADCCFFA6;">Endereçamento de dispositivos finais</mark> - Os dispositivos finais devem ser configurados com um endereço IP exclusivo para identificação na rede.
	- <mark style="background: #ADCCFFA6;">Encapsulamento</mark> - A camada de rede encapsula a unidade de dados de protocolo (PDU) da camada de transporte em um pacote. O processo de encapsulamento adiciona informações de cabeçalho IP, como os endereços IP dos hosts origem (emissor) e destino (receptor). O processo de encapsulamento é executado pela origem do pacote IP.
	- <mark style="background: #ADCCFFA6;">Roteamento</mark> - A camada de rede fornece serviços para direcionar os pacotes para um host de destino em outra rede. O pacote deve ser processado pelo roteador, pois é ele quem determina o melhor caminho para os pacotes seguirem do host origem para o destino. Cada roteador por onde o pacote atravessa até chegar ao host de destino é conhecido como hop ou salto.
	- <mark style="background: #ADCCFFA6;">Desencapsulamento</mark> - Quando o pacote chega na camada de rede do host de destino, o host verifica o cabeçalho IP do pacote. Se o endereço IP de destino no cabeçalho corresponder ao seu próprio endereço IP, o cabeçalho IP será removido do pacote. Depois que o pacote é desencapsulado pela camada de rede, a PDU resultante da Camada 4 é transferida para o serviço apropriado na camada de transporte. O processo de desencapsulamento é executado pelo host de destino do pacote IP.
- Diferentemente da camada de transporte (OSI Layer 4), que gerencia o transporte de dados entre os processos em execução em cada host, os protocolos de comunicação da camada de rede (ou seja, IPv4 e IPv6) especificam a estrutura de pacotes e o processamento usado para transportar os dados de um host para outro hospedeiro. A operação sem levar em consideração os dados contidos em cada pacote permite que a camada de rede transporte pacotes para diversos tipos de comunicações entre vários hosts.

# *Encapsulamento IP*

- ![[encapsulamento ip.png]]
- O encapsulamento é importante por possibilitar o desenvolvimento e expansão dos serviços nas diferentes camadas sem afeta-las. 
- O cabeçalho IP é examinado por dispositivos de camada 3, ou seja, roteadores e switches de camada 3, à medida que viaja pela rede até seu destino. As informações do endereçamento IP não mudam até chegar ao host destino, diferente dos quadros da camada 2 que mudavam o endereço MAC com frequência. 
- A única exceção é quando os pacotes são traduzidos pelo dispositivo que executa a Tradução de Endereços de Rede (NAT) para IPv4.
- Os roteadores implementam protocolos de roteamento para rotear pacotes entre redes. O roteamento realizado por esses dispositivos intermediários examina o endereçamento da camada de rede no cabeçalho do pacote. Em todos os casos, a parte de dados do pacote, ou seja, a PDU da camada de transporte encapsulada ou outros dados, permanece inalterada durante os processos da camada de rede.

# *Características do IP*

- O protocolo IP fornece apenas as funções necessárias para enviar um pacote de uma origem a um destino por um sistema interconectado de redes. O protocolo não foi projetado para rastrear e gerenciar o fluxo de pacotes. Essas funções, se exigido, são realizadas por outros protocolos em outras camadas, principalmente TCP na Camada 4.
- Estas são as características básicas da IP:
	- **Sem conexão** - Não há conexão com o destino estabelecido antes do envio de pacotes de dados.
	- **Melhor esforço** - o IP é inerentemente não confiável, porque a entrega de pacotes não é garantida.
	- **Independente da mídia** - A operação é independente do meio (ou seja, cobre, fibra ótica ou sem fio) que carrega os dados.

# *Sem conexão*

- Significa que nenhuma conexão ponta a ponta dedicada é criada pelo IP antes que os dados sejam enviados. 
- A comunicação sem conexão envia um pacote sem informar o destinatário com antecedência. 

# *Melhor esforço*

- O protocolo IP não garante que o pacote enviado seja, de fato, recebido. A figura ilustra a característica de entrega não confiável ou de melhor esforço do protocolo IP.
- ![[melhor esforco.png]]

# *Independente de mídia*

- Não confiável significa que o IP não tem a capacidade de gerenciar e recuperar pacotes não entregues ou corrompidos. Os pacotes podem chegar ao destino corrompidos, fora de sequência ou simplesmente não chegar. O IP não tem capacidade de retransmitir os pacotes em caso de erros.
- Se os pacotes forem entregues fora de ordem ou estiver faltando algum pacote, as aplicações que usam os dados, ou serviços de camada superior, deverão resolver esses problemas. Isso permite que o IP funcione de forma bem eficiente. No conjunto de protocolos TCP / IP, a confiabilidade é o papel do protocolo TCP na camada de transporte.
- O IP opera independente da mídia que transporta os dados. Esse é o papel dos protocolos da camada de data link.
- ![[independente de midia.png]]
- Há, no entanto, uma característica muito importante dos meios físicos que a camada de rede considera: o tamanho máximo da PDU que cada meio consegue transportar. 
- Essa característica é chamada de unidade máxima de transmissão (maximum transmission unit - MTU). A camada de enlace de dados informa o valor da MTU para a camada de rede. 
- Em alguns casos, um dispositivo intermediário, geralmente um roteador, deve dividir um pacote IPv4 ao transmiti-lo de um meio para outro com uma MTU menor. Esse processo é conhecido como fragmentação ed pacote ou fragmentação. A fragmentação causa latência. Os pacotes IPv6 não podem ser fragmentados pelo roteador.
