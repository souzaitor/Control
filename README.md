# Resumo Disciplina

Data: 17/08/2021
Disciplina: Controle 1
Semana: Resumo

## Sumário

## Funções de Transferência de Elementos Dinâmicos

$a_2d^2\frac {\theta_0}{dt^2}+a_1\frac{d\theta_0}{dt}+a_0\theta_0=b_1\theta_i$

- A **função de transferência** $G(s)$ de um sistema linear que descreve o comportamento dinâmico é definia como a ração da transformada de Laplace da variável de saída $\theta_0(s)$ pela transformada de Laplace da variável de entrada $\theta_i(s)$:

$G(s)=\frac{\theta_0}{\theta_i}=\frac{b_1}{a_2s+a_1s+a_0}$

[Voltar ao Topo](https://www.notion.so/Resumo-Disciplina-f6daa7f509974998b4d0e7f46c2629f2)

## Elementos de Primeira e Segunda Ordens

- **Ordem do sistema**: A mais alta potência da derivada na equação diferencial ou a mais alta potência de s no denominador
- **Forma Geral Sistema de Primeira Ordem no domínio s**:

- **Forma Geral Sistema de Segunda Ordem no domínio s**:

$G(s)=\frac{\theta_o(s)}{\theta_i(s)}=\frac{b_0}{a_2s^2+a_1s+a_0}=\frac{(b_0/a_0)}{(a_2/a_0)s^2+(a_1/a_0)s+1}=\frac{b_0\omega_n^2}{s^2+2\zeta\omega_ns+\omega_n^2}$

## Sistemas de Primeira Ordem

$G(s)=\frac{\theta_o(s)}{\theta_i(s)}=\frac {b_0}{a_1s+a_0}=\frac{b_0/a_0}{(a_1/a_0)+1}=\frac{G}{\tau s+1}$

### Entrada Degrau para Sistema de Primeira Ordem

- **Reposta**: $\theta_o = G[1-e^{(-t/\tau)}]$

 

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled.png)

### Entrada Rampa para Sistema de Primeira Ordem

- **Reposta**: $\theta_o = G[t-\tau(1-e^{-t/\tau})]$

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%201.png)

### Entrada Impulso para um Sistema de Primeira Ordem

- **Resposta:** $\theta_o = G(1/\tau)e^{-t/\tau}$

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%202.png)

## Sistemas de Segunda Ordem

$G(s)=\frac{\theta_o(s)}{\theta_i(s)}=\frac{b_0}{a_2s^2+a_1s+a_0}=\frac{(b_0/a_0)}{(a_2/a_0)s^2+(a_1/a_0)s+1}=\frac{b_0\omega_n^2}{s^2+2\zeta\omega_ns+\omega_n^2}$

### Entrada Degrau para Sistema de Segunda Ordem

Característica da resposta de sistemas de 2ª ordem:

**Amortecimento** 

$ζ > 1$ 

$ζ = 1$

$0 < ζ < 1$ 

$ζ = 0$

**Classificação** 

Super amortecida 

Criticamente Amortecida 

Sub amortecida 

Não Amortecida

**Raízes**

2, Reais

1, Reais iguais

2, Complexas

2, Complexas Puras

 **Resposta**

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%203.png)

$\theta_o=b_0[1-\sin\omega_nt]$

 $\theta_o=b_0[1-\frac1{\sqrt{(1-\zeta^2)}}e^{-(\zeta\omega_n)t}\sin(\omega_n\sqrt{1-\zeta^2}\space t+\phi)]$,$\cos \phi = \zeta$

 $\theta_o=b_0[1-e^{(-\omega_n)t}-\omega_nte^{(-\omega_n)t}]$

 $\theta_0=1+[\mp\frac{b_0\zeta}{2\sqrt{(\zeta^2-1)}}-\frac{b_0}{2}]e^{(-\zeta\omega_n\pm\omega_n\sqrt{(\zeta^2-1)})t}$

## Medidas de Desempenho Para Sistemas de Segunda Ordem

- **Tempo de pico**  $\omega t_P$ = $\pi$  : Tempo gasto para a resposta ir de 0 ao primeiro valor de pico. Tempo para a resposta oscilatória completar um meio ciclo, $\pi$
- **Sobre Sinal**: Quantidade máxima na qual a reposta ultrapassa o valor em regime permanente. Amplitude do primeiro pico.
- **Sobre Sinal Percentual**   $\exp(\frac {-\zeta \pi} {\sqrt{(1-\zeta^2)}})\times100 \%$   : Porcentagem do valor em regime permanente
- **Primeiro Sobre Sinal**:  $\theta_{ss}\exp(\frac {-\zeta \pi} {\sqrt{(1-\zeta^2)}})$
- **Segundo Sobre Sinal**:  $\theta_{ss}\exp(\frac {-2\zeta \pi} {\sqrt{(1-\zeta^2)}})$
- **Razão de Decaimento:  $\exp |\frac{-\zeta\pi}{\sqrt{(1-\zeta^2)}}|$  :** Indica a velocidade de decaimento, razão entre a amplitude do segundo sobre sinal e amplitude do primeiro sobre sinal
- **Tempo de Estabilização** $t_s$  : Tempo gasto para que as oscilações desapareçam, resposta diminuir e ficar dentro de um percentual
- **Tempo de Estabilização $t_s$ 2% do valor final:  $t_s$ = $4 / \zeta\omega_n$**
- **Tempo de Estabilização $t_s$ 5% do valor final:  $t_s$ = $3 / \zeta\omega_n$**
- **Período**: $2\pi$ / $\omega_n$
- **Número de Oscilações** = tempo de estabilização / período : $2/\pi$ $\sqrt{(\frac{1}{\zeta^2}-1)}$

## Classificação dos Sistemas

- O sistema em malha fechada é considerado tendo realimentação unitária
- Os sistemas são classificados com base na função de transferência do ramo direto com realimentação unitária, a **função de transferência de malha aberta** de um sistema em malha fechada
- A **função de transferência de malha aberta** de um sistema com função de transferência do ramo direto $G(s)$ e de realimentação $H(s)$ é calculada por:

$G_o(s)=\frac{G(s)}{1+G(s)[H(s)-1]}$

- A função de transferência de malha aberta de sistemas tem a **forma geral**:

$\frac{K(s^m+a_{m-1}s^{m-1}+a_{m-2}s^{m-2}+...+a_1s+a_0)}{s^q(s^n+b_{n-1}s^{n-1}+b_{n-2}s^{n-2}+...+b_1s+b_0)}$

- $q$ é o valor chamado **tipo** ou **classe do sistema.** Identifica o número de fatores $1/s$ na , ou número de integradores função de transferência de malha aberta

## Erro em Regime Permanente

- **Erro**: A diferença entre o sinal de saída de saída, a referência, e o sinal de saída real que ocorre no sistema:

$E(s)=\theta_i(s)-\theta_o(s)$

![Untitled.png](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%204.png)

### Classificação dos Sistemas

- A **função de transferência de malha aberta** de um sistema com função de transferência do ramo direto $G(s)$ e de realimentação $H(s)$ é calculada por:

$G_o(s)=\frac{G(s)}{1+G(s)[H(s)-1]}$

- A função de transferência de malha aberta de sistemas tem a **forma geral**:

$\frac{K(s^m+a_{m-1}s^{m-1}+a_{m-2}s^{m-2}+...+a_1s+a_0)}{s^q(s^n+b_{n-1}s^{n-1}+b_{n-2}s^{n-2}+...+b_1s+b_0)}$

- $q$ é o valor chamado **tipo** ou **classe do sistema**
- Identifica o **número de integradores** ou termos independentes s no denominador ($1/s$) na **função de transferência de malha aberta**

### Erro em Regime Permanente para uma Entrada Degrau

- $K_P$ é chamado **constante de erro de posição**, sem unidades:

$K_P=\lim\limits_{s\to0}G_0(s)$

- O erro em regime permanente para um **sistema tipo 0** é:

$e_{ss}=\frac1{1+K_P}$

- Para sistemas de tipo maiores o **erro em regime permanente** é 0

### Erro em Regime Permanente para uma Entrada Rampa

- $K_V$ é chamado **constante de erro de erro de velocidade**, e tem unidade $s^{-1}$:

$K_V=\lim\limits_{s\to0}sG_0(s)$

- Para um entrada rampa com uma razão de variação com o tempo de uma constante $A$, o erro em regime permanente para o **sistema tipo 1** é:

 $e_{ss}=\frac A{K_V}$

- Para sistemas de tipo maiores o **erro em regime permanente** é 0
- Para sistemas de tipo 1 o **erro em regime permanente** é $\infin$

### Erro em Regime Permanente para uma Entrada Parabólica

- $K_A$ é chamado **constante de erro de erro de aceleração**, e tem unidade $s^{-2}$:

$K_A=\lim\limits_{s\to0}s^2G_0(s)$

- Se a entrada é parabólica da forma $\frac A{s^3}$, onde $A$ é uma constante, o erro em regime permanente para o **sistema tipo 2** é:

$e_{ss}=\frac A{K_A}$

- Para sistemas de tipo maiores o **erro em regime permanente** é 0
- Para sistemas de tipo menores o **erro em regime permanente** é $\infin$

### Erro em Regime Permanente para Entradas Diferentes

- Pelo principio da superposição, o erro em regime permanente é igual a soma dos erros de cada segmento do sinal de entrada

## Pólos e Zeros

- A função de transferência em malha fechada pode ser representada como:

$G(s)=\frac{K(s+z_1)(s+z_2)...(s+z_m)}{(s+p_1)(s+p_2)...(s+p_n)}$

- Os **zeros** são as raízes $-z_1$,$-z_2$,...,$-z_m$ do numerador e os valores de s para os quais a função de transferência é zero
- Os **pólos** são as raízes $-p_1$,$-p_2$,...,$-p_n$ do denominador e os valores de s para os quais a função de transferência é infinita

### Diagrama de Pólos e Zeros

- Forma de representar os pólos e zeros de uma função de transferência
- O eixo x é a parte real e o eixo y é a parte imaginária
- A posição de um **pólo** é marcada por um $X$
- A posição de um **zero** é marcada por um $O$
- O gráfico bidimensional é chamado plano $s$

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%205.png)

## Estabilidade

- Um sistema é **estável** se para entradas finitas (limitadas) ele produz saídas limitadas (limite, saídas que tendem a algum valor)
- Um sistema é **instável** se para entradas finitas (limitadas) ele **não** produz saídas limitadas

**Por Análise de Pólos:**

- **Estabilidade**: Todos os pólos devem ter parte real negativa
- **Criticamente Estável**: Um ou mais pólos tem parte real zero e nenhuma pode ser positiva
- **Instabilidade**: Um ou mais pólos tem parte real positiva

### Saídas para diferentes Pólos a uma Entrada Impulso

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%206.png)

### Saídas para diferentes Pólos a uma Entrada Degrau

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%207.png)

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%208.png)

## Controle Proporcional

- A saída do controlador é proporcional ao erro e a **constante de ganho proporcional, $K_P$.** Depende apenas da amplitude do erro no instante de tempo

$\text{Saída}=K_Pe$

- **Função de Transferência do Controlador**: $G_C(s)=K_P$
- O controlador é um amplificador com ganho constante
- Um ganho constante tende a existir somente para uma certa faixa de erros, chamada **banda proporcional**

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%209.png)

- **Sistema com Controle Proporcional**:

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%2010.png)

- **Função de Transferência**: $G_o(s)=K_PG_P(s)$
- Altera os pólos da função
- **Desvantagem**: O controlador não introduz o termo $1/s$ no ramo direto → Se o sistema é do tipo 0, continua sendo do tipo 0 → Continua com erro em regime permanente

## Controle Integral

- A saída do controlador é proporcional à integral do sinal do erro e a **constante de ganho integral, $K_I$.** Tem unidade $s^{-1}$

$\text{Saída}=K_I\int\limits_0^1e \space dt$

- **Função de Transferência do Controlador**: $G_C(s)=\frac{K_I}{s}$
- A integral é a área da curva do sinal do erro e aumenta de maneira regular a medida que o erro aumenta
- A saída é proporcional ao acúmulo de efeitos de erros em momentos anteriores

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%2011.png)

- **Sistema com Controle Integral**:

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%2012.png)

- **Função de Transferência**: $G_o(s)=(\frac{K_I}{s})G_P(s)$
- **Vantagem**: O controlador introduz o termo $1/s$ no ramo direto → Aumenta o tipo do sistema em 1 → Se o sistema é do tipo 0, o erro em regime permanente desaparece para uma entrada degrau
- **Desvantagem**: Introdução de um pólo na origem, a assíntotas da raízes apontam mais em direção ao semi plano direito to plano s, ou seja, a **estabilidade** relativa fica **reduzida**

## Controle Proporcional + Integral

- A redução na estabilidade relativa resultante do controle integral pode ser resolvida pela ação de controle proporcional mais integral

$\text{Saída}=K_Pe+K_I\int\limits_0^tedt$

- **Função de Transferência do Controlador**: $G_C(s)=\frac{K_P[s+(K_I/K_P)]}{s}$
- $\tau_I=K_P/K_I$ é a **constante de tempo integral**
- A saída do controlador quando existe um erro em degrau

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%2013.png)

**Sistema com Controle Integral + Proporcional:**

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%2014.png)

- **Função de Transferência**: $G_o(s)=(\frac{K_P[s+(1/\tau_I)]}{s})G_P(s)$
- **Vantagem**: O fator $1/s$ aumenta o tipo do sistema para 1 e  remove a possibilidade de um erro em regime permanente para uma entrada degrau
- **Desvantagem**: Redução da estabilidade relativa, mas não é tão grande no caso do controle integral sozinho

## Controle Derivativo

- A saída do controlador é proporcional à taxa de variação do sinal do erro e a **constante de ganho derivativo, $K_D$.** Tem unidade $s$

$\text{Saída}=K_I\int\limits_0^1e \space dt$

- **Função de Transferência do Controlador**: $G_C(s)=K_Ds$
- O controle derivativo é insensível a sinais de erro constantes ou de variação lenta, é usado em combinação com outras formas de controle
- A saída é proporcional à taxa de variação do erro

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%2015.png)

- **Sistema com Controle Derivativo**:

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%2016.png)

- **Função de Transferência**: $G_o(s)=\frac{K_DG_P(s)}{1+K_DsG_P(s)}$
- **Vantagem**: Usado com outras formas de controle, aumenta a velocidade de correção da resposta de um sistema ao erro
- **Desvantagem**: Cancela um termo $1/s$ e reduz a ordem do sistema em 1

- Na prática, um controle derivativo é obtido usando um **compensador em avanço**. O controlador tem função de transferência: $K(s+z)/(s+p), \text{com } p>z$

## Controle Proporcional + Derivativo

- **Função de Transferência**: $G_O(s)=(K_P+K_Ds)G_P(s)=K_D[(1/\tau_D)+s]G_P(s)$
- $\tau_D=K_P/K_D$ é a **constante de tempo derivativo**
- Um zero é introduzido em $s=-1\tau_D$
- Sem mudanças no tipo do sistemas e no erro permanente
- **Sistema com Controle Proporcional + Derivativo:**

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%2017.png)

[Voltar ao Topo](https://www.notion.so/Resumo-Disciplina-f6daa7f509974998b4d0e7f46c2629f2)

## Parâmetros

![Untitled](Resumo%20Disciplina%20959244f5ac23436daea3904d5ff61812/Untitled%2018.png)