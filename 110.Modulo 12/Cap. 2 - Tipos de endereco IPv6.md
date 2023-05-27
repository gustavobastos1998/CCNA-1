# *Unicast, Multicast e Anycast*

- **Unicast** – Um endereço IPv6 unicast identifica exclusivamente uma interface em um dispositivo habilitado para IPv6.
- **Multicast** – Um endereço IPv6 multicast é usado para enviar um único pacote IPv6 para vários destinos.
- **Anycast** – Um endereço IPv6 anycast é qualquer endereço IPv6 unicast que possa ser atribuído a vários dispositivos. Um pacote enviado a um endereço de anycast é roteado para o dispositivo mais próximo que tenha esse endereço.
- Ao contrário do IPv4, o IPv6 não possui um endereço de broadcast. No entanto, há um endereço multicast para todos os nós IPv6 que fornece basicamente o mesmo resultado.

# *Comprimento do prefixo IPv6*

- No IPv4 o /24 é chamado de prefixo. No IPv6 é chamado de comprimento do prefixo. O IPv6 não usa a notação decimal com pontos da máscara de sub rede. Como o IPv4, o comprimento do prefixo é representado na notação de barra e é usado para indicar a parte da rede de um endereço IPv6.
- O comprimento do prefixo pode variar de 0 a 128. O comprimento do prefixo IPv6 recomendado para LANs e a maioria dos outros tipos de redes é /64, conforme mostrado na figura.
- ![[comprimento prefixo IPv6.png]]
- É recomendado o uso de /64 bits para a maioria das redes. Isso ocorre pois a configuração automática de endereço sem estado (SLAAC) usa 64 bits para a parte do host. Também ajuda na hora de criação e gerenciamento de sub redes. 

# *Outros tipos de endereços IPv6 Unicast*

- ![[unicast address IPv6.png]]
- Ao contrário dos dispositivos IPv4 que têm apenas um único endereço, os endereços IPv6 normalmente têm dois endereços unicast:

### **Um endereço unicast global (GUA)**

-  É semelhante a um endereço IPv4 público. São endereços de Internet roteáveis e globalmente exclusivos. GUAs podem ser configurados estaticamente ou dinamicamente distribuídos.

### **Endereço LLA (Link Local Address)**

- Isso é necessário para cada dispositivo habilitado para IPv6. Os LLAs são usados para se comunicar com outros dispositivos no mesmo link local. No IPv6, o <mark style="background: #BBFABBA6;">termo link</mark> se refere a uma <mark style="background: #BBFABBA6;">sub rede</mark>. Limitados a um único link. 
- Sua exclusividade só deve ser confirmada nesse link, porque eles não são roteáveis além do link. Em outras palavras, os roteadores não encaminham pacotes com um endereço de link local origem ou destino.

# *Observação sobre o endereço local exclusivo*

- Endereços locais exclusivos (intervalo fc00::/7 a fdff::/7) ainda não são comumente implementados.
- Endereços locais exclusivos podem eventualmente ser usados para endereçar dispositivos que não devem ser acessíveis de fora, como servidores internos e impressoras.
- Os endereços unique local são utilizados para endereçamento local dentro de um site ou entre um número limitado de sites.
- Os endereços unique local podem ser usados para dispositivos que nunca precisarão ou terão acesso por outra rede.
- Endereços locais exclusivos não são globalmente roteados ou traduzidos para um endereço IPv6 global.

# *GUA IPv6*

- São os endereços IPv6 que são globalmente acessados e roteáveis. São exclusivos de cada dispositivo e são equivalentes ao endereço público do IPv4. 
- No momento, somente endereços unicast globais com os primeiros três bits de 001 ou 2000::/3 estão sendo atribuídos.
- A figura mostra o intervalo de valores para o primeiro hexteto onde o primeiro dígito hexadecimal para GUAs atualmente disponíveis começa com um 2 ou um 3. Isso é apenas um oitavo do espaço de endereço IPv6 total disponível, excluindo uma parte muito pequena de outros tipos de endereços unicast e multicast.
- ![[enderecos IPv6 que sao utilizados.png]]

### **Endereço IPv6 com prefixo de roteamento global /48 e prefixo /64**

- ![[prefixo 64 e roteamento global 48.png]]

# *Estrutura IPv6 GUA*

### **Prefixo de roteamento global**

- O prefixo global de roteamento é o prefixo (parte de rede) do endereço que é atribuído pelo provedor (como um ISP) a um cliente ou um site. Por exemplo, é comum que os ISPs atribuam um prefixo de roteamento global /48 a seus clientes. O prefixo de roteamento global geralmente varia dependendo das políticas do ISP.
- Por exemplo, o endereço IPv6 2001:db8:acad::/ 48 possui um prefixo de roteamento global que indica que os primeiros 48 bits (3 hextets) (2001:db8:acad) são como o ISP conhece esse prefixo (rede). Dois-pontos duplo (::) antes do comprimento de prefixo /48 significa que o restante do endereço contém apenas 0s. O tamanho do prefixo de roteamento global determina o tamanho da ID da sub-rede.

### **ID da sub rede**

- O campo ID de sub rede é a área entre o Prefixo de roteamento global e o ID da interface. Ao contrário do IPv4, onde você deve pedir bits emprestados da parte do host para criar sub redes, o IPv6 foi projetado tendo em mente a sub rede. A ID da sub rede é usada por uma empresa para identificar sub redes localmente. Quanto maior a ID da sub rede, mais sub redes disponíveis.
- Com comprimento de prefixo /64 é comum que os primeiros 4 hextetos sejam para parte da rede do endereço, sendo o quarto o ID da sub rede e os outros 4 hextetos são para o ID da interface. 
### **ID da interface**

- A ID da interface IPv6 equivale à parte de host de um endereço IPv4. O termo ID da interface é usado porque um único host pode ter várias interfaces, cada uma com um ou mais endereços IPv6.
- Uma sub-rede /64 ou prefixo (Prefixo de roteamento global + ID da sub-rede) deixa 64 bits para o ID da interface. Isso é recomendado para permitir que dispositivos habilitados para SLAAC criem seu próprio ID de interface de 64 bits. Também torna o desenvolvimento de um plano de endereçamento IPv6 simples e eficaz.
- **Observação**: Ao contrário do IPv4, no IPv6 todos os endereços de host apenas com 0s ou apenas com 1s podem ser atribuídos a um dispositivo. O endereço todos-1s pode ser usado porque os endereços de broadcast não são usados dentro do IPv6. O endereço apenas de 0s também pode ser usado, mas é reservado como endereço anycast de roteadores de sub-redes e só deve ser atribuído a roteadores.

# *IPv6 LLA*

- Um endereço IPv6 de link-local permite que um dispositivo se comunique com outros dispositivos habilitados para IPv6 no mesmo link e somente nesse link (sub rede). Os pacotes com endereço de link local origem ou destino não podem ser roteados além do link de onde o pacote foi originado.
- A GUA não é requisito porém o cada interface de rede habilitada para IPv6 deve ter uma LLA.
- Se um LLA não estiver configurado manualmente em uma interface, o dispositivo criará automaticamente um próprio, sem se comunicar com um servidor DHCP. Os hosts habilitados para LLA IPv6 criarão um endereço IPv6 mesmo que não tenha sido atribuído um endereço IPv6 unicast global ao dispositivo. 
- Isso permite que dispositivos habilitados para IPv6 se comuniquem com outros dispositivos semelhantes na mesma sub rede. Isso inclui a comunicação com o gateway padrão (roteador).
- ![[comunicacao IPv6 local.png]]
- ![[comunicacao IPv6 entre routers.png]]
- **Observação**: Normalmente, é o LLA do roteador, e não a GUA, que é usado como o gateway padrão para outros dispositivos no link.