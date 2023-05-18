# *Visão geral do ARP*

- O Protocolo de Resolução de Endereços (ARP) é usado para determinar o endereço MAC de um IPv4 do dispositivo de destino conhecido. Descoberta de vizinhos (ND) é usado para determinar o endereço MAC de um endereço IPv6 do dispositivo de destino conhecido.
- Para enviar um pacote para outro host na mesma rede IPv4 local, um host deve saber o endereço IPv4 e o endereço MAC do dispositivo de destino. Os endereços IPv4 de destino do dispositivo são conhecidos ou resolvidos pelo nome do dispositivo. No entanto, os endereços MAC devem ser descobertos.
- Um dispositivo utiliza o protocolo ARP (Address Resolution Protocol) para determinar o endereço MAC de destino de um dispositivo local quando conhece o endereço IPv4.
- O ARP mantém uma tabela de mapeamento de endereços IPv4 para MAC.

# *Funções do ARP*

- Quando um pacote é enviado à camada de enlace de dados para ser encapsulado em um quadro Ethernet, o dispositivo consulta uma tabela em sua memória para encontrar o endereço MAC que é mapeado para o endereço IPv4. Esta tabela é armazenada temporariamente na memória RAM e denominada tabela ARP ou cache ARP.
- Caso os dois computadores estejam na mesma rede, o PC de origem apenas busca em sua tabela ARP o IPv4 do destino.
- Caso os dois computadores estejam em redes diferentes, o PC de origem pesquisará o endereço IPv4 na tabela ARP do gateway padrão.
- Cada entrada (linha) da tabela ARP vincula um endereço IPv4 a um endereço MAC. Chamamos a relação entre os dois valores de um mapa.
- A tabela ARP salva (armazena em cache) temporariamente o mapeamento dos dispositivos da LAN.

# *Solicitação ARP*

- As mensagens do ARP são encapsuladas diretamente em um quadro Ethernet. Não há cabeçalho IPv4. A requisição ARP é encapsulada em um quadro Ethernet usando as seguintes informações de cabeçalho:
	- **Endereço MAC de destino -** Este é um endereço de broadcast FF-FF-FF-FF-FF-FF, exigindo que todas as NICs Ethernet na LAN aceitem e processem a solicitação ARP.
	- **Endereço MAC de origem** - Este é o endereço MAC do remetente da solicitação ARP.
	- **Tipo** - As mensagens ARP têm um campo de tipo 0x806. Ele informa à NIC de recebimento que a parte de dados do quadro precisa ser transferida para o processo ARP.
- ARP é uma transmissão, isso significa que todas as portas de um switch serão inundadas, exceto a porta de entrada. Todos os dispositivos da LAN devem processar a requisição ARP e informar o MAC caso o IPv4 seja o requerido no ARP.
- Somente um dispositivo responderá. Roteadores não encaminhará broadcasts pelas outras interfaces. 

# *Operação do ARP*

- A resposta ARP é encapsulada em um quadro Ethernet usando as seguintes informações de cabeçalho:
	- **Endereço MAC de destino** - Este é o endereço MAC do remetente da solicitação ARP.
	- **Endereço MAC de origem** - Este é o endereço MAC do remetente da resposta ARP.
	- **Tipo** - As mensagens ARP têm um campo de tipo 0x806. Ele informa à NIC de recebimento que a parte de dados do quadro precisa ser transferida para o processo ARP.
- Apenas quem fez a requisição ARP receberá a resposta. Após receber a resposta ARP unicast, o dispositivo adicionará o IPv4 e o endereço MAC à sua tabela ARP. Agora com o MAC e o IPv4 em mãos, o quadro de enlace de dados pode ser feito, encapsulando o pacote de rede. 
- Se nenhum dispositivo responder à requisição ARP, o pacote será descartado porque não será possível criar um quadro.
- Todas as entradas na tabela ARP tem um tempo de vida. Caso uma delas não receba um quadro durante seu período de vida, a entrada é retirada da tabela ARP.
- Além disso, entradas de mapa estáticas podem ser inseridas em uma tabela ARP, mas isso é raro. As entradas estáticas na tabela ARP não expiram com o tempo e devem ser removidas manualmente.
- **Observação**: O IPv6 usa um processo semelhante ao ARP para IPv4, conhecido como ND (ICMPv6 Descoberta de vizinhos). O IPv6 usa mensagens de requisição e de anúncio de vizinho, semelhantes a solicitações ARP e respostas ARP no IPv4.

# *Função ARP nas comunicações remotas*

- Caso o IPv4 de destino não esteja na rede local, ele deverá encaminhar o quadro para o gateway padrão.
- Quando um host cria um pacote para um destino, ele compara o IPv4 destino com o seu próprio para determinar se estão na mesma rede. Caso não esteja, a origem utiliza a tabela ARP e encaminha o quadro para o gateway padrão. 
- Caso o MAC do gateway padrão não esteja em sua tabela, ele fará o processo de ARP para determinar um endereço MAC do gateway padrão.

# *Problemas de ARP - transmissões de ARP e falsificação de ARP*

- Caso um grande número de dispositivos precisem acessar serviços de rede ao mesmo tempo, pode haver alguma redução no desempenho por um curto período de tempo. 
- Depois que os dispositivos enviarem os broadcasts ARP iniciais e tiverem reconhecido os endereços MAC necessários, qualquer impácto na rede será minimizado.

### **Falsificação ARP**

- É um ataque de envenenamento por ARP. O ataque funciona da seguinte forma, quando uma requisição broadcast ARP é mandada na rede, um dos dispositivos, que não seja o IPv4 na requisição, responde como se fosse ele. Dessa maneira, o dispositivo que fez a requisição ARP adiciona à sua tabela o MAC errado para o IP requerido. 
- Com o ataque bem sucedido, quando o dispositivo quiser mandar alguma informação para, por exemplo, o gateway padrão o pacote irá ser enviado para o MAC do atacante.
- ![[falsificacao arp.png]]

