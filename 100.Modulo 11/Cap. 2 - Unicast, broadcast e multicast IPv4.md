# *Unicast*

- Transmissão unicast refere-se a um dispositivo que envia uma mensagem para outro dispositivo em comunicações um-para-um.
- Os endereços de host unicast IPv4 estão no intervalo de endereços de 1.1.1.1 a 223.255.255.255. Contudo, dentro desse intervalo há muitos endereços que já são reservados para fins especiais.

# *Broadcast*

- A transmissão de difusão, ou broadcast, refere-se a um dispositivo que envia uma mensagem para todos os dispositivos em uma rede em comunicações um para todos.
- Um pacote de broadcast possui um endereço IP de destino com todos os (1s) na parte do host ou 32 (um) bits.
- Não existe pacotes broadcast com IPv6. 
- Um pacote de difusão deve ser processado por todos os dispositivos no mesmo domínio de difusão. Um domínio de difusão identifica todos os hosts no mesmo segmento de rede. Uma transmissão pode ser direcionada ou limitada. 
- Um broadcast direcionado é enviado para todos os hosts em uma rede específica. Por exemplo, um host na rede 172.16.4.0/24 envia um pacote para 172.16.4.255. Uma broadcast limitado é enviado para 255.255.255.255. Por padrão, os roteadores não encaminham broadcasts.

# *Multicast*

- Um pacote multicast é um pacote com um endereço IP de destino que é um endereço multicast. O IPv4 reservou os endereços 224.0.0.0 a 239.255.255.255 como intervalo de multicast.
- Cada grupo multicast é representado por um único endereço IPv4 multicast de destino. Quando um host IPv4 se inscreve em um grupo multicast, o host processa pacotes endereçados tanto a esse endereço multicast como a seu endereço unicast alocado exclusivamente.
- Protocolos de roteamento, como OSPF, usam transmissões multicast. Por exemplo, os roteadores habilitados com OSPF se comunicam entre si usando o endereço multicast OSPF reservado 224.0.0.5. 
- Somente dispositivos habilitados com OSPF processarão esses pacotes com 224.0.0.5 como endereço IPv4 de destino. Todos os outros dispositivos ignorarão esses pacotes.