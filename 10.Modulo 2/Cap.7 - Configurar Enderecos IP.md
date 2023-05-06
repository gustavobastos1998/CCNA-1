# *Configuração Manual de Endereço IP para dispositivos finais*

- As informações de endereço IPv4 podem ser inseridas nos dispositivos finais manualmente ou automaticamente usando o DHCP (Dynamic Host Configuration Protocol).
- Para configurar manualmente um endereço IPv4 em um host do Windows, abra o **Control Panel > Network Sharing Center > Change adapter settings** e escolha o adaptador. Em seguida, clique com o botão direito do mouse e selecione **Properties** para exibir o **Local Area Connection Properties**, como mostrado na figura. 
- ![[Ethernet Properties.png]]
- Destaque Internet Protocol versão 4 (TCP/IPv4) e clique **Properties** para abrir a **Internet Protocol Version 4 (TCP/IPv4) Properties** janela, mostrada na figura. Configure as informações de endereço IPv4 e máscara de sub-rede e o gateway padrão.
- ![[IPv4.png]]
- As opções para o IPv6 é semelhante ao IPv4. 
- Os campos de DNS server são os endereços IPv4 e IPv6 do servidor DNS que será usado para converter os endereços IP em nomes de domínio. 

# *Configuração Automática de endereços IP para dispositivos finais*

- Geralmente, dispositivos finais usam o DHCP para configurar automaticamente o IPv4 e o DNS server. Sem o DHCP, toda vez que o dispositivo se conectasse à rede você teria de inserir manualmente o IPv4, máscara de rede, gateway padrão e o DNS server. Além de poder ocorrer de dois dispositivos na mesma rede usarem IPv4 iguais, ocasionando em problemas. 
- Para utilizar o DHCP só é preciso marcar a opção de obter IP automaticamente nas propriedades de IPv4. O mesmo vale para o DNS server. 

# *Configuração da Interface Virtual de Switch*

- Para poder acessar o switch remotamente um endereço IP e uma máscara deve ser configurado na SVI (Switch Virtual Interface). Use o comando <mark style="background: #ABF7F7A6;">interface vlan 1</mark>, <mark style="background: #ABF7F7A6;">ip address endereço-ip mascara-de-rede</mark>, por fim <mark style="background: #ABF7F7A6;">no shutdown</mark> tudo isso no modo de <mark style="background: #BBFABBA6;">configuração global</mark>. A vlan 1 não é uma interface física, mas sim uma virtual. 