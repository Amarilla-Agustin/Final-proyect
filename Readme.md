# Análisis de Adopción y Uso de Inteligencia Artificial en Empresas

## 📊 Descripción del proyecto

Este proyecto analiza los patrones de **adopción y uso de herramientas de Inteligencia Artificial (IA) en empresas**, con el objetivo de identificar qué factores están asociados con una mayor adopción y cuáles generan un mayor nivel de uso diario.

El análisis busca responder una pregunta de negocio concreta: **¿qué características de una empresa y de las herramientas utilizadas pueden explicar el éxito en la adopción de IA?**

A partir del análisis de variables relacionadas con el **tamaño de la empresa, industria, herramienta de IA, año, tasa de adopción y usuarios activos diarios**, se buscan patrones que permitan formular recomendaciones para la toma de decisiones sobre inversión y estrategia tecnológica.

> **Enfoque:** este proyecto se plantea como un caso de análisis real, donde los datos se utilizan para responder preguntas de negocio y no únicamente para generar visualizaciones.

---

## 🎯 Pregunta principal

> **¿Qué factores —tipo de herramienta, industria y tamaño de empresa— determinan el éxito en la adopción y uso diario de IA, y dónde están las mayores oportunidades de inversión tecnológica para las empresas?**

---

## 💡 Objetivo del análisis

Identificar patrones de éxito en la implementación de Inteligencia Artificial para **recomendar estrategias de digitalización a empresas según su industria y tamaño**, buscando maximizar tanto la adopción como el uso activo de las herramientas.

El análisis pretende pasar de los datos a conclusiones accionables, identificando:

- Qué tamaños de empresa presentan mayores niveles de adopción.
- Qué industrias muestran una mayor utilización de IA.
- Qué tipos de herramientas predominan según la industria.
- Cómo evolucionó la adopción entre 2023 y 2024.
- Qué herramientas presentan mayores niveles de engagement.
- Qué oportunidades de inversión tecnológica pueden identificarse a partir de estos patrones.

---

## 🔎 Preguntas secundarias

El análisis se estructura alrededor de cuatro preguntas:

### 1. Adopción según tamaño de empresa

**¿Existen diferencias significativas en la tasa de adopción entre Startups, PyMEs (SME) y grandes corporaciones (Enterprise)?**

Se compararán los niveles de adopción entre los distintos tamaños de empresa para determinar si la estructura y dimensión organizacional están relacionadas con la velocidad de incorporación de IA.

**Métricas principales:**

- Promedio de `adoption_rate`
- Mediana de `adoption_rate`
- Distribución de la tasa de adopción

**Visualización propuesta:** Boxplot.

**Decisión de negocio:** orientar estrategias comerciales y de consultoría de IA hacia los segmentos con mayor potencial de adopción.

---

### 2. Uso de IA generativa según industria

**¿Qué industrias lideran el uso de IA generativa de texto frente a herramientas de generación de imágenes?**

Las herramientas serán clasificadas en categorías de uso, permitiendo comparar los patrones de adopción entre IA generativa de texto e IA generativa de imágenes.

**Variables principales:**

- `industry`
- `ai_tool`
- `adoption_rate`

**Transformaciones:**

- Clasificación de las herramientas según tipo de IA.
- Agrupación por industria.
- Tabla pivote para comparar categorías.

**Métrica principal:**

- Tasa de adopción promedio por categoría.

**Visualización propuesta:** Barras apiladas al 100%.

**Decisión de negocio:** determinar qué tipos de licencias, herramientas y capacitaciones podrían resultar más relevantes según la industria.

---

### 3. Evolución de la adopción

**¿Cómo evolucionó la tasa de adopción promedio y el volumen de usuarios diarios entre 2023 y 2024?**

Se analizará la evolución temporal de la adopción, comparando los resultados entre años y, cuando corresponda, entre industrias.

**Variables principales:**

- `year`
- `industry`
- `adoption_rate`
- `daily_active_users`

**Métricas:**

- Tasa de adopción promedio.
- Variación interanual.
- Evolución de usuarios activos diarios.

**Visualización propuesta:**

- Gráfico de líneas.
- Barras agrupadas.
- Slope chart para comparaciones entre períodos.

**Decisión de negocio:** evaluar la velocidad de crecimiento de la adopción y determinar si existe una necesidad creciente de inversión en IA.

---

### 4. Engagement por herramienta

**¿Qué herramientas generan mayor retención o engagement medido a través de usuarios activos diarios (DAU)?**

La tasa de adopción no necesariamente implica un uso intensivo. Por este motivo, se analizará el volumen de usuarios activos diarios para identificar qué herramientas generan mayor utilización efectiva.

**Variables principales:**

- `ai_tool`
- `daily_active_users`

**Métrica principal:**

- Promedio de `daily_active_users` por herramienta.

**Visualización propuesta:** Barras horizontales ordenadas.

**Decisión de negocio:** identificar qué herramientas podrían ser candidatas para una estrategia de estandarización o adopción institucional.

---

# 🧠 Hipótesis iniciales

Antes de realizar el análisis se plantean las siguientes hipótesis:

### Hipótesis 1 — Tamaño de empresa

> **Las Startups presentan una tasa de adopción general mayor que las Enterprises**, debido a una mayor agilidad organizacional y una menor cantidad de niveles burocráticos para incorporar nuevas tecnologías.

### Hipótesis 2 — Tipo de herramienta e industria

> **ChatGPT y otras herramientas de IA generativa de texto presentan una adopción transversal entre industrias**, mientras que las herramientas de generación de imágenes presentan niveles de adopción especialmente elevados en determinados sectores creativos y comerciales.

### Hipótesis 3 — Evolución temporal

> **La adopción de IA aumentó significativamente entre 2023 y 2024**, reflejando una aceleración general en la incorporación de estas tecnologías por parte de las empresas.

Las hipótesis serán contrastadas con los datos y **no se asumirán como conclusiones previamente confirmadas**.

---

# 📐 Metodología

El análisis seguirá un proceso de trabajo orientado a responder las preguntas planteadas:

### 1. Exploración de los datos

- Identificación de variables.
- Análisis de tipos de datos.
- Detección de valores nulos.
- Identificación de posibles valores atípicos.
- Análisis de la distribución de las variables principales.

### 2. Preparación y transformación

Se realizarán las transformaciones necesarias para poder responder las preguntas de negocio, incluyendo:

- Agrupaciones mediante `groupby`.
- Cálculo de estadísticas descriptivas.
- Creación de nuevas variables.
- Clasificación de herramientas por tipo.
- Tablas pivote.
- Cálculo de variaciones interanuales.

### 3. Análisis exploratorio

Se utilizarán diferentes visualizaciones para identificar patrones y diferencias entre:

- Tamaños de empresa.
- Industrias.
- Herramientas.
- Tipos de IA.
- Períodos de tiempo.

### 4. Interpretación

Los resultados serán interpretados desde una perspectiva de negocio, buscando responder:

> **¿Qué significa este resultado y qué decisión podría apoyar?**

El objetivo no será únicamente describir los datos, sino transformar los resultados en **insights accionables**.

---

# 📌 KPIs principales

| KPI                          | Descripción                                         |
| ---------------------------- | --------------------------------------------------- |
| **Adoption Rate**            | Tasa de adopción de herramientas de IA              |
| **Daily Active Users (DAU)** | Usuarios activos diarios de cada herramienta        |
| **Adopción promedio**        | Promedio de adopción según segmento                 |
| **Mediana de adopción**      | Valor central de la distribución de adopción        |
| **Variación interanual**     | Cambio porcentual entre 2023 y 2024                 |
| **Adopción por industria**   | Nivel promedio de adopción dentro de cada industria |
| **Adopción por tipo de IA**  | Comparación entre herramientas de texto e imagen    |

---

# 📈 Resultados y hallazgos

> Esta sección se completará una vez finalizado el análisis exploratorio.

Se documentarán los principales hallazgos encontrados en los datos, priorizando aquellos que tengan relevancia para la toma de decisiones.

Para cada hallazgo se buscará responder:

1. **¿Qué encontramos?**
2. **¿Qué evidencia lo demuestra?**
3. **¿Por qué es relevante?**
4. **¿Qué decisión podría apoyar?**

### Hallazgo 1

*Pendiente de análisis.*

### Hallazgo 2

*Pendiente de análisis.*

### Hallazgo 3

*Pendiente de análisis.*

---

# 💼 Conclusiones y recomendaciones

> Esta sección se completará luego de contrastar las hipótesis y analizar los resultados.

Las conclusiones estarán orientadas a transformar los principales insights en recomendaciones concretas para la estrategia de adopción de IA.

Se buscará determinar:

- Qué segmentos presentan mayor potencial.
- Qué industrias muestran oportunidades de crecimiento.
- Qué herramientas tienen mayor nivel de engagement.
- Qué tendencias justifican nuevas inversiones.
- Qué estrategia de adopción podría recomendarse según el perfil de la empresa.

---

# 📂 Estructura del repositorio

```text
├── README.md
├── proyecto_final.ipynb
├── data/
│   └── dataset.csv
└── presentacion/
    └── presentacion_final.pdf
```

### Archivos principales
<!-- pendiente a cambiar cuando hagamos todo -->
**`proyecto_final.ipynb`**

Notebook principal que contiene:

- Exploración de datos.
- Limpieza y transformación.
- Análisis.
- Visualizaciones.
- Interpretación de resultados.
- Conclusiones.

**`data/`**

Contiene el dataset utilizado en el análisis o, en caso de no poder distribuirse directamente, la referencia a su fuente.

**`presentacion/`**

Contiene las diapositivas utilizadas para presentar los resultados.

---

# ▶️ Cómo ejecutar el proyecto

### Requisitos

- Python 3.x
- Jupyter Notebook o JupyterLab
- Pandas
- NumPy
- Matplotlib
- Seaborn

<!-- pendiente a actualizar al terminar el proyecto -->
### Instalación

Clonar el repositorio:

```bash
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_REPOSITORIO>
```

Instalar las dependencias:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

Ejecutar Jupyter Notebook:

```bash
jupyter notebook
```

Abrir:
<!-- pendiente a cambio -->
```text
proyecto_final.ipynb
```

y ejecutar las celdas en orden.

---

# 🎤 Presentación

Los resultados del análisis se presentan en una presentación de **5 a 10 minutos**, orientada a una audiencia de negocio.

La presentación sigue la siguiente estructura:

1. **Resumen ejecutivo**

   - Hallazgo principal.
   - Recomendación principal.

2. **Problema**

   - Pregunta de negocio.

3. **Dataset**

   - Fuente y variables relevantes.

4. **Metodología**

   - Cómo se abordó el problema.

5. **KPIs**

   - Métricas utilizadas.

6. **Hallazgos**

   - Principales resultados.

7. **Conclusiones**

   - Insights y recomendaciones.

> **La presentación prioriza la comunicación de resultados sobre los aspectos técnicos. No se incluye código.**

---

# 🛠️ Tecnologías utilizadas

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**
- **Git / GitHub**

---

# 👤 Autor

**Agustín Amarilla, Guillermo Kafka**

Proyecto final — Análisis de Datos - Comunidad IT
