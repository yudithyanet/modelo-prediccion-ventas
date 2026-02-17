📊 Modelo de Predicción de Ventas – Análisis y Estrategia de Marketing
📌 Descripción General del Proyecto

Este proyecto analiza datos históricos de ventas de una plataforma de e-commerce con el objetivo de comprender los principales drivers del ingreso, evaluar la factibilidad de un modelo predictivo y traducir los resultados en decisiones estratégicas de negocio y marketing.

El enfoque combina análisis exploratorio, modelado de Machine Learning y pensamiento estratégico, priorizando el valor para la toma de decisiones por sobre la complejidad técnica.

🧩 Problema de Negocio

MarketPlus enfrenta desafíos típicos de plataformas de comercio electrónico:

Baja precisión en la proyección de la demanda mensual

Exceso de inventario en ciertos productos y quiebres de stock en otros

Falta de visibilidad sobre productos y categorías más rentables

Aplicación de descuentos sin análisis de impacto en el margen

Escasa segmentación geográfica del origen de los ingresos

🔎 Impacto: Sobrecostos logísticos, menor eficiencia comercial y decisiones basadas en intuición más que en datos.

🔬 Hipótesis del Análisis

Productos con mejores calificaciones y tiempos de entrega más cortos generan mayor volumen de ventas.

Aproximadamente el 20% de los productos concentra cerca del 80% de los ingresos (Ley de Pareto).

Los descuentos aplicados de forma estratégica pueden incrementar ventas sin deteriorar el margen.

La incorporación de variables externas (estacionalidad, campañas, geografía) mejora la capacidad predictiva.

🧠 Objetivos del Proyecto

Realizar un Análisis Exploratorio de Datos (EDA) para identificar patrones, outliers y relaciones clave.

Construir un modelo de regresión supervisada para predecir el ingreso total (ingreso_total).

Evaluar el desempeño del modelo mediante métricas y visualizaciones.

Traducir los hallazgos en conclusiones accionables de negocio y marketing.

🧰 Tecnologías Utilizadas

Lenguaje: Python 3.9+

Entorno: Jupyter Notebook

Librerías: pandas, numpy, matplotlib, seaborn, scikit-learn, joblib

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

Durante el EDA se realizaron:

Identificación de outliers mediante el método IQR.

Análisis de distribuciones e histogramas.

Evaluación de correlaciones entre variables clave.

Validación de reglas de negocio y consistencia de los datos.

📌 Conclusiones del Análisis de Datos
1️⃣ Concentración de ingresos (Ley de Pareto)

Un porcentaje reducido de productos genera la mayor parte de los ingresos.

📌 Implicación: Priorizar inventario, logística y estrategia de precios en productos clave.

2️⃣ Factores que influyen en las ventas

Precio unitario y cantidad explican gran parte del ingreso.

Mejores calificaciones se asocian con mayores ventas.

Tiempos de entrega largos impactan negativamente.

Los descuentos no siempre generan aumentos proporcionales del ingreso.

📌 Implicación: La experiencia del cliente es un driver central del desempeño comercial.

3️⃣ Impacto de los descuentos

Descuentos generalizados pueden reducir el margen sin aumentar ventas.

La respuesta promocional varía por producto.

📌 Implicación: Las promociones deben basarse en análisis de elasticidad y rotación.

4️⃣ Diferencias geográficas

Existen regiones con alta concentración de ingresos y otras con potencial de crecimiento.

📌 Implicación: Oportunidades para estrategias de marketing y logística segmentadas.

🤖 Modelado y Evaluación

Resultados del modelo inicial:

Métrica	Valor
MAE	7,369.61
RMSE	7,800.76
R²	-26.49

📌 Interpretación:
El R² negativo indica que el modelo no explica adecuadamente la variabilidad del ingreso, sugiriendo relaciones no lineales y variables relevantes ausentes.

📌 Conclusión técnica:
El modelo cumple un rol exploratorio, pero no es apto para predicción operativa ni para forecasting confiable.

🎯 Estrategia de Marketing Basada en Datos

🛒 Optimización de inventario: priorizar productos de alta contribución.

💸 Descuentos inteligentes: promociones focalizadas y basadas en elasticidad.

🚚 Experiencia del cliente: reducir tiempos de entrega y mantener calidad.

📍 Estrategia geográfica: campañas y logística segmentadas por región.

🧠 Roadmap de Mejora del Modelo

Feature engineering (estacionalidad, campañas, categoría).

Segmentación por tipo de producto.

Modelos no lineales (Random Forest, Gradient Boosting).

Validación cruzada y análisis de errores por segmento.

🏁 Conclusión Final

Este proyecto demuestra que el valor del análisis de datos no depende exclusivamente de un modelo predictivo exitoso.
Incluso con un modelo limitado, el análisis permitió identificar oportunidades claras de mejora en inventario, marketing y experiencia del cliente, sentando las bases para una solución predictiva más robusta en etapas futuras.
