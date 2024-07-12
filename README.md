# Introducción

Este código tiene como objetivo predecir la edad de pacientes con base en otros datos disponibles en un conjunto de datos de enfermedades cardíacas. Se utiliza un modelo de regresión lineal para aprender la relación entre las variables y luego se utiliza para estimar las edades faltantes.

# Descripción del código

--Importación de bibliotecas:

pandas: para manipulación de datos.
numpy: para operaciones matemáticas.
sklearn.linear_model: para la creación del modelo de regresión lineal.
sklearn.metrics: para el cálculo de métricas de evaluación del modelo.
plotly.graph_objs: para la creación de visualizaciones.
--Función prediccion_edades:

Esta función carga el conjunto de datos CSV heart_failure_data_ETL.csv.
Elimina las columnas DEATH_EVENT, age y Edad_Categoria del conjunto de datos para crear la matriz de características X.
Define la variable objetivo y como la columna age.
Ajusta un modelo de regresión lineal utilizando sklearn.linear_model.LinearRegression.
Utiliza el modelo ajustado para predecir las edades y las almacena en y_pred.
Calcula el error cuadrático medio (MSE) entre las edades reales y predichas.
Muestra un DataFrame con las edades reales y predichas, junto con el MSE.
Guarda las predicciones en un archivo CSV llamado prediciendo_la_edad.csv.
Devuelve el valor del MSE.
--Ejecución de la función:

--Se llama a la función prediccion_edades() y se almacena el valor del MSE devuelto.
--Se imprime el valor del MSE como "Error cuadrático medio de las predicciones de edad:".
# Parte 10: Prediciendo datos de una columna

Este código puede usarse para estimar valores faltantes en la columna age utilizando las demás columnas del conjunto de datos como variables predictoras. El modelo de regresión lineal aprende la relación entre las variables y luego la utiliza para predecir las edades faltantes. El MSE proporciona una medida de la precisión de las predicciones.

# Consideraciones adicionales:

Este código asume que los datos están limpios y no contienen valores faltantes en las columnas utilizadas para entrenar el modelo. Cómo en efecto están ya tratados.
Es importante evaluar el rendimiento del modelo en un conjunto de datos de prueba independiente para garantizar su generalización.
Se pueden explorar otros modelos de aprendizaje automático para mejorar la precisión de las predicciones.
