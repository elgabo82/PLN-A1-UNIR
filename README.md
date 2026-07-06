# PLN-A1-UNIR

Repositorio correspondiente a la Actividad 1 de la asignatura **Procesamiento del Lenguaje Natural**, del **Máster Universitario en Inteligencia Artificial** de la **Universidad Internacional de La Rioja (UNIR)**.

El trabajo desarrolla un proceso de **caracterización de textos** mediante técnicas básicas de PLN, utilizando principalmente la librería **spaCy** para el procesamiento automático de comentarios en español.

## Autor

**Gabriel Morejón López**
Fecha de elaboración: **05-07-2026**

## Descripción del proyecto

Este repositorio contiene un notebook de Google Colab/Jupyter en el que se realiza el análisis de un corpus textual con el objetivo de extraer características lingüísticas relevantes. La actividad permite familiarizarse con el manejo de modelos de lenguaje, tokenización, análisis morfosintáctico y extracción de rasgos textuales útiles para tareas posteriores de clasificación.

El ejercicio se centra en el procesamiento automático de textos para identificar características básicas del lenguaje y analizar posibles diferencias entre comentarios asociados a distintos niveles de intensidad.

## Objetivos

* Cargar y preprocesar un corpus textual en español.
* Utilizar modelos de lenguaje de **spaCy** para procesar comentarios.
* Aplicar técnicas básicas de **Procesamiento del Lenguaje Natural**.
* Extraer características lingüísticas y estilísticas de los textos.
* Analizar diferencias entre grupos de comentarios.
* Reflexionar sobre la utilidad de las características extraídas para tareas de clasificación.

## Contenido del repositorio

```text
PLN-A1-UNIR/
│
├── README.md
└── caracteristicasOdio_Gabriel_Morejón.ipynb
```

## Notebook principal

El archivo principal del repositorio es:

```text
caracteristicasOdio_Gabriel_Morejón.ipynb
```

Este notebook incluye:

* Instalación y carga de librerías necesarias.
* Carga del dataset de comentarios.
* Preprocesamiento del texto.
* Tokenización con spaCy.
* Análisis de registros del corpus.
* Extracción de características lingüísticas.
* Comparación entre grupos de comentarios.
* Reflexión final sobre la capacidad discriminatoria de las variables extraídas.

## Tecnologías utilizadas

* Python 3
* Google Colab / Jupyter Notebook
* spaCy
* pandas
* Modelos de spaCy para español:

  * `es_core_news_sm`
  * `es_core_news_md`

## Requisitos

Para ejecutar el notebook en un entorno local, se recomienda tener instalado Python 3.10 o superior.

Instalar las dependencias principales:

```bash
pip install pandas spacy
python -m spacy download es_core_news_sm
python -m spacy download es_core_news_md
```

En caso de mantener la importación del modelo en inglés incluida en el notebook, también puede instalarse:

```bash
python -m spacy download en_core_web_sm
```

## Dataset

El notebook espera trabajar con un archivo CSV denominado:

```text
02Dataset_anonimizado.csv
```

Este archivo debe ubicarse en la raíz del proyecto o en la ruta indicada dentro del notebook.

El dataset utilizado contiene comentarios textuales y una variable de intensidad. Las columnas principales utilizadas son:

```text
CONTENIDO A ANALIZAR
INTENSIDAD
```

## Ejecución en Google Colab

El notebook está preparado para ejecutarse en Google Colab. Para utilizarlo:

1. Abrir el archivo `caracteristicasOdio_Gabriel_Morejón.ipynb`.
2. Ejecutar las celdas iniciales de instalación de dependencias.
3. Subir o disponer del archivo `02Dataset_anonimizado.csv`.
4. Ejecutar las celdas de carga, preprocesamiento y análisis.
5. Revisar las respuestas y resultados obtenidos en cada pregunta.

También puede abrirse directamente desde Colab con el siguiente enlace:

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elgabo82/PLN-A1-UNIR/blob/main/caracteristicasOdio_Gabriel_Morej%C3%B3n.ipynb)

## Principales tareas desarrolladas

El trabajo realiza, entre otras, las siguientes acciones:

* Lectura del corpus textual desde un archivo CSV.
* Selección de las columnas necesarias para el análisis.
* Conversión del contenido textual a formato procesable.
* Carga del modelo `es_core_news_md` de spaCy.
* Procesamiento de los comentarios mediante el objeto `nlp`.
* Creación de listas de documentos procesados y valores de intensidad.
* Cálculo del número de registros del corpus.
* Cálculo de características textuales y lingüísticas.
* Comparación de características entre comentarios clasificados como odio y no odio.
* Reflexión sobre la utilidad de las características como entrada para futuros modelos de clasificación.

## Características analizadas

Entre las características trabajadas en el notebook se incluyen:

* Número de registros del corpus.
* Promedio de palabras por comentario.
* Densidad de signos de exclamación e interrogación.
* Proporción de tokens en mayúsculas.
* Densidad de adjetivos.
* Riqueza léxica mediante Type-Token Ratio sobre lemas.
* Comparación estadística entre grupos de comentarios.

## Estructura general del análisis

El desarrollo del notebook sigue la siguiente secuencia:

1. **Carga de librerías**
   Se importan las librerías necesarias para el procesamiento textual y el análisis de datos.

2. **Carga del modelo de lenguaje**
   Se utiliza un modelo de spaCy entrenado para español.

3. **Lectura del dataset**
   Se carga el archivo CSV con los comentarios y sus valores de intensidad.

4. **Preprocesamiento**
   Se convierten los textos a formato cadena y se preparan para ser procesados.

5. **Tokenización y análisis lingüístico**
   Cada comentario se procesa mediante spaCy para obtener tokens, lemas, categorías gramaticales y otros atributos.

6. **Extracción de características**
   Se calculan variables lingüísticas y estilísticas que permiten describir el corpus.

7. **Comparación de grupos**
   Se analizan diferencias entre comentarios de odio y no odio.

8. **Reflexión final**
   Se valora la utilidad de las características extraídas para tareas posteriores de clasificación automática.

## Posibles mejoras futuras

* Incorporar visualizaciones gráficas de las características extraídas.
* Añadir un archivo `requirements.txt` con las dependencias del proyecto.
* Incluir pruebas con otros modelos de spaCy.
* Aplicar técnicas de vectorización como TF-IDF o embeddings.
* Entrenar modelos de clasificación supervisada.
* Evaluar métricas como accuracy, precision, recall y F1-score.
* Documentar el origen del dataset y sus condiciones de uso.
* Separar el código en módulos reutilizables de Python.

## Licencia

Este repositorio tiene fines académicos. En caso de reutilización, se recomienda citar adecuadamente el trabajo y respetar las condiciones de uso del dataset empleado.

## Referencias útiles

* Documentación de spaCy: https://spacy.io/
* Modelos de spaCy para español: https://spacy.io/models/es
* Documentación de pandas: https://pandas.pydata.org/docs/
* Google Colab: https://colab.research.google.com/
