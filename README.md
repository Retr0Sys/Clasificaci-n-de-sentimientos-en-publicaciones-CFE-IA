## Clasificación de Sentimientos CFE IA
## Este proyecto presenta la implementación de un modelo de Aprendizaje Supervisado (Regresión Logística) desarrollado en Python para la clasificación binaria de sentimientos a partir de texto. El objetivo es clasificar los mensajes de texto como positivo (1) o negativo (0), mediante la identificación de patrones lingüísticos.
---

<div align="center"> <img src="https://github.com/user-attachments/assets/cf22be69-13d2-41ec-8ec1-59e212b3ab2e" alt="afa0e8_0be0c0c7217d427dbc939dbd0017eea7" width="800"> </div>

---

## 1. Preprocesamiento y Ingeniería de Datos
La fase inicial es crucial y se centra en la preparación y transformación del dataset para su posterior análisis mediante técnicas de Procesamiento del Lenguaje Natural (PLN).

### Proceso de Limpieza y Organización
Inspección Estructural: Se realiza una visualización inicial del conjunto de datos para comprender su conformación y la forma de las variables.

Gestión de Valores Nulos: Se emplea la función ".info()" y "df.isnull().sum()" para diagnosticar la cantidad de datos faltantes y vacios en las variables clave. Posteriormente utilizamos df.drop_duplicates(inplace=True) para verificar archivos si existen archivos duplicados.

Alineación de Etiquetas: La columna sentimiento del dataset de entrenamiento (dataset_train.csv) se renombra como etiqueta antes de la exportación final para cumplir con el formato de ranking.

---

## 2. Desarrollo y Entrenamiento del Modelo
El modelo se entrena para establecer la relación entre el contenido del mensaje y su clasificación binaria de sentimiento.

### Variables Clave y Metodología
Variable Independiente: "text" (Contenido textual a analizar).

Variable Dependiente: "sentimiento" (Etiqueta binaria: 1 = positivo, 0 = negativo).

Vectorización: Se aplica un método de vectorización sobre la variable text para transformar el contenido textual en un formato numérico procesable por el modelo.

Para la validación interna del rendimiento, el conjunto de datos de entrenamiento es dividido mediante la técnica de "train_test_split", reservando una porción para el entrenamiento y otra para la prueba. Podemos observar la calidad de nuestro modelo utilizando la función "accuracy_score" para comprobar mediante porcentaje que tan certero es el modelo.


--- 

## 3. Evaluación y Validación Externa
La robustez del modelo se comprueba mediante la aplicación a un conjunto de datos sin la columna objetivo y una validación externa que simula un entorno real de competición.

### Proceso de Generación y Validación de Predicciones
Generación de Predicciones: El modelo entrenado se aplica al conjunto de datos de prueba externo (dataset_test_sin_sentimiento.csv), que carece de la columna sentimiento. El modelo genera y asigna los valores predictivos a esta columna.

Entrega: El archivo resultante (submission.csv), que contiene el id y la columna sentimiento agregada (etiqueta), es exportado para la validación en la plataforma de ranking.

---

## 4. Resultados
<div align="center"> <img width="800" alt="Métrica de Desempeño del Modelo" src="https://github.com/user-attachments/assets/7c9234c8-a0bc-4450-a0a6-d1fba6ad1ade" /> </div>

El modelo ha demostrado una alta tasa de efectividad, siendo el porcentaje de acierto estimado mayor al 80% 
