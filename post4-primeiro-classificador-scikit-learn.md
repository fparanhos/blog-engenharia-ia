# Criando seu primeiro classificador de IA com Python e Scikit-learn

Hora de aplicar o que vimos. Vamos construir um modelo para reconhecer **dígitos escritos à mão**.

---

## Passo 1 – Importando bibliotecas

```python
from sklearn.datasets import load_digits
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, confusion_matrix

# Carregando dados
digits = load_digits()
X, y = digits.data, digits.target
```

---

## Passo 2 – Dividindo dados

```python
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

---

## Passo 3 – Treinando modelo

```python
model = LogisticRegression(max_iter=10000)
model.fit(X_train, y_train)
```

---

## Passo 4 – Avaliando

```python
y_pred = model.predict(X_test)
print("Acurácia:", accuracy_score(y_test, y_pred))
print("Matriz de Confusão:\n", confusion_matrix(y_test, y_pred))
```

---

## Resultados
- Espera-se acurácia acima de 90%  
- A matriz de confusão mostra onde o modelo erra  

👉 *Teste trocar LogisticRegression por RandomForestClassifier e compare os resultados!*