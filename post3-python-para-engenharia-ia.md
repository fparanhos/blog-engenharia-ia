# Python para Engenharia de IA: as bibliotecas que você precisa dominar

Python é a **linguagem oficial da Inteligência Artificial**.

---

## Principais bibliotecas
- **NumPy** – cálculos numéricos rápidos  
- **Pandas** – manipulação de dados  
- **Matplotlib/Seaborn** – visualização  
- **Scikit-learn** – algoritmos clássicos de ML  

---

## Exemplo prático

```python
import numpy as np
import pandas as pd
from sklearn.linear_model import LinearRegression

# Criando dados simples
X = np.array([[1], [2], [3], [4]])
y = np.array([2, 4, 6, 8])

# Treinando modelo
model = LinearRegression()
model.fit(X, y)

print("Coeficiente:", model.coef_)
print("Intercepto:", model.intercept_)
print("Previsão para 5:", model.predict([[5]]))
```

---

## Conclusão
Essas bibliotecas formam a base de qualquer projeto em IA. Domine-as antes de partir para frameworks mais avançados.

👉 *No próximo post, vamos colocar a mão na massa com um classificador real usando Scikit-learn.*