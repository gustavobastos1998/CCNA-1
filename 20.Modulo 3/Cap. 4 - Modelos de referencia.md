# *Benefícios de usar um modelo de camadas*

- Auxiliar no projeto de protocolos porque os protocolos que operam em uma camada específica definiram as informações sobre as quais atuam e uma interface definida para as camadas acima e abaixo.
- Fomentar a concorrência porque produtos de diferentes fornecedores podem trabalhar juntos.
- Impedir que alterações de tecnologia ou capacidade em uma camada afetem outras camadas acima e abaixo.
- Fornecer uma linguagem comum para descrever funções e capacidades de rede.
- Existem dois modelos em camadas que são usados para descrever operações de rede: modelo OSI (Open System Interconnection) e modelo TCP/IP.
- ![[modelos em camada.png]]

# *Modelo de Referência OSI*

- O modelo de referência OSI fornece uma extensa lista de funções e serviços que podem ocorrer em cada camada.
- ![[modelo OSI.png]]

# *Modelo de protocolo TCP/IP*

- Esse tipo de modelo corresponde à estrutura de um conjunto de protocolos específico. O modelo TCP/IP é um modelo de protocolo porque descreve as funções que ocorrem em cada camada de protocolos dentro da suíte TCP/IP.
- ![[modelo referencia tcp-ip.png]]

# *OSI x TCP/IP*

- Há diferenças em relação as camadas de aplicação e acesso à rede. O modelo OSI divide essas duas camadas devido a funções discretas que devem ocorrer nelas. 
- A camada de acesso à rede no modelo TCP/IP não especifica qual protocolo usar ao transmitir por meio físico, ele descreve somente a transmissão da camada de Internet aos protocolos de rede física. Já as Camadas 1 e 2 do modelo OSI discutem os procedimentos necessários para acessar a mídia e o meio físico para enviar dados por uma rede.
- As principais semelhanças estão nas camadas de transporte e rede; no entanto, os dois modelos diferem em como eles se relacionam com as camadas acima e abaixo de cada camada:
	- A Camada OSI 3, a camada de rede, é mapeada diretamente para a camada de Internet TCP/IP. Essa camada é usada para descrever os protocolos que endereçam e encaminham mensagens em uma rede interconectada.
	- A Camada OSI 4, a camada de transporte, mapeia diretamente para a camada de transporte TCP/IP. Essa camada descreve os serviços e as funções gerais que fornecem uma entrega ordenada e confiável de dados entre os hosts origem e destino.
	- A camada de aplicativos TCP/IP inclui vários protocolos que fornecem funcionalidade específica para uma variedade de aplicativos do usuário final. As camadas 5, 6 e 7 do modelo OSI são usadas como referências para desenvolvedores e fornecedores de software de aplicação para produzir aplicações que operam em redes.
	- Ambos os modelos TCP/IP e OSI são usados geralmente para referenciar protocolos em várias camadas. Como o modelo OSI separa a camada de enlace de dados da camada física, geralmente é usado para referenciar as camadas inferiores.