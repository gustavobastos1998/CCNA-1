# *Domínios de transmissão e segmentação*

- Em uma LAN Ethernet, os dispositivos usam transmissões e o Protocolo de Resolução de Endereços (ARP) para localizar outros dispositivos. O ARP envia difusões da Camada 2 para um endereço IPv4 conhecido na rede local para descobrir o endereço MAC associado. Os dispositivos em LANs Ethernet também localizam outros dispositivos usando serviços. Um host normalmente adquire sua configuração de endereço IPv4 usando o protocolo DHCP (Dynamic Host Configuration Protocol) que envia difusões na rede local para localizar um servidor DHCP.

# *Problemas com grandes domínios de broadcast*

- Se uma rede for grande demais isso pode ser um problema. Quando os hosts gerarem broadcasts em excesso a rede será afetada negativamente. Isso resulta em operações lentas de rede. 
- ![[dominio broadcast grande.png]]
- A solução para esse problema é reduzir o tamanho da rede para criar domínios de broadcast menores. Esse processo se chama divisão em sub-rede. 
- Na figura acima, a LAN 1 tem prefixo 16 permitindo mais de 400 hosts na mesma rede. Porém, ao dividir a rede em duas, cada uma suportaria a metade dos quadros enviados pela rede, tornando as operações de rede mais viáveis. 
- ![[divisao em subrede.png]]
- Observação: os termos sub-rede e rede costumam ser usados de maneira intercambiável. A maioria das redes são uma sub-rede de um bloco de endereços maior.

# *Razões para segmentar redes*

- A divisão em sub-redes reduz o tráfego total da rede e melhora seu desempenho. Além disso, permite que o administrador implemente políticas de segurança como, por exemplo, quais sub-redes podem ou não se comunicar com quais sub-redes. 
- Há diversas maneiras em que as redes podem ser divididas, alguns exemplos são:

### **Localização**

- ![[divisao rede por localizacao.png]]

### **Grupo ou função**

- ![[divisao rede por grupo ou funcao.png]]

### **Tipo de dispositivo**

- ![[divisao rede por tipo de dispositivo.png]]