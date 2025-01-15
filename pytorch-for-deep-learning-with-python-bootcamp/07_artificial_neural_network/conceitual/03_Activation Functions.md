# Activation Functions
- \( b \) → offset  
- \( w \) → dá a importância necessária para a entrada  

Por exemplo, se \( x \cdot w < 10 \) e \( b = 10 \), então o \( b \) ajusta o valor dentro desse threshold de modo que o \( w \) não tenha muita importância.  

Em \( z = w \cdot x + b \), podemos aplicar uma função que limita o valor de \( z \), como uma função sigmoide, para um problema de classificação. Isso faz com que o valor de \( z \) fique entre 0 e 1, resultando em uma curva suave, sem um degrau abrupto em \( x = 1 \). A fórmula da função sigmoide é:

$$
\sigma(z) = \frac{1}{1 + e^{-z}}
$$

Outra opção é a **ReLU** (Rectified Linear Unit). Para ReLU:

- Se \( z \leq 0 \), então \( z = 0 \).  
- Se \( z > 0 \), então \( z = z \).

A função ReLU é particularmente boa para resolver o problema do **vanishing gradient**, sendo frequentemente considerada a melhor escolha para redes neurais.

Para mais detalhes, veja a [página da Wikipédia sobre Funções de Ativação](https://en.wikipedia.org/wiki/Activation_function).
