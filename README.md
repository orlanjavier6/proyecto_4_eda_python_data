# Proyecto 4: DataProject: Proyecto EDA con Python

Este proyecto forma parte del módulo de **Python for Data** del Máster en Data & Analytics. 
Consiste en el diseño, desarrollo y documentación de un flujo completo de **Ingeniería de Datos y Análisis Exploratorio de Datos (EDA)**. El objetivo principal es la unificación y saneamiento de fuentes de datos independientes de una entidad financiera para identificar el perfil de cliente óptimo de cara a la contratación de depósitos bancarios a plazo fijo.

El proyecto abarca desde la manipulación avanzada de estructuras de datos y la unificación relacional mediante claves primarias, hasta la imputación estadística de valores nulos y el diseño de visualizaciones analíticas complejas mediante librerías de distribución estadística.

---

## Estructura del Proyecto
El repositorio está organizado para facilitar la inspección del código y la ejecución del entorno:

mi_proyecto_eda/

├── DataProject_ Proyecto EDA con Python.docx      #Documento original con las directrices y enunciados

├── README.md                                      #Descripción general del proyecto y documentación

├── analisis_exploratorio.ipynb                    #Jupyter Notebook principal con el pipeline de código ejecutado y limpio

├── bank-additional.csv                            #Dataset original con los resultados de los contactos

└── customer-details.xlsx                          #Dataset original con la información socioeconómica de los clientes


---

## Herramientas y Tecnologías Utilizadas
- **Python 3.x** → Lenguaje de programación principal para el procesamiento de datos.
- **Jupyter Notebook / VS Code** → Entorno interactivo utilizado para el desarrollo, pruebas y documentación en vivo de las celdas de código.
- **Librerías del Ecosistema de Datos:**
    - `pandas` para la carga distribuidora de ficheros CSV, indexación, unificación relacional (`merge`) y manipulación de DataFrames.
    - `numpy` para el soporte de operaciones matriciales y gestión de estructuras de datos nulos.
    - `matplotlib.pyplot` para la inicialización de lienzos dinámicos, gestión de dimensiones de figuras y optimización de espacios de gráficos.
    - `seaborn` para la construcción de gráficos estadísticos de alta densidad informativa y aplicación de paletas categóricas (`Set2`, `Pastel1`).

---

## Proceso Metodológico de Desarrollo y Apoyo
1. **Unificación Relacional de Fuentes (Data Merge):** Consolidación de un ecosistema de datos fragmentado mediante el uso de la función `pd.merge()`, vinculando la información demográfica con el histórico de campañas a través de la clave común `id_cliente`.
2. **Ingeniería de Limpieza Defensiva (Data Imputation):** Diagnóstico proactivo de valores faltantes (`NaN`) en el dataset unificado. Implementación de una estrategia de imputación selectiva: uso de la **mediana** para salvaguardar variables numéricas frente a valores extremos y la **moda** estadística para rellenar campos categóricos sin distorsionar las frecuencias naturales.
3. **Análisis de Frecuencias y Métricas de Conversión:** Evaluación matemática del balanceo de la variable objetivo (`y`) mediante el cálculo automatizado de proporciones normalizadas sobre el total de la población del dataset.
4. **Modelado y Visualización Gráfica:** Diseño de gráficos de conteo categórico y diagramas de distribución segmentada para transformar datos tabulares en conclusiones visuales directas de negocio.

***

**Nota sobre el proyecto:** Dado que este es un proceso de aprendizaje orientado a consolidar la ingeniería de datos y el análisis exploratorio con Python, se utilizó apoyo de una IA para depurar conflictos de entorno de ejecución en las librerías de gráficos, optimizar la sintaxis de los bucles iterativos de imputación y estructurar de forma clara el flujo lógico del cuaderno interactivo. Esto garantizó la entrega de código limpio, idiomático (*Pythonic*) y eficiente.

***

## Resultados y Conclusiones

- **Volumen de Datos Procesado:** Unificación exitosa de una muestra masiva de **43,000 registros** sin pérdida de filas durante el tratamiento de limpieza.
- **Análisis de Conversión Comercial:** Diagnóstico exacto del rendimiento de la campaña telefónica, revelando un comportamiento desbalanceado con un **88.73% de rechazos (`no`)** frente a un **11.26% de contrataciones exitosas (`yes`)**.
- **Perfil Demográfico Central:** Identificación de las variables métricas del cliente promedio: edad media de **39.7 años**, ingresos anuales medios de **93,241 €** y una frecuencia de interacción digital de **16.5 visitas mensuales**.
- **Casos de Uso e Insights de Negocio Extraídos:**
    - **Análisis de Perfil por Profesión:** El gráfico de barras (`countplot`) demostró que los empleados administrativos (`admin.`) representan el nicho de mercado con mayor volumen de contratación.
    - **Rompiendo Mitos Económicos:** El diagrama de cajas (`boxplot`) reveló que el nivel económico **no es un factor determinante** ni discriminatorio para predecir si un cliente contratará el producto, ya que la mediana de ingresos es simétrica en ambos grupos.

---

## Habilidades Demostradas

- **Ingeniería de Datos Práctica:** Capacidad para enlazar archivos relacionales independientes garantizando la integridad del volumen de registros.
- **Estadística Descriptiva Aplicada:** Uso eficiente de métodos analíticos para sintetizar poblaciones de datos complejas en métricas de negocio.
- **Robustez de Entorno:** Resolución de conflictos de dependencias del Kernel mediante el despliegue directo del operador de instalación `%pip`.

---

## Acceso al Código
**Consulta el cuaderno completo con todas las celdas de limpieza y gráficos ejecutadas:**
[Abrir analisis_exploratorio.ipynb](./analisis_exploratorio.ipynb)

---

## Próximos Pasos
- Desarrollar un modelo predictivo de Clasificación (ej. Regresión Logística) utilizando `Scikit-Learn` para automatizar la asignación de propensión de compra a nuevos clientes.
- Implementar técnicas de sobremuestreo (como SMOTE) para compensar el desbalanceo del 11% frente al 88% en la variable objetivo.

---

## Autor
**[Orlan Javier Parra Parra]**

[@orlanjavier6](https://github.com/orlanjavier6)
