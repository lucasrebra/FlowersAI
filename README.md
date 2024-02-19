
# Documentación del Proyecto de Clasificación de Imágenes de Rosas y Girasoles

## Descripción

Este proyecto utiliza técnicas de aprendizaje profundo para clasificar imágenes en dos categorías: rosas y girasoles. A través de un modelo de Red Neuronal Convolucional (CNN), se busca demostrar la capacidad de las CNNs para reconocer y diferenciar características visuales complejas en imágenes.

## Objetivos

- Desarrollar un modelo de clasificación de imágenes preciso y eficiente.
- Aplicar técnicas de preprocesamiento y aumentación de datos para mejorar el rendimiento del modelo.
- Evaluar el modelo utilizando métricas estándar como precisión, recall y F1-score.

## Tecnologías Utilizadas

- Python
- TensorFlow y Keras para la construcción y entrenamiento de modelos de aprendizaje profundo.
- Matplotlib para la visualización de datos.
- Jupyter Notebook para el desarrollo y la documentación del proyecto.

## Metodología

1. **Preprocesamiento de Datos:** Las imágenes se normalizan y redimensionan para preparar los datos para el entrenamiento.
2. **Aumentación de Datos:** Para aumentar la diversidad del conjunto de entrenamiento, se aplican técnicas de aumentación de datos como rotación y cambio de escala.
3. **Construcción del Modelo:** Se utiliza una arquitectura de CNN, optimizada para la clasificación de imágenes.
4. **Entrenamiento y Validación:** El modelo se entrena con un conjunto de datos de entrenamiento y se valida su rendimiento con un conjunto de datos de validación.
5. **Evaluación:** Se evalúa el modelo final utilizando un conjunto de datos de prueba para determinar su precisión y eficacia en la clasificación de nuevas imágenes.

## Cómo Ejecutar el Código

Para ejecutar este proyecto, sigue estos pasos:

1. Clona el repositorio en tu máquina local.
2. Asegúrate de tener instaladas todas las dependencias necesarias (`requirements.txt`).
3. Abre el cuaderno `Rosesandsunflowers.ipynb` en Jupyter Notebook o JupyterLab.
4. Ejecuta las celdas en orden para ver los resultados del modelo.

## Contribuciones

Las contribuciones al proyecto son bienvenidas. Si deseas contribuir, por favor:

1. Haz un fork del repositorio.
2. Crea una nueva rama para tus cambios.
3. Envía un pull request con tus cambios.

## Licencia

Este proyecto está licenciado bajo [incluir tipo de licencia], lo que permite su uso, modificación y distribución bajo los términos de esa licencia.

# Documentación Avanzada del Modelo de Clasificación de Rosas y Girasoles

## Introducción

Este documento detalla la metodología, arquitectura de red neuronal y resultados obtenidos en el proyecto de clasificación de imágenes de rosas y girasoles. Se utilizaron técnicas avanzadas de aprendizaje profundo para distinguir entre estas dos categorías de imágenes.

## Arquitectura de la Red Neuronal

### Red Neuronal Convolucional Base

- **Preprocesamiento**:
  - Las imágenes se redimensionaron a 180x180 píxeles.
  - Normalización de los valores de píxeles en el rango [0, 1].

- **Arquitectura**:
  - Capas convolucionales con activación ReLU y max pooling.
  - Capa de aplanamiento para transición a capas densas.
  - Capa densa con 128 neuronas y activación ReLU.
  - Capa de salida densa con 2 neuronas (para girasoles y rosas) con activación softmax.

- **Compilación y Entrenamiento**:
  - Optimizador: Adam.
  - Función de pérdida: SparseCategoricalCrossentropy.
  - Métricas: Precisión.
  - 10 épocas, mostrando mejora continua en precisión y disminución de pérdida.

## Resultados

- **Precisión Final en Entrenamiento**: Aproximadamente 98.86%.
- **Precisión Final en Validación**: Aproximadamente 94.77%.

## Mejoras Sugeridas

- Implementación de parada temprana (Early Stopping) para prevenir el sobreajuste.
- Agregar capas de abandono (Dropout) y aplicar técnicas de regularización L2.

## Conclusión

El modelo demostró un alto grado de precisión en el conjunto de entrenamiento y una sólida precisión en el conjunto de validación. Sin embargo, se observó una señal de sobreajuste, lo cual sugiere la necesidad de estrategias adicionales para mejorar la capacidad de generalización del modelo.
