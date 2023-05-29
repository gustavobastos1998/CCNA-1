# *Endereços IPv6 Multicast Atribuídos*

- Os endereços IPv6 multicast são semelhantes aos endereços IPv4 multicast. Lembre-se de que um endereço multicast é usado para enviar um único pacote a um ou mais destinos (grupo multicast). Os endereços multicast <mark style="background: #BBFABBA6;">IPv6</mark> têm o <mark style="background: #BBFABBA6;">prefixo ff00::/8</mark>.
- Há dois tipos de endereços IPv6 multicast:
	- Endereços multicast conhecidos
	- Endereços multicast do nó solicitados

# *Endereços comuns de multicast IPv6*

- São endereços atribuídos e reservados para grupos predefinidos de dispositivos. 
- Os endereços multicast atribuídos são usados no contexto com protocolos específicos, como o DHCPv6.
- Estes são dois grupos multicast atribuídos ao IPv6 comuns:

### **ff02::1 grupo multicast de todos os nós**

- Grupo ao qual todos os dispositivos habilitados para IPv6 se juntam. Tem o mesmo efeito que o endereço de broadcast para IPv4. Um pacote enviado para esse grupo é recebido e processado por todas as interfaces IPv6 no link ou rede.
- ![[multicast IPv6 all nodes.png]]

### **ff02::2 grupo multicast de todos os roteadores**

- Grupo ao qual todos os roteadores fazem parte. O roteador faz parte desse grupo ao habilitar o roteamento IPv6 com o comando <mark style="background: #ABF7F7A6;">ipv6 unicast-routing</mark>. Um pacote enviado para esse grupo é recebido e processado por todos os roteadores IPv6 no link ou rede.

# *Endereços IPv6 Multicast do nó solicitado*

- Semelhante ao multicast all nodes. A vantagem do endereço do nó solicitado é que ele é mapeado para um endereço multicast Ethernet especial. 
- Isso é possível pois a placa de rede Ethernet filtra o quadro, examinando o endereço MAC de destino sem enviá-lo ao processo IPv6 para ver se o dispositivo é o alvo pretendido do pacote IPv6. 
- ![[multicast no solicitado.png]]