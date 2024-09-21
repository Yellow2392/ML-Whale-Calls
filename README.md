# ML-Whale-Calls
Proyecto final para la asignatura de Machine Learning
## Resumen

El proyecto número 4 de Machine Learning se centra en la clasificación de llamadas de ballenas para prevenir colisiones, basado en señales de audio. Utilizando un subconjunto de un extenso conjunto de datos de segmentos de audio anotados, donde se aplicarán técnicas de extracción de características de audio para obtener los vectores característicos.

## Introducción

### Descripción General

El problema se basa en clasificar distintas señales de audios en si se tratan de sonidos de ballenas francas o no. Las muestras positivas contienen "up-calls" de ballena franca, una vocalización común con una firma acústica de aproximadamente 60Hz-250Hz. La clasificación es desafiante debido a la presencia de ruido antropogénico, como el ruido de barcos, perforaciones, amontonamiento u operaciones navales.

### Objetivo General

El objetivo es desarrollar un sistema de Machine Learning capaz de clasificar segmentos de audio para determinar si contienen o no llamadas de ballenas francas. Se pretende mejorar la precisión en la identificación de estas llamadas.

### Objetivos Específicos

1. Implementar distintos modelos de clasificación, verificando la eficacia y precisión de los resultados.
2. Comprender la naturaleza de los datos para un posterior análisis de los testeos.
3. Comparar los diferentes modelos propuestos respecto al problema establecido en torno a los resultados.

## Dataset

### Descripción

El dataset está compuesto por segmentos de audio de dos segundos de duración, muestreados a una frecuencia de 2kHz. Cada segmento de audio en Train está etiquetado como "Right Whale" o "No Whale". A continuación, se detallan algunos de los archivos y carpetas que componen el dataset:

- `test/`: Subcarpeta que contiene los audios del apartado de testing.
- `train/`: Subcarpeta que contiene los audios del apartado de training.
- `train.csv`: Contiene los ids y las clases de la data de Train.
- `sample_submission.csv`: Contiene el ejemplo de subida para la competición de Kaggle.

### Extracción de Características

Para la extracción de características se usó la librería `librosa`, que se utilizó para procesar los audios y extraer sus vectores característicos MFCC. La matriz MFCC es de forma (20, 230), representando cada ventana de análisis del audio con un vector de 20 dimensiones, dividiendo el audio en 230 ventanas de análisis. También se usó `Pickle` para almacenar los resultados del encoding de Train y Test, ahorrando tiempo en cada ejecución.

### Estructura del dataset

El dataset se compone de dos carpetas con los audios, Test y Train. A continuación, los detalles de las carpetas:

**Train data:**
1. 10934 audios totales
2. 5467 etiquetados como RightWhale
3. 5467 etiquetados como NoWhale
4. 2 segundos de duración en promedio

**Test data:**
1. 1962 audios totales
2. 2 segundos de duración en promedio

Se destinó el 80% de los audios de Train para el entrenamiento y el 20% restante para testing. Los audios de Test se tomaron como base para un segundo testing en la competición de Kaggle.

## Metodología

Se trabajó con MLP, SVM, Regresión Logística, Decision Tree y KNN. Después de hacer pruebas, se optó por usar 3 modelos que dieron los mejores resultados.

## Implementación y Avances

Originalmente el proyecto fue realizado en Google Colaboratory y el documento respectivo fue escrito en Latex. El presente informe en markdown es un resumen del informe en Latex original. 
Entre los archivos se adjunta el susodicho reporte.

**Enlace al Google colab en cuestión:** https://colab.research.google.com/drive/1rxO5v2gYQHatq-1W4PAHTvDcCYZtBvrk?usp=sharing
