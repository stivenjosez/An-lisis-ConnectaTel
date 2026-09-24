ConnectaTel: Análisis de Datos, Segmentación y Comportamiento de Usuarios

🎯 Objetivo del Proyecto

El objetivo principal de este proyecto es realizar una auditoría completa de calidad de datos, limpieza, análisis exploratorio y segmentación de clientes (users y usage) para la compañía ConnectaTel. Esto permite categorizar a los usuarios según sus patrones reales de consumo de voz y mensajería, extrayendo insights de negocio accionables para optimizar la oferta comercial y los planes de servicios.

📂 Datasets Utilizados

El análisis se fundamenta en el cruce y procesamiento de dos fuentes principales:

users: Contiene la información demográfica, fecha de registro y tipo de plan asignado a cada cliente (Básico o Premium).

usage: Registra las métricas operativas del servicio por usuario, abarcando variables clave como la cantidad de mensajes (cant_mensajes), cantidad de llamadas (cant_llamadas) y minutos totales de llamada (total_minutos_llamada) y fecha que utilizo el servicio.

plans: Contiene la descripcion de beneficios que contiene cada tipo de plan y las tarifas de uso al superar los limites establecidos

🔍 Etapas del Análisis Realizadas

El flujo de trabajo analítico se estructuró en 7 fases principales:

Carga y Exploración Inicial: Importación de librerías (pandas, numpy, seaborn, matplotlib) y lectura de fuentes de datos.

Limpieza y Tratamiento de Anomalías: Identificación y corrección de valores atípicos imposibles (edades con $-999$, cantidades negativas) y filtrado de fechas de registro futuras (superiores a 2024). Imputación de valores nulos utilizando medidas de tendencia central como la mediana.

Análisis Estadístico y Distribuciones: Generación de histogramas y gráficos de densidad para evaluar el comportamiento de los clientes segmentados por tipo de plan.

Detección de Outliers (Método IQR): Cálculo de cuartiles ($Q_1$, $Q_3$), rango intercuartílico ($IQR$) y límites superiores para auditar registros extremos en mensajes, llamadas y minutos.

Segmentación de Clientes (grupo_uso y grupo_edad): Implementación de reglas de negocio mediante estructuras condicionales (funciones con if/elif/else y np.select) para clasificar a la base en categorías operativas (Bajo uso, Uso medio, Alto uso).

Visualización de Segmentos: Construcción de diagramas de barras con conteos (countplot) para auditar la distribución de la base de clientes.

Insights Ejecutivos: Traducción de los hallazgos técnicos en recomendaciones comerciales y estratégicas para los stakeholders de ConnectaTel.

🚀 Cómo Ejecutar el Notebook

Puedes ejecutar y visualizar este proyecto de forma interactiva en la nube sin necesidad de instalar dependencias locales:

Sube tu archivo de notebook (.ipynb) a un repositorio personal de GitHub.

Ingresa a Google Colab.

Selecciona la pestaña GitHub e introduce la URL de tu repositorio.

Abre el archivo y ejecuta las celdas de manera secuencial (de arriba hacia abajo).

📘 Cómo reproducir el análisis
1.	Abre notebooks/everpeak_analysis.ipynb
2.	Ejecuta las celdas en orden
3.	El notebook carga automáticamente el dataset desde /data/ o desde un enlace público (según corresponda)
