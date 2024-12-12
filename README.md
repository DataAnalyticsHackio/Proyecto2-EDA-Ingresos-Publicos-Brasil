<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_naranja@4x.png?raw=true" alt="esquema" />
</div>


# Proyecto: **Análisis de la Ejecución de Ingresos Públicos en Brasil**

El gobierno de Brasil, a través de sus distintos órganos, gestiona la recaudación de ingresos públicos para financiar los servicios y proyectos que benefician a la sociedad. Cada año, se realiza una planificación detallada para prever cuánto se espera recaudar, pero a menudo la recaudación real difiere de lo previsto debido a diversos factores como la evasión fiscal, fluctuaciones económicas, ineficiencias administrativas, entre otros.

Has sido contratado por la Secretaría de Hacienda para analizar los datos históricos de la ejecución de ingresos entre 2013 y 2021. La misión es identificar patrones, detectar áreas problemáticas donde la recaudación ha sido consistentemente menor a lo previsto, y proponer recomendaciones basadas en los datos que ayuden a mejorar la precisión de las previsiones y la eficiencia de la recaudación.

Los problemas concretos que te han pedido resolver son:

1.	**Desviaciones entre lo previsto y lo recaudado**: Determinar en qué categorías económicas o tipos de ingresos las diferencias son más pronunciadas.

2.	**Evolución temporal de la recaudación**: Identificar cómo han cambiado las previsiones y recaudaciones año a año, y si existen patrones temporales, como meses específicos donde hay mayores discrepancias.

3.	**Rendimiento por órgano y unidad gestora**: Evaluar qué órganos o unidades gestoras son más eficientes en términos de alcanzar las metas de recaudación y cuáles presentan consistentemente una baja ejecución.


# Objetivos del Proyecto

- **Limpieza de datos:** Resolver problemas comunes como valores nulos, formatos inconsistentes y duplicados.

- **Unión de conjuntos de datos:** Combinar todos los archivos en un solo dataframe para análisis global. Si es necesario, deberéis crear una columna extra para no perder información. 

- **Análisis Exploratorio de Datos (EDA):** Examinar la relación entre diferentes variables clave y explorar categorías relevantes para identificar patrones o discrepancias significativas.

- **Visualización:** Generar gráficos que permitan identificar tendencias y patrones relevantes en los datos analizados.

# Instrucciones Detalladas

## Fase 1: Unión de Conjuntos de Datos

1. **Lectura y Exploración Inicial:**

   - Cargar los diferentes archivos CSV en dataframes individuales.

   - Explorar la estructura de cada archivo para asegurarse de que las columnas sean consistentes y tengan un formato homogéneo.

2. **Estandarización y Limpieza:**

   - Estandarizar nombres de columnas si es necesario.

   - Asegurar que los tipos de datos (fechas, valores monetarios) sean consistentes en todos los archivos.

   - Tratar los valores nulos y eliminar filas o columnas irrelevantes.

3. **Unión de los Dataframes:**

   - Unir los dataframes de todos los archivos para crear un solo dataframe consolidado.

   - Verificar la existencia de duplicados y corregir cualquier inconsistencia en los datos.

## Fase 2: Limpieza de Datos

1. **Tratamiento de Valores Nulos:**

   - Identificar y manejar los valores nulos: decidir si se deben rellenar, eliminar o imputar según el contexto.

2. **Corrección de Formatos:**

   - Convertir valores monetarios a formato numérico, eliminando símbolos y asegurando que todas las cifras sean comparables.

   - Asegurarse de que las fechas estén en un formato uniforme y puedan ser fácilmente manipuladas para análisis temporal.

3. **Detección y Corrección de Errores en Categorizaciones:**

   - Revisar posibles inconsistencias en las categorías económicas (errores tipográficos, variaciones en los nombres) y unificarlas.

## Fase 3: Análisis Exploratorio de Datos (EDA)

1. **Distribución de Ingresos por Categoría Económica:**

   - Analizar las categorías de ingresos más significativas y su participación en los ingresos totales.

   - Calcular la diferencia promedio entre ingresos previstos y realizados por cada categoría.

2. **Análisis Temporal:**

   - Evaluar las tendencias a lo largo del tiempo, por ejemplo, cómo cambian los ingresos realizados de un mes a otro o de un año a otro.

3. **Identificación de Discrepancias:**

   - Investigar las categorías con mayor diferencia entre lo previsto y lo realizado, identificando patrones en la subejecución o sobre ejecución.

## Fase 4: Visualización de Datos

1. **Gráficos de Barras y Líneas:**

   - Crear gráficos que muestren la comparación entre ingresos previstos, lanzados y realizados para cada categoría.

   - Graficar la evolución temporal de los ingresos realizados y previstos.

2. **Diagramas de Caja:**

   - Evaluar la dispersión de las diferencias entre los valores previstos y realizados en diferentes categorías.

## Fase 5: Conclusiones y Recomendaciones

1. **Resumen de Hallazgos:**

   - Identificar las categorías y períodos con mayor discrepancia entre lo previsto y lo realizado.

   - Describir tendencias observadas en la ejecución de ingresos.

2. **Propuestas de Mejora:**
   - Sugerir acciones para mejorar la precisión en la planificación y ejecución de los ingresos.

# Los Datos

Los conjuntos de datos que usaremos corresponden a la ejecución de ingresos públicos en Brasil durante los años 2013 al 2021. La **ejecución de ingresos públicos** se refiere al proceso mediante el cual un gobierno recauda y gestiona sus ingresos fiscales y no fiscales para financiar sus actividades y programas. En el contexto de Brasil, y en los datos que mencionas, la ejecución de ingresos públicos implica cómo se administraron los recursos que el gobierno planeaba recibir (ingresos previstos) y lo que efectivamente recaudó (ingresos realizados) durante un periodo específico, en este caso, desde 2013 hasta 2021. En Brasil, los ingresos públicos pueden venir de:

- **Impuestos:** Como el Imposto de Renda (IR) y el Imposto sobre Produtos Industrializados (IPI).

- **Contribuciones Sociales:** Como las contribuciones para la seguridad social (INSS).

- **Tasas y Tarifas:** Que pueden ser cobradas por servicios específicos.

- **Otros Ingresos:** Como multas, indemnizaciones, y la venta de activos.


Las columnas presentes en estos archivos son:

- `código órgão superior`: Código numérico que identifica la entidad gubernamental superior.

- `nome órgão superior`: Nombre de la entidad gubernamental superior.

- `código órgão`: Código numérico que identifica la entidad gubernamental específica.

- `nome órgão`: Nombre de la entidad gubernamental específica.

- `código unidade gestora`: Código numérico de la unidad gestora responsable.

- `nome unidade gestora`: Nombre de la unidad gestora.

- `categoria econômica`: Clasificación económica de los ingresos (por ejemplo, "Receitas Correntes").

- `origem receita`: Fuente específica del ingreso (por ejemplo, "Outras Receitas Correntes").

- `espécie receita`: Tipo de ingreso dentro de la fuente (por ejemplo, "Demais receitas correntes").

- `detalhamento`: Detalle adicional del tipo de ingreso (por ejemplo, "Receita de honorários de advogados").

- `valor previsto atualizado`: Monto actualizado del ingreso previsto (formato texto).

- `valor lançado`: Monto que fue registrado como lanzado (formato texto).

- `valor realizado`: Monto realmente recaudado (formato texto).

- `percentual realizado`: Porcentaje de ejecución respecto al valor previsto.

- `data lançamento`: Fecha en la que se registró la ejecución del ingreso.

- `ano exercício`: Año correspondiente a la ejecución de los ingresos.

# Entrega del Proyecto

La entrega del proyecto se realizará a través de una **issue en GitHub**, trabajando en un repositorio propio en tu cuenta personal. Los pasos que deberás seguir para hacer la entrega del proyecto son:


- **Crear un nuevo repositorio en tu cuenta de GitHub:**

   - Crea un nuevo repositorio llamado `Proyecto2-Insights Brasil`. Este nombre es obligatorio, no podremos llamarlo de otra forma. 

   - Configuralo como público. 


- **Desarrolla el proyecto:**

   - Implementa el código de los juegos según las especificaciones y guías proporcionadas.

   - Recuerda hacer commits regulares mientras avanzas en el desarrollo:

     ```bash
     git add .
     git commit -m "Descripción del avance"
     git push
     ```


- **Crear una issue en el repositorio original del curso:**

   - Ve al repositorio original del curso y dirígete a la pestaña de **Issues**.

- **Abrir una nueva issue para tu entrega:**

   - Haz clic en **New Issue** y llena los siguientes campos:

     - **Título:** Usa el formato "Entrega Proyecto: ProyectoMineríaDatos - [Tu Nombre]".

     - **Descripción:** En la descripción, incluye:

       - Una breve explicación de tu proyecto.

       - Instrucciones para ejecutar tu código (si aplica).

       - Un enlace a tu repositorio personal donde está alojado el proyecto.


# 🚀 Entrega del Proyecto 🚀

**Fecha y hora límite:**

🗓️ **Martes a las 18:00.**


**Nota importante:**

⚠️ **Todos los proyectos que sean entregados o modificados después de la hora límite (lunes a las 9:00 AM) se considerarán como no entregados.** Por favor, asegúrate de completar y enviar tu trabajo a tiempo para evitar problemas.


# 🎤 Presentación de Proyectos 🎤

El martes a primera hora tendremos las **presentaciones de los proyectos**. La dinámica será la siguiente:

- De forma **aleatoria**, seleccionaremos entre **3 y 5 alumnos** para presentar su proyecto.

- Cada alumno tendrá **5 minutos** para explicar su proyecto y hacer una demo en vivo. Durante este tiempo podrán mostrar cómo funciona su juego y resaltar las características principales.

**Detalles importantes:**
- Es importante que lleguéis puntuales, ya que comenzaremos las presentaciones de inmediato.

- Asegúrate de que tu código esté listo y funcional para la demo.

- Todos debemos estar preparados para presentar, ya que la selección será completamente aleatoria.
