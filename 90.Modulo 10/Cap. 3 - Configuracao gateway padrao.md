# *Gateway padrão em um host*

- O gateway padrão é geralmente um roteador em uma rede LAN que é usado para se comunicar com outras redes. Caso uma rede tenha mais de um roteador, um deles deve ser configurado como o gateway padrão. 

# *Gateway padrão em um switch*

- Um comutador que interconecta computadores clientes geralmente é um dispositivo da Camada 2. Como tal, um switch de Camada 2 não precisa de um endereço IP para funcionar corretamente. No entanto, uma configuração IP pode ser configurada em um switch para dar acesso remoto a um administrador ao switch.
- Para se conectar e gerenciar um switch em uma rede IP local, ele deve ter uma interface virtual de switch (SVI) configurada. O SVI é configurado com um endereço IPv4 e uma máscara de sub-rede na LAN local. O switch também deve ter um endereço de gateway padrão configurado para gerenciar remotamente o switch de outra rede.
- O comando para configurar o gateway padrão em um switch é <mark style="background: #ABF7F7A6;">ip default-gateway {ip-address}</mark>. Esse comando é executado na <mark style="background: #BBFABBA6;">configuração global</mark>. 