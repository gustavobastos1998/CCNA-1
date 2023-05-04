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
