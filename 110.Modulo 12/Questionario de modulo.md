1. Qual é o formato válido mais compactado possível do endereço IPv6 2001:0DB8:0000:AB00:0000:0000:0000:1234?
	- Existem duas regras que definem como um endereço IPv6 pode ser compactado. A primeira regra estabelece que os zeros iniciais de um hexteto podem ser eliminados. A segunda regra define que um único :: pode ser usado para representar um ou mais hextetos contíguos todos em zero. Só pode haver um :: em um endereço IPv6.
    
    (x)2001:DB8:0:AB00::1234
    
    2001:DB8::AB00::1234
    
    2001:DB8:0:AB:0:1234
    
    2001:DB8:0:AB::1234
    
2. Qual é o prefixo associado ao endereço IPv6 2001: DB8: D15: EA: CC44 :: 1/64?
    
	- O /64 representa os campos IPv6 de rede e sub-rede. O quarto campo de dígitos hexadecimais é chamado de ID da sub-rede. O ID de sub-rede para este endereço é 2001:DB8:D15:EA::0/64.​​
    
    2001::/64
    
    2001:DB8:D15:EA:CC44::/64​
    
    2001:DB8::/64​
    
    (x)2001:DB8:D15:EA::/64​
    
3. Que tipo de endereço é atribuído automaticamente a uma interface quando o IPv6 está habilitado nessa interface?
    
    - Quando o IPv6 está habilitado em qualquer interface, essa interface gerará automaticamente um endereço de link local IPv6.
    
    unicast global
    
    unique local
    
    loopback
    
    (x)link local
    
4. Qual prefixo de rede IPv6 é destinado apenas a links locais e não pode ser roteado?
    
    - FE80: :/10 é um prefixo link-local. Dispositivos com apenas endereços locais de link podem se comunicar com outros dispositivos na mesma rede, mas não com dispositivos em qualquer outra rede.
    
    FC00::/7
    
    FF00::/12
    
    (x)FE80::/10
    
    2001::/3
    
5. Qual é o propósito do comando **ping ::1**?
    
    - O endereço IPv6 :: 1 é o endereço de loopback. Usando o comando **ping ::1**ping ::1**ping ::1**, testa a pilha IP interna para verificar se ela está configurada e funcionando corretamente. Ele não testa a acessibilidade a qualquer dispositivo externo nem confirma se os endereços IPv6 estão configurados corretamente no host.
    
    Testar a acessibilidade do gateway padrão da rede.
    
    Testar a conectividade de multicast de todos os hosts da sub-rede.
    
    (x)Testar a configuração interna de um host IPv6.
    
    Testar o recurso de broadcast de todos os hosts da sub-rede.
    
6. Qual é a ID da interface do endereço IPv6 2001:DB8::1000:A9CD:47FF:FE57:FE94/64?
    
    - O ID da interface de um endereço IPv6 é o 64 bits mais à direita, ou os últimos quatro hextets, do endereço se nenhum bit de ID da interface tiver sido usado para sub-redes.
    
    1000:A9CD:47FF:FE57:FE94
    
    FE94
    
    FE57:FE94
    
    (x)A9CD:47FF:FE57:FE94
    
    47FF:FE57:FE94
    
7. Qual é o endereço de rede para o endereço IPv6 2001: DB8: AA04: B5 :: 1/64?
    
    - O elemento /64 representa os campos IPv6 de rede e sub-rede que são os quatro primeiros grupos de dígitos hexadecimais. O primeiro endereço nesse intervalo é o endereço de sub-rede 2001:DB8:AA04:B5::/64.​
    
    (x)2001:DB8:AA04:B5::/64​
    
    2001:DB8::/64​
    
    2001::/64
    
    2001:DB8:AA04::/64​
    
8. Qual tipo de endereço não é suportado no IPv6?
    
    - IPv6 suporta endereços unicast, privados e multicast, mas não suporta transmissões de Camada 3.
    
    privado
    
    (x)transmissão
    
    multicast
    
    unicast
    
9. O que é indicado por um ping bem-sucedido para o endereço IPv6: :1?
    
    - O endereço IPv6 :: 1 é o endereço de loopback. Um ping bem-sucedido para esse endereço significa que a pilha TCP/IP está instalada corretamente. Isso não significa que quaisquer endereços estão configurados corretamente.
    
    O host é cabeado corretamente.
    
    O endereço de gateway padrão está configurado corretamente.
    
    (x)O IP está instalado corretamente no host.
    
    Todos os hosts no link local estão disponíveis.
    
    O endereço de link local está configurado corretamente.
    
10. Qual é a representação mais comprimida do endereço IPv6 2001:0db8:0000:abcd:0000:0000:0000:0001?
    
    - O endereço IPv6 2001:0db8:0000:abcd:0000:0000:0000:0001 em seu formato mais compactado seria 2001:db8:0:abcd::1. O um zero à esquerda no segundo hexteto pode ser removido. O primeiro hexteto de zeros ser comprimidos em um único zero. Os três hextets consecutivos de zeros podem ser comprimidos para dois pontos::. Os três zeros à esquerda no último hextet podem ser removidos. Os dois pontos duplos :: só podem ser usados uma vez em um endereço.
    
    2001:0db8:0000:abcd::1
    
    2001:0db8:abcd::0001
    
    2001:0db8:abcd::1
    
    (x)2001:db8:0:abcd::1
    
    2001:db8::abcd:0:1
    
11. Qual é a configuração mínima para uma interface de roteador que esteja participando do roteamento IPv6?
    
    - Frequentemente, com o IPv6, uma interface do roteador apresenta mais de um endereço IPv6. O roteador terá ao menos um endereço de link local que pode ser gerado de forma automática, mas, normalmente, também terá um endereço unicast global configurado.
    
    deve ter um endereço automaticamente gerado de loopback
    
    (x)deve ter um endereço de link-local
    
    deve ter um endereço IPv6 unicast de link local e global
    
    deve ter um endereço IPv4 e outro endereço IPv6
    
12. No mínimo, qual é o endereço exigido para interfaces habilitadas para IPv6?
    
    - Todas as interfaces habilitadas para IPv6 devem ter no mínimo um endereço local de link. Outros endereços IPv6 podem ser atribuídos à interface, conforme necessário.
    
    (x)link local
    
    unique local
    
    unicast global
    
    site local
    
13. Quais são as três partes de um endereço unicast global IPv6? (Escolha três.)
    
    - Existem três elementos que compõem um endereço unicast global IPv6. Um prefixo de roteamento global fornecido por um ISP, um ID de sub rede que é determinado pela organização e um ID de interface que identifica exclusivamente a interface de interface de um host.
    
    (x)um prefixo de roteamento global que é usado para identificar a parte da rede do endereço que foi fornecido por um ISP
    
    um prefixo de roteamento global que é usado para identificar a parte do endereço de rede fornecido por um administrador local
    
    (x)um ID de sub rede que é usado para identificar redes dentro do site corporativo local
    
    um ID de interface que é usado para identificar a rede local de um host específico
    
    (x)um ID de interface que é usado para identificar o host local na rede
    
14. Sua organização é emitido o prefixo IPv6 de 2001:db8:130f::/48 pelo provedor de serviços. Com esse prefixo, quantos bits estão disponíveis para uso na sua organização, para criar sub redes na barra /64, se os bits do ID da interface não forem emprestados?
    
    - O prefixo de roteamento global atribuído à organização tem 48 bits. Os próximos 16 bits são usados para o ID da sub rede. Isso compõe os primeiros 64 bits do endereço, que normalmente é a parte da rede do endereço. Os 64 bits restantes do endereço IPv6 de 128 bits são para a parte do ID de interface (ou host) do endereço.
    
    8
    
    (x)16
    
    80
    
    128
    
15. Que tipo de endereço IPv6 não é roteável e usado apenas para comunicação em uma única sub rede?
    
    - Endereços Link-local têm relevância apenas no link local. Em outras palavras, os roteadores não encaminham pacotes com um endereço de link local origem ou destino.
    
    Endereço unicast global
    
    endereço não especificado
    
    Endereço local exclusivo
    
    endereço de loopback
    
    (x)endereço de link-local