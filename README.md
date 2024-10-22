# Comercio Local

### Carga de Datos:  
El proyecto comienza con la carga de datos desde un archivo CSV utilizando la biblioteca pandas. Para este análisis, se importan también numpy y matplotlib para la manipulación de datos y la generación de gráficos.

Los datos se cargan desde el archivo CSV llamado 2024_locals_us_desti.csv, almacenándolos en un DataFrame llamado df para su procesamiento posterior.

Análisis Exploratorio de Datos (EDA): 
Se implementa una función personalizada que analiza las columnas del dataset, proporcionando información clave sobre los tipos de datos y los valores únicos en cada columna. Esto permite obtener una visión general del estado de los datos.

Limpieza de Datos:
Eliminación de duplicados: Se eliminan las filas duplicadas en el DataFrame para evitar sesgos en el análisis.
Conteo de valores nulos: Se cuenta el número de valores nulos por columna, lo que ayuda a identificar posibles problemas con los datos faltantes.
Exportación de datos limpios: El DataFrame limpio se exporta en formato JSON (provisional) para que el equipo backend pueda revisarlo, y también en formato CSV para futuros análisis, excluyendo el índice.
Una vez limpio el primer dataset, se carga un segundo dataset para realizar análisis adicionales.

Limpieza del Segundo Dataset: 
Eliminación de duplicados y valores nulos: Se eliminan filas duplicadas y aquellas que contienen valores nulos en columnas clave como Porta, Solar, Codi_Parcela, etc., asegurando que no haya datos incompletos.
Eliminación de columnas innecesarias: Se eliminan las columnas que no son relevantes para el análisis, como nombres de mercados y centros comerciales.
Transformación de fechas: La columna Data_Revisio se convierte al formato de fecha y hora (datetime), y se extrae solo el año, creando la columna Data_Revision.
El dataset limpio se guarda en formato JSON y CSV para análisis posteriores, y se utiliza la función analyze_columns para revisar los tipos de datos y valores únicos.

Transformación de Datos:
Ambos datasets se combinan en un solo DataFrame para realizar un análisis conjunto. A partir de estos datos, se crean varias columnas calculadas que proporcionan información relevante, tales como:

Cantidad de negocios por barrio.
Diversidad de categorías de negocios.
Proporción de negocios destacados.
Antigüedad promedio de los negocios.
Densidad geográfica y distancia promedio entre negocios.
Crecimiento de negocios en los últimos 5 años.
Distribución de tamaño de negocios.
Proporción de negocios en la categoría predominante.
Cantidad de negocios con más de 10 años de antigüedad.
Estas características calculadas por barrio se guardan en formato CSV y JSON para análisis futuros.

Resultados:
Figura 1: Top 15 Barrios con Mayor Cantidad de Negocios

Esta visualización muestra los 15 barrios con mayor cantidad de negocios abiertos, lo que facilita la identificación de áreas con alta actividad comercial.

