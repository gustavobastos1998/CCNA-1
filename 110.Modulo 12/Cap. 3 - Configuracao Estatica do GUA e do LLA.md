# *Configuração de GUA estática em um roteador*

- É fácil configurar estaticamente GUAs e LLAs IPv6 em roteadores para ajudá-lo a criar uma rede IPv6. 
- A maioria dos comandos de configuração e verificação do IPv6 no Cisco IOS são semelhantes aos seus equivalentes no IPv4. Em muitos casos, a única diferença é o uso de **ipv6** no lugar **ip** de dentro dos comandos.
- Por exemplo, o comando Cisco IOS para configurar um endereço IPv4 em uma <mark style="background: #BBFABBA6;">interface</mark> é <mark style="background: #ABF7F7A6;">ip address ip-address subnet-mask</mark>. Em contraste, o comando para configurar um GUA IPv6 em uma <mark style="background: #BBFABBA6;">interface</mark> é <mark style="background: #ABF7F7A6;">ipv6 address ipv6-address/prefix-length</mark>.
- Na figura abaixo, basta acessar cada interface (G0/0/0, G0/0/1 e S0/1/0) do R1 e por o comando com seus respectivos IPv6 e comprimento de prefixo. Não esquecer do <mark style="background: #ABF7F7A6;">no shutdown</mark> após configurar cada IPv6 para que a interface seja de fato iniciada.

# *Configuração de GUA estática em um Host Windows*

- Essa configuração é feita com aplicativos nativos do windows. O default gateway na imagem abaixo é a GUA da interface GigabitEthernet do roteador na mesma rede. Pode-se utilizar o LLA como default gateway, inclusive é uma prática recomendável. 
- ![[IPv6 windows.png]]
- Há duas maneiras de um dispositivo obter um endereço IPv6 unicast global automaticamente:
	- Configuração automática de endereço stateless (SLAAC)
	- Com estado DHCPv6
- **Observação**: Quando o DHCPv6 ou o SLAAC é usado, o LLA do roteador será especificado automaticamente como o endereço de gateway padrão.

# *Configuração estática de um endereço Unicast local de link*

- A configuração manual de endereços link local permite criar um address reconhecível e fácil de lembrar. Geralmente, só é necessário criar endereços de link local reconhecíveis nos roteadores. Isso se dá pois os LLAs do roteador são importantes para gateway padrão e roteamento de mensagens de anúncio. 
- A configuração é parecida com a GUA, porém o comando para configurar o endereço muda um pouco. O comando para configurar o endereço link local é <mark style="background: #ABF7F7A6;">ipv6 address  ipv6-link-local-address link-local</mark>. 
- Outro detalhe, o endereço está dentro do range fe80 a febf. Cada interface faz parte de uma rede, então ao configurar o LLA deve-se fazer: ipv6 address fe80::1:1 link-local. 
- O último hexteto dirá a interface do dispositivo. O penúltimo mudará de interface a interface, pois são redes diferentes. 
- **Observação**: O <mark style="background: #ADCCFFA6;">mesmo LLA pode ser configurado em cada link</mark>, <mark style="background: #ADCCFFA6;">desde que seja exclusivo nesse link</mark>. Isso é possível porque as interfaces de link local só precisam ser exclusivas nesse link. No entanto, a prática comum é <mark style="background: #FF5582A6;">criar um LLA diferente em cada interface do roteador</mark> para facilitar a identificação do roteador e da interface específica.