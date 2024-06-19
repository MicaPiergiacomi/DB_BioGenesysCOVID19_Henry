# Expansión Estratégica de Biogenesys

Biogenesys, una empresa farmacéutica líder, busca expandir su presencia en Latinoamérica mediante la apertura de nuevos laboratorios farmacéuticos. Para identificar las ubicaciones óptimas, se realizó un estudio exhaustivo de datos de incidencia de COVID-19, tasas de vacunación, infraestructura sanitaria, distribución de la población y factores socioeconómicos. Este informe detalla la metodología empleada, los hallazgos obtenidos y las recomendaciones para la toma de decisiones estratégicas.


## Desarrollo del proyecto
### Metodología de recopilación y selección de datos:
Se recopilaron datos sobre incidencia de COVID-19, tasas de vacunación, infraestructura sanitaria, distribución de la población, prevalencia de enfermedades crónicas, PIB per cápita, entre otros indicadores relevantes.

## Python y Jupyter Notebook

## **Avance 1**: Carga y Transformación de Datos
### IMPORTACION DE LIBRERIAS

```javascript
import pandas as pd
import numpy as np
```

### LECTURA DE ARCHIVOS .CSV
```javascript
data = pd.read_csv("data_latinoamerica.csv", sep=',')
```

### EXPLORACIÓN DE DATOS

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


