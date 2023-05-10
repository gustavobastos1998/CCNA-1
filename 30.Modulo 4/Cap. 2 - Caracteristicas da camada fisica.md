# *Padrões da camada física*

- A camada física consiste em circuitos eletrônicos, meios físicos e conectores desenvolvidos pelos engenheiros. Portanto, é aconselhável que os padrões que regem esse hardware sejam definidos pelas organizações de engenharia de comunicações e elétrica relevantes.
- Os padrões de hardware, mídia, codificação e sinalização da camada física são definidos e governados por essas organizações de padrões:
	- International Organization for Standardization (ISO);
	- Telecommunications Industry Association/Electronic Industries Association (TIA/EIA);
	- União Internacional de Telecomunicações (ITU);
	- Instituto Nacional de Padronização Americano (ANSI);
	- Institute of Electrical and Electronics Engineers (IEEE);
	- Autoridades reguladoras de telecomunicações nacionais, incluem Federal Communication Commission (FCC) nos EUA e European Telecommunications Standards Institute (ETSI);

# *Componentes físicos*

- Os padrões da camada física abordam 3 áreas funcionais: <mark style="background: #FFB8EBA6;">componentes físicos</mark>; <mark style="background: #FFB8EBA6;">codificação</mark>; <mark style="background: #FFB8EBA6;">sinalização</mark>.
- Os componentes físicos são os dispositivos de hardware eletrônico, mídia e outros conectores que transmitem os sinais que representam os bits. Os componentes de hardware, como NICs, interfaces e conectores, materiais de cabo e projetos de cabo são especificados nos padrões associados à camada física.

# *Codificação*

- A codificação ou codificação de linha é um método para converter um fluxo de bits de dados em um "código” predefinido.
- Os códigos são agrupamentos de bits usados para fornecer um padrão previsível que pode ser reconhecido tanto pelo emissor quanto pelo receptor.
- Semelhante ao código Morse.

### **Codificação Manchester**

- Representa um bit 0 por uma transição de alta para baixa voltagem e um bit 1 o contrário. A transição ocorre no meio de cada período de bit. 
- ![[codificacao manchester.png]]

# *Sinalização*

- A camada física deve gerar os sinais elétricos, ópticos ou sem fio que representam os valores “1” e “0” no meio físico. A maneira como os bits são representados é chamada de método de sinalização.
- Os padrões de camada física devem definir que tipo de sinal representa o valor “1” e que tipo de sinal representa o valor “0”. Isso pode ser tão simples quanto uma alteração no nível de um sinal elétrico ou de um pulso óptico. 
- Por exemplo, um pulso longo pode representar um 1, enquanto um pulso curto pode representar um 0.

### **Sinalização para cabo de cobre**

- ![[sinalizacao cabo cobre.png]]

### **Sinalização para cabo de fibra óptica**

- ![[sinalizacao cabo optico.png]]

### **Sinalização para mídia sem fio**

- ![[sinalizacao sem fio.png]]

# *Largura de banda*

- É a capacidade na qual um meio pode transportar dados. A largura de banda digital mede a quantidade de dados que podem fluir de um lugar a outro durante um determinado tempo. Normalmente medida em kbps, Mbps ou Gbps. 
- Uma combinação de fatores determina a largura de banda prática de uma rede:
	- As propriedades do meio físico.
	- As tecnologias escolhidas para sinalização e detecção de sinais de rede.

# *Terminologia de largura de banda*

### **Latência**

- O termo latência se refere ao tempo necessário para os dados viajarem de um ponto a outro, incluindo atrasos.
- Em uma internetwork ou em uma rede com vários segmentos, a taxa de transferência não pode ser mais rápida que o link mais lento no caminho da origem ao destino. Mesmo que todos ou a maioria dos segmentos tenham alta largura de banda, será necessário apenas um segmento no caminho com baixa taxa de transferência para criar um gargalo na taxa de transferência de toda a rede.

### **Taxa de transferência**

- Taxa de transferência é a medida da transferência de bits através da mídia durante um determinado período.
- Devido a alguns fatores, geralmente a taxa de transferência não corresponde à largura de banda especificada nas implementações da camada física. A taxa de transferência geralmente é menor que a largura de banda. Existem muitos fatores que influenciam a taxa de transferência:
	- A quantidade de tráfego;
	- O tipo de tráfego;
	- A latência criada pelo número de dispositivos de rede encontrados entre a origem e o destino.

### **Dados úteis**

- Goodput é a medida de dados usáveis transferidos em um determinado período.
- Goodput é a taxa de transferência menos a sobrecarga de tráfego para estabelecer sessões, reconhecimentos, encapsulamento e bits retransmitidos. 
- O goodput é sempre menor que a taxa de transferência, que geralmente é menor do que a largura de banda.