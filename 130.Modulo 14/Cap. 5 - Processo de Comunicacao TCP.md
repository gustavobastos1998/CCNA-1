# *Estabelecimento de Conexão TCP*

- Nas conexões TCP, o cliente host estabelece a conexão com o servidor usando o processo de three way handshake.
- O three way handshake valida se o host de destino está disponível para comunicação. 

### **Etapa 1. SYN**

- O cliente iniciador requisita uma sessão de comunicação cliente-servidor.
- ![[etapa SYN.png]]

### **Etapa 2. ACK e SYN**

- O servidor confirma a sessão de comunicação cliente-servidor e requisita uma sessão de comunicação de servidor-cliente.
- ![[etapa SYN ACK.png]]

### **Etapa 3. ACK**

- O cliente iniciador confirma a sessão de comunicação de servidor-cliente.
- ![[etapa ACK.png]]

# *Encerramento da sessão*

- Para encerrar a comunicação, uma flag de controle Finish (FIN) deve ser ligada no cabeçalho do segmento. 
- Para terminar cada sessão TCP de uma via, um handshake duplo, consistindo de um segmento FIN e um segmento ACK (Acknowledgment) é usado.
- Portanto, quatro trocas são necessárias para finalizar ambas as sessões. Tanto o cliente quanto o servidor podem iniciar o encerramento. São quatro etapas, ou seja, duas two way handshake. FIN, ACK e resposta ACK, duas vezes.

### **Etapa 1. FIN**

- Quando um host não tem mais dados para enviar no fluxo, ele envia um segmento com uma flag FIN.
- ![[ETAPA 1-FIN.png]]

### **Etapa 2. ACK**

- O outro host envia um ACK para confirmar o recebimento de FIN para encerrar a sessão.
- ![[ETAPA 2-ACK.png]]

### **Etapa 3. FIN**

- O segundo host também envia um FIN ao primeiro para encerrar a sessão.
- ![[ETAPA 3-FIN.png]]

### **Etapa 4. ACK**

- O primeiro host envia um ACK para reconhecer o FIN do segundo.
- ![[ETAPA 4-ACK.png]]

# *Análise do three way handshake TCP*

- O TCP é um protocolo full-duplex, em que cada conexão representa duas sessões de comunicação unidirecional.
- Estas são as funções do three way handshake:
	- Estabelece que o dispositivo de destino está presente na rede.
	- Ele verifica se o dispositivo de destino possui um serviço ativo e está aceitando solicitações no número da porta de destino que o cliente inicial pretende usar.
	- Ele informa ao dispositivo de destino que o cliente de origem pretende estabelecer uma sessão de comunicação nesse número de porta.

### **Campo de bits de controle**

- Também conhecidos como as flags do TCP. Há 6 bits de controle sinalizadores:
	- **URG** - Campo de ponteiro urgente significativo.
	- **ACK** - Indicador de confirmação usado no estabelecimento de conexão e encerramento de sessão.
	- **PSH** - Função Push.
	- **RST** - Redefina a conexão quando ocorrer um erro ou tempo limite.
	- **SYN** - Sincronizar números de sequência usados no estabelecimento de conexão.
	- **FIN** - Não há mais dados do remetente e usados no encerramento da sessão.
- O campo de bits de controle tem 6 bits. Cada um deles pode ser 1 ou 0 e representam uma flag do TCP. 
- ![[flags tcp.png]]