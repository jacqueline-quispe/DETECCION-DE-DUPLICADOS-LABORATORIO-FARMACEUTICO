![Image text](https://github.com/jacqueline-quispe/DETECCION-DE-DUPLICADOS-LABORATORIO-FARMACEUTICO/blob/main/UIDE.png)

# Maestría en Sistemas de Información con mención en Inteligencia de Negocios y Analítica de datos.

## Proyecto: 
### Diseño de un modelo de detección de datos duplicados mediante Procesamiento del Lenguaje Natural para Optimizar la Eficiencia en la Gestión de Datos en un Laboratorio Farmacéutico

## Autores: 
* Doménica Gómez
* Cristina Pavón
* Dario Herrera
* Jacqueline Quispe








## Tabla de contenidos
1. [Información General](#general-info)
2. [Tecnología](#technologies)
3. [Desarrollo](#installation)
4. [Enlaces de interés](#collaboration)


### Información General
***

El Laboratorio Farmacéutico maneja una gran cantidad de datos, tales como: datos de los médicos, nombres de los visitadores, nombre de productos, entre otros. En la actualidad existen procesos manuales dentro de la Compañía, que implica la ocurrencia de errores humanos en la digitación y duplicación de información, lo que dificulta el posterior análisis de datos. Por tal motivo existe la necesidad de identificar y eliminar dichos datos.
La detección manual de duplicados en grandes conjuntos de datos es un proceso laborioso y propenso a errores, lo que hace indispensable el desarrollo de un modelo de procesamiento del lenguaje natural (NLP) que permita identificar automáticamente duplicados con precisión y eficiencia.

La implementación de un modelo de lenguaje natural que valide o identifique automáticamente los datos duplicados ayudará a la compañía a disminuir la acumulación de información errónea en las diferentes bases de datos, reducción de asignaciones duplicadas de presupuestos, disminución de los gastos operativos, reducción de tiempos en los procesos de tratamiento de datos y verificación de información. También permitirá el análisis adecuando de la información en los procesos posteriores, tales como: segmentación de médicos, cálculo de comisiones, entre otros.

La implementación de validaciones programadas en Excel, como el uso de macros, acompañada de un modelo NLP robusto, permitirá a la organización procesar y analizar los datos de manera más eficiente. Al automatizar la detección de duplicados y la corrección de errores lingüísticos y semánticos, se reducirá 4significativamente el tiempo y el esfuerzo requeridos para mantener la integridad de los datos. Esto no solo mejorará la calidad y confiabilidad de la información, sino que también optimizará la toma de decisiones y la gestión de los recursos de la empresa.


![Image text](https://github.com/jacqueline-quispe/DETECCION-DE-DUPLICADOS-LABORATORIO-FARMACEUTICO/blob/main/NLP.jpg)


## Tecnología
***
Los programas utilizados son:
* [Python](https://www.python.org/): Version 3.8.6
* [VSC](https://code.visualstudio.com/)
* [Jupyter Notebook](https://jupyter.org/)
* [SQL Server](https://www.microsoft.com/es-es/sql-server/sql-server-downloads)
* [MongoDB](https://www.mongodb.com/)


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

https://github.com/jacqueline-quispe/DETECCION-DE-DUPLICADOS-LABORATORIO-FARMACEUTICO/blob/main/MEDICOS%20NUEVOS.xlsx

El notebook es:

https://github.com/jacqueline-quispe/DETECCION-DE-DUPLICADOS-LABORATORIO-FARMACEUTICO/blob/main/C%C3%93DIGO%20NLP.ipynb

## Conclusión.
***

* La implementación de este proyecto ayudará a mejorar la calidad de los datos, reducir costos/tiempo, optimizar recursos, identificando patrones y tendencias para una toma de decisiones eficiente a los departamentos de Marketing, Gerencia de Ventas, Business Inteligencie, Tecnología.

* El algoritmo y modelo de Procesamiento de Lenguaje Natural (NLP), ayudará a mantener una integridad en las bases de datos de la compañía.

* Este proyecto aporta y se alinea a la iniciativa de integración de nuevas tecnologías propuesta por la empresa con el objetivo de mantenerse a la vanguardia de la transformación digital.

## Recomendación.
***

* Orientar al cliente en las necesidades y requerimientos que tiene acerca del modelo de detección de datos duplicados y llegar a un consenso entre ambas partes. De esta manera se puede identificar y solucionar problemas que podrían incrementarse conforme avanza el proyecto.

* Sugerimos a la Compañía implementar las políticas, procedimientos, programas y códigos que permitan garantizar el uso, manejo y recopilación de datos personales, en cumplimiento con la normativa vigente.

* Dado la eficiencia demostrada que tuvo el proyecto en este proceso especifico, se recomienda integrar estratégicamente modelos de procesamiento de lenguaje natural en los distintos sistemas y áreas de la compañía. Esto garantizará una notable mejora en la eficiencia operativa, así como también consolidará la calidad de la información y reforzará la integridad de los datos en toda la organización.

## Enlaces de interés
***
* https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data
* https://interactivechaos.com/es/manual/tutorial-de-machine-learning/clasificadores-svm-en-scikit-learn
* https://www.cienciadedatos.net/documentos/py24-svm-python.html
* https://www.ibm.com/co-es/topics/knn#:~:text=El%20algoritmo%20de%20k%20vecinos%20m%C3%A1s%20cercanos%2C%20tambi%C3%A9n%20conocido%20como,un%20punto%20de%20datos%20individual.
* https://aws.amazon.com/es/what-is/boosting/#:~:text=El%20boosting%20crea%20un%20modelo,una%20entrada%20al%20%C3%A1rbol%20siguiente.
* https://www.cancer.org/es/cancer/cancer-de-seno/acerca/que-es-el-cancer-de-seno.html

##
