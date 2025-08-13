![Header](imgs/TelecomX_P1_Header.jpg)

Este proyecto tiene como finalidad analizar y concluir cuál de las 4 tiendas de las cuales nos dieron su información en .csv, es la que tiene **peor desempeño, para ser vendida**. La idea es explorar con las herramientas que tenemos disponibles y a la vez, ser una instancia para mejorar nuestro aprendizaje.

---

### 📋 Información para partir
* Recibimos 4 archivos .csv, en donde cada uno corresponde a una tienda: Tienda 1 , Tienda 2, Tienda 3, Tienda 4. Para no perder los datos, los subí a este repositorio.
* El nombre de las columnas a trabajar son:
  * producto
  * categoriaProducto
  * precio
  * costoEnvio
  * fechaCompra
  * vendedor
  * lugarCompra
  * calificacion
  * metodoPago
  * cantidadCuotas
  * lat
  * lon
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
* 📥 **Extracción y carga de datos :**
   * Se llaman los .csv cargados en este repositorio.
   * Luego, se limpian y preparan los datos para el análisis: conversión de columnas a tipos numéricos y el manejo de valores nulos.
   * Para asegurarnos que haya quedado bien, al final se imprimen los nombres de columnas y los 5 primeros datos por tienda.
 
* 💰 **Ingresos totales por tienda :**
   * Suma total de ingresos por tienda
   * 📊 Porcentaje total de ventas por tienda
   * 📊 Ingresos totales por tienda
   * 📊 Ventas totales por tienda y año v/s media (2020-2022)
   * 📊 Porcentaje de cuota de venta (ingresos), por tienda y por año (1/2020 - 3/2023)
   * 📊 Cantidad de ventas por tienda y año
   
* 📦 **Ventas por categoría :**
   * 📊 Porcentaje de ventas por categoría por tiendas
   * Categorías más vendidas por tienda

* 🛍️ **Productos más vendidos y menos vendidos :**
   *  Productos con más y menos ventas por tienda

* 🚚 **Costo de envío promedio por tienda :** Un spoiler 🤫 promedio no es la herramienta para llegar al valor correcto. Hay que revisar cómo es la distribución de cantidad de ventas y el costo de los productos vendidos, de lo contrario el valor será uno que no corresponde a la realidad debido a la anomalía de unos datos.
   * Costo de envío promedio por tienda
   * Detalle de ventas, costo de envío y porcentaje por tienda
   * Detalle de ventas por año, por tienda
   * Detalle de envíos gratuitos por tienda
   * 📊 Distribución de precios de productos por tienda
   * Análisis descriptivo del precio de productos por tienda
   * 📊 Distribución de costos de envío por tienda
   * Mediana del costo de envío por tienda
   * Moda del costo de envío por tienda
   * Análisis del costo de envío por tienda
   * Análisis del costo de envío por tienda (excluyendo envíos gratuitos)
   * 📊 Relación entre la moda del costo de despacho y la cantidad de compras por ciudad
   * Relación entre la moda del costo de despacho y la cantidad de compras por ciudad (Tabla)
 
* ⭐ **Calificación por tienda :**
   * Calificación promedio por tienda y año
   * 📊 Calificación promedio anual por tienda
   * 📊 Relación entre calificaciones e ingresos por tienda
  
* 🌎 **Análisis de la distribución geográfica de las ventas**
   * 📊 Distribución geográfica de ventas por tienda
   * 📊 Visualización de densidad con agrupamiento por cantidad de ventas
   * 📊 Concentración de ventas de ciudad por tienda
   * 📊 Ventas totales por ciudad
   * 📊 Porcentaje de ventas totales por ciudad
     
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






# TelecomX_P1
Primera parte del challenge de Telecom X


Diccionario para nombre de columnas
customerID: número de identificación único de cada cliente
Churn: si el cliente dejó o no la empresa
gender: género (masculino y femenino)
SeniorCitizen: información sobre si un cliente tiene o no una edad igual o mayor a 65 años
Partner: si el cliente tiene o no una pareja
Dependents: si el cliente tiene o no dependientes
tenure: meses de contrato del cliente
PhoneService: suscripción al servicio telefónico
MultipleLines: suscripción a más de una línea telefónica
InternetService: suscripción a un proveedor de internet
OnlineSecurity: suscripción adicional de seguridad en línea
OnlineBackup: suscripción adicional de respaldo en línea
DeviceProtection: suscripción adicional de protección del dispositivo
TechSupport: suscripción adicional de soporte técnico, menor tiempo de espera
StreamingTV: suscripción de televisión por cable
StreamingMovies: suscripción de streaming de películas
Contract: tipo de contrato
facturaOnline: si el cliente prefiere recibir la factura en línea
metodoPago: Método de pago usado por cliente
cargosMensuales: Total mensual de gasto en todos los servicios contratados por el cliente
cargosTotales: Total gastado por cliente en la empresa
