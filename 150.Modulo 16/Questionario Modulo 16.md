1. Qual componente foi projetado para proteger contra comunicações não autorizadas de e para um computador?
    
    Tópico 16.3.0 - Software antivírus e antimalware são usados para prevenir a infecção por software mal-intencionado. Um scanner de porta é usado para testar uma conexão de rede do PC para determinar quais portas o PC está escutando. O centro de segurança é uma área do Windows que mantém o controle do software de segurança e das configurações no PC. Um firewall foi concebido para bloquear tentativas de ligação não solicitadas a um PC, a menos que sejam especificamente permitidas.
    
    Antivírus
    
    Antimalware
    
    Centro de Segurança
    
    Scanner de porta
    
    (x) Firewall
    
2. Qual comando bloqueará as tentativas de login no RouterA por um período de 30 segundos, se houver duas tentativas de login com falha dentro de 10 segundos?
    
    Tópico 16.4.0 - A sintaxe correta é RouterA(config)# **login block-for** _number of seconds)_ **attempts** (_number of attempts_) **within** (_number of seconds_).
    
    RouterA(config)# **login block-for 10 attempts 2 within 30**
    
    RouterA(config)# **login block-for 2 attempts 30 within 10**
    
    RouterA(config)# **login block-for 30 attempts 10 within 2**
    
    (x) RouterA(config)# **login block-for 30 attempts 2 within 10**
    
3. Qual é o objetivo da função de contabilidade de segurança de rede?
    
    Tópico 16.3.0 - Autenticação, autorização e contabilidade são serviços de rede conhecidos coletivamente como AAA. Autenticação exige que os usuários provem quem são. Autorização determina quais recursos o usuário pode acessar. Accounting rastreia as ações do usuário.
    
    Determinar quais recursos o usuário pode acessar
    
    Fornecer perguntas para desafios e respostas
    
    (x) Rastrear as ações de um usuário
    
    Exigir que os usuários provem quem são
    
4. Que tipo de ataque pode envolver o uso de ferramentas como nslookup e fping**?**
    
    Tópico 16.2.0 - Para ataques de reconhecimento, invasores externos podem usar ferramentas da Internet, como a pesquisa e as facilidades, para determinar facilmente o espaço de endereço IP atribuído a uma determinada corporação ou entidade. Após o espaço de endereçamento IP ser determinado, um invasor pode então, fazer ping para os endereços IP disponíveis publicamente para identificar os endereços que estão ativos.Fping é uma ferramenta de varredura de ping que pode ajudar a automatizar este processo.
    
    Ataque de acesso
    
    Ataque de worms
    
    (x) Ataque de reconhecimento
    
    Ataque de negação de serviço
    
5. Qual o benefício que o SSH oferece sobre o Telnet para gerenciar remotamente um roteador?
    
    Tópico 16.4.0 - SSH fornece acesso seguro a um dispositivo de rede para gerenciamento remoto. Ele usa uma autorização de senha mais forte do que o Telnet faz e criptografa todos os dados que são transportados durante a sessão.
    
    (x) Criptografia
    
    Conexões através de várias linhas VTY
    
    Autorização
    
    Uso do TCP
    
6. Qual é a ferramenta de segurança mais eficaz disponível para proteger os usuários de ameaças externas?
    
    Tópico 16.3.0 - Um firewall é uma das ferramentas de segurança mais eficazes para proteger os usuários internos da rede contra ameaças externas. Um firewall reside entre duas ou mais redes, controla o tráfego entre elas e ajuda a impedir o acesso não autorizado.Um sistema de prevenção de intrusões de host pode ajudar a impedir invasores externos e deve ser usado em todos os sistemas.
    
    (x) Firewalls
    
    Técnicas de criptografia de senha
    
    Servidores de patches
    
    Roteador que execute serviços AAA
    
7. Qual tipo de ameaça à rede destina-se a impedir que usuários autorizados acessem os recursos?
    
    Tópico 16.2.0 - Os ataques de reconhecimento de rede envolvem a descoberta e o mapeamento não autorizados da rede e dos sistemas de rede. Ataques de acesso e exploração de confiança envolvem a manipulação não autorizada de dados, do acesso ao sistema ou de privilégios do usuário. DoS, ou ataques de negação de serviço, destinam-se a impedir que usuários e dispositivos legítimos acessem os recursos da rede.
    
    (x) Ataques de negação de serviço (DoS)
    
    Ataques de reconhecimento
    
    Exploração de confiança
    
    Ataques de acesso
    
8. Quais são os três serviços fornecidos pela estrutura AAA? (Escolha três.)
    
    Tópico 16.3.0 - A estrutura de autenticação, autorização e contabilidade (AAA) fornece serviços para ajudar a proteger ou acessar dispositivos de rede.
    
    (x) Autorização
    
    Autobalanceamento
    
    Autoconfiguração
    
    (x) Autenticação
    
    (x) Contabilidade
    
    Automação
    
9. Qual ataque de código mal-intencionado é autônomo e tenta explorar uma vulnerabilidade específica em um sistema que está sendo atacado?
    
    Tópico 16.2.0 - Um worm é um programa de computador que é auto-replicado com a intenção de atacar um sistema e tentar explorar uma vulnerabilidade específica no alvo. Tanto o vírus como o cavalo de Tróia dependem de um mecanismo de entrega para transportá-los de um hospedeiro para outro. Engenharia social não é um tipo de ataque de código malicioso.
    
    Vírus
    
    (x) Worm
    
    Cavalo de troia
    
    Engenharia social
    
10. Alguns roteadores e switches em um wiring closet deram defeito após uma falha na unidade de ar condicionado. Que tipo de ameaça a situação descreve? 
    
    Tópico 16.1.0 - As quatro classes de ameaças são as seguintes:
    
    - Ameaças de hardware - danos físicos a servidores, roteadores, comutadores, instalações de cabeamento e estações de trabalho
    - Ameaças ambientais - temperaturas extremas (muito quentes ou muito frias) ou umidade extrema (muito úmidas ou muito secas)
    - Ameaças elétricas - picos de tensão, tensão de alimentação insuficiente (quedas de energia), energia não condicionada (ruído) e perda total de energia
    - Ameaças à manutenção - manuseio inadequado dos principais componentes elétricos (descarga eletrostática), falta de peças sobressalentes críticas, cabeamento inadequado e rotulagem inadequada
    
    Elétrica
    
    Manutenção
    
    Configuração
    
    (x) Ambiental
    
11. O que o termo vulnerabilidade significa?
    
    Tópico 16.1.0 - Uma vulnerabilidade não é uma ameaça, mas é uma fraqueza que faz do PC ou do software um alvo de ataques.
    
    Um alvo conhecido ou uma máquina vítima
    
    Uma ameaça em potencial criada por um hacker
    
    Um método de ataque para explorar um alvo
    
    Um computador que contém informações confidenciais
    
    (x) Uma fraqueza que torna um alvo suscetível a um ataque
    
12. Quais três etapas de configuração devem ser executadas para implementar o acesso SSH a um roteador? (Escolha três.)
    
    Tópico 16.4.0 - Para implementar SSH em um roteador, as seguintes etapas precisam ser executadas:
    
    - Configure um nome de host exclusivo.
    - Configure o nome de domínio da rede.
    - Configure uma conta de usuário para usar AAA ou banco de dados local para autenticação.
    - Gere chaves RSA.
    - Ative sessões VTY SSH.
    
    (x) Um nome de domínio IP
    
    (x) Uma conta de usuário
    
    Uma senha de modo habilitado
    
    (x) Um nome de host exclusivo
    
    Uma senha na linha do console
    
    Uma senha criptografada
    
13. Qual é o objetivo de um ataque de reconhecimento de rede?
    
    Tópico 16.2.0 - O objetivo de um ataque de reconhecimento de rede é descobrir informações sobre uma rede, sistemas de rede e serviços de rede.
    
    (x) Descoberta e mapeamento de sistemas
    
    Desativação de sistemas ou serviços de rede
    
    Manipulação não autorizada de dados
    
    Negação de acesso de usuários legítimos aos recursos
    
14. Por motivos de segurança, um administrador de rede precisa garantir que os computadores locais não possam efetuar ping entre si. Quais configurações podem realizar essa tarefa?
    
    Tópico 16.3.0 - As configurações do sistema de arquivos e do cartão inteligente não afetam a operação da rede. As configurações de endereço MAC e a filtragem podem ser usadas para controlar o acesso à rede do dispositivo, mas não podem ser usadas para filtrar diferentes tipos de tráfego de dados.
    
    (x) Configurações de firewall
    
    Configurações de endereço MAC
    
    Configurações do smart card
    
    Configurações do sistema de arquivos
    
15. Um administrador de rede estabelece uma conexão com um switch via SSH. Qual característica descreve exclusivamente a conexão SSH?
    
    Tópico 16.4.0 - SSH fornece um login remoto seguro através de uma interface virtual. O SSH fornece uma autenticação de senha mais forte do que o Telnet. O SSH também criptografa os dados durante a sessão.
    
    (x) acesso remoto a um switch onde os dados são criptografados durante a sessão
    
    acesso direto ao switch através do uso de um programa de emulação de terminal
    
    Acesso fora de banda a um switch através do uso de um terminal virtual com autenticação de senha
    
    Acesso no local a um switch através do uso de um PC conectado diretamente e um cabo do console
    
    Acesso remoto ao comutador através da utilização de uma ligação telefónica telefónica