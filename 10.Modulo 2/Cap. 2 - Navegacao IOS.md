# *Modos de Comando Primários*

- Esse tópico aborda o uso da CLI para navegar pelo Cisco IOS.

### **Modo EXEC de usuário**

- Possui recursos limitados mas é útil para utilizações básicas. Não permite modificação  ou execução de comandos que possam alterar arquivos importantes para o SO. 
- Nível de permissão de usuário comum. 

### **Modo EXEC privilegiado**

- Pode executar tudo no computador. Conhecido como usuário root ou super usuário. Pode ser perigoso pois esse modo privilegiado tem acesso à arquivos que podem comprometer o SO, necessitando de uma formatação na partição onde está o sistema operacional. 

# *Modo de configuração e modos de subconfiguração*

- Para configurar o dispositivo deve-se entrar no modo de configuração global.
- Neste modo, são feitas alterações via CLI que afetam o dispositivo por completo. O modo de configuração global é identificado por um prompt que termina com (config)#após após o nome do dispositivo, como **Switch(config)#**
- No modo de configuração global, o usuário pode inserir diferentes modos de subconfiguração. Dois deles são: modo de configuração de linha e modo de configuração da interface.

### **Modo de configuração de linha**

- Usado para configurar o acesso ao console, SSH, telnet ou Porta AUX.
- Seu prompt padrão aparece da seguinte forma **Switch(config-line)#**. 

### **Modo de configuração da interface**

- Usado para configurar uma porta de switch ou interface de rede do roteador. 
- Seu prompt padrão aparece da seguinte forma **Switch(config-if)#**.

# *Navegar entre os modos do IOS*

- Use o comando **enable** no moco EXEC de usuário para acessar o modo privilegiado. Comando **disable** para fazer o contrário.
- Entrar e sair do modo de configuração global **configure terminal**, deve ser executado no modo privilegiado. Para voltar para o modo EXEC privilegiado use o comando **exit**. 
- **line console 0** para acessar o console de subconfiguração de linha. O parâmetro 'console' diz respeito a conexção entre os dispositivos, por exemplo, a porta RS232 está conectada a um switch com auxilio de um cabo console. **line vty 0 15** é um comando que também acessa o modo de configuração de linha, porém este é utilizado para o virtual terminal management. É usado para acesso remoto de administração do switch.
- O comando **end** volta de qualquer modo de subconfiguração para o modo EXEC privilegiado. Também conseguimos o mesmo resultado usando a hotkey **Ctrl+z**. 
- Pode mudar de um modo de subconfiguração para outro, por exemplo, caso você esteja no modo de configuração de linha e queira ir para o de interface, basta usar o comando **interface FastEthernet 0/1**, esse comando configura a interface para a conexão a porta fastethernet 0/1. Assim como no modo de configuração de linha, você pode especificar qual a conexão que quer para o modo de configuração de interface também. **interface vlan 1** esse comando acessa o modo de configuração de interface que está conectado à vlan 1.


