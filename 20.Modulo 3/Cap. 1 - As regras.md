# *Fundamentos das Comunicações*

- Não basta existir uma conexão entre os dispositivos, seja ela com ou sem fio, eles devem sabem como se comunicar. 
- Três elementos que formam a comunicação:

### **Fonta da Mensagem (remetente)**

- Pessoas ou dispositivos eletrônicos que presicam enviar uma mensagem para outras pessoas ou outros dispositivos.

### **Destino da Mensagem (destinatário)**

- Quem recebe a mensagem.

### **Canal**

- Mídia que fornece o caminho pelo qual a mensagem é transmitida.

# *Protocolos de comunicação*

- O envio de mensagem é regido por regras chamadas protocolos. 
- Uma analogia a comunicação de redes seria a conversa entre duas pessoas, antes da comunicação os participantes devem estabelecer como se comunicar, seja por voz, carta, sinal de fumaça o que for. Em seguida devem acordar o idioma e em seguida o remetente formata uma mensagem de forma que seja compreensível. 
- Se a mensagem for mal formatada pode ser facilmente mal interpretada. Cada uma dessas tarefas descreve protocolos usados para realizar a comunicação. 

# *Estabelecimento de regras*

- Os protocolos devem ter em conta os seguintes requisitos para entregar com êxito uma mensagem compreendida pelo receptor:
	- Um emissor e um receptor identificados;
	- Língua e gramática comum;
	- Velocidade e ritmo de transmissão;
	- Requisitos de confirmação ou recepção.

# *Requisitos de protocolo de rede*

- Os protocolos usados nas comunicações de rede compartilham muitas dessas características fundamentais. Protocolos de computador comuns incluem os seguintes requisitos:
	- Codificação de mensagens;
	- Formatação e encapsulamento de mensagens;
	- Tamanho da mensagem;
	- Tempo da mensagem;
	- Opções de envio de mensagem.

# *Codificação de Mensagens*

- Uma das primeiras etapas para enviar uma mensagem é codificá-la. A codificação é o processo de conversão de informações em outra forma aceitável para a transmissão. A decodificação reverte esse processo para interpretar as informações.
- A codificação entre hosts deve estar em um formato adequado para o meio físico. As mensagens enviadas pela rede são convertidas primeiramente em bits pelo host emissor. Cada bit é codificado em um padrão de tensões em fios de cobre, luz infravermelha em fibras ópticas ou microondas para sistemas sem fio. O host de destino recebe e decodifica os sinais para interpretar a mensagem.

# *Formatação e Encapsulamento de Mensagens*

- Quando uma mensagem é enviada da origem para o destino, deve usar um formato ou uma estrutura específica. Os formatos da mensagem dependem do tipo de mensagem e do canal usado para entregá-la.
- Internet Protocol (IP) é um protocolo com uma função semelhante ao exemplo de um envelope. Na figura, os campos do pacote IPv6 (Internet Protocol versão 6) identificam a origem do pacote e seu destino. IP é responsável por enviar uma mensagem da origem da mensagem para o destino através de uma ou mais redes.
- ![[protocolo IPv6.png]]

# *Tamanho da mensagem*

- Quando uma mensagem é longa demais ela é dividida em partes menores. Elas são chamdas de pacotes ou quadros. Essas regras de divisão em pacotes são rígidas. 
- As restrições de tamanho dos quadros exigem que o host origem divida uma mensagem longa em pedaços individuais que atendam aos requisitos de tamanho mínimo e máximo. A mensagem longa será enviada em quadros separados, e cada um contém uma parte da mensagem original. Cada quadro também terá suas próprias informações de endereço. No host destino, as partes individuais da mensagem são reconstruídas na mensagem original.

# *Temporização da mensagem*

- O tempo das mensagens também é importante ans comunicações de rede. 

### **Controle de Fluxo**

- Gerencia taxa de transmissão de dados.  Controla quanta informação pode ser enviada e a velocidade com que pode ser entregue. Existem protocolos de rede usados pelos dispositivos de origem e destino que negociam e gerenciam o fluxo de informações. 

### *Tempo limite de resposta (time-out)*

- Caso não haja uma resposta do destino dizendo que a mensagem chegou com sucesso, o remetente assume que a mensagem não foi enviada ou que algo aconteceu. Ações podem ser tomadas, com o reenvio da mensagem ou prosseguir com a conversa. Os hosts usam protocolos de rede que especificam quanto tempo devem esperar pelas respostas e que ações devem ser executadas caso haja um time-out. 

### **Método de Acesso**

- Determina quando alguém pode enviar uma mensagem. Isso deve ser explicitado para que não haja uma colisão de informações. Quando um dispositivo deseja transmitir em uma LAN sem fio, é necessário que a placa de interface de rede (NIC) da WLAN determine se a mídia sem fio está disponível.

# *Opções de Envio de Mensagem*

- A mensagem pode ser entregue de diferentes maneiras. 
- As comunicações em rede têm opções de entrega semelhantes para se comunicar. 

### **Unicast**

- Dados enviados para um único dispositivo final.

### **Multicast**

- Dados enviados para um ou mais dispositivos finais.

### **Broadcast**

- Dados enviados para todos os dispositivos finais.