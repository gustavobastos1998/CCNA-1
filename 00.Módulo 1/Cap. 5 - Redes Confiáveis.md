# *Arquitetura de Redes*

- Há quatro pilares que tornam uma rede confiável, são eles: tolerância a falhas; escalabilidade; qualidade de serviço (QoS) e segurança.

# *Tolerância a falhas*

- Uma rede tolerante a falhas permite recuperação rápida quando ocorre um problema. Elas dependem de vários caminhos entre a origem e o destino de uma mensagem. Caso um dispositivo falhe, há outro caminho por onde a mensagem pode passar. Ter vários caminhos para a transmissão de dados é conhecido como redundância.
- A implementação de uma rede comutada por pacotes é uma das maneiras pelas quais redes confiáveis fornecem redundância. A comutação de pacotes divide os dados do tráfego em pacotes que são roteados por uma rede compartilhada. Uma única mensagem é dividida em pacotes e transmitida pela rede. Os roteadores alternam os caminhos que os pacotes farão de acordo com o estado da rede no momento.
- Imagem ilustrativa:![[Tolerancia a falhas.png]]

# *Escalabilidade*

- Escalabilidade é a capacidade de expandir algo oferecendo suporte a novos usuários e aplicativos. No caso de redes escalonáveis, é a possibilidade de adicionar um rede nova a uma existente sem prejudicar o desempenho dos serviços que já estão em execução por usuários. 
- Padrões e protocolos são seguidos por projetistas para tornar as redes escalonáveis.
- Imagem ilustrativa:![[escalabilidade.png]]


# *Qualidade de Serviço*

- O QoS é um mecanismo essencial para gerenciar o congestionamento e garantir a entrega confiável do conteúdo da mensagem para todos os usuários. 
- O congestionamento ocorre quando a demanda por largura de banda excede a quantidade disponível. A largura de banda é medida pelo número de bits que podem ser transmitidos em um único segundo. 
- Quando o volume do tráfego é grande demais, os dispositivos retêm os pacotes em memória e os liberam quando os recursos estiverem disponíveis.
- A política de QoS pode configurar uma lista de serviços que devem ser priorizados, tornando serviços mais importantes que outros. Com isso, os que estiverem no topo da lista de prioridade terão os pacotes relacionados a tal serviço transmitidos primeiro. 
- Imagem ilustrativa:![[QoS.png]]

# *Segurança da Rede*

- A infraestrutura da rede, os serviços e os dados contidos nos dispositivos conectados à rede são recursos pessoais e comerciais críticos. Os administradores de rede devem abordar dois tipos de preocupações de segurança de rede: segurança da infraestrutura de rede e segurança da informação. 
- Proteger a infraestrutura de rede inclui proteger fisicamente os dispositivos que fornecem conectividade de rede e impedir o acesso não autorizado ao software de gerenciamento que reside neles. 
- Os administradores de rede também devem se preocupar com as informações dos pacotes transmitidos e insformações armazenadas nos dispositivos conectados à rede. Para atingir os objetivos de segurança de rede, há 3 requisitos principais que devem ser satisfeitos.

### **Confidencialidade**

- Significa que apenas os destinatários pretendidos e autorizados podem ter acesso aos dados.

### **Integridade**

- Garante que as informações não foram alteradas durante a transmissão.

### **Disponibilidade**

- Garante acesso oportuno e confiável aos serviços de dados para usuários autorizados.

- Imagem ilustrativa:![[Segurança redes.png]]

