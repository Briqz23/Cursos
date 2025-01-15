# Backpropagation

O algoritmo de **backpropagation** é usado para ajustar os pesos em redes neurais, propagando o erro da saída de volta para as camadas anteriores. Ele fornece um método sistemático para calcular o gradiente da função de custo em relação aos pesos e vieses da rede.

---

## Passo a Passo do Algoritmo:

1. **Entrada (\(x\))**:  
   Defina a ativação correspondente \(a^{(1)}\) para a camada de entrada.  

2. **Feedforward**:  
   Para cada camada \(l = 2, 3, \dots, L\):  
   - Calcule:
     $$
     z^{(l)} = w^{(l)} a^{(l-1)} + b^{(l)}
     $$
   - Aplique a função de ativação:
     $$
     a^{(l)} = \sigma(z^{(l)})
     $$

3. **Erro na camada de saída (\(\delta^{(L)}\))**:  
   Calcule o vetor de erro na última camada:  
   $$
   \delta^{(L)} = \nabla_a C \odot \sigma'(z^{(L)})
   $$

4. **Retropropagar o erro**:  
   Para cada camada \(l = L-1, L-2, \dots, 2\):  
   - Calcule:
     $$
     \delta^{(l)} = \left( (w^{(l+1)})^T \delta^{(l+1)} \right) \odot \sigma'(z^{(l)})
     $$

5. **Saída (Gradiente da Função de Custo)**:  
   O gradiente da função de custo é dado por:  
   - Para os pesos:
     $$
     \frac{\partial C}{\partial w^{(l)}_{jk}} = a^{(l-1)}_k \delta^{(l)}_j
     $$
   - Para os vieses:
     $$
     \frac{\partial C}{\partial b^{(l)}_j} = \delta^{(l)}_j
     $$

---

## Por que o nome "Backpropagation"?

O nome vem do fato de que os vetores de erro \(\delta^{(l)}\) são calculados **para trás**, começando pela camada final (\(L\)) até a camada inicial.  
Isso ocorre porque a função de custo depende das saídas da rede. Para entender como a função de custo varia em relação aos pesos e vieses das camadas anteriores, é necessário aplicar a **regra da cadeia** de forma retrógrada através das camadas.

---

## Notas:
- **\(\sigma(z)\)**: Função de ativação (ex.: Sigmoid, ReLU, etc.).  
- **\(\odot\)**: Produto elemento a elemento (Hadamard product).  
- **\(\nabla_a C\)**: Gradiente da função de custo em relação às ativações.  

---

Essa é a base do treinamento das redes neurais modernas, permitindo que os pesos e vieses sejam ajustados para minimizar o erro de previsão.
