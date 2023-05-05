# *Nome de dispositivo*

- É importante um nome específico para dispositivos. Assim você saberá se está se conectando com a máquina certa via SSH por exemplo. O nome padrão para um switch Cisco IOS é "Switch". 
- O nome padrão deve ser alterado para algo mais descritivo. Com uma escolha sábia de nomes, é mais fácil lembrar, documentar e identificar dispositivos de rede. Aqui estão algumas diretrizes de nomenclatura importantes para hosts: começar com uma letra; não conter espaços; terminar com dígito ou letra; usar somente letras, números e traços; ter menos de 64 caracteres.
- Para alterar o nome do dispositivo, entre no modo de configuração usando o comando **configure terminal**. Agora, basta usar **hostname nome-dispositivo**.

# *Diretrizes de senha*

- Senhas fortes são imprescindíveis para manter a segurança da rede. O Cisco IOS pode ser configurado para usar senhas do modo hierárquico para permitir privilégios de acesso diferentes a um dispositivo de rede.

# *Configurar senha*

- Para por uma senha para acessar o modo de EXEC do usuário, basta ir para o modo de configuração de linha com o comando **line console 0** a partir do mood de configuração global. Então, digite o comando **password password** e por fim usa o comando login para ativar o acesso EXEC do usuário. Após tudo isso, ao tentar acessar o switch no modo de usuário, a senha criada será exigida.
- Para por uma senha ao modo EXEC privilegiado basta ir para o modo de configuração global e usar **enable secret password**. Assim, ao tentar utilizar o modo EXEC privilegiado a senha será solicitada.

# *Criptografar as senhas*

- Arquivos como startup-config e runnig-config exibem a maioria das senhas em texto simples. Para evitar que as senha sejam roubadas todas elas devem ser encriptografadas. 
- O comando **service password-encryption** quando executado no modo de configuração global encripta todas as senha não encriptografadas. Ela aplica  uma criptografia simples e apenas as senhas no arquivo de configuração. A senhas que são transmitidas pela rede não necessariamente estão encriptografadas. O intuito de encriptografar as senhas aqui é para evitar de alguém mal intencionado de ter acesso direto aos arquivos do dispositivo.
- Para saber se as senhas foram encriptografadas, vá para o modod EXEC privilegiado e digite **show running-config**, isso lhe mostrará o conteúdo do arquivo especificado.

# *Mensagens de Banner*

