# Expansión Estratégica de Biogenesys

Biogenesys, una empresa farmacéutica líder, busca expandir su presencia en Latinoamérica mediante la apertura de nuevos laboratorios farmacéuticos. Para identificar las ubicaciones óptimas, se realizó un estudio exhaustivo de datos de incidencia de COVID-19, tasas de vacunación, infraestructura sanitaria, distribución de la población y factores socioeconómicos. Este informe detalla la metodología empleada, los hallazgos obtenidos y las recomendaciones para la toma de decisiones estratégicas.


## Desarrollo del proyecto
### Metodología de recopilación y selección de datos:
Se recopilaron datos sobre incidencia de COVID-19, tasas de vacunación, infraestructura sanitaria, distribución de la población, prevalencia de enfermedades crónicas, PIB per cápita, entre otros indicadores relevantes.

## Python y Jupyter Notebook

## **Avance 1**: Carga y Transformación de Datos
#### Importación de Librerias

```javascript
import pandas as pd
import numpy as np
```

#### Lectura de Archivo .CSV
 `data = pd.read_csv("data_latinoamerica.csv", sep=',')`


#### Exploración de Datos
Para tener informacion inicial de los datos:
- `data.shape` Devuelve las dimensiones del DataFrame, (filas, columnas)
- `data.head()` Muestra los datos de las primeras 5 filas
- `print(data.dtypes)` Se observa que la columna date esta de tipo de dato object 
- `print(data.isnull().sum())` Verificar la cantidad de valores nulos de cada columna

#### Filtrado de Dataset y Nueva Exploración de Datos

`paises_seleccionados=['Argentina','Chile','Colombia','Mexico','Peru','Brazil']`  Creación de lista con los paises a analizar

`data_latinoamerica=data[data['country_name'].isin(paises_seleccionados)]` Aplicaremos un filtro a la base original con la lista previamente creada

`data_latinoamerica['date'] = pd.to_datetime(data_latinoamerica['date'])` Convertimos la columna 'date' a tipo datetime

`print(data_latinoamerica['date'].dtype)` Verificar el tipo de datos de la columna 'Date'

`print(data_latinoamerica.isnull().sum())` Revision de registro de nulos a partir del filtrado

`data_latinoamerica_paises = data_latinoamerica[data_latinoamerica['location_key'].isin(['AR','CL','CO','MX','PE','BR'])]` Al verificar los datos faltantes en las columna *'location_key'*, se extrae los datos de los paises seleccionados: 'AR','CL','CO','MX','PE','BR'

`data_latinoamerica_paises_Fecha=data_latinoamerica_paises[data_latinoamerica_paises['date']>'2021-01-01']` Filtrado de datos por fecha mayor al 01/01/2021

`valores_nulos_fecha=data_latinoamerica_paises_Fecha.isnull().sum()[data_latinoamerica_paises_Fecha.isnull().sum()>0]
`print(valores_nulos_fecha)`
`print(np.shape(data_latinoamerica_paises_Fecha))` Recuento de Valores Nulos a partir del último filtro aplicado`

## EDA e insights
Se aplicó un análisis exploratorio de datos (EDA) para identificar patrones, tendencias y relaciones entre las variables. Se utilizaron técnicas estadísticas, mediciones y visualizaciones para obtener insights valiosos. Se observaron las siguientes tendencias:
- Disparidad en la tasa de vacunación: Los países con mayor PIB per cápita (Chile, Argentina y Brasil) también presentan las tasas de vacunación más altas.
- Infraestructura sanitaria: Los países con mayor cantidad de médicos y enfermeros por cada 1000 habitantes (Chile, Argentina y Perú).
- Distribución de la población: La mayoría de la población en Argentina y Chile vive en zonas urbanas, mientras que en Colombia, Perú, México y Brasil la población está más distribuida entre zonas urbanas y rurales.


## Insights Relevantes
- Población: Brasil y México tienen las mayores poblaciones urbanas.
- Tasa de mortalidad por COVID-19: Perú y México tienen las tasas más altas.
- Promedio de dosis administradas: Chile tiene la mayor cobertura de vacunación.
- PBI per cápita: Chile y Argentina tienen los más altos, indicando mayor capacidad económica.


