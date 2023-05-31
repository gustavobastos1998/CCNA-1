# *Recursos UDP*

- UDP é um protocolo de transporte de melhor esforço. O UDP é um protocolo de transporte leve que oferece a mesma segmentação de dados e remontagem que o TCP, mas sem a confiabilidade e o controle de fluxo do TCP.
- Os recursos UDP incluem o seguinte:
	- Os dados são reagrupados na ordem em que são recebidos.
	- Quaisquer segmentos perdidos não são reenviados.
	- Não há estabelecimento de sessão.
	- O envio não é informado sobre a disponibilidade do recurso.

# *Cabeçalho UDP*

- É um protocolo stateless, o que significa que nem o cliente nem o servidor rastreiam o estado da sessão de comunicação. Se a confiabilidade for necessária ao usar o UDP como protocolo de transporte, ela deve ser tratada pela aplicação.
- Um dos requisitos mais importantes para transmitir vídeo ao vivo e voz sobre a rede é que os dados continuem fluindo rapidamente. 
- Vídeo ao vivo e aplicações de voz podem tolerar alguma perda de dados com efeito mínimo ou sem visibilidade e são perfeitos para o UDP.
- Os blocos de comunicação no UDP são chamados de datagramas ou segmentos. Esses datagramas são enviados como o melhor esforço pelo protocolo da camada de transporte.
- ![[cabecalho udp.png]]

# *Campos de cabeçalho UDP*

- ![[campos cabecalho udp.png]]

# *Aplicações que usam UDP*

- ![[aplicacoes que usam udp.png]]
- Embora por padrão DNS e SNMP usem UDP, ambos podem usar TCP. O DNS usará o TCP se a solicitação ou resposta de DNS for maior que 512 bytes, como quando uma resposta de DNS inclui muitas resoluções de nome. 
- Da mesma forma, em algumas situações o administrador de redes pode querer configurar o SNMP para usar o TCP.

### **Aplicativos de vídeo e multimídia ao vivo**

- Esses aplicativos podem tolerar a perda de dados, mas requerem pouco ou nenhum atraso. Os exemplos incluem VoIP e transmissão de vídeo ao vivo.

### **Solicitações Simples e Aplicativos de Resposta**

- Aplicativos com transações simples em que um host envia uma solicitação e pode ou não receber uma resposta. Os exemplos incluem DNS e DHCP.

### **Aplicativos que lidam com a confiabilidade**

- Comunicações unidirecionais em que o controle de fluxo, a detecção de erros, as confirmações e a recuperação de erros não são necessários ou podem ser gerenciados pelo aplicativo. Os exemplos incluem SNMP e TFTP.