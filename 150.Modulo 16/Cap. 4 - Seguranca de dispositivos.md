# *AutoSecure Cisco*

- Os dispositivos devem ter uma atenção especial para manter a segurança. As configurações de segurança padrão, quando um novo sistema operacional é instalado, são definidas. Na maioria dos caso, esse nível de segurança é inadequado. 
- Para roteadores Cisco, o recurso Cisco AutoSecure pode ser usado para ajudar a proteger o sistema. 
- Além disso, existem algumas etapas simples que podem ser executadas e que se aplicam à maioria dos sistemas:
	- Nomes de usuário e senhas padrão devem ser trocados imediatamente.
	- O acesso aos recursos do sistema deve ser restrito apenas aos indivíduos que estão autorizados a usá-los.
	- Todos os serviços e aplicações desnecessários devem ser desativados e desinstalados assim que possível.

# *Segurança de Senhas Adicional*

- Além de senhas fortes para a segurança, algumas etapas podem ser tomadas para ajudar a garantir que as senhas permaneçam secretas em um roteador e switch Cisco. Alguma dessas etapas:
	- Criptografando todas as senhas de texto sem formatação;
	- Definindo um tamanho mínimo aceitável de senha;
	- Detenção de ataques de adivinhação de senha de força bruta;
	- Desativando um acesso de modo EXEC privilegiado inativo após um período especificado.
- Para garantir um tamanho mínimo para as senhas o comando <mark style="background: #ABF7F7A6;">security passwords min-length length</mark> no modo de <mark style="background: #BBFABBA6;">configuração global</mark>. Exemplo: security passwords min-length 14. 
- Para mitigar ataques de brute force, o comando <mark style="background: #ABF7F7A6;">login block-for # attempts # within #</mark> no modo de <mark style="background: #BBFABBA6;">configuração global</mark> deve ser usado. Os '#' representam números naturais. 
- Exemplo: login block-for 120 attemtps 3 within 60, <mark style="background: #D2B3FFA6;">bloqueará por 120</mark> segundos as tentativas de login caso <mark style="background: #D2B3FFA6;">3 tentativas incorretas</mark> forem inseridas <mark style="background: #D2B3FFA6;">dentro de 60 segundos</mark>.
- Há como settar um timer para fazer logout de uma sessão EXEC privilegiada. Por padrão, esse timer é de 10 minutos, porém esse tempo é muito extenso. Para diminuir, basta utilizar o comando <mark style="background: #ABF7F7A6;">exec-timeout minutos segundos</mark> na <mark style="background: #BBFABBA6;">configuração das linhas de acesso</mark> (vty 0 4). 

# *Ativação do SSH*

- É recomendável ativar o SSH para acesso seguro remotamente. Para configurar um dispositivo Cisco para suportar SSH usam estas 6 etapas:

### **Etapa 1. Configurar um hostname exclusivo**

- Um dispositivo deve ter um nome de host exclusivo e diferente do padrão.

### **Etapa 2. Configurar o nome do domínio IP**

- Configure o domain name do IP da rede usando o comando na <mark style="background: #BBFABBA6;">configuração global</mark> <mark style="background: #ABF7F7A6;">ip domain name nome</mark>.

### **Etapa 3. Gerar chave para criptografar o tráfego SSH**

- O SSH criptografa o tráfego entre origem e destino. Para isso ocorrer, uma chave de autenticação exclusiva deve ser gerada usando o comando de <mark style="background: #BBFABBA6;">configuração global</mark> <mark style="background: #ABF7F7A6;">crypto key generate rsa general-keys modulus qtd_bits</mark>. 
- O módulo bits determina o tamanho da chave e pode ser configurado de 360 a 2048 bits. Quanto maior for a chave, mais segura ela é, porém para criptografar e decifrar o tempo também aumenta. O tamanho mínimo recomendado é 1024 bits.

### **Etapa 4. Verifique ou crie uma entrada de banco de dados local**

- Crie uma entrada de nome de usuário do banco de dados local usando o comando <mark style="background: #ABF7F7A6;">username</mark> na <mark style="background: #BBFABBA6;">configuração global</mark>.

### **Etapa 5. Autenticar no banco de dados local**

- Use o comando <mark style="background: #ABF7F7A6;">login local</mark> em <mark style="background: #BBFABBA6;">configuração de linha</mark> para autenticar a linha <mark style="background: #BBFABBA6;">vty</mark> no banco de dados local. 

### **Etapa 6. Habilite as sessões SSH de entrada vty**

- Por padrão, nenhuma sessão de entrada é permitida em <mark style="background: #BBFABBA6;">linhas vty</mark>. Para habilitar o ssh e o telnet, use o comando <mark style="background: #ABF7F7A6;">transport input ssh telnet</mark>. 

# *Desativar serviços não utilizados*

- Verifique quais portas estão abertas com o comando <mark style="background: #ABF7F7A6;">show ip ports all</mark> em <mark style="background: #BBFABBA6;">modo EXEC privilegiado</mark>. Versões do IOS anteriores ao IOS-XE usam o comando <mark style="background: #ABF7F7A6;">show control-plane host open-ports</mark>. 
- Para desativar serviços como http use <mark style="background: #ABF7F7A6;">no ip http server</mark> em <mark style="background: #BBFABBA6;">configuração global</mark>. Para desativar telnet, vá para <mark style="background: #BBFABBA6;">configuração de linha vty 0 4</mark> e simplesmente omita o parâmetro 'telnet' do comando <mark style="background: #ABF7F7A6;">transport input ssh</mark>. 