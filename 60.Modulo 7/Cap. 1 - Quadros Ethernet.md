# *Encapsulamento Ethernet*

- A Ethernet é uma das duas tecnologias de LAN usadas atualmente, sendo a outra LANs sem fio (WLANs). A Ethernet utiliza comunicações com fios, incluindo par trançado, ligações de fibra óptica e cabos coaxiais.
- Ela opera na camada de enlace de dados e na camada física. É uma família de tecnologias de rede definidas nos padrões IEEE 802.2 e 802.3. 
- ![[Tecnologia ethernet.png]]

# *Subcamada MAC*

- A Ethernet herdada, usando uma topologia de barramento ou hubs, é um meio compartilhado e half-duplex. Ethernet sobre um meio half-duplex usa um método de acesso baseado em contenção, detecção de múltiplos acessos/detecção de colisão (CSMA/CD). 
- O CSMA/CD permite que vários dispositivos compartilhem o mesmo meio half-duplex, detectando uma colisão quando mais de um dispositivo tenta transmitir simultaneamente. Ele também fornece um algoritmo de recuo para retransmissão.
- As LANs Ethernet de hoje usam switches que operam em full-duplex. As comunicações full-duplex com switches Ethernet não exigem controle de acesso através do CSMA/CD.
- A subcamada MAC detecta erros em bits recebidos e usa CSMA/CD ou CSMA/CA para oferecer suporte à tecnologia Ethernet. 

# *Campos de um quadro Ethernet*

- O tamanho mínimo de quadro Ethernet é 64 bytes e o máximo é 1518 bytes. O campo de preâmbulo não é incluído ao descrever o tamanho do quadro.
- Qualquer quadro com comprimento menor que 64 bytes é considerado um"fragmento de colisão" ou um "quadro desprezível" e é automaticamente descartado pelas estações receptoras. Enquanto quadros com mais de 1.500 bytes de dados são considerados “jumbo” ou “baby giant”.
- Os quadros jumbo geralmente são suportados pela maioria dos switches e NICs Fast Ethernet e Gigabit Ethernet.
- ![[campos quadro ethernet.png]]

### **Preâmbulo e Delimitador Início de Quadro**

- O preâmbulo tem tamanho 7 bytes e o SFD 1 byte. São usados para sincronização entre os dispositivos de envio e recepção. Informam aos receptores para que estes se preparem para receber um novo quadro.
### **Endereço MAC de destino**

- Identifica a NIC do destinatário desejado. 
- O endereço no quadro é em comparação com o endereço MAC no dispositivo. Se houver uma correspondência, o aceita o quadro. Pode ser unicast, multicast ou broadcast endereço.
### **Endereço MAC de origem**

- Identifica a NIC ou interface de origem do quadro.
- Endereços de Camada 2 para o quadro. Cada endereço tem 48 bits (ou 6 octetos), expressos como 12 dígitos hexadecimais, 0-9,A-F. Um formato comum é 12:34:56:78:9A:BC. 
- Os primeiros seis números hexadecimais indicam o fabricante da placa de interface de rede (NIC) e os últimos seis números hexadecimais são o número de série dela. 
- O endereço destino pode ser broadcast, que contém todos os valores em 1, ou unicast. O endereço origem é sempre unicast.
### **Tipo/comprimento (EtherType)**

- Identifica qual protocolo está sendo usado na camada superior, camda de rede. Os valores comuns são, em hexadecimal, 0x800 para IPv4, 0x86DD para IPv6 e 0x806 para ARP.
### **Dados**

- Contém os dados encapsulados de um camada superior, que é uma PDU de Camada 3 genérica, ou mais comumente, um IPv4 pacote. 
- Todos os quadros devem ter pelo menos 64 bytes. Se um pequeno pacote for encapsulado, bits adicionais chamados pad são usados para aumentar o tamanho do quadro para este tamanho mínimo.
### **Sequência de Verificação de Quadro**

- FCS (Frame Check Sequence) é usado para detectar erros em um quadro. Ele utiliza uma verificação de redundância cíclica (CRC).
- O dispositivo de envio inclui os resultados de um CRC no campo FCS do quadro. O dispositivo receptor recebe o quadro e gera um CRC para procurar erros.
- Se o cálculo corresponder, significa que não houve erro. Cálculos que não coincidem são uma indicação de que os dados foram alterados. Portanto, o quadro é descartado.
- 