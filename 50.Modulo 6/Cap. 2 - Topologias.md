# *As topologias de WAN*

- As 3 mais comuns são: P2P, estrela e malha.

### **Topologia de estrela**

- Esta é uma versão WAN da topologia em estrela na qual um site central interconecta sites de filial através do uso de links ponto a ponto. Os sites de filiais não podem trocar dados com outros sites de filiais sem passar pelo site central.
- ![[topologia estrela.png]]

### **Topologia de malha**

- Essa topologia fornece alta disponibilidade, mas requer que todos os sistemas finais estejam interconectados a todos os outros sistemas. Portanto, os custos administrativos e físicos podem ser significativos. Cada link é essencialmente um link ponto a ponto para outro nó.
- ![[topologia de malha.png]]

# *Topologia de WAN P2P*

- As topologias ponto a ponto físicas conectam diretamente dois nós. Além disso, ao usar um protocolo de comunicação serial como o protocolo ponto a ponto (PPP), um nó não precisa determinar se um quadro de entrada é destinado a ele ou a outro nó.
- Um nó de origem e destino podem ser indiretamente conectado entre si por alguma distância geográfica, usando vários dispositivos intermediários. No entanto, o uso de dispositivos físicos na rede não afeta a topologia lógica, conforme ilustrado na figura. Na figura, adicionar conexões físicas intermediárias pode não alterar a topologia lógica. A conexão lógica ponto a ponto é a mesma.
- ![[topologia p2p.png]]

# *Topologias LAN*

- Em LANs multiacesso, os dispositivos finais (isto é, nós) são interligados usando topologias estrelares ou estrelares estendidas. 
- Neste tipo de topologia, os dispositivos finais são conectados a um dispositivo intermediário central, neste caso, um switch Ethernet. A **extended star** estende essa topologia interconectando vários switches Ethernet.
- São fáceis de instalar e são escalonaveis. 

### **Topologia de redes legadas**

- Barramento - Todos os sistemas finais são encadeados e terminados de alguma forma em cada extremidade. Os dispositivos de infraestrutura, como switches, não são necessários para interconectar os dispositivos finais. As redes Ethernet herdadas costumavam ser topologias de barramento usando cabos coaxiais, porque era barato e fácil de configurar.
- Anel - Os sistemas finais são conectados ao respectivo vizinho formando um anel. O anel não precisa ser terminado, ao contrário da topologia de barramento. As redes de interface de dados distribuídos de fibra herdada (FDDI) e Token Ring usavam topologias de anel.
- ![[topologias LAN.png]]

# *Comunicação em half-duplex e full-duplex*

- Compreender a comunicação duplex é importante ao discutir topologias de LAN porque se refere à direção da transmissão de dados entre dois dispositivos.
- É importante que duas interfaces interconectadas, como uma NIC de host e uma interface em um comutador Ethernet, operem usando o mesmo modo duplex. Caso contrário, haverá uma incompatibilidade de duplex que criará ineficiência e latência no link.

### **Comunicação Half-duplex**

- Ambos podem transmitir e receber no meio físico, porém não ao mesmo tempo. WLANs e topologias de barramento herdadas com hubs Ethernet usam o modo half-duplex.

### **Comunicação Full-duplex**

- Ambos os dispositivos podem transmitir e receber simultaneamente na mídia compartilhada. A camada de enlace de dados supõe que o meio físico está disponível para transmissão para ambos os nós a qualquer momento.

# *Métodos de controle de acesso*

- LANs Ethernet e WLANs são exemplos de redes multiacesso. Uma rede multiacesso é uma rede que pode ter dois ou mais dispositivos finais tentando acessar a rede simultaneamente.

### **Acesso baseado em contenção**

- Em redes multiacesso baseadas em contenção, todos os nós estão operando em half-duplex, competindo pelo uso do meio.
- Exemplos de métodos de acesso baseados em contenção incluem o seguinte:
	- Acesso múltiplo com detecção de colisão (CSMA/CD) usado em LANs Ethernet de topologia de barramento herdado.
	- Acesso múltiplo por operadora com preveção de olisão (CSMA/CA) usado em WLANs.

### **Acesso controlado**

- Em uma rede multiacesso controlada, cada nó tem seu próprio tempo para usar o meio. Esses tipos determinísticos de redes herdadas são ineficientes porque um dispositivo deve aguardar sua vez para acessar o meio.

# *Acesso baseado em conteção (CSMA/CD)*

- Para LANs Ethernet herdadas, ambos os dispositivos detectam a colisão na rede. Esta é a parte de detecção de colisão (CD) do CSMA/CD. 
- A NIC compara os dados transmitidos com os dados recebidos ou reconhecendo que a amplitude do sinal é maior que o normal na mídia. Os dados enviados por ambos os dispositivos serão corrompidos e precisarão ser reenviados.

# *Acesso baseado em contenção (CSMA/CA)*

- Outra forma de CSMA usada pelas WLANs IEEE 802.11 é o acesso múltiplo por detecção de portadora/prevenção de colisão (CSMA/CA).
- O CMSA/CA usa um método semelhante ao CSMA/CD para detectar se a mídia está livre. Em ambientes sem fio pode não ser possível para um dispositivo detectar uma colisão. 
- O CSMA/CA não detecta colisões, mas tenta evita-las esperando antes de transmitir. Cada dispositivo que transmite inclui o tempo necessário para a transmissão. Todos os outros dispositivos sem fio recebem essas informações e sabem quanto tempo a mídia ficará indisponível.
- Quer se trate de uma LAN Ethernet que use hubs, ou uma WLAN, os sistemas baseados em contenção não escalam bem sob uso intenso.