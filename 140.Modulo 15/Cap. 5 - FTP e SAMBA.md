# *Protocolo FTP*

- O FTP foi desenvolvido para possibilitar transferências de arquivos entre um cliente e um servidor. Um cliente FTP é um aplicativo que é executado em um computador que está sendo usado para enviar e receber dados de um servidor FTP.
- ![[conexao ftp.png]]

# *Protocolo SMB (SAMBA)*

- O Server Message Block (SMB) é um protocolo de compartilhamento de arquivos cliente/servidor, que descreve a estrutura de recursos de rede compartilhados, como diretórios, arquivos, impressoras e portas seriais.
- Aqui estão três funções de mensagens SMB:
	- Iniciar, autenticar e encerrar sessões.Iniciar, autenticar e encerrar sessões.
	- Arquivo de controle e acesso à impressora.
	- Permitir que um aplicativo envie ou receba mensagens para ou de outro dispositivo.
- Diferentemente do compartilhamento de arquivos permitido pelo FTP, os clientes estabelecem uma conexão de longo prazo com os servidores. 
- Depois que a conexão é estabelecida, o usuário do cliente pode acessar os recursos no servidor como se o recurso fosse local para o host do cliente.
- Os sistemas operacionais LINUX e UNIX também fornecem um método de compartilhamento de recursos com redes Microsoft usando uma versão do SMB chamada SAMBA. 
- Os sistemas operacionais Apple Macintosh também oferecem suporte ao compartilhamento de recursos usando o protocolo SMB.