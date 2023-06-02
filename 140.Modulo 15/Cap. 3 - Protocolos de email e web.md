# *HTTP e HTTPS*

- Os três tipos de mensagens comuns são GET (veja a figura), POST e PUT:
	- **GET** - Esta é uma solicitação de dados do cliente. Um cliente (navegador Web) envia a mensagem GET ao servidor Web para requisitar páginas HTML.
	- **POST** - Isso carrega arquivos de dados no servidor da web, como dados do formulário.
	- **PUT** - Isso carrega recursos ou conteúdo para o servidor da web, como uma imagem.
- ![[http get.png]]
- Apesar do HTTP ser flexível ele não é seguro. Os textos enviados pela rede não são criptografados. Para resolver esse problema o protocolo HTTP Secure (HTTPS) é utilizado para manter um alto nível de segurança. 

# *Protocolos de E-mail*

### **SMTP**

- Os formatos de mensagens SMTP exigem um cabeçalho de mensagem e um corpo de mensagem.
- Depois que a conexão é feita, o cliente tenta enviar o e-mail para o servidor através da conexão. 
- Quando o servidor recebe a mensagem, ele a coloca em uma conta local, se o destinatário for local, ou encaminha a mensagem para outro servidor de correio para entrega.
- O servidor de e-mail de destino pode não estar on-line ou estar ocupado quando as mensagens de e-mail são enviadas. Portanto, o SMTP armazena mensagens a serem enviadas mais tarde.
- Periodicamente, o servidor verifica se há mensagens na fila e tenta enviá-las novamente. Se a mensagem ainda não for entregue após um período pré-determinado de expiração, ela é devolvida ao remetente como não entregue.
- ![[smtp.png]]

### **POP**

- O POP é usado por uma aplicação para recuperar e-mails de um servidor de e-mail. 
- Com o POP, o e-mail será transferido do servidor ao cliente e excluído do servidor. Esta é a operação padrão do POP.
- O servidor inicia o serviço POP ao escutar de forma passiva a porta TCP 110 por requisições de conexão dos clientes. 
- Quando um cliente deseja fazer uso do serviço, ele envia uma solicitação para estabelecer uma conexão TCP com o servidor.
- Com o POP, as mensagens de e-mail são baixadas para o cliente e removidas do servidor, portanto não há um local centralizado onde as mensagens de e-mail sejam mantidas.
- POP3 é a versão mais usada.
- ![[POP3.png]]

### **IMAP**

-  O IMAP é outro protocolo que descreve um método para recuperar mensagens de e-mail. Ao contrário do POP, as mensagens originais são mantidas no servidor até que sejam excluídas manualmente. 
- Os usuários exibem cópias das mensagens em seu software cliente de e-mail. Quando um usuário decide excluir uma mensagem, o servidor sincroniza essa ação e exclui a mensagem do servidor.
- ![[IMAP.png]]