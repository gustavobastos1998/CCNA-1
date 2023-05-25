# *Endereços IPv4 públicos e privados*

- Assim como existem diferentes maneiras de transmitir um pacote IPv4, existem também diferentes tipos de endereços IPv4. Alguns endereços IPv4 não podem ser usados para sair para a Internet, e outros são especificamente alocados para roteamento para a Internet.
- Endereços IPv4 públicos são endereços roteados globalmente entre os roteadores do provedor de serviços de Internet (ISP). No entanto, nem todos os endereços IPv4 disponíveis podem ser usados na Internet.
- Existem blocos de endereços (conhecidos como endereços privados) que são usados pela maioria das organizações para atribuir endereços IPv4 a hosts internos.
- ![[private address block.png]]

# *Roteamento para a Internet*

- A maioria das redes internas, de grandes empresas a redes domésticas, usa endereços IPv4 privados para endereçar todos os dispositivos internos (intranet), incluindo hosts e roteadores. No entanto, os endereços privados não são globalmente roteáveis.
- Quando um pacote IP é formado, o endereço de origem é o privado enquanto o destino é o IP público (globalmente roteável).
- ![[private IPv4 and NAT.png]]
- Antes que o ISP possa encaminhar esse pacote, ele deve traduzir o endereço IPv4 de origem, que é um endereço privado, para um endereço IPv4 público usando a Conversão de Endereços de Rede (NAT). O NAT é usado para converter entre endereços IPv4 privados e IPv4 públicos.

# *Endereços IPv4 de uso especial*

- Os endereços de loopback (127.0.0.0 / 8 ou 127.0.0.1 a 127.255.255.254) são mais comumente identificados como apenas 127.0.0.1, esses são endereços especiais usados por um host para direcionar o tráfego para si próprio. Por exemplo, ele pode ser usado em um host para testar se a configuração TCP / IP está operacional. 
- Os endereços locais de link (169.254.0.0 / 16 ou 169.254.0.1 a 169.254.255.254) são mais conhecidos como endereços de endereçamento IP privado automático (APIPA) ou endereços auto-atribuídos. Eles são usados por um cliente DHCP do Windows para auto-configurar no caso de não existirem servidores DHCP disponíveis. Endereços de link local podem ser usados em uma conexão ponto a ponto, mas não são comumente usados para esse fim.

# *Endereços Classful Legado*

### **Classe A (0.0.0.0/8 ate 127.0.0.0/8)**

- Para redes extremamente grandes. Por seu prefixo ser 8, o primeiro octeto indica a rede enquanto os outros 3 são usados para designar hosts únicos, podendo existir mais de 16 milhões.

### **Classe B (128.0.0.0/16 ate 191.255.0.0/16)**

- Para redes grandes podendo ter aproximadamente 65000 endereços de hosts. 

### **Classe C (192.0.0.0/24 ate 233.255.255.0/24)**

- Para redes pequenas usadas em LANs domésticas e comerciais. Capacidade de no máximo 254 hosts. 

## *Observação*

- Há também um bloco multicast de Classe D que consiste em 224.0.0.0 a 239.0.0.0 e um bloco de endereço experimental de Classe E que consiste em 240.0.0.0 - 255.0.0.0.

# *Atribuição de endereços IP*

- Endereços IPv4 públicos são endereços roteados globalmente pela Internet. Endereços IPv4 públicos devem ser exclusivos.
- ![[regional internet registries.png]]