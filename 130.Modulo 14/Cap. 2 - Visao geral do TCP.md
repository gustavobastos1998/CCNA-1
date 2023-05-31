# *Recursos TCP*

- Serviços do TCP:

### **Estabelece uma sessão**

- O TCP é um protocolo orientado à conexão que negocia e estabelece uma conexão permanente entre os dispositivos de origem e destino antes de encaminhar qualquer tráfego. 
- Com o estabelecimento da sessão, os dispositivos negociam o volume de tráfego esperado que pode ser encaminhado em determinado momento e os dados de comunicação entre os dois podem ser gerenciados atentamente. 

### **Garante a entrega confiável**

- Dados podem ser corrompidos ou perdidos por diversos motivos. O TCP  garante que cada segmento enviado chega ao destino.

### **Fornece entrega no mesmo pedido**

- Como as redes podem fornecer várias rotas que podem ter taxas de transmissão diferentes, os dados podem chegar na ordem errada. 
- Ao numerar e sequenciar os segmentos, o TCP garante que os segmentos sejam remontados na ordem correta.

### **Suporta controle de fluxo**

- Hosts de rede têm recursos limitados, ou seja, memória e poder de processamento. O TCP, ao notar que esses recursos estão sobrecarregados, requisita que a aplicação emissora reduza a taxa de fluxo de dados. 
- Esse controle de fluxo pode impedir a necessidade de retransmissão de dados quando os recursos do host receptor estão sobrecarregados. 

# *Cabeçalho TCP*

- TCP é um protocolo stateful, o que significa que ele controla o estado da sessão de comunicação. Para manter o controle do estado de uma sessão, o TCP registra quais informações ele enviou e quais informações foram confirmadas. 
- A sessão com estado começa com o estabelecimento da sessão e termina com o encerramento da sessão.
- ![[cabecalho tcp.png]]

# *Campos de cabeçalho TCP*

- ![[campo cabecalho tcp.png]]

# *Aplicações que usam TCP*

- O TCP lida com todas as tarefas associadas à divisão do fluxo de dados em segmentos, fornecendo confiabilidade, controlando o fluxo de dados e reordenando segmentos.
- Aplicações como as mostradas na imagem, podem simplesmente enviar o fluxo de dados à camada de transporte e usar os serviços TCP.
- ![[aplicacoes que usam tcp.png]]