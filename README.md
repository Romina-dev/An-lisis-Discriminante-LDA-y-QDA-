# Comparación de LDA y QDA con Wine Dataset

## Descripción del proyecto

Este proyecto corresponde a la tarea **U4_S14: Análisis Discriminante Lineal (LDA) y Análisis Discriminante Cuadrático (QDA)**. El objetivo es comparar el desempeño de ambos modelos de clasificación usando el **Wine Dataset** de `scikit-learn`.

El trabajo utiliza el dataset sin tratamiento de limpieza adicional, es decir, no se eliminaron datos, no se imputaron valores faltantes, no se quitaron valores atípicos y no se aplicó normalización o estandarización al modelo principal. La única preparación realizada fue la separación de los datos en entrenamiento y prueba, usando partición estratificada para conservar la proporción de clases.

## Archivos del repositorio

El repositorio contiene los siguientes archivos:

- `U4_S14_Tarea_Análisis_Discriminante_(LDA_y_QDA).ipynb`: notebook principal con el desarrollo completo.
- `wine_dataset.csv`: conjunto de datos utilizado en formato CSV.
- `README.md`: archivo explicativo del proyecto, instrucciones de ejecución y resumen de hallazgos.

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

## Requisitos para ejecutar el proyecto

El notebook puede ejecutarse directamente en Google Colab.

Librerías utilizadas:

```python
numpy
pandas
matplotlib
seaborn
scikit-learn

Auror: Romina Salomé Vera Narváez
