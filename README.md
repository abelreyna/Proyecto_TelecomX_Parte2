# 📊 Telecom Churn Prediction Analysis

![Python](https://img.shields.io/badge/python-3.x-blue.svg)
![Data Science](https://img.shields.io/badge/Machine%20Learning-Predictive%20Modeling-orange)
![License](https://img.shields.io/badge/License-MIT-green.svg)

Este proyecto desarrolla un sistema de análisis predictivo para identificar la probabilidad de cancelación de clientes (*Churn*) en una empresa de telecomunicaciones. Se implementaron y compararon múltiples modelos de Machine Learning para determinar los factores críticos que impulsan el abandono y proponer estrategias de retención basadas en datos.

## 🎯 Objetivo del Proyecto
El objetivo principal es construir un modelo robusto que permita a la empresa anticiparse a la salida de clientes, clasificándolos según su nivel de riesgo y entendiendo el "porqué" detrás de su decisión.

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python 3.x
* **Librerías principales:** * `Pandas` y `NumPy` para manipulación de datos.
    * `Scikit-Learn` para modelado predictivo (LogReg, KNN, SVM, Random Forest).
    * `Matplotlib` y `Seaborn` para visualización de datos y análisis de importancia de variables.
* **Entorno:** Google Colab / Jupyter Notebook.

## 📈 Análisis de Modelos y Resultados

Se evaluaron 4 algoritmos principales, obteniendo los siguientes hallazgos sobre la relevancia de las variables:

### 1. Regresión Logística y SVM
Permitieron identificar la **dirección** del impacto. 
* **Factores de Riesgo:** Contratos mes a mes y uso de Fibra Óptica.
* **Factores de Retención:** Antigüedad del cliente (*Tenure*) y contratos a largo plazo.

### 2. Random Forest
Fue el modelo más preciso para jerarquizar la importancia de las variables mediante la reducción de impureza de Gini. 
* **Variables Top:** `Tenure`, `ChargesTotal`, y `ChargesMonthly`.

### 3. KNN (K-Nearest Neighbors)
Confirmó que los perfiles de abandono se agrupan fuertemente según el comportamiento de facturación y tiempo de permanencia.

---



## 🔍 Hallazgos Principales (Insights)

1. **El Contrato es Clave:** Los clientes con contrato "Mes a Mes" son los más propensos a irse. Los contratos de 1 y 2 años reducen el riesgo drásticamente.
2. **La Curva de Aprendizaje del Cliente:** Existe un periodo crítico en los primeros meses (`Tenure` bajo). Si el cliente supera este umbral, su lealtad aumenta exponencialmente.
3. **Sensibilidad al Precio:** Los cargos mensuales elevados sin una diferenciación clara de servicio disparan las alertas de cancelación.
4. **Paradoja de la Fibra Óptica:** A pesar de ser una tecnología superior, los usuarios de fibra presentan mayor churn, sugiriendo problemas de estabilidad o costos no justificados.

## 💡 Estrategias de Retención Propuestas

| Estrategia | Acción |
| :--- | :--- |
| **Fidelización Contractual** | Incentivos para migrar de planes mensuales a anuales. |
| **Monitoreo Early Tenure** | Atención prioritaria y campañas de bienvenida durante los primeros 6 meses. |
| **Optimización de Costos** | Auditoría de precios para clientes de alto valor y planes de fibra óptica. |
