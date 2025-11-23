# suicide-mental-health-analysis
# Análisis de Datos: Salud Mental y Tasas de Suicidio

Este repositorio contiene el desarrollo de una exploración de datos basada en el dataset “Global Suicide, Mental Health & Substance Use Disorders” disponible en Kaggle. El propósito principal es aplicar los conceptos aprendidos sobre problemas de **regresión** y **clasificación**, utilizando una variable numérica continua (tasa de suicidios) y una versión categorizada de la misma variable.

El proyecto se centra en comprender el comportamiento de los datos, identificar una posible variable objetivo y evaluar cómo el tipo de variable determina el enfoque metodológico.

---

## 1. Introducción

Las tasas de suicidio representan un indicador crítico de salud pública a nivel mundial. Su análisis permite identificar patrones poblacionales y puede servir como base para estudios predictivos orientados a medir niveles de riesgo. A partir de este contexto, el presente análisis utiliza un dataset global con información relacionada a tasas de suicidio y enfermedades crónicas para evaluar cómo estos datos pueden abordarse desde dos perspectivas fundamentales del análisis predictivo:

- **Regresión**, cuando la variable objetivo es numérica continua.
- **Clasificación**, cuando la variable objetivo se convierte en categorías o clases.

Este ejercicio permite comparar ambos enfoques utilizando un mismo conjunto de datos y comprender cómo la naturaleza de la variable objetivo define el tipo de problema.

---

## 2. Dataset Utilizado

- **Fuente:** Kaggle  
- **Nombre del dataset:** Global Suicide, Mental Health & Substance Use Disorders  
- **Formato original:** Dos archivos CSV  
  - `crude suicide rates.csv`
  - `share-with-alcohol-and-substance-use-disorders 1990-2016.csv`

Para este análisis, se trabajó principalmente con el archivo relacionado a tasas de suicidio.

### Variables Principales

Luego de la limpieza y renombrado de columnas, se identificaron las siguientes variables relevantes:

- `tasa_suicidios_total`: tasa de suicidios por cada 100 000 habitantes (variable objetivo numérica).
- `prob_muerte_cronica_total`: probabilidad de muerte por enfermedades crónicas.
- `prob_muerte_cronica_hombres`: probabilidad en población masculina.
- `prob_muerte_cronica_mujeres`: probabilidad en población femenina.

Adicionalmente, se eliminaron columnas consideradas irrelevantes para el análisis (`id0`, `id1`).

---

## 3. Objetivo del Análisis

**Objetivo General**
- Analizar la variable relacionada a la tasa de suicidios y determinar de qué manera el problema puede abordarse como regresión y como clasificación.

**Objetivos Específicos**
1. Limpiar y preparar el dataset para análisis.
2. Identificar la variable objetivo y determinar su naturaleza.
3. Crear una versión categórica de la tasa de suicidios.
4. Generar análisis univariante y bivariante desde ambos enfoques.
5. Reflexionar sobre las diferencias prácticas entre clasificación y regresión.

---

## 4. Metodología

### 4.1 Limpieza y Renombrado
Las columnas originales presentaban nombres extensos y repetidos. Se asignaron nombres más claros y se eliminaron columnas sin utilidad analítica. La variable objetivo fue convertida a formato numérico, ya que inicialmente se encontraba como texto.

### 4.2 Enfoque de Regresión
Se trabajó con la variable continua `tasa_suicidios_total`, realizando:
- Estadísticos descriptivos
- Histogramas
- Gráficos de dispersión frente a otras variables numéricas

Este enfoque permite plantear la predicción de un valor real (la tasa de suicidios).

### 4.3 Enfoque de Clasificación
La variable continua fue transformada en una variable categórica mediante cuantiles, generando la columna:

- `nivel_tasa_suicidio` = baja, media, alta

Esto permite reformular el problema como clasificación, es decir, asignación de registros a clases.

### 4.4 Análisis Bivariante
- **Regresión:** Scatterplots entre la tasa total y otras variables numéricas.
- **Clasificación:** Boxplots comparando variables numéricas entre las categorías definidas.

---

## 5. Resultados Relevantes

- La variable `tasa_suicidios_total` se comporta como una variable numérica continua, por lo que el planteamiento natural del problema corresponde a **regresión**.
- La transformación a categorías permitió construir un segundo enfoque basado en **clasificación**, sin necesidad de modificar el dataset original.
- Las distribuciones muestran diferencias entre los grupos definidos, lo que indica que ambas metodologías pueden aportar información útil sobre los datos.
- La naturaleza de la variable objetivo determinó el enfoque a aplicar, lo que refuerza el criterio metodológico trabajado académicamente.

---

## 6. Conclusiones

El análisis demuestra que un mismo dataset puede ser abordado desde distintos enfoques dependiendo de la forma en que se defina la variable objetivo. Cuando la tasa de suicidios se analiza como un valor continuo, se plantea un problema de **regresión**, orientado a predecir una cifra específica. En cambio, al convertir esta variable en categorías, el problema se transforma en uno de **clasificación**, centrado en determinar a qué grupo pertenece cada observación.

Este ejercicio confirma que la distinción entre regresión y clasificación no depende del dataset en sí, sino del tipo y formato de la variable que se desea predecir.

---

## 7. Archivos del Repositorio

Analisis_salud_mental_suicidio.ipynb 
# Notebook con el análisis completo
suicide_processed.csv 
# Dataset procesado con variable categórica
README.md 
# Documentación del proyecto


---

## 8. Propósito Académico

Este trabajo se realizó con fines educativos, como ejercicio de exploración y preparación de datos aplicado al estudio de los conceptos de regresión y clasificación dentro del análisis predictivo.


