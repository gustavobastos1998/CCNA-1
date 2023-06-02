# *Formato de mensagem DNS*

- O servidor DNS armazena diferentes tipos de registros de recursos usados \u200b\u200b para resolver nomes. 
- Esses registros contêm o nome, endereço e tipo de registro. Alguns desses tipos de registro são os seguintes:
	- **A** - Um endereço IPv4 do dispositivo final.
	- **NS** - Um servidor de nomes com autoridade.
	- **AAAA** - Um endereço IPv6 do dispositivo final (pronunciado quad-A).
	- **MX** - Um registro de troca de correio.
- O servidor DNS primeiro olha os seus próprios registros para resolver o nome. Caso não encontre, ele entrará em contato com outros servidores DNS.
- ![[secao de mensagem dns.png]]

# *Hierarquia DNS*

- O DNS usa os nomes de domínio para formar a hierarquia. O DNS é escalável porque a resolução do nome do host está espalhada por vários servidores.
- Quando um servidor DNS recebe uma requisição para a conversão de um nome que não faça parte da sua zona DNS, o servidor DNS a encaminha para outro servidor DNS na zona apropriada para a tradução. 
- O DNS é escalável porque a resolução do nome do host está espalhada por vários servidores.
- ![[hierarquia dns.png]]

# *Comando nslookup*

- Permite ao usuário consultar manualmente os servidores de nomes para resolver um determinado nome de host. Quando o comando **nslookup** é emitido, o servidor DNS padrão configurado para o seu host é exibido.

# *Protocolo de Configuração Dinâmica de Host (DHCP)*

- O serviço DHCP para IPv4 torna automática a atribuição de endereços IPv4, máscaras de sub-rede, gateways e outros parâmetros de rede IPv4. Isso é conhecido como o endereçamento dinâmico.
- Quando um host está conectado à Internet, o servidor DHCP é contatado e um endereço é requisitado. O servidor DHCP escolhe um endereço de uma lista configurada de endereços chamada pool e o atribui (aloca) ao host.
- O DHCP pode alocar endereços IP por um período de tempo configurável, chamado <mark style="background: #FFB86CA6;">período de concessão</mark>.
- O DHCP é usado para hosts de uso geral, como dispositivos de usuário final. O endereçamento estático é usado para dispositivos de rede, como roteadores de gateway, comutadores, servidores e impressoras.
- O DHCP para IPv6 (DHCPv6) fornece serviços semelhantes para clientes IPv6. Uma diferença importante é que o DHCPv6 não fornece o endereço do gateway padrão. Isso só pode ser obtido dinamicamente a partir da mensagem Anúncio do roteador.

# *Operação do DHCP*

- Quando um dispositivo IPv4 configurado com DHCP inicia ou se <mark style="background: #BBFABBA6;">conecta à rede</mark>, o cliente transmite uma mensagem de <mark style="background: #ABF7F7A6;">descoberta DHCP</mark> (DHCPDISCOVER) para identificar qualquer servidor DHCP disponível na rede.
- Um <mark style="background: #FFB86CA6;">servidor DHCP</mark> responde com uma mensagem de <mark style="background: #ABF7F7A6;">oferta DHCP</mark> (DHCPOFFER), que oferece uma locação ao cliente. A oferta contém endereço IPv4 e subnet mask a serem atribuídos, endereço IPv4 do servidor DNS e IPv4 do default gateway. A oferta de locação também inclui a duração da locação.
- ![[operacao DHCP.png]]
- O servidor retornará uma mensagem de confirmação DHCP (DHCPACK) que confirma para o cliente que a locação foi finalizada. Se a oferta não for mais válida, o servidor responde com DHCP negativa (DHCPNAK). 
- Caso DHCPNAK for retornada, o processo de seleção deverá ocorrer novamente com a transmissão de uma nova mensagem DHCPDISCOVER.