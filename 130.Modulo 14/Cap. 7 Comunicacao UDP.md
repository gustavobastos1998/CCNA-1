# *Baixa Sobrecarga do UDP vs Confiabilidade*

- O UDP fornece transporte de dados de baixa sobrecarga, porque tem um cabeçalho de datagrama pequeno e nenhum tráfego de gerenciamento de rede.

# *Remontagem do datagrama UDP*

- O UDP não rastreia os números de sequência da forma que o TCP faz. O UDP não tem como reordenar os datagramas na sua ordem de transmissão.
- O UDP envia os dados para a camada de aplicação na ordem de chegada. Se a sequência de dados for importante, a aplicação deve tratar disso.
- ![[sem conexao e nao confiavel.png]]

# *Processos em servidores e requisições UDP*

- As aplicações de servidor baseadas em UDP recebem números de portas bem conhecidas ou registradas, assim como as do TCP.

# *Processos em clientes UDP*

- Assim como o TCP, a comunicação cliente servidor é iniciada por uma aplicação cliente que requisita dados de um processo em um servidor. 
- O processo no cliente UDP seleciona dinamicamente um número de porta a partir de uma faixa de números de portas e a usa como a porta de origem para a conversa. 
- A porta de destino será geralmente o número de porta muito conhecida ou registrada atribuído ao processo no servidor.