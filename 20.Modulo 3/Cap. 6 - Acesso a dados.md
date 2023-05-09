# *Endereços*

- As camadas de rede e de enlace de dados são responsáveis por entregar os dados do dispositivo origem para o dispositivo destino. Conforme mostrado na figura, os protocolos nas duas camadas contêm um endereço de origem e de destino, mas seus endereços têm finalidades diferentes:
- ![[endereco enlace-rede.png]]

### **Endereços de origem e destino da camada de rede**

- Responsável por entregar pacote IP da origem ao destino.

### **Endereços de origem e destino da camada de enlace**

- Responsável por fornecer o frame de enlace de dados de uma placa de interface de rede (NIC) para outra NIC na mesma rede. 

# *Endereço Lógico da camada de rede*

- O IP contém duas partes:

### **Parte de rede (IPv4) ou prefixo (IPv6)**

- As 3 primeiras partes do endereço indica a rede na qual o endereço IP é um membro. Todos os dispositivos na mesma rede terão a mesma parte da rede no endereço. 

### **Parte do host (IPv4) ou ID da interface (IPv6)**

- O último número do endereço identifica um dispositivo específico na rede. Essa parte é exclusiva para cada dispositivo ou interface na rede.

# *Dispositivos na mesma rede*

- Exemplo de dispositivos na mesma rede: computador-1, IPv4 192.168.1.10; computador-2, IPv4 192.168.1.11
- A única coisa que os difere é o número do host localizado mais a direita do endereço.

# *Função dos endereços da camada de enlace para uma mesma rede*

- Quando os dispositivos estão na mesma rede o frame da camada de enlace será enviado diretamente ao dispositivo receptor. Pois para o protocolo Ethernet, a origem e o destino dos dispositivos envolvidos na comunicação são identificados pelo MAC ( Media Access Control) address. 
- Os endereços MAC são embutidos fisicamente na placa de interface de rede (NIC) Ethernet. 
- O MAC Ethernet do dispositivo envia o frame de link de dados com o pacote IP encapsulado. Ele é escrito em notação hexadecimal.
- Exemplo de endereço MAC: AA-AA-AA-AA-AA-AA

# *Comportamento para IPs em redes diferentes*

- A única diferença que há quando os dispositivos estão em redes diferentes é que os pacotes dos dados terão de ser enviados pelo gateway padrão. O roteador enviará os pacotes por outras redes até que cheguem no dispositivo destino. 

# *Endereços de enlace de dados*

- Conforme o pacote IP viaja do host para o roteador, de roteador para roteador e de roteador para host, em cada ponto ao longo do caminho, o pacote IP é encapsulado em um novo quadro de enlace de dados. Cada quadro de enlace de dados contém o endereço de enlace de dados origem da placa NIC que envia o quadro, e o endereço de enlace de dados destino da placa NIC que recebe o quadro.
- A camada 2, enlace de dados, só é desencapsulada ao chegar na rede certa. Pois o protocolo usado na camada de link de dados é de NIC para NIC na mesma rede. 
- O pacote IP é encapsulado em um quadro de link de dados que contém as seguintes informações de link de dados:

### **Endereço de link de dados de origem**

- O endereço físico da NIC que está enviando o quadro de link de dados.

### **Endereço de link de dados de destino**

- O endereço físico da NIC que está recebendo o quadro de link de dados. Esse endereço é o roteador do próximo salto ou o endereço do dispositivo de destino final.