# *Topologia de pequenas redes*

- ![[topologia pequena rede.png]]
- Essa pequena rede requer um roteador, um switch e um ponto de acesso sem fio para conectar usuários com fio e sem fio. 
- Redes pequenas geralmente têm uma única conexão WAN fornecida por DSL, cabo ou conexão Ethernet.

# *Seleção de Dispositivos para uma rede pequena*

- Como redes grandes, redes pequenas exigem planejamento e design para atender aos requisitos do usuário. 
- Uma das primeiras considerações de design é o tipo de dispositivos intermediários a serem usados para oferecer suporte à rede.

### **Custo**

- O custo de um switch ou roteador é determinado por sua capacidade e recursos. Isso inclui o número e os tipos de portas disponíveis e a velocidade do backplane.
- Recursos de gerenciamento de rede, tecnologias de segurança incorporadas e tecnologias de comutação avançadas opcionais também influenciam o custo.
- Cabeamento necessário entre cada dispositivo e a quantidade de redundância a ser incorporada na rede também devem ser considerados. 

### **Velocidade e Tipos de portas/interfaces**

- A escolha do número e do tipo de portas em um roteador ou switch é uma decisão importante. Os computadores mais novos possuem NICs de 1 Gbps incorporadas. Alguns servidores podem até ter portas de 10 Gbps.
- Embora seja mais caro, a escolha de dispositivos da Camada 2 que podem acomodar velocidades maiores permite que a rede evolua sem substituir os dispositivos centrais.

### **Capacidade de expansão**

- Os dispositivos de rede estão disponíveis em configurações físicas fixas e modulares. A configuração fixa tem número e tipo específico de portas ou interfaces e não podem ser expandidos. 
- A configuração modular possui slots de expansão para novos módulos a medida que os requisitos evoluem. Os switches são disponibilizados com portas adicionais para uplinks de alta velocidade.
- Roteadores podem ser usados para conectar diferentes tipos de redes. Deve-se ter cuidado ao selecionar os módulos e interfaces apropriados para as mídias específicas.

### **Serviços e Recursos do SO**

- Os dispositivos de rede devem ter sistemas operacionais que possam suportar os requisitos da organização, como os seguintes:
	- Switching de Camada 3
	- Tradução de Endereço de Rede (NAT)
	- Protocolo de Configuração Dinâmica de Host (DHCP)
	- Segurança
	- Qualidade de Serviço (QoS – Quality-of-Service).
	- VoIP (Voice over IP)

# *Endereçamento IP para uma rede pequena*

- ![[enderecamento 3 LANs.png]]
- A organização decidiu implementar um esquema de endereçamento IP consistente para cada LAN 192.168.x.0/24 usando o seguinte plano:
- ![[tabela enderecamento IP.png]]
- A imagem a seguir demonstra como ficaria os IPs dos dispositivos da rede 192.168.2.0/24:
- ![[distribuicao IPs.png]]
- Os intervalos utilizados dos endereços IPs foram alocados deliberadamente em limites de sub rede para simplificar o tipo de grupo. Por exemplo, caso outro switch seja adicionado com endereço 192.168.2.6, para identificar todos os switchs a rede pode ser resumida como 192.168.x.4/30.

# *Redundância em uma rede pequena*

- Outra parte importante no projeto de rede é a confiabilidade. Para manter um alto grau de confiabilidade, _redundância_ é necessária no design da rede.
- A redundância elimina os pontos únicos de falha. 
- ![[redundancia.png]]
- Geralmente só há um gateway padrão. Caso o roteador falhe, toda a rede perderá conectividade com a Internet. Pode ser vantajoso contratar outro serviço provedor de Internet como backup. 

# *Gerenciamento de tráfego*

- O objetivo de um bom design de rede, mesmo para uma pequena rede, é aumentar a produtividade dos funcionários e minimizar o tempo de inatividade da rede.
- De fato, um bom design de rede implementará qualidade de serviço (QoS) para classificar o tráfego cuidadosamente de acordo com a prioridade.
- ![[gerenciamento de trafego.png]]