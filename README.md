# Data Science - Ingenias - Fundación YPF - 2025

# Introducción
A medida que el cambio climático se acelera, los océanos del mundo experimentan transformaciones significativas. Este dataset recopila mediciones sintéticas, pero realistas, de la temperatura superficial del mar (TSM), los niveles de pH, la gravedad del blanqueamiento de corales y observaciones de especies en zonas marinas ecológicamente críticas. Abarca el período de 2015 a 2023 y simula cómo responden los entornos marinos al calentamiento global, la acidificación y las olas de calor.

# Objetivo
El objetivo de este trabajo es analizar cuáles de estas variables climáticas han tenido mayor variabilidad a lo largo del tiempo y si el cambio en las condiciones del medio tiene o no una correlación con los cambios en los registros biológicos, dependiendo del lugar en que se realizan las simulaciones.

# Dataset:
https://www.google.com/url?q=https%3A%2F%2Fwww.kaggle.com%2Fdatasets%2Fatharvasoundankar%2Fshifting-seas-ocean-climate-and-marine-life-dataset


# Análisis Exploratorio (analisis_exploratorio.ipynb)
Este archivo nos da un primer vistazo sobre la información que brinda cada columna y algunas relaciones entre sí. Se trabaja en corregir valores faltantes y en tratar los outliers.


# Modelo supervisado de clasificación (clasificacion_bleaching_modelo.ipynb)
Este archivo presenta el entrenamiento de modelos de aprendizaje supervisado para predecir la gravedad del blanqueamiento de coral en función de variables ambientales.
Se evaluaron cuatro algoritmos de clasificación:
 - Random Forest
 - Árbol de Decisión
 - k-Nearest Neighbors (kNN)
 - Regresión Logística

El proceso se desarrolló en tres etapas:
  1) Entrenamiento inicial (“en crudo”): sin optimización de parámetros ni técnicas específicas de validación.
  2) Validación cruzada (Stratified K-Fold): para obtener métricas más robustas, dada la escasa cantidad de datos y el desbalance de clases.
  3) Optimización de hiperparámetros (Grid Search): se ajustaron los parámetros de cada modelo para mejorar su rendimiento predictivo.
