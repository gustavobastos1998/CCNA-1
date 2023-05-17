# *Limitações do IPv4*

### **Esgotamento do endereço IPv4**

- Há um número limitado de endereços IPv4 públicos exclusivos disponíveis. Por mais que esse número seja de aproximadamente 4 bilhões de endereços IPv4, o número crescente de novos dispositivos aumenta a necessidade de mais endreços.

### **Falta de conectividade ponto a ponto**

- Network Address Translation (NAT) é uma tecnologia comumente implementada em redes IPv4. A NAT é uma forma de vários dispositivos compartilharem um único endereço IPv4 público. 
- No entanto, como o endereço IPv4 público é compartilhado, o endereço IPv4 de um host de rede interna fica oculto. Isso pode ser problemático para tecnologias que exigem conectividade de ponta a ponta.

### **Maior complexidade de rede**

- O NAT ampliou a vida útil do IPv4. Porém, ele tem várias implementações complexas na rede, criando latência e dificultando a solução de problemas.

# *Visão geral do IPv6*

- As melhorias que o IPv6 fornece:
	- **Espaço de endereço aumentado** - os endereços IPv6 são baseados no endereçamento hierárquico de 128 bits, em oposição ao IPv4 com 32 bits.
	- **Manipulação aprimorada de pacotes** - O cabeçalho IPv6 foi simplificado com menos campos.
	- **Elimina a necessidade de NAT** - com um número tão grande de endereços IPv6 públicos, o NAT entre um endereço IPv4 privado e um IPv4 público não é necessário. Isso evita alguns dos problemas induzidos por NAT enfrentados por aplicativos que exigem conectividade de ponta a ponta.
- O espaço de 32 bits de um endereço IPv4 fornece aproximadamente 4.294.967.296 endereços exclusivos. O espaço de endereço IPv6 fornece 340.282.366.920.938.463.463.374.607.431.768.211.456, ou 340 undecilhões de endereços. Isto é aproximadamente equivalente a cada grão de areia na Terra. 1 undecilhão é 10^36.

# *Campos do cabeçalho IPv4 no cabeçalho IPv6*

- Alguns campos foram matidos, outros modificados e alterados suas posições e outros campos não são mais necessários. 
- O cabeçalho IPv4 pode variar de 20 bytes até 60 bytes caso o campo de opções seja usado. O cabeçalho IPv6 é simplificado, ele tem comprimento fixo de 40 bytes. 
- ![[cabecalho IPv6.png]]

# *Campos do cabeçalho IPv6*

- ![[info campos IPv6.png]]
- Um pacote IPv6 pode conter também cabeçalhos de extensão (EH), que fornecem informações de camada de rede. Opcionais, os cabeçalhos de extensão ficam posicionados entre o cabeçalho IPv6 e a carga. Eles são usados para fragmentação, segurança, suporte à mobilidade e muito mais.
- Ao contrário de IPv4, os roteadores não fragmentam os pacotes IPv6 roteados.

