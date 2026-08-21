# Análisis de Conversión y Experimento A/B

## Resumen ejecutivo
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?logo=postgresql&logoColor=white)
![PowerBI](https://img.shields.io/badge/PowerBI-F2C811?logo=powerbi&logoColor=black)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)

Este proyecto evalúa el rendimiento de dos versiones de una landing page, **A** y **B**, mediante un experimento A/B. El análisis busca determinar cuál variante genera una **mayor tasa de conversión** y un **mayor gasto promedio por usuario convertido**, con el fin de sustentar una decisión de negocio basada en evidencia.

**Hallazgo principal:** la **landing page B** muestra un mejor desempeño general que la versión A, tanto en conversión como en valor generado por usuario convertido.

## Objetivo de negocio
Responder, con evidencia estadística, a las siguientes preguntas:
- ¿La página **B** convierte mejor que la página **A**?
- ¿Los usuarios que convierten en la página **B** gastan más en promedio?
- ¿Variables como la **fuente de tráfico** o el **tipo de usuario** se relacionan con la conversión?

## Dataset
El archivo `landing_experiment.csv` contiene información de **40,000 usuarios** expuestos a una de las dos variantes de la landing page entre el **1 de enero de 2026** y el **28 de enero de 2026**.

### Variables principales
- `user_id`: identificador único del usuario
- `date`: fecha de exposición al experimento
- `landing`: versión mostrada (`A` o `B`)
- `region`: región geográfica del usuario
- `dispositivo`: dispositivo utilizado
- `traffic_source`: canal de adquisición
- `user_type`: tipo de usuario
- `converted`: indicador de conversión (`0` = no convirtió, `1` = convirtió)
- `gasto`: monto gastado por el usuario

## Metodología
El análisis se desarrolló en las siguientes etapas:
1. **Carga y validación de datos**
2. **Análisis exploratorio (EDA)**
3. **Comparación del gasto promedio** entre usuarios convertidos de A y B
4. **Comparación de la tasa de conversión** entre ambas variantes
5. **Evaluación de asociación** entre variables categóricas y conversión
6. **Interpretación de resultados** y recomendaciones de negocio

### Pruebas estadísticas utilizadas
- **t-test de muestras independientes** para comparar el gasto promedio entre grupos
- **z-test de proporciones** para comparar la tasa de conversión entre A y B
- **chi-cuadrado de independencia** para evaluar la relación entre variables categóricas y conversión

## Resultados clave
- La variante **B** presenta una **tasa de conversión mayor** que la variante **A**.
- La variante **B** también registra un **gasto promedio superior** entre los usuarios que convierten.
- Las diferencias observadas entre ambas páginas son **estadísticamente significativas**.
- El principal hallazgo del experimento es que la variante **B** es la mejor opción para escalar la estrategia de conversión.

## Conclusión de negocio
A partir de los resultados obtenidos, se recomienda **implementar la landing page B** como versión ganadora del experimento. Esta variante no solo incrementa la probabilidad de conversión, sino que también mejora el valor económico generado por los usuarios que completan la acción esperada.

## Estructura actual del repositorio
```text
.
├── README.md
├── S9 Version_Student_Proyecto_Landing_Experiment.ipynb
├── landing_experiment.csv
├── requirements.txt
└── .gitignore
```

## Cómo ejecutar el proyecto
1. Clona este repositorio.
2. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```
3. Abre **Jupyter Notebook** o **JupyterLab**.
4. Ejecuta el notebook `S9 Version_Student_Proyecto_Landing_Experiment.ipynb`.

> **Recomendación:** para mejorar la portabilidad del proyecto, conviene actualizar dentro del notebook la ruta de carga del CSV para usar una ruta relativa del repositorio.

## Tecnologías utilizadas
- Python
- Pandas
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- Jupyter Notebook

## Oportunidades de mejora
- Reorganizar los archivos en carpetas como `data/`, `notebooks/` e `images/`
- Exportar visualizaciones clave e incluirlas en el README
- Renombrar el notebook con un nombre más claro y profesional
- Convertir el notebook en una versión más orientada a portafolio
- Añadir conclusiones ejecutivas más sintéticas en cada sección del análisis

## Valor del proyecto
Este proyecto demuestra habilidades en:
- análisis exploratorio de datos
- diseño e interpretación de experimentos A/B
- pruebas de hipótesis
- análisis orientado a negocio
- comunicación de hallazgos con enfoque analítico
