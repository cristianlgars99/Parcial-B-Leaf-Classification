📘 README — Proyecto de Clasificación de Especies de Árboles
📌 Descripción del Proyecto

Este proyecto desarrolla un sistema de clasificación de especies de árboles utilizando características numéricas extraídas de imágenes de hojas (márgenes, texturas y formas).
Se aplica un flujo completo de Machine Learning: exploración, preprocesamiento, entrenamiento, selección de características, evaluación y comparativa de múltiples modelos.

El objetivo final es predecir correctamente la especie de una hoja a partir de sus descriptores numéricos.

📁 Contenido del Notebook

El archivo incluye los siguientes módulos:

1. Carga y Exploración de Datos

Lectura del dataset original con pandas.

Inspección inicial: columnas, tipos de datos, shape y primeras filas.

Análisis de balance de clases.

2. Preprocesamiento

Codificación de etiquetas (LabelEncoder).

Estandarización / normalización (StandardScaler, RobustScaler).

Discretización opcional (KBinsDiscretizer).

Separación en train y test con estratificación.

3. Análisis Exploratorio y Visualización

Histogramas, boxplots y gráficas de distribución.

Heatmap de correlaciones.

PCA para exploración de estructura interna de los datos.

4. Selección de Características

Métodos estadísticos con:

SelectKBest

f_classif

Reducción de dimensionalidad con PCA.

5. Entrenamiento de Modelos

El notebook incluye múltiples algoritmos de clasificación:

RandomForestClassifier

MLPClassifier (Red Neuronal)

SVC (Support Vector Machine)

Logistic Regression

XGBoost Classifier

Se utilizan técnicas de búsqueda de hiperparámetros (RandomizedSearchCV) para mejorar el rendimiento.

6. Evaluación del Modelo

Se emplean las métricas más importantes para clasificación multiclase:

accuracy_score

f1_score

balanced_accuracy_score

classification_report

confusion_matrix

Además, se visualiza la matriz de confusión de forma gráfica con seaborn.

🧪 Tecnologías y Librerías Utilizadas
Python

pandas

numpy

seaborn

matplotlib

Scikit-Learn

Preprocesamiento

Modelos

Métricas

Búsqueda de hiperparámetros

Selección de características

PCA

XGBoost

XGBClassifier para modelos basados en boosting.

🚀 Cómo Ejecutar el Proyecto

Instala las dependencias:

pip install -r requirements.txt


Abre el notebook:

jupyter notebook


Ejecuta las celdas en orden, desde la carga de datos hasta la evaluación final.

📊 Resultados

El archivo genera:

métricas de rendimiento detalladas,

comparación entre modelos,

visualizaciones de la estructura de los datos,

gráficos de errores del modelo,

selección de características más importantes.

Dependiendo del modelo optimizado, se obtiene una predicción precisa de las especies de árboles a partir de sus descriptores.

📎 Estructura Recomendada del Proyecto
project/
│── data/
│    ├── train.csv
│── notebook.ipynb
│── README.md
│── requirements.txt

📝 Autor

Proyecto elaborado para fines académicos con el objetivo de analizar técnicas de clasificación multiclase aplicadas a bio-datos.