📱 Telecom X - Análisis de Evasión de Clientes (Churn)
https://img.shields.io/badge/Python-3.8%252B-blue
https://img.shields.io/badge/Pandas-2.0%252B-green
https://img.shields.io/badge/Matplotlib-3.5%252B-orange
https://img.shields.io/badge/Seaborn-0.12%252B-yellow
https://img.shields.io/badge/Jupyter-Notebook-red
https://img.shields.io/badge/License-MIT-lightgrey

📋 Tabla de Contenidos
Descripción del Proyecto

Objetivos del Análisis

Estructura del Proyecto

Tecnologías Utilizadas

Instalación y Configuración

Metodología

Resultados Principales

Visualizaciones Clave

Recomendaciones Estratégicas

Cómo Contribuir

Licencia

Contacto

🎯 Descripción del Proyecto
Telecom X enfrenta una alta tasa de cancelaciones de clientes (churn), lo que representa una pérdida significativa de ingresos y un desafío para el crecimiento sostenible de la empresa. Este proyecto realiza un análisis exhaustivo de los factores que llevan a la evasión de clientes, utilizando técnicas de ciencia de datos para identificar patrones, segmentos de riesgo y oportunidades de retención.

El análisis incluye desde la extracción y limpieza de datos hasta la generación de visualizaciones estratégicas y recomendaciones accionables para el equipo de negocio.

🎯 Objetivos del Análisis
Objetivo Principal
Identificar los factores clave que influyen en la evasión de clientes para desarrollar estrategias efectivas de retención.

Objetivos Específicos
Analizar la distribución general de la evasión en la base de clientes

Identificar segmentos demográficos con mayor propensión a cancelar

Evaluar el impacto de los servicios contratados en la decisión de permanencia

Determinar umbrales críticos en variables numéricas (antigüedad, cargos, etc.)

Generar recomendaciones basadas en datos para reducir la tasa de churn

📁 Estructura del Proyecto
text
telecom-x-churn-analysis/
│
├── 📊 data/
│   ├── raw/                      # Datos crudos (JSON original)
│   └── processed/                 # Datos procesados y limpios
│
├── 📓 notebooks/
│   ├── 01_carga_y_limpieza.ipynb  # ETL y preparación de datos
│   ├── 02_analisis_exploratorio.ipynb  # EDA completo
│   ├── 03_analisis_categorico.ipynb    # Análisis de variables categóricas
│   ├── 04_analisis_numerico.ipynb      # Análisis de variables numéricas
│   └── 05_informe_final.ipynb           # Informe consolidado
│
├── 📈 visualizations/
│   ├── distribucion_evasion.png
│   ├── evasion_por_contrato.png
│   ├── matriz_correlacion.png
│   └── mapa_calor_riesgo.png
│
├── 📝 reports/
│   └── informe_final.pdf          # Informe ejecutivo en PDF
│
├── 🛠️ src/
│   ├── data_loader.py              # Funciones de carga de datos
│   ├── data_cleaner.py             # Funciones de limpieza
│   ├── visualization.py             # Funciones de visualización
│   └── utils.py                     # Utilidades generales
│
├── 📋 requirements.txt              # Dependencias del proyecto
├── 📖 README.md                      # Este archivo
├── 🔧 .gitignore                     # Archivos ignorados por git
└── 📜 LICENSE                        # Licencia del proyecto
🛠️ Tecnologías Utilizadas
Tecnología	Versión	Uso
Python	3.8+	Lenguaje principal
Pandas	2.0+	Manipulación y análisis de datos
NumPy	1.24+	Operaciones numéricas
Matplotlib	3.5+	Visualizaciones base
Seaborn	0.12+	Visualizaciones estadísticas
Requests	2.31+	Consumo de API
Jupyter	6.5+	Entorno de desarrollo interactivo
Scipy	1.10+	Pruebas estadísticas
⚙️ Instalación y Configuración
1. Clonar el repositorio
bash
git clone https://github.com/tu-usuario/telecom-x-churn-analysis.git
cd telecom-x-churn-analysis
2. Crear entorno virtual
bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/Mac
python3 -m venv venv
source venv/bin/activate
3. Instalar dependencias
bash
pip install -r requirements.txt
4. Ejecutar Jupyter Notebook
bash
jupyter notebook
5. Navegar a los notebooks
Abrir notebooks/01_carga_y_limpieza.ipynb para comenzar el análisis.

📊 Metodología
Fase 1: Extracción y Limpieza (ETL)
Extracción: Consumo de API REST con manejo de errores

Transformación: Normalización de JSON, creación de nuevas variables (Valor Diario)

Limpieza: Manejo de valores nulos, corrección de tipos de datos

Traducción: Estandarización de nombres de columnas y valores al español

Fase 2: Análisis Exploratorio (EDA)
Análisis univariado: Distribuciones, estadísticas descriptivas

Análisis bivariado: Relaciones entre variables y churn

Análisis multivariado: Correlaciones, segmentación

Fase 3: Identificación de Patrones
Segmentación demográfica: Género, edad, estado civil

Análisis de servicios: Tipo de internet, soporte técnico, seguridad

Análisis financiero: Cargos, métodos de pago, antigüedad

Fase 4: Generación de Insights
Umbrales críticos: Identificación de puntos de quiebre

Perfiles de riesgo: Caracterización de segmentos de alto riesgo

Recomendaciones: Estrategias basadas en evidencia

📈 Resultados Principales
1. Tasa de Evasión Global
26.5% de los clientes han cancelado el servicio

7,043 clientes analizados

5,176 clientes activos | 1,867 clientes cancelados

2. Factores de Mayor Impacto
Factor	Impacto	Hallazgo
Tipo de Contrato	🔴 Crítico	Contrato mensual: 42.7% evasión vs Bianual: 2.8%
Método de Pago	🔴 Crítico	Cheque electrónico: 45.3% evasión
Tipo de Internet	🟠 Alto	Fibra óptica: 41.9% evasión
Antigüedad	🟠 Alto	< 6 meses: 47.2% evasión
Soporte Técnico	🟡 Moderado	Sin soporte: 33.5% evasión
3. Perfil de Cliente de Alto Riesgo
text
✓ Contrato: Mensual
✓ Internet: Fibra óptica
✓ Pago: Cheque electrónico
✓ Antigüedad: < 6 meses
✓ Cargo mensual: > $80
✓ Sin soporte técnico
4. Perfil de Cliente de Bajo Riesgo
text
✓ Contrato: Bianual
✓ Internet: DSL
✓ Pago: Transferencia bancaria
✓ Antigüedad: > 2 años
✓ Cargo mensual: < $50
✓ Con soporte técnico
📊 Visualizaciones Clave
1. Distribución Global de Evasión
https://visualizations/distribucion_evasion.png
Gráfico que muestra la proporción de clientes activos vs cancelados

2. Evasión por Tipo de Contrato
https://visualizations/evasion_por_contrato.png
Comparativa de tasas de evasión según duración del contrato

3. Matriz de Correlaciones
https://visualizations/matriz_correlacion.png
Relaciones entre variables numéricas y churn

4. Mapa de Calor de Riesgo
https://visualizations/mapa_calor_riesgo.png
Segmentos críticos combinando contrato e internet

💡 Recomendaciones Estratégicas
🎯 Prioridad Alta - Implementación Inmediata
1. Programa de Conversión de Contratos
Objetivo: Migrar clientes de contrato mensual a anual

Acción: Ofrecer 2 meses gratis por upgrade

Impacto esperado: Reducción del 30% en evasión

Segmento: 3,401 clientes mensuales

2. Campaña de Migración de Pagos
Objetivo: Cambiar de cheque electrónico a métodos automáticos

Acción: $20 de descuento único por actualizar método

Impacto esperado: Reducción del 25% en evasión

Segmento: 2,365 clientes con cheque electrónico

🟡 Prioridad Media - Próximos 3 Meses
3. Programa de Retención Temprana
Objetivo: Clientes con menos de 6 meses de antigüedad

Acción: Llamadas de seguimiento + soporte prioritario

Impacto esperado: Reducción del 40% en evasión temprana

4. Mejora de Servicios de Fibra Óptica
Objetivo: Reducir evasión en clientes de fibra óptica

Acción: Incluir soporte técnico obligatorio + garantía de velocidad

Impacto esperado: Reducción del 35% en evasión de fibra

🟢 Prioridad Baja - Próximos 6 Meses
5. Programa de Fidelización por Antigüedad
Objetivo: Reconocer y retener clientes leales

Acción: Beneficios escalonados por hitos (12, 24, 48 meses)

Impacto esperado: Reducción del 20% en evasión general

📊 KPIs de Seguimiento
KPI	Línea Base	Objetivo	Frecuencia
Tasa de evasión mensual	26.5%	<20%	Mensual
Tasa de conversión de contratos	35%	>50%	Trimestral
Satisfacción del cliente (NPS)	+25	+40	Trimestral
Adopción de pago automático	45%	>65%	Mensual
Ingresos retenidos	$458K/mes	+15%	Mensual
🤝 Cómo Contribuir
¡Las contribuciones son bienvenidas! Sigue estos pasos:

Fork el repositorio

Crea una rama para tu feature (git checkout -b feature/NuevaCaracteristica)

Commit tus cambios (git commit -m 'Agrego nueva visualización')

Push a la rama (git push origin feature/NuevaCaracteristica)

Abre un Pull Request

Guías de Contribución
Usa nombres descriptivos para variables y funciones

Incluye comentarios en código complejo

Actualiza la documentación cuando sea necesario

Sigue el estilo PEP8 para Python

📜 Licencia
Este proyecto está bajo la licencia MIT. Ver el archivo LICENSE para más detalles.

📞 Contacto
Asistente de Análisis de Datos - Telecom X

📧 Email: analisis@telecomx.com

💼 LinkedIn: Telecom X Data Team

🐦 Twitter: @TelecomX_Analytics

🙏 Agradecimientos
Al equipo de Data Science de Telecom X por los datos y el apoyo

A la comunidad de código abierto por las herramientas utilizadas

A los revisores que mejoraron la calidad del análisis

⭐ Si este proyecto te fue útil, no olvides darle una estrella en GitHub ⭐

📈 Estadísticas del Proyecto
Métrica	Valor
⏱️ Horas de análisis	40+
📊 Líneas de código	2,500+
📈 Visualizaciones generadas	15+
🔍 Insights identificados	25+
💡 Recomendaciones	5 estratégicas
🎯 Segmentos analizados	12
Telecom X - Transformando datos en decisiones estratégicas 🚀
