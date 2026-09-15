# Análisis de Adopción y Uso de Inteligencia Artificial en Empresas

## 📊 Descripción del proyecto

Este proyecto analiza los patrones de **adopción y uso de herramientas de Inteligencia Artificial (IA) en empresas**, con el objetivo de identificar qué factores están asociados con la adopción y con el nivel de uso diario.

El análisis busca responder una pregunta de negocio concreta:

> **¿Qué factores —tipo de herramienta, industria y tamaño de empresa— están asociados con el éxito en la adopción y uso diario de IA?**

A partir de variables relacionadas con el **tamaño de la empresa, industria, herramienta de IA, año, tasa de adopción y usuarios activos diarios**, se identifican patrones y se evalúa si estas variables permiten diferenciar niveles relevantes de adopción o engagement.

> **Enfoque:** el proyecto se plantea como un caso de análisis de datos orientado a responder preguntas concretas y transformar los resultados en conclusiones interpretables, y no únicamente en generar visualizaciones.

---

## 🗂️ Fuente y alcance del dataset

**Fuente:** [Kaggle — Global AI Tool Adoption Across Industries](https://www.kaggle.com/datasets/tfisthis/global-ai-tool-adoption-across-industries)

El dataset utilizado contiene **145.000 registros y 9 variables**:

- País
- Industria
- Herramienta de IA
- Tasa de adopción
- Usuarios activos diarios
- Año
- Feedback de usuario
- Grupo etario
- Tamaño de empresa

El período observado comprende los años **2023 y 2024**.

Cada fila se interpreta como una observación de adopción y uso de una herramienta de IA. La base no incluye un identificador único de empresa, por lo que **no permite contar compañías únicas ni realizar un seguimiento de la misma organización entre ambos años**.

---

## 🎯 Pregunta principal

> **¿Qué factores —tipo de herramienta, industria y tamaño de empresa— están asociados con el éxito en la adopción y uso diario de IA?**

---

## 💡 Objetivo del análisis

Identificar patrones de adopción y utilización de herramientas de IA y determinar si el **tamaño de empresa, la industria, el tipo de herramienta y el año** presentan diferencias relevantes en las métricas analizadas.

El análisis busca responder:

- ¿Existen diferencias de adopción según el tamaño de empresa?
- ¿Qué categorías de IA presentan mayores niveles de adopción según la industria?
- ¿Cómo evolucionaron la adopción y los usuarios activos diarios entre 2023 y 2024?
- ¿Qué herramientas presentan mayores niveles de uso diario?
- ¿La presencia de una herramienta en la muestra se relaciona con un mayor engagement?

---

# 🔎 Preguntas de análisis

## 1. Adopción según tamaño de empresa

**¿Existen diferencias significativas en la tasa de adopción entre Startups, PyMEs (SME) y grandes corporaciones (Enterprise)?**

Se comparan los niveles de adopción entre los distintos tamaños de empresa mediante medidas de tendencia central y distribución.

### Métricas principales

- Promedio de `adoption_rate`
- Mediana de `adoption_rate`
- Cantidad de registros por segmento
- Distribución de la tasa de adopción

### Visualización

Gráfico de barras para comparar la adopción promedio entre segmentos.

### Decisión de negocio

Evaluar si el tamaño de empresa constituye un criterio útil para diferenciar estrategias de adopción de IA.

---

## 2. Uso de IA generativa según industria

**¿Qué industrias presentan diferencias entre la adopción de IA generativa de texto y de imagen?**

Las herramientas se clasifican en dos categorías:

- **Generación de Texto:** ChatGPT, Claude y Bard.
- **Generación de Imagen:** Midjourney y Stable Diffusion.

### Variables principales

- `industry`
- `ai_tool`
- `tool_category`
- `adoption_rate`

### Transformaciones

- Clasificación de herramientas mediante un mapeo.
- Agrupación por industria y categoría de IA.
- Creación de tablas de comparación.
- Cálculo de la diferencia entre adopción de texto e imagen.

### Métrica principal

- Tasa de adopción promedio por industria y categoría.

### Visualización

Gráfico de barras comparativo.

### Decisión de negocio

Determinar si la industria permite identificar una preferencia clara por una categoría de IA.

---

## 3. Evolución de la adopción

**¿Cómo evolucionaron la tasa de adopción promedio y los usuarios activos diarios entre 2023 y 2024?**

Se comparan los principales indicadores entre ambos años para determinar si existe una tendencia de crecimiento, estabilidad o disminución.

### Variables principales

- `year`
- `adoption_rate`
- `daily_active_users`

### Métricas

- Tasa de adopción promedio.
- Variación interanual de adopción.
- DAU promedio.
- Variación interanual de DAU.

### Visualización

Gráficos de líneas para comparar la evolución de ambos indicadores.

### Decisión de negocio

Determinar si los datos muestran una aceleración de la adopción o, por el contrario, un comportamiento estable durante el período analizado.

---

## 4. Engagement por herramienta

**¿Qué herramientas presentan mayores niveles de utilización medidos a través de usuarios activos diarios (DAU)?**

La tasa de adopción y el uso diario representan dimensiones diferentes. Por este motivo, se analiza el DAU promedio para comparar el nivel de utilización de cada herramienta.

### Variables principales

- `ai_tool`
- `daily_active_users`
- `adoption_rate`

### Métricas

- DAU promedio por herramienta.
- Tasa de adopción promedio.
- Cantidad de registros por herramienta.

### Visualización

Ranking mediante barras horizontales ordenadas.

### Decisión de negocio

Evaluar las herramientas considerando su utilización efectiva y no únicamente su presencia o cantidad de registros en la muestra.

---

# 🧠 Hipótesis iniciales

Antes del análisis se plantearon las siguientes hipótesis:

### Hipótesis 1 — Tamaño de empresa

> **Las Startups presentan una tasa de adopción general mayor que las Enterprises**, debido a una mayor agilidad organizacional para incorporar nuevas tecnologías.

### Hipótesis 2 — Tipo de herramienta e industria

> **Las herramientas de IA generativa de texto presentan una adopción transversal entre industrias**, mientras que las herramientas de generación de imágenes podrían presentar mayores niveles de adopción en determinados sectores.

### Hipótesis 3 — Evolución temporal

> **La adopción de IA aumentó significativamente entre 2023 y 2024**, reflejando una aceleración general en la incorporación de estas tecnologías.

Las hipótesis fueron planteadas como **supuestos iniciales** y posteriormente contrastadas con los datos.

---

# 📐 Metodología

El análisis sigue un proceso estructurado:

### 1. Exploración de los datos

- Identificación de variables.
- Análisis de tipos de datos.
- Detección de valores nulos.
- Identificación de duplicados.
- Análisis estadístico de variables numéricas.
- Revisión de valores únicos en variables categóricas.

### 2. Limpieza y preparación

La revisión inicial confirmó:

- **145.000 registros.**
- **9 variables.**
- **Sin valores faltantes.**
- **Sin filas exactamente duplicadas.**

Se validaron las variables numéricas y se creó `tool_category` para clasificar las herramientas entre generación de texto e imagen.

Además, `company_size` y `tool_category` se transformaron en variables categóricas ordenadas para mantener una presentación consistente en tablas y gráficos.

### 3. Análisis exploratorio

Se realizaron análisis sobre:

- Tamaño de empresa.
- Industria.
- Tipo de herramienta.
- Categoría de IA.
- Evolución temporal.
- Usuarios activos diarios.

### 4. Interpretación

Los resultados se interpretan desde una perspectiva de negocio, buscando responder:

> **¿Qué significa este resultado y qué decisión podría apoyar?**

El objetivo es diferenciar los resultados descriptivos de las conclusiones que realmente pueden sostenerse con la evidencia disponible.

---

# 📌 KPIs principales

| KPI | Resultado / descripción |
|---|---|
| **Tasa de adopción promedio global** | 49,92% aproximadamente |
| **Adopción promedio 2023** | 50,02% |
| **Adopción promedio 2024** | 49,81% |
| **Variación interanual de adopción** | -0,21 puntos porcentuales |
| **DAU promedio 2023** | 5.034 |
| **DAU promedio 2024** | 5.041 |
| **Variación interanual del DAU** | +0,13% |
| **Herramienta con mayor DAU promedio** | Claude — 5.063,64 |
| **Herramienta con mayor cantidad de registros** | ChatGPT — 58.045 registros |

> Los KPIs se calculan sobre los registros disponibles en el dataset y no representan necesariamente empresas únicas.

---

# 📈 Resultados y hallazgos

## 1. El tamaño de empresa no muestra una brecha práctica de adopción

**Resultado:** las Startups registran una adopción promedio de **50,04%**, frente a **49,84% en Enterprise** y **49,74% en SME**.

La diferencia máxima entre segmentos es de apenas **0,30 puntos porcentuales**.

**Interpretación:** los tres segmentos presentan niveles de adopción muy similares, concentrados alrededor del 50%.

**Conclusión:** el tamaño de empresa, por sí solo, **no permite identificar una ventaja relevante de adopción ni justificar una priorización comercial basada únicamente en este factor**.

---

## 2. Texto e imagen presentan niveles de adopción muy similares entre industrias

**Resultado:** la mayor diferencia observada entre las categorías de generación de texto e imagen es de aproximadamente **0,58 puntos porcentuales**.

Por ejemplo:

- **Transporte:** 50,10% para texto frente a 49,52% para imagen.
- **Educación:** 49,56% para texto frente a 50,06% para imagen.

**Interpretación:** la categoría con mayor adopción cambia según la industria y las diferencias son pequeñas.

**Conclusión:** no existe evidencia suficiente para recomendar una categoría de IA sobre otra únicamente por su tasa de adopción promedio. La elección debería considerar principalmente el **caso de uso y las necesidades específicas de cada sector**.

---

## 3. La adopción y el uso diario se mantuvieron estables entre 2023 y 2024

**Resultado:** la adopción promedio pasó de **50,02% en 2023 a 49,81% en 2024**, una disminución de **0,21 puntos porcentuales**.

Durante el mismo período, el DAU promedio pasó de **5.034 a 5.041 usuarios**, equivalente a una variación aproximada de **+0,13%**.

**Interpretación:** ambos indicadores presentan variaciones marginales.

**Conclusión:** con los datos disponibles **no se puede sostener una aceleración general de la adopción de IA entre 2023 y 2024**. El uso diario también permanece esencialmente estable.

---

## 4. La cantidad de registros no implica mayor engagement

**Resultado:** ChatGPT concentra **58.045 registros**, equivalentes al **40,03% de la muestra**, pero Claude presenta el mayor DAU promedio con **5.063,64 usuarios** frente a **5.030,00 de ChatGPT**.

**Interpretación:** la cantidad de registros y el uso diario promedio representan dimensiones diferentes.

Además, la diferencia de DAU entre ambas herramientas es reducida.

**Conclusión:** no sería adecuado seleccionar o estandarizar una herramienta únicamente por su presencia en la muestra o por su posición en el ranking de DAU. Para una decisión real deberían incorporarse otros factores como **costos, casos de uso y satisfacción de los usuarios**.

---

# 💼 Conclusiones y recomendaciones

El análisis muestra que las variables estudiadas presentan **diferencias muy pequeñas en términos de adopción**.

### Principales conclusiones

- La adopción promedio se mantiene alrededor del **50%** en la muestra.
- No se observa una diferencia práctica relevante entre Startups, SME y Enterprise.
- Las categorías de generación de texto e imagen presentan niveles de adopción muy similares entre industrias.
- Entre 2023 y 2024, tanto la adopción como el DAU permanecen esencialmente estables.
- La herramienta con mayor presencia en la muestra no necesariamente presenta el mayor DAU promedio.
- La elección de una herramienta no debería basarse en una única métrica.

### Recomendaciones

A partir de estos resultados, se recomienda:

1. **No segmentar una estrategia de adopción únicamente por tamaño de empresa**, debido a las diferencias mínimas observadas.
2. **Seleccionar herramientas según el caso de uso y las necesidades de la industria**, ya que las diferencias entre categorías de IA son reducidas.
3. **Complementar el análisis de DAU con costos, satisfacción y utilidad de la herramienta** antes de tomar decisiones de estandarización.
4. Para futuros análisis, incorporar variables adicionales que permitan explicar mejor las diferencias de adopción.

> Estas recomendaciones tienen carácter **informativo y exploratorio**. Los resultados describen asociaciones presentes en esta muestra y no permiten establecer relaciones causales ni generalizar automáticamente los resultados a todas las empresas.

---

# ⚠️ Supuestos y limitaciones

- Cada fila se trata como una observación independiente de adopción y uso.
- La base no incluye un ID de empresa, por lo que no permite identificar compañías únicas ni construir un seguimiento longitudinal individual.
- La comparación entre 2023 y 2024 muestra asociaciones agregadas y no demuestra causalidad.
- Solo se observan dos años, por lo que no es posible establecer una tendencia temporal de largo plazo.
- La cantidad de registros puede diferir entre períodos y categorías, por lo que las variaciones deben interpretarse con cautela.
- Se asume que `adoption_rate` y `daily_active_users` fueron medidos de manera consistente en todos los registros.
- El dataset no proporciona información sobre el denominador utilizado para calcular `adoption_rate` ni sobre la metodología de muestreo.
- `user_feedback` no se analiza en esta etapa.
- El análisis no incorpora costos, satisfacción, productividad u otras variables necesarias para evaluar una decisión de inversión real.
- Los resultados deben considerarse **descriptivos y exploratorios**, no como recomendaciones gerenciales definitivas.

### Posibles extensiones

Como trabajo futuro sería útil incorporar:

- Análisis de sentimiento sobre `user_feedback`.
- Identificador de empresa.
- Datos con mayor granularidad temporal.
- Tamaño de plantilla.
- Costos de las herramientas.
- Métricas de productividad.
- Indicadores de satisfacción y retención.

---

# 📂 Estructura del repositorio

```text
Final-proyect/
│
├── README.md
├── proyecto_final.ipynb
├── requirements.txt
│
├── dataset/
│   ├── raw/
│   │   └── ai_adoption_dataset.csv
│   │
│   └── clean/
│       └── ai_adoption_dataset.csv
│
└── presentacion/
    └── presentacion_final.pdf
```

### Archivos principales

**`proyecto_final.ipynb`**

Notebook principal que contiene:

- Exploración de datos.
- Limpieza y preparación.
- Transformación de variables.
- Análisis exploratorio.
- Cálculo de KPIs.
- Visualizaciones.
- Interpretación de resultados.
- Conclusiones.
- Limitaciones.

**`dataset/`**

Contiene las versiones del dataset utilizadas durante el proyecto:

- `raw/`: archivo original.
- `clean/`: archivo preparado para el análisis.

**`requirements.txt`**

Contiene las dependencias necesarias para ejecutar el proyecto.

**`presentacion/`**

Contiene la presentación final utilizada para comunicar los principales resultados del análisis.

---

# ▶️ Cómo ejecutar el proyecto

## Requisitos

- Python 3.x
- Jupyter Notebook o JupyterLab
- pip

## Instalación

Clonar el repositorio:

```bash
git clone https://github.com/Amarilla-Agustin/Final-proyect.git
cd Final-proyect
```

Instalar las dependencias:

```bash
pip install -r requirements.txt
```

Iniciar Jupyter Notebook:

```bash
jupyter notebook
```

Abrir:

```text
proyecto_final.ipynb
```

y ejecutar las celdas en orden.

> **Nota:** el notebook utiliza rutas relativas hacia los archivos ubicados dentro de `dataset/raw/` y `dataset/clean/`. Por lo tanto, se recomienda ejecutar Jupyter desde la carpeta raíz del repositorio.

---

# 🎤 Presentación

Los resultados del análisis se presentan en una exposición de **5 a 10 minutos**, orientada a una audiencia de negocio.

La presentación sigue la siguiente estructura:

1. **Resumen ejecutivo**
   - Principales hallazgos.
   - Conclusiones.

2. **Problema**
   - Pregunta de negocio.
   - Objetivo del análisis.

3. **Dataset**
   - Fuente.
   - Alcance.
   - Variables relevantes.

4. **Metodología**
   - Limpieza.
   - Transformación.
   - Análisis exploratorio.

5. **KPIs**
   - Principales métricas.

6. **Hallazgos**
   - Resultados más relevantes.
   - Evidencia visual.

7. **Conclusiones**
   - Insights.
   - Recomendaciones.
   - Limitaciones.

> **La presentación prioriza la comunicación de resultados sobre los aspectos técnicos y no incluye código.**

---

# 🛠️ Tecnologías utilizadas

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**
- **Git**
- **GitHub**

---

# 👤 Autores

**Agustín Amarilla**  
**Guillermo Kafka**

Proyecto Final — **Análisis de Datos | Comunidad IT**
