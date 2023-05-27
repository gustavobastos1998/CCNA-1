# *Mensagem RS e RA*

- Para o GUA, um dispositivo obtém o endereço dinamicamente através de mensagens ICMPv6 (Internet Control Message Protocol versão 6). Os roteadores IPv6 enviam mensagens ICMPv6 de RA a cada 200 segundos para todos os dispositivos habilitados para IPv6 na rede. 
- Uma mensagem de RA também é enviada em resposta a um host que envie uma mensagem ICMPv6 de RS (Solicitação de Roteador). Ambas as mensagens são mostradas na figura.
- ![[icmpv6 rs ra.png]]
- As mensagens de RA estão em interfaces Ethernet de roteador IPv6. O roteador deve estar habilitado para roteamento IPv6, que não está habilitado por padrão. Para ativar um roteador como roteador IPv6, deve ser usado o comando de **ipv6 unicast-routing** configuração global ipv6 unicast-routing.
- Uma mensagem ICMPv6 de RA inclui:
	- **Prefixo de rede e comprimento do prefixo** – Informa ao dispositivo a que rede ele pertence.
	- **Endereço do gateway padrão** – É um endereço LLA IPv6, o endereço IPv6 origem da mensagem de RA.
	- **Endereços DNS e nome de domínio** – Endereços de servidores DNS e um nome de domínio.
- Existem 3 métodos para mensagens RA:

### **SLAAC**

- O SLAAC tem tudo o que o host precisa, incluindo o prefixo, comprimento do prefixo e endereço de gateway padrão

### **SLAAC com um server DHCPv6 stateless**

- Esse método tem as mesma informações do SLAAC, mas o host precisa obter outras informações, como endereços DNS, de um servidor DHCPv6 sem estado. 

### **DHCPv6 com estado (sem SLAAC)**

- Informa o gateway padrão, mas exige que o host peça a um DHCPv6 server com estado que informe todo o resto. 

# *SLAAC*

- SLAAC é um método que permite que um dispositivo crie seu próprio GUA sem os serviços do DHCPv6. Com SLAAC, os dispositivos dependem das mensagens ICMPv6 de RA (Anúncio de Roteador) do roteador local para obter as informações necessárias.
- Por padrão, a mensagem de RA sugere que o dispositivo de recebimento use as informações dessa mensagem para criar seu próprio endereço IPv6 unicast global e para todas as demais informações. Os serviços de um servidor DHCPv6 não são obrigatórios.
- Com SLAAC, o dispositivo cliente usa as informações da mensagem de RA para criar seu próprio endereço unicast global. Como mostrado na Figura , as duas partes do endereço são criadas da seguinte forma:
	- **Prefixo** - Isso é anunciado na mensagem RA.
	- **ID da Interface** - Isso usa o processo EUI-64 ou gera um número aleatório de 64 bits, dependendo do sistema operacional do dispositivo.
- ![[SLAAC.png]]

# *SLAAC e DHCPv6 stateless*

- SLAAC para criar seu próprio IPv6 GUA;;
- O LLA do roteador, que é o endereço IPv6 de origem RA, como o endereço de gateway padrão;
- Um servidor DHCPv6 stateless para obter outras informações como o endereço de um servidor DNS e um nome de domínio.
- ![[SLAAC e DHCPv6 stateless.png]]

# *DHCPv6 stateful*

- Uma interface de roteador pode ser configurada para enviar um RA usando apenas DHCPv6 com estado.
- O DHCPv6 stateful é semelhante ao DHCP para IPv4. Um dispositivo pode receber automaticamente suas informações de endereçamento, incluindo uma GUA, tamanho do prefixo e os endereços dos servidores DNS de um servidor DHCPv6 com monitoração de estado.
- A mensagem RA sugere ao host que eles usem:
	- O LLA do roteador, que é o endereço IPv6 de origem RA, como o endereço de gateway padrão
	- Um servidor DHCPv6 stateful para obter o endereço unicast global, o endereço do servidor DNS, o nome do domínio e todas as demais informações.
- ![[DHCPv6 stateful.png]]
- **Observação:** O endereço de gateway padrão só pode ser obtido dinamicamente a partir da mensagem RA. O servidor DHCPv6 stateless ou stateful não fornece o endereço de gateway padrão.

# *Processo EUI-64 ou gerado aleatoriamente*

- Quando a mensagem de RA é SLAAC ou SLAAC com DHCPv6 stateless, o cliente deve gerar sua própria ID da interface. O cliente conhece a parte de prefixo do endereço da mensagem de RA, mas deve criar sua própria ID da interface. 
- A ID da interface pode ser criada por meio do processo EUI-64 ou de um número de 64 bits gerado aleatoriamente, como mostrado na imagem.
- ![[ID interface.png]]