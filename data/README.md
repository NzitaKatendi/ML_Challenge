# Datos del Proyecto ML Challenge

## Resumen del Proyecto

**Objetivo**: Predicción del riesgo de accidentes de tráfico utilizando técnicas de aprendizaje automático con selección de características basada en análisis ANOVA.

### Dataset y Variables

- **Tamaño**: 517,754 registros de entrenamiento, 172,585 de prueba
- **Variables originales**: 12 características predictoras
- **Variables seleccionadas**: 7 características (reducción del 41.7%)
- **Variable objetivo**: `accident_risk` (riesgo continuo de 0 a 1)

### Resultados del Análisis ANOVA

**Variables más influyentes identificadas:**

1. **`lighting`** (condiciones de iluminación) - Factor de mayor impacto
2. **`weather`** (condiciones climáticas) - Segundo factor más influyente
3. **`road_type`** (tipo de carretera) - Diferencias significativas entre tipos
4. **`time_of_day`** (hora del día) - Patrones temporales de riesgo

**Beneficios de la selección ANOVA:**

- Modelo más interpretable y menos propenso a overfitting
- Permite enfocar acciones de prevención en factores más relevantes
- Entrenamiento más eficiente y robusto

### Métricas del Modelo Final (Gradient Boosting)

- **MSE**: 0.0032 (error cuadrático muy bajo)
- **RMSE**: 0.0564 (error promedio de ~5.6%)
- **MAE**: 0.0437 (error absoluto de ~4.4%)
- **R²**: 0.8850 (88.5% de varianza explicada)

## Instrucciones para Obtener los Datos

## Dataset: Playground Series S5E10 - Predicting Road Accident Risk

### Fuente

- **Kaggle Competition**: https://www.kaggle.com/competitions/playground-series-s5e10/data

### Archivos Necesarios

Los siguientes archivos deben descargarse y colocarse en esta carpeta (`data/`):

1. **train.csv** - Dataset de entrenamiento con características y variable objetivo
2. **test.csv** - Dataset de prueba para generar predicciones
3. **sample_submission.csv** - Formato de archivo de submisión

### Cómo Descargar

#### Opción 1: Descarga Manual

1. Visita: https://www.kaggle.com/competitions/playground-series-s5e10/data
2. Descarga los archivos: `train.csv`, `test.csv`, `sample_submission.csv`
3. Coloca los archivos en esta carpeta `data/`

#### Opción 2: Usando Kaggle API

```bash
# Instalar Kaggle API
pip install kaggle

# Configurar credenciales (requiere cuenta de Kaggle)
# Descargar kaggle.json desde tu perfil de Kaggle
# Colocar en ~/.kaggle/kaggle.json

# Descargar dataset
kaggle competitions download -c playground-series-s5e10

# Extraer archivos
unzip playground-series-s5e10.zip -d data/
```

### Estructura Final

Después de descargar, la carpeta `data/` debe contener:

```
data/
├── train.csv
├── test.csv
└── sample_submission.csv
```

### Verificación

Una vez descargados los archivos, puedes verificar que están correctos ejecutando:

```python
import pandas as pd

# Verificar archivos
train = pd.read_csv('data/train.csv')
test = pd.read_csv('data/test.csv')
sample = pd.read_csv('data/sample_submission.csv')

print(f"Train shape: {train.shape}")
print(f"Test shape: {test.shape}")
print(f"Sample submission shape: {sample.shape}")
```

### Notas Importantes

- Los archivos CSV ya están incluidos en este repositorio
- Si necesitas descargar versiones actualizadas, usa las instrucciones anteriores
- El dataset es público y gratuito en Kaggle
