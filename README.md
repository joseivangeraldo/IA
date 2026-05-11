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

# 📈 Relatório de Análise: Inclinação da Reta (Slope)
> **Tópico:** Regressão Linear Simples | **Parte:** II - Coeficientes

---

## 🎯 Objetivo
Após determinar a força da relação com o Coeficiente de Pearson ($r$), o próximo passo é calcular a **Inclinação ($m$)**. Este valor define o quanto a variável dependente (Custo) aumenta para cada unidade adicional da variável independente (Idade).

---

## 📐 Fundamentação Matemática

A inclinação da reta de regressão é calculada utilizando a correlação e os desvios padrão das duas variáveis.

### Fórmula Utilizada
$$m = r \cdot \left( \frac{S_y}{S_x} \right)$$

**Onde:**
* **$m$**: Inclinação (Slope).
* **$r$**: Coeficiente de correlação de Pearson.
* **$S_y$**: Desvio padrão da variável dependente (Custo).
* **$S_x$**: Desvio padrão da variável independente (Idade).

---

## 📝 Desenvolvimento do Cálculo
Com base nos dados extraídos da análise:

1. **Parâmetros Identificados:**
    * $r = 0,9879$
    * $S_y = 751,6200$
    * $S_x = 15,9855$

2. **Aplicação na Fórmula:**
    $$m = 0,9879 \cdot \left( \frac{751,6200}{15,9855} \right)$$

> ### 💡 Resultado Final
> **$m = 46,45$**
>
> *Interpretação:* Para este modelo, cada **1 ano** a mais de idade resulta em um aumento estimado de **46,45 unidades de custo**.

---

## 🔍 O que este valor representa?
A inclinação é o "coração" da equação da reta ($y = mx + b$). 
- Se $m$ é **positivo**, a reta sobe (relação direta).
- Se $m$ fosse **zero**, a idade não teria influência nenhuma no custo.

---
*Notas: Cálculos baseados no módulo de Cálculos na Regressão Linear.*
