# *Endereços IP*

- Se você quiser que seus dispositivos finais se comuniquem entre si, você deve garantir que cada um deles tenha um endereço IP apropriado e esteja conectado corretamente. 
- O IP permite que os dispositivos se localizem e estabelçame comunicação ponto a ponto na Internet. 
- A estrutura de um endereço IPv4 é chamada notação decimal com ponto e é representada por quatro números decimais entre 0 e 255. Os endereços IPv4 são atribuídos individualmente a dispositivos conectados a uma rede.
- O IPv6 é uma versão mais recente do IP e está substituindo o IPv4 mains comum.
- Uma máscara de sub-rede IPv4 também é necessária. Uma máscara de sub-rede (_subnet mask_, em inglês) é um número de 32 bits utilizado para separar os endereços IP em partes de rede e host. Ao definir quantos bits do endereço IP representam a parte da rede e quantos bits representam a parte do host, ela ajuda no gerenciamento e desempenho do tráfego. A máscara ajuda a segmentar redes grandes em redes menores, favorecendo fluxo e tráfego mais dinâmico. 
- O exemplo na figura exibe o endereço IPv4 (192.168.1.10), máscara de sub-rede (255.255.255.0) e gateway padrão (192.168.1.1) atribuído a um host. O endereço de gateway padrão é o endereço IP do roteador que o host usará para acessar redes remotas, incluindo a Internet.
  ![[IPv4.png]]
- Os endereços IPv6 têm 128 bits e são escritos como uma sequência de valores hexadecimais. A cada quatro bits é representado por um único dígito hexadecimal; para um total de 32 valores hexadecimais. Grupos de quatro dígitos hexadecimais são separados por dois pontos (:). Os endereços IPv6 não diferenciam maiúsculas e minúsculas e podem ser escritos tanto em minúsculas como em maiúsculas.

# *Interfaces e portas*

- As comunicações em rede dependem de interfaces do dispositivo de usuário final, interfaces do dispositivo de rede e cabos que as conectam. Cada interface física tem especificações ou padrões que a definem. Um cabo conectado à interface deve ser projetado de acordo com os padrões físicos da interface. 
- Diferentes tipos de meio físico de rede oferecem características e benefícios diferentes. Nem todas as mídias de rede têm as mesmas características. Nem todas as mídias são apropriadas para o mesmo propósito. Estas são algumas das diferenças entre os vários tipos de mídia:
	-   A distância pela qual o meio físico consegue carregar um sinal com êxito;
	-   O ambiente no qual o meio físico deve ser instalado;
	-   A quantidade e a velocidade de dados nas quais eles devem ser transmitidos;
	-   O custo do meio físico e da instalação.
- Os switches Cisco IOS de Camada 2 têm portas físicas para se conectarem a dispositivos. Essas portas não são compatíveis com endereços IP da Camada 3. Portanto, os switches têm uma ou mais interfaces virtuais de switch (SVIs). Essas interfaces virtuais existem porque não há hardware físico no dispositivo associado. Uma SVI é criada no software.
- A interface virtual permite gerenciar remotamente um switch em uma rede usando IPv4 e IPv6. Todo switch tem uma SVI na configuração padrão pronta para uso. A SVI padrão é a interface VLAN1. 

