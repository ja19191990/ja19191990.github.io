# Acerca de mí

Químico Farmacéutico Biólogo, con maestría en Síntesis Total certificado en Ciencia de Datos con sólida experiencia en limipieza de datos, ingeniería de características, construcción de modelos de aprendizaje automático y su optimización.

Doy certeza en la toma de decisiones estratégicas y ahorro tiempo mediante la automatización usando modelos de aprendizaje automático y pruebas de hipótesis que realizan predicciones confiables.

## Hard Skills


- Generación de modelos predictivos usando __Scikit-learn, PyTorch, TensorFlow__
- Optimización de modelos de __Machine Learning__ con __CatBoost, Optuna, LigthGBM__ y __GridSearchCV__
- Visualización de datos con herramientas como __Seaborn, Matplotlib, PowerBI, Chemdraw__ y __MestreNova__

## Soft Skills


| Pensamiento crítico | Alta capacidad de análisis | Gestión de proyectos | Coordinación de equipos multidicplinarios | Gestión del tiempo | Optimización de procesos | Investigación aplicada | Comunicación efectiva | Adaptabilidad | Química Orgánica | 

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style-for-the-badge&logo=linkedin&logoColor=white&labelColor=101010)](https://www.linkedin.com/in/juanluisalvaretana/)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style-for-the-badge&logo=gmail&logoColor=white&labelColor=101010)](mailto:juanluisalva60@gmail.com)

# Proyectos relevantes

## Análisis de la retención de clientes en la industria de telecomunicaciones


Según un estudio de Harvard Business School, el coste de adquisición de un nuevo cliente es de 5 a 7 veces mayor que el coste de retener un cliente existente. Con la finalidad de __reducir costos__ desarrollé un modelo predictivo que permitió identificar a los clientes que cancelarian su servicio con Telecom, permitiendo desarrollar __estrategias promocionales focalizadas__ aumentando la __fidelización efectiva__.

### Herramientas utilizadas


[![Python](https://img.shields.io/badge/Python-3776AB?style-for-the-badge&logo=python&logoColor=white&labelColor=101010)]()
[![Numpy](https://img.shields.io/badge/Numpy-013243?style-for-the-badge&logo=numpy&logoColor=white&labelColor=101010)]()
[![Pandas](https://img.shields.io/badge/Pandas-150458?style-for-the-badge&logo=numpy&logoColor=white&labelColor=101010)]()
[![Scikit-learn](https://img.shields.io/badge/Scikit-learn-F7931E?style-for-the-badge&logo=scikitlearn&logoColor=white&labelColor=101010)]()
[![Seaborn]]
[![Clasificación]]()
[![Modelo Predictivo]]()
[![Aprendizaje Supervisado]]()

### Requerimiento para el éxito:


El modelo debe de ser capaz de predecir con un AUC-ROC superior a 0.65.

### Preguntas clave


1. ¿Qué factores podrían afectar la cancelación del servicio?
2. ¿Qué ventana de temporal debería de utilizarse para realizar la predicción?
3. ¿Cómo se pueden segmentar los clientes para entrenar efectivamente un modelo de aprendizaje automático?

### Metodología


__Importación de datos__: Se importaron los datos a partir de varios archivos .csv de Telecom con diferentes datos a analizar.
__Exploratory Data Analysis (EDA)__: Se identificó la variable objetivo y las características de cara a un problema de clasificación desbalanceada en una población con tres tipos de duración de contrato que pueden abarcar los servicios de telefonia y/o internet y se definé un horizonte de predicción de 6 años con base en los datos presentados por el cliente. Se consolida la información necesaria en un solo dataset, y se homogenizaron formatos, gestionando valores ausentes y corroborando la duplicación de valores explícitos.
__Preprocesamiento__: Se realizó feature engineering al crear y eliminar columnas, codificación de columnas categóricas utilizando One-Hot Encoding y Codificación de etiquetas, escalamiento, segmentación de datos y el usó de upsampling.
__Modelos__: Se entrenaron modelos de regresión logística y tipo bosque aleatorio de clasificación, probando métodologías con y sin validación cruzada, con y sin optimización bayesiana de hiperparámetros, y con y sin boosting.
__Modelo Final__: El modelo final predijo correctamente el 72% de los casos de prueba superando el requerimiento de cliente.

### Recomendaciones


__Focalizar esfuerzos__: Exiten dos tipos de clientes, sin embargo aquellos clientes que contratan servicios de telefonia e internet aportan la mayor parte del ingreso independientemente del tipo de contrato contratado.
__Facilitar la transición de contratos__: Los clientes más fieles en su mayoría comienzan con un contrato mensual, que eventualmente cambian a uno anual y finalmente a una bianual. Facilitar la transición entre un tipo de contrato y otro podría aumentar la fidelización.

### Visualizaciones


1. ¿Cómo son los clientes?


Los clientes constan de dos poblaciones que se separa en un valor de gasto cercano a 40, siendo menor a dicho valor si sólo se contrata uno de los dos servicios disponibles comportamiento apreciado al analizar los cargos totales contra la fecha de incio del contrato. Por otra parte, la distribución de los valores de End_Date, 0 y 1, se observa en ambas poblaciones y en cada relación de variables representada por lo que es poco probable que estos factores mantengan una relación determinante por si mismos para predecir la cancelació o no del servicio.

![agrupacion_por_target](/assets/img/agrupacion_por_target.png)

2. ¿Cómo influye la ventana contractual en los clientes?


Observamos que la mayoría de los clientes actualmente tiene contratos mensuales, sin embargo existe una migración a contratos de mayor duración en los clientes leales. Por otra parte, la mayor parte de los cargos totales se deben a contratos bianuales.

![agrupación_por_tipo_de_contrato](/assets/img/agrupacion_por_tipo_de_contrato.png)

3. Desbalanceo de clases


Los datos iniciales tenían un marcado desbalanceo con una aproximación 10:1.

![target_original](/assets/img/desblanceo_de_clases_original.png)

Dicho desbalanceo se trató con upsampling logrando balancear las clases. Acontinuación se muestra el conjunto de entrenamiento balanceado.

![train_balanceado](assets/img/conjunto_de_entrenamiento_balanceado.png)

4. Curva AUC-ROC


El modelo final permitió realizar predicciones correctas el 72% de las ocasiones superando el requerimiento del cliente.

![curva_auc_roc](assets/img/modelo_final_auc_roc)
