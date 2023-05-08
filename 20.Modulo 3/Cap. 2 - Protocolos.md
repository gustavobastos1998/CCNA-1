# *Visão geral do protocolo de rede*

- Vários tipos de protocolos são necessários para habilitar a comunicação entre redes. Dentre eles temos:

### **Protocolos de comunicação em rede**

- Protocolo que permite dois ou mais dispositivos se comunicarem através de uma ou mais redes. A família de tecnologias Ethernet envolve uma variedade de protocolos como IP, Transmission Control Protocol (TCP), HyperText Protocolo de transferência (HTTP) e muito mais.

### **Protocolos de segurança de rede**

- Protocolos protegem os dados para fornecer autenticação, integridade dos dados e criptografia de dados. Exemplos de protocolos seguros incluem o Secure Shell (SSH), SSL (Secure Sockets Layer) e TLS (Transport Layer Security).

### **Protocolos de roteamento**

- Protocolos permitem que os roteadores troquem informações de rota, compare caminho e, em seguida, selecionar o melhor caminho para o destino remota. Exemplos de protocolos de roteamento incluem Open Shortest Path First (OSPF) e Border Gateway Protocol (BGP).

### **Protocolos de descoberta de serviço**

- Protocolos são usados para a detecção automática de dispositivos ou serviços. Exemplos de protocolos de detecção de serviços incluem Host dinâmico Protocolo de Configuração (DHCP) que detecta serviços para endereço IP alocação e Sistema de Nomes de Domínio (DNS) que é usado para executar conversão de nome para endereço IP.

# *Funções de protocolo de rede*

### **Endereçamento**

- Identifica o remetente e o destinatário pretendido da mensagem usando um esquema de endereçamento definido. Exemplos de protocolos que fornecem incluem Ethernet, IPv4 e IPv6.

### **Confiabilidade**

- Esta função fornece mecanismos de entrega garantidos em caso de mensagens são perdidos ou corrompidos em trânsito. O TCP fornece entrega garantida.

### **Controle de fluxo**

- Esta função garante que os fluxos de dados a uma taxa eficiente entre dois dispositivos de comunicação. O TCP fornece serviços de controle de fluxo.

### **Sequenciamento**

- Esta função rotula exclusivamente cada segmento de dados transmitido. Usa as informações de sequenciamento para remontar as informações corretamente. Isso é útil se os segmentos de dados forem perdidos, atrasados ou recebidos fora de ordem. O TCP fornece serviços de sequenciamento.

### **Detecção de erros**

- Esta função é usada para determinar se os dados foram corrompidos durante transmissão. Vários protocolos que fornecem detecção de erros incluem Ethernet, IPv4, IPv6 e TCP.

### **Interface de aplicação**

- Esta função contém informações usadas para processo a processo comunicações entre aplicações de rede. Por exemplo, ao acessar uma página da Web, protocolos HTTP ou HTTPS são usados para se comunicar entre o processos da Web do cliente e do servidor.

# *Interação de protocolos*

- Ao enviar uma mensagem pela rede de computadores, diversos protocolos são utilizados com suas próprias funções estabelecidas. 

### **HTTP**

- HyperText Transfer Protocol controla a maneira como um servidor web e um cliente interagem. O HTTP define conteúdo e formatação das solicitações e respostas trocadas entre cliente e servidor. Tanto o cliente quanto o servidor web implementam HTTP como parte da aplicação. 

### **TCP**

- Transmission Control Protocol gerencia as conversas individuais. O TCP é responsável por garantir a entrega confiável das informações assim como o gerenciamento do controle de fluxo entre os dispositivos. 

### **IP**

- Internet Protocol é responsável por enviar a mensagem da origem ao destino. IP é usado em roteadores para encaminhar as mensagens em várias redes. 

### **Ethernet**

- Responsável por entregar mensagens de uma NIC (placa de rede) para outra na mesma rede local Ethernet. 

