# *Significado cores*

- <mark style="background: #ABF7F7A6;">ciano</mark> = comando.
- <mark style="background: #BBFABBA6;">verde</mark> = onde o comando deve ser executado.
- <mark style="background: #FFB8EBA6;">roza</mark> = que modo será afetado.
- <mark style="background: #FFF3A3A6;">amarelo</mark> = nome de arquivo.
- <mark style="background: #D2B3FFA6;">roxo</mark> = nota.

# *Nome de dispositivo*

- É importante um nome específico para dispositivos. Assim você saberá se está se conectando com a máquina certa via SSH por exemplo. O nome padrão para um switch Cisco IOS é "Switch". 
- O nome padrão deve ser alterado para algo mais descritivo. Com uma escolha sábia de nomes, é mais fácil lembrar, documentar e identificar dispositivos de rede. Aqui estão algumas diretrizes de nomenclatura importantes para hosts: começar com uma letra; não conter espaços; terminar com dígito ou letra; usar somente letras, números e traços; ter menos de 64 caracteres.
- Para alterar o nome do dispositivo, entre no modo de <mark style="background: #BBFABBA6;">configuração global</mark> usando o comando <mark style="background: #ABF7F7A6;">configure terminal</mark>. Agora, basta usar <mark style="background: #ABF7F7A6;">hostname nome-dispositivo</mark>.

# *Diretrizes de senha*

- Senhas fortes são imprescindíveis para manter a segurança da rede. O Cisco IOS pode ser configurado para usar senhas do modo hierárquico para permitir privilégios de acesso diferentes a um dispositivo de rede.

# *Configurar senha*

- Para por uma senha para acessar o <mark style="background: #FFB8EBA6;">modo de EXEC do usuário</mark>, basta ir para o modo de <mark style="background: #BBFABBA6;">configuração de linha</mark> com o comando <mark style="background: #ABF7F7A6;">line console 0</mark> a partir do mood de configuração global. Também há a possibilidade de atribuir senha para as linhas VTY de 0 a 15 do switch, basta ao invés de usar o <mark style="background: #ABF7F7A6;">line console 0</mark> usar o comando <mark style="background: #ABF7F7A6;">line vty 0 15</mark>. Então, digite o comando <mark style="background: #ABF7F7A6;">password password</mark> e por fim usa o comando login para ativar o acesso EXEC do usuário. Após tudo isso, ao tentar acessar o switch no modo de usuário, a senha criada será exigida.
- Para por uma senha ao <mark style="background: #FFB8EBA6;">modo EXEC privilegiado</mark> basta ir para o modo de <mark style="background: #BBFABBA6;">configuração global</mark> e usar <mark style="background: #ABF7F7A6;">enable secret password</mark>. Assim, ao tentar utilizar o modo EXEC privilegiado a senha será solicitada.

# *Criptografar as senhas*

- Arquivos como <mark style="background: #FFF3A3A6;">startup-config</mark> e <mark style="background: #FFF3A3A6;">runnig-config</mark> exibem a maioria das senhas em texto simples. Para evitar que as senha sejam roubadas todas elas devem ser encriptografadas. 
- O comando <mark style="background: #ABF7F7A6;">service password-encryption</mark> quando executado no modo de <mark style="background: #BBFABBA6;">configuração global</mark> encripta todas as senha não encriptografadas. Ela aplica uma criptografia simples e apenas as senhas no arquivo de configuração. A senhas que são transmitidas pela rede não necessariamente estão encriptografadas. O intuito de encriptografar as senhas aqui é para evitar de alguém mal intencionado de ter acesso direto aos arquivos do dispositivo.
- Para saber se as senhas foram encriptografadas, vá para o <mark style="background: #BBFABBA6;">modo EXEC privilegiado</mark> e digite <mark style="background: #ABF7F7A6;">show running-config</mark>, isso lhe mostrará o conteúdo do arquivo especificado.

# *Mensagens de Banner*

- É uma mensagem que geralmente é usada para informar que somente pessoas autorizadas devem tentar acesso ao dispositivo em quesito. Ajuda na parte burocrática e legal caso alguém seja processado por invadir um dispositivo.
- Em <mark style="background: #BBFABBA6;">configuração global</mark> use <mark style="background: #ABF7F7A6;">banner motd # mensagem#</mark>. 
- <mark style="background: #D2B3FFA6;">Nota</mark>: esse espaço entre o primeiro # e a mensagem não existe, o obsidian encara isso como uma tag. 

