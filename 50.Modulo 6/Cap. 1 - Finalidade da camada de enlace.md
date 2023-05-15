# *A camada de enlace*

- A camada de enlace de dados do modelo OSI (Camada 2) prepara os dados da rede para a rede física. Ela é responsável por controlar a transferência de quadros pelo meio físico. 
- A camada de enlace de dados é responsável pela placa de interface de rede (NIC) para comunicações de placa de interface de rede. A camada de enlace de dados faz o seguinte:
	- Permite que as camadas superiores acessem a mídia. O protocolo de camada superior não está completamente ciente do tipo de mídia que é usado para encaminhar os dados.
	- Aceita dados, geralmente pacotes de Camada 3 (ou seja, IPv4 ou IPv6), e os encapsula em quadros da Camada 2.
	- Controla como os dados são colocados e recebidos na mídia.
	- Troca quadros entre pontos de extremidade através da mídia de rede.
	- Recebe dados encapsulados, geralmente pacotes de Camada 3, e os direciona para o protocolo de camada superior apropriado.
	- Executa a detecção de erros e rejeita qualquer quadro corrompido.
- Sem a camada de enlace de dados, um protocolo de camada de rede, como o IP, teria de estar preparado para se conectar a cada tipo de meio físico que poderia existir ao longo do caminho. Além disso, toda vez que uma nova tecnologia ou meio de rede fosse desenvolvido, o IP teria que se adaptar.
- ![[enlace de dados.png]]

# *IEEE 802 subcamadas de link de dados de LAN/MAN*

- A subcamada LLC pega os dados do protocolo de rede, que geralmente é um pacote IPv4 ou IPv6, e adiciona informações de controle da camada 2 para ajudar a entregar o pacote ao nó de destino. 

## **Logical Link Control (LLC)**

- Esta subcamada IEEE 802.2 comunica entre o software de rede nas camadas superiores e o hardware do dispositivo nas camadas inferiores. Ela coloca a informação no quadro que identifica qual protocolo de camada de rede está sendo usado para o quadro. Essas informações permitem que vários protocolos da camada 3, como IPv4 e IPv6, usem a mesma interface de rede e mídia.

## **Controle de Acesso a Mídia (MAC)**

- Implementa esta subcamada (IEEE 802.3, 802.11 ou 802.15) no hardware. É responsável pelo encapsulamento de dados e controle de acesso à mídia. Ele fornece endereçamento de camada de link de dados e é integrado com várias tecnologias de camada física.
- A subcamada MAC também fornece controle de acesso a mídia, permitindo que vários dispositivos se comuniquem através de uma mídia compartilhada (half-duplex). As comunicações full-duplex não exigem controle de acesso.
- A subcamada MAC controla a NIC e outro hardware responsável pelo envio e recebimento de dados no meio LAN/MAN com ou sem fio.
- Os dois critérios para determinar o método de controle de acesso de mídia usados são: o tipo de compartilhamento de mídia envolvido e a topologia.
- O encapsulamento de dados IEEE 802.3 inclui o seguinte:
	- **Quadro Ethernet** - Esta é a estrutura interna do quadro Ethernet.
	- **Endereçamento Ethernet** - O quadro Ethernet inclui um endereço MAC de origem e de destino para fornecer o quadro Ethernet da NIC Ethernet para a NIC Ethernet na mesma LAN.
	- **Detecção de erro Ethernet** - O quadro Ethernet inclui um trailer de sequência de verificação de quadros (FCS) usado para detecção de erros.
- ![[LLC e MAC.png]]

### **Delimitação de quadros**

- O processo de enquadramento fornece delimitadores importantes para identificar campos dentro de um quadro. Esses bits de delimitação promovem a sincronização entre os nós de transmissão e de recepção.

### **Endereçamento**

- Fornece endereçamento de origem e destino para transportar o quadro da camada 2 entre dispositivos na mesma mídia compartilhada.

### **Detecção de erro**

- Inclui um trailer usado para detectar erros de transmissão.

# *Fornecimento de Acesso ao meio físico*

- Cada ambiente de rede que os pacotes encontram à medida que eles viajam de um host local a um host remoto pode ter diferentes características. Com links seriais, o método de acesso só pode consistir em uma conexão direta entre apenas dois dispositivos, geralmente dois roteadores.