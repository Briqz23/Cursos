# Cost Function Equation

- A função de custo nos ajuda a determinar qual valor de **w** corresponde ao menor **C(w)**.  
- Utilizamos uma função ao quadrado para evitar valores negativos e penalizar mais fortemente os outliers.  

Imagine a função **C(w)** plotada em um gráfico. O objetivo é encontrar o valor de **w** que minimiza **C(w)**. Esse **w** será o melhor para o neurônio.

## Gradient Descent
Para resolver o problema de encontrar o menor **w**, utilizamos o método de **gradient descent**.  
- Quando a inclinação (slope) da função convergir para zero, teremos encontrado o menor **w**.  
- Cada passo na direção do gradiente é controlado por um parâmetro chamado **learning rate** (alpha).

### Adam Method
O **Adam method** é um algoritmo para otimizar o processo de gradient descent. Ele ajusta automaticamente o learning rate para evitar:  
- **Overshooting**: Quando o learning rate é alto demais.  
- **Convergência lenta**: Quando o learning rate é baixo demais.  

### Cost Functions
Para problemas de classificação, geralmente usamos a função de custo de **cross-entropy** ao invés da função de custo quadrática **C(w)**.  
- A função de cross-entropy presume que o modelo gera uma probabilidade (p) para determinar a classe.  

A fórmula da função de custo de **cross-entropy** para classificação é:

$$
H(p, q) = -\sum_{i} p_i \log(q_i)
$$

Onde:
- **p_i**: Valor real (ground truth) para a classe *i*.  
- **q_i**: Probabilidade prevista pelo modelo para a classe *i*.  
