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

**Procesamiento de Datos**

- Se cargaron y limpiaron los datos de PIB y clasificación de países.
- Se convirtió el problema en clasificación dividiendo el PIB en categorías (Low, Medium, High).
- Se estandarizaron las variables numéricas y se aplicó encoding a las categóricas.
  
**Construcción de Modelos**

- Se implementaron tres modelos de redes neuronales:
- MLP con Scikit-Learn: Optimización de hiperparámetros.
- MLP con TensorFlow: Modelo más profundo con tuning avanzado.
- Experimento con mala función de pérdida: Uso incorrecto de MSE en clasificación.
- 
**Evaluación de Modelos**
  
- Se analizaron métricas como precisión, pérdida, matriz de confusión y curva ROC.
- Se compararon los modelos en términos de desempeño y estabilidad.

---

## Resultados y Análisis
Se evaluaron dos modelos de redes neuronales:
⿡ MLPClassifier de Scikit-learn
⿢ Red neuronal profunda con TensorFlow

Ambos modelos se usaron para predecir el nivel de PIB en tres categorías (Low, Medium, High GDP). Se aplicó búsqueda de hiperparámetros y se analizaron métricas clave como precisión, recall, F1-score y curvas ROC.

📈 Resultados clave:

MLPClassifier (Scikit-learn) alcanzó una precisión del 59%, destacando en la clase 0 (88% precisión, 83% recall), pero con un rendimiento bajo en la clase 2 (36% precisión, 22% recall).
Red neuronal TensorFlow mostró un rendimiento similar en un escenario, pero en otro experimento logró 99% de precisión, lo que sugiere posible sobreajuste.
Curvas ROC muestran que la clase 0 se clasifica mejor (AUC ≈ 0.87), mientras que la clase 2 tiene problemas (AUC ≈ 0.66).

Análisis de Resultados
1. MLPClassifier:
Su mejor configuración: (32 neuronas, activación logistic, LR=0.05).
Problema: El recall en la clase 2 es bajo, lo que indica que el modelo no identifica bien los países con alto PIB.

2. Red Neuronal con TensorFlow:
Un experimento mostró resultados realistas (57% precisión), mientras que otro alcanzó 99% de precisión, lo cual indica sobreajuste.
El sobreajuste se evidencia en la pérdida de validación, que crece mientras la de entrenamiento sigue bajando.

3. Tasa de aprendizaje fija:
Gráficos muestran learning rate constante, lo que puede impedir mejor convergencia.



---

## Conclusiones y Recomendaciones

1. El modelo de TensorFlow muestra sobreajuste extremo
La matriz de confusión en entrenamiento es casi perfecta (99%+ de precisión), mientras que en prueba el rendimiento baja notablemente.
Esto indica que el modelo memoriza los datos de entrenamiento pero no generaliza bien a datos nuevos.
2. Problema de clasificación en clases "Medium" y "High"
La clase "Low" se predice con alta precisión en ambos conjuntos.
Las clases "Medium" y "High" se confunden constantemente, lo que sugiere falta de diferenciación en los datos o una distribución desbalanceada.
3. El modelo de Scikit-learn es más estable pero menos potente
MLPClassifier de Scikit-learn obtuvo 59% de precisión en prueba, con mejor balance entre clases.
Sin embargo, su arquitectura es más simple y podría no capturar relaciones complejas en los datos.

Recomendaciones:
✅ Reducir la complejidad del modelo de TensorFlow para evitar memorizar datos de entrenamiento.
✅ Agregar más regularización  para mejorar la capacidad de generalización.
✅ Equilibrar las clases.
✅ Usar learning rate decay para que el modelo aprenda de manera más estable.
✅ Revisar la calidad de los datos y aplicar técnicas de preprocesamiento para mejorar la separación entre clases.

🔹 Próximo paso: Ajustar el modelo de TensorFlow con las recomendaciones y evaluar nuevamente su desempeño. 🚀📊
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
- Dario montoya - Autor principa

---

## 📦 Requisitos de Instalación

Para ejecutar este proyecto, asegúrate de tener instaladas las siguientes bibliotecas:

```bash
pip install numpy pandas scikit-learn xgboost imbalanced-learn matplotlib seaborn



