# 📱 Telecom X - Análisis de Evasión de Clientes (Churn)

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-green)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.5%2B-orange)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-0.12%2B-yellow)](https://seaborn.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-red)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](LICENSE)

</div>

## 📋 Tabla de Contenidos
- [Descripción del Proyecto](#-descripción-del-proyecto)
- [Acceso al Análisis Detallado](#-acceso-al-análisis-detalladoo)
- [Objetivos del Análisis](#-objetivos-del-análisis)
- [Dataset](#-dataset)
- [Tecnologías Utilizadas](#-tecnologías-utilizadas)
- [Metodología](#-Metodología)
- [Resultados Principales](#-resultados-principales)
- [Recomendaciones Estratégicas](#-recomendaciones-estratégicas)
- [KPIs de Seguimiento](#-kpis-de-seguimiento)
- [Autores](#-autores)

---

## 🎯 Descripción del Proyecto

**Telecom X** enfrenta una alta tasa de cancelaciones de clientes (*churn*). Este proyecto realiza un análisis exhaustivo de los factores que llevan a la evasión, utilizando técnicas de ciencia de datos para identificar patrones de riesgo y generar oportunidades de retención basadas en evidencia.

### 🔗 Acceso al Análisis Detallado
Puedes ver el desarrollo completo del proyecto en el siguiente notebook de Jupyter:
[**`Desafío_Telecom_X_Edward_Tuanama.ipynb`**](https://github.com/Tuanama21/Challenge-Telecom-X-an-lisis-de-evasi-n-de-clientes---Edward-Tuanama/blob/main/Desaf%C3%ADo_Telecom_X_Edward_Tuanama.ipynb)

---

## 🎯 Objetivos del Análisis

| # | Objetivo | Métrica de Éxito |
|---|----------|------------------|
| 1 | Analizar la distribución global de la evasión. | Calcular la tasa de churn actual. |
| 2 | Identificar los segmentos de clientes con mayor riesgo. | Segmentos con una tasa de churn >30%. |
| 3 | Evaluar el impacto de los diferentes servicios contratados. | Correlación significativa (positiva/negativa) con el churn. |
| 4 | Determinar umbrales críticos en variables como antigüedad o cargos. | Puntos de quiebre donde la probabilidad de churn aumenta drásticamente. |
| 5 | Generar recomendaciones accionables y priorizadas para retención. | Un plan de acción con impacto esperado cuantificado. |

---

## 📊 Dataset

| Característica | Descripción |
|----------------|-------------|
| **Fuente** | API REST (formato JSON) |
| **Registros** | 7,043 clientes |
| **Variables** | 21 características (demográficas, de servicios, financieras y de cuenta) |
| **Período** | Datos históricos de la relación con el cliente |

---

## 🛠️ Tecnologías Utilizadas

| Tecnología | Versión | Uso Principal |
| :--- | :--- | :--- |
| **Python** | 3.8+ | Lenguaje de programación principal. |
| **Pandas** | 2.0+ | Manipulación, limpieza y análisis de datos. |
| **NumPy** | 1.24+ | Operaciones numéricas y manejo de arreglos. |
| **Requests** | 2.31+ | Consumo de la API REST para la extracción de datos. |
| **Matplotlib** | 3.5+ | Creación de visualizaciones base. |
| **Seaborn** | 0.12+ | Visualizaciones estadísticas avanzadas y atractivas. |
| **Scipy** | 1.10+ | Realización de pruebas estadísticas. |
| **Jupyter** | 6.5+ | Entorno de desarrollo interactivo para el análisis. |

---

## ⚙️ Metodología

### Fase 1: Extracción, Transformación y Carga (ETL)
- **Extracción:** Consumo de la API REST con manejo de errores y reintentos.
- **Transformación:** Normalización de la estructura JSON anidada. Creación de nuevas variables, como el *Valor Diario* por cliente.
- **Limpieza:** Tratamiento de valores nulos y corrección de tipos de datos.
- **Estandarización:** Traducción y unificación de nombres de columnas y categorías al español para facilitar el análisis.

### Fase 2: Análisis Exploratorio de Datos (EDA)
- **Análisis Univariado:** Estudio de la distribución y estadísticas descriptivas de cada variable por separado.
- **Análisis Bivariado:** Exploración de la relación entre cada variable predictora y la variable objetivo (`Churn`).
- **Análisis Multivariado:** Identificación de correlaciones entre variables y creación de segmentos de clientes complejos.

### Fase 3: Identificación de Patrones y Perfiles de Riesgo
- **Segmentación:** Agrupación de clientes por características demográficas (género, edad), tipo de servicios (internet, soporte) y comportamiento financiero (método de pago, antigüedad).
- **Caracterización:** Definición de perfiles de clientes con alta propensión a la cancelación.

### Fase 4: Generación de Insights y Recomendaciones
- **Umbrales Críticos:** Determinación de puntos de quiebre numéricos (ej. "clientes con menos de 6 meses de antigüedad").
- **Síntesis:** Traducción de los hallazgos técnicos a un lenguaje de negocio claro.
- **Estrategia:** Formulación de un plan de acción con recomendaciones priorizadas y su impacto esperado.

---

## 📈 Resultados Principales

### 1. Tasa de Evasión Global
- Se identificó una **tasa de cancelación del 26.5%**.
- De un total de **7,043** clientes, **1,867** han cancelado el servicio, frente a **5,176** que permanecen activos.

### 2. Factores de Mayor Impacto en el Churn

| Factor | Impacto | Hallazgo Clave |
|:-------|:--------|:---------|
| **Tipo de Contrato** | 🔴 **Crítico** | Clientes con contrato mensual tienen una tasa de evasión del **42.7%**, mientras que en contratos bianuales es solo del **2.8%**. |
| **Método de Pago** | 🔴 **Crítico** | El uso de cheque electrónico se asocia con una evasión del **45.3%**, la más alta entre todos los métodos. |
| **Tipo de Internet** | 🟠 **Alto** | Clientes con servicio de fibra óptica presentan una tasa de churn del **41.9%**, significativamente mayor que en DSL. |
| **Antigüedad** | 🟠 **Alto** | Los nuevos clientes (< 6 meses) son los más propensos a irse, con una tasa del **47.2%**. |
| **Soporte Técnico** | 🟡 **Moderado** | La falta de soporte técnico o soporte básico incrementa la probabilidad de cancelación. |

---

## 💡 Recomendaciones Estratégicas

Basado en los hallazgos, se proponen las siguientes acciones, priorizadas por su impacto potencial.

### 🚨 Prioridad Alta - Implementación Inmediata

#### 1. Programa de Conversión de Contratos
- **Objetivo:** Migrar clientes de contrato mensual a anual o bianual.
- **Acción:** Ofrecer un incentivo atractivo, como 2 meses de servicio gratis o un descuento significativo en el primer año, al cambiar de contrato.
- **Impacto Esperado:** Reducción de hasta un 30% en la tasa de churn de este segmento.
- **Segmento Objetivo:** Los **3,401 clientes** actuales con contrato mensual.

#### 2. Campaña de Migración de Métodos de Pago
- **Objetivo:** Reducir el uso de cheque electrónico, promoviendo métodos automáticos (débito directo o tarjeta).
- **Acción:** Lanzar una campaña informativa sobre los beneficios y la seguridad del pago automático, ofreciendo un descuento único de $20 por actualizar el método.
- **Impacto Esperado:** Disminución del 25% en la evasión del segmento de alto riesgo por método de pago.
- **Segmento Objetivo:** Los **2,365 clientes** que pagan con cheque electrónico.

### 🟡 Prioridad Media - Próximos 3 Meses

#### 3. Programa de Retención Temprana ("Bienvenida Prolongada")
- **Objetivo:** Fidelizar a los clientes nuevos desde el inicio, combatiendo la alta evasión en los primeros 6 meses.
- **Acción:** Implementar un programa de llamadas de seguimiento al primer y tercer mes, ofrecer una línea de soporte prioritario y enviar tips para aprovechar mejor el servicio durante este período crítico.
- **Impacto Esperado:** Reducción del 40% en la tasa de churn de clientes con menos de 6 meses de antigüedad.

#### 4. Mejora de la Experiencia en Fibra Óptica
- **Objetivo:** Abordar la alta insatisfacción (reflejada en el churn) de los clientes de fibra óptica.
- **Acción:** Incluir el servicio de soporte técnico premium de forma gratuita en todos los paquetes de fibra. Implementar una garantía de velocidad de conexión.
- **Impacto Esperado:** Reducción del 35% en la evasión dentro del segmento de fibra óptica.

### 🟢 Prioridad Baja - Próximos 6 Meses

#### 5. Programa de Fidelización por Antigüedad
- **Objetivo:** Reconocer y recompensar la lealtad de los clientes de largo plazo, reduciendo la erosión base.
- **Acción:** Crear un programa de beneficios escalonados que se activen al alcanzar hitos de antigüedad (ej. 12, 24, 48 meses). Estos podrían incluir descuentos en servicios adicionales, upgrades gratuitos o acceso a eventos exclusivos.
- **Impacto Esperado:** Reducción del 20% en la tasa de churn general, mejorando la satisfacción de la base más estable.

---

### 📊 KPIs de Seguimiento

Para medir la efectividad de las acciones, se proponen los siguientes indicadores clave de rendimiento:

| KPI | Línea Base (Actual) | Objetivo (12 Meses) | Frecuencia |
|:-----|:-----------|:---------|:-----------|
| Tasa de evasión mensual (Churn Rate) | 26.5% | <20% | Mensual |
| % de clientes con contrato anual o bianual | 51% | >65% | Trimestral |
| Satisfacción del cliente (NPS) | +25 | +40 | Trimestral |
| % de adopción de pago automático | 45% | >65% | Mensual |
| Ingresos retenidos por acciones de retención | $458K/mes | +15% | Mensual |

---

### **Abre y ejecuta el notebook:**
    En la interfaz de Jupyter, navega hasta el archivo `Desafío_Telecom_X_Edward_Tuanama.ipynb` y ejecuta las celdas secuencialmente para reproducir el análisis.

---

## 👤 Autores

<div align="center">

### [**Edward Tuanama (Tuanama21)**](https://github.com/Tuanama21)

[![GitHub followers](https://img.shields.io/github/followers/Tuanama21?style=social)](https://github.com/Tuanama21)

</div>

---

## 📈 Estadísticas del Proyecto

| Métrica | Valor |
|:--------|:------|
| ⏱️ Horas de análisis | 40+ |
| 📊 Líneas de código | ~2,500 |
| 📈 Visualizaciones generadas | 15+ |
| 🔍 Insights identificados | 25+ |
| 💡 Recomendaciones estratégicas | 5 |
| 🎯 Segmentos de clientes analizados | 12 |

---

<div align="center">

⭐ **Si este proyecto te resultó útil o interesante, ¡no olvides darle una estrella en GitHub!** ⭐

Hecho con ❤️ por Edward Tuanama, con el apoyo de **#AluraLatam** y **#oraclenexteducation**.

</div>
[![GitHub Stars](https://img.shields.io/github/stars/Tuanama21?style=social)](https://github.com/Tuanama21)

</div>

¡Si te gustó este proyecto, no olvides dejar una estrella ⭐ en el repositorio!

<div align="center">
Hecho con ❤️ por <a href="[https://github.com/tu-usuario](https://github.com/Tuanama21)">Edward Tuanama Gracias a #AluraLatam y #oraclenexteducation! </a>
</div>
