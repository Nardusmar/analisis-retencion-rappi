# 📊 Análisis de Rentabilidad y Retención de Usuarios 

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?logo=pandas)
![SQL](https://img.shields.io/badge/SQL-PostgreSQL-4169E1?logo=postgresql)
![PowerBI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?logo=powerbi)
![Status](https://img.shields.io/badge/Status-Completado-brightgreen)

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1AG1FaJv3bNFCSsiR81VnzBuaSjN-JUGM/view?usp=sharing)
## 📌 Descripción del proyecto

Análisis de rentabilidad y retención de usuarios para un caso de estudio inspirado en Rappi,
enfocado en entender por qué los usuarios abandonan el proceso de compra (funnel) y qué impacto
tiene esto en la rentabilidad del negocio. El resultado es un dashboard interactivo que sirvió
como base evidenciada estadísticamente para decisiones de retención.

> **Nota:** Este es un proyecto de portafolio. Para este análisis utilizaremos la tabla events, que se encuentra almacenada en una base de datos.
⚙️ Importante: La conexión a esta base de datos se realizará desde el Jupyter Notebook.

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


-🔑 La retención es muy estable entre semanas — los usuarios que regresan en semana 1 tienden a seguir activos en semana 2 y 3. No hay caída drástica.
-🔑 Solo ~42% de usuarios regresa — más de la mitad de los usuarios no vuelve después de registrarse. Hay oportunidad de mejora con estrategias de reactivación (emails, notificaciones, ofertas).
-🔑 No hay diferencia significativa entre cohortes — el producto se comporta igual mes a mes, lo que indica consistencia pero también que no ha habido mejoras que aumenten la retención.
-🔑 Aunque el grupo de tratamiento muestra una tasa de conversión ligeramente mayor (16.29% vs 15.69%), la diferencia de 0.60 puntos porcentuales NO es estadísticamente significativa. Con un p-valor de 0.4319, hay un 43% de probabilidad de que esta diferencia sea simplemente por azar, muy por encima del 5% permitido.
-🔑 Cuentan con ingresos totatles por 9.64 miill. con una utilidad de 2.93 mill.

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

**Martha Nardeth Martínez**


[LinkedIn](www.linkedin.com/in/nardeth-martinez-rodriguez) · [Portafolio](https://nardusmar.github.io/)
