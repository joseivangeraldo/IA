# 📊 Relatório de Análise: Correlação de Pearson
> **Status:** Em estudo | **Data:** 10 de Maio de 2026 | **Tópico:** Machine Learning

---

## 📝 Descrição do Estudo
Este documento apresenta os cálculos de correlação entre as variáveis **Idade** e **Custo**, fundamentais para a construção de modelos de Regressão Linear.

### 1. Coleta de Dados
Abaixo estão os dados brutos extraídos da análise:

| Idade (X) | Custo (Y) |
| :--- | :--- |
| 18 | 871 |
| 23 | 1100 |
| 25 | 1393 |
| 33 | 1654 |
| 34 | 1915 |
| 43 | 2100 |
| 48 | 2356 |
| 51 | 2698 |
| 58 | 2959 |
| 63 | 3000 |
| 67 | 3100 |

---

## 📐 Fundamentação Matemática
A correlação de Pearson ($r$) mede o grau da relação linear entre duas variáveis quantitativas.

### Fórmula Aplicada
$$r = \frac{cov(X, Y)}{\sqrt{var(X) \cdot var(Y)}}$$

**Desenvolvimento do Cálculo:**
1. **Covariância:** $11869,71$
2. **Raiz do Produto das Variâncias:** $\approx 12015,04$

> ### 💡 Resultado Final
> **$r = 0,9879$**
> 
> *Interpretação:* Existe uma **correlação positiva muito forte** (próxima a 1), indicando que o custo aumenta proporcionalmente à idade.

---

## 💻 Implementação em Python
Para automatizar este cálculo, utilizamos a biblioteca `pandas`:

```python
import pandas as pd

# Criando o dataset
data = {'Idade': [18, 23, 25, 33, 34, 43, 48, 51, 58, 63, 67],
        'Custo': [871, 1100, 1393, 1654, 1915, 2100, 2356, 2698, 2959, 3000, 3100]}

df = pd.DataFrame(data)

# Calculando a correlação
correlacao = df['Idade'].corr(df['Custo'])
print(f"O coeficiente de Pearson é: {correlacao:.4f}")
