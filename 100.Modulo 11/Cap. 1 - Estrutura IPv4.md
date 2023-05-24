# *Parte de rede e de host*

- Um endereço IPv4 é um endereço hierárquico de 32 bits, composto por uma parte da rede e outra de host. 
- ![[parte rede host ipv4.png]]

# *Máscara de sub-rede*

- Para identificar as partes da rede e do host de um endereço IPv4, a máscara de sub-rede é comparada com o endereço IPv4 bit por bit, da esquerda para a direita. 
- ![[subnet mask e ipv4.png]]
- Para o exemplo acima, a sub-rede é 192.168.10.0.

# *Comprimento do prefixo*

- O comprimento do prefixo é o número de bits definido como 1 na máscara de sub-rede. Está escrito em "notação de barra", que é anotada por uma barra (/) seguida pelo número de bits definido como 1. Portanto, conte o número de bits da máscara de sub-rede e preceda-o com uma barra.
- ![[comprimento do prefixo.png]]
- Então, quando um IPv4 é apresentado como 192.168.10.3/24 isso indica que sua mascara de sub-rede é 255.255.255.0. 
- **Observação**: Um endereço de rede também é referido como prefixo ou prefixo de rede. Portanto, o comprimento do prefixo é o número de 1 bits na máscara de sub-rede.
- O comprimento do prefixo determina qual é a porção de rede e host para um IPv4. Caso o comprimento seja 8, somente o primeiro octeto será usado para expressar a porção da rede enquanto os últimos 3 octetos representarão hosts distintos. 

# *Determinando a rede: Lógica AND*

- Porta AND lógica é um operação que compara duas entradas booleanas e retorna verdadeiro se somente se os dois parâmetros forem verdadeiros. 
- Essa exata lógica é usada para determinar o endereço de rede para hosts IPv4 em conjunto com sua subnet mask. 
- ![[logica AND subnet ipv4.png]]

# *Endereços de broadcast, host e rede*

- ![[multiplos propositos para endereco.png]]
- O endereço de rede é um endereço que representa uma rede específica. Um dispositivo pertence a esta rede se atender a 3 critérios: 
	- Tem a mesma máscara de sub-rede que o endereço de rede.
	- Ele tem os mesmos bits de rede que o endereço de rede, conforme indicado pela máscara de sub-rede.
	- Ele está localizado no mesmo domínio de difusão que outros hosts com o mesmo endereço de rede.