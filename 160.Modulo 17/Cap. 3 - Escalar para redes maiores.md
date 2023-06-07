# *Crescimento de redes pequenas*

- O crescimento é um processo natural para muitas empresas de pequeno porte, e suas redes devem acompanhá-lo. Para escalonar uma rede, vários elementos são necessários:
	- **Documentação de rede** - Topologia física e lógica
	- **Inventário de dispositivos** - Lista de dispositivos que usam ou compreendem a rede
	- **Orçamento** - orçamento de TI detalhado, incluindo orçamento de compra de equipamentos do ano fiscal
	- **Análise de tráfego** - Protocolos, aplicativos e serviços e seus respectivos requisitos de tráfego devem ser documentados

# *Análise de Protocolos*

- É importante entender o tipo de tráfego que está atravessando a rede, bem como o fluxo de tráfego atual. A imagem a seguir exibe estatísticas de hierarquia de protocolo Wireshark para um host windows em uma pequena rede. 
- ![[wireshark hierarquia protocolos.png]]
- Para determinar os padrões de fluxo de tráfego, é importante fazer o seguinte:
	- Capturar o tráfego durante as horas de pico de utilização para obter uma boa ideia dos diferentes tipos de tráfego.
	- Realize a captura em diferentes segmentos e dispositivos de rede, pois algum tráfego será local para um segmento específico.
- As informações reunidas são avaliadas com base na origem e destino do tráfego, bem como o tipo de tráfego que é enviado. Essa análise ajuda a como gerenciar o tráfego com mais eficiência. 
- Pode ser feito reduzindo fluxo de tráfego desnecessário ou alternando totalmente os padrões de fluxo com a mudança de um servidor.

# *Utilização da Rede pelos Funcionários*

- Muitos sistemas operacionais fornecem ferramentas integradas para exibir essas informações. Por exemplo, um host Windows fornece ferramentas como o gerenciador de tarefas, visualizador de eventos e ferramentas de uso de dados.
- Documentar snapshots é muito útil para identificar requisitos de protocolos em evolução e fluxos de tráfego associados. 