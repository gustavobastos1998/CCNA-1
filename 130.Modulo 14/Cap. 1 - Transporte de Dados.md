# *Propósito da Camada de Transporte*

- A camada de transporte e responsável pela comunicação lógica entre os aplicativos executados em hosts diferentes. 
- Isso pode incluir serviços como o estabelecimento de uma sessão temporária entre dois hosts e a transmissão confiável de informações para um aplicativo.
- ![[camada de transporte.png]]
- A camada de transporte não tem conhecimento do tipo de host de destino, o tipo de mídia pela qual os dados devem percorrer, o caminho percorrido pelos dados, o congestionamento em um link ou o tamanho da rede.

# *Responsabilidade da camada de transporte*

### **Rastreamento de Conversações Individuais**

- Na camada de transporte, cada conjunto de dados que flui entre um aplicativo de origem e um aplicativo de destino é conhecido como conversa e é rastreado separadamente. 
- É responsabilidade da camada de transporte manter e monitorar essas várias conversações.
- A maioria das redes tem uma limitação da quantidade de dados que pode ser incluída em um único pacote. Portanto, os dados devem ser divididos em partes gerenciáveis.

### **Segmentação de Dados e Remontagem de Segmentos**

- A camada de transporte é responsável por dividir os dados do aplicativo em blocos de tamanho adequado. Dependendo do protocolo de transporte, esses blocos são chamados de segmentos ou datagramas. 
- ![[segmento-datagrama.png]]

### **Adicionar Informações de Cabeçalho**

- Essas informações contém dados binários organizados em vários campos a cada bloco de dados. 
- São os valores nesses campos que permitem que os vários protocolos da camada de transporte realizem diferentes funções no gerenciamento da comunicação de dados.
- Um exemplo da utilização desse cabeçalho seria para a remontagem dos blocos de dados pelo host receptor. 
- A camada de transporte garante que, mesmo com vários aplicativos em execução em um dispositivo, todos os aplicativos recebam os dados corretos.
- ![[informacoes de cabecalho.png]]

### **Identificação das Aplicações**

- Para passar os dados corretos para as aplicações adequadas a camada de transporte identifica o aplicativo de destino usando um identificador chamado de porta. Como por exemplo a famosa porta 80 para páginas web.
- ![[identificacao de apps.png]]

### **Multiplexação das Conversas**

- A segmentação permite a multiplexação de conversação. A multiplexação permite vários aplicativos usarem a rede ao mesmo tempo. 
- A verificação de erros pode ser realizada nos dados do segmento, para determinar se o segmento foi alterado durante a transmissão.
- ![[multiplexacao.png]]

# *Protocolo TCP (Transmission Control Protocol)*

- É considerado um protocolo de transporte confiável, completo e que garante a chegada de todos os dados ao destino. 
- O TCP inclui campos que garantem a entrega dos dados do aplicativo. Esses campos exigem processamento adicional pelos hosts de envio e recebimento.
- O transporte TCP é análogo a enviar pacotes que são rastreados da origem ao destino.
- O TCP fornece confiabilidade e controle de fluxo usando as operações:
	- Número e rastreamento de segmentos de dados transmitidos para um host específico a partir de um aplicativo específico;
	- Confirmar dados recebidos;
	- Retransmitir todos os dados não confirmados após um determinado período de tempo
	- Dados de sequência que podem chegar em ordem errada
	- Enviar dados a uma taxa eficiente que seja aceitável pelo receptor.
- Para manter o estado de uma conversa e rastrear as informações, o TCP deve primeiro estabelecer uma conexão entre o remetente e o receptor. É por isso que o TCP é conhecido como um protocolo orientado a conexão.

# *Protocolo UDP (User Datagram Protocol)*

- É mais simples que o TCP. Não fornece confiabilidade e controle de fluxo. Tem menos campos que o TCP. 
- São processados mais rápidos que os segmentos TCP, pois o remetente e o receptor não precisam gerenciar confiabilidade e controle de fluxo.
- O UDP fornece as funções básicas para fornecer datagramas entre os aplicativos apropriados, com muito pouca sobrecarga e verificação de dados.
- É um protocolo sem conexão. Como o UDP não fornece confiabilidade e controle de fluxo, ele não requer uma conexão estabelecida. 
- Por não controlar informações enviadas e recebidas também é conhecido como um protocolo stateless. 
- É um protocolo de entrega de melhor esforço por que não há confirmação de que os dados são recebidos no destino. O UDP não verifica se o destinatário está disponível para receber os datagramas.

# *Protocolo certo para aplicativo certo*

### **Utilização do UDP**

- Alguns aplicativos podem tolerar a perda de dados durante a transmissão pela rede, mas atrasos na transmissão são inaceitáveis. Para esses aplicativos, o UDP é a melhor escolha, pois requer menos sobrecarga da rede. O UDP é preferível para aplicativos de <mark style="background: #BBFABBA6;">voz sobre IP (VoIP).</mark> 
- O UDP também é utilizado na solicitação e resposta onde dados são mínimos, e a retransmissão pode ser feita rapidamente. 
- Exemplo disso e o <mark style="background: #BBFABBA6;">serviço DNS</mark> que usa UDP para esse tipo de transmissão. O cliente solicita IPv4 e IPv6 para um dado nome de domínio ao servidor DNS e caso ele não receba uma resposta em um determinado período de tempo, o cliente simplesmente envia novamente a solicitação.  
- Outro exemplo prático é caso um ou dois segmentos de uma transmissão de vídeo ao vivo não consiga chegar ao destino, isso resultará em uma interrupção momentânea na transmissão. Pode ser uma distorção na imagem ou no som. Se o dispositivo de destino <mark style="background: #ABF7F7A6;">considerar os dados perdidos</mark>, a transmissão poderia atrasar, enquanto aguardasse as retransmissões. Dessa forma <mark style="background: #ABF7F7A6;">grandes perdas de áudio e vídeo seriam notadas</mark>. Nesse caso, é melhor fornecer a melhor experiência de mídia com os segmentos recebidos e descartar a confiabilidade.

### **Utilização do TCP**

- Para outras aplicações, é imprescindível a chegada de todos os dados e que possam ser processados em sua sequência adequada. Aplicações de <mark style="background: #BBFABBA6;">bando de dados, navegadores e clientes de email</mark> exigem que todos os dados enviados cheguem ao destino em seu estado original . 
- Quaisquer <mark style="background: #ABF7F7A6;">dados ausentes</mark> podem corromper uma comunicação, tornando-a <mark style="background: #ABF7F7A6;">incompleta ou ilegível</mark>. Por exemplo, é importante ao acessar informações bancárias pela web certificar-se de que todas as informações são enviadas e recebidas corretamente.

### **Escolha do protocolo**

- Essa decisão e dos desenvolvedores de aplicações. Eles devem escolher qual é o mais apropriado com base nas necessidades de suas aplicações. 
- Vídeo pode ser enviado através de TCP ou UDP. Aplicativos de transmissão de de áudio e vídeo armazenados normalmente usam TCP. 
- Vídeo e voz em tempo real geralmente usam UDP, mas também podem usar TCP ou UDP e TCP. 
- Um aplicativo de videoconferência pode usar UDP por padrão, mas como muitos firewalls bloqueiam UDP, o aplicativo também pode ser enviado por TCP.
- Filmes e vídeos no Youtube são transmitidos usando TCP. Caso a rede não comporte a largura de banda necessária para transmissão de um filme ou vídeo, a aplicação interrompe a transmissão. 
- ![[UDP vs TCP.png]]