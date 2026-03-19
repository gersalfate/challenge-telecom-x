# 📡 Challenge: Data Science - Análisis de fuga en Telecom X

![Status](https://img.shields.io/badge/STATUS-FINALIZADO-green)
![Python](https://img.shields.io/badge/Python-3.12-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20cleaning-orange)

## 📌 Descripción del proyecto

Este proyecto forma parte del programa **Oracle Next Education (ONE)** de **Oracle + Alura Latam**. Se enfoca en el análisis de fuga de clientes (*churn*) para la empresa Telecom X. El objetivo principal es realizar un **Análisis Exploratorio de Datos (EDA)** exhaustivo para identificar los factores críticos que impulsan la pérdida de suscriptores y preparar el dataset para futuros modelos predictivos.

## 🚀 Metodología de ingeniería de datos

El flujo de trabajo se dividió en etapas estrictas para garantizar la calidad de los hallazgos:

### 1. Extracción y normalización (ETL)

* **Consumo de API:** Recuperación de datos crudos en formato JSON desde repositorios remotos.
* **Aplanamiento (flattening):** Uso de `json_normalize` para transformar estructuras anidadas en un DataFrame relacional de 21 columnas.

### 2. Limpieza y tratamiento (Data cleaning)

* **Gestión de inconsistencias:** Identificación y eliminación de registros con valores vacíos en la variable objetivo (`Churn`), representando un 3.08% de la muestra.
* **Estandarización de datos:** Conversión de métricas financieras de `object` a `float64` para permitir cálculos estadísticos.
* **Ingeniería de características (Feature engineering):**
    * Creación de `charges_daily`: Desglose de costos diarios para análisis de granularidad.
    * Creación de `total_services`: Variable agregada para medir el nivel de adopción tecnológica del cliente.

### 3. Análisis estadístico y correlación

* **Matriz de correlación:** Identificación de relaciones directas entre `tenure` (antigüedad), `charges_monthly` y la probabilidad de fuga.
* **Visualización científica:** Implementación de histogramas, diagramas de caja (boxplots) y pairplots usando `seaborn` para detectar anomalías y patrones de comportamiento.

## 🛠️ Stack tecnológico

* **Lenguaje:** Python 3.12
* **Librerías core:**
    * `pandas`: Tratamiento de datos y normalización de JSON.
    * `matplotlib` & `seaborn`: Visualización estadística avanzada.
    * `numpy`: Operaciones matriciales para análisis de correlación.
* **Entorno:** Google Colab / Jupyter Notebook.

## 📈 Hallazgos estratégicos (Insights)

* **Tasa de fuga:** Se identificó un **26.6% de churn de clientes**, lo que representa una alerta operativa crítica.
* **Factor antigüedad:** Los clientes con menor tiempo de contrato (`tenure` bajo) presentan una probabilidad significativamente mayor de fuga.
* **Sensibilidad al precio:** Existe una correlación positiva entre los cargos mensuales elevados y el abandono del servicio.
* **Método de pago:** Los clientes con 'Electronic check' muestran una tendencia de fuga superior en comparación con métodos automáticos.

## 👤 Autor

* **Gerardo Salfate** ([LinkedIn](https://www.linkedin.com/in/gerardo-salfate/) | [GitHub](https://github.com/gersalfate))
