# bank_churn

# 🏦 Predicción de Baja de Clientes Bancarios (Customer Churn)

Este proyecto utiliza técnicas de ciencia de datos en R para predecir la probabilidad de que un cliente se dé de baja de un banco, basándose en variables demográficas, financieras y de comportamiento.

## 📊 Objetivo

El objetivo principal es desarrollar un modelo predictivo que ayude a identificar **clientes en riesgo de abandono**, permitiendo a las áreas comerciales y de retención actuar proactivamente.

## 📁 Dataset

El dataset contiene información de clientes como:
- Score crediticio
- Género, edad, país
- Salario estimado
- Tipo de tarjeta, quejas, riesgo FCC
- Actividad en los últimos 6 meses (acreditaciones y débitos)

La variable objetivo es `Baja (del banco)`, donde `1` indica que el cliente se dio de baja.

## 🔧 Tecnologías y herramientas

- `tidyverse` para manipulación de datos
- `lubridate` para fechas
- `caret` y `randomForest` para modelado
- `ROCR` para evaluación de performance
- Modelo final: **Random Forest**

## 🧪 Flujo del proyecto

1. **Limpieza de datos**
2. **Análisis exploratorio (EDA)**
3. Ingeniería de variables (acreditaciones totales, débitos, etc.)
4. División en entrenamiento/test
5. Entrenamiento con Random Forest
6. Evaluación con matriz de confusión y AUC - ROC
7. Guardado del modelo entrenado

## 📈 Resultados

El modelo alcanzó una **precisión del XX%** y un **AUC de YY** sobre los datos de test, lo que demuestra una buena capacidad para identificar clientes en riesgo.

Se visualizó también la importancia de variables, destacando:
- Score crediticio
- Cantidad de productos
- Total de débitos en 6 meses
- Score de satisfacción

## 📌 Posibles mejoras

- Comparación con modelos como `xgboost` o `glmnet`
- Feature engineering avanzado (ej. segmentación por tipo de tarjeta)
- Implementación en `Shiny` para visualización interactiva
- Uso de técnicas de `SMOTE` para balancear la clase

## 🚀 Cómo correr el proyecto

```r
# Cargar librerías
install.packages(c("tidyverse", "caret", "randomForest", "ROCR", "lubridate"))
source("customer_churn_prediction.R")
