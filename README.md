# Análisis de Movilidad Urbana y Productividad Económica

## 📊 Descripción del Proyecto

Este proyecto analiza la relación entre la movilidad urbana y la productividad económica en principales ciudades de Latinoamérica. Se estudia cómo factores como la congestión, los tiempos de viaje y los retrasos impactan indicadores económicos como el PIB per cápita y la tasa de desempleo.

## 🎯 Problema de Negocio

Un banco de desarrollo busca identificar en qué ciudades invertir en infraestructura de transporte para mejorar la productividad económica y el bienestar de la población.

## 🎯 Objetivo

Explorar y analizar la relación entre indicadores de movilidad urbana y desempeño económico, con el fin de generar recomendaciones basadas en datos para la toma de decisiones estratégicas.

## 📁 Dataset

Este proyecto utiliza dos fuentes principales de datos para analizar la relación entre movilidad urbana y productividad económica:

### 🔹 Datos de Movilidad Urbana

* **Fuente:** `tomtom_traffic.csv`
* **Descripción:** Contiene información sobre congestión vehicular y condiciones de tráfico en distintas ciudades del mundo.
* **Variables clave:**

  * `country`: País
  * `jams_delay`: Tiempo total de retraso por congestión
  * `traffic_index_live`: Índice actual de tráfico
  * `jams_length_kms`: Longitud total de congestión (km)
  * `jams_count`: Número de congestiones registradas
  * `mins_delay`: Minutos de retraso
  * `travel_time_live_per_10kms_mins`: Tiempo de viaje actual por cada 10 km (minutos)
  * `travel_time_hist_per_10kms_mins`: Tiempo de viaje histórico por cada 10 km (minutos)

### 🔹 Datos Económicos y Ambientales

* **Fuente:** `oecd_city_economy.csv`
* **Descripción:** Incluye indicadores económicos, demográficos y ambientales a nivel ciudad, recopilados por la OECD (Organización para la Cooperación y el Desarrollo Económicos).
* **Variables clave:**

  * `year`: Año
  * `country`: País
  * `city_gdp_per_capita`: PIB per cápita por ciudad
  * `unemployment_rate`: Tasa de desempleo (%)
  * `pm25`: Concentración de partículas PM2.5 (μg/m³)
  * `population_millions`: Población (millones)

## 🔗 Integración y Preparación de Datos

Para realizar el análisis, fue necesario integrar dos fuentes de datos con estructuras y niveles de detalle diferentes.

### 🧩 Proceso de Integración

* Se estandarizaron los nombres de columnas en ambos datasets (formato *snake_case*).
* Se revisaron y limpiaron valores nulos y registros inconsistentes.
* Se unificaron los campos de país (`country`) para asegurar compatibilidad entre datasets.
* Se realizó la unión de datos (*merge*) considerando variables comunes como país y, cuando fue posible, año.

### 🧹 Preparación de Datos

* Se filtraron las ciudades con información incompleta en variables clave.
* Se verificaron outliers en variables como PIB per cápita y niveles de congestión.
* Se generaron variables derivadas para facilitar el análisis (por ejemplo, métricas comparativas de tiempo de viaje).

### ⚠️ Consideraciones

* No todos los registros tienen correspondencia directa entre datasets, lo que puede limitar algunos análisis comparativos.
* Existen diferencias metodológicas en la recolección de datos entre fuentes, por lo que los resultados deben interpretarse con cautela.

Esta etapa fue clave para garantizar la calidad del análisis y la validez de los insights obtenidos.

## 🛠️ Herramientas y Tecnologías

* Python (Pandas, NumPy)
* Visualización de datos (Matplotlib, Seaborn)
* Jupyter Notebook

## 🔍 Proceso de Análisis

1. Limpieza y preparación de datos
2. Análisis exploratorio (EDA)
3. Análisis de correlación entre variables de movilidad y económicas
4. Visualización de datos
5. Generación de insights

## 📈 Principales Hallazgos

* Altos niveles de congestión tienden a asociarse con menor productividad en algunas ciudades
* Ciudades con mejores condiciones de movilidad presentan mayor estabilidad económica
* Existen casos atípicos donde ciudades con alta congestión mantienen alto PIB, lo que sugiere factores estructurales adicionales

## ✅ Conclusiones

La mejora en la infraestructura de movilidad urbana puede contribuir positivamente a la productividad económica y al empleo. Sin embargo, la relación no es homogénea entre todas las ciudades, por lo que se requieren estrategias de inversión diferenciadas.

## 📸 Visualizaciones

  * Histograma: para analizar la forma de la distribución y el valor promedio del PIB per cápita.
    <img width="439" height="332" alt="image" src="https://github.com/user-attachments/assets/07330d14-8201-4836-ab5c-36fc7d9b3ead" />
  * gráfico de barras: compara ambas variables, para observar si existe alguna relación entre ellas.
    <img width="824" height="388" alt="image" src="https://github.com/user-attachments/assets/8ec6c0ee-8138-4191-8222-e89c0ce13f09" />

