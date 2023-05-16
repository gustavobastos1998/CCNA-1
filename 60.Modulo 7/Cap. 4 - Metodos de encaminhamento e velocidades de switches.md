# *Métodos de encaminhamento de quadros em switches da cisco*

- Os switches usam um dos seguintes métodos de encaminhamento para o switching (comutação) de dados entre suas interfaces de rede:

### **Switching store-and-forward**

- Este método de encaminhamento de quadros recebe o quadro inteiro e calcula o CRC. O CRC usa uma fórmula matemática, baseada no número de bits (valores 1) no quadro, para determinar se o quadro recebido apresenta erro. 
- Se o CRC é válido, o switch procura o endereço de destino, que determina a interface de saída. Em seguida, o quadro é encaminhado para fora da porta correta.
- O switch store-and-forward é necessário para a análise de qualidade de serviço (QoS) em redes convergentes onde a classificação de quadros para priorização de tráfego é necessária.

### **Switching cut-through**

- Esse método de encaminhamento de quadros encaminha o quadro antes de ser totalmente recebido. Pelo menos o endereço de destino do quadro deve ser lido para que o quadro possa ser encaminhado.

# *Switching cut-through*

- O switch armazena em buffer apenas o quadro suficiente para ler o endereço MAC de destino, para que possa determinar para qual porta deve encaminhar os dados.
- O switch consulta o endereço MAC de destino na tabela de switching, determina a porta da interface de saída e encaminha o quadro ao seu destino pela porta de switch designada. O switch não realiza nenhuma verificação de erros no quadro.
- Há duas formas de switching cut-through:

### **Comutação fast-forward**

- Menor latência e encaminha o pacote imediatamente após ler seu endereço de destino. 
- Como o switching fast-forward começa o encaminhamento antes de receber todo o pacote, alguns pacotes podem ser retransmitidos com erros. Isso ocorre com pouca freqüência e a NIC de destino descarta o pacote com defeito após o recebimento.
- Esse é o método típico de switching.

### **Comutação fragment-free**

- Livre de fragmentos, o switch armazena os primeiros 64 bytes do quadro antes de encaminhar. Pode ser encarado como o meio termo entre o fast-forward e store-and-forward. 
- A maioria dos erros e as colisões de rede são encontradas nos primeiros 64 bytes. 
- O switching fragment-free tenta melhorar o switching fast-forward executando uma pequena verificação de erros nos primeiros 64 bytes do quadro para garantir que não ocorra uma colisão antes de encaminhar o quadro.
- O switching fragment-free é um compromisso entre a alta latência e a alta integridade do switching store-and-forward e a baixa latência e a integridade reduzida do switching fast-forward.

# *Buffers de memória em switches*

- O buffer pode ser usado quando a porta de destino está ocupada devido ao congestionamento. O switch armazena o quadro até que ele possa ser transmitido.
- ![[memory buffering methods.png]]
- O buffer de memória compartilhada também resulta na capacidade de armazenar quadros maiores com potencialmente menos quadros descartados. 
- Isso é importante com a comutação assimétrica, que permite taxas de dados diferentes em portas diferentes, como ao conectar um servidor a uma porta de switch de 10 Gbps e PCs a portas de 1 Gbps.

# *Configurações de Interface: velocidade e transmissão duplex*

- Duas das configurações mais básicas em um switch são as configurações de largura de banda (às vezes denominadas "velocidade") e duplex para cada porta do switch individual. 
- É fundamental a correspondência dessas configurações na porta do switch e nos dispositivos conectados, como um computador ou outro switch.
- Também existe a possibilidade de uma negociação automática. Essa opção é encontrada na maioria dos switches Ethernet e NICs. Permite que os dispositivos negociem automaticamente as melhores capacidades de velocidade e duplex.

# *MDIX Automático*

- Conexões entre dispositivos exigiam uso de cabo cruzado ou direto. O tipo de cabo dependia do tipo de dispositivos interconectados.
- Caso os dispositivos fossem os mesmos (switch conecta switch), o cabo utilizado é o cruzado. O cabo direto é usado para dispositivos diferentes.
- <mark style="background: #BBFABBA6;">OBS</mark>: uma conexão direta entre um roteador e um host requer um cabo cruzado.
- A maioria dos dispositivos de switch agora suporta o recurso de (Auto-MDIX) interface dependente automática. Quando ativado, o switch detecta automaticamente o tipo de cabo conectado à porta e configura as interfaces de acordo. 
- Com isso, você pode utilizar um cabo cruzado ou direto para conexões a uma porta 10/100/1000 Mb/s de cobre no switch, seja qual for o tipo de dispositivo na outra extremidade da conexão.