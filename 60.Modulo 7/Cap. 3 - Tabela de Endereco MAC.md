# *Noções básicas sobre switches*

- Se um switch apenas encaminhasse cada quadro recebido de todas as portas, a rede ficaria tão congestionada que provavelmente chegaria a uma parada completa.
- Um switch Ethernet da camada 2 usa endereços MAC da camada 2 para tomar decisões de encaminhamento. Desconhece completamente os dados (protocolo) que estão sendo transportados na parte de dados do quadro, como um pacote IPv4, uma mensagem ARP ou um pacote ND IPv6. 
- O switch toma suas decisões de encaminhamento com base apenas nos endereços MAC Ethernet da camada 2.
- Um switch Ethernet examina sua tabela de endereços MAC para tomar uma decisão de encaminhamento para cada quadro, ao contrário dos hubs Ethernet herdados que repetem bits em todas as portas, exceto a porta de entrada.

# *Alterar aprendizado e encaminhamento*

- O switch cria a tabela de endereços MAC dinamicamente examinando o endereço MAC de origem dos quadros recebidos em uma porta.O switch encaminha os quadros procurando uma correspondência entre o endereço MAC de destino no quadro e uma entrada na tabela de endereços MAC.

### **Aprendizado**

- Examine o endereço MAC de origem. Todo quadro que entra em um switch é verificado quanto ao aprendizado de novas informações. Se o MAC de origem não existir na tabela, o switch o adiciona juntamente com o número da porta. 
- Se o endereço MAC de origem existir, o switch atualizará o cronômetro de atualização para essa entrada na tabela. Por padrão, uma entrada é mantida na tabela por 5 minutos. 
- **Nota**: Se o endereço MAC de origem não existir na tabela, mas em uma porta diferente, o switch tratará isso como uma nova entrada. A entrada é substituída usando o mesmo endereço MAC, mas com o número de porta mais atual.

# *Encaminhamento*

- Encontre o endereço MAC de destino. Caso o MAC de destino for unicast, o switch procurará seu endereço na tabela. Se o endereço MAC estiver na tabela, ele encaminhará o quadro para a porta específica.
- Caso o switch não conheça o MAC de destino, ele manda o quadro para todas as portas exceto a de entrada. Isso é conhecido como unicast desconhecido.
- Somente o dispositivo com o MAC certo aceitará o quadro.