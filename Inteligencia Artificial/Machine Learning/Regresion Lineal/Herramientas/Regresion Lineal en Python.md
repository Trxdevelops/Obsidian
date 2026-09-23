---
tags: [ia, regresion-lineal, herramientas, python]
asignatura: Inteligencia Artificial
tema: Tema 4
---

# Regresión lineal en Python

Parte de [[Regresion Lineal]].

## numpy (ecuación normal)

```python
import numpy as np

X1 = np.column_stack(( X, np.ones(len(X)) ))
betas = np.linalg.inv(X1.T @ X1) @ X1.T @ y
print("beta_n,...,beta_0", betas)
```

> [!warning] En producción se usa `np.linalg.lstsq(X, y, rcond=None)`: mismo resultado, pero resolviendo por descomposición QR en vez de invertir, que es numéricamente más estable.

## statsmodels (OLS)
Puede que necesites: `!pip install -q statsmodels`.

```python
import statsmodels.api as sm

X = sm.add_constant(X)   # añade la columna de unos
model = sm.OLS(y, X)
results = model.fit()
print(results.summary())
```

> [!info] `results.summary()` devuelve la tabla estadística completa: coeficientes, errores estándar, valores p, $R^2$ e intervalos de confianza.

## scikit-learn

```python
from sklearn.linear_model import LinearRegression

regressor = LinearRegression(fit_intercept=True)
regressor.fit(X_train, y_train)
y_pred = regressor.predict(X_test)

beta_1 = regressor.coef_
beta_0 = regressor.intercept_
```

> [!info] La opción `fit_intercept=True` crea por ti la columna de unos necesaria para calcular $\beta_0$.

## seaborn (inspección visual / EDA)

```python
sns.lmplot(x=X, y=y, data=data, ci=95)
```

Muestra el ajuste con su intervalo de confianza.

Relacionado: [[Ecuacion Normal]] · [[Minimos Cuadrados Ordinarios]] · [[Explicabilidad de los Coeficientes]]
