# fashionMinst
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
  
