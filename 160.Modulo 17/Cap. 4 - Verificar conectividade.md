# *Verificação com ping*

- O ping é extremamente útil para verificar conectividade da camada 3. Ele usa mensagens ICMP echo (ICMP type 8) e echo reply (ICMP type 0). 
- O ping, dependendo do SO em que você esteja, informa de maneiras diferentes o echo reply, assim como a quantidade de mensagens ICMP que são enviadas. Para o Cisco IOS o ponto de exclamação indica o recebimento bem sucedido de um echo reply.
- ![[Cisco IOS ping indicators.png]]

# *Ping estendido*

- O Cisco IOS permite o uso de um ping "especial". Esse comando é usado no modo EXEC privilegiado sem o parâmetro do endereço IP. Após clicar a tecla "enter" sem parâmetro, o CLI pedirá algumas informações além do IP address como repeat count, timeout in seconds entre outros.

# *Verificação com traceroute*

- Comando ótimo para verificar se há algo de errado na conectividade da camada 3. Ele não identifica o problema, mas informa cada hop IP da origem ao destino. Com essa informação, fica mais fácil de localizar o ponto de falha.

# *Traceroute estendido*

- Assim como o ping, há também a possibilidade do comando traceroute estendido. Permite ajustar os parâmetros relacionados a essa operação. 
- Como no ping estendido, é so digitar o comando traceroute, sem parâmetros, e clicar enter. Uma série de parâmetros serão solicitados com diversas possibilidades.

# *Linha de Base de Rede*

- Uma das ferramentas mais eficazes para o monitoramento e a solução de problemas de desempenho de rede é estabelecer uma linha de base da rede.
- É realizada ao longo de um período de tempo. Medir o desempenho em momentos e cargas variados ajudará a criar uma imagem melhor do desempenho geral da rede.
- O resultado derivado dos comandos de rede contribui com dados para a linha de base da rede. As informações dos comandos ping e traceroute devem ser armazenadas em arquivos de texto com data atrelada para posterior comparação. 
- Entre itens a serem considerados estão mensagens de erro e os tempos de resposta host a host. Se houver um aumento considerável nos tempos de resposta, pode existir um problema de latência a ser resolvido.