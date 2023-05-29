# *LLA Dinâmico*

- Todos os dispositivos IPv6 devem ter um IPv6 LLA. Assim como IPv6 GUAs, você também pode criar LLAs dinamicamente. 
- Independentemente de como você cria seus LLAS (e seus GUAs), é importante que você verifique toda a configuração de endereço IPv6.

# *LLAs dinâmicos no Windows*

- Normalmente usarão o mesmo método para um GUA criado pelo SLAAC e um LLA atribuído dinamicamente.
- ![[EUI-46 vs gerado aleatoriamente.png]]

# *LLAs dinâmicos em Cisco Routers*

- Os roteadores Cisco criam automaticamente um endereço IPv6 de link local sempre que um endereço unicast global é atribuído à interface. 
- Por padrão, os roteadores Cisco IOS usam o EUI-64 para gerar a ID da interface de todos os endereços de link local em interfaces IPv6. Em interfaces seriais, o roteador usará o endereço MAC de uma interface Ethernet
- Para tornar mais fácil reconhecer esses endereços em roteadores e lembrar deles, é comum configurar estaticamente endereços IPv6 de link local nos roteadores.
- ![[IPv6 LLA EUI-63 Cisco Router.png]]

# *Verificar a Configuração de Endereço IPv6*

### <mark style="background: #ABF7F7A6;">show ipv6 interface brief</mark>

- O comando **show ipv6 interface brief** exibe o endereço MAC das interfaces Ethernet. EUI-64 usa esse endereço MAC para gerar a ID da interface para o endereço de link local. Além disso, o comando **show ipv6 interface brief** exibe a saída abreviada para cada uma das interfaces. 
- A saída [up/up] na mesma linha que a interface indica que o estado da Camada 1/Camada 2 da interface. Isso é o mesmo que as colunas de status e de protocolo no comando IPv4 equivalente.
- O primeiro endereço é o GUA e o segundo LLA.
- ![[command show ipv6 inter b.png]]

### <mark style="background: #ABF7F7A6;">show ipv6 route</mark>

-  Pode ser usado para verificar se foram instalados redes IPv6 e endereços IPv6 específicos na tabela de roteamento IPv6.
- Esse comando não exibe IPv4. 
- **C** se trata de uma rede diretamente conectada. Quando a interface está configurada com uma GUA e se encontra no estado "up/up", o prefixo IPv6 e o comprimento do prefixo são adicionados à tabela de roteamento IPv6 como uma rota conectada.
- **L** indica rota local, o endereço IPv6 específico atribuído à interface. Não é um LLA. Endereços LLA não estão na tabela de roteamento por não serem roteáveis. 
- O GUA também é instalado na tabela de roteamento como uma rota local. A rota local tem um comprimento de prefixo de /128. 
- As rotas locais são usadas pela tabela de roteamento para processar de forma eficiente pacotes com um endereço destino igual ao endereço da interface do roteador.
- ![[command show ipv6 route.png]]

### <mark style="background: #ABF7F7A6;">ping</mark>

- Idêntico ao comando usado no IPv4.
- ![[command ping.png]]