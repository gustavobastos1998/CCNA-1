# *Ping loopback*

- Para IPv4 é 127.0.0.1 e IPv6 ::1. Ele indica que o IP  está instalado corretamente no host.
- Essa resposta vem da camada de rede. No entanto, ela não significa que os endereços, as máscaras ou os gateways estão configurados adequadamente.
- Uma mensagem de erro indica que o TCP/IP não está operacional no host.

# *Traceroute*

- É um utilitário que gera uma lista de saltos que foram alcançados com sucesso ao longo do caminho.
- O uso do traceroute fornece tempo de ida e volta para cada salto ao longo do caminho e indica se um salto falha na resposta. O tempo de ida e volta é o tempo que um pacote leva para alcançar o host remoto e retornar a resposta do host. Um asterisco '*' é usado para indicar um pacote perdido ou não respondido.