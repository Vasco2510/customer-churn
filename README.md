# Predicción de Abandono de Clientes (Telco Churn Prediction) 📊

Este proyecto fue desarrollado como parte del **Case Analysis 3: Reto 2 - "Abriendo la Caja Negra"** para la Universidad de Ingeniería y Tecnología (UTEC). El objetivo principal es predecir el abandono de clientes (*churn*) en una empresa de telecomunicaciones y aplicar técnicas de **IA Explicable (XAI)** para convertir predicciones en estrategias comerciales.

## 📁 Estructura del Proyecto

* `EDA_CHURN_dataset.ipynb`: Análisis exploratorio de datos, limpieza de variables (como `TotalCharges`) y visualización de correlaciones.
* `DecTree_churn_prediction.ipynb`: Implementación, optimización de hiperparámetros (`GridSearchCV`) y extracción de reglas de decisión.
* `SVM_CHURN_prediction.ipynb`: Experimentación con Máquinas de Soporte de Vectores para comparación de rendimiento.
* `Slides - Case analisis 3.pdf`: Presentación ejecutiva con los hallazgos clave y la estrategia de negocio propuesta.

## 📊 Dataset
Se utilizó el dataset **Telco Customer Churn** de Kaggle, que incluye:
* **7,043 clientes** con 21 variables.
* **Variables clave:** Tipo de contrato, seguridad online, antigüedad (*tenure*), cargos mensuales y método de pago.
* **Target:** `Churn` (Si el cliente dejó la compañía o no).

## 🚀 Resultados del Modelo

El modelo de **Árbol de Decisión** fue optimizado para maximizar el F1-Score, logrando un equilibrio entre precisión y exhaustividad:

| Modelo | F1-Score |
| :--- | :--- |
| Árbol de Decisión (Base) | 0.5204 |
| **Árbol de Decisión (Optimizado)** | **0.6176** |

### Factores más influyentes (Feature Importance)
1.  **Contract (0.674):** El tipo de contrato es el factor determinante.
2.  **OnlineSecurity (0.116):** La falta de seguridad online aumenta drásticamente el riesgo.
3.  **Tenure (0.061):** La lealtad se consolida con el tiempo.

## 💡 Insights y Estrategia de Negocio

Tras "abrir la caja negra" del modelo, identificamos un **Perfil de Máximo Riesgo**: Clientes con contrato mes a mes, sin seguridad online y con menos de 12 meses de antigüedad.

### Recomendaciones Estratégicas:
* **Conversión de Contratos:** Los clientes con contratos mensuales tienen una tasa de cancelación del **43.8%** frente al **5.5%** de los contratos anuales. Se recomienda incentivar el cambio a planes de largo plazo.
* **Venta Cruzada de Seguridad:** La falta de `Online Security` multiplica el riesgo por 4. Se propone ofrecer este servicio de forma gratuita o con descuento para asegurar la retención en los primeros meses.

## 👥 Autores
* **Grupo 6 - Sección 2.01**
* Universidad de Ingeniería y Tecnología (UTEC)

---
*Nota: Los notebooks descargan automáticamente el dataset mediante la librería `kagglehub`.*
