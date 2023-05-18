# *Cabeçalho IPv4*

- O cabeçalho do pacote IPv4 é usado para garantir que esse pacote seja entregue para sua próxima parada no caminho para seu dispositivo final de destino.

# *Campos do cabeçalho de pacote IPv4*

- ![[campos IPv4.png]]
- ![[info campos IPv4.png]]
- Os campos Tamanho do Cabeçalho de Internet (IHL), Tamanho Total e Soma de Verificação do Cabeçalho servem para identificar e validar o pacote.
- O pacote IPv4 usa especificamente os campos Identificação, Flags e Deslocamento do Fragmento para organizar os fragmentos.

# *OBSERVAÇÃO*

- Os IPs no range 192.168.0.0 - 192.168.255.255 são IPs reservados pela IANA (Internet Assigned Numbers Authority). Esses IPs são usados em milhões de redes operadas de forma independente e são configurados automaticamente em centenas de milhões de dispositivos. Eles se destinam apenas ao uso privado, e o tráfego que precisa atravessar a Internet precisará usar um endereço diferente e exclusivo.