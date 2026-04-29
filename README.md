# Machine Learning – Unidad 3  
## PCA y Benchmarking de Algoritmos de Clustering

---

##  Descripción del proyecto

Este proyecto corresponde al Trabajo N°3 de la asignatura de Machine Learning, donde se da continuidad a los desarrollos realizados en la Unidad 1 y Unidad 2.

- En la Unidad 1 se construyó un pipeline reproducible de preparación de datos.
- En la Unidad 2 se reformuló el problema como clasificación binaria mediante la variable `HighPrice`.
- En la Unidad 3 se aplican técnicas de clustering y reducción de dimensionalidad mediante PCA.

---

##  Objetivo

Comparar distintos algoritmos de clustering, evaluando su desempeño mediante métricas internas y externas, con el fin de seleccionar el modelo que mejor represente la estructura de los datos.

---

##  Metodología

El desarrollo del proyecto considera las siguientes etapas:

1. Preparación de datos:
   - Limpieza de datos
   - Tratamiento de valores faltantes
   - One Hot Encoding
   - Normalización

2. Reducción de dimensionalidad:
   - Aplicación de PCA conservando al menos el 90% de la varianza

3. Benchmarking de modelos:
   - K-Means
   - Agglomerative Clustering
   - Gaussian Mixture
   - DBSCAN
   - OPTICS

4. Evaluación de modelos:
   - Métricas internas:
     - Silhouette Score
     - Davies-Bouldin Index
     - Calinski-Harabasz Index
   - Métricas externas:
     - ARI (Adjusted Rand Index)
     - NMI (Normalized Mutual Information)

5. Selección del modelo final

---

##  Resultados

El modelo que presentó mejor desempeño fue **K-Means sin PCA**, ya que obtuvo los valores más altos en ARI y NMI.

Esto indica que los clusters generados tienen una mejor correspondencia con la variable `HighPrice`, utilizada como referencia externa.

Si bien los valores de Silhouette fueron bajos, lo que sugiere que los clusters no están completamente separados, el modelo logró diferenciar de manera razonable viviendas de alto y bajo precio.

Los algoritmos basados en densidad, como DBSCAN y OPTICS, no lograron generar clusters representativos en este caso.

---

##  Conclusión

El trabajo demuestra que:

- La preparación de datos es clave para el desempeño de los modelos.
- PCA puede mejorar la estructura interna, pero no siempre mejora la correspondencia con la variable objetivo.
- Los algoritmos de clustering no siempre encuentran separaciones claras en los datos.
- K-Means es una alternativa simple y efectiva cuando existe una estructura parcialmente separable.

---

##  Reproducibilidad

El proyecto se encuentra desarrollado en un cuaderno Python (`.ipynb`) que puede ejecutarse completamente.

Se utilizó una semilla fija (`random_state=42`) para asegurar consistencia en los resultados.

---

##  Dataset

Dataset utilizado:

House Prices – Advanced Regression Techniques  
https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques

---

##  Integrantes

- Muñoz Morales, Diego Ignacio
- Villarroel Montecinos, Yenny Vanessa
- Matujara Contreras, Jordan Hernán
- Sepúlveda Alvial, Segundo Alejandro
---

## 🔗 Repositorio

https://github.com/diegomunozmo-ops/Trabajo-3-machine-learning
