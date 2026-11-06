# 📊 Análisis de Datos y Segmentación de Clientes - ConnectaTel

Este repositorio contiene el desarrollo de un proyecto end-to-end de análisis exploratorio de datos (EDA), limpieza, tratamiento de valores nulos, análisis de valores atípicos (*outliers*) y segmentación de clientes para la compañía **ConnectaTel**.

---

## 🎯 1. Objetivo del Proyecto
Traducir los datos de perfiles de usuario en conclusiones accionables para el negocio, identificando patrones de consumo, agrupando a los clientes según su edad e intensidad de uso, y generando recomendaciones estratégicas orientadas a mejorar la oferta de planes, maximizar el ARPU y optimizar la retención de clientes.

---

## 📂 2. Datasets Utilizados
* **`user_profile`**: Dataset principal que recopila información demográfica y de consumo de los clientes de ConnectaTel, incluyendo:
  * **Datos demográficos y de cuenta**: `user_id`, `first_name`, `last_name`, `age`, `city`, `reg_date`, `plan`, `churn_date`.
  * **Métricas de consumo**: `cant_minutos_llamada`, `cant_mensajes`, `cant_llamadas`, entre otras.

---

## 🔍 3. Etapas del Análisis Realizadas
El proyecto se estructuró en las siguientes fases clave:
1. **Limpieza e Inspección Inicial**: Carga del DataFrame, verificación de tipos de datos, inspección de valores nulos y manejo de registros faltantes en columnas clave (como ciudades, apellidos y fechas de cancelación de usuarios activos).
2. **Análisis de Outliers (Valores Atípicos)**: Aplicación del método del Rango Intercuartílico (IQR) sobre las variables de consumo. Decisión fundamentada de retener estos registros al clasificarlos como *power users* (usuarios de alto valor con patrones de consumo legítimos).
3. **Ingeniería de Características y Segmentación**:
   * **`grupo_edad`**: Clasificación de los usuarios utilizando comparaciones lógicas (`Joven` si < 30 años, `Adulto` si < 60 años, y `Adulto Mayor` para el resto).
   * **`grupo_uso`**: Categorización de la intensidad de interacción de los clientes en `Bajo uso`, `Uso medio` y `Alto uso`.
4. **Visualización de Datos**: Generación de gráficos de distribución (`countplot`) para analizar el comportamiento y la concentración de usuarios por edad y nivel de uso.
5. **Informe Ejecutivo**: Síntesis de hallazgos orientada a *stakeholders*, respondiendo preguntas clave de negocio sobre calidad de datos, valor de segmentos e implicaciones de los *outliers*.

---

## 🚀 4. Cómo Ejecutar el Notebook
Puedes ejecutar este proyecto de forma interactiva utilizando **Google Colab** o de manera local:

### Opción A: Ejecutar en Google Colab
1. Sube tu archivo `.ipynb` a [Google Colab](https://colab.research.google.com/).
2. Asegúrate de tener instaladas las librerías necesarias (`pandas`, `numpy`, `matplotlib`, `seaborn`).
3. Ejecuta las celdas de forma secuencial de arriba a abajo.

### Opción B: Ejecutar Localmente
1. Clona este repositorio en tu computadora:
   ```bash
   git clone [https://github.com/julych080808/Analysis-everpeak.git](https://github.com/julych080808/Analysis-everpeak.git)
