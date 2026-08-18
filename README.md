# sprint7-final-project

objetivo: El objetivo  de este proyecto es analizar el comportamiento de uso de llamadas y mensajes de los usuarios móviles de ConnectaTel en México y Colombia. A través de este análisis se buscan identificar patrones de consumo, detectar comportamientos atípicos (outliers), entender la variabilidad entre segmentos demográficos (edad y plan) y proponer recomendaciones para optimizar la oferta comercial y mejorar la retención de usuarios.

Datasets Utilizados
El análisis se realizó integrando tres fuentes de datos principales:
plans.csv: Catálogo de planes con sus precios y beneficios.(precio mensual, minutos y GB incluidos, costo por consumo adicional).
users_latam.csv: Información de cada usuario (ID de usuario, nombre, edad, ciudad, fecha de registro, plan contratado y fecha de cancelación/churn).
usage.csv:  Actividad generada por los usuarios (tipo de interacción: llamadas con su duración en minutos, y mensajes con su longitud en caracteres).m

Etapas del Análisis
1. **Carga y Exploración Inicial:** Inspección de la estructura, formas (`shape`) y tipos de datos de cada dataset.
2. **Identificación y Limpieza de Datos:**
   * Diagnóstico y tratamiento de valores nulos (distinguiendo ausentes justificables MAR como duración/longitud).
   * Corrección de valores *sentinel* ( `-999` en la columna de edad) e imputación mediante estadísticas descriptivas.
   * Conversión y filtrado de fechas fuera de rango (inconsistencias con años futuros).
3. **Análisis Estadístico Descriptivo:** Cálculo de medidas de tendencia central (media, mediana) y dispersión para comprender el perfil típico de consumo.
4. **Visualización de Distribuciones y Outliers:**
   * Generación de histogramas con diferenciación por plan (`hue='plan'`).
   * Construcción de diagramas de caja (*boxplots*) y cálculo de límites mediante el rango intercuartílico (IQR) para identificar *heavy users*.
5. **Segmentación de Clientes:**
   * Clasificación por nivel de uso (`Bajo uso`, `Uso medio`, `Alto uso`).
   * Categorización por rango de edad (`Joven`, `Adulto`, `Adulto Mayor`).
6. **Insight Ejecutivo y Recomendaciones:** Formulación de conclusiones accionables orientadas a la toma de decisiones comerciales.

7. Cómo Ejecutar el Notebook

1. Ve al repositorio en GitHub donde se encuentra cargado este proyecto.
2. Abre el archivo `.ipynb`.
3. Haz clic en el botón de **"Open in Colab"** (o copia la URL del notebook y ábrela directamente desde [Google Colab](https://colab.research.google.com/)).
4. Asegúrate de ejecutar todas las celdas en orden en el menú superior: `Entorno de ejecución` $\rightarrow$ `Ejecutar todas`.
