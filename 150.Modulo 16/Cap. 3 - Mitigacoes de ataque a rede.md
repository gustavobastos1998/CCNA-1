# *Abordagem de defesa em camadas*

- A maioria das organizações emprega uma abordagem de defesa profunda (também conhecida como abordagem em camadas) à segurança. Isso requer uma combinação de dispositivos e serviços de rede trabalhando em conjunto.
- Existem vários dispositivos e serviços de segurança que foram implementados para proteger seus usuários e ativos contra ameaças TCP/IP.
- ![[dispositivos e servicos de seguranca.png]]

# *Manter backups*

- Fazer backup de configurações e dados do dispositivo é uma das maneiras mais eficazes de se proteger contra a perda de dados.
- O backup de dados armazena uma cópia das informações de um computador em uma mídia removível de backup que pode ser guardada em um local seguro.
- ![[consideracoes backup.png]]

# *Atualização e patch*

- Manter-se atualizado com os desenvolvimentos mais recentes pode levar a uma defesa mais eficaz contra ataques à rede. 
- Quando um novo malware é lançado, as empresas precisam manter as suas atuais versões de software antivírus atualizadas.
- A forma mais eficaz de reduzir um ataque de worm e baixar as atualizações de segurança do sistema operacional. 

# *Autenticação, autorização e auditoria*

- Os serviços de segurança de rede de autenticação, autorização e auditoria (AAA ou "triplo A") fornecem a estrutura principal para configurar o controle de acesso nos dispositivos de rede.
- O AAA é uma maneira de controlar quem tem permissão para acessar uma rede (autenticar), quais ações eles executam enquanto acessam a rede (autorizar) e fazer um registro do que foi feito enquanto eles estão lá (auditoria).

# *Firewalls*

- Um firewall é uma das ferramentas de segurança disponíveis mais eficazes na proteção dos usuários contra ameaças externas. Um firewall protege computadores e redes impedindo que tráfego indesejável entre em redes internas.
- Os firewalls de rede estão localizados entre duas ou mais redes, e controlam o tráfego entre elas, além de ajudar a evitar o acesso não autorizado.
- ![[operacao do firewall.png]]
- O firewall pode permitir a usuários externos controle sobre alguns serviços específicos. Os servidores acessíveis a usuários externos geralmente estão localizados em uma rede especial referida como a zona desmilitarizada (DMZ). 
- A DMZ permite que um administrador de rede aplique políticas específicas para hosts conectados a essa rede.
- ![[topologia DMZ.png]]

# *Tipos de firewall*

### **Filtragem de pacotes**

- Impede ou permite acesso com base em endereços IP ou MAC.

### **Filtragem de aplicativos**

- Impede ou permite acesso por tipos de aplicativos específicos com base nos números de porta. 

### **Filtragem de URL**

- Impede ou permite acesso a sites com base em URLs ou palavras chave específicas.

### **Filtragem de pacotes com estado (SPI)**

- Os pacotes recebidos devem ser respostas legítimas às solicitações dos hosts internos. Os pacotes não solicitados são bloqueados, a menos os especificamente permitidos. 
- O SPI também pode incluir o recurso de reconhecer e filtrar tipos específicos de ataques como DoS. 

# *Segurança de Endpoints*

- É um laptop, computador, servidor, smartphone ou tablet etc. Um dos problemas mais difíceis de resolver da segurança, porque envolve a natureza humana.
- Uma empresa deve ter obrigatoriamente políticas em vigor bem documentadas e os funcionários devem conhecê-las. Eles devem ser treinados para usarem a rede corretamente. 
- As políticas em geral incluem o uso de software antivírus e prevenção contra invasões. Soluções de segurança de endpoints mais abrangentes baseiam-se no controle de acesso à rede.