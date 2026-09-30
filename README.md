# NACA_AeroPredictor 

Este repositorio contiene la implementación de modelos predictivos basados en Machine Learning (Redes Neuronales) diseñados para la predicción de características aerodinámicas. Específicamente, incluye modelos para estimar las propiedades de la capa límite (Boundary Layer - BL) y el espectro de presión en la pared (Wall Pressure Spectra - WPS).

La arquitectura detallada de las redes neuronales empleadas se encuentra evidenciada y comentada dentro del código de cada cuaderno.

Contenido del Repositorio

El proyecto se divide en dos enfoques principales, cada uno con su respectivo cuaderno (notebook), modelo entrenado y escalador de datos:

Modelo de Capa Límite (BL):

Modelo_predictivo_BL.ipynb: Cuaderno principal con el código de predicción.

modelo_BL.pkl: Archivo del modelo entrenado.

scaler_BL.pkl: Escalador utilizado para normalizar las entradas del modelo BL.

Modelo de Espectros de Presión (WPS):

Modelo_predictivo_WPS.ipynb: Cuaderno principal que predice el espectro de presión a partir de características de la capa límite y otras variables.

modelo_mlp.pth: Pesos del modelo de red neuronal (Multi-Layer Perceptron) entrenado para WPS.

scaler.pkl: Escalador utilizado para normalizar las entradas del modelo WPS.

 Guía de Uso

La forma más sencilla y rápida de ejecutar estos modelos es utilizando Google Colab, ya que no requiere configurar un entorno local. A continuación se explican los pasos para utilizar cada modelo.

1. Uso del Modelo Predictivo de la Capa Límite (BL)

Este modelo predice las características de la capa límite basándose en parámetros iniciales como la turbulencia, entre otros.

Pasos:

Descarga los archivos Modelo_predictivo_BL.ipynb, modelo_BL.pkl y scaler_BL.pkl de este repositorio.

Abre Google Colab y sube el cuaderno Modelo_predictivo_BL.ipynb.

En el panel izquierdo de Colab (sección de "Archivos"), sube los archivos modelo_BL.pkl y scaler_BL.pkl al entorno virtual.

Explora el código y ubica la sección de variables de entrada (turbulencia, condiciones de flujo, etc.). Modifica estas características según tu caso de estudio.

Ejecuta todas las celdas del cuaderno para obtener las predicciones de la capa límite.

2. Uso del Modelo Predictivo del Espectro de Presión (WPS)

Este modelo toma como entrada las características de la capa límite (que pueden haber sido calculadas con el modelo anterior) y otras características adicionales para predecir el comportamiento del espectro de presión.

Pasos:

Descarga los archivos Modelo_predictivo_WPS.ipynb, modelo_mlp.pth y scaler.pkl.

Abre Google Colab y sube el cuaderno Modelo_predictivo_WPS.ipynb.

Sube los archivos modelo_mlp.pth y scaler.pkl al entorno de archivos de Colab.

En el código, reemplaza o ingresa los valores correspondientes a las características de la capa límite y demás variables requeridas por el modelo.

Ejecuta las celdas para que la red neuronal procese los datos y genere las predicciones del espectro de presión.

Tecnologías y Requisitos

Lenguaje: Python

Librerías principales: El código hace uso de librerías estándar de Machine Learning y Deep Learning (las dependencias exactas se importan en la primera celda de los cuadernos, habitualmente numpy, pandas, scikit-learn y frameworks como PyTorch para cargar los archivos .pth).

Entorno recomendado: Google Colab.
