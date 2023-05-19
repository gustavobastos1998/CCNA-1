# *Configurar Interfaces do Roteador*

- Também muito parecido com a configuração do switch.

# *Informações adicionais para configuração de interfaces de roteadores*

- O comando <mark style="background: #ABF7F7A6;">description {string}</mark>, apesar de também estar presente para interfaces de switch, permite o configurador adicionar uma descrição para uma interface. 
- Esse comando não é necessário para a configuração de uma interface, porém é extremamente útil para solucionar problemas de rede de produção, pois ela fornece informações sobre o tipo de rede conectada. A descrição, quando bem escrita, informa informações sobre conexão e contato de terceiros. 
- Um diferencial para os roteadores é a adição de comandos exclusivos de routers. Um exemplo deles seria o <mark style="background: #ABF7F7A6;">ipv6</mark> que é usado para settar o IPv6 e o prefix-length da interface. Além de comandos novos, os routers também têm a tabela de vizinhos conhecidos. Arquivos que mapeiam IPv6 com MAC address.
- A sintax do comando ipv6 é: <mark style="background: #ABF7F7A6;">ipv6 address 2001:db8:acad:10::1/64</mark>
- O comando <mark style="background: #ABF7F7A6;">no shutdown</mark> ativa a interface, deve ser utilizada <mark style="background: #FFF3A3A6;">SEMPRE</mark>.

# *Comandos de Verificação de Configuração*

- ![[comandos verif conf router.png]]