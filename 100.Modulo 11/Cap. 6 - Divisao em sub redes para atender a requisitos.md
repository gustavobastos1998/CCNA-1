# *Espaço de endereços IPv4 privados de sub rede público*

- Embora seja bom segmentar rapidamente uma rede em sub redes, a rede da sua organização pode usar endereços IPv4 públicos e privados. Isto afeta. a forma como irá sub rede da rede.
- A figura mostra uma rede empresarial típica:
	- **Intranet -** Esta é a parte interna da rede de uma empresa, acessível apenas dentro da organização. Os dispositivos na intranet usam endereços IPv4 privados.
	- **DMZ -** Faz parte da rede da empresa que contém recursos disponíveis para a internet, como um servidor web. Os dispositivos na DMZ usam endereços IPv4 públicos.
- ![[IPv4 publico e privado.png]]

# *Minimizar endereços IPv4 de host não utilizados e maximizar sub redes*

- Para minimizar o número de endereços IPv4 de host não utilizados e maximizar o número de sub redes disponíveis, há duas considerações ao planejar sub redes: o número de endereços de host necessários para cada rede e o número de sub redes individuais necessárias.