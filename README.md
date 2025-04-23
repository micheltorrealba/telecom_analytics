# 📍 Análisis del Acceso a Internet y las Brechas de Conectividad en las Provincias de Argentina (2024)

## 🧠 Contexto y Objetivo

En la actualidad, el acceso a internet es un factor determinante para el desarrollo económico, social y educativo de cualquier región. En Argentina, a pesar de contar con un número considerable de conexiones, persisten grandes desigualdades entre provincias en términos de cobertura, velocidad de navegación y adopción de tecnologías como la fibra óptica.

Este proyecto fue desarrollado con el objetivo de brindar a una empresa prestadora de servicios de telecomunicaciones una visión clara del estado actual del acceso a internet en todo el país. A través del análisis exploratorio de datos y visualizaciones interactivas, se busca:

- Evaluar el nivel de conectividad por provincia.
- Identificar las regiones con mayor brecha digital.
- Estimar el impacto potencial de una mejora del 2% en la cobertura.
- Proponer KPIs relevantes para la toma de decisiones.

## 💡 Hipótesis

A pesar de que Argentina cuenta con una importante infraestructura de telecomunicaciones en términos generales, existen marcadas desigualdades entre provincias en cuanto a la disponibilidad, calidad y tecnología del servicio de internet. Se espera encontrar que las provincias con menor densidad poblacional y menor desarrollo económico presentan los niveles más bajos de acceso y menor adopción de fibra óptica.

## 📊 KPIs definidos

Durante el desarrollo del proyecto se definieron cuatro indicadores clave (KPIs) con el objetivo de cuantificar y monitorear los aspectos más relevantes del acceso a internet en las provincias de Argentina. Estos KPIs permiten analizar la situación actual, proyectar mejoras y priorizar decisiones de inversión en conectividad.

### 🟡 KPI 1 – Proyección de incremento de acceso (+2%)
**Objetivo:** Medir el impacto de un aumento del 2% en el acceso a internet por cada 100 hogares en cada provincia.  
**Fórmula:** ((Nuevo acceso - Acceso actual) / Acceso actual) * 100  
**Visualización:** Gráfico de barras agrupadas por provincia y tarjeta resumen.

### 🟡 KPI 2 – Porcentaje de acceso por fibra óptica
**Objetivo:** Identificar la penetración de tecnología de alta velocidad (fibra óptica) en cada provincia.  
**Fórmula:** (Conexiones por fibra óptica / Total de conexiones) * 100  
**Visualización:** Mapa de calor interactivo por provincia y gráfico de barras.

### 🟡 KPI 3 – Habitantes sin acceso a internet
**Objetivo:** Detectar las provincias con mayor cantidad absoluta de personas excluidas digitalmente.  
**Fórmula:** Población estimada - (Accesos por cada 100 hab. * Población / 100)  
**Visualización:** Gráfico de barras horizontal y tarjeta resumen.

### 🟡 KPI 4 – Habitantes con acceso estimado (+2%)
**Objetivo:** Estimar la cantidad total de personas que ganarían acceso a internet si se implementara el aumento proyectado.  
**Fórmula:** (Accesos por cada 100 hab. * 1.02) * Población / 100  
**Visualización:** Gráfico de comparación lado a lado y tarjeta resumen.

### 🟡 KPI 5 – Velocidad promedio nacional
**Objetivo:** Ofrecer una métrica global de calidad del servicio.  
**Fórmula:** Promedio simple de la velocidad de bajada por provincia.  
**Visualización:** Tarjeta resumen de velocidad promedio y gráfico de barras por provincia.

## 🔍 Exploratory Data Analysis (EDA) y Metodología

### 🗃️ Fuentes y preparación de los datos

Se trabajó con el dataset oficial de ENACOM y fuentes complementarias oficiales que contienen información sobre el acceso a internet en Argentina, distribuidos por provincia. Entre los datos analizados se incluyeron:

- Accesos por cada 100 hogares y habitantes.
- Tecnología de conexión (fibra óptica, cablemodem, ADSL, etc.).
- Velocidad promedio de bajada (Mbps).
- Población estimada por provincia.

Los datos fueron limpiados y unificados en un único archivo `.csv`, manteniendo como estructura central el desglose por provincia. Se ajustaron valores nulos, se homogeneizaron nombres de provincias y se agregaron columnas calculadas para facilitar el análisis de KPIs. También se verificó que el archivo final fuera compatible con Tableau como única fuente de datos.

### 🧪 Análisis exploratorio

El EDA fue realizado en un notebook de Python con Pandas, y se centró en:

- Detección de valores faltantes o inconsistencias.
- Visualización de distribuciones por tecnología y velocidad.
- Identificación de outliers en indicadores clave.
- Verificación de correlaciones iniciales entre población, acceso y tecnología.

Cada paso fue documentado en el notebook con sus respectivas visualizaciones y conclusiones parciales.

### ⚙️ Metodología aplicada

1. **Unificación de datos:** Consolidación de múltiples fuentes y transformación de datos brutos en métricas útiles.
2. **Cálculo de KPIs personalizados:** Aplicación de fórmulas específicas adaptadas a los objetivos del análisis.
3. **Visualización y diseño del dashboard:** Creación de visualizaciones interactivas en Tableau Public, manteniendo consistencia visual y claridad narrativa.
4. **Construcción de filtros dinámicos:** Implementación de filtros por provincia para permitir una exploración profunda.

## 📈 Conclusiones

1. **Desigualdad en el acceso:** Provincias como La Pampa y Formosa no alcanzan el 50% de acceso por hogar, mientras que otras superan el 100%.
2. **Impacto del aumento del 2%:** Provincias con alta población como Buenos Aires podrían sumar millones de nuevos usuarios.
3. **Brecha digital:** Buenos Aires lidera en cantidad de habitantes sin acceso, lo que urge su priorización.
4. **Velocidad desigual:** San Luis y CABA tienen velocidades muy superiores al promedio; Chubut y Tierra del Fuego, muy por debajo.
5. **Adopción de fibra óptica baja en regiones clave:** Especialmente en Buenos Aires, Santiago del Estero y La Rioja.

## 📝 Recomendaciones

1. **Priorizar inversiones en provincias con baja penetración y alta población:** Buenos Aires, La Pampa, Tierra del Fuego y Chubut.
2. **Aplicar metas escalables por provincia:** Mejoras como el 2% permiten planificar por trimestres.
3. **Expandir la fibra óptica en regiones con base instalada:** Como Santa Fe, Mendoza o Córdoba.
4. **Considerar el contexto socioeconómico:** No analizar solo números duros; tener en cuenta la densidad y el poder adquisitivo por provincia.

## 📂 Archivos del Repositorio

- `telecom_dataset_final_ok_24provincias.csv`: Dataset final limpio con todas las columnas calculadas para el dashboard.
- `EDA_notebook.ipynb`: Notebook en Python con el análisis exploratorio completo y visualizaciones iniciales.
- `dashboard_tableau.png`: Captura del dashboard interactivo.
- `README.md`: Documento principal con toda la información del proyecto.

## 👨‍💻 Autor

Michel Torrealba  
Analista de Datos

