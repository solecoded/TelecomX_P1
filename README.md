![Header](imgs/TelecomX_P1_Header.jpg)

Este proyecto tiene como finalidad 

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
* Desarrollar al menos 3 gráficos diferentes en el análisis. Hice 16 ✅
* Un informe final recomendando una tienda para vender y argumentando las razones, dentro del desarrollo del proyecto✅
* Un Readme.md para el proyecto (este mismo documento) ✅
* Como un extra, analizar geográficamente los datos. Dentro de lo posible: gráficos que demuestran una concentración geográfica en ventas y/o destino de las compras. Del mapa, solo pude subir una captura porque ya estaba colapsado mi notebook ✅
---

### 💻 Estructura del notebook

**📕 Nota:** Se indica que los datos a analizar van desde el 1 de enero de 2020 al 31 de marzo del 2023. Esa información la pude sacar por tablas, pero como hay gráficos que no se visualizan en Github, tuve que sacar capturas de pantalla a cada uno de ellos y eso aumentó bastante el peso de mi notebook. Eliminé todo lo que pude, incluyendo las tablas donde se ve la primera y la ultima compra registrada en todas las tiendas para llegar a un peso más liviano.

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
   * Normalizacion Datos de internet
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
     * Análisis descriptivo general de churn
     * Matriz de correlación
     * Estadísticas descriptivas de variables clave por churn
     * Métricas (media, mediana y desviación estándar) para permanencia, cargos mensuales y cargos totales
   * Análisis por variables categóricas
   * Análisis por variables numéricas
   * Análisis descriptivo de los datos
 
     
* 🤝 **Conclusiones y recomendaciones:** Esta parte la dividí en 5 secciones para resumir el argumento de por qué vender la tienda que se recomienda. 
   * Ingresos
   * Distribución de precios y productos
   * Costos de envío
   * Calificación y desempeño
   * Conclusión y recomendación
* Gracias a toda la colección de 16 gráficos, cruce de información entre variables, división y visualización de datos según otro conjunto de variables, muchas tablas de visualización: la recomendada para vender es la Tienda 4. ¿Por qué? Muy en resumen: es una tienda que vende prácticamente la misma cantidad de artículos que el resto de tiendas, pero son productos de un valor menor. Ese factor impacta fuertemente en los ingresos de la tienda. 

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


