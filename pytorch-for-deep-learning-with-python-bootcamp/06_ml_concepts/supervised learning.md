# Supervised Learning
Supervised learning trabalha com dados **rotulados**. Exemplos de aplicação:  
- **Exemplo 1**: Catalogar e-mails como spam ou não-spam.  
- **Exemplo 2**: Classificar reviews como positivas ou negativas.  

## Passo-a-passo
1. **Data acquisition**: Coleta de dados.  
2. **Data cleaning**: Limpeza dos dados, incluindo a divisão em conjuntos de treinamento, validação e teste.  
   - **Test data**: Mantido separado para avaliar o modelo ao final.  
3. **Model training & building**: Treinamento e construção do modelo.  
4. **Model testing**: Testar o modelo. Caso o desempenho não seja satisfatório, voltar ao passo 3.  
5. **Deploy**: Implantar o modelo em produção.  

---

## Underfitting x Overfitting x Bom Fitting

**Modelo de aprendizado supervisionado:** Recebe \( X \) (entradas) e prevê \( Y \) (saídas).  

- **Overfitting**:  
  - O modelo se ajusta muito bem ao conjunto de treinamento, capturando até os ruídos.  
  - **Problema**: Baixo erro no conjunto de treinamento, mas alto erro em novos conjuntos de dados.  
  - **Exemplo visual**: Curvas muito complexas em um gráfico, passando por todos os pontos de treinamento.  

- **Underfitting**:  
  - O modelo é muito simples para capturar os padrões nos dados.  
  - **Problema**: Alta bias e baixa variância.  
  - **Exemplo visual**: Uma reta simples que não reflete bem a distribuição dos dados.  

- **Bom fitting**:  
  - No treinamento, o erro começa alto, diminui gradualmente e estabiliza.  
  - Em redes neurais, isso acontece ao longo de múltiplas **épocas** (epochs).  

---

## Model Evaluation (Classification)
Métricas para avaliar classificadores:

- **Accuracy**: Proporção de previsões corretas.  
  - **Quando usar**: Para classes balanceadas (ex.: 50 gatos e 50 cachorros).  

- **Recall** (\( \text{TPR} \)):  
  - Fórmula: 
    \[
    \text{Recall} = \frac{\text{TP}}{\text{TP} + \text{FN}}
    \]  
  - Mede a capacidade do modelo de identificar todos os casos relevantes no conjunto de dados.  

- **Precision**:  
  - Fórmula: 
    \[
    \text{Precision} = \frac{\text{TP}}{\text{TP} + \text{FP}}
    \]  
  - Mede a habilidade do modelo de identificar apenas os dados relevantes.  

- **F1 Score**:  
  - Combina **Precision** e **Recall**.  
  - Fórmula: 
    \[
    \text{F1} = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}}
    \]  
  - É a média harmônica entre Precision e Recall.

### Confusion Matrix
Matriz que organiza os resultados da classificação:  
- **Condição positiva**:  
  - True Positive (TP): Correto, previsto como positivo.  
  - False Negative (FN): Errado, previsto como negativo.  
- **Condição negativa**:  
  - False Positive (FP): Errado, previsto como positivo.  
  - True Negative (TN): Correto, previsto como negativo.  

---

## Model Evaluation (Regression)
Avaliação para valores contínuos (não categóricos):  

- **Mean Absolute Error (MAE)**: Média dos valores absolutos dos erros.  
  - **Prós**: Menos sensível a outliers.  
  - **Contras**: Pode não penalizar adequadamente grandes erros.  

- **Mean Squared Error (MSE)**: Média dos erros elevados ao quadrado.  
  - **Prós**: Penaliza fortemente outliers.  
  - **Contras**: Difícil de interpretar devido à escala quadrática.  

- **Root Mean Squared Error (RMSE)**: Raiz quadrada do MSE.  
  - Mais interpretável que o MSE, já que retorna na mesma unidade dos dados originais.  

---

# Unsupervised Learning
Modelos usados quando os dados **não possuem rótulos**.  

### Exemplos:
- **Clustering**:  
  - Agrupa dados semelhantes.  
  - Exemplo: Em vez