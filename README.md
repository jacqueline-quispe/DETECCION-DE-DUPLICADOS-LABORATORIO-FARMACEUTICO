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
1. [Introducción](#introducción)
2. [Tecnología](#tecnologia)
3. [Desarrollo](#desarrollo)
4. [Conclusiones](#conclusiones)
5. [Recomendaciones](#recomendaciones)
6. [Enlaces de interés](#enlaces-de-interés)


### Introducción
***

El Laboratorio Farmacéutico maneja una gran cantidad de datos, tales como: datos de los médicos, nombres de los visitadores, nombre de productos, entre otros. En la actualidad existen procesos manuales dentro de la Compañía, que implica la ocurrencia de errores humanos en la digitación y duplicación de información, lo que dificulta el posterior análisis de datos. Por tal motivo existe la necesidad de identificar y eliminar dichos datos.
La detección manual de duplicados en grandes conjuntos de datos es un proceso laborioso y propenso a errores, lo que hace indispensable el desarrollo de un modelo de procesamiento del lenguaje natural (NLP) que permita identificar automáticamente duplicados con precisión y eficiencia.

La implementación de un modelo de lenguaje natural que valide o identifique automáticamente los datos duplicados ayudará a la compañía a disminuir la acumulación de información errónea en las diferentes bases de datos, reducción de asignaciones duplicadas de presupuestos, disminución de los gastos operativos, reducción de tiempos en los procesos de tratamiento de datos y verificación de información. También permitirá el análisis adecuando de la información en los procesos posteriores, tales como: segmentación de médicos, cálculo de comisiones, entre otros.

![Image text](https://github.com/jacqueline-quispe/DETECCION-DE-DUPLICADOS-LABORATORIO-FARMACEUTICO/blob/main/NLP.jpg)

La implementación de validaciones programadas en Excel, como el uso de macros, acompañada de un modelo NLP robusto, permitirá a la organización procesar y analizar los datos de manera más eficiente. Al automatizar la detección de duplicados y la corrección de errores lingüísticos y semánticos, se reducirá 4significativamente el tiempo y el esfuerzo requeridos para mantener la integridad de los datos. Esto no solo mejorará la calidad y confiabilidad de la información, sino que también optimizará la toma de decisiones y la gestión de los recursos de la empresa.

![Image text](https://github.com/jacqueline-quispe/DETECCION-DE-DUPLICADOS-LABORATORIO-FARMACEUTICO/blob/main/EXCE.png)


## Tecnología
***
Los programas utilizados son:
* [Python](https://www.python.org/): Version 3.11.4
* [VSC](https://code.visualstudio.com/)
* [Jupyter Notebook](https://jupyter.org/)
* [SQL Server](https://www.microsoft.com/es-es/sql-server/sql-server-downloads)
* [MongoDB](https://www.mongodb.com/)
* [Microsoft Excel](https://www.microsoft.com/es/microsoft-365/excel)


## Desarrollo
***
Un humano puede distinguir con claridad la intención de una palabra mal escrita de un solo vistazo. Para una computadora, la distinción no es tan clara. Por tal motivo para el desarrollo del proyecto se ha realizado pruebas con diferentes modelos y algoritmos de NLP, tales como:

### Modelo FuzzyWuzzy

En el ámbito del análisis de datos y el procesamiento del lenguaje natural, comparar y hacer coincidir cadenas es una tarea común y crucial. Sin embargo, debido a variaciones en la ortografía, el orden de las palabras y diferencias menores, es posible que la coincidencia exacta de cadenas no siempre produzca resultados precisos. Aquí es donde entran en juego los algoritmos de coincidencia de cadenas difusas. (Chandra, 2023)

El algoritmo de coincidencia difusa de cadenas busca determinar el grado de cercanía entre dos cadenas diferentes. Esto se descubre utilizando una métrica de distancia conocida como "editar distancia". La distancia de edición determina qué tan cerca están dos cadenas al encontrar el número mínimo de "ediciones" necesarias para transformar una cadena en otra. (Dutta, 2023) 

Hay cuatro tipos principales de ediciones:
* Insertar una letra
* Eliminar una letra
* Intercambiar dos letras adyacentes
* Reemplazar una letra por otra
  
Combinar las operaciones de edición le permite descubrir la lista de posibles cadenas que están a N ediciones de distancia, donde N es el número de operaciones de edición.  Existen diferentes variaciones sobre cómo calcular la distancia de edición. Una de ellas es la distancia de Levenshtein. (Pykes, 2023

#### La distancia de Levenshtein

Es una métrica que lleva el nombre de Vladimir Levenshtein, quien la consideró originalmente en 1965 para medir la diferencia entre dos secuencias de palabras. Podemos usarlo para descubrir la cantidad mínima de ediciones que debe realizar para cambiar una secuencia de una palabra a otra. (Pykes, 2023)


![Image text](https://github.com/jacqueline-quispe/DETECCION-DE-DUPLICADOS-LABORATORIO-FARMACEUTICO/blob/main/lev.png)

Donde
![Image text](https://github.com/jacqueline-quispe/DETECCION-DE-DUPLICADOS-LABORATORIO-FARMACEUTICO/blob/main/1.png)


denota 0 cuando a=b  y 1 en caso contrario. 

Es importante tener en cuenta que las filas del mínimo anterior corresponden a una eliminación, una inserción y una sustitución en ese orden.


Algunos de los algoritmos más comunes incluidos en FuzzyWuzzy son:

#### Algortimo Fuzz Ratio

Este algortimo mide la similitud entre dos cadenas calculando el número mínimo de ediciones de un solo carácter (inserciones, eliminaciones o sustituciones) necesarias para transformar una cadena en la otra. Es útil cuando necesitas comparar dos cadenas y determinar su similitud general. Es eficaz para identificar cadenas similares que pueden tener diferencias menores debido a errores tipográficos o variaciones ortográficas. (Chandra, 2023)

#### Algortimo Fuzz Partial Ratio

Es bastante similar al anterior, pero considera solo la subcadena que mejor coincide entre dos cadenas. Calcula la puntuación de similitud en función de la longitud de la subcadena común más larga, en lugar de la longitud de la cadena completa. Este enfoque ayuda a manejar casos en los que una cadena es un subconjunto o prefijo de la otra. El algoritmo es útil cuando desea encontrar la similitud entre dos cadenas, centrándose solo en la subcadena que mejor coincide. Es particularmente eficaz para identificar coincidencias cuando una cadena es un subconjunto o prefijo de la otra. (Chandra, 2023)

#### Algortimo Fuzz Token Sort Ratio

El algoritmo Token Sort Ratio tokeniza ambas cadenas de entrada, ordena los tokens alfabéticamente y calcula la puntuación de similitud en función de la relación Fuzz entre las listas de tokens ordenadas. Maneja casos en los que el orden de las palabras difiere, pero existe el mismo conjunto de palabras en ambas cadenas. Token Sort Ratio es útil cuando desea comparar cadenas y considerar variaciones en el orden de las palabras. Es particularmente eficaz cuando se espera que las palabras sean similares, pero su posición puede diferir. (Chandra, 2023)

#### Algortimo Fuzz Token Set Ratio

Tokeniza ambas cadenas de entrada, elimina tokens duplicados y calcula la puntuación de similitud en función de la intersección y unión de los conjuntos de tokens. Capta la esencia del contenido de las cadenas en lugar de su orden específico. Token Set Ratio es útil cuando desea comparar cadenas independientemente del orden de las palabras. Es eficaz para escenarios en los que la disposición de las palabras puede variar pero el contenido general sigue siendo similar. (Chandra, 2023)

Algunas de las características clave de FuzzyWuzzy incluyen:
* --Cálculo de similitud:-- FuzzyWuzzy proporciona diversas funciones para calcular la similitud entre cadenas de texto, lo que es útil en la comparación de registros, corrección de ortografía y de duplicación de datos. (GitHub, 2023)
* --Opciones de tokenización:-- FuzzyWuzzy permite personalizar la tokenización y el procesamiento de cadenas para adaptarse a las necesidades específicas del problema. (GitHub, 2023)
* --Selección de la mejor coincidencia:-- Puedes utilizar la función fuzz.extractOne para encontrar la mejor coincidencia entre una cadena de consulta y una lista de cadenas. (GitHub, 2023)
* --Escalabilidad:-- FuzzyWuzzy es eficiente y escalable, lo que lo hace adecuado para aplicaciones que involucran grandes conjuntos de datos. (GitHub, 2023)
* --Fácil de usar:-- La biblioteca es fácil de utilizar y está disponible a través de la instalación con pip en Python. (GitHub, 2023)




### Modelo Berth

![Image text](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTYegJ823ROLc4sxfRTLM3QL5yINzHlLVvBVDYEoU2f7ZEP9FWds-xwtKvlkX7RU4kEEAI&usqp=CAU)

"BERT" (Bidirectional Encoder Representations from Transformers)​ (Devlin, 2008)​, que es uno de los modelos de procesamiento de lenguaje natural más influyentes y ampliamente utilizados desarrollado por Google. 

La metodología de clasificación de texto con BERT es distinta de la presentada anteriormente y se diferencia en que la vectorización y clasificación del texto se hacen en un mismo proceso. Se dice que BERT es un modelo de propósito general ya que se utiliza en diferentes tareas de NLP y para definir el uso que se le quiere dar solo se debe conectar una capa especializada en una tarea específica sobre la capa de output de BERT. Para clasificar texto, sobre la capa de output de BERT se añade el clasificador basado en redes neuronales y durante el entrenamiento se modifican los pesos de BERT y los del clasificador simultáneamente. 

El entrenamiento de BERT consta de 2 fases, el preentrenamiento y la fase de ajuste de parámetros (fine-tuning). En el preentrenamiento el modelo es realizado de manera no supervisada utilizando un corpus grande y es extremadamente costoso en términos de tiempo y poder computacional. En comparación con el tiempo de entrenamiento de FastText, que demora minutos en un computador convencional, el preentrenamiento de BERT podría durar semanas y es por esto por lo que se requiere hardware especializado para procesarlo. Đado que el preentrenamiento de BERT es el equipo de Google Research ha liberado varios modelos BERT costoso. preentrenados bajo distintas condiciones, con corpus de lenguajes diferentes y están disponibles para ser utilizados por la comunidad. En este trabajo se utilizó el modelo preentrenado BERT Base Multilingual Uncased implementado en la librería transformers ​(Wolf, 2019)​. 

BERT se caracteriza por ser un modelo Aprendizaje Profundo, es decir, es una red neuronal de múltiples capaz, y sus buenos resultados en cuanto a la captura de propiedades intrínsecas del lenguaje se deben a la arquitectura de la red. La forma en que están conectadas las capas de la red no es común y cada microestructura dentro de la red tiene un objetivo específico. El modelo BERT se explica de manera conceptual ya que su alta complejidad dificulta detallarlo matemáticamente ​(Wolf, 2019)​. 

Algunas de las características clave de BERT incluyen: 

* --Bidireccionalidad:-- BERT es capaz de capturar el contexto en ambas direcciones en una oración, lo que lo hace más hábil para comprender el significado y la relación entre palabras. 

* --Pre-entrenamiento y ajuste fino:-- BERT se entrena primero en grandes cantidades de texto sin supervisión, lo que le permite aprender representaciones de palabras contextualmente ricas. Luego, se puede ajustar para tareas específicas de NLP con datos de entrenamiento más pequeños ​(Wolf, 2019)​. 

* --Transferencia de conocimiento:-- Debido a su pre-entrenamiento en una gran cantidad de datos, BERT ha demostrado ser altamente efectivo en una variedad de tareas de NLP, como el etiquetado de entidades, la clasificación de texto, la traducción automática, el resumen de texto y más. 

* --Amplia disponibilidad:-- BERT y sus variantes, como RoBERTa, GPT-2 y otros, están disponibles como modelos pre-entrenados y se pueden utilizar en diversas aplicaciones a través de bibliotecas de Python como Hugging Face Transformers. 

* --Elevado rendimiento:-- BERT y sus derivados han logrado un rendimiento líder en muchas tareas de procesamiento de lenguaje natural y han establecido un estándar alto en el campo. 

El modelo que obtuvo un mejor rendimiento en cuanto a resultados y tiempo de ejecución es el modelo FuzzyWuzzy Token Sort Ratio, para lo cual se ha integrado la base de datos y notebook para poder ejecutarlo:

La base de datos utilizada para el proyecto esta en:

https://github.com/jacqueline-quispe/DETECCION-DE-DUPLICADOS-LABORATORIO-FARMACEUTICO/blob/main/ALTAS%20MED_1.xlsm

El notebook es:

https://github.com/jacqueline-quispe/DETECCION-DE-DUPLICADOS-LABORATORIO-FARMACEUTICO/blob/main/CODIGO%20NLP.ipynb


## Conclusiones.
***

* La implementación de este proyecto ayudará a mejorar la calidad de los datos, reducir costos/tiempo, optimizar recursos, identificando patrones y tendencias para una toma de decisiones eficiente a los departamentos de Marketing, Gerencia de Ventas, Business Inteligencie, Tecnología.

* El algoritmo y modelo de Procesamiento de Lenguaje Natural (NLP), ayudará a mantener una integridad en las bases de datos de la compañía.

* Este proyecto aporta y se alinea a la iniciativa de integración de nuevas tecnologías propuesta por la empresa con el objetivo de mantenerse a la vanguardia de la transformación digital.

## Recomendaciones.
***

* Orientar al cliente en las necesidades y requerimientos que tiene acerca del modelo de detección de datos duplicados y llegar a un consenso entre ambas partes. De esta manera se puede identificar y solucionar problemas que podrían incrementarse conforme avanza el proyecto.

* Sugerimos a la Compañía implementar las políticas, procedimientos, programas y códigos que permitan garantizar el uso, manejo y recopilación de datos personales, en cumplimiento con la normativa vigente.

* Dado la eficiencia demostrada que tuvo el proyecto en este proceso especifico, se recomienda integrar estratégicamente modelos de procesamiento de lenguaje natural en los distintos sistemas y áreas de la compañía. Esto garantizará una notable mejora en la eficiencia operativa, así como también consolidará la calidad de la información y reforzará la integridad de los datos en toda la organización.

## Enlaces de interés
***
* https://www.datacamp.com/tutorial/fuzzy-string-python
* https://www.analyticsvidhya.com/blog/2021/07/fuzzy-string-matching-a-hands-on-guide/#h-partial-ratio-using-fuzzywuzzy
* https://medium.com/@chandu.bathula16/understanding-fuzzy-string-matching-exploring-fuzz-ratio-fuzz-partial-ratio-token-set-ratio-and-d6892430f53c
* https://www.analyticsvidhya.com/blog/2021/07/fuzzy-string-matching-a-hands-on-guide/#h-partial-ratio-using-fuzzywuzzy

##
