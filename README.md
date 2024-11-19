# Análisis de Formatos de Almacenamiento para Datos de Retrasos en Vuelos

Este proyecto tiene como objetivo realizar un análisis de diferentes formatos de almacenamiento para los datos de retrasos en los vuelos de 2018. A lo largo del notebook, se exploran y comparan varios formatos como **Parquet**, **ORC**, **Snappy-ORC**, y **Avro**, enfocados en dos aspectos clave:

1. **Tamaño de los archivos** generados.
2. **Tiempo de creación** de cada archivo.

## Descripción

En este análisis se utilizaron los datos de los retrasos de vuelos disponibles en el dataset de Kaggle de **"Airline Delay and Cancellation Data"** para el año 2018. El objetivo fue generar archivos en varios formatos de almacenamiento, medir el tamaño de los mismos y comparar el rendimiento en cuanto a tiempo de creación.

Los archivos generados incluyen:
- **Parquet**
- **ORC**
- **Snappy-ORC** (comprimido)
- **Avro** (con datos seleccionados: fecha, aerolínea y retraso)

Además, se ha medido el **tiempo de creación** y el **tamaño** de cada archivo para comparar la eficiencia de los diferentes formatos.



## Archivos Generados

Los siguientes archivos fueron generados y almacenados en el directorio de salida `/kaggle/working/`:

- `air2018.parquet`
- `air2018.orc`
- `air2018_snappy.orc`
- `air2018_small.avro`
- `air2018_small.parquet`

Cada uno de estos archivos fue creado utilizando el dataset original en formato CSV.

## Requisitos

Para ejecutar este notebook, asegúrate de tener instalados los siguientes paquetes de Python:

- `pandas`
- `pyarrow`
- `fastavro`
- `os`
- `time`

Además, necesitarás tener una cuenta de **Kaggle** y acceso al dataset de **Airline Delay and Cancellation Data**.


## Guía Paso a Paso

Si deseas ver el **paso a paso** de cómo realicé este análisis y transformación de datos en Kaggle, he preparado una guía detallada en mi **[portfolio personal](https://leonardonarvaez.com/blog/detail/ejercicio-de-transformacion-de-datos-en-kaggle-analisis-de-retrasos-en-vuelos/)**. 

En esta guía podrás encontrar información adicional y detalles sobre el proceso, desde la carga de datos hasta la conversión a diferentes formatos de almacenamiento.

¡Espero que te sea útil!

## Instrucciones para Ejecutar el Notebook

1. **Clona este repositorio**:

   ```bash
   git clone https://github.com/leo-narvaez/dataset-format-conversion.git
   ```

2. **Sube el notebook y los archivos necesarios a tu entorno de Kaggle.**
   
3. **Cargar el dataset**: Asegúrate de que el archivo `2018.csv` (o cualquier otro año que prefieras) esté correctamente cargado en tu entorno. El archivo debe estar en el directorio de **Inputs** de Kaggle. Puedes descargar el contenido aquí: [Dataset de Retrasos de Vuelos en Kaggle](https://www.kaggle.com/datasets/yuanyuwendymu/airline-delay-and-cancellation-data-2009-2018)


4. **Ejecutar el Notebook**: Puedes ejecutar cada celda del notebook para:
   - Leer y cargar el dataset CSV.
   - Convertirlo a los diferentes formatos de almacenamiento.
   - Medir el tamaño y el tiempo de creación de los archivos generados.

5. **Resultados**: Los resultados se mostrarán en una tabla donde podrás ver:
   - El tamaño de cada archivo (en MB o GB).
   - El tiempo de creación (en milisegundos).

6. **Descargar los archivos**: Una vez completado el análisis, los archivos generados estarán disponibles en la carpeta de salida y podrás descargarlos desde **Kaggle**.

## Resultados Esperados

Los resultados de la ejecución del notebook incluirán:

- **Tamaño de cada archivo** en diferentes formatos (MB, GB).
- **Tiempo de creación** de cada archivo en milisegundos.
- **Comparación de los formatos** en términos de eficiencia de almacenamiento y velocidad de creación.

## Conclusión

Este análisis permite comprender cómo los diferentes formatos de almacenamiento impactan el tamaño de los archivos y el tiempo de procesamiento. Dependiendo del caso de uso (por ejemplo, almacenamiento eficiente o rapidez en el procesamiento), se puede elegir el formato más adecuado.
