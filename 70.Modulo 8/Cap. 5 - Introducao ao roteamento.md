# *Decisão de encaminhamento de pacotes do roteador*

- Quando um host envia um pacote para outro host, ele consulta sua tabela de roteamento para determinar para onde enviar o pacote.
- Se o host de destino estiver em uma rede remota, o pacote será encaminhado para o gateway padrão, que geralmente é o roteador local.
- O roteador examina o endereço IP de destino do pacote e pesquisa sua tabela de roteamento para determinar para onde encaminhar o pacote. 
- A tabela de roteamento contém uma lista de todos os endereços de rede conhecidos (prefixos) e para onde encaminhar o pacote. 
- Essas entradas são conhecidas como entradas de rota ou rotas. O roteador encaminhará o pacote usando a melhor (mais longa) entrada de rota correspondente.
- ![[decisao roteamento.png]]
- ![[tabela de roteamento.png]]

# *Tabela de Roteamento do Roteador IP*

- A tabela de roteamento do roteador contém entradas de rota de rede listando todos os possíveis destinos de rede conhecidos.
- A tabela de roteamento armazena 3 tipos de entradas de rota.
- ![[tipos entrada de rota.png]]
- Um roteador pode aprender sobre redes remotas de duas maneiras:
	- **Manualmente** - As redes remotas são inseridas manualmente na tabela de rotas usando rotas estáticas.
	- **Dinamicamente** - As redes remotas são aprendidas automaticamente usando um protocolo de roteamento dinâmico.

### **Redes conectadas diretamente**

- Essas entradas de rota de rede são interfaces de roteador ativas. Cada porta do roteador está conectada a um segmento de rede diferente. 
- Na figura, as redes diretamente conectadas na tabela de roteamento IPv4 R1 seriam 192.168.10.0/24 e 209.165.200.224/30.

### **Redes Remotas**

- Essas entradas de rotas de rede são conectadas a outros roteadores. 
- Os roteadores aprendem sobre redes remotas sendo explicitamente configurados por um administrador ou trocando informações de rota usando um protocolo de roteamento dinâmico. 
- Na figura, a rede remota na tabela de roteamento IPv4 R1 seria 10.1.1.0/24.

### **Rota padrão**

- Como um host, a maioria dos roteadores também inclui uma entrada de rota padrão, um gateway de último recurso. A rota padrão é usada quando não há correspondência melhor na tabela de roteamento IP. Na figura, a tabela de roteamento IPv4 R1 provavelmente incluiria uma rota padrão para encaminhar todos os pacotes para o roteador R2.

# *Roteamento estático*

- São entradas de rota configuradas manualmente. 
- A rota estática inclui o endereço de rede remota e o endereço IP do roteador de salto seguinte.
- ![[config roteamento estatico.png]]
- Caso haja alguma mudança na topologia da rede a rota estática não será atualizada automaticamente. Para que a rota seja atualizada, ela deverá ser reconfigurada manualmente. 
- ![[reconfig roteamento estatico.png]]
- O roteamento estático é perfeito para redes pequenas quando há poucos ou nenhum vínculo redundante.
- Uma rota estática é comumente usada com um protocolo de roteamento dinâmico para configurar uma rota padrão.

# *Roteamento dinâmico*

- Um protocolo de roteamento dinâmico permite que os roteadores aprendam automaticamente sobre redes remotas, incluindo uma rota padrão, de outros roteadores.
- Os roteadores compartilham automaticamente informações de roteamento uns com os outros e compensam qualquer alteração de topologia sem envolver o administrador de rede. 
- Se houver uma mudança na topologia de rede, os roteadores se informam e atualizam automaticamente suas tabelas de roteamento.
- ![[roteamento dinamico.png]]
- A configuração básica requer apenas que o administrador de rede habilite as redes conectadas diretamente dentro do protocolo de roteamento dinâmico. O protocolo de roteamento dinâmico fará automaticamente o seguinte:
	- Descobrir redes remotas;
	- Manter as informações de roteamento atualizadas;
	- Escolha o melhor caminho para as redes de destino;
	- Tente encontrar um novo melhor caminho se o caminho atual não estiver mais disponível.
- Quando o roteador é configurado manualmente ou quando usa um protocolo de roteamento dinâmico o endereço de rede remota e o endereço do próximo hop são inseridos na tabela de roteamento.

# *Introdução a uma tabela de roteamento IPv4*

- ![[ip route comando.png]]
- A tabela de roteamento exibe todas as rotas de destino IPv4 conhecidas para um roteador. 
- Uma rota diretamente conectada é criada automaticamente quando uma interface do roteador é configurada com informações de endereço IP e é ativada. 
- Uma rota padrão tem um endereço de rede de todos os zeros. Por exemplo, o endereço de rede IPv4 é 0.0.0.0. 
- Uma entrada de rota estática na tabela de roteamento começa com um código de S*, conforme destacado no exemplo.