# *Características do cabeamento de cobre*

- As redes usam mídia de cobre porque é barata, fácil de instalar e tem baixa resistência à corrente elétrica. Entretanto, ela é limitada pela distância e interferência de sinal.
- Os dados são transmitidos por cabos de cobre como pulsos elétricos. Um detector na interface de rede de um dispositivo destino tem que receber um sinal que poderá ser decodificado com êxito para corresponder ao sinal enviado. 
- No entanto, quanto mais o sinal viaja, mais ele se deteriora. Isso se chama atenuação de sinal. Por isso, todas as mídias de cobre devem seguir limitações de distância rigorosas, conforme especificado nos padrões de orientação.
- Duas fonte podem interferir na temporização e voltagem dos pulsos elétricos:

### **Interferência eletromagnética (EMI) ou interferência de radiofrequência (RFI)**

- Os sinais EMI e RFI podem distorcer e corromper os sinais de dados que estão sendo transportados pela mídia de cobre.

### **Diafonia**

- Diafonia é uma perturbação causada pelos campos elétrico ou magnético de um sinal em um fio para o sinal em um fio adjacente. 
- Nos circuitos de telefone, a diafonia pode fazer com que parte de outra conversa de voz de um circuito adjacente seja ouvida (linha cruzada).
- Especificamente, quando uma corrente elétrica flui através de um cabo, ela cria um pequeno campo magnético circular ao redor do cabo, que pode ser captado por um cabo adjacente.

# *Contrabalanceamento dos efeitos negativos*

- Para evitar os problemas causados pelo EMI e RFI alguns cabos de cobre têm uma proteção metálica e exigem conexões devidamente aterradas. 
- Para evitar os efeitos negativos do crosstalk alguns cabos de cobre têm pares de cabos de circuitos opostos juntos, o que efetivamente cancela a linha cruzada.

# *Tipos de cabeamento de cobre*

- ![[tipos de cabo de cobre.png]]

# *Par trançado não blindado (UTP)*

- O cabeamento de par trançado não blindado (UTP) é o meio físico de rede mais comum. O cabeamento UTP, terminado com conectores RJ-45, é usado para interconectar hosts de rede com dispositivos de rede intermediários, como comutadores e roteadores.
- Nas LANs, o cabo UTP consiste em quatro pares de cabos codificados por cores que foram trançados e depois colocados em uma capa plástica flexível que protege contra danos físicos menores. O processo de trançar cabos ajuda na proteção contra interferência de sinais de outros cabos.
- ![[cabo trancado nao blindado-utp.png]]

# *Par trançado blindado (STP)*

- O par trançado blindado (STP) oferece maior proteção contra ruído do que o cabeamento UTP. No entanto, em comparação com o cabo UTP, o cabo STP é significativamente mais caro e difícil instalação. Assim como o cabo UTP, o STP usa um conector RJ-45.
- A blindagem evita os problemas causados por EMI e RFI e são trançados para conter a linha cruzada. 
- Para aproveitar totalmente a blindagem, os cabos STP são terminados com conectores de dados STP blindados especiais. Se o cabo não estiver devidamente aterrado, a blindagem poderá atuar como uma antena e captar sinais indesejados.
- ![[cabo trancado blindado-stp.png]]

# *Cabo Coaxial*

- O cabo coaxial, ou coax para abreviar, recebeu seu nome porque tem dois condutores que compartilham o mesmo eixo.
- Características do cabo coax incluem: 
	- Um condutor de cobre é usado para transmitir os sinais eletrônicos.
	- Uma camada de isolamento plástico flexível envolve um condutor de cobre.
	- O material de isolamento é envolvido em uma malha de cobre com tecido, ou uma folha metálica, que atua como o segundo cabo no circuito e uma proteção para o condutor interno. Essa segunda camada, ou blindagem, também reduz a quantidade de interferência eletromagnética externa.
	- Todo o cabo é coberto com um revestimento para evitar danos físicos menores.
- Há tipos diferentes de conectores utilizados com o cabo coax. Os conectores Bayonet Neill-Concelman (BNC), tipo N e tipo F são mostrados na figura.
- Embora o UTP substituiu essencialmente o cabo coaxial nas modernas instalações Ethernet o cabo coax é usado para conectar antenas a dispositivos sem fio.
- ![[cabo coax.png]]