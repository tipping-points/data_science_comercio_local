## README del Notebook Hackaton 

En el repositorio de Data Science se encuentra el archivo hackaton.ipynb donde se desarrolla el proyecto.

## Objetivo del Proyecto

El objetivo principal de este proyecto es desarrollar una herramienta de Business Intelligence que permita a personas emprendedoras o empresas que buscan establecerse en diferentes barrios de Barcelona, acceder a información estratégica sobre la actividad comercial en cada barrio. A través de esta herramienta, los usuarios podrán evaluar aspectos clave como la densidad comercial, la diversidad de categorías de negocio, la antigüedad promedio de los establecimientos, y más. De esta manera, se facilitará la toma de decisiones para la apertura de nuevos negocios, maximizando las oportunidades de éxito al identificar barrios con alto potencial comercial.

## Descripción paso a paso del proceso
### Importación de Bibliotecas:
En esta primera parte, se importan las bibliotecas necesarias como pandas para la manipulación de datos, y matplotlib para la visualización de gráficos.

### Carga de los datasets:
Los datos de los negocios en diferentes barrios se cargan desde archivos JSON que ya han sido limpiados previamente. Los datos contienen información clave como la ubicación de los negocios, su antigüedad, categoría de actividad, entre otros detalles.

### Concatenación de datasets:
Los dos conjuntos de datos se combinan en un solo DataFrame para hacer un análisis conjunto y estructurado de los negocios en los barrios de Barcelona.

### Creación de características (Feature Engineering):
Se generan múltiples características clave para analizar los negocios por barrio, entre las cuales se incluyen:

Cantidad de negocios por barrio: Calcula cuántos negocios hay en cada barrio.
Diversidad de categorías: Mide cuántas categorías de negocios diferentes existen por barrio.
Proporción de negocios destacados: Determina el porcentaje de negocios destacados (de alto valor) en cada barrio.
Antigüedad promedio: Calcula la edad promedio de los negocios en función de su última revisión.
Última modificación promedio: Extrae el promedio del año de la última modificación de los negocios.
Valor promedio de los negocios: Mide el valor promedio de los negocios en cada barrio según su grupo de actividad.
Densidad geográfica: Mide la concentración de negocios en función de su ubicación geográfica.
Distancia promedio entre negocios: Calcula la proximidad entre los negocios utilizando la desviación estándar de las coordenadas geográficas.
Negocios con más de 10 años: Mide cuántos negocios en cada barrio tienen más de 10 años de antigüedad.
Crecimiento de negocios en los últimos 5 años: Determina cuántos negocios nuevos se han creado en los últimos 5 años.
Tamaño de los negocios: Clasifica los negocios en pequeños, medianos o grandes según su actividad comercial predominante.
Combinación de características:
Todas las características generadas se combinan en un nuevo DataFrame, uniendo la información de cada barrio para tener una vista integral del panorama comercial de Barcelona.

### Guardar los resultados:
El DataFrame final que contiene todas las características de los negocios en los barrios se guarda en un archivo CSV y otro JSON. Estos archivos sirven como la base de datos para generar informes de Business Intelligence.

### Informes de Business Intelligence:
A partir de las características creadas en el proceso de feature engineering, se generaron informes detallados para cada barrio de Barcelona, que incluyen:

Poblenou: Con un número total de 1,512 negocios, una antigüedad promedio de 2.64 años y una alta concentración de medianos y grandes negocios. Se sugiere aprovechar la infraestructura existente para nuevas alianzas estratégicas y expansión comercial.

El Clot: Con 861 negocios y una antigüedad promedio de 2.76 años, se observa una predominancia de negocios medianos y pequeños. Se recomienda diversificar la oferta comercial para atraer nuevas inversiones.

Poble Sec: Cuenta con 1,288 negocios y una antigüedad promedio de 2.78 años. La mayoría de los negocios son medianos, lo que sugiere oportunidades para el crecimiento de pequeños comercios.

Estos informes proporcionan información clave para identificar oportunidades comerciales, hacer análisis comparativos entre barrios, y ofrecer recomendaciones personalizadas para emprendedores o empresas que busquen expandirse en Barcelona.

Poble Sec: With 1,288 businesses and an average age of 2.78 years. Most businesses are medium-sized, which suggests opportunities for the growth of small businesses.

These reports provide key information to identify commercial opportunities, perform comparative analysis between neighborhoods, and offer personalized recommendations for entrepreneurs or companies looking to expand in Barcelona.


