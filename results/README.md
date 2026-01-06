# Resultados del Proyecto ML Challenge

Esta carpeta contiene todos los outputs, figuras, métricas y resultados generados durante el análisis de predicción de riesgo de accidentes de tráfico.

## Archivos Generados

### Predicciones Finales

- **submission.csv** - Archivo final de predicciones para Kaggle con 172,585 predicciones
  - Formato: `id, accident_risk`
  - Rango de predicciones: 0.0318 - 0.8669
  - Media: 0.3517
  - Desviación estándar: 0.1568

## Resultados del Modelado

### Comparación de Modelos

| Modelo                  | MSE      | RMSE     | MAE      | R²      | CV R²   |
| ----------------------- | -------- | -------- | -------- | -------- | -------- |
| **Random Forest** | 0.003169 | 0.056294 | 0.043647 | 0.885231 | 0.886328 |
| Gradient Boosting       | 0.003254 | 0.057041 | 0.044369 | 0.882167 | 0.883405 |
| Linear Regression       | 0.007822 | 0.088444 | 0.070809 | 0.716707 | 0.716982 |

### Mejor Modelo: Random Forest

**Configuración:**

- n_estimators: 300
- max_depth: 10
- min_samples_split: 5
- random_state: 42

**Métricas Finales:**

- MSE: 0.0032
- RMSE: 0.0563
- MAE: 0.0436
- R²: 0.8852 (88.52% de varianza explicada)

## Visualizaciones Generadas

Durante la ejecución del notebook se generan las siguientes visualizaciones:

### Análisis Exploratorio

- Distribución de la variable objetivo (accident_risk)
- Boxplot para detección de outliers
- Estadísticas descriptivas por variable

### Comparación de Modelos

- Gráficos de barras comparando R², MSE, RMSE y MAE
- Visualización del rendimiento de cada modelo

### Análisis de Datos

- Correlaciones entre variables numéricas
- Distribuciones de variables categóricas
- Análisis de la calidad de los datos

## Estructura de Archivos

```
results/
├── submission.csv          # Predicciones finales (172,585 filas)
└── README.md              # Este archivo
```

## Interpretación de Resultados

### Calidad del Modelo

- **Excelente rendimiento**: R² = 0.8852 indica que el modelo explica el 88.52% de la varianza
- **Error bajo**: RMSE = 0.0563 muestra predicciones muy precisas
- **Consistencia**: La validación cruzada (CV R² = 0.8863) confirma la estabilidad

### Distribución de Predicciones

- Las predicciones cubren todo el rango esperado (0-1)
- Media de 0.3517 sugiere un riesgo moderado promedio
- Distribución razonable sin valores extremos problemáticos

## Reproducibilidad

- Todos los resultados son reproducibles usando `random_state=42`
- El modelo final está entrenado con el dataset completo
- Las métricas reportadas provienen de validación cruzada de 5 folds

## Notas Técnicas

- **Preprocesamiento**: StandardScaler aplicado a todas las características
- **Codificación**: Label Encoding para variables categóricas
- **División**: 80% entrenamiento, 20% validación
- **Método de evaluación**: Validación cruzada estratificada
