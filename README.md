📊 Modelo de Predicción de Ventas – Análisis y Estrategia de Marketing
📌 Descripción General del Proyecto

Este proyecto tiene como objetivo analizar datos históricos de ventas de una plataforma de e-commerce y desarrollar un modelo de Machine Learning para estimar el ingreso total de los productos, así como generar insights estratégicos que apoyen la toma de decisiones comerciales y de marketing.

El enfoque principal no solo es técnico, sino también orientado a negocio, buscando identificar patrones de comportamiento, oportunidades de optimización y riesgos operativos.

🧩 Problema de Negocio

MarketPlus enfrenta diversos desafíos comunes en plataformas de comercio electrónico:

Falta de precisión en la proyección de la demanda mensual

Exceso de inventario en ciertos productos y quiebres de stock en otros

Desconocimiento de los productos y categorías más rentables

Aplicación de descuentos sin análisis de impacto en margen

Escasa visibilidad geográfica del origen de los ingresos

🔎 Impacto:
Sobrecostos logísticos, pérdida de eficiencia comercial y toma de decisiones basada en intuición más que en datos.

🔬 Hipótesis del Análisis

Los productos con mejores calificaciones y tiempos de entrega más rápidos generan mayor volumen de ventas.

Aproximadamente el 20% de los productos concentra cerca del 80% de los ingresos (Ley de Pareto).

Los descuentos aplicados estratégicamente pueden incrementar ventas sin afectar negativamente el margen.

Incorporar variables externas (estacionalidad, campañas y geografía) mejora la precisión del forecast.

🧠 Objetivos del Proyecto

Realizar un Análisis Exploratorio de Datos (EDA) para identificar patrones, outliers y relaciones entre variables.

Construir un modelo de regresión supervisada para predecir el ingreso total (ingreso_total) usando variables como:

precio_unitario

cantidad

descuento

tiempo_entrega_dias

calificacion

Evaluar el desempeño del modelo mediante métricas y visualizaciones.

Traducir los resultados en conclusiones de negocio y estrategias de marketing.

🧰 Tecnologías Utilizadas

Lenguaje: Python 3.9+

Entorno: Jupyter Notebook

Librerías:

pandas, numpy

matplotlib, seaborn

scikit-learn

joblib

📈 Estructura del Proyecto
analisis_ventas_ml/
│
├── data/
│   └── ventas.csv
├── notebooks/
│   ├── 01_ANALISIS_EXPLORATORIO.ipynb
│   └── 02_MODELO_PREDICCION_VENTAS.ipynb
├── models/
│   └── modelo_regresion.pkl
├── visuals/
│   └── comparativo_prediccion.png
├── requirements.txt
└── README.md

🔍 Análisis Exploratorio de Datos (EDA)

Durante el EDA se realizaron las siguientes actividades:

Identificación de outliers mediante el método del rango intercuartílico (IQR).

Análisis de distribuciones e histogramas de variables numéricas.

Evaluación de correlaciones para identificar factores que influyen en el ingreso.

Validación de reglas de negocio y consistencia de los datos.

📌 Conclusiones del Análisis de Datos
1️⃣ Concentración de ingresos (Ley de Pareto)

Un porcentaje reducido de productos genera la mayor parte de los ingresos.

El negocio depende fuertemente de su catálogo estrella.

📌 Implicación:
Es crítico priorizar inventario, logística y estrategia de precios en estos productos clave.

2️⃣ Factores que influyen en las ventas

Precio unitario y cantidad explican gran parte del ingreso.

Mejores calificaciones se asocian con mayores ventas.

Tiempos de entrega largos impactan negativamente el volumen vendido.

Los descuentos no siempre generan un aumento proporcional del ingreso.

📌 Implicación:
La experiencia del cliente es un factor determinante en el desempeño comercial.

3️⃣ Impacto de los descuentos

Los descuentos generalizados pueden reducir el margen sin mejorar ventas.

La respuesta a promociones varía según el producto.

📌 Implicación:
Las promociones deben basarse en análisis de elasticidad y rotación.

4️⃣ Diferencias geográficas

Existen regiones que concentran mayores ingresos y otras con potencial de crecimiento.

📌 Implicación:
Oportunidad para estrategias de marketing y logística segmentadas por zona.

🤖 Modelado y Evaluación

El modelo de regresión inicial obtuvo los siguientes resultados:

Métrica	Valor
MAE	7,369.61
RMSE	7,800.76
R²	-26.49
Interpretación

El R² negativo indica que el modelo no logra explicar la variabilidad del ingreso.

Esto sugiere relaciones no lineales o variables relevantes ausentes.

📌 Conclusión técnica:
El modelo cumple un propósito exploratorio, pero no es adecuado aún para predicción operativa ni para un dashboard de forecasting.

🎯 Estrategia de Marketing Basada en Datos
🛒 Optimización de inventario

Priorizar productos que concentran el mayor ingreso.

Reducir stock de productos con baja rotación.

💸 Descuentos inteligentes

Aplicar promociones solo a productos con alta elasticidad.

Evitar descuentos masivos sin análisis previo.

🚚 Mejora de experiencia del cliente

Reducir tiempos de entrega en productos estratégicos.

Mantener altos estándares de calidad y calificación.

📍 Estrategia geográfica

Incrementar inversión en regiones de alto desempeño.

Diseñar campañas específicas para zonas con potencial de crecimiento.

🧠 Roadmap de Mejora del Modelo Predictivo

Feature engineering (estacionalidad, campañas, categoría).

Segmentación por tipo de producto.

Implementación de modelos no lineales:

Random Forest

Gradient Boosting (XGBoost, LightGBM)

Validación cruzada y análisis de errores por segmento.

🏁 Conclusión Final

Este proyecto demuestra cómo el análisis de datos y Machine Learning pueden generar valor incluso cuando el modelo predictivo inicial presenta limitaciones.
El enfoque analítico permitió identificar oportunidades claras de mejora en inventario, marketing y experiencia del cliente, sentando las bases para una solución predictiva más robusta en futuras iteraciones.

## 🧪 Cómo Ejecutar el Proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/Yudithyanet/analisis_ventas_ml.git
   cd analisis_ventas_ml
