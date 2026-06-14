# Análisis de Conversión y Experimento A/B

## Descripción del proyecto
Este proyecto analiza el desempeño de dos landing pages (A y B) mediante un experimento A/B para evaluar su impacto en la tasa de conversión y el gasto promedio por usuario. El objetivo es identificar qué versión genera mejores resultados y traducir los hallazgos en recomendaciones accionables para negocio.

## Objetivo de negocio
Determinar si la landing page B supera a la landing page A en:
- **Tasa de conversión**
- **Gasto promedio** de los usuarios que convierten

Además, se explora si variables como la **fuente de tráfico** y el **tipo de usuario** presentan asociación con la conversión.

## Dataset
El archivo `landing_experiment.csv` contiene información de 40,000 usuarios expuestos a una de dos versiones de la landing page durante el periodo comprendido entre el **1 de enero de 2026** y el **28 de enero de 2026**.

Variables principales:
- `user_id`: identificador único del usuario
- `date`: fecha de exposición
- `landing`: versión mostrada (A o B)
- `region`: región geográfica
- `dispositivo`: tipo de dispositivo
- `traffic_source`: canal de adquisición
- `user_type`: tipo de usuario
- `converted`: indicador de conversión (0/1)
- `gasto`: monto gastado por el usuario

## Metodología
El análisis sigue estas etapas:
1. Carga y validación de datos
2. Análisis exploratorio
3. Comparación del gasto promedio entre A y B
4. Comparación de la tasa de conversión entre A y B
5. Evaluación de asociación entre variables categóricas y conversión
6. Interpretación de resultados y recomendaciones

Pruebas estadísticas utilizadas:
- **t-test de muestras independientes** para comparar gasto promedio entre grupos
- **z-test de proporciones** para comparar tasa de conversión
- **chi-cuadrado de independencia** para evaluar relación entre variables categóricas y conversión

## Resultados clave
- La **landing page B** presenta una **mayor tasa de conversión** que la versión A.
- La **landing page B** también muestra un **mayor gasto promedio** entre los usuarios que convierten.
- La diferencia observada en conversión entre ambas páginas es **estadísticamente significativa**.
- Variables como `traffic_source` y `user_type` pueden explorarse como factores complementarios, pero el principal hallazgo del experimento es la superioridad de la variante B.

## Conclusión de negocio
Los resultados respaldan la implementación de la **landing page B** como versión ganadora del experimento, ya que mejora la conversión y genera mayor valor por usuario convertido.

## Estructura del repositorio
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
3. Abre Jupyter Notebook o JupyterLab.
4. Ejecuta el notebook `S9 Version_Student_Proyecto_Landing_Experiment.ipynb`.

> Nota: si deseas mejorar la portabilidad del proyecto, se recomienda actualizar la ruta de carga del CSV dentro del notebook para que lea el archivo desde una ruta relativa del repositorio.

## Tecnologías utilizadas
- Python
- Pandas
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- Jupyter Notebook

## Próximos pasos sugeridos
- Reorganizar archivos en carpetas como `data/`, `notebooks/` e `images/`
- Exportar visualizaciones clave para incluirlas en el README
- Convertir el notebook en una versión más orientada a portafolio profesional
- Añadir conclusiones más sintéticas y ejecutivas por sección
