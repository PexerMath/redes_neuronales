# Perceptrón Simple: Predicción de Diabetes en Mujeres Pima

## Descripción

Este proyecto tiene como objetivo construir un modelo de perceptrón simple 
(red neuronal de una sola neurona) para predecir la presencia de diabetes en mujeres Pima.
Utilizamos el conjunto de datos Pima Indians Diabetes Dataset, que proporciona datos 
médicos y demográficos de mujeres Pima mayores de 21 años, incluyendo características 
relevantes como niveles de glucosa, presión arterial, índice de masa corporal, entre otros. 
Este proyecto introduce conceptos básicos de redes neuronales y técnicas de preprocesamiento 
de datos en Python con Keras.

## Contenido del Proyecto

- Introducción y Contexto
    Este proyecto explora la alta incidencia de diabetes en mujeres Pima, 
    un fenómeno atribuido a factores genéticos y ambientales. Se estudian 
    diversas características clínicas y su relación con la diabetes en esta población.

- Análisis Exploratorio de los Datos
    Se exploran y visualizan las variables para identificar posibles anomalías, 
    valores nulos y tendencias que puedan afectar el modelo.
    `Ejemplo de hallazgo`: Se detectó un grupo de valores inusuales en la variable 
    pedigri_diabetes, lo cual se corrigió sustituyéndolos por la mediana de esa variable.

- Preprocesamiento de los Datos
    Se escalan las características numéricas utilizando StandardScaler de 
    Scikit-Learn para optimizar el rendimiento del perceptrón simple.

- Construcción del Modelo
    Se crea un modelo de perceptrón simple en Keras. La arquitectura del modelo contiene:
    Una capa densa (neuronas conectadas) con una neurona de salida y activación sigmoide para 
    clasificar de manera binaria entre presencia o ausencia de diabetes.

- Entrenamiento y Validación del Modelo
    El modelo se entrena con un conjunto de entrenamiento, usando validación cruzada 
    para ajustar sus parámetros y evaluar su rendimiento en datos no vistos.

- Evaluación y Resultados
    El modelo se evalúa en el conjunto de prueba y se grafican las métricas de 
    accuracy y loss para entrenamiento y validación a lo largo de las épocas de entrenamiento.

## Requisitos
    Python 3.11.9
    Bibliotecas:
        numpy==1.23.5
        pandas==2.2.3
        matplotlib==3.9.2
        seaborn==0.13.2
        scikit-learn==1.5.2
        tensorflow==2.13.0

## Estructura del Proyecto
    ├── README.md           # Descripción general del proyecto
    ├── diabetes_mujeres_pimas.ipynb # Código fuente del proyecto en Jupyter Notebook
    └── pima_diabetes.csv   # Datos de entrada (cargados en línea desde una URL)

## Resultados

El modelo logra una precisión de aproximadamente 75-80% en el conjunto de prueba. 
Para mejorar los resultados, se recomienda:

    - Añadir más capas ocultas o probar una red neuronal multicapa (MLP).
    - Ajustar hiperparámetros como el learning_rate, el batch_size, y el número de épocas.
    - Probar otros optimizadores y técnicas de regularización para evitar el sobreajuste.
