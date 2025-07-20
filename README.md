📄 Informe Final – Análisis de Evasión de Clientes (Churn)

🎯 Introducción

El presente análisis tiene como objetivo identificar patrones asociados a la evasión de clientes (churn) en una compañía de telecomunicaciones. Detectar estos patrones es clave para desarrollar estrategias de retención y fidelización, aumentando la rentabilidad del negocio.

🧼 Limpieza y Tratamiento de Datos

Los datos fueron extraídos directamente desde una API pública (repositorio GitHub).
Se identificaron estructuras anidadas (customer, phone, internet, account) que fueron aplanadas para facilitar el análisis.
Se eliminaron registros con campos vacíos en la columna Churn.
Se convirtieron campos numéricos y se creó la variable Cuentas_Diarias como derivada del cargo mensual.
Se estandarizaron valores binarios (Yes/No → 1/0) para su uso en modelos y visualizaciones.
Columnas clave fueron renombradas para mayor legibilidad: CargoMensual, CargoTotal, TenureMeses.

📊 Análisis Exploratorio de Datos

🔹 Distribución General
La evasión (Churn) muestra una proporción significativa de clientes que abandonan la empresa.
La variable objetivo fue correctamente binarizada para facilitar segmentación y predicción.

🔹 Variables Categóricas
El tipo de contrato muestra fuerte correlación con churn:
Contratos mensuales tienen mayor tasa de evasión.
Contratos a largo plazo muestran mayor fidelización.

🔹 Variables Numéricas
Clientes con mayor cargo mensual tienden a mostrar mayor churn.
Clientes con mayor tiempo de permanencia (tenure) son menos propensos a cancelar.

🔎 Conclusiones e Insights
El tipo de contrato es el principal predictor de evasión.
Clientes con cargos elevados y corto tiempo en la compañía son más propensos a cancelar.
La mayoría de evasiones se concentran en contratos sin compromiso a largo plazo.

🧭 Recomendaciones Estratégicas
Incentivar contratos anuales o bianuales, con beneficios adicionales para nuevos clientes.
Segmentar campañas de retención para quienes tienen cargos mensuales altos.
Crear alertas preventivas con modelos predictivos para detectar riesgo de churn.

✅ Próximo paso sugerido
Entrenar un modelo de clasificación (Logistic Regression, Random Forest, etc.) con estas variables para predecir la evasión y tomar decisiones proactivas.
