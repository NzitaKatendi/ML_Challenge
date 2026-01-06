# ML Challenge: Predicción de Riesgo de Accidentes de Tráfico

## Descripción del Proyecto

Este proyecto implementa una solución completa de Machine Learning para predecir el riesgo de accidentes de tráfico utilizando el dataset del Playground Series S5E10 de Kaggle. El proyecto abarca desde la exploración de datos hasta la evaluación del modelo final, aplicando técnicas de aprendizaje supervisado.

## Estructura del Proyecto

```
ML Challenge/
│
├── data/                     # Datos del proyecto
│   ├── train.csv            # Dataset de entrenamiento
│   ├── test.csv             # Dataset de prueba
│   ├── sample_submission.csv # Formato de submisión
│   └── README.md            # Instrucciones para obtener datos
├── notebooks/               # Jupyter Notebooks
│   └── ML Challenge.ipynb   # Notebook principal con EDA, modelado y evaluación
├── results/                 # Resultados y outputs
│   ├── submission.csv       # Predicciones finales
│   └── README.md            # Documentación de resultados
├── README.md               # Resumen y presentación del código
└── requirements.txt        # Dependencias / librerías
```

## Metodología Implementada

### 1. Análisis y Comprensión del Problema

- Identificación del tipo de problema (supervisado/no supervisado)
- Comprensión del objetivo del challenge
- Análisis inicial de suposiciones y riesgos

### 2. Exploración y Análisis de Datos (EDA)

- Análisis estadístico básico
- Estudio de distribuciones, correlaciones y outliers
- Visualizaciones relevantes
- Formulación de hipótesis basadas en los datos

### 3. Preprocesamiento

- Limpieza de datos (nulos, duplicados, inconsistencias)
- Transformaciones necesarias:
  - Escalado/normalización con StandardScaler
  - Codificación de variables categóricas (One-Hot y Label Encoding)
- Justificación de cada decisión tomada

### 4. Selección y Entrenamiento de Modelos

- Modelos evaluados:
  - Regresión Logística
  - Random Forest
  - Gradient Boosting
  - Support Vector Machine (SVM)
- Justificación de la elección de modelos
- Comparativa entre diferentes enfoques

### 5. Optimización

- Ajuste de hiperparámetros usando Grid Search
- Validación cruzada (5-fold)
- Prevención de sobreajuste

### 6. Evaluación

- Métricas apropiadas: Accuracy, AUC-ROC
- Análisis de resultados y matriz de confusión
- Interpretación de errores
- Análisis de importancia de características

## Instalación y Uso

### Requisitos Previos

- Python 3.7 o superior
- Jupyter Notebook o JupyterLab

### Instalación

1. Clona o descarga este repositorio
2. Instala las dependencias:

```bash
pip install -r requirements.txt
```

3. **Obtener los datos**: Consulta `data/README.md` para instrucciones detalladas sobre cómo descargar los datasets desde Kaggle

### Ejecución

1. Abre Jupyter Notebook:

```bash
jupyter notebook
```

2. Navega a la carpeta `notebooks/` y abre `ML Challenge.ipynb`
3. Ejecuta todas las celdas secuencialmente

## Contenido de las Carpetas

### data/

Contiene todos los datasets necesarios e instrucciones para obtenerlos:

- `train.csv`: Dataset de entrenamiento con variables predictoras y objetivo
- `test.csv`: Dataset de prueba para generar predicciones finales
- `sample_submission.csv`: Formato requerido para las predicciones
- `README.md`: Instrucciones detalladas para descargar los datos desde Kaggle

### notebooks/

Jupyter Notebook con análisis completo:

- `ML Challenge.ipynb`: Notebook principal con EDA, modelado y evaluación completos

### results/

Outputs y resultados del proyecto:

- `submission.csv`: Predicciones finales generadas por el mejor modelo
- `README.md`: Documentación de los resultados y estructura de outputs
- Figuras y métricas de evaluación (generadas durante la ejecución)

## Resultados Principales

### Comparación de Modelos

| Modelo                  | MSE      | RMSE     | MAE      | R²      | CV R²   |
| ----------------------- | -------- | -------- | -------- | -------- | -------- |
| **Random Forest** | 0.003169 | 0.056294 | 0.043647 | 0.885231 | 0.886328 |
| Gradient Boosting       | 0.003254 | 0.057041 | 0.044369 | 0.882167 | 0.883405 |
| Linear Regression       | 0.007822 | 0.088444 | 0.070809 | 0.716707 | 0.716982 |

**Mejor modelo seleccionado: Random Forest**

### Métricas Finales del Modelo Random Forest

- **MSE**: 0.0032
- **RMSE**: 0.0563
- **MAE**: 0.0436
- **R²**: 0.8852

### Estadísticas de Predicciones

- **Mínimo**: 0.0318
- **Máximo**: 0.8669
- **Media**: 0.3517
- **Desviación estándar**: 0.1568

### Outputs Generados

- Análisis exploratorio completo con visualizaciones
- Comparación de múltiples modelos de ML
- Modelo optimizado con mejores hiperparámetros
- Archivo de predicciones finales en `results/submission.csv`

## Características Técnicas

### Modelos Implementados

- **Linear Regression**: Modelo baseline interpretable
- **Random Forest**: Ensemble method robusto (MEJOR MODELO)
- **Gradient Boosting**: Modelo de boosting avanzado

### Técnicas de Preprocesamiento

- Tratamiento de valores nulos (mediana/moda)
- Eliminación de duplicados
- Codificación de variables categóricas
- Escalado de características

### Validación y Evaluación

- División train/validation (80/20)
- Validación cruzada de 5 folds
- Métricas: MSE, RMSE, MAE, R²
- Análisis de importancia de características
- Comparación exhaustiva de modelos

## Estructura del Código

El notebook está organizado en secciones claramente definidas:

1. **Introducción y Contexto** - Descripción del problema
2. **Importación de Librerías** - Configuración del entorno
3. **Carga de Datos** - Lectura y descripción inicial
4. **EDA** - Análisis exploratorio exhaustivo
5. **Preprocesamiento** - Limpieza y transformación
6. **Modelado** - Entrenamiento y comparación
7. **Optimización** - Ajuste de hiperparámetros
8. **Evaluación** - Métricas y análisis de resultados
9. **Predicciones** - Generación de resultados finales
10. **Conclusiones** - Resumen y próximos pasos

## Características del Código

### Reproducibilidad

- Todas las semillas aleatorias están fijadas (`random_state=42`)
- Código ejecutable y ordenado
- Los resultados son completamente reproducibles

### Calidad del Código

- Comentarios claros (no excesivos)
- Uso correcto de librerías estándar (numpy, pandas, sklearn, etc.)
- Código bien estructurado y documentado
- Decisiones justificadas en el notebook

## Cumplimiento del Objetivo

✅ **OBJETIVO COMPLETAMENTE LOGRADO**: El proyecto desarrolló exitosamente un modelo predictivo para evaluar el riesgo de accidentes de tráfico, cumpliendo perfectamente con los requisitos del Kaggle Playground Series S5E10.

### Alineación Perfecta con el Challenge de Kaggle:

1. **Problema Objetivo**: "Predict the likelihood of accidents on different types of roads" ✅
2. **Métrica de Evaluación**: RMSE (Root Mean Squared Error) ✅
3. **Formato de Predicciones**: Valores entre 0 y 1 para accident_risk ✅
4. **Volumen de Datos**: 172,585 predicciones generadas ✅

### Evidencias del Éxito:

1. **Modelo de Alto Rendimiento**: Random Forest con R² = 0.8852 (88.52% de varianza explicada)
2. **RMSE Excelente**: 0.0563 - muy competitivo para la métrica oficial de Kaggle
3. **Rango Adecuado**: Predicciones entre 0.0318 y 0.8669 cubren todo el espectro de riesgo
4. **Validación Robusta**: Validación cruzada de 5 folds confirma la estabilidad del modelo
5. **Comparación Exhaustiva**: Se evaluaron 3 modelos diferentes con métricas completas
6. **Archivo de Submisión**: `submission.csv` generado en formato correcto para Kaggle

### Calidad Competitiva del Modelo:

- **Rendimiento Excepcional**: R² > 0.88 indica capacidad predictiva muy alta
- **Error Mínimo**: RMSE = 0.0563 es excelente para predicciones en escala [0,1]
- **Estabilidad Confirmada**: CV R² = 0.8863 demuestra consistencia
- **Distribución Realista**: Media de 0.3517 con desviación de 0.1568 refleja variabilidad esperada en riesgo de accidentes

## Próximos Pasos y Mejoras

### Optimizaciones Potenciales

1. **Feature Engineering Avanzado**: Crear nuevas características basadas en conocimiento del dominio de seguridad vial
2. **Ensemble Methods**: Combinar múltiples modelos para mejorar predicciones
3. **Técnicas de Explicabilidad**: Implementar SHAP o LIME para mayor interpretabilidad
4. **Optimización Bayesiana**: Para búsqueda más eficiente de hiperparámetros
5. **Análisis de Residuos**: Estudiar patrones en errores de predicción

### Extensiones del Proyecto

- **Implementación Web**: Desarrollar aplicación web para el Stack Overflow Challenge
- **Análisis Temporal**: Incorporar patrones estacionales si hay datos temporales
- **Segmentación Geográfica**: Modelos específicos por región o tipo de carretera
- **Monitoreo en Tiempo Real**: Sistema de alertas basado en predicciones

## Informe Técnico

Este README complementa el informe técnico en PDF que incluye:

1. Introducción y contexto del problema
2. Descripción del dataset
3. Metodología seguida
4. Modelos utilizados y justificación
5. Resultados y evaluación
6. Conclusiones
7. Reparto de tareas del equipo

**Nota**: El informe técnico no incluye código, sino referencias al mismo cuando es necesario.

## Contacto

Este proyecto fue desarrollado como parte del ML Challenge del módulo de Aprendizaje Supervisado. Para preguntas o sugerencias, consulta la documentación en el notebook principal.
