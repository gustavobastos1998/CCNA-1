# *Várias comunicações separadas*

- Os protocolos de camada de transporte TCP e UDP usam números de porta para gerenciar várias conversas simultâneas.
- O número da porta de origem está associado ao aplicativo de origem no host local, enquanto o número da porta de destino está associado ao aplicativo de destino no host remoto.
- Por exemplo, suponha que um host está iniciando uma solicitação de página da Web a partir de um servidor Web. Quando o host inicia a solicitação de página da Web, o <mark style="background: #BBFABBA6;">número da porta de origem é gerado dinamicamente</mark> pelo host para identificar exclusivamente a conversa. Cada solicitação gerada por um host usará um número de porta de origem criado dinamicamente diferente. Este processo permite que <mark style="background: #BBFABBA6;">várias conversações ocorram simultaneamente</mark>.
- Na solicitação, o número da porta de destino é o que <mark style="background: #BBFABBA6;">identifica o tipo de serviço que está sendo solicitado</mark> do servidor Web de destino. Por exemplo, quando um cliente especifica a porta 80 na porta de destino, o servidor que receber a mensagem sabe que os serviços Web são solicitados.

# *Pares de sockets*

- A combinação do endereço IP de origem e o número de porta de origem, ou do endereço IP de destino e o número de porta de destino é conhecida como um socket.
- ![[pares de socket.png]]
- Juntos, esses dois sockets se combinam para formar um _par de sockets_: 192.168.1.5:1099, 192.168.1.7:80. Os sockets permitem que vários processos em execução em um cliente se diferenciem uns dos outros, e várias conexões com um processo no servidor sejam diferentes umas das outras.
- Este número de porta age como um endereço de retorno para a aplicação que faz a solicitação. A camada de transporte rastreia essa porta e a aplicação que iniciou a solicitação, de modo que quando uma resposta é retornada, ela pode ser encaminhada para a aplicação correta.

# *Grupo de números de porta*

- ![[grupo de portas.png]]
- **Observação**: Alguns sistemas operacionais clientes podem usar números de porta registrados em vez de números de porta dinâmicos para atribuir portas de origem.
- ![[portas comuns.png]]

# *Comando netstat*

- O netstat é um utilitário de rede importante que pode ser usado para verificar essas conexões.
- Por padrão, o comando **netstat** tentará resolver endereços IP para nomes de domínio e números de porta para aplicativos conhecidos. A**-n** opção pode ser usada para exibir endereços IP e números de porta em sua forma numérica.