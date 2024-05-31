# ST0256 Tópicos Especiales en Telemática

## Estudiante:
- Nombre: Juan Esteban Avendaño Castaño
- Correo: jeavendanc@eafit.edu.co

## Profesor:
- Nombre: Álvaro Ospina
- Correo: aeospinas@eafit.edu.co

# Proyecto 3 - Spark con Notebooks y PySpark
Este proyecto se enfoca en el uso de Spark con Notebooks y PySpark.
Se hará uso de Google Colab para ejecutar PySpark.

En dataset que se usará es el de [Casos positivos de COVID 19](https://www.datos.gov.co/api/views/gt2j-8ykr/rows.csv?accessType=DOWNLOAD) en Colombia.

## 1 Subir datos Google Drive
Primero se sube el archivo `Casos_positivos_de_COVID-19_en_Colombia.csv` a Google Drive. Este archivo contiene los datos de los casos positivos de COVID-19 en Colombia.

![Google Drive](images/google-drive.png)

## 2 Análisis de exploratorio de los datos
### 2.1 Listar columnas
Se listan las columnas del dataset de la siguiente manera:
![Listar columnas](images/list-columns.png)

### 2.2 Tipos de datos
Se muestran los tipos de datos de las columnas del dataset de la siguiente manera:
![Tipos de datos](images/data-types.png)

### 2.3 Seleccionar algunas columnas
Se seleccionan algunas columnas del dataset de la siguiente manera:
![Seleccionar columnas](images/select-columns.png)

### 2.4 Renombrar columnas
Se renombran las columnas sin espacios en blanco y sin mayúsculas de la siguiente
manera:
![Renombrar columnas](images/rename-columns.png)

### 2.5 Agregar columna
Agregamos una columna al dataset. En este caso agregamos una columna con el tiempo
de recuperación de los pacientes:
![Agregar columna](images/add-column.png)

### 2.6 Borrar columnas
Borramos la columna que acabamos de agregar al dataset:
![Borrar columna](images/delete-column.png)

### 2.7 Filtrar datos
Filtramos los datos del dataset. En este caso filtramos los datos de los pacientes
que tienen más de 60 años:
![Filtrar datos](images/filter-data.png)

### 2.8 Ejecutar una función UDF creando una nueva columna
Se crea una función UDF que categoriza a los pacientes según su edad:
![Función UDF](images/udf.png)

## 3 Preguntas de negocio
Realizamos las preguntas y guardamos los resultados en csv para guardarlo en S3.

### 3.1 Los 10 departamentos con más casos de COVID-19 ordenados de mayor a menor
![Top 10 departamentos](images/top-10-departments.png)

### 3.2 Las 10 ciudades con más casos de COVID-19 ordenadas de mayor a menor
![Top 10 ciudades](images/top-10-cities.png)

### 3.3 Los 10 días con más casos de COVID-19 ordenados de mayor a menor
Lista de los 10 días con más casos de COVID-19 ordenados de mayor a menor
en base a las fechas de diagnóstico, ya que en el diagnóstico se confirma
si el paciente tiene COVID-19:
![Top 10 días](images/top-10-dates.png)

### 3.4 Distribución de casos de COVID-19 por edades en Colombia
![Distribución de casos por edades](images/age-distribution.png)

### 3.5 Distribución de casos de COVID-19 por departamentos en Colombia
![Distribución de casos por departamentos](images/department-distribution.png)

## 4 Subir archivos a Amazon S3
Primero listamos los archivos en el directorio actual para verificar que se crearon los archivos CSV con los resultados de las preguntas de negocio:
![Listar archivos](images/list-csv.png)

Creamos la carpeta `proyecto-3` en S3:
![Crear carpeta en S3](images/create-folder.png)

Instalamos boto3 para poder subir los archivos a Amazon S3:
![Instalar boto3](images/boto-install.png)

Creamos el objeto de conexión a S3:
![Conexión a S3](images/s3-object.png)

Subimos los archivos CSV a S3:
![Subir archivos a S3](images/upload-csv.png)

Verificamos que los archivos se hayan subido correctamente a S3:
![Verificar archivos en S3](images/files-in-s3.png)

## 5 Video
El video del proyecto se encuentra en el siguiente enlace:

[![Explanations video](https://img.youtube.com/vi/CObutEJjC7U/maxresdefault.jpg)](https://youtu.be/CObutEJjC7U)

## 6 Conclusiones
- Se realizó un análisis exploratorio de los datos de los casos positivos de COVID-19 en Colombia.
- Se respondieron preguntas de negocio sobre los casos de COVID-19 en Colombia.
- Se subieron los archivos CSV con los resultados de las preguntas de negocio a Amazon S3.
- Se logró 100% de ejecución de las celdas de PySpark en Google Colab.
