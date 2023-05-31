# *Mensagens ICMPv4 e ICMPv6*

- Embora o IP seja apenas um protocolo de melhor esforço, o pacote TCP/IP fornece mensagens de erro e mensagens informativas ao se comunicar com outro dispositivo IP. Essas mensagens são enviadas com os serviços do ICMP.
- O objetivo dessas mensagens é dar feedback sobre questões relativas ao processamento de pacotes IP sob certas condições, e não tornar o IP confiável. As mensagens ICMP não são necessárias e muitas vezes não são permitidas por questões de segurança.

# *Acessibilidade do host*

- Uma mensagem de eco ICMP pode ser usada para testar a capacidade de acesso de um host em uma rede IP. A origem manda um echo request e o destino responde com um echo repply.
- Esse uso de mensagens de eco ICMP é a base do comando ping.

# *Disponibilidade ou serviço inalcançável*

- Quando um host ou um gateway recebe um pacote que não pode entregar, ele pode usar uma mensagem ICMP de destino inalcançável para notificar à origem que o destino ou o serviço está inalcançável. 
- A mensagem conterá um código que indica por que não foi possível entregar o pacote.
- Alguns dos códigos de Destino inacessível para o ICMPv4 são os seguintes:
	- 0 - rede inalcançável
	- 1 - host inalcançável
	- 2 - protocolo inalcançável
	- 3 - porta inalcançável
- Alguns dos códigos de Destino inacessível para o ICMPv6 são os seguintes:
	- 0 - Nenhuma rota para o destino
	- 1 - A comunicação com o destino é administrativamente proibida (por exemplo, firewall)
	- 2 - Além do escopo do endereço de origem
	- 3 - Endereço inacessível
	- 4 - porta inalcançável

# *Tempo excedido (Time out)*

- Uma mensagem ICMPv4 de tempo excedido é usada por um roteador para indicar que um pacote não pode ser encaminhado porque o campo Vida Útil (TTL) do pacote foi reduzido a 0.
- Para o ICMPv6 o campo de Time-to-Live é chamado de limite de saltos.

# *Mensagens ICMPv6*

- As mensagens informativas e de erro encontradas no ICMPv6 são muito semelhantes às mensagens de controle e de erros implementadas pelo ICMPv4. 
- No entanto, o ICMPv6 tem funcionalidade aprimorada e novos recursos que não são encontrados no ICMPv4. As mensagens ICMPv6 são encapsuladas no IPv6.
- As mensagens entre um roteador IPv6 e um dispositivo IPv6, incluindo alocação de endereços dinâmicos, são as seguintes:
	- Mensagem de Solicitação de Roteador (RS)
	- Mensagem de Anúncio de Roteador (RA)
- As mensagens entre dispositivos IPv6, incluindo detecção de endereço duplicado e resolução de endereço são as seguintes:
	- Mensagem de Solicitação de vizinhos (NS)
	- Mensagem de Anúncio de vizinhos (NA)