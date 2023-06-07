# *Abordagens de solução de problemas básica*

- Os problemas de rede podem ser simples ou complexos e podem resultar de uma combinação de problemas de hardware, software e conectividade.
- ![[resolucao de problema.png]]

# *Resolver ou escalonar?*

- Em algumas situações, talvez não seja possível resolver o problema imediatamente. Um problema deve ser escalado quando requer uma decisão do gerente, algum conhecimento específico ou nível de acesso à rede indisponível para o técnico de solução de problemas.
- Uma política da empresa deve indicar claramente quando e como um técnico deve escalar um problema.

# *O comando de debug*

- O comando IOS **debug** permite que o administrador exiba essas mensagens em tempo real para análise. 
- O Cisco IOS permite restringir a saída para incluir **debug** apenas o recurso ou sub funcionalidade relevante. Isso é importante porque a depuração da saída recebe alta prioridade no processo da CPU e pode travar o sistema.
- Para desativar o debug use o comando 'no' para o recurso específico. Exemplo: <mark style="background: #ABF7F7A6;">debug ip icmp</mark>, para ativar a depuração e <mark style="background: #ABF7F7A6;">no debug ip icmp</mark> para desativar. 
- Também pode usar o comando <mark style="background: #ABF7F7A6;">undebug</mark>, ou <mark style="background: #ABF7F7A6;">undebug all</mark> para desativar todos os debugs. 

# *O Comando terminal monitor*

- Determinadas mensagens IOS são exibidas automaticamente em uma conexão de console, mas não em uma conexão remota.
- Por exemplo, as saídas do debug são exibidas por padrão em conexões de console porém não em conexões remotas. Para poder visualizar, use o comando <mark style="background: #ABF7F7A6;">terminal monitor</mark> para poder ter acesso à essas informações.
- O comando <mark style="background: #ABF7F7A6;">terminal no monito</mark>r é usado para desfazer o efeito do primeiro. 