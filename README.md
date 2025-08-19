# 📉 Predicción de Cancelación de Clientes - Telecom X

Este proyecto tiene como objetivo predecir la cancelación (churn) de clientes en una empresa ficticia de telecomunicaciones llamada *Telecom X*, utilizando técnicas de Machine Learning. 

Se desarrollaron modelos de Regresión Logística y Random Forest, junto con análisis exploratorio, balanceo de clases (SMOTE), evaluación de desempeño y análisis de variables clave que influyen en la cancelación.

## 🧠 Modelos Utilizados

- **Regresión Logística** (con normalización)
- **Random Forest** (sin necesidad de normalización)

Ambos modelos fueron entrenados y evaluados utilizando las métricas: Accuracy, Precision, Recall, F1-score y ROC-AUC.

## 📊 Resultados Comparativos

| Métrica              | Regresión Logística | Random Forest |
|----------------------|---------------------|---------------|
| Accuracy             | 0.784               | 0.786         |
| Precision (Clase 1)  | 0.590               | 0.630         |
| Recall (Clase 1)     | 0.640               | 0.470         |
| F1-score (Clase 1)   | 0.610               | 0.540         |
| ROC-AUC              | 0.830               | 0.820         |

## 🔍 Análisis de Variables Relevantes

- Variables destacadas según Regresión Logística:
  - `Contract_Two year` (contrato de dos años)
  - `tenure` (meses de permanencia)
  - `InternetService_Fiber optic` (servicio de fibra óptica)
  - `MonthlyCharges` (cargos mensuales)

- Variables destacadas según Random Forest:
  - `MonthlyCharges`
  - `tenure`
  - `TotalCharges`
  - `Contract` y `InternetService`

## 🧪 Conclusiones

- Ambos modelos presentaron desempeños similares, pero la Regresión Logística mostró mejor balance entre Precision y Recall para la clase minoritaria.
- Las principales variables que influyen en la cancelación están relacionadas con el tipo de contrato, duración del servicio y tipo de internet.
- Se propone como estrategia de retención: ofrecer contratos más largos con beneficios, mejorar la experiencia de usuarios con fibra óptica y reducir el churn en clientes nuevos (tenure bajo).

## 🗂 Estructura del Proyecto

├── telecomx_datos_limpios.csv # Dataset preprocesado
├── notebook.ipynb # Análisis completo en Jupyter Notebook
├── imágenes/ # Gráficos y visualizaciones
└── README.md # Descripción del proyecto


## 🛠 Requisitos

- Python 3.8+
- pandas, seaborn, matplotlib
- scikit-learn
- imbalanced-learn

