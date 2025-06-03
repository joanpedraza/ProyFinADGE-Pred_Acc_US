# 🚗 US Accidents Analysis with PySpark & XGBoost (2016–2023)

Proyecto final de la materia **Análisis de Datos a Gran Escala** – Universidad Industrial de Santander (2025-I)

---

## 📌 Descripción

Este proyecto analiza más de **7.7 millones de registros** de accidentes de tránsito ocurridos en Estados Unidos entre 2016 y 2023. Se implementó un pipeline completo que combina **tecnologías de Big Data (PySpark)** con **modelos de aprendizaje automático (XGBoost)** para:

- Preprocesar y transformar datos masivos de forma distribuida
- Predecir la cantidad de accidentes diarios por ciudad
- Evaluar el impacto de variables climáticas en el rendimiento del modelo

---

## 🎯 Objetivos

### General:
Analizar grandes volúmenes de datos de accidentes en EE. UU. para identificar patrones y construir modelos predictivos.

### Específicos:
- Explorar relaciones entre variables temporales, geográficas y climáticas.
- Implementar un pipeline distribuido con PySpark.
- Entrenar y evaluar modelos de regresión con y sin variables climáticas.
- Visualizar la importancia de los factores involucrados en los accidentes.

---

## 🧠 Tecnologías utilizadas

| Herramienta | Descripción |
|-------------|-------------|
| **PySpark** | Procesamiento distribuido de datos a gran escala |
| **Pandas**  | Manipulación de datos para modelado |
| **XGBoost** | Algoritmo de boosting para regresión |
| **MLflow**  | Seguimiento y registro de experimentos de ML |
| **Matplotlib / Seaborn** | Visualización de resultados |

---

## ⚙️ Estructura del Pipeline

1. **Carga y limpieza de datos** (`PySpark`)
   - Lectura del CSV original (2016–2023)
   - Conversión de fechas, limpieza de nulos
2. **Agregación diaria**
   - Conteo de accidentes diarios
   - Promedios diarios de variables climáticas
3. **Exportación**
   - Datos `.parquet` por año
4. **Entrenamiento por año (`XGBoost`)**
   - Modelos con y sin variables climáticas
   - Evaluación: RMSE, MAE, R²
5. **Visualización**
   - Importancia de variables por año
   - Comparaciones con vs. sin clima

---
| Año | R² sin clima | R² con clima |
|-----|--------------|--------------|
| 2016 | -0.490 | 0.162 |
| 2017 | 0.105  | 0.188 |
| 2018 | 0.214  | 0.319 |
| ... | ...    | ...   |
| 2023 | 0.307  | 0.404 |

✔️ **Incluir clima mejora sistemáticamente el desempeño del modelo.**

---

## 📌 Conclusiones

- **PySpark** fue fundamental para manejar y transformar el dataset a escala.
- **XGBoost** permitió construir modelos eficientes de predicción.
- Las variables climáticas aportaron significativamente al rendimiento.
- Este proyecto demuestra cómo unir técnicas de Big Data y Machine Learning en un flujo reproducible y escalable.

---

## ✍️ Autores

- Mateo Ortiz Cruzate
- Joan Sebastian Pedraza  
- Josué Rodríguez de la Rosa  

Docente: David Edmundo Romo Bucheli  
Análisis de Datos a Gran Escala – UIS  
Junio 2025
