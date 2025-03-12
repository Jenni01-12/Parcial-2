# Predicción del PIB Mundial con Redes Neuronales

## 📌 Descripción del Proyecto

Este proyecto tiene como objetivo analizar y predecir el Producto Interno Bruto (PIB) mundial utilizando Redes Neuronales y técnicas avanzadas de Machine Learning. Para ello, se ha utilizado el conjunto de datos World GDP Dataset extraído del World Bank Group, el cual contiene información del PIB de múltiples países desde 1960 hasta 2022. En si, el análisis se basa en transformar un problema de regresión en un problema de clasificación, segmentando los países según su PIB en categorías: Low GDP, Medium GDP y High GDP. Ademas, se entrenaron diferentes modelos de redes neuronales para comparar su desempeño en esta tarea.

---

## 🎯 Objetivo del Proyecto

El objetivo principal es desarrollar un modelo robusto para clasificar países según su PIB, utilizando un enfoque de Deep Learning, que incluye:

- Análisis Exploratorio de Datos (EDA) para comprender la distribución y evolución del PIB.
- Preprocesamiento de Datos, incluyendo tratamiento de valores atípicos y transformación de variables.
- Transformación del problema de regresión a clasificación (Low, Medium y High GDP).
- Entrenamiento y comparación de redes neuronales con Scikit-Learn y TensorFlow.
- Análisis de desempeño, utilizando métricas como precisión, curva ROC, matriz de confusión y más.

---

## 📊 Descripción del Dataset

🔗 **Fuente :**  [World GDP Dataset - Kaggle](https://www.kaggle.com/datasets/sazidthe1/world-gdp-data)

📂**Archivos Utilizados:**

- gdp_data.csv → Contiene valores del PIB por país y año.
- country_codes.csv → Información de países, regiones y grupos de ingreso.

**Descripción**:
  - Contiene información del PIB de múltiples países desde **1960 hasta 2022**.
  - Se usaron dos archivos principales:
    - **gdp_data.csv** → Datos del PIB por país y año.
    - **country_codes.csv** → Información de países, regiones y grupos de ingreso.

### 📌 Variables del dataset

- **Country Name**: Nombre del país.
- **Year**: Año del registro.
- **GDP**: Producto Interno Bruto en dólares.
- **Region**: Región geográfica del país.
- **Income Group**: Clasificación del país por nivel de ingreso.

📌 **Transformación de la Variable Objetivo**  
Se clasificó el PIB en tres categorías:
- **Low GDP**: Países con PIB bajo.
- **Medium GDP**: Países con PIB medio.
- **High GDP**: Países con PIB alto.

📊 **Análisis Exploratorio de Datos (EDA)**
- Se identificaron patrones históricos en el PIB.
- Se exploraron correlaciones entre variables.
- Se analizaron tendencias económicas a lo largo del tiempo.
---

## 🚀 Modelos Implementados

📌 **Modelos de Redes Neuronales**  
Se compararon diferentes arquitecturas para optimizar la clasificación del PIB:

1️⃣ **Red Neuronal con Scikit-Learn**  
2️⃣ **Red Neuronal Profunda con TensorFlow**  
3️⃣ **Red con una mala configuración de función de pérdida**  

---

## Resultados y Análisis


---

## Conclusiones y Recomendaciones



---

## 👥 Autores

Este proyecto fue desarrollado para IA Aplicada a la Economía – Período 2025-10.

Profesor: Juan Camilo Vega.

Institución: Universidad de los Andes.

Autores:

- Marcelo Yepes - Autor principal
- Jennifer Sanabria - Autor principal
- Angela Torres - Autor principal
- Laura Pabon - Autor principa
Dario montoya - Autor principa

---

## 📦 Requisitos de Instalación

Para ejecutar este proyecto, asegúrate de tener instaladas las siguientes bibliotecas:

```bash
pip install numpy pandas scikit-learn xgboost imbalanced-learn matplotlib seaborn



