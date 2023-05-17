# *Desição de encaminhamento do host*

- Os pacotes IPv4 e IPv6 são sempre criados no host de origem. Ele deve ser capaz de encaminhar o pacote para o host destino e para que isso aconteça, os dispositivos finais criam sua própria tabela de roteamento. 
- Os possíveis destinatários para os hosts de origem são:
	- Ele mesmo - o host origem pode fazer um ping nele mesmo usando o IPv4 especial 127.0.0.1 ou o IPv6 ::1 que é referido como a interface de loopback. 
	- Host local - host destino está na mesma rede local que o host origem.
	- Host remoto - o Host destino está em uma rede diferente da do host origem.
- O método para determinar qual o possível destinatário varia com a versão IP.
- O dispositivo final de origem usa a máscara de sub-rede e seu próprio IPv4 juntamente com o IPv4 destino para fazer essa determinação.
- Para o IPv6, o roteador local anuncia o endereço de rede local para todos os dispositivos na rede.

# *Gateway Padrão*

- É o roteador ou switch de camada 3 que roteia os dados para outra rede. 

# *O host direciona para o gateway padrão*

- Uma tabela de roteamento de host normalmente inclui um gateway padrão.
- A configuração do gateway padrão cria uma rota padrão na tabela de roteamento do computador. Uma rota padrão é a rota ou o caminho que o computador usa quando tenta entrar em contato com uma rede remota.

# *Tabela de Roteamento dos hosts*

- A inserção do comando **netstat -r** ou o comando equivalente **route print** exibe três seções relacionadas às conexões de rede TCP / IP atuais:

### **Lista de Interfaces**

- Lista o endereço MAC e o número de interface atribuído de todas as interfaces com capacidade de rede no host, incluindo adaptadores Ethernet, Wi-Fi e Bluetooth.

### **Tabela de rotas IPv4**

- Lista todas as rotas IPv4 conhecidas, incluindo conexões diretas, rede local e rotas padrão locais.

### **Tabela de rotas IPv6**

- Lista todas as rotas IPv6 conhecidas, incluindo conexões diretas, rede local e rotas padrão locais.