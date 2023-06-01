1. Qual função da camada de transporte é usada para estabelecer uma sessão orientada a conexão?
    
    Tópico 14.5.0 - TCP usa o handshake de 3 vias. UDP não usa este recurso. O handshake de 3 vias garante que haja conectividade entre os dispositivos de origem e destino antes da transmissão ocorrer.
    
    Indicador ACK UDP
    
    (x) Handshake de 3 vias TCP
    
    Número da porta TCP
    
    Número de sequência UDP
    
2. Qual é a gama completa de portas TCP e UDP bem conhecidas?
    
    Tópico 14.4.0 - Existem três intervalos de portas TCP e UDP. A gama bem conhecida de números de porta é de 0 a 1023.
    
    0 a 255
    
    256 - 1023
    
    1.024 a 49.151
    
    (x) 0 a 1023
    
3. O que é um soquete?
    
    Tópico 14.4.0 - Um soquete é uma combinação do endereço IP de origem e porta de origem ou o endereço IP de destino e o número da porta de destino.
    
    A combinação da sequência de origem e de destino e dos números de confirmação
    
    A combinação dos números de sequência de origem e de destino e dos números de porta
    
    A combinação do endereço IP de origem e destino e endereço Ethernet de origem e destino
    
    (x) A combinação de um endereço IP de origem e número de porta ou um endereço IP de destino e número de porta
    
4. Como um servidor em rede gerencia solicitações de vários clientes para serviços diferentes?
    
    Tópico 14.4.0 - Cada serviço fornecido por um servidor, como transferências de e-mail ou arquivos, usa um número de porta específico. O número da porta de origem de uma solicitação de serviço identifica o cliente que está solicitando serviços. O número da porta de destino identifica o serviço específico. Os servidores não usam informações de endereço para fornecer serviços. Os roteadores e switches usam informações de endereçamento para mover o tráfego pela rede.
    
    O servidor usa endereços IP para identificar serviços diferentes.
    
    Cada solicitação é rastreada através do endereço físico do cliente.
    
    O servidor envia todas as solicitações por meio de um gateway padrão.
    
    (x) Cada solicitação possui uma combinação de números de porta de origem e destino, provenientes de um endereço IP exclusivo.
    
5. O que acontece se parte de uma mensagem FTP não for entregue ao destino?
    
    Tópico 14.6.0 - Como o FTP usa o TCP como protocolo de camada de transporte, os números de sequência e confirmação identificam os segmentos ausentes, que serão reenviados para concluir a mensagem.
    
    A mensagem é perdida porque o FTP não usa um método de entrega confiável.
    
    Toda a mensagem FTP é reenviada.
    
    O host de origem FTP envia uma consulta para o host de destino.
    
    (x) A parte da mensagem FTP que foi perdida é reenviada.
    
6. Que tipo de aplicações são mais adequadas para usar o protocolo UDP?
    
    Tópico 14.3.0 - O UDP não é um protocolo orientado a conexão e não fornece mecanismos de retransmissão, sequenciamento ou controle de fluxo. Ele oferece funções básicas da camada de transporte com uma sobrecarga muito inferior à do TCP. Uma sobrecarga inferior faz com que o protocolo UDP seja adequado para as aplicações sensíveis a atraso.
    
    aplicações que precisam de entrega confiável
    
    aplicações que são sensíveis a perda de pacotes
    
    aplicações que precisam de retransmissão de segmentos perdidos
    
    (x) aplicações que são sensíveis a atrasos
    
7. Com o congestionamento da rede, a origem soube da perda de segmentos TCP que foram enviados ao destino. Qual é uma maneira do protocolo TCP lidar com isso?
    
    Tópico 14.6.0 - Se a fonte determinar que os segmentos TCP não estão sendo reconhecidos ou não são reconhecidos em tempo hábil, é possível reduzir o número de bytes que envia antes de receber um reconhecimento. Isso não envolve alterar a janela do cabeçalho do segmento. A origem não reduz a janela enviada no cabeçalho do segmento. A janela no cabeçalho do segmento é ajustada pelo host destino quando ele recebe dados mais rapidamente do que é capaz de processar, e não quando se depara com o congestionamento de rede.
    
    A origem diminui o tamanho da janela para reduzir a taxa de transmissão do destino.
    
    O destino envia menos mensagens de confirmação a fim de preservar a largura de banda.
    
    (x) A origem diminui o volume de dados que pode ser transmitido antes de receber uma confirmação do destino.
    
    O destino diminui o tamanho da janela.
    
8. Quais duas operações são fornecidas pelo TCP, mas não pelo UDP? (Escolha duas.)
    
    Tópico 14.1.0 - Numeração e rastreamento de segmentos de dados, confirmação de dados recebidos e retransmissão de quaisquer dados não reconhecidos são operações de confiabilidade para garantir que todos os dados cheguem ao destino. O UDP não fornece confiabilidade. O TCP e o UDP identificam os aplicativos e acompanham conversas individuais. O UDP não numera segmentos de dados e reconstrói dados na ordem em que é recebido.
    
    Identificar de conversas individuais
    
    identificando os aplicativos
    
    reconstruindo dados na ordem recebida
    
    (x) retransmissão de quaisquer dados não reconhecidos
    
    (x) reconhecendo dados recebidos
    
9. Qual é o propósito de usar um número de porta de origem em uma comunicação TCP?
    
    Tópico 14.4.0 - O número da porta de origem em um cabeçalho de segmento é usado para manter o controle de várias conversas entre dispositivos. Ele também é usado para manter uma entrada aberta para a resposta do servidor. As opções incorretas estão mais relacionadas ao controle de fluxo e entrega garantida.
    
    Para montar os segmentos que chegaram fora de ordem
    
    Para notificar o dispositivo remoto de que a conversa acabou
    
    (x) Para manter o controle de várias conversas entre dispositivos
    
    Para pesquisar um segmento não recebido
    
10. Quais dois sinalizadores no cabeçalho TCP são usados em um handshake de três vias TCP para estabelecer conectividade entre dois dispositivos de rede? (Escolha duas.)
    
    Tópico 14.5.0 - TCP usa os sinalizadores SYN e ACK para estabelecer conectividade entre dois dispositivos de rede.
    
    RST
    
    URG
    
    FIN
    
    (x) ACK
    
    PSH
    
    (x) SYN
    
11. Qual mecanismo TCP é usado para melhorar o desempenho, permitindo que um dispositivo envie continuamente um fluxo contínuo de segmentos, desde que o dispositivo também esteja recebendo as confirmações necessárias?
    
    Tópico 14.6.0 - O TCP usa janelas para tentar gerenciar a taxa de transmissão até o fluxo máximo que a rede e o dispositivo de destino podem suportar, minimizando perdas e retransmissões. O destino pode enviar uma requisição de redução da janela, quando sobrecarregado com dados. O processo de envio de confirmações pelo destino enquanto processa os bytes recebidos, e o ajuste contínuo da janela de envio da origem é conhecido como janelas deslizantes.
    
    handshake duplo
    
    pares de sockets
    
    handshake triplo
    
    (x) Janelas deslizantes
    
12. Qual ação é executada por um cliente ao estabelecer comunicação com um servidor através do uso de UDP na camada de transporte?
    
    Tópico 14.7.0 - Como uma sessão não precisa ser estabelecida para UDP, o cliente seleciona uma porta de origem aleatória para iniciar uma conexão. O número de porta aleatória selecionado é inserido no campo de porta de origem do cabeçalho UDP.
    
    O cliente envia um segmento de sincronização para iniciar a sessão.
    
    O cliente envia um ISN para o servidor para iniciar o handshake de 3 vias.
    
    (x) O cliente seleciona aleatoriamente um número de porta de origem.
    
    O cliente define o tamanho da janela para a sessão.
    
13. Que dois serviços ou protocolos preferem usar o protocolo UDP para agilizar a transmissão e reduzir a sobrecarga? (Escolha duas)
    
    Tópico 14.3.0 - BTanto o DNS quanto o VoIP usam UDP para fornecer serviços de baixa sobrecarga em uma implementação de rede.​
    
    (x) VoIP
    
    (x) DNS
    
    HTTP
    
    FTP
    
    POP3
    
14. Qual número ou conjunto de números representa um soquete?
    
    Tópico 14.4.0 - Um soquete é definido pela combinação de um endereço IP e um número de porta, e identifica exclusivamente uma comunicação específica.
    
    21
    
    01-23-45-67-89-AB
    
    (x) 192.168.1.1:80
    
    10.1.1.15
    
15. O que é uma responsabilidade dos protocolos de camada de transporte?
    
    Tópico 14.1.0 - Existem três responsabilidades principais para protocolos de camada de transporte TCP e UDP:
    
    - Acompanhamento de conversas individuais
    - Segmentando dados e remontando segmentos
    - Identificando os aplicativos
    
    (x) rastreamento de conversas individuais
    
    determinando o melhor caminho para encaminhar um pacote
    
    fornecendo acesso à rede
    
    traduzindo endereços IP privados em endereços IP públicos