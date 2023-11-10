![Image text](https://www.google.com/url?sa=i&url=https%3A%2F%2Fenlinea2.uide.edu.ec%2F&psig=AOvVaw3Y7nCWB_7h5gqJPPyNoxan&ust=1699668787720000&source=images&cd=vfe&opi=89978449&ved=0CBEQjRxqFwoTCKCK0dGtuIIDFQAAAAAdAAAAABAD.jpg)

# Maestría en Sistemas de Información con mención en Inteligencia de Negocios y Analítica de datos.

## Proyecto: 
### Diseño de un modelo de detección de datos duplicados mediante Procesamiento del Lenguaje Natural para Optimizar la Eficiencia en la Gestión de Datos en un Laboratorio Farmacéutico

## Autores: 
Doménica Gómez
Cristina Pavón
Dario Herrera
Jacqueline Quispe








## Tabla de contenidos
1. [Información General](#general-info)
2. [Tecnología](#technologies)
3. [Desarrollo](#installation)
4. [Enlaces de interés](#collaboration)


### Información General
***
El cáncer de seno (mama) se origina cuando las células mamarias comienzan a crecer sin control. Las células cancerosas del seno normalmente forman un tumor que a menudo se puede observar en una radiografía o se puede palpar como una masa o bulto.
Es importante que sepa que la mayoría de los bultos en los senos son benignos y no cancerosos (malignos). Los tumores no cancerosos de los senos (benignos) son crecimientos anormales, pero no se propagan fuera de los senos. Estos tumores no representan un peligro para la vida, aunque algunos tipos de bultos benignos pueden aumentar el riesgo de una mujer de padecer cáncer de seno. Cualquier bulto o cambio en el seno debe ser examinado por un profesional de atención médica para saber si es benigno o maligno (cáncer), y si podría afectar su riesgo futuro de padecer cáncer. 

Los cánceres de seno pueden originarse en diferentes partes del seno.

* La mayoría de los cánceres de seno comienza en los conductos que llevan la leche hacia el pezón (cánceres ductales).
* Algunos cánceres se originan en las glándulas que producen leche (cánceres lobulillares).
* También hay otros tipos de cáncer de seno que son menos comunes como el tumor filodes y el angiosarcoma.
* Un pequeño número de cánceres comienza en otros tejidos del seno. A estos cánceres se les llama sarcomas y linfomas, y en realidad no se consideran cánceres de seno.
* Aunque muchos tipos de cáncer de seno pueden causar un bulto  en el seno, no todos lo hacen. 


![Image text](https://colon15.com/wp-content/uploads/2019/08/sintomas-iniciales-cancer-mama.jpg)


## Tecnología
***
Los programas utilizados son:
* [Python](https://www.python.org/): Version 3.8.6
* [VSC](https://code.visualstudio.com/)
* [Jupyter Notebook](https://jupyter.org/)


## Desarrollo
***
Supongamos que usted trabaja en el servicio de salud y recibe muestras que provienen de mujeres con cáncer de mama.
Los médicos han extraído características y las han anotado, el trabajo es crear un modelo que sea capaz de identificar si un paciente tiene o no cáncer.
Recordemos que un falso positivo no es tan preocupante como un falso negativo, ya que en el futuro se le hacen más pruebas a las pacientes y hay oportunidades de descubrir que estábamos en un error.
Sin embargo, un falso negativo puede llevar a que el cáncer se desarrolle sin supervisión durante más tiempo del necesario y podría llevar a daños más graves o incluso la muerte de la paciente.
Teniendo esto en cuenta, desarrolla un modelo que funcione lo mejor posible y explica qué decisiones has tomado en su elaboración y por que.

## Información de atributos:

1) Número de identificación
2) Diagnóstico (M = maligno, B = benigno)

Se calculan diez características de valor real para cada núcleo celular:

a) radio (media de las distancias desde el centro hasta los puntos del perímetro)

b) textura (desviación estándar de los valores de la escala de grises)

c) perímetro

d) área

e) uniformidad (variación local en las longitudes de los radios)

f) compacidad (perímetro^2 / área - 1,0)

g) concavidad (severidad de las partes cóncavas del contorno)

h ) puntos cóncavos (número de porciones cóncavas del contorno)

i) simetría

j) dimensión fractal ("aproximación a la línea de costa" - 1)

Los modelo usados para la predicción son: 

### Modelo Boosting

Es una técnica de aprendizaje automático que combina varios clasificadores o modelos débiles para crear un modelo sólido. La idea detrás del impulso es entrenar una secuencia de modelos, cada uno de los cuales se enfoca en los ejemplos que previamente fueron mal clasificados por el modelo anterior.

### Modelo SVC

Es un algoritmo de clasificación y regresión desarrollado en la década de los 90, dentro del campo de la ciencia computacional. Aunque inicialmente se desarrolló como un método de clasificación binaria, su aplicación se ha extendido a problemas de clasificación múltiple y regresión. SVMs ha resultado ser uno de los mejores clasificadores para un amplio abanico de situaciones, por lo que se considera uno de los referentes dentro del ámbito de aprendizaje estadístico y machine learning.

### Modelo KNN

Es un clasificador de aprendizaje supervisado no paramétrico, que utiliza la proximidad para hacer clasificaciones o predicciones sobre la agrupación de un punto de datos individual.

La base de datos utilizada para el proyecto esta en:

https://github.com/jacqueline-quispe/Proyecto-de-c-ncer/blob/main/data.csv

El notebook es:

https://github.com/jacqueline-quispe/Proyecto-de-c-ncer/blob/main/PROYECTO%20C%C3%81NCER%20DE%20SENO.ipynb

## Conclusión.
***

En el modelo KNN tenemos un error de train de 7.07% y de test de 7.68%, en cuanto a la matriz de confusión tenemos que este modelo predijo correctamente 142 casos de cancer benignos y 279 malignos, los falsos negativos que nos da el modelo es de 27 casos.

El modelo Boosting tenemos un error de train de 0.0% y de test de 5.26%, en cuanto a la matriz de confusión tenemos que este modelo predijo correctamente 283 casos de cancer benignos y 149 malignos, los falsos negativos que nos da el modelo es de 20 casos.

El modelo Boosting tenemos un error de train de 9.73% y de test de 10.96%, en cuanto a la matriz de confusión tenemos que este modelo predijo correctamente 284 casos de cancer benignos y 122 malignos, los falsos negativos que nos da el modelo es de 47 casos.

El modelo Boosting es el que mejor predice la base de datos del cáncer. Debido a que otorga solo 20 casos falsos negativos.

## Enlaces de interés
***
* https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data
* https://interactivechaos.com/es/manual/tutorial-de-machine-learning/clasificadores-svm-en-scikit-learn
* https://www.cienciadedatos.net/documentos/py24-svm-python.html
* https://www.ibm.com/co-es/topics/knn#:~:text=El%20algoritmo%20de%20k%20vecinos%20m%C3%A1s%20cercanos%2C%20tambi%C3%A9n%20conocido%20como,un%20punto%20de%20datos%20individual.
* https://aws.amazon.com/es/what-is/boosting/#:~:text=El%20boosting%20crea%20un%20modelo,una%20entrada%20al%20%C3%A1rbol%20siguiente.
* https://www.cancer.org/es/cancer/cancer-de-seno/acerca/que-es-el-cancer-de-seno.html

##
