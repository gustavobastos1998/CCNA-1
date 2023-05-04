# *Sistemas Operacionais*

- Além dos computadores domésticos e servidores, dispositivos de rede também precisam de um SO. Quase todos os dispositivos da Cisco utilizam o Cisco IOS como sistema operacional.

# *GUI x CLI*

- A diferença é gritante entre eles, o GUI (Graphic User Interface) é uma interface gráfica que permite o usuário interagir com o SO por meio de ícones e com a utilização de mouse.
- É intuitivo o uso de um GUI. Exemplos de GUI: Windows, macOS, Ubuntu, Android etc.
- O CLI (Command Line Interface) é uma interface por linha de comando. Isso significa que o seu uso é exlusivamente com o teclado e exige conhecimento dos comandos necessários para utiliza-lo. 
- É pouco intuitivo, porém todo comando tem um manual de utilização assim como uma flag '--help' que ajuda no uso dos comandos.
- Ambos são usados para interagir com o SO.

# *Objetivo de um SO*

- Tem como principal objetivo executar programas ou comandos que o usuário pede. 

# *Métodos de acesso*

### **Console**

- Porta de gerenciamento físico que fornece acesso fora de banda a um dispositivo Cisco. O acesso out-of-band se refere ao acesso por meio de um canal dedicado de gerenciamento que é usado somente para fins de manutenção do dispositivo. Não necessita de nenhum serviço de rede configurado para fazer o acesso. 
- Um computador com um terminal e um cabo de console especial são necessários para fazer a conexão de console.

### **Secure Shell (SSH)**

- Protocolo para efetuação de acesso remoto a um dispositivo. A comunicação é segura e o usuário tem acesso a um CLI do dispositivo conectado. 
- É necessário serviço de rede ativo para fazer a conexão. 

### **Telnet**

- Método inseguro em banda para estabelecer uma sessão de CLI remotamente, por meo de uma interface virtual, por uma rede. As credenciais do usuário são transmitidos em texto limpo pela rede o que o torna bem inseguro. Só deve ser usado em ambientes de laboratório onde há a certeza de que esses dados não serão vazados ou interceptados.

### **Porta AUX**

- Estabelece uma sessão CLI remotamente por uma conexão telefônica usando um modem. De modo semelhante a uma conexão de console, a porta AUX é do tipo fora de banda e não requer serviços de rede para ser configurada ou estar disponível.