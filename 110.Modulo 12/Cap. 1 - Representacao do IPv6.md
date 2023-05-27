# *Formatos de IPv6*

- Os endereços IPv6 têm 128 bits e são escritos como uma sequência de valores hexadecimais. Cada 4 bits são representados por um único dígito hexadecimal, totalizando 32 valores hexadecimais, como mostra a Figura 1. Os endereços IPv6 não diferenciam maiúsculas e minúsculas e podem ser escritos tanto em minúsculas como em maiúsculas.
- ![[Hextets de 16 bits.png]]

# *Regras para reduzir a notação IPv6*

### **Omitir zeros à esquerda**

- A primeira regra para ajudar a reduzir a notação de endereços IPv6 é omitir os 0s (zeros) à esquerda de qualquer seção de 16 bits ou hexteto. Aqui estão quatro exemplos de maneiras de omitir zeros à esquerda:
- ![[zeros a esquerda.png]]

### **Dois pontos duplos**

- A segunda regra para redução da notação dos endereços IPv6 é o suo de dois pontos duplos '::'. Exemplo: 2001:db8:cafe:1:0:0:0:1 pode ser escrito como 2001:db8:1::1. 
- Se um endereço tiver mais de uma cadeia contígua de todos os hextets 0, a prática recomendada é usar dois pontos duplos (::) na cadeia mais longa. Se as strings forem iguais, a primeira string deve usar dois pontos duplos (::).
- <mark style="background: #FFB8EBA6;">Exemplo errôneo</mark>: 2001:db8::abcd::1234.
- Esse exemplo de notação errada para o IPv6 abre espaço para diversos IPv6 diferentes. Os possíveis endereços de formato compactado incorreto: 2001:db8:0000:abcd::1234 ; 2001:db8::abcd:0000:0000:1234 ; 2001:db8::abcd:0000:0000:0000:1234 ; 2001:db8:0000:0000:abcd::1234 ; 
- ![[zero a esquerda e segmentos 0.png]]