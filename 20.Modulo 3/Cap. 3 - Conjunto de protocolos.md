# *Conjunto de protocolos de rede*

- Os conuuntos de protocolos são projetados para poderem trabalhar entre si sem problemas. Um conjunto de protocolos é um grupo de protocolos inter-relacionados necessários para executar uma função de comunicação.
- Uma das melhores maneiras de visualizar como os protocolos dentro de uma suíte interagem é ver a interação como uma pilha. Uma pilha de protocolos mostra como os protocolos individuais dentro de uma suíte são implementados. Os protocolos são visualizados em termos de camadas, com cada serviço de nível superior, dependendo da funcionalidade definida pelos protocolos mostrados nos níveis inferiores.

# *Evolução dos conjuntos de protocolos*

- Uma suíte de protocolos é um grupo de protocolos que funcionam em conjunto para fornecer serviços abrangentes de comunicação em redes. Desde a década de 1970 há vários pacotes de protocolos diferentes, alguns desenvolvidos por uma organização de padrões e outros desenvolvidos por vários fornecedores. 
- Durante a evolução das comunicações em rede e da Internet, houveram vários conjuntos de protocolos concorrentes. 
- ![[suite de protocolos.png]]

# *Exemplo de protocolo TCP/IP*

- Os protocolos TCP / IP estão disponíveis para as camadas de aplicativo, transporte e Internet. Não há protocolos TCP/IP na camada de acesso à rede. Os protocolos LAN da camada de acesso à rede mais comuns são os protocolos Ethernet e WLAN (LAN sem fio). Os protocolos da camada de acesso à rede são responsáveis por entregar o pacote IP pela mídia física.
- A figura mostra um exemplo dos três protocolos TCP/IP usados para enviar pacotes entre o navegador da Web de um host e o servidor web. HTTP, TCP e IP são os protocolos TCP/IP usados. Na camada de acesso à rede, Ethernet é usada no exemplo. No entanto, isso também pode ser um padrão sem fio, como WLAN ou serviço celular.
- ![[protocolo tcp-ip.png]]

# *Suítes de Protocolos TCP/IP*

- Hoje, o conjunto de protocolos TCP/IP inclui muitos protocolos e continua a evoluir para oferecer suporte a novos serviços. A Figura mostra alguns dos mais populares.
- ![[protocolo tcp-ip atual.png]]
- TCP/IP é um conjunto de protocolos usados pela Internet e as redes de hoje. O TCP/IP tem dois aspectos importantes para fornecedores e fabricantes:

### **Conjunto de protocolos de padrão aberto**

- Está disponível gratuitamente ao público e pode ser usado por qualquer fornecedor em seu hardware ou software. 

### **Conjunto de protocolos com base em padrões**

- Endossado pela indústria de rede e aprovado por uma organização de padrões. Isso garante que produtos de diferentes fabricantes possam interoperar com êxito. 

## **Camada de aplicação**

### **Sistemas de nomes**

- <mark style="background: #FFB86CA6;">DNS</mark> - Domain Name Service converte nomes de domínios em endereços IP. 

### **Configuração de hosts**

- <mark style="background: #FFB86CA6;">DHCPv4</mark> - Dynamic Host Configuration Protocol version 4 atribui dinamicamente endereços IPv4 aos clientes DHCPv4 na inicialização permite que os endereços sejam reutilizados quando não forem mais necessários. 
- <mark style="background: #FFB86CA6;">DHCPv6</mark> - Dynamic Host Configuration Protocol version 6 é semelhante ao DHCPv4 porém ele utiliza o IPv6 ao invés do IPv4.
- <mark style="background: #FFB86CA6;">SLAAC</mark> - Stateless Address Autoconfiguration é um método que permite um dispositivo obtenha suas informações de endereçamento IPv6 sem usar um servidor DHCPv6. 

### **E-mail**

- <mark style="background: #FFB86CA6;">SMTP</mark> - Simple Male Transfer Protocol permite os clientes enviarem e-mail para um servidor de e-mail e estes para outros servidores.
- <mark style="background: #FFB86CA6;">POP3</mark> - Post Office Protocol version 3 permite os clientes recuperarem e-mails de um servidor de email e baixarem o email para o aplicativo de email local do cliente. 
- <mark style="background: #FFB86CA6;">IMAP</mark> - Internet Message Access Protocol permite os clientes acessarem o email armazenados em um servidor de email e também mantenham o email dentro dele. 

### **Transferência de arquivos**

- <mark style="background: #FFB86CA6;">FTP</mark> - File Transfer Protocol permite que o usuário em um host acesse e transfira arquivos para e de outros host em uma rede. O FTP é um protocolo de entrega de arquivos confiável, orientado a conexão e reconhecido. 
- <mark style="background: #FFB86CA6;">SFTP</mark> - Secure File Transfer Protocol. Como uma extensão do protocolo Secure Shell (SSH), o SFTP pode ser usado para estabelecer uma sessão segura de transferência de arquivos na qual a transferência é criptografada.
- <mark style="background: #FFB86CA6;">TFTP</mark> - Trivial File Transfer Protocol é um protocolo de transferência de arquivos simples e sem conexão com entrega de arquivos não confirmada e de melhor esforço. Ele usa menos sobrecarga que o FTP.

### **Web e serviço web**

- <mark style="background: #FFB86CA6;">HTTP</mark> - HyperText Transfer Protocol é um conjunto de regras para troca de texto, imagens, som, vídeo e outros arquivos multimídia na World Wide Web. 
- <mark style="background: #FFB86CA6;">HTTPS</mark> - HTTP Seguro. Uma forma segura do HTTP que criptografa os dados que são enviados pelas redes. 
- <mark style="background: #FFB86CA6;">REST</mark> - Representation State Tranfer é um serviço web que utiliza interfaces de programação de aplicações (APIs) e pedidos HTTP para criar aplicações web. 

## **Camada de transporte**

### **Conexão orientada**

- <mark style="background: #FFB86CA6;">TCP</mark> - Transfer Control Protocol permite comunicação entre processos executados em hosts separados e fornece transmissões confiáveis e reconhecidas que confirmam a entrega bem sucedida. 

### **Sem conexão**

- <mark style="background: #FFB86CA6;">UDP</mark> - User Datagram Protocol permite que um processo em execução em um host envie pacotes para um processo em execução em outro host. UDP não confirma transmissão bem sucedida do datagrama.

## **Camada de Internet**

### **Internet Protocol**

- <mark style="background: #FFB86CA6;">IPv4</mark> - Internet Protocol version 4. Recebe segmentos de mensagem da camada de transporte, empacota mensagens em pacotes e endereça pacotes para entrega de ponta a ponta através de uma rede. O IPv4 usa um endereço de 32 bits.
- <mark style="background: #FFB86CA6;">IPv6</mark> - IP vension 6. Semelhante ao IPv4, mas usa um endereço de 128 bits.
- <mark style="background: #FFB86CA6;">NAT</mark> - Network Address Translation. Converte endereços IPv4 de uma rede privada em endereços IPv4 públicos globalmente exclusivos.

### **Mensagens**

- <mark style="background: #FFB86CA6;">ICMPv4</mark> - Internet Control Message Protocol for IPv4. Fornece feedback de um host de destino para um host de origem sobre erros na entrega de pacotes.
- <mark style="background: #FFB86CA6;">ICMPv6</mark> - Internet Control Message Protocol for IPv6. Funcionalidade semelhante ao ICMPv4, mas é usada para pacotes IPv6.
- <mark style="background: #FFB86CA6;">ICMPv6 ND</mark> - ICMPv6 Neighbor Discovery. Inclui quatro mensagens de protocolo que são usadas para resolução de endereço e detecção de endereço duplicado.

### **Protocolos de Roteamento**

- <mark style="background: #FFB86CA6;">OSPF</mark> - Open Shortest Path First. Protocolo de roteamento de estado de link que usa um experimento hierárquico baseado em áreas. OSPF é um protocolo de roteamento interno padrão aberto.
- <mark style="background: #FFB86CA6;">EIGRP</mark> - Enhanced Interior Gateway Routing Protocol. Um protocolo de roteamento de padrão aberto desenvolvido pela Cisco que usa uma métrica composta com base na largura de banda, atraso, carga e confiabilidade.
- <mark style="background: #FFB86CA6;">BGP</mark> - Border Gateway Protocol. Um protocolo de roteamento de gateway externo padrão aberto usado entre os Internet Service Providers (ISPs). O BGP também é comumente usado entre os ISPs e seus grandes clientes particulares para trocar informações de roteamento.

## **Camada de Acesso à rede**

### **Resolução de endereços**

- <mark style="background: #FFB86CA6;">ARP</mark> - Address Resolution Protocol. Fornece mapeamento de endereço dinâmico entre um endereço IPv4 e um endereço de hardware.
- <mark style="background: #FFF3A3A6;">Observação</mark>: Você pode ver outro estado de documentação que o ARP opera na Camada da Internet (Camada OSI 3). No entanto, neste curso, afirmamos que o ARP opera na camada de Acesso à Rede (OSI Camada 2) porque seu objetivo principal é descobrir o endereço MAC do destino. Um endereço MAC é um endereço da camada 2.

### **Protocolos de link de dados**

- <mark style="background: #FFB86CA6;">Ethernet</mark> - Define as regras para os padrões de fiação e sinalização da camada de acesso à rede.
- <mark style="background: #FFB86CA6;">WLAN</mark> - Wireless LAN. Define as regras para sinalização sem fio nas frequências de rádio de 2,4 GHz e 5 GHz.