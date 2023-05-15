# *MAC e Hexadecimal*

- Um endereço MAC Ethernet consiste em um valor binário de 48 bits. Hexadecimal é usado para identificar um endereço Ethernet porque um único dígito hexadecimal representa quatro bits binários. Portanto, um endereço MAC Ethernet de 48 bits pode ser expresso usando apenas 12 valores hexadecimais.
- As equivalências decimais e binárias de 0 a F em hexadecimal são:
- ![[deci-hexa-bina.png]]
- Outras equivalências interessantes são:
- ![[deci-hexa-bin interessantes.png]]
- Note que os zeros à esquerda sempre são exibidos para completar a representação 8 bits. 

# *Endereços MAC Ethernet*

- Um endereço MAC Ethernet é um endereço de 48 bits expresso usando 12 dígitos hexadecimais, como mostrado na figura. Como um byte é igual a 8 bits, também podemos dizer que um endereço MAC tem 6 bytes de comprimento.
- ![[MAC Address.png]]
- Todos os endereços MAC devem ser exclusivos do dispositivo Ethernet ou da interface Ethernet. 
- Para garantir isso, todos os fornecedores que vendem dispositivos Ethernet devem se registrar no IEEE para obter um código hexadecimal exclusivo de 6 (ou seja, 24 bits ou 3 bytes) chamado identificador exclusivo organizacionalmente (OUI).
- ![[OUI.png]]

# *Processamento de quadros*

- O endereço MAC é chamado também de endereço gravado de fábrica (BIA - Burned-in-Address) , porque ele é gravado na ROM da NIC. 
- **Observação**: Nos modernos sistemas operacionais de PC e NICs, é possível alterar o endereço MAC no software. Isso é útil para tentar obter acesso a uma rede que filtre com base no BIA. Consequentemente, a filtragem ou o controle de tráfego com base no endereço MAC não é mais tão seguro.
- Quando uma NIC recebe um quadro Ethernet, examina o endereço MAC de destino para verificar se corresponde ao endereço MAC físico armazenado na RAM. Se não houver correspondência, o dispositivo descartará o quadro. Caso haja, ele passará o quadro para cima nas camadas OSI, onde o processo de desencapsulamento ocorre.
- **Note:** As NICs Ethernet também aceitarão quadros se o endereço MAC de destino for uma transmissão ou um grupo multicast do qual o host é membro.

# *Endereço MAC Unicast*

- Um endereço MAC de unicast é o endereço exclusivo usado quando um quadro é enviado de um único dispositivo de transmissão para um único dispositivo de destino.
- O processo que um host de origem usa para determinar o endereço MAC de destino associado a um endereço IPv4 é conhecido como ARP (Address Resolution Protocol). 
- O processo que um host de origem usa para determinar o endereço MAC de destino associado a um endereço IPv6 é conhecido como ND (Neighbour Discovery).
- **Observação:** O endereço MAC de origem deve ser sempre unicast.

# *Endereço MAC Broadcast*

- Um quadro de transmissão Ethernet é recebido e processado por cada dispositivo na LAN Ethernet. Os recursos de uma transmissão Ethernet são os seguintes:
	- Possui um endereço MAC de destino de FF-FF-FF-FF-FF-FF em hexadecimal.
	- É inundada todas as portas de switch Ethernet, exceto a porta de entrada.
	- Ele não é encaminhado por um roteador.
- Se os dados encapsulados forem um pacote de transmissão IPv4, isso significa que o pacote contém um endereço IPv4 de destino que possui todos os 1s na parte do host. Essa numeração no endereço significa que todos os hosts naquela rede local (domínio de broadcast) receberão e processarão o pacote.
- Exemplo: quando o IPv4 destino for 192.168.1.255. Conhecido como pacote IPv4 broadcast. 
- Quando o IPv4 broadcast é encapsulado o endereço MAC de destino é o MAC de broadcast FF-FF-FF-FF-FF-FF. 

# *Endereço MAC Multicast*

- Um quadro de multicast Ethernet é recebido e processado por um grupo de dispositivos na LAN Ethernet que pertencem ao mesmo grupo de multicast.
- Os recursos de um multicast Ethernet são os seguintes:
	- Há um endereço MAC de destino <mark style="background: #BBFABBA6;">01-00-5E</mark> quando os dados encapsulados são um pacote multicast <mark style="background: #BBFABBA6;">IPv4</mark> e um endereço MAC de destino de <mark style="background: #FFF3A3A6;">33-33</mark> quando os dados encapsulados são um pacote multicast <mark style="background: #FFF3A3A6;">IPv6</mark>.
	- Há outros endereços MAC de destino multicast reservados para quando os dados encapsulados não são IP, como STP (Spanning Tree Protocol) e LLDP (Link Layer Discovery Protocol).
	- São inundadas todas as portas de switch Ethernet, exceto a porta de entrada, a menos que o switch esteja configurado para espionagem multicast.
	- Ele não é encaminhado por um roteador, a menos que o roteador esteja configurado para rotear pacotes multicast.
- Se os dados encapsulados forem um pacote multicast IP, os dispositivos que pertencem a um grupo multicast recebem um endereço IP do grupo multicast. 
- O intervalo de endereços multicast IPv4 é 224.0.0.0 a 239.255.255.255. O intervalo de endereços multicast IPv6 começa com ff00::/8. 
- Como os endereços multicast representam um grupo de endereços (às vezes chamado de grupo de hosts), eles só podem ser utilizados como destino de um pacote. A origem sempre será um endereço unicast.