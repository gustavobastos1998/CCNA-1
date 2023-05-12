# *Endereços hexadecimais e IPv6*

- O sistema de numeração hexadecimal é usado em rede para representar endereços IP versão 6 e endereços MAC Ethernet.
- Os endereços IPv6 têm 128 bits de comprimento e a cada 4 bits é representado por um único dígito hexadecimal; para um total de 32 valores hexadecimais. Os endereços IPv6 não é case sensitive e podem ser escritos tanto em minúsculas como em maiúsculas.
- O formato preferido para escrever um endereço IPv6 é x:x:x:x:x:x:x:x, com cada "x" consistindo em quatro dígitos hexadecimais ou um segmento de 16 bits.
- Hexteto é um termo não oficial que se refere a cada 'x' unicamente. 
- ![[IPv6 representacao.png]]

# *Conversões decimal para hexadecimal e vice-versa*

- É muito mais prático converter usando o sistema de numeração binário como ponte. 
- Isso significa que caso queira converter de hexadecimal para decimal, primeiro converta para binário e depois para decimal ou o contrário. 
- É mais fácil porque cada dígito hexadecimal pode ser representado por quatro dígitos binários. 
- ![[deci-hexa-bina.png]]

### **Decimal para hexadecimal**

- Converta o número decimal para strings binárias de 8 bits.
- Divida as cadeias binárias em grupos de 4 a partir da posição mais a direita.
- Converta cada quatro números binários em seu dígito hexadecimal equivalente.

### **Hexadecimal para decimal**

- Converta o número hexadecimal em cadeias binárias de 4 bits, ou seja, converta cada dígito hexadecimal a seu equivalente em quatro bits.
- Criar agrupamento binário de 8 bits a partir da posição mais a direita.
- Converta cada agrupamento binário de 8 bits em seu dígito decimal equivalente.