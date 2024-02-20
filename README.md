# fashionMinst
#Problematica
Generar un modelo que categorice las diferente prendas por categoría basadas en imagenes de 28*28.

#Proceso
1. Se importan las librerias necesarias para generar los diferentes procesos que se reuieran en el modelo (Redes neuronales,aprendizaje automatico, creación de vectores y matrices, graficos, etc)
2. Se importa el dataset (En este caso se obtuvo dedede el nlace de descarga  keras.datasets.fashion_mnist.load_data())
3. Se validan los conjuntos de datos para conocer las dimenciones de los conjuntos de datos
4. Se transforman los conjuntos de datos para que se muestren en codigo binario
5. Se agrega una dimención adicional a los cojuntos de datos ya que estamos trabajando con imagenes y entrenando una red neuronal
6. Se grafica un elemento de cada modelo
7. Se genera el modelo en base a la forma de los conjuntos
8. Se configura el tamaño del lote que se va a procesar en cada epoca y cuantas epocas se van a ejecutar y se compila el modelo
9. Se grafica la matriz de confusión en base al entrenamiento.

# Datos de entrenamiento
#Librerias
- import numpy as np
- import keras
- from keras import layers
- import matplotlib.pyplot as plt
- from sklearn.metrics import confusion_matrix
- import seaborn as sns
- import matplotlib.pyplot as plt

# Enlace de desacarga del dataset
- (x_train, y_train), (x_test, y_test) = keras.datasets.fashion_mnist.load_data()

#Configuraciones de entrenamiento
- Train
  batch_size = 152
  epochs = 27
  model.compile(loss="categorical_crossentropy", optimizer="adam", metrics=["accuracy"])
  model.fit(x_train, y_train_cat, batch_size=batch_size, epochs=epochs, validation_split=0.1)
- Test
  batch_size = 132
  epochs = 21
  model.compile(loss="categorical_crossentropy", optimizer="adam", metrics=["accuracy"])
  model.fit(x_test, y_test_cat, batch_size=batch_size, epochs=epochs, validation_split=0.1)
  
  Nota: A pesar de los diferentes parametros utilizados el valor  de val_accuracy no supero el 0.9258
  
