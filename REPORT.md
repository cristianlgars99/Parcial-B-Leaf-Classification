📘 1. Introducción

Este proyecto desarrolla un modelo de Machine Learning para la clasificación automática de especies de árboles a partir de características numéricas derivadas de imágenes de hojas. El dataset contiene atributos relacionados con la forma, los márgenes y la textura de cada hoja, normalizados previamente para facilitar el entrenamiento de modelos.

El propósito es construir un sistema preciso capaz de identificar la especie correspondiente a una hoja mediante algoritmos de clasificación supervisada.

📁 2. Descripción del Dataset

El dataset incluye:

990 muestras (hojas)

194 columnas

192 características numéricas

1 columna de identificador (id)

1 columna objetivo (species)

Tipos de características

Margin1–Margin8: describen la forma del borde de la hoja.

Shape1–ShapeN: representan componentes geométricos (si existen).

Texture1–Texture64: describen patrones de textura extraídos de la imagen.

La variable objetivo species contiene las especies de árboles a clasificar.

🔧 3. Preprocesamiento de los Datos

El pipeline de preprocesamiento incluye:

3.1 Codificación de etiquetas

Se utiliza LabelEncoder para transformar las especies en valores numéricos.

3.2 Separación del dataset

Los datos se dividen en:

80% entrenamiento

20% prueba
Usando train_test_split con estratificación para mantener el balance de clases.

3.3 Normalización / Escalado

Se emplean diferentes técnicas según el modelo:

StandardScaler

RobustScaler

KBinsDiscretizer (opcional)

3.4 Selección de características

Se aplican dos métodos:

SelectKBest (f_classif)

Reducción de dimensionalidad con PCA

Esto ayuda a identificar las características más relevantes y reducir ruido.

📊 4. Análisis Exploratorio

Incluye visualizaciones clave para entender la estructura de los datos:

Distribución de clases

Heatmap de correlación

Histogramas y boxplots

Proyección PCA (2D o 3D)

Análisis de varianza explicada

Estas gráficas permiten detectar outliers, correlaciones fuertes y redundancia en los datos.

🤖 5. Modelos Implementados

Se entrenaron y compararon varios algoritmos de clasificación:

5.1 Random Forest

Modelo robusto basado en múltiples árboles de decisión.

5.2 MLPClassifier

Red neuronal multicapa aplicada sobre datos tabulares.

5.3 Support Vector Machine (SVC)

Buen desempeño en problemas de alta dimensionalidad.

5.4 Logistic Regression

Modelo lineal para referencia base (baseline).

5.5 XGBoost

Modelo ensamble altamente eficiente y preciso.

Cada modelo fue optimizado usando RandomizedSearchCV para ajustar hiperparámetros.

📈 6. Evaluación y Métricas

Las evaluaciones del proyecto se realizaron usando:

Accuracy

Balanced Accuracy

F1-Score (macro y weighted)

Classification Report

Matriz de Confusión

Estas métricas permiten evaluar el desempeño sobre todas las clases, incluso las minoritarias.

La matriz de confusión se graficó con seaborn para identificar errores específicos entre especies.

🧠 7. Resultados

Aunque depende de la ejecución final, típicamente:

Los modelos basados en ensembles (Random Forest, XGBoost) suelen lograr los mejores resultados.

PCA ayuda a reducir dimensionalidad sin perder precisión.

SVM y Redes Neuronales requieren normalización adecuada para rendir bien.

En general, se obtuvo un alto rendimiento en la clasificación multiclase.

🚀 8. Conclusiones

El uso de características numéricas extraídas de imágenes permite clasificar eficazmente especies de árboles.

El preprocesamiento (escalado, selección de características y PCA) mejora significativamente el rendimiento.

Los modelos ensamble como Random Forest y XGBoost ofrecen los mejores resultados para este tipo de datos.

Las visualizaciones y análisis exploratorios son fundamentales para entender la estructura del dataset.

El pipeline desarrollado es fácilmente adaptable a otros problemas de clasificación multiclase.