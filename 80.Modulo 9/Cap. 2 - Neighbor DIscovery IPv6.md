# *Mensagem de descoberta de vizinhos IPv6*

- O protocolo IPv6 descoberta de vizinhos é referido como ND ou NDP. Ele é usado para associar IPv6 aos endereços MAC. 
- Similar ao ARP só que dessa vez o protocolo de internet é o IPv6.
- O ND fornece serviços de resolução de endereço, descoberta de roteador e redirecionamento para IPv6 usando ICMPv6. 
- O ICMPv6 ND usa cinco mensagens ICMPv6 para executar estes serviços:
	- Mensagens de solicitação de vizinho;
	- Mensagens de anúncio vizinho;
	- Mensagens de solicitação de roteador;
	- Mensagens de anúncio do roteador;
	- Redirecionar mensagem.
- As mensagens de solicitação de vizinho e anúncio de vizinho são usadas para mensagens de dispositivo a dispositivo, como resolução de endereço (semelhante ao ARP para IPv4). Os dispositivos incluem computadores host e roteadores.
- **Observação**: A quinta mensagem ICMPv6 ND é uma mensagem de redirecionamento que é usada para melhor seleção do próximo salto.
- As mensagens de solicitação de roteador e anúncio de roteador são para mensagens entre dispositivos e roteadores. Normalmente, a descoberta de roteador é usada para alocação de endereços dinâmicos e auto configuração de endereço sem estado (SLAAC - Stateless Address Auto-Configuration). O SLAAC auto configura os endereços IPv6, sem necessitar do DHCPv6 servers. 

# *Descoberta de vizinhos IPv6 - resolução de endereços*

- As mensagens Solicitação de vizinho ICMPv6 e Anúncio de vizinho são usadas para a resolução de endereço MAC. Isso é semelhante às Solicitações ARP e Respostas ARP usadas pelo ARP para IPv4.
- ![[solicitacao e anuncio de vizinho IPv6.png]]
- As mensagens de solicitação de vizinhos ICMPv6 são enviadas usando endereços de multicast Ethernet e IPv6 especiais. Isso permite que a NIC Ethernet do dispositivo receptor determine se a mensagem de solicitação de vizinho é para si mesmo sem ter que enviá-la para o sistema operacional para processamento.

