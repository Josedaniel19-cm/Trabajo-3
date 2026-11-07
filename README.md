# Trabajo Práctico 3: Aprendizaje No Supervisado

## Palmer Penguins: Reducción de Dimensionalidad y Agrupamiento

## 1. Descripción del proyecto

Este proyecto tiene como propósito desarrollar un experimento de aprendizaje no supervisado utilizando el conjunto de datos **Palmer Penguins**. Se busca explorar las características físicas de diferentes especies de pingüinos mediante técnicas de reducción de dimensionalidad, selección de variables y algoritmos de agrupamiento.

El análisis compara tres enfoques: el conjunto de datos original, la reducción a dos componentes principales mediante PCA y la selección de variables basada en el análisis de correlación. Posteriormente, se aplica el algoritmo K-means para identificar posibles agrupamientos y evaluar su calidad mediante diferentes métricas.

## 2. Objetivo general

Diseñar y ejecutar un experimento de aprendizaje no supervisado que permita explorar y comparar diferentes enfoques de reducción de dimensionalidad y agrupamiento, utilizando PCA, selección de variables y K-means como herramientas principales de análisis.

## 3. Descripción del dataset

Se utiliza el conjunto de datos **Palmer Penguins**, que contiene información sobre características físicas de pingüinos observados en el archipiélago Palmer, ubicado en la Antártida.

El dataset original contiene 344 observaciones y registra información de tres especies:

- Adelie.
- Chinstrap.
- Gentoo.

Para el desarrollo del experimento se seleccionaron cuatro variables numéricas:

| Variable | Descripción |
|---|---|
| `bill_length_mm` | Longitud del pico (mm). |
| `bill_depth_mm` | Profundidad del pico (mm). |
| `flipper_length_mm` | Longitud de las aletas (mm). |
| `body_mass_g` | Masa corporal (g). |

Los registros que presentan valores faltantes en las variables seleccionadas se eliminan para trabajar con información completa.

**Fuente del dataset:** [Palmer Penguins - GitHub](https://github.com/allisonhorst/palmerpenguins)

## 4. Metodología

El experimento se desarrolla en las siguientes etapas:

### 4.1. Preparación de los datos
- Carga y exploración inicial del dataset.
- Selección de las cuatro variables numéricas.
- Eliminación de registros con valores faltantes.
- Análisis estadístico descriptivo.
- Estandarización mediante `StandardScaler`.

### 4.2. Reducción de dimensionalidad mediante PCA
- Aplicación del Análisis de Componentes Principales.
- Cálculo de la varianza explicada por cada componente.
- Elaboración del gráfico Scree Plot.
- Reducción del conjunto de datos a dos componentes principales.
- Visualización e interpretación de los patrones encontrados.

### 4.3. Selección de variables
- Construcción de la matriz de correlación.
- Identificación de relaciones entre las variables.
- Aplicación de un umbral de correlación absoluta de 0.80.
- Selección de características con menor redundancia.

### 4.4. Agrupamiento mediante K-means

Se aplica K-means sobre tres versiones del conjunto de datos:

1. Dataset original estandarizado.
2. Dataset reducido mediante PCA a dos componentes.
3. Dataset obtenido mediante selección de variables.

Se prueban valores de K entre 2 y 6 para comparar el comportamiento de los agrupamientos.

### 4.5. Evaluación y comparación

Se utilizan las siguientes herramientas de evaluación:

- **Método del codo (Elbow Method):** permite analizar la inercia y determinar posibles cantidades adecuadas de agrupamientos.
- **Silhouette Score:** evalúa la cohesión interna y separación entre los grupos.
- **Adjusted Rand Index (ARI):** permite comparar los agrupamientos encontrados con las especies originales como evaluación externa.

## 5. Herramientas y tecnologías

El proyecto se desarrolla en Python utilizando las siguientes librerías:

| Herramienta | Aplicación |
|---|---|
| Python | Lenguaje de programación. |
| Pandas | Manipulación y análisis de datos. |
| NumPy | Operaciones numéricas. |
| Matplotlib | Visualización gráfica. |
| Seaborn | Análisis y visualización estadística. |
| Scikit-learn | Estandarización, PCA y K-means. |
| Jupyter Notebook | Desarrollo y documentación del experimento. |

## 6. Estructura del repositorio

```text
Trabajo-Practico-3/
│
├── Palmer_Penguins_Analisis.ipynb
│
├── README.md
│
└── data/
    └── penguins.csv
```

## 7. Resultados y hallazgos

El experimento permitirá comparar el desempeño de los tres enfoques de agrupamiento y determinar cuál ofrece mejores resultados para identificar patrones en las características físicas de los pingüinos.

Se analizarán principalmente:

- La proporción de varianza explicada por las componentes principales.
- Las relaciones entre las variables seleccionadas.
- La cantidad de agrupamientos más adecuada.
- Las diferencias en los valores de Silhouette Score e inercia.
- La correspondencia entre los grupos identificados y las especies originales.

Los resultados numéricos, gráficos e interpretaciones definitivas se encuentran documentados en el Jupyter Notebook.

## 8. Conclusión

El desarrollo de este experimento permite comprender la utilidad de las técnicas de aprendizaje no supervisado para identificar patrones en conjuntos de datos sin necesidad de utilizar una variable objetivo durante el entrenamiento.

La comparación entre PCA, selección de variables y K-means permite evaluar cómo la transformación y reducción de características pueden influir en la calidad de los agrupamientos.

De esta manera, el proyecto busca determinar cuál enfoque resulta más apropiado para representar y analizar las diferencias físicas entre los pingüinos del conjunto de datos seleccionado.

---

**Trabajo Práctico 3 - Aprendizaje No Supervisado**

Proyecto académico desarrollado en Python.
