# *Problemas de operação duplex e incompatibilidade*

- Muitos problemas comuns de rede podem ser identificados e resolvidos com pouco esforço.
- As interfaces Ethernet de interconexão devem operar no mesmo modo duplex para obter melhor desempenho de comunicação e evitar ineficiência e latência no link.
- Primeiramente, os dispositivos conectados anunciam seus recursos de compatibilidade e, depois, escolhem o modo de desempenho mais alto, compatível com as duas extremidades.

# *Problemas de endereçamento IP em dispositivos IOS*

- Os problemas relacionados ao endereço IP provavelmente impedirão que os dispositivos de rede remota se comuniquem.
- Como os endereços IP são hierárquicos, qualquer IP address deve estar dentro do intervalo de endereços dessa rede. 
- Duas causas comuns de atribuição de IPv4 incorreta são os erros de atribuição manual ou problemas relacionados a DHCP.

# *Problemas de endereçamento IP em dispositivos finais*

- No Windows, quando o dispositivo não consegue um IP com o DHCP server o Windows atribui a ele um endereço que pertence ao intervalo 169.254.0.0/16. Esse recurso é chamado de endereçamento IP privado automático (APIPA). 
- Um dispositivo atribuído com um endereço APIPA, normalmente, não conseguirá se comunicar com outros dispositivos na rede. Isso ocorre por que ele, provavelmente, não faz parte da mesma rede local. 
- Essa situação indica um problema de atribuição automática de endereço IPv4 que precisa ser corrigido. A maioria dos dispositivos finais são configurados de forma que dependam de um servidor DHCP para a atribuição automática de endereço IPv4.

# *Problemas de gateway padrão*

- Caso o default gateway não seja settado corretamente, o dispositivo em questão não conseguirá se comunicar com outras redes. 
- O endereço do gateway padrão pode ser manualmente definido ou obtido de um servidor DHCP. Assim como problemas de endereçamento de IP, os problemas de gateway padrão podem estar relacionados a configuração manual errada ou problemas de DHCP (caso a atribuição manual estiver em uso).
- Para solucionar esse problema, basta verificar que o dispositivo está com o default gateway configurado corretamente. 
- Também é importante verificar se o endereço IPv4 e a máscara de sub rede adequados foram configurados na interface do roteador e se a interface está ativa.

# *Como solucionar problemas de DNS*

- Não é crucial para a comunicação do dispositivo, mas é importante para o usuário final. 
- Embora o roteamento de pacotes e todos os serviços de rede continuem em operação, as falhas de DNS normalmente levam o usuário à conclusão errada.
- Os endereços de servidor DNS podem ser atribuídos de forma manual ou automática. 
- Embora seja comum para as empresas gerenciarem seus próprios servidores DNS, qualquer servidor DNS alcançável pode ser usado para resolver nomes.