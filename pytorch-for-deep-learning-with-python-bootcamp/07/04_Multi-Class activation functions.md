# Multi-Class Activation Functions

## Duas principais:

- **Non-exclusive classes**: Existem várias classes/categorias atribuídas a um único ponto de dado.  
  Exemplo: Uma foto pode ser marcada como "família", "praia" e "férias" ao mesmo tempo. Neste caso, uma boa escolha é a **função sigmoide**, pois cada neurônio irá produzir um valor entre 0 e 1 para cada classe.

- **Mutually exclusive classes**: Apenas uma classe é atribuída a um único ponto de dado.  
  Exemplo: Classificar uma cor em um espaço de cor como grayscale. Você pode usar **one-hot encoding**. Para cada ponto de dado, você pode ter uma cor representada entre as classes (por exemplo, vermelho, verde e azul).

![One-hot Encoding Example](https://miro.medium.com/v2/resize:fit:1400/1*yNxUR1Ofc0it2vu7wSUHiA.png)

### Softmax Function
Com a função **softmax**, onde \( k \) é o número de categorias, ela calcula a probabilidade de cada categoria, sendo que a soma das probabilidades de todas as categorias é igual a 1.

A fórmula da **softmax** é dada por:

$$
\text{Softmax}(z_i) = \frac{e^{z_i}}{\sum_{k=1}^{K} e^{z_k}}
$$

Onde:
- \( z_i \) é o valor da entrada para a classe \( i \),
- \( K \) é o número total de classes.

Exemplo:  
Se tivermos três categorias, como **Red**, **Green**, e **Blue**, a saída pode ser:

$$
\text{Softmax}([0.1, 0.6, 0.3]) = [0.2, 0.6, 0.2]
$$
