# Preprocesamiento y Optimización de Modelos

Pipeline completo de machine learning para la limpieza, transformación y entrenamiento de modelos en un dataset multivariable. Este proyecto explora distintas técnicas de preprocesamiento y selección de algoritmos, incluyendo la optimización avanzada de hiperparámetros con GridSearchCV, RandomizedSearchCV y Optuna.

---

## Objetivo

Seleccionar la técnica de machine learning más adecuada para un conjunto de datos específico, optimizando su rendimiento mediante un pipeline reproducible que integra:

- Limpieza y transformación estructurada.
- Entrenamiento y evaluación comparativa.
- Tuning exhaustivo de hiperparámetros con métodos clásicos y modernos.

---

## Tecnologías y Librerías

- **Python**
- **Pandas**, **NumPy**, **scikit-learn**
- **XGBoost**, **LightGBM**
- **Optuna**, **Matplotlib**, **Seaborn**

---

## Preprocesamiento

Se creó un pipeline modular con `ColumnTransformer` y `Pipeline` que incluye:

- Tratamiento de valores nulos (imputación).
- Detección y transformación de outliers.
- Codificación de variables categóricas (One-Hot Encoding).
- Escalado de variables numéricas (`StandardScaler`).
- Visualización del impacto del preprocesamiento.

---

## Modelos Entrenados y Métricas

Se evaluaron los siguientes algoritmos:

| Modelo              | Métricas Evaluadas                   | Observaciones |
|---------------------|--------------------------------------|----------------|
| Regresión Lineal    | MAE, RMSE                            | Baseline |
| KNN                 | Accuracy, F1-Score                   | Sensible a escalado |
| Árbol de Decisión   | Accuracy, F1, ROC-AUC                | Interpretabilidad |
| Random Forest       | Precision, Recall, F1, ROC-AUC       | Robustez |
| XGBoost             | F1, ROC-AUC, feature importance      | Rendimiento superior |
| LightGBM            | ROC-AUC, Recall                      | Eficiencia computacional |

---

## Optimización de Hiperparámetros

Para el modelo con mejor rendimiento se aplicaron tres métodos:

1. **GridSearchCV**  
   - Búsqueda exhaustiva sobre hiperparámetros definidos.
   - Análisis de curva de validación.

2. **RandomizedSearchCV**  
   - Sampling aleatorio eficiente.
   - Útil en espacios de búsqueda extensos.

3. **Optuna**  
   - Optimización bayesiana y pruning dinámico.
   - Visualización de importancia de hiperparámetros.

---

## Comparación de Modelos

Se evaluaron múltiples algoritmos mediante validación cruzada y métricas de clasificación.

| Modelo                | Validación Cruzada | ROC-AUC  | F1-Score   |
|-----------------------|---------------------|----------|------------|
| Random Forest         | 0.8026              | 0.9142   | **0.9158** |
| XGBoost               | 0.7599              | 0.9142   | 0.9151     |
| Random Forest (Optuna)| —                   | 0.9142   | 0.9069     |


> ✅ Random Forest mostró el mejor rendimiento y fue seleccionado para la optimización.
> Aunque Optuna logró un excelente rendimiento durante la validación cruzada, en el conjunto de prueba el modelo inicial mostró una F1 ligeramente superior.
> Esta comparación resalta la importancia de validar la generalización frente al ajuste fino.

---

## Lecciones y Reflexión

- La automatización con `Pipeline` mejora la reproducibilidad.
- Optuna permite tuning avanzado con menos coste computacional.
- La interpretabilidad sigue siendo clave en contextos reales, incluso al usar modelos complejos.

---

## 👤 Conéctate conmigo

[![Conectar en LinkedIn](https://img.shields.io/badge/LinkedIn-Conectar-blue?logo=linkedin&style=flat-square)](https://www.linkedin.com/in/daniel-araneda-yasic)

¿Eres reclutador o profesional del sector interesado en proyectos aplicados de Data Science, visualización de datos o inteligencia artificial eficiente?  
Este proyecto refleja mi enfoque técnico y comunicativo, y estoy abierto a oportunidades laborales, colaboración en equipos multidisciplinarios y desarrollo de soluciones prácticas y reproducibles.

📫 No dudes en contactarme para conversar sobre cómo puedo aportar valor desde la intersección entre análisis técnico, creatividad visual y documentación didáctica.

