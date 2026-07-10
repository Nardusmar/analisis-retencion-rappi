# 📊 Análisis de Rentabilidad y Retención de Usuarios – Caso Rappi

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?logo=pandas)
![SQL](https://img.shields.io/badge/SQL-PostgreSQL-4169E1?logo=postgresql)
![PowerBI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?logo=powerbi)
![Status](https://img.shields.io/badge/Status-Completado-brightgreen)

## 📌 Descripción del proyecto

Análisis de rentabilidad y retención de usuarios para un caso de estudio inspirado en Rappi,
enfocado en entender por qué los usuarios abandonan el proceso de compra (funnel) y qué impacto
tiene esto en la rentabilidad del negocio. El resultado es un dashboard interactivo que sirvió
como base evidenciada estadísticamente para decisiones de retención.

> **Nota:** Este es un proyecto de práctica/portafolio. [Aquí aclara si usaste datos públicos,
> simulados, o un dataset de un curso — reemplaza esta nota con el detalle real].

## 🎯 Objetivos

- Mapear el funnel completo del usuario (registro → navegación → carrito → checkout → compra)
- Identificar en qué etapa del funnel se concentra el mayor abandono
- Validar estadísticamente si el checkout es un punto crítico de fuga de usuarios
- Traducir los hallazgos en un dashboard accionable para el equipo de negocio

## 🗂️ Fuente de los datos

- **Origen:**
https://practicum-content.s3.amazonaws.com/datasets/rappiplus_orders_raw.csv
https://practicum-content.s3.amazonaws.com/datasets/rappiplus_catalog.csv
https://practicum-content.s3.amazonaws.com/datasets/rappiplus_marketing_spend.csv
- **Periodo analizado:** Enero 2025 - Junio 2025
- **Variables clave:** usuario, etapa del funnel, timestamp, monto de la orden, método de pago, etc.

## 🛠️ Herramientas utilizadas

| Herramienta | Uso |
|---|---|
| SQL | Extracción y consolidación de datos de usuarios y transacciones |
| Python (Pandas) | Limpieza, transformación y cálculo de métricas de funnel |
| Power BI | Construcción del dashboard interactivo de rentabilidad y retención |

## 🔍 Metodología

1. **Extracción de datos** con SQL desde las tablas de usuarios, órdenes y eventos del funnel
2. **Limpieza y transformación** en Python: cálculo de tasas de conversión por etapa
3. **Análisis estadístico** para validar si la caída en checkout era significativa (no solo ruido)
4. **Construcción del dashboard** en Power BI para visualizar el funnel y métricas de rentabilidad

## 📈 Hallazgos clave

![Funnel de conversión](img/funnel_conversion.png)

- 🔑 El **checkout** se identificó como el punto crítico de mayor abandono dentro del funnel
- 🔑 El cambio de checkout probado se validó **con evidencia estadística**, confirmando que el
  aumento/caída en la tasa de abandono no era producto del azar
- 🔑 El dashboard permitió cuantificar el impacto de este abandono en la rentabilidad general

*(Reemplaza estos puntos con tus números reales: ej. "el 42% de los usuarios abandonaban en
checkout" o "el nuevo diseño redujo el abandono en 8 puntos porcentuales, p-value < 0.05")*

## 💡 Recomendaciones de negocio

- Priorizar rediseño del checkout como palanca de retención de alto impacto
- Monitorear la tasa de conversión por etapa como KPI recurrente
- [agrega tus recomendaciones específicas]

## 📁 Estructura del repositorio

```
analisis-retencion-rappi/
├── data/
│   ├── raw/
│   └── processed/
├── sql/
│   └── extraccion_funnel.sql
├── notebooks/
│   └── 01_limpieza_y_analisis.ipynb
├── dashboard/
│   └── retencion_rentabilidad.pbix
├── img/
│   └── funnel_conversion.png
├── requirements.txt
└── README.md
```

## ▶️ Cómo reproducir este análisis

```bash
git clone https://github.com/tu-usuario/analisis-retencion-rappi.git
cd analisis-retencion-rappi
pip install -r requirements.txt
jupyter notebook notebooks/01_limpieza_y_analisis.ipynb
```

Para ver el dashboard, abre `dashboard/retencion_rentabilidad.pbix` con Power BI Desktop.

## 👤 Autor

**Tu Nombre**
[LinkedIn](www.linkedin.com/in/nardeth-martinez-rodriguez) · [Portafolio](https://nardusmar.github.io/)
