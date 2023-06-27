# Preguntas y respuestas comunes en un examen de Spark

## 1\. ¿En qué lenguaje está desarrollado Spark?

Python

R

Java

**Scala**

**Spark está desarrollado principalmente en Scala. Scala es un lenguaje de programación que se ejecuta en la Máquina Virtual de Java (JVM) y proporciona una sintaxis concisa y expresiva. Aunque Spark admite varios lenguajes de programación, incluyendo Python, R y Java, su implementación principal se realiza en Scala.**

## 2\. Spark Streaming, ¿de qué fuentes puede ser la data?

- Kafka
- Flume
- Kinesis
- **Todas las anteriores**

**Explicación:**
En Spark Streaming, los datos se pueden obtener de diversas fuentes, incluyendo Kafka, Flume y Kinesis. Spark Streaming proporciona conectores o receptores integrados para estas populares plataformas de streaming, lo que facilita la ingesta de datos desde ellas. Por lo tanto, la respuesta correcta es "Todas las anteriores" (All of the Above). Spark Streaming ofrece flexibilidad e interoperabilidad con múltiples fuentes de datos para satisfacer diferentes requisitos de ingestión de datos en tiempo real.

## 3\. Apache Spark cuenta con API en

- Java
- Scala
- Python
- **Todas las anteriores**

**Explicación:**
Apache Spark ofrece APIs en Java, Scala y Python. Estos tres lenguajes son compatibles con Spark, lo que permite a los desarrolladores elegir su lenguaje preferido para interactuar con la funcionalidad de Spark y construir aplicaciones en Spark. Las APIs de Spark están diseñadas para proporcionar una experiencia consistente en estos lenguajes, permitiendo a los desarrolladores aprovechar el poder de Spark utilizando el lenguaje de programación con el que se sientan más cómodos.

## 4\. ¿Cuál de los siguientes no es un componente del ecosistema de Spark?

- Sqoop
- GraphX
- MLlib
- BlinkDB
- **Sqoop**

**Explicación:**
Sqoop no es un componente del ecosistema de Spark. Sqoop es en realidad una herramienta desarrollada por Apache para transferir eficientemente grandes volúmenes de datos entre Apache Hadoop y bases de datos estructuradas, como bases de datos relacionales. Por otro lado, GraphX, MLlib y BlinkDB son componentes del ecosistema de Spark.

GraphX es una biblioteca de procesamiento de gráficos construida sobre Spark que proporciona un marco de trabajo de cálculo distribuido para análisis de gráficos. MLlib, también conocida como Spark ML, es una biblioteca de aprendizaje automático que ofrece diversos algoritmos y herramientas para análisis de datos y tareas de aprendizaje automático. BlinkDB, aunque es un componente experimental, es un motor de consultas diseñado para análisis e exploración interactiva de grandes volúmenes de datos dentro de Spark.

## 5\. La abstracción básica de Spark Streaming es

- **Dstream**
- RDD
- Variable compartida
- Ninguna de las anteriores

**Explicación:**
La abstracción básica de Spark Streaming es DStream (Discretized Stream). DStream representa un flujo continuo de datos en Spark Streaming. Es una secuencia de RDDs (Resilient Distributed Datasets), donde cada RDD contiene datos de un intervalo de tiempo específico.

DStream proporciona una API de alto nivel para realizar transformaciones y acciones en los datos de streaming. Permite a los desarrolladores aplicar diversas operaciones, como filtrado, mapeo, reducción y unión, en el flujo de datos. Los DStreams abstraen la complejidad de manejar flujos de datos continuos y proporcionan una interfaz de programación similar al trabajo con datos por lotes en los RDDs de Spark.

Los DStreams se pueden crear a partir de datos en vivo (como datos de HDFS, Kafka o Flume) o se pueden generar mediante la transformación de DStreams existentes utilizando operaciones como map, window y reduceByKeyAndWindow.

Internamente, los DStreams se caracterizan por algunas propiedades básicas:

- Dependencia de una lista de otros DStreams.
- Un intervalo de tiempo en el que el DStream genera un RDD.
- Una función que se utiliza para generar un RDD después de cada intervalo de tiempo.

## 6\. ¿Cuál de los siguientes algoritmos no está presente en MLlib?

- Regresión lineal en streaming (Streaming Linear Regression)
- KMeans en streaming (Streaming KMeans)
- **Distancia de Tanimoto (Tanimoto distance)**
- Ninguno de los anteriores

**Explicación:**
El algoritmo que no está presente en MLlib (la biblioteca de aprendizaje automático de Spark) es la distancia de Tanimoto (Tanimoto distance).

MLlib ofrece una amplia gama de algoritmos de aprendizaje automático y utilidades para diversas tareas, como clasificación, regresión, agrupamiento y filtrado colaborativo. Sin embargo, MLlib no incluye el algoritmo de distancia de Tanimoto.

Por otro lado, MLlib sí incluye los algoritmos de Regresión lineal en streaming (Streaming Linear Regression) y KMeans en streaming (Streaming KMeans), los cuales son compatibles para manejar datos en streaming en escenarios en tiempo real.

## 7\. Internamente, DStream es

- **Flujo continuo de RDD (Resilient Distributed Datasets)**
- Flujo continuo de DataFrame
- Flujo continuo de DataSet
- **Ninguna de las anteriores**

**Explicación:**
Internamente, DStream representa un flujo continuo de RDDs (Resilient Distributed Datasets). Por lo tanto, la respuesta correcta es "Flujo continuo de RDD" (Continuous Stream of RDD). DStream es una abstracción fundamental en Spark Streaming y proporciona una interfaz de programación de alto nivel para procesar y manipular datos de streaming. Permite a los desarrolladores aplicar transformaciones y acciones en el flujo de RDDs, lo que permite el procesamiento y análisis de datos en tiempo real en Spark Streaming.

## 8\. ¿Podemos agregar o configurar nuevas tareas de cálculo después de que el SparkContext se inicie?

- Sí
- No
- **No**

**Explicación:**
No podemos agregar o configurar nuevas tareas de cálculo después de que el SparkContext se inicie.

Una vez que el SparkContext se inicializa y comienza a ejecutarse, representa el punto de entrada para interactuar con un clúster de Spark y coordinar la ejecución de las aplicaciones de Spark. Configura el entorno y la configuración para la aplicación de Spark, incluida la asignación de recursos, la programación de tareas y la comunicación con el clúster.

Cualquier configuración o cálculo que deba agregarse o configurarse debe hacerse antes de iniciar el SparkContext. Una vez que el SparkContext está en ejecución, no es posible modificar su configuración ni agregar nuevas tareas de cálculo de manera dinámica.

Si necesitas realizar cambios en el cálculo o la configuración, normalmente tendrías que detener el SparkContext y reiniciarlo con los cambios deseados.

## 10\. ¿Cuál es la abstracción de Apache Spark?

- Variable compartida (Shared Variable)
- **RDD**
- Ambos los anteriores

**Explicación:**
La abstracción de Apache Spark es el Resilient Distributed Dataset (RDD). RDD es una estructura de datos fundamental en Spark que representa una colección distribuida e inmutable de objetos. Los RDD proporcionan una forma tolerante a fallos y eficiente de realizar tareas de procesamiento de datos distribuidos en un clúster de máquinas.

Los RDD permiten transformaciones y acciones distribuidas en Spark, lo que permite a los usuarios realizar diversas operaciones, como filtrado, mapeo, reducción, unión y más, en conjuntos de datos grandes. Los RDD son resilientes porque se recuperan automáticamente de fallos de nodos y proporcionan tolerancia a fallos a través de la línea de linaje, lo que les permite ser reconstruidos en caso de fallos.

Las variables compartidas, por otro lado, son un mecanismo en Spark para compartir variables entre tareas o nodos en un entorno de computación distribuida. Si bien las variables compartidas son esenciales para ciertos cálculos en Spark, los RDD son la abstracción principal y la base para el procesamiento de datos en Apache Spark.

## 11\. ¿Cuáles son los parámetros definidos para especificar una operación de ventana?

- **Longitud de la ventana, intervalo deslizante (Window length, sliding interval)**
- Tamaño del estado, longitud de la ventana (State size, window length)
- Tamaño del estado, intervalo deslizante (State size, sliding interval)
- Ninguna de las anteriores

**Explicación:**
Los parámetros definidos para especificar una operación de ventana en Apache Spark son la longitud de la ventana (window length) y el intervalo deslizante (sliding interval).

Longitud de la ventana: Determina el tamaño o duración de la ventana, es decir, la cantidad de elementos incluidos en cada ventana. Especifica el rango de datos que se tendrá en cuenta en la operación de ventana.

Intervalo deslizante: Especifica el intervalo o tamaño del paso con el que la ventana se mueve o desliza sobre el flujo de datos. Determina con qué frecuencia se realiza la operación de ventana y el solapamiento entre ventanas consecutivas.

Al especificar estos dos parámetros, puedes definir el tamaño y el movimiento de la ventana para realizar cálculos o agregaciones en los datos de streaming.

La respuesta correcta es "Longitud de la ventana, intervalo deslizante" (Window length, sliding interval).

## 12. ¿Cuál de las siguientes operaciones no es una operación de salida en DStream?

- SaveAsTextFiles
- ForeachRDD
- SaveAsHadoopFiles
- **ReduceByKeyAndWindow**

**Explicación:**
"ReduceByKeyAndWindow" no es una operación de salida en DStream.

En Spark Streaming, DStream proporciona varias operaciones de salida que te permiten escribir o procesar los datos en el DStream.

"SaveAsTextFiles" es una operación de salida que guarda los datos del DStream en archivos de texto.

"ForeachRDD" es una operación de salida que te permite aplicar una función a cada RDD en el DStream. Esta función puede realizar un procesamiento personalizado o escribir los datos en sistemas externos.

"SaveAsHadoopFiles" es una operación de salida que guarda los datos del DStream en archivos de Hadoop utilizando la API más antigua de Hadoop.

Por otro lado, "ReduceByKeyAndWindow" no es una operación de salida. Es una operación de transformación que realiza una reducción en pares clave-valor dentro de una ventana deslizante.

La respuesta correcta es "ReduceByKeyAndWindow".


## 13. ¿En qué versión de Spark se introdujo Dataset?

- **Spark 1.6**
- Spark 1.4.0
- Spark 2.1.0
- Spark 1.1

La API de Dataset se introdujo en Spark 1.6. Fue una adición significativa a Spark, proporcionando una abstracción de nivel superior en comparación con los RDD (Resilient Distributed Datasets), al tiempo que ofrecía beneficios de tipado fuerte y optimización.

Antes de Spark 1.6, Spark principalmente proporcionaba RDDs como la abstracción central de datos para la computación distribuida. Sin embargo, la API de Dataset trajo una forma más estructurada y eficiente de trabajar con datos al combinar las mejores características de RDDs y DataFrames.

La respuesta correcta es "Spark 1.6".


## 14. Cluster Manager que soporta Spark:

- Standalone Cluster Manager
- MESOS
- YARN
- **Todos los anteriores**

Spark admite varios administradores de clústeres, incluyendo Standalone Cluster Manager, Mesos y YARN.

**Explicación:**

Spark es compatible con todos los administradores de clústeres mencionados:

- **Standalone Cluster Manager:** Spark tiene su propio administrador de clústeres independiente incorporado, que te permite implementar y gestionar aplicaciones de Spark en un clúster sin depender de ningún administrador de recursos externo.

- **Mesos:** Spark también se puede ejecutar en Apache Mesos, un administrador de clústeres de propósito general que proporciona aislamiento y uso compartido de recursos entre aplicaciones distribuidas.

- **YARN:** Spark puede integrarse con Apache Hadoop YARN (Yet Another Resource Negotiator), que es una tecnología de gestión de clústeres utilizada en el ecosistema de Hadoop. Las aplicaciones de Spark se pueden implementar y ejecutar en YARN, aprovechando sus capacidades de gestión de recursos.

La respuesta correcta es **Todos los anteriores**.

## 15. ¿Cuál es el nivel de almacenamiento predeterminado de `cache()`?

- **MEMORY_ONLY**
- MEMORY_AND_DISK
- DISK_ONLY
- MEMORY_ONLY_SER

**El nivel de almacenamiento predeterminado de la operación `cache()` en Apache Spark es MEMORY_ONLY.**

Cuando llamas a `cache()` en un DataFrame o RDD en Spark, se almacena en caché los datos en memoria para un acceso más rápido durante las operaciones posteriores. El nivel de almacenamiento predeterminado asegura que los datos se almacenen en memoria como objetos Java deserializados.

Sin embargo, es importante tener en cuenta que el nivel de almacenamiento predeterminado se puede cambiar modificando el parámetro de configuración `spark.storage.memoryFraction` en la configuración de Spark. Este parámetro determina la fracción del espacio del montón de Java asignado para la caché de almacenamiento de Spark.

Si deseas cambiar explícitamente el nivel de almacenamiento al almacenar en caché, puedes utilizar el método `persist()` y pasar el nivel de almacenamiento deseado como parámetro. Por ejemplo, puedes usar `persist(StorageLevel.DISK_ONLY)` para almacenar en caché los datos solo en disco.

Sin embargo, de forma predeterminada, sin especificar explícitamente el nivel de almacenamiento, los datos se almacenarán en caché en memoria utilizando el nivel de almacenamiento MEMORY_ONLY.

## 16. ¿Cuál de las siguientes opciones no es un componente que se encuentra encima de Spark Core?

- **Spark RDD**
- Spark Streaming
- MLlib
- Ninguna de las anteriores

## 17. ¿En qué año se lanzó Apache Spark como software de código abierto?

- **2010**
- 2011	 	
- 2008
- 2009

**Apache Spark se lanzó como software de código abierto en el año 2010.**

Inicialmente desarrollado en el AMPLab de la Universidad de California, Berkeley, Apache Spark se convirtió en un proyecto de código abierto bajo la supervisión de la Apache Software Foundation (ASF). Desde entonces, ha experimentado un crecimiento significativo y se ha convertido en uno de los proyectos de código abierto más populares y ampliamente utilizados en el campo del procesamiento y análisis de datos a gran escala.

## 18. Además de los trabajos de procesamiento de datos en streaming, ¿qué otras funcionalidades proporciona Spark?

- Aprendizaje automático (Machine Learning)
- Procesamiento de gráficos (Graph Processing)
- Procesamiento por lotes (Batch Processing)
- **Todas las anteriores**

Spark proporciona todas las funcionalidades mencionadas además de los trabajos de procesamiento de datos en streaming.

- Aprendizaje automático: Spark proporciona una biblioteca de aprendizaje automático llamada MLlib, que ofrece una amplia gama de algoritmos y herramientas de aprendizaje automático. Permite a los desarrolladores realizar diversas tareas, como clasificación, regresión, clustering, recomendación, y más, utilizando el procesamiento distribuido.

- Procesamiento de gráficos: Spark proporciona una biblioteca de procesamiento de gráficos llamada GraphX. Permite a los desarrolladores realizar cálculos y análisis de grafos, incluyendo algoritmos de grafos, consultas de grafos y visualización de grafos, en grafos a gran escala utilizando capacidades de procesamiento distribuido.

- Procesamiento por lotes: Spark es conocido por su capacidad de manejar eficientemente cargas de trabajo de procesamiento por lotes. Permite a los desarrolladores procesar grandes volúmenes de datos en paralelo utilizando RDDs y las APIs DataFrame/Dataset. Spark optimiza la ejecución de trabajos por lotes y proporciona un conjunto completo de transformaciones y acciones para la manipulación y análisis de datos.

La respuesta correcta es "Todas las anteriores".


## 19.- ¿Se incluye Spark en todas las distribuciones principales de Hadoop?

**Si**

NOTA: Para esta respuesta en todos lados encuentras que si, y en los examenes parece ser que se asume esa como la respuesta correcta pero también está otra respuesta que siento que sería la *real*:

No, Spark no se incluye en todas las distribuciones principales de Hadoop de forma predeterminada. Aunque Spark se puede integrar con Hadoop y ejecutarse en clústeres de Hadoop, no es un componente obligatorio de todas las distribuciones de Hadoop.

Las distribuciones de Hadoop suelen incluir los componentes principales del ecosistema de Hadoop, como el Sistema de Archivos Distribuidos de Hadoop (HDFS) y el framework de procesamiento MapReduce. Sin embargo, Spark es un proyecto independiente y separado de Hadoop, y debe instalarse y configurarse por separado en un clúster de Hadoop si se desea utilizar junto con Hadoop.

Dicho esto, **muchas distribuciones de Hadoop, como Cloudera, Hortonworks y MapR, proporcionan soporte integrado para Spark. Pueden ofrecer instalaciones preempaquetadas o brindar guías de integración para ayudar a los usuarios a configurar y ejecutar Spark en sus clústeres de Hadoop. Sin embargo, esto depende de la distribución específica de Hadoop y sus ofertas.**


## 20.- ¿Cuál de las siguientes afirmaciones no es cierta para Hadoop y Spark?

**Opciones:**
a) Ambos son plataformas de procesamiento de datos.
b) Ambos son entornos de cómputo distribuido.
**c) Ambos tienen su propio sistema de archivos.**
d) Ambos utilizan APIs de código abierto para vincular diferentes herramientas.

**Respuesta: c) Ambos tienen su propio sistema de archivos**

La afirmación "Ambos tienen su propio sistema de archivos" no es cierta para Hadoop y Spark.
 	
Hadoop y Spark son plataformas de procesamiento de datos y entornos de cómputo distribuido, pero difieren en términos de sus sistemas de archivos.

Hadoop, específicamente el ecosistema de Apache Hadoop, incluye el Sistema de Archivos Distribuidos de Hadoop (HDFS) como su capa de almacenamiento principal. HDFS es un sistema de archivos distribuido diseñado para almacenar y procesar grandes conjuntos de datos en un clúster de hardware económico. Proporciona tolerancia a fallos, alto rendimiento y escalabilidad.

Por otro lado, Spark no tiene su propio sistema de archivos dedicado. En cambio, está diseñado para ser compatible con varios sistemas de almacenamiento, incluyendo HDFS, Amazon S3, Azure Data Lake Storage, entre otros. Spark puede leer y procesar datos de diferentes sistemas de archivos y fuentes de datos, aprovechando sus optimizaciones y características específicas.

En cuanto a las opciones restantes:
a) Ambos son plataformas de procesamiento de datos: Esto es cierto para Hadoop y Spark.
b) Ambos son entornos de cómputo distribuido: Esto también es cierto para Hadoop y Spark.
d) Ambos utilizan APIs de código abierto para vincular diferentes herramientas: Esto también es cierto para Hadoop y Spark. Ambos proyectos proporcionan APIs de código abierto que permiten la integración con diversas herramientas y frameworks.

## 21.- ¿Cuánto más rápido puede ejecutar Apache Spark programas de procesamiento por lotes en memoria en comparación con MapReduce?

- 10 veces más rápido.
- 20 veces más rápido.
- **100 veces más rápido.**
- 200 veces más rápido.

**Respuesta: 100 veces más rápido.**

Apache Spark puede potencialmente ejecutar programas de procesamiento por lotes mucho más rápido en memoria en comparación con MapReduce. Si bien el rendimiento real depende de varios factores, en general, se reconoce que Spark es significativamente más rápido que MapReduce para el procesamiento en memoria.

La estimación común es que Apache Spark puede ser hasta 100 veces más rápido que MapReduce para programas de procesamiento por lotes cuando se ejecutan en memoria. Esta mejora de rendimiento sustancial se debe principalmente a la capacidad de Spark para almacenar en caché datos en memoria y realizar cálculos en memoria, evitando costosas operaciones de E/S en disco.

Es importante tener en cuenta que la ganancia de rendimiento puede variar según la carga de trabajo específica, el tamaño de los datos, la configuración del clúster y la eficiencia del programa de Spark en sí. Sin embargo, la capacidad de procesamiento en memoria de Spark es una de sus principales ventajas, lo que permite un procesamiento de datos más rápido y cálculos iterativos.

Por lo tanto, la respuesta correcta es 100 veces más rápido. Apache Spark puede ofrecer un aumento significativo de velocidad en comparación con MapReduce cuando se ejecutan programas de procesamiento por lotes en memoria.

## 22.- ¿Cuál de las siguientes opciones proporciona la capacidad de programación rápida de Spark Core para realizar análisis en tiempo real?

- RDD
- GraphX
- **Spark Streaming**
- Spark R

**Respuesta: Spark Streaming.**

Spark Streaming proporciona la capacidad de programación rápida a Spark Core para realizar análisis en tiempo real. Es una extensión de Spark Core diseñada específicamente para procesar y analizar datos de transmisión en tiempo real.

RDD (Resilient Distributed Datasets) es la abstracción de datos principal en Spark, que representa colecciones distribuidas de objetos que se pueden procesar en paralelo. Los RDD se utilizan en Spark Streaming como la estructura de datos subyacente para procesar datos de transmisión, pero no proporcionan directamente la capacidad de programación rápida.

GraphX es una biblioteca de procesamiento de gráficos en Spark que permite realizar cálculos de gráficos. Si bien es un componente construido sobre Spark Core, no está directamente relacionado con la capacidad de programación rápida para el análisis en tiempo real.

Spark R es un paquete de R que proporciona una interfaz para ejecutar cálculos de Spark utilizando el lenguaje de programación R. Si bien permite usar Spark con R, no es responsable de manera específica de la capacidad de programación rápida en Spark Core para el análisis en tiempo real.

La opción correcta es "Spark Streaming". Proporciona la funcionalidad necesaria y las capacidades de programación rápida dentro de Spark Core para realizar análisis en tiempo real en datos de transmisión.

## 23.- ¿Cuál de las siguientes opciones es la razón por la cual Spark es más rápido que MapReduce?

- Soporte para diferentes APIs de lenguaje como Scala, Java, Python y R
- Los RDD son inmutables y tolerantes a fallos
- **Ninguna de las anteriores**

**Respuesta: Ninguna de las anteriores.**

Si bien ambas opciones mencionadas son características de Apache Spark, no son las razones específicas por las cuales Spark es más rápido que MapReduce.

La razón principal por la cual Spark es más rápido y tiene un mejor rendimiento que MapReduce es su capacidad de procesamiento en memoria. A diferencia de MapReduce, que depende en gran medida de la E/S de disco para el almacenamiento y recuperación de datos, Spark utiliza RDDs (Resilient Distributed Datasets) para almacenar en caché datos en memoria y realizar cálculos en memoria.

Al mantener los datos en memoria, Spark evita la sobrecarga de operaciones frecuentes de lectura y escritura en disco, lo que se traduce en tiempos de procesamiento significativamente más rápidos. Además, Spark optimiza la ejecución de operaciones mediante la habilitación de la canalización de datos y la evaluación perezosa, minimizando la transferencia de datos y mejorando la eficiencia general.

Si bien el soporte de Spark para diferentes APIs de lenguaje y la inmutabilidad y tolerancia a fallos de los RDDs son características importantes que contribuyen a su versatilidad y confiabilidad, NO son los principales factores que hacen que Spark sea más rápido que MapReduce.

La respuesta correcta es "Ninguna de las anteriores". La razón principal por la cual Spark es rápido en comparación con MapReduce es su capacidad de procesamiento en memoria.


## 24.- ¿Es posible combinar las bibliotecas de Apache Spark en la misma aplicación, por ejemplo, MLlib, GraphX, SQL y DataFrames, etc.?

- **Sí**
- No

**Respuesta: Sí**, puedes combinar múltiples bibliotecas de Apache Spark en la misma aplicación. Spark está diseñado como un motor de análisis unificado, que proporciona diversas bibliotecas y APIs que se pueden utilizar juntas en una sola aplicación.

Puedes combinar bibliotecas como MLlib (Biblioteca de Aprendizaje Automático), GraphX (Biblioteca de Procesamiento de Gráficos), Spark SQL y DataFrames en la misma aplicación de Spark. Esto te permite realizar una amplia gama de procesamiento de datos, análisis y tareas de aprendizaje automático utilizando un único marco de trabajo.

Puedes utilizar Spark SQL y DataFrames para consultas y manipulación de datos estructurados, MLlib para entrenar y evaluar modelos de aprendizaje automático, y GraphX para realizar cálculos y análisis de gráficos. Al combinar estas bibliotecas, puedes aprovechar las capacidades de Spark para procesar diferentes tipos de datos y realizar diversas tareas analíticas dentro de la misma aplicación.

## 25.- ¿Cuál de las siguientes afirmaciones es verdadera para RDD?

- RDD es un paradigma de programación.
- **RDD en Apache Spark es una colección inmutable de objetos**.
- Es una base de datos. 	
- Ninguna de las anteriores.

**Respuesta: "RDD en Apache Spark es una colección inmutable de objetos"** es verdadero para RDD (Resilient Distributed Dataset).

Un RDD es una colección distribuida e inmutable de objetos en Apache Spark. Representa una abstracción de datos fundamental en Spark y sirve como la estructura de datos principal para tareas de procesamiento de datos. Los RDD están diseñados para ser tolerantes a fallos y pueden procesarse en paralelo en un clúster de máquinas.

Los RDD son inmutables, lo que significa que una vez creados, no pueden modificarse. En cambio, las transformaciones de RDD crean nuevos RDD como resultado de las operaciones de transformación. Esta inmutabilidad garantiza la tolerancia a fallos y la consistencia de los datos en los cálculos distribuidos.

RDD no es un paradigma de programación ni una base de datos; es una estructura de datos fundamental en Spark que proporciona capacidades de procesamiento distribuido, inmutabilidad y tolerancia a fallos.


## 26.- ¿Cuál de las siguientes opciones no es una función de Spark Context en Apache Spark?

- **Punto de entrada a Spark SQL**.
- Acceder a varios servicios.
- Establecer la configuración.
- Obtener el estado actual de la aplicación Spark.

La función "Punto de entrada a Spark SQL" no es una función directa de Spark Context en Apache Spark.

Spark Context es el punto de entrada principal y el fundamento de la aplicación Spark. Proporciona la conexión al clúster de Spark y coordina la ejecución de tareas. Sin embargo, Spark Context en sí mismo no sirve directamente como punto de entrada a Spark SQL.

Para usar Spark SQL, es necesario crear un SQLContext o SparkSession separado, que proporciona una interfaz de programación para trabajar con datos estructurados y semiestructurados mediante consultas similares a SQL y la API de DataFrame. Por lo general, el SQLContext o SparkSession se crea utilizando Spark Context como base.

Las funciones de Spark Context incluyen:

- Acceder a varios servicios: Spark Context proporciona acceso a varios servicios y APIs dentro de Spark, incluyendo Spark Streaming, Spark SQL, MLlib, GraphX, y más.

- Establecer la configuración: Spark Context te permite establecer varias opciones de configuración para tu aplicación Spark, como el número de ejecutores, asignación de memoria, niveles de registro y otras configuraciones en tiempo de ejecución.

- Obtener el estado actual de la aplicación Spark: Spark Context proporciona información sobre el estado actual de la aplicación Spark, incluyendo el progreso del trabajo, etapas y detalles de ejecución de tareas.

La opción correcta es "Punto de entrada a Spark SQL". Spark Context sirve como el punto de entrada para las aplicaciones Spark y proporciona funciones relacionadas con el acceso a servicios, establecimiento de configuraciones y obtención del estado de la aplicación. Sin embargo, la funcionalidad de Spark SQL se accede a través de un objeto SQLContext o SparkSession separado.

**EJEMPLO:**

```scala
import org.apache.spark.SparkContext
import org.apache.spark.sql.{SparkSession, DataFrame}

// Creando un nuevo SparkContext
val sc = new SparkContext("local[*]", "MiAplicacionSpark")

// Creando un SparkSession usando el SparkContext
val spark = SparkSession.builder().appName("MiAplicacionSpark").getOrCreate()

// Leyendo datos desde un archivo Parquet en un DataFrame
val data_df: DataFrame = spark.read.parquet("ruta/al/archivo.parquet")

// Realizando algunas operaciones en el DataFrame
val resultado: DataFrame = data_df.filter($"edad" > 30).groupBy("genero").count()

// Mostrando el resultado
resultado.show()

// Deteniendo el SparkContext
sc.stop()
```

## 27.- ¿Cuáles son las características de Spark RDD?

- Computación en memoria.
- Evaluaciones perezosas.
- Tolerancia a fallos.
- **Todas las anteriores**.

Todas las opciones anteriores son características de Spark RDD (Resilient Distributed Dataset).

- **Computación en memoria:** RDD permite almacenar datos en memoria, lo que permite un procesamiento más rápido al reducir las operaciones de E/S en disco.

- **Evaluaciones perezosas:** RDD admite evaluaciones perezosas, lo que significa que las transformaciones en los RDD no se ejecutan de inmediato. En cambio, las transformaciones se registran y se ejecutan solo cuando se realiza una acción, lo que permite planes de ejecución optimizados.

- **Tolerancia a fallos:** Los RDD están diseñados para ser tolerantes a fallos. Registran información de linaje, lo que les permite recuperar particiones de datos perdidas en caso de fallos.

Por lo tanto, todas estas características hacen que los RDD sean una abstracción poderosa en Spark para el procesamiento distribuido de datos.


## 28.- ¿Cuántos Spark Context pueden estar activos por JVM?

- Más de uno.
- **Solo uno**.
- No específico.
- Ninguna de las anteriores.

En Apache Spark, solo puede haber un SparkContext activo por JVM. Intentar crear múltiples instancias de SparkContext en la misma JVM puede provocar conflictos y comportamientos inesperados. SparkContext es el punto de entrada para interactuar con la funcionalidad de Spark y representa la conexión a un clúster de Spark. Administra los recursos y configuraciones subyacentes necesarios para las aplicaciones de Spark.


## 29.- ¿De cuántas formas se puede crear un RDD?

- 4
- 3
- **2**
- 1

**Esta respuesta es ambigua porque en muchos lados aparece que hay dos otros que en tres, pero la documentación solo menciona dos, cual será la verdad verdadera para los que aplican la prueba?**

![411bccd046e59fd78fa45ffeeaba8c23.png](:/ccaf2afe7ccd49bdab2b666a8d52431b)

Un RDD (Resilient Distributed Dataset) se puede crear de dos formas:

1. Paralelizando una colección existente: Los RDD se pueden crear paralelizando una colección existente en el programa controlador (driver program). Esto implica distribuir la colección en el clúster y crear particiones de datos.

2. Cargando conjuntos de datos externos: Los RDD también se pueden crear cargando datos desde sistemas de almacenamiento externos como Hadoop Distributed File System (HDFS), sistemas de archivos locales o cualquier fuente de datos compatible con los InputFormats de Hadoop.


## 30.- ¿Cuántas tareas ejecuta Spark en cada partición?

- Cualquier número de tareas
- **Una**
- Más de una pero menos de cinco

Por defecto, Spark ejecuta una tarea por partición. Cada partición de un RDD es procesada por una única tarea. Sin embargo, es importante tener en cuenta que el número de tareas se puede configurar y ajustar en función de factores como la configuración del clúster, los recursos disponibles y las operaciones específicas que se realicen. Al especificar el número de particiones o utilizar operaciones como repartition() o coalesce(), se puede aumentar o disminuir el número de tareas. Por lo tanto, aunque el valor predeterminado es una tarea por partición, es posible tener más de una tarea por partición dependiendo de la configuración y los requisitos de la aplicación de Spark.

## 31.- ¿Podemos editar los datos de un RDD, por ejemplo, cambiar el formato del texto?

- Sí
- **No**

No, no podemos editar directamente los datos de un RDD en Apache Spark. Los RDD son inmutables, lo que significa que no se pueden modificar una vez creados. Sin embargo, podemos aplicar transformaciones a los RDD para crear nuevos RDD con modificaciones u operaciones deseadas.

Cambiar el formato del texto, como cambiar el caso (mayúsculas o minúsculas) de los caracteres en una cadena, se considera una modificación de los datos. Por ejemplo, convertir "Hola" a "hola" o "MUNDO" a "mundo". Esto requeriría aplicar una transformación específica al RDD, como map(), para crear un nuevo RDD con los datos modificados.
