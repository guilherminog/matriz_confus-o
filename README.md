# Interpretação da Matriz de Confusão e Métricas de Avaliação

A matriz de confusão é uma ferramenta fundamental para avaliar o desempenho de modelos de classificação. Ela nos permite visualizar a distribuição das previsões feitas pelo modelo em relação aos valores verdadeiros.

## Matriz de Confusão

Considere a seguinte matriz de confusão para um modelo de classificação binária (spam vs. não spam):

|               | Previsto: Spam | Previsto: Não Spam |
|---------------|----------------|---------------------|
| **Real: Spam**     |      100       |          20         |
| **Real: Não Spam** |       10       |         300         |

- **Verdadeiros Positivos (True Positives - TP):** 100. São os casos em que o modelo previu corretamente que o e-mail era spam e o e-mail era realmente spam.
- **Falsos Positivos (False Positives - FP):** 20. São os casos em que o modelo previu incorretamente que o e-mail era spam quando na verdade não era spam.
- **Verdadeiros Negativos (True Negatives - TN):** 300. São os casos em que o modelo previu corretamente que o e-mail não era spam e o e-mail era realmente não spam.
- **Falsos Negativos (False Negatives - FN):** 10. São os casos em que o modelo previu incorretamente que o e-mail não era spam quando na verdade era spam.

## Métricas de Avaliação

Com base na matriz de confusão, podemos calcular diversas métricas de avaliação:

### Precisão (Precision)
Precision = frac{TP}{TP + FP}
Precision = frac{100}{100 + 20} \approx 0.833

A precisão mede a proporção de exemplos positivos previstos corretamente pelo modelo em relação ao número total de exemplos previstos como positivos. Neste caso, aproximadamente 83.3% das previsões positivas do modelo são realmente positivas.

### Recall (ou Sensibilidade - Sensitivity)
Recall = frac{TP}{TP + FN}
Recall = frac{100}{100 + 10} \approx 0.909

O recall mede a proporção de exemplos positivos previstos corretamente pelo modelo em relação ao número total de exemplos positivos reais no conjunto de dados. Neste caso, aproximadamente 90.9% dos exemplos positivos foram corretamente identificados pelo modelo.

### F1-Score
F1-Score = 2 \times \frac{{Precision} \times \{Recall}}{{Precision} +{Recall}}
F1-Score = 2 \times \frac{0.833 \times 0.909}{0.833 + 0.909} \approx 0.869

O F1-Score é a média harmônica entre a precisão e o recall. Ele fornece uma única métrica que combina essas duas medidas. Neste caso, o F1-Score é aproximadamente 0.869*

#### *No exemplo cita neste README.
