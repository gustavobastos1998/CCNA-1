1. Em uma rede doméstica, qual dispositivo mais provavelmente fornecerá o endereçamento IPv4 dinâmico aos clientes na rede doméstica?
    
    Tópico 15.4.0 - Em uma rede doméstica, um roteador doméstico geralmente serve como servidor DHCP. O roteador doméstico é responsável por atribuir endereços IPv4 dinamicamente a clientes na rede doméstica. Os ISPs também usam o DHCP, mas normalmente atribuem um endereço IPv4 à interface de Internet do roteador doméstico, e não aos clientes na rede doméstica. As empresas costumam ter um servidor de arquivos ou outro servidor dedicado para fornecer serviços DHCP à rede. Por fim, um servidor DNS é responsável por encontrar o endereço IP de uma URL, e não por fornecer endereçamento dinâmico aos clientes da rede.
    
    Um servidor de arquivos dedicado
    
    Um servidor DHCP do ISP
    
    (x) Um roteador doméstico
    
    Um servidor DNS
    
2. Que parte da URL, http:[](https://contenthub.netacad.com/itn-dl/15.6.1)//www.cisco[](https://contenthub.netacad.com/itn-dl/15.6.1).com/index.html, representa o domínio DNS de nível superior?
    
    Tópico 15.4.0 - Os componentes do URL http:[](https://contenthub.netacad.com/itn-dl/15.6.1)//www.cisco[](https://contenthub.netacad.com/itn-dl/15.6.1).com/index.html são os seguintes:
    
    - http = protocolo
    - www = parte do nome do servidor
    - cisco = parte do nome do domínio
    - index = nome do arquivo
    - com = o domínio de nível superior
    
    Indice
    
    (x) .com
    
    http
    
    www
    
3. Quais são duas características da camada de aplicação do modelo TCP/IP? (Escolha duas.)
    
    Tópico 15.1.0 - A camada de aplicação do modelo TCP / IP é a camada mais próxima do usuário final, fornecendo a interface entre as aplicações. Ela é responsável pela formatação, compressão e criptografia dos dados, além de ser usada na criação e manutenção de diálogos entre as aplicações origem e destino.
    
    Responsabilidade pelo endereçamento físico
    
    é responsável pelo endereçamento lógico
    
    (x) A mais próxima do usuário final
    
    (x) A criação e manutenção de diálogo entre aplicativos de origem e destino
    
4. Que tipo de mensagem é usado por um cliente HTTP para solicitar dados de um servidor da Web?
    
    Tópico 15.3.0 - Clientes HTTP enviam mensagens GET para solicitar dados de servidores web.
    
    (x) GET
    
    ACK
    
    POST
    
    PUT
    
5. Qual protocolo pode ser usado para transferir mensagens de um servidor de e-mail para um cliente de e-mail?
    
    Tópico 15.3.0 - O SMTP é usado para enviar e-mails do cliente para o servidor, mas o POP3 é usado para baixar e-mails do servidor para o cliente. Os protocolos HTTP e SNMP não são usados para recuperar mensagens de e-mail.
    
    SMTP
    
    HTTP
    
    SNMP
    
    (x) POP3
    
6. Qual protocolo da camada de aplicação é usado para oferecer serviços de compartilhamento de arquivos e impressão às aplicações da Microsoft?
    
    Tópico 15.5.0 - SMB é usado nas redes Microsoft para compartilhamento de arquivos e serviços de impressão. O sistema operacional Linux tem um método de compartilhar recursos com redes da Microsoft usando uma versão do protocolo SMB chamada SAMBA.
    
    SMTP
    
    (x) SMB
    
    DHCP
    
    HTTP
    
7. Quais são os três protocolos ou padrões usados na camada de aplicação do modelo TCP/IP? (Escolha três.)
    
    Tópico 15.1.0 - HTTP, MPEG e GIF operam na camada de aplicação do modelo TCP / IP. TCP e UDP operam na camada de transporte. IP opera na camada de Internet.
    
    (x) MPEG
    
    IP
    
    UDP
    
    (x) HTTP
    
    TCP
    
    (x) GIF
    
8. Por que o DHCP para IPv4 é recomendável para redes grandes?
    
    Tópico 15.4.0 - A atribuição de endereço IPv4 estático requer que a equipe configure cada host de rede com endereços manualmente. As redes grandes podem mudar com frequência e ter muito mais hosts para configurar do que as redes menores. O DHCP é muito mais eficiente para configurar e gerenciar endereços IPv4 em redes grandes do que a atribuição de endereços estáticos.
    
    Ele evita o compartilhamento de arquivos de propriedade intelectual.
    
    Os hosts de redes grandes precisam de mais definições de configurações de endereçamentos IPv4 do que os hosts de redes pequenas.
    
    (x) É mais eficiente para gerenciar endereços IPv4 do que a atribuição de endereços estáticos.
    
    As redes grandes enviam mais requisição de domínio para a resolução de endereço IP do que as redes menores.
    
    O DHCP usa um protocolo de camada de transporte confiável.
    
9. Um autor está carregando um documento de um capítulo de um computador pessoal para um servidor de arquivos de uma editora. Que função desempenha o computador pessoal neste modelo de rede?
    
    Tópico 15.2.0 - No modelo de rede cliente / servidor, um dispositivo de rede assume a função de servidor para fornecer um serviço específico, como transferência e armazenamento de arquivos. O dispositivo que requisita o serviço desempenha a função de cliente. No modelo de rede cliente/servidor, um servidor dedicado não precisa necessariamente ser usado, mas se houver um, o modelo de rede em uso é o modelo cliente/servidor. Ao contrário de um modelo de rede peer-to-peer que não tem um servidor dedicado.
    
    Slave
    
    Master
    
    (x) Cliente
    
    Servidor
    
    Transitório
    
10. Qual afirmação é verdadeira sobre o FTP?
    
    Tópico 15.5.0 - FTP é um protocolo cliente/servidor. O FTP requer duas conexões entre o cliente e o servidor e usa TCP para fornecer conexões confiáveis. Com o FTP, a transferência de dados pode ocorrer em qualquer direção. O cliente pode transferir dados (receber) do servidor ou fazer upload de dados (enviar) para o servidor.
    
    O cliente pode escolher se o FTP vai estabelecer uma ou duas conexões com o servidor.
    
    (x) O cliente pode baixar ou fazer upload de dados para o servidor.
    
    O FTP é um aplicativo ponto a ponto.
    
    O FTP não fornece confiabilidade durante a transmissão de dados.
    
11. Um host sem fio deve requisitar um endereço IPv4. Qual protocolo deve ser usado para processar a requisição?
    
    Tópico 15.4.0 - O protocolo DHCP é usado para solicitar, emitir e gerenciar informações de endereçamento IP. CSMA/CD é o método de acesso usado com a Ethernet com fio. O ICMP é usado para testar a conectividade. O SNMP é usado para o gerenciamento de rede e o FTP é usado para transferência de arquivos.
    
    FTP
    
    (x) DHCP
    
    ICMP
    
    HTTP
    
    SNMP
    
12. Qual camada do modelo TCP/IP fica mais próxima do usuário final?
    
    Tópico 15.1.0 - Usuários finais usam aplicativos para interagir e usar a rede. A camada de aplicação do modelo TCP/IP fica mais próxima do usuário final. Os protocolos da camada de aplicação são utilizados para a comunicação e a troca de mensagens com outros dispositivos e aplicações da rede. Estas são as camadas do modelo TCP/IP de cima para baixo (dica de memorização: ATIA): aplicação, transporte, internet e acesso à rede
    
    (x) Aplicação
    
    Acesso à rede
    
    Transporte
    
    Internet
    
13. Ao recuperar mensagens de e-mail, qual protocolo permite armazenamento e backup fáceis e centralizados de e-mails que seriam desejáveis para uma pequena e média empresa?
    
    Tópico 15.3.0 - IMAP é preferido para pequenas e médias empresas, pois IMAP permite armazenamento centralizado e backup de e-mails, com cópias dos e-mails sendo encaminhadas para clientes. POP entrega os e-mails para os clientes e os exclui no servidor de e-mail. SMTP é usado para enviar e-mails e não para recebê-los. HTTPS não é usado para navegação segura na Web.
    
    (x) IMAP
    
    SMTP
    
    HTTPS
    
    POP
    
14. Qual protocolo usa criptografia?
    
    Tópico 15.1.0 - HTTPS usa SSL (Secure Socket Layer) para criptografar o tráfego acessado de um servidor Web.
    
    (x) HTTPS
    
    DHCP
    
    FTP
    
    DNS
    
15. Quais as duas tarefas que podem ser executadas por um servidor DNS local? (Escolha duas.)
    
    Tópico 15.4.0 - Duas funções importantes do DNS são (1) fornecer endereços IP para nomes de domínio como www.cisco.com e (2) encaminhar solicitações que não podem ser resolvidas para outros servidores para fornecer nome de domínio para IPO DHCP fornece informações de endereçamento IP para dispositivos locais. Um protocolo de transferência de arquivos como FTP, SFTP, ou TFTP fornece serviço de compartilhamento de arquivos. IMAP ou POP pode ser usado para recuperar uma mensagem de e-mail em um servidor.
    
    (x) Mapear nome para endereço IP para hosts internos
    
    Recuperar mensagens de e-mail
    
    Permitir a transferência de dados entre dois dispositivos de rede
    
    Fornecer endereços IP para hosts locais
    
    (x) Encaminhar requisições de resolução de nome entre servidores