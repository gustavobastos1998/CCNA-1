# *Sub rede usando o ID de sub rede*

- Com o IPv4, devemos pedir bits emprestados da parte do host para criar sub redes. Isso ocorre porque a sub rede foi um pensamento tardio com IPv4. No entanto, o IPv6 foi projetado com a sub rede em mente. Um campo de ID de sub rede separado no GUA IPv6 é usado para criar sub redes.
- ![[GUA com ID de sub rede de 16 bits.png]]
- O benefício de um endereço de 128 bits é que ele pode suportar sub redes e hosts mais do que suficientes por sub rede, para cada rede. Conservação de endereços não é um problema. Por exemplo, se o prefixo de roteamento global for /48, e usando um 64 bits típico para o ID de interface, isso criará um ID de sub rede de 16 bits.
- **ID de sub rede de 16 bits** - Cria até 65.536 sub redes.
- **ID da interface de 64 bits** - Suporta até 18 quintilhões de endereços IPv6 de host por sub rede.
- A divisão de IPv6 em sub redes também é mais fácil de implementar do que no IPv4, porque não há necessidade da conversão em binário. Para determinar a próxima sub rede disponível, basta contar em ordem crescente em hexadecimal.

# *Exemplo de sub rede IPv6*

- Por exemplo, suponha que uma organização tenha sido atribuída ao prefixo de roteamento global 2001:db8:acad::/48 com um ID de sub rede de 16 bits. 
- O prefixo global de roteamento é o mesmo para todas as sub redes. Somente o hexteto da ID da sub rede é incrementado em hexadecimal para cada sub rede.
- ![[sub rede ID 16 bits.png]]

# *Alocação de sub redes IPv6*

- A topologia a seguir requer cinco sub redes, uma para cada LAN e outra para interconectar os roteadores. Ao contrário do IPv4, o IPv6 utiliza o mesmo comprimento de prefixo para todas as sub redes (LANs e WAN). 
- ![[topologia sub redes IPv6.png]]