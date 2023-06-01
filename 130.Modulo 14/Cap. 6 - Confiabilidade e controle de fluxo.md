# *Confiabilidade do TCP - Entrega garantida e solicitada*

- Os segmentos TCP podem não chegar no destino. Outras vezes, os segmentos podem chegar fora de ordem. Para a mensagem original ser entendida com exatidão, no cabeçalho do TCP são atribuídos os números de sequência. 
- O número de sequência representa o primeiro byte de dados do segmento TCP. 
- Durante o estabelecimento de uma sessão, um número de sequência inicial (ISN) é definido. Este ISN representa o valor inicial dos bytes que são transmitidos ao aplicativo receptor. O ISN não começa em um por motivos de segurança. Isso impede que determinados tipos de ataques maliciosos sejam executados. 
- À medida que os dados são transmitidos durante a sessão, número de sequência é incrementado do número de bytes que foram transmitidos. 
- Esse rastreamento dos bytes de dados permite que cada segmento seja identificado e confirmado de forma única. Segmentos perdidos podem então, ser identificados.
- Exemplo: um segmento inicial com 10 bytes de comprimento e ISN 1 é enviado para o destino. O destino recebe o segmento e informa ao outro host que o próximo que ele espera é o ISN+valor do comprimento de bytes, neste caso 11. 
- ![[ISN.png]]
- O TCP receptor coloca os dados de um segmento em um buffer. Os segmentos são então colocados na ordem de sequência correta e passados para a camada de aplicação quando remontados. 

# *Confiabilidade do TCP - perda de dados e retransmissão*

- O número de sequência (SEQ) e o número de confirmação (ACK) são usados juntamente para confirmar o recebimento dos bytes de dados contidos nos segmentos. 
- O número SEQ identifica o primeiro byte de dados no segmento que está sendo transmitido. 
- O TCP usa o número de confirmação (ACK) enviado de volta à origem para indicar o próximo byte que o destino espera receber. Isto é chamado de confirmação antecipatória.
- Antes das melhorias para o TCP, ele só podia reconhecer o próximo byte esperado. Caso um host envie 10 segmentos para outro, e o terceiro e quarto não cheguem por algum motivo, o host que recebe os segmentos enviará um ACK igual a 3 pois está esperando o terceiro segmento que não chegou.
- O host que envia não tem ideia de quais segmentos não chegaram, então ele envia o terceiro e todos os que vem depois deste. Isso gera uma duplicação dos segmentos 5 até 10. Pode gerar atrasos, congestionamento e ineficiência.
- ![[segmentos duplicados.png]]
- Hoje em dia, os sistemas operacionais de host utilizam um recurso TCP opcional chamado reconhecimento seletivo (SACK), negociado durante o three way handshake. 
- Se ambos os hosts suportarem SACK, o receptor pode reconhecer quais segmentos foram recebidos. Desta maneira, o host ao enviar uma mensagem de volta para o primeiro informando qual segmento espera ser o próximo, ele também informa quais segmentos foram recebidos. 
- ![[SACK.png]]
- O TCP, normalmente, envia ACKs para todos os outros pacotes. O TCP usa temporizadores para saber quanto tempo esperar antes de reenviar um segmento.

# *Controle de fluxo - Tamanho de janela e confirmações*

- O TCP também fornece mecanismos para controle de fluxo. Controle de fluxo é a quantidade de dados que o destino pode receber e processar de forma confiável. 
- O controle de fluxo ajuda a manter a confiabilidade da transmissão TCP definindo a taxa de fluxo de dados entre a origem e o destino em uma determinada sessão. Para realizar isso, o cabeçalho TCP inclui um campo de 16 bits chamado de tamanho da janela.
- ![[tamanho da janela tcp.png]]
- O tamanho da janela determina o número de bytes que podem ser enviados antes de esperar uma confirmação. O número de reconhecimento é o número do próximo byte esperado.
- O tamanho da janela inicial é determinado quando a sessão é estabelecida durante o three way handshake. 
- **Nota**: Os dispositivos hoje usam o protocolo de janelas deslizantes. O receptor normalmente envia uma confirmação após cada dois segmentos que recebe. O número de segmentos recebidos antes de ser confirmado pode variar. A vantagem de janelas deslizantes é que permite que o emissor transmita continuamente segmentos, desde que o receptor esteja reconhecendo segmentos anteriores.

# *Controle de fluxo TCP - tamanho máximo do segmento*

- Na figura, a fonte está transmitindo 1.460 bytes de dados dentro de cada segmento TCP. Normalmente, este é o tamanho máximo do segmento (MSS) que o dispositivo de destino pode receber. O MSS faz parte do campo de opções no cabeçalho TCP que especifica a maior quantidade de dados, em bytes, que um dispositivo pode receber em um único segmento TCP. O tamanho do MSS não inclui o cabeçalho TCP. O MSS é normalmente incluído durante o three way handshake.
- Um MSS comum é 1.460 bytes ao usar IPv4. Um host determina o valor do campo de MSS subtraindo os cabeçalhos de IP e de TCP da MTU (Maximum transmission unit, Unidade máxima de transmissão) da Ethernet.
- ![[tamanho mss.png]]

# *Controle de fluxo TCP - Prevenção de Congestionamento*

- Ao determinar a taxa na qual os segmentos TCP são enviados, mas não confirmados, a origem pode pressupor um certo nível de congestionamento da rede.
- Sempre que ocorrer um congestionamento, ocorrerá a retransmissão de segmentos TCP perdidos por parte da origem.
- Se a retransmissão não for devidamente controlada, a retransmissão adicional dos segmentos TCP pode agravar o congestionamento. O TCP emprega alguns mecanismos para lidar com o congestionamento, temporizadores e algoritmos.
- Se a origem determina que os segmentos TCP não são confirmados ou não são confirmados em tempo hábil, isso pode reduzir o número de bytes enviados antes do recebimento de uma confirmação. 
- Conforme ilustrado na figura, o PC A detecta que há congestionamento e, portanto, reduz o número de bytes que envia antes de receber uma confirmação do PC B.
- ![[controle de congestionamento.png]]