# Red Neuronal para Clasificación de Dígitos MNIST

Este proyecto tiene como objetivo construir y entrenar una red neuronal para clasificar dígitos manuscritos del conjunto de datos MNIST. Utilizamos el conjunto de datos MNIST, que contiene 60,000 imágenes de entrenamiento y 10,000 imágenes de prueba de dígitos del 0 al 9. Cada imagen tiene un tamaño de 28x28 píxeles. Este proyecto introduce conceptos fundamentales de redes neuronales, desde el preprocesamiento de datos hasta la evaluación del modelo, usando Keras y TensorFlow.

## Contenido del Proyecto

- Introducción y Contexto

    El proyecto se centra en la clasificación de dígitos manuscritos, una tarea común en el campo de la visión por computadora. El conjunto de datos MNIST es ampliamente utilizado para probar algoritmos de aprendizaje automático, y la red neuronal propuesta tiene como objetivo lograr una clasificación precisa de las imágenes.

- Análisis Exploratorio de los Datos

    Se analizan las imágenes y etiquetas del conjunto de datos MNIST para comprender mejor su estructura y distribución. En esta etapa, se observa la distribución de las clases, así como el tamaño y la resolución de las imágenes, con el fin de asegurar que los datos estén listos para el entrenamiento del modelo.

- Preprocesamiento de los Datos

    Se realiza el preprocesamiento de las imágenes, que incluye la normalización de los valores de los píxeles y la conversión de las etiquetas en formato one-hot encoding.

- Construcción del Modelo

    El modelo es una red neuronal multicapa que consta de una capa de entrada (con 784 neuronas, una por cada píxel de la imagen 28x28), una capa oculta con 512 neuronas y una capa de salida con 10 neuronas, una por cada clase (dígito del 0 al 9). La función de activación utilizada para la capa oculta es ReLU y para la capa de salida es softmax, que es adecuada para la clasificación multiclase.

- Entrenamiento y Validación del Modelo
    
    El modelo se entrena utilizando el optimizador SGD con un learning rate de 0.005 y se evalúa utilizando la categorical crossentropy como función de pérdida. Se entrenó durante 50 épocas con 128 muestras por lote. Durante el entrenamiento, se monitorean las métricas de precisión y pérdida tanto para el conjunto de entrenamiento como para el conjunto de validación.

- Evaluación y Resultados
    
    El modelo se evalúa en el conjunto de prueba y se calculan diversas métricas como la precisión, recall y f1-score para cada clase. Se observa un rendimiento general del modelo de aproximadamente 94% de precisión en la clasificación de dígitos, lo que indica que el modelo generaliza bien a datos no vistos.

## Requisitos

    Python 3.11.9
    Librerías:
        numpy==1.23.5
        tensorflow==2.13.0
        matplotlib==3.9.2
        scikit-learn==1.5.2

    Puedes instalar las dependencias ejecutando:
        pip install -r requirements.txt

## Estructura del Proyecto

    ├── README.md                          # Descripción general del proyecto
    ├── reconocimiento_de_digitos.ipynb    # Código fuente del proyecto en Jupyter Notebook
    └── requirements.txt                   # Archivo con las dependencias del proyecto

## Resultados

    El modelo alcanza una precisión de aproximadamente 94% en el conjunto de prueba. Se han observado métricas de precisión, recall y F1-score muy altas para todas las clases.