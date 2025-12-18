# 📑 TelecomX Latam: Análisis de Evasión de Clientes

📌 **Descripción del Proyecto**

Este proyecto tiene como objetivo analizar el fenómeno de evasión de clientes (Churn) en la empresa TelecomX Latam, identificando patrones y factores que influyen en la decisión de los clientes de abandonar el servicio. La evasión de clientes es un desafío crítico, ya que afecta directamente los ingresos y la sostenibilidad del negocio.

El análisis se realizó mediante un pipeline de extracción, transformación y carga (ETL), seguido de un análisis exploratorio de datos (EDA) y la generación de visualizaciones interactivas y estáticas.

📁 **Estructura del Proyecto**

**TelecomX_LATAM/**

* data/

     * TelecomX_Data.json

* notebooks/

     * Challenge_TelecomX_LATAM_Principal.ipynb

* outputs/

     * TelecomX_Transformacion_Final.csv
  
     * TelecomX_Transformacion_Final.xlsx
  
     * TelecomX_Transformacion_Final.json

* graficos/
  
     * Grafico-Distribucion-Evasion.png
  
     * Grafico-Distribucion-Evasion-Variables-Categoricas.png
  
     * Grafico-Proporcion-Clientes-Evasion.png
  
     * Grafico-Mapa-Correlaciones.png
  
* README.md/

🛠️ **Tecnologías Utilizadas**

* Lenguaje de programación → Python 3

* Pandas → Manipulación y limpieza de datos

* NumPy → Operaciones numéricas

* Matplotlib & Seaborn → Visualizaciones estáticas

* Plotly Express → Visualizaciones interactivas

* Requests → Extracción de datos desde API

* OS / JSON / AST → Manejo de archivos y diccionarios

* Google Colab → Ambiente de trabajo del proyecto

📂 **Flujo del Análisis**

**1. Extracción de Datos**
   
* Se cargaron los datos desde un endpoint JSON proporcionado por la API.

* Se convirtieron en un DataFrame de Pandas para su manipulación.

**2. Transformación de Datos**
   
**Exploración inicial:** 

* Revisión de columnas, tipos de datos y valores nulos.

**Tratamiento de inconsistencias:**

* Conversión de diccionarios anidados en columnas planas.

* Eliminación de duplicados.

* Relleno de valores nulos en servicios (OnlineSecurity, TechSupport, etc.) con "No".

**Creación de nuevas variables:**

* Charges.Daily = Charges.Monthly / 30

**Normalización de etiquetas y tipos:**

* Conversión de variables binarias (Yes/No) a valores numéricos (1/0).

* Reordenamiento de columnas para mayor claridad.

**Exportación final:** 

* Dataset transformado en formatos .csv, .xlsx y .json.

**3. Análisis Exploratorio de Datos (EDA)**

**Estadísticas descriptivas:** 

* Medias medianas, desviaciones estándar y modas.

* Distribución de valores nulos y categóricos.

**Visualizaciones clave:**

* Distribución general de evasión (barras y pastel).

* Evolución de cargos mensuales según Tenure (línea interactiva).

* Mapa de correlaciones entre variables numéricas.

* Evasión por método de pago (Seaborn y Plotly).

* Evasión por variables categóricas (género, contrato, servicio de internet, método de pago).

📊 **Principales Insights**

**Tiempo de permanencia (Tenure):** 

* Clientes con mayor antigüedad tienen menor probabilidad de evadir.

**Método de pago:**

* Los clientes que usan Electronic Check presentan la mayor tasa de evasión.

* Los que usan transferencias automáticas muestran menor evasión.

* Cargos mensuales altos en clientes nuevos: Los clientes que enfrentan cargos elevados en los primeros meses muestran mayor tendencia a evadir.

**Segmentos vulnerables:** 

* Clientes nuevos + cargos altos + métodos de pago poco comprometidos → mayor riesgo de abandono.

✅ **Conclusiones**

* La evasión está fuertemente relacionada con el Tenure y el método de pago.

* Los cargos mensuales altos en clientes nuevos son un factor de riesgo.

* La mayoría de clientes permanece, pero la evasión representa un porcentaje significativo que debe atenderse.

🚀 **Recomendaciones Estratégicas**

* Retención temprana: ofrecer descuentos o planes especiales a clientes en sus primeros meses.

* Promover métodos de pago automáticos: incentivar transferencias bancarias o tarjetas automáticas.

* Monitoreo de clientes con cargos altos: soporte personalizado y planes alternativos.

* Programas de fidelización: beneficios exclusivos para clientes de larga permanencia.

* Comunicación proactiva: alertas y campañas dirigidas a clientes en riesgo de evasión.

📌 **Autor**

* Proyecto desarrollado como parte del Challenge de Data Science LATAM – Alura. 

* Análisis y documentación elaborados por María Fernanda Hernández Solano.
