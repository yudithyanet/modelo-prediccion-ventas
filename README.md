# 📊 Modelo de Predicción de Ventas

Este proyecto tiene como objetivo analizar datos históricos de ventas y construir un **modelo predictivo de Machine Learning** capaz de estimar los ingresos futuros de productos, utilizando Python y librerías de análisis de datos.

Problema
MarketPlus enfrenta desafíos comunes en plataformas de e-commerce:
•	Falta de precisión en la proyección de la demanda mensual.
•	Exceso de inventario en ciertos productos y faltantes en otros.
•	Desconocimiento de los productos y categorías más rentables.
•	Estrategias de descuento sin análisis de impacto en margen.
•	Escasa visibilidad geográfica sobre el origen de los ingresos.
🔎 Impacto: sobrecostos logísticos, pérdida de eficiencia comercial y decisiones poco informadas.

🔬 Hipótesis
1.	Los productos con mejores calificaciones y entregas más rápidas generan mayor volumen de ventas.
2.	El 20% de los productos explica aproximadamente el 80% de los ingresos totales (Ley de Pareto).
3.	Los descuentos aplicados estratégicamente aumentan ventas sin deteriorar márgenes.
4.	Incorporar variables externas (estacionalidad, campañas y geografía) mejora la precisión del forecast.

## 🧠 Objetivo del Proyecto

- Realizar un **análisis exploratorio de datos (EDA)** para identificar patrones, outliers y relaciones entre variables.
- Desarrollar un **modelo de regresión supervisada** para predecir el ingreso total (`ingreso_total`) a partir de variables como:
  - `precio_unitario`
  - `cantidad`
  - `descuento`
  - `tiempo_entrega_dias`
  - `calificacion`
- Evaluar el desempeño del modelo mediante métricas de error y visualización de resultados.

## 🧰 Tecnologías y Librerías Utilizadas

- **Lenguaje:** Python 3.9+
- **Entorno:** Jupyter Notebook
- **Librerías principales:**
  - `pandas` → manipulación de datos
  - `numpy` → cálculos numéricos
  - `matplotlib` y `seaborn` → visualización de datos
  - `scikit-learn` → modelos de machine learning y métricas
  - `joblib` → guardar y cargar modelos

## 📈 Estructura del Proyecto

analisis_ventas_ml/
│
├── data/ # Archivos de datos (CSV, Excel, etc.)
│ └── ventas.csv
│
├── notebooks/ # Notebooks del análisis y modelo
│ ├── 01_ANALISIS_EXPLORATORIO.ipynb
│ └── 02_MODELO_PREDICCION_VENTAS.ipynb
│
├── models/ # Modelos entrenados
│ └── modelo_regresion.pkl
│
├── visuals/ # Gráficos y visualizaciones
│ └── comparativo_prediccion.png
│
├── requirements.txt # Dependencias del proyecto
└── README.md # Descripción general

---

## 🔍 Análisis Exploratorio (EDA)

Durante el análisis exploratorio se realizaron las siguientes tareas:
- Identificación de **outliers** usando el método del rango intercuartílico (IQR).  
- Visualización de **distribuciones e histogramas** por variable numérica.  
- Análisis de **correlaciones** para determinar qué variables influyen más en las ventas.  
- Verificación de **reglas de negocio** y consistencia de los datos.

---

## 🤖 Modelado y Evaluación

El modelo seleccionado se entrenó usando los datos normalizados.  
Las métricas obtenidas fueron:

| Métrica | Resultado |
|----------|------------|
| **MAE (Error Absoluto Medio)** | 7,369.61 |
| **RMSE (Raíz del Error Cuadrático Medio)** | 7,800.76 |
| **R² (Coeficiente de Determinación)** | -26.49 |

📉 *Interpretación:* el modelo inicial presenta un desempeño deficiente (R² negativo), indicando la necesidad de ajustar hiperparámetros, realizar feature engineering o probar modelos más robustos (como Random Forest o Gradient Boosting).

---

## 🧪 Cómo Ejecutar el Proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/Yudithyanet/analisis_ventas_ml.git
   cd analisis_ventas_ml
