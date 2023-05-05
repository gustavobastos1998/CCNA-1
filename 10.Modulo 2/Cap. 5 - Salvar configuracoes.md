
# *Significado cores*

- <mark style="background: #ABF7F7A6;">ciano</mark> = comando.
- <mark style="background: #BBFABBA6;">verde</mark> = onde o comando deve ser executado.

# *Arquivos de configuração*

- Há dois arquivos que armazenam a configuração do dispositivo:

### **startup-config**

- Salva armazenamento na NVRAM. 
- Contém todos os comandos que serão usados pelo dispositivo na inicialização ou reiniciação. 
- O flash não perde seu conteúdo ao desligar o dispositivo. 

### **running-config**

- Armazenado na RAM. 
- Reflete a configuração atual.
- Modificar algo que está ativo afeta o funcionamento do dispositivo Cisco imediatamente. 
- Ao desligar ou reiniciar o dispositivo todo seu conteúdo é perdido. Para que as alterações não sejam perdidas caso algo aconteça, use o comando <mark style="background: #ABF7F7A6;">copy running-config startup-config</mark> no <mark style="background: #BBFABBA6;">modo EXEC privilegiado</mark>. 

# *Alterar configuração ativa*

- Caso uma modificação seja feita e não é exatamente como o esperado, no <mark style="background: #BBFABBA6;">modo EXEC privilegiado</mark> use o comando <mark style="background: #ABF7F7A6;">reload</mark>. Ao fazer isso, o IOS percebe que alterações foram feitas e pergunta antes de dar o reboot se quer que as alterações sejam feitas, basta digitar 'n' ou 'no' e elas serão descartadas. 
- Caso as alterações foram salvas e deseja voltar para a configuração de fábrica, utilize o comando <mark style="background: #ABF7F7A6;">erase startup-config</mark> em <mark style="background: #BBFABBA6;">modo EXEC privilegiado</mark>. 