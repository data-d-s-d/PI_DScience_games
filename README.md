<img src="https://c4.wallpaperflare.com/wallpaper/577/286/481/steam-logo-hd-wallpaper-preview.jpg" alt="Logo de Steam" width="800">
# Proyecto Individual Machine Learning Operations Steam Games
# Índice
1. [Descripción del Proyecto](#descripcion-del-proyecto)
2. [Resumen del Proceso](#resumen-del-proceso)
   - [Adquisición y Limpieza de Datos](#adquisicion-y-limpieza-de-datos)
   - [Ingeniería de Características](#ingenieria-de-caracteristicas)
   - [Desarrollo de la API](#desarrollo-de-la-api)
   - [Implementación](#implementacion)
   - [Análisis Exploratorio de Datos (EDA)](#analisis-exploratorio-de-datos-eda)
   - [Modelo de Aprendizaje Automático](#modelo-de-aprendizaje-automatico)
   - [Presentación en Video](#presentacion-en-video)
3. [Criterios de Evaluación del Proyecto](#criterios-de-evaluacion-del-proyecto)
4. [Video de Presentación](#video-de-presentacion)
5. [Conclusión](#conclusion)
# README del Proyecto MVP - Análisis y Recomendación de Juegos <a name="descripcion-del-proyecto"></a>

## Descripción del Proyecto

Este proyecto está orientado al análisis y recomendación de juegos. 
El objetivo principal es abordar el procesamiento de datos relacionados con juegos a través de la lectura, limpieza y disponibilidad 
de estos datos a través de una API, así como desarrollar un sistema de recomendación basado en aprendizaje automático.

## Resumen del Proceso <a name="resumen-del-proceso"></a>

El proyecto se ha desarrollado en varias etapas clave:

### 1. Adquisición y Limpieza de Datos <a name="adquisicion-y-limpieza-de-datos"></a>

En esta fase, se trabajó con tres archivos JSON que contenían datos relacionados con juegos. Se llevaron a cabo las siguientes acciones:

- Descompresión de los archivos JSON.gzip
- Importación de los datos en Python utilizando dataframes (pandas).
- Limpieza de los datos, incluyendo la eliminación de columnas innecesarias y la preparación de los datos para su análisis posterior.

### 2. Ingeniería de Características <a name="ingenieria-de-caracteristicas"></a>

El proyecto incluyó la creación de una nueva característica llamada 'sentiment_analysis' mediante el análisis de sentimiento basado en procesamiento 
de lenguaje natural (NLP) aplicado a las reseñas de los usuarios. Esta característica asigna valores '0' para sentimiento negativo,
'1' para sentimiento neutral y '2' para sentimiento positivo. Además, esta nueva característica reemplaza la columna 'user_reviews.review' 
para facilitar el análisis de datos y el uso en modelos de aprendizaje automático.

### 3. Desarrollo de la API <a name="desarrollo-de-la-api"></a>

Se implementó una API utilizando el marco FastAPI para proporcionar acceso a los datos procesados. 
Se crearon los siguientes endpoints con los decoradores adecuados (@app.get('/')):

- developer: Devuelve la cantidad de elementos y el porcentaje de contenido gratuito por año para un desarrollador específico.
- userdata: Proporciona información sobre un usuario, incluyendo el dinero gastado, el porcentaje de recomendación basado en reseñas y la cantidad de elementos.
- UserForGenre: Ofrece el usuario con más horas jugadas para un género específico y una lista de horas jugadas por año de lanzamiento.
- best_developer_year: Devuelve los 3 mejores desarrolladores con los juegos más recomendados por los usuarios para un año determinado.
- developer_reviews_analysis: Proporciona un diccionario con el número total de reseñas de usuarios categorizadas como positivas y negativas para un desarrollador específico.

### 4. Implementación

La API desarrollada se implementó en la plataforma Render, para que sea accesible a través de un browser.

### 5. Análisis Exploratorio de Datos (EDA)
Se realizó un Análisis Exploratorio de Datos manual para explorar relaciones, detectar valores atípicos o anomalías, y descubrir patrones interesantes en los datos. Además, se crearon nubes de palabras para visualizar las palabras más frecuentes en los títulos de los juegos, entre otras visualizaciones.

### 6. Modelo de Aprendizaje Automático
Se construyó un sistema de recomendación basado en aprendizaje automático. Pudimos elegir entre un sistema de recomendación de ítem-ítem o de usuario-ítem. Decidí realizar la primera opción:
recomendacion_juego: Dado un ID de producto, devuelve una lista de 5 juegos similares.

### 7. Presentación en Video
Se creó una presentación en video para demostrar el funcionamiento de los puntos finales de la API y proporcionar una breve descripción del modelo de aprendizaje automático utilizado para las recomendaciones.

## Criterios de Evaluación del Proyecto <a name="criterios-de-evaluacion-del-proyecto"></a>

El proyecto se evaluará según los siguientes criterios:

- Calidad y organización del código, incluyendo el uso de funciones y clases cuando sea necesario.
- Nomenclatura adecuada de archivos y organización del repositorio.
- Un README bien documentado que proporcione una descripción completa del proyecto y un resumen de los pasos clave.
- Cumplimiento de los requisitos del proyecto según lo especificado en la propuesta inicial.
- Implementación exitosa de la API en una plataforma de alojamiento.
- Efectiva implementación del Análisis Exploratorio de Datos.
- Creación de un sistema de recomendación de aprendizaje automático funcional.
- Presentación de resultados en un video, con explicaciones claras de la funcionalidad de la API y los modelos de aprendizaje automático.

## Video de Presentación <a name="video-de-presentacion"></a>

- El video debe mostrar los puntos finales de la API en funcionamiento y proporcionar una breve descripción del modelo de aprendizaje automático utilizado para las recomendaciones. El video debe tener una duración máxima de 7 minutos.

## Conclusión <a name="conclusion"></a>
- Presentación de resultados en un video, con explicaciones claras de la funcionalidad de la API y los modelos de aprendizaje automático.
- Video de Presentación
- El video debe mostrar los puntos finales de la API en funcionamiento y proporcionar una breve descripción del modelo de aprendizaje automático utilizado para las recomendaciones. El video debe tener una duración máxima de 7 minutos.

Conclusión:
