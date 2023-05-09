# *Segmentando mensagens*

- Segmentação é o processo de dividir um fluxo de dados em unidades menores para transmissões através da rede. A segmentação é necessária porque as redes de dados usam o conjunto de protocolos TCP/IP enviar dados em pacotes IP individuais. 
- Cada pacote é enviado separadamente, semelhante ao envio de uma carta longa como uma série de cartões postais individuais. Pacotes que contêm segmentos para o mesmo destino podem ser enviados por caminhos diferentes.

### **Aumento na velocidade**

- Como o fluxo de grande dados é segmentado em pacotes, grande quantidade de dados podem ser enviadas pela rede sem amarrar um link de comunicação. 
- Isso permite que muitas conversas diferentes sejam intercaladas na rede chamada multiplexação.

### **Aumento na eficiência**

- Se um único segmento não conseguir alcançar seu destino devido a uma falha na rede ou no congestionamento da rede, somente esse segmento precisa ser retransmitido em vez de reenviar todo o fluxo de dados.

# *Sequenciamento*

- Nas comunicações em rede, cada segmento da mensagem deve passar por um processo de enumeração para garantir que chegue ao destino correto e possa ser remontado no conteúdo da mensagem original, conforme mostrado na figura. O TCP é responsável por sequenciar os segmentos individuais.
- ![[sequenciamento.png]]

# *Unidade de dados de protocolo*

- À medida que os dados da aplicação são passados pela pilha de protocolos em seu caminho para serem transmitidos pelo meio físico de rede, várias informações de protocolos são adicionadas em cada nível. Isso é conhecido como o processo de encapsulamento.
- O formato que uma parte de dados assume em qualquer camada é chamado de unidade de dados de protocolo (PDU). Durante o encapsulamento, cada camada sucessora encapsula a PDU que recebe da camada superior de acordo com o protocolo sendo usado.
- ![[PDU.png]]

# *Exemplo de Encapsulamento*

- Quando as mensagens estão sendo enviadas em uma rede, o processo de encapsulamento funciona de cima para baixo. Em cada camada, as informações da camada superior são consideradas dados encapsulados no protocolo. Por exemplo, o segmento TCP é considerado dados dentro do pacote IP.
- Um website sendo enviado do servidor para o cliente é encapsulado. O dado da camada de aplicação é justamente a página web e quando vai para a camada de transporte é encapsulada e depois para a camada de rede onde o protocolo IP encapsula o pacote novamente com suas informações necessárias para regir seu papel. 

# *Exemplo de desencapsulamento*

- Esse processo é revertido no host de recebimento e é conhecido como desencapsulamento. O desencapsulamento é o processo usado por um dispositivo receptor para remover um ou mais cabeçalhos de protocolo. Os dados são desencapsulados à medida que se movem na pilha em direção à aplicação do usuário final.
- O website chegando ao cliente é um exemplo de desencapsulamento. Aqui, o processo inverso é feito. Os cabeçalhos dos protocolos informam todas as informações necessárias e prevista que devem ser checadas para que o dispositivo destino saiba que é esse pacote que ele estava esperando. Por exemplo, o protocolo Ethernet informa os MAC address das portas do remetente e do destino, o IP informa quais os endereços IPv4 da origem e destinatário. Caso essas informações sejam satisfeitas, o pacote vai sendo desencapsulado para que a próxima camada seja averiguada.