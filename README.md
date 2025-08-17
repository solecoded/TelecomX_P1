![Header](imgs/TelecomX_P1_Header.jpg)

Este proyecto tiene como finalidad analizar y comprender el problema del abandono de clientes, conocido como "Churn", en TelecomX. El abandono de clientes es un problema crítico, ya que la retención de clientes es más rentable que la adquisición de nuevos. A través de un análisis exhaustivo de los datos, buscaremos identificar los factores que influyen en el abandono y proponer recomendaciones estratégicas para mitigarlo.

---

### 📋 Información para partir
* Recibimos 1 archivos .json en donde hay registros y datos de clientes. Parte del desafío es limpiarlos y dejarlos listos para el análisis.
* El nombre de las columnas reales y originales encontradas en el archivo .json. Agrego la traducción que me parece más clara y correcta para mi desarrollo del proyecto:

  * **customerID →** ID_cliente
  * **Churn →** churn
  * **customer →** cliente
  * **gender →** genero
  * **SeniorCitizen →** adultoMayor
  * **Partner →** pareja
  * **Dependents →** dependientes
  * **tenure →** permanenciaMeses
  * **phone →** telefono
  * **internet →** internet
  * **account →** cuenta
  * **PhoneService →** servicioTelefonico
  * **MultipleLines →** multiplesLineas
  * **InternetService →** servicioInternet
  * **OnlineSecurity →** seguridadOnline
  * **OnlineBackup →** respaldoOnline
  * **DeviceProtection →** proteccionDispositivo
  * **TechSupport →** soporteTecnico
  * **StreamingTV →** streamingTV
  * **StreamingMovies →** streamingPeliculas
  * **Contract →** tipoContrato
  * **PaperlessBilling →** facturacionOnline
  * **PaymentMethod →** metodoPago
  * **Charges.Monthly →** cargosMensuales
  * **Charges.Total →** cargosTotales

---

### 📌 Debemos entregar

* El proyecto desarrollado en Python. En mi caso lo desarrollé en [Google Colab] (https://colab.research.google.com/) ✅
* Link al repositorio de nuestro proyecto subido en Github ✅
* Un informe final incluído en el Notebook (en mi caso)✅
* Un Readme.md para el proyecto (este mismo documento) ✅
* Crear una columna de costo diario y ver si hay algún hallazgo...
  - Correlación entre el costo diario y el abandono.
  - Correlación entre la cantidad de servicios y el abandono ✅
---

### 💻 Estructura del notebook

El proyecto fue realizado en Google Colab y tiene la siguiente estructura:
* 📚 **Diccionario de mapeo**
  
* 📥 **Extracción (E - Extract)**
   * Importa .json / Verifica que la conversión a DataFrame sea exitosa
   * Resumen del DataFrame
 
* 🔄 **Transformación (T - Transform)**
   * Aplanado de columnas
   * Mapeo nombre de columnas a sus traducciones
   * Normalización columna cargosTotales
   * Normalización situación sentimental
   * Normalizacion datos de internet
   * Normalización columna Dependientes
   * Verificación de inconsistencias en la columna "Churn"
   * Limpieza y recálculo de la columna 'Churn'
   * DataFrame con la nueva columna 'Cuentas Diarias'
   * Transformación de variables categóricas a binarias (0/1)
   * Mapeo al español de valores en la columna tipoContrato
   * Mapeo numérico de valores en la columna metodoPago
   * Mapeo de valores numéricos en la columna servicioInternet
   * Estandarización de columnas binarias churn y facturacionOnline
 
* 🕵️ **Verificación**
   * Verificación de existencia de valores duplicados
   * Verificación de valores nulos (Missing Values)
   * Verificación de tipos de datos (Data Types)
   * Verificación de datos anidados
   * Verificación de duplicados
   * Verificación de valores únicos y consistencia (Categóricas)
   * Verificación de estadísticas descriptivas (Numéricas)
   * Verificación de consistencia lógica (Servicio de internet)
   * Verificaión final de datos
   * Verificacion de valores en columnas
   * Verificación de valores en columnas servicioInternet , tipoContrato y metodoPago     

* 📊 **Carga y Análisis (L - Load & Analysis)**
   * Análisis descriptivo inicial y correlación
     * 📅 Distribución de abandono (Churn) y tipo de contrato
     * 📅 Resumen estadístico de variables numéricas
     * 📅 Matriz de correlación
     * 📅 Tabla de correlación (para cuando da problemas ver la matriz)
     * 📅 Resumen estadístico por Churn
     * 📅 Estadísticas descriptivas de variables clave por churn
     * 📅 Métricas (media, mediana y desviación estándar) para permanencia, cargos mensuales y cargos totales
     * 📅 Análisis comparativo de métricas clave por grupo etario y abandono
   * Análisis por variables categóricas
     * 📅 Análisis de Churn por variables categóricas 
   * Análisis descriptivo de los datos
     * 📊 Cantidad de clientes por método de pago
     * 📊 Distribución etaria de clientes por método de pago
     * 📊 Distribución de uso de servicio telefónico por grupo etario
     * 📊 Distribución de clientes por tipo de servicio y método de pago
     * 📊 Clientes con servicio telefónico y contratación de líneas múltiples
   * Visualizar la distribución del abandono de clientes (churn)     
     * 📊 Visualización de la distribución de churn
     * 📊 Visualización de la distribución de abandono (Churn)
     * 📊 Abandono por género
     * 📊 Abandono por tipo de contrato
     * 📊 Correlación entre costo de contrato promedio y tasa de abandono
     * 📊 Correlación entre mediana de costo de contrato y tasa de abandono
     * 📊 Análisis de churn para servicio de internet por grupo etario
     * 📊 Distribución de permanencia por tipo de contrato y estado de abandono (fibra óptica)
     * 📊 Distribución de permanencia por tipo de contrato y estado de abandono (adultos mayores + fibra óptica)
     * 📊 Distribución de permanencia por tipo de contrato y estado de abandono (NO adultos mayores + fibra óptica)
     * 📊 Abandono por método de pago
     * 📅 Análisis del impacto económico del abandono (Churn)
     * 📊 Estado de clientes Adultos mayores según situación de pareja
     * 📊 Tasa de abandono por grupo etario
     * 📊 Distribución de abandonos por grupo etario
     * 📊 Distribución de abandono (Churn) por permanencia del cliente
     * 📊 Distribución del churn por grupo etario
     * 📊 Distribución del churn por grupo etario / permanencia 0 a 24 meses
     * 📊 Distribución del churn por grupo etario / permanencia 25 meses y más
     * 📊 Análisis de abandono (Churn) por servicio y grupo etario
     * 📊 Cargos mensuales v/s cargos totales por churn
     * 📊 Permanencia vs cargos totales por Churn
     * 📊 Cargos mensuales vs cargos totales por Churn
     * 📊 Permanencia vs cargos **mensuales** por churn y grupo etario
     * 📊 Permanencia vs cargos **totales** por churn y grupo etario

*📔 **Informe**     
El objetivo de este informe es analizar y comprender el problema del abandono de clientes, conocido como "Churn", en TelecomX. El abandono de clientes es un problema crítico, ya que la retención de clientes es más rentable que la adquisición de nuevos. A través de un análisis exhaustivo de los datos, buscaremos identificar los factores que influyen en el abandono y proponer recomendaciones estratégicas para mitigarlo.
    * 📤 **Extracción (E - Extract)**
    * 🔄 **Transformación (T - Transform)**
    * 🕵️ **Verificación**
    * 📊 **Carga y Análisis (L - Load & Analysis)**
      Se realizaron diversos análisis y visualizaciones para identificar patrones y tendencias en el abandono de clientes.
          * Abandono por tipo de contrato y permanencia
          * Abandono por grupo etario y servicios
          * Abandono por permanencia y cargos
    * 🤝 **Conclusiones e Insights:** El problema de abandono es más severo en el segmento de adultos mayores. Este grupo es un punto crítico para la retención, ya que su tasa de abandono es significativamente más alta en casi todos los servicios.
          * El abandono es un fenómeno de "etapa temprana"
          * Factores de abandono por segmento
               * Adultos mayores (+65)
               * No adultos mayores
               * Impacto de la situación de pareja
               * Método de pago como factor de abandono
    * 👨‍🏫 Recomendaciones
          * Estrategias de retención para adultos mayores
          * Fidelización temprana
          * Análisis de la experiencia del usuario con fibra óptica
          * Revisión de ofertas de bajo costo
          * Análisis minuciosos con más información
          * Temporalidad
          
---

### 

Para ejecutar este proyecto, necesitas tener instalado **Python 3.x** (pero en su reemplazo puedes usar Google Colab o Jupyter notebook; o doble clic en el .ipynb para ver el código, tablas y gráficos del proyecto). Las bibliotecas usadas son:

* 🐼 **pandas:** Para la manipulación y análisis de los datos.
* 📊 **matplotlib:** Para la visualización de los gráficos.
* 🔥 **seaborn:** Para gráficos estadísticos, como el mapa de calor.
* 🖱️ **plotly:** Para la creación de gráficos interactivos, como los de dispersión y de barras.
* 👀 **Ipython.display:** Para la correcta visualización del Markdown y las imágenes en el notebook.
* 🧮 **numpy:** Para operaciones numéricas, especialmente en el análisis de agrupamiento.

👾👾👾 **Puedes instalar todo lo  necesario con la siguiente línea:** 👾👾👾

```bash
pip install pandas matplotlib plotly seaborn numpy


