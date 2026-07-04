# Comparación de LDA y QDA con Wine Dataset

## Descripción del proyecto

Este proyecto corresponde a la tarea **U4_S14: Análisis Discriminante Lineal (LDA) y Análisis Discriminante Cuadrático (QDA)**. El objetivo es comparar el desempeño de ambos modelos de clasificación usando el **Wine Dataset** de `scikit-learn`.

El trabajo utiliza el dataset sin tratamiento de limpieza adicional, es decir, no se eliminaron datos, no se imputaron valores faltantes, no se quitaron valores atípicos y no se aplicó normalización o estandarización al modelo principal. La única preparación realizada fue la separación de los datos en entrenamiento y prueba, usando partición estratificada para conservar la proporción de clases.

## Archivos del repositorio

El repositorio contiene los siguientes archivos:

- `U4_S14_Tarea_Análisis_Discriminante_(LDA_y_QDA).ipynb`: notebook principal con el desarrollo completo.
- `wine_dataset.csv`: conjunto de datos utilizado en formato CSV.

## Dataset utilizado

Se utilizó el **Wine Dataset**, disponible en la librería `scikit-learn` mediante `load_wine()`.

Características principales:

- Número de observaciones: 178
- Número de variables predictoras: 13
- Variable objetivo: `target`
- Número de clases: 3
- Tipo de problema: clasificación multiclase

## Modelos implementados

### 1. Análisis Discriminante Lineal (LDA)

Se utilizó `LinearDiscriminantAnalysis` de `sklearn.discriminant_analysis`. Este modelo asume que las clases comparten una misma matriz de covarianza, por eso genera fronteras de decisión lineales.

### 2. Análisis Discriminante Cuadrático (QDA)

Se utilizó `QuadraticDiscriminantAnalysis` de `sklearn.discriminant_analysis`. Este modelo permite que cada clase tenga su propia matriz de covarianza, por eso puede generar fronteras cuadráticas o más flexibles.

## Estructura del notebook

El notebook está organizado según las secciones solicitadas:

1. Descripción del conjunto de datos
2. Exploración de los datos
3. Visualización
4. Preparación de los datos
5. Implementación de LDA
6. Implementación de QDA
7. Comparación de modelos
8. Fronteras de decisión
9. Conclusiones

### Autor: Romina Salomé Vera Narváez

## Requisitos para ejecutar el proyecto

1. Ingresar a Google Colab.
2. Subir el archivo:

   `U4_S14_Tarea_Análisis_Discriminante_(LDA_y_QDA).ipynb`

3. Ejecutar las celdas en orden, desde la primera hasta la última.
4. Revisar las salidas generadas: tablas, visualizaciones, matrices de confusión, métricas y fronteras de decisión.

En Google Colab no es necesario instalar librerías manualmente, ya que normalmente las librerías utilizadas ya están disponibles.

### Opción 2: Ejecutar en entorno local

1. Clonar el repositorio:

```bash
git clone https://github.com/Romina-dev/An-lisis-Discriminante-LDA-y-QDA-/edit/main/README.md
```
2. Ingresar a la carpeta del proyecto:
```bash
cd An-lisis-Discriminante-LDA-y-QDA-
```

3. Instalar las librerías necesarias:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

4. Abrir Jupyter Notebook:
```bash
jupyter notebook
```
5. Ejecutar el archivo:
U4_S14_Tarea_Análisis_Discriminante_(LDA_y_QDA).ipynb

Librerías utilizadas:

```python
numpy
pandas
matplotlib
seaborn
scikit-learn
```

## Preparación de los datos

La preparación consistió en separar el dataset en entrenamiento y prueba.

Se utilizó una partición estratificada con stratify=y para conservar la proporción de las tres clases tanto en el conjunto de entrenamiento como en el conjunto de prueba.

No se aplicó normalización ni estandarización, debido a que la consigna indica usar el Wine Dataset sin tratamiento.

## Métricas de evaluación

Para comparar los modelos se utilizaron las siguientes métricas:

- Accuracy.
- Precision macro.
- Recall macro.
- F1-score macro.
- Matriz de confusión.
- Tiempo de entrenamiento.
