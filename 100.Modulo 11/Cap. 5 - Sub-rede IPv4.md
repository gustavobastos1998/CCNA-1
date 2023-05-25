# *Sub-rede em um limite de octeto*

- As sub-redes IPv4 são criadas com um ou mais bits de host sendo usados como bits de rede. Isso é feito estendendo-se a máscara de sub-rede para pegar emprestado alguns dos bits da parte de host do endereço e criar bits de rede adicionais. 
- Quanto mais bits de host forem emprestados, mais sub-redes poderão ser definidas. Quanto mais bits forem emprestados para aumentar o número de sub-redes reduz o número de hosts por sub-rede.
- É mais fácil dividir redes quando o prefixo é: /8, /16 ou /24. 

# *Sub-rede dentro de um limite de octeto*

- ![[subnet a -24 network.png]]
 - **Linha /25** - O empréstimo 1 bit do quarto octeto cria 2 sub redes que suportam 126 hosts cada.
- **Linha /26** - O empréstimo de 2 bits cria 4 sub redes que suportam 62 hosts cada.
- **Linha /27** - O empréstimo de 3 bits cria 8 sub redes que suportam 30 hosts cada.
- **Linha /28** - O empréstimo de 4 bits cria 16 sub redes que suportam 14 hosts cada.
- **Linha /29** - O empréstimo de 5 bits cria 32 sub redes que suportam 6 hosts cada.
- **Linha /30** - O empréstimo de 6 bits cria 64 sub redes que suportam 2 hosts cada.
- O número "mágico" é representado pelo '1' mais a direita. Ele decresce da esquerda para a direita e determina as divisões de cada sub rede criada. O número mágico nos diz como achar nossas sub redes e cada sub rede aumentará conforme ele. 
- Exemplo: ![[exemplo magic number.png]]

# *Observações*

- A rede 172.16.0.0 tem como máscara padrão 255.255.0.0 ou /16. 
- A rede 10.0.0.0 tem como máscara padrão 255.0.0.0 ou /8.
- ![[subnet for prefix 16.png]]
- O mesmo conceito de "emprestar" bits para a parte da rede funciona com essas duas redes com máscaras diferentes. 
- O que as difere é que a rede 172.16.0.0/16 pode criar um número maior de sub redes que a 192.168.0.0/24. Consequentemente, a rede 10.0.0.0/8 pode criar mais sub redes que as outras duas. 
- ![[numero de sub redes criadas.png]]
- O primeiro endereço é reservado para o endereço de rede e o último endereço é reservado para broadcast. 