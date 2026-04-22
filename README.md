# Normalización de Datos y Gradiente Descendente

Este repositorio contiene un análisis práctico sobre el impacto de la normalización de variables en algoritmos de optimización de Machine Learning.

## ¿Qué hace el notebook?
El notebook principal (oston_normalization_strategies.ipynb) implementa un algoritmo de Regresión Lineal Simple mediante Gradiente Descendente para predecir precios de viviendas del famoso dataset de Boston Housing. 

En lugar de utilizar librerías pre-construidas, modela la optimización desde cero para comparar iteración a iteración el comportamiento del entrenamiento con los datos brutos frente a diferentes estrategias de escalado:
- **Z-Score Normalization** (Estandarización)
- **Min-Max Scaling**
- **Robust Scaling**
- **Log Scaling**

## ¿Para qué sirve?
Su propósito es puramente analítico y educativo. Demuestra de manera visual y cuantitativa el rol fundamental de las escalas en la topología de los datos. En concreto sirve para evidenciar cómo corregir las escalas afecta drásticamente a:
1. **La Tasa de Aprendizaje (Learning Rate):** Datos asimétricos o sin escalar obligan a utilizar tasas minúsculas (del orden de 1e-4) para evitar la divergencia, limitando el algoritmo drásticamente.
2. **La Velocidad de Convergencia:** Las variables normalizadas aceleran radicalmente el tiempo que necesita el Descenso Múltiple para estabilizarse en un mínimo global de precisión.
3. **La Trayectoria Visual:** Permite trazar la diferencia geométrica entre las estrategias para lograr encajar la mejor recta de regresión posible antes de que expire la tolerancia del costo de gradiente.
