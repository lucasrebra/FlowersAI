
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
