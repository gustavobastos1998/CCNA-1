# *O Quadro*

- O protocolo de link de dados é responsável pelas comunicações NIC para NIC dentro da mesma rede. Embora existam muitos protocolos de camada de enlace de dados diferentes que descrevem os quadros de camada de enlace de dados, cada tipo de quadro tem três partes básicas:
	- Cabeçalho;
	- Dados;
	- Trailer.
- Ao contrário de outros protocolos de encapsulamento, a camada de link de dados acrescenta informações na forma de um trailer no final do quadro.
- Todos os protocolos da camada de enlace de dados encapsulam os dados dentro do campo de dados do quadro. No entanto, a estrutura do quadro e os campos contidos no cabeçalho e trailer variam de acordo com o protocolo.
- Não há uma estrutura de quadro que satisfaça a todas as necessidades de todo transporte de dados através de todos os tipos de mídia. Dependendo do ambiente, a quantidade de informações de controle necessária no quadro varia para corresponder às exigências de controle de acesso ao meio físico e à topologia lógica. Por exemplo, um quadro WLAN deve incluir procedimentos para evitar colisões e, portanto, requer informações de controle adicionais quando comparado a um quadro Ethernet.

# *Campos do Quadro*

- O enquadramento quebra o fluxo em agrupamentos decifráveis, com a informação de controle inserida no cabeçalho e trailer como valores em diferentes campos. Esse formato fornece aos sinais físicos uma estrutura reconhecida por nós e decodificada em pacotes no destino.
- Os campos de quadro genérico são mostrados na figura. Nem todos os protocolos incluem todos esses campos. Os padrões para um protocolo de enlace de dados específico definem o formato real do quadro.
- ![[campo do quadro.png]]
- Os protocolos da DLL acrescentam um trailer ao final de cada quadro. Em um processo chamado detecção de erros, o trailer determina se o quadro chegou sem erros. Essa detecção de erro deve existir para essa camada pois os sinais na mídia podem estar sujeitos a interferências, distorções ou perdas que ocasionam na alteração de bits que esses sinais representam. 
- Um nó de transmissão cria um resumo lógico dos conteúdos do quadro, conhecido como valor de verificação de redundância cíclica (cyclic redundancy check - CRC).
- Este valor é colocado no campo FCS (Sequência de Verificação de Quadro) para exibição ou conteúdo do quadro. No trailer Ethernet, o FCS fornece um método para o nó de recebimento determinar se o quadro apresentou erros de transmissão.

# *Endereço da camada 2*

- Os endereços de dispositivos nesta camada são chamados de endereços físicos. O endereçamento da camada de enlace de dados está contido no cabeçalho do quadro e especifica o nó destino do quadro na rede local.
- Normalmente, ele está no início do quadro, portanto, a NIC pode determinar rapidamente se ela corresponde ao seu próprio endereço de Camada 2 antes de aceitar o restante do quadro. O cabeçalho do quadro também pode conter o endereço de origem do quadro.
- Os endereços da camada de rede são hierárquicos porém os físicos não indicam em que rede o dispositivo está. 
- Em vez disso, o endereço físico é um endereço exclusivo do dispositivo específico. Um dispositivo ainda funcionará com o mesmo endereço físico da Camada 2, mesmo que o dispositivo se mova para outra rede ou sub-rede.
- Portanto, os endereços de Camada 2 são usados apenas para conectar dispositivos dentro da mesma mídia compartilhada, na mesma rede IP.

### **Transmissão de dados para uma rede diferente**
- Como os protocolos da data link só podem especificar os endereços físicos localizados na mesma rede, do host ao roteador o quadro de de enlace de dados é preenchido com os endereços físicos do dispositivo final e do gateway padrão.
- Ao chegar no roteador que mandará os dados para outra rede, ele desencapsula e forma um novo quadro informando agora que o endereço físico origem é ele e o destino é outro roteador. O processo de desencapsulamento também ajuda a saber o endereço lógico está sendo utilizado, além de também auxiliar na hora de escolher por onde os dados serão enviados pela rede.
- Quando o quadro chega no roteador certo, ele também desencapsula o quadro para informar os NICs certos, finalizando assim a entrega dos dados ao dispositivo localizado na rede local.
- ![[host-roteador.png]]

# *Quadros de LAN e WAN*

- Protocolos Ethernet são usados por LANs com fio. As comunicações sem fio se enquadram nos protocolos WLAN (IEEE 802.11). Esses protocolos foram projetados para redes multiacesso.
- As WANs tradicionalmente usavam outros tipos de protocolos para vários tipos de topologias ponto a ponto, hub-spoke e malha completa. Alguns dos protocolos WAN comuns ao longo dos anos incluíram:
	- Protocolo ponto a ponto (PPP);
	- Controle de Enlace de Dados de Alto Nível (HDLC);
	- Frame Relay;
	- Modo de Transferência Assíncrona (ATM);
	- X.25;
- Esses protocolos de Camada 2 agora estão sendo substituídos na WAN por Ethernet.
- Em uma rede TCP/IP, todos os protocolos de Camada 2 do modelo OSI trabalham com o IP na Camada 3 do modelo. No entanto, o protocolo de Camada 2 usado depende da topologia lógica e do meio físico.
- O protocolo da camada 2 usado para uma topologia de rede específica é determinado pela tecnologia usada para implementar essa topologia. A tecnologia usada é determinada pelo tamanho da rede, em termos do número de hosts e do escopo geográfico, e dos serviços a serem fornecidos pela rede.
- Uma LAN normalmente usa uma tecnologia de alta largura de banda capaz de suportar um grande número de hosts. A área geográfica relativamente pequena de uma LAN (um único edifício ou um campus com vários edifícios) e sua alta densidade de usuários tornam essa tecnologia econômica.
- Já com as WANs são diferentes, pois elas abragem uma área muito maior. Os custos para links físicos e a tecnologia usada para transmitir os sinais por essas distâncias geralmente resultam em uma capacidade de largura de banda menor que uma LAN. 
- Essa diferença ocasiona em um diferente uso de protocolos para LAN e WAN. 