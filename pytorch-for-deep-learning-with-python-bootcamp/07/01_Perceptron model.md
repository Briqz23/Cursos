# Perceptron Model

The perceptron works as follows:

**INPUT** → ([Axon] → [Nucleus] → [Dendrite]) → **OUTPUT**

---

### Example: Summation Function

- The model receives two inputs, \( x_1 \) and \( x_2 \), which pass through a function \( f(x) \), producing an output \( y \).  
  - Initial formula:  
    ```math
    y = x_1 + x_2
    ```

- To allow the function to learn and adjust, weights \( w_1 \) and \( w_2 \) are added to the inputs before they pass to \( f(x) \).  
  - Updated formula:  
    ```math
    y = w_1x_1 + w_2x_2
    ```  

- The perceptron adjusts the values of \( w \) as it learns.  

- To account for cases where \( x = 0 \) (ensuring the model still produces meaningful outputs), a **bias** term \( b \) is introduced:  
  - Final formula:  
    ```math
    y = (w_1x_1 + b) + (w_2x_2 + b)
    ```  

### General Perceptron Formula
```math
y = \sum_{i=1}^{n} w_ix_i + b
```
where:
- x: input
- w: weight
- b: bias