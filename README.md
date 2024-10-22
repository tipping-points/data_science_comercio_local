# Comercio Local

Carga de Datos:
El proyecto comienza con la carga de datos desde un archivo CSV utilizando pandas, una biblioteca ampliamente utilizada para manipulación de datos en Python.

Bibliotecas Importadas:
pandas: Utilizada para la manipulación de datos.
numpy: Ofrece funciones matemáticas avanzadas, aunque en este fragmento no se utiliza directamente.
matplotlib.pyplot: Se importa para la creación de visualizaciones, aunque tampoco se usa en este bloque.

Cargar los datos:
Los datos se cargan desde el archivo CSV llamado 2024_locals_us_desti.csv ubicado en la carpeta ./Data/ y se almacenan en un DataFrame llamado df. El archivo contiene información sobre locales y mercados que se utilizarán en el análisis.

EDA

Se incluye una función personalizada para analizar las columnas de los datasets, brindando información clave sobre los tipos de datos y los valores únicos presentes en cada columna.


LIMPIEZA

Eliminación de duplicados:
Se eliminan las filas duplicadas en el DataFrame para evitar sesgos en el análisis posterior.
Conteo de valores nulos: Se cuenta el número de valores nulos por columna para identificar posibles problemas con los datos faltantes.

Se exporta el DataFrame limpio a un archivo JSON provisional (2024_locals_us_desti_cleaned.json) para que el equipo de backend lo pueda revisar. El archivo se guarda con el formato de "records", donde cada línea representa un registro independiente.

Se guarda el DataFrame limpio en formato CSV para análisis posteriores, excluyendo el índice del DataFrame como columna.
Análisis del dataset limpio:

Finalmente, se utiliza la función analyze_columns para mostrar un análisis de las columnas del dataset limpio, incluyendo los tipos de datos y los valores únicos por columna.



El primer dataset esta listo y cargamos un segundo dataset para realizar análisis adicionales.

Procedemos a la limpieza:

Se eliminan las filas duplicadas para asegurar que cada registro sea único.
Eliminación de filas con valores nulos:

Se eliminan las filas que tienen valores nulos en las columnas clave (Porta, Solar, Codi_Parcela, etc.), lo que asegura que los datos incompletos no afecten el análisis.
Eliminación de columnas innecesarias:

Se eliminan columnas que no son relevantes para el análisis, como nombres de mercados, galerías, centros comerciales y otras variables redundantes.
Transformación de fechas:

Se convierte la columna Data_Revisio al formato de fecha y hora (datetime).
Luego, se extrae solo el año de la columna de fecha, creando una nueva columna Data_Revision.

se guarda el dataset de los datos limpios:

El dataset limpio se guarda en formato JSON  y CSV para su revisión y análisis futuro.

Finalmente, se utiliza la función analyze_columns para revisar los tipos de datos y los valores únicos en el nuevo dataset limpio.


TRANSFORMACIÓN DE DATOS
Ambos datasets se combinan en un solo DataFrame para hacer un análisis conjunto.
Creamos varias columnas calculadas:
-Cantidad de negocios por barrio.
-Diversidad de categorías de negocios.
-Proporción de negocios destacados.
-Antigüedad promedio de los negocios.
-Densidad geográfica y distancia promedio entre negocios.
-Crecimiento de negocios en los últimos 5 años.
-Distribución de tamaño de negocios.
-Proporción de negocios en la categoría predominante.
-Cantidad de negocios con más de 10 años de antigüedad.

Se utiliza la columna de Data_Revision para calcular la antigüedad de los negocios y el promedio de años de revisión por barrio.
Guardado de las características:

Las nuevas características calculadas por barrio se guardan en dos formatos: CSV (features_barrio.csv) y JSON (features_barrio.json).


RESULTADOS
Figura 1: Top 15 Barrios con Mayor Cantidad de Negocios

Nos permite visualizar los barrios con mayor cantidad de negocios abiertos, facilitando la identificación de áreas con alta actividad comercial.




