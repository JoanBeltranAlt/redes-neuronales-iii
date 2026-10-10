# Redes Neuronales III — Optimización, Regularización y Evaluación

![Python](https://img.shields.io/badge/Python-3.x-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange)
![Colab](https://img.shields.io/badge/Google%20Colab-ready-yellow)

Tercera práctica de la serie de Deep Learning: aplica técnicas de **optimización** (SGD, momentum, RMSProp, Adam, learning rate decay, batch normalization), **regularización** (L2, Dropout, Early Stopping) y **métricas de evaluación** (accuracy, precision, recall, F1-score, matriz de confusión, sensitivity/specificity) sobre una red neuronal densa entrenada con el dataset **MNIST**.

Continúa la entrega anterior: [redes-neuronales-ii](https://github.com/JoanBeltranAlt/redes-neuronales-ii) (backpropagation, funciones de activación, clasificación multiclase con TensorFlow/Keras y PyTorch).

**Repositorio:** https://github.com/JoanBeltranAlt/redes-neuronales-iii
**Entorno:** Google Colab

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/JoanBeltranAlt/redes-neuronales-iii/blob/main/Redes_Neuronales_III_Optimizacion_Regularizacion_Metricas.ipynb)

## Tabla de contenido

- [Objetivo de la práctica](#objetivo-de-la-práctica)
- [Estructura del repositorio](#estructura-del-repositorio)
- [Contenido del notebook](#contenido-del-notebook)
- [Resultados](#resultados)
- [Cómo ejecutarlo](#cómo-ejecutarlo)
- [Requisitos cumplidos](#requisitos-cumplidos)
- [Autor](#autor)

## Objetivo de la práctica

Profundizar, sobre el dataset MNIST ya trabajado en la entrega anterior, en los contenidos de las semanas 5 a 7 de la asignatura:

- **Semana 5 — Optimización:** hiperparámetros, conjuntos train/dev/test, feature scaling, batch normalization, mini-batch gradient descent, momentum, RMSProp, Adam y learning rate decay.
- **Semana 6 — Regularización:** bias/variance tradeoff, overfitting, regularización L1/L2, Dropout y Early Stopping.
- **Semana 7 — Evaluación:** matriz de confusión, accuracy, precision, recall, F1-score, sensitivity/specificity, y la correcta distribución y preprocesamiento de los datos.

## Estructura del repositorio

```
redes-neuronales-iii/
├── Redes_Neuronales_III_Optimizacion_Regularizacion_Metricas.ipynb
├── comparacion_optimizadores.png
├── evidencia_overfitting.png
├── efecto_regularizacion.png
├── matriz_confusion.png
└── README.md
```

## Contenido del notebook

| Sección | Descripción |
|---|---|
| 0-2 | Carga de MNIST, división train/dev/test y preprocesamiento (escalado de píxeles) |
| 3 | Comparación de optimizadores (SGD, SGD+Momentum, RMSProp, Adam) con Batch Normalization, y learning rate decay |
| 4 | Demostración de overfitting (bias/variance) con una red sobredimensionada entrenada sobre pocos datos |
| 4 (cont.) | Corrección del overfitting aplicando L2, Dropout y Early Stopping sobre la misma arquitectura |
| 5 | Modelo final: métricas completas (accuracy, precision, recall, F1-score macro), matriz de confusión y sensitivity/specificity por dígito |
| 6 | Conclusiones |

## Resultados

- Adam y RMSProp convergieron más rápido y de forma más estable que SGD puro en el mismo número de épocas.
- El modelo sobredimensionado sin regularización mostró una brecha clara entre accuracy de entrenamiento y de validación (alta variance / overfitting).
- Al aplicar L2 + Dropout + Early Stopping sobre la misma arquitectura, esa brecha se redujo de forma notoria.
- El modelo final, entrenado con una distribución adecuada de datos y regularización moderada, alcanzó un desempeño alto y consistente en todas las métricas evaluadas sobre el conjunto de prueba.

## Cómo ejecutarlo

1. Entrar a [Google Colab](https://colab.research.google.com/) o hacer clic en el badge de arriba.
2. Si se abre manualmente: `Archivo → Abrir notebook → GitHub`, pegar la URL de este repositorio y seleccionar el notebook.
3. Ejecutar todas las celdas en orden (`Entorno de ejecución → Ejecutar todas`).
4. TensorFlow ya viene preinstalado en Google Colab; no se requiere instalación adicional. MNIST se descarga automáticamente.

## Requisitos cumplidos

- [x] Desarrollo individual en Google Colab, con TensorFlow + Keras.
- [x] Conjuntos train/dev/test correctamente distribuidos y documentados.
- [x] Preprocesamiento de datos (feature scaling, aplanado de imágenes).
- [x] Técnicas de optimización: SGD, momentum, RMSProp, Adam, learning rate decay, batch normalization.
- [x] Bias/variance tradeoff evidenciado experimentalmente (overfitting controlado).
- [x] Métodos de regularización: L2, Dropout, Early Stopping.
- [x] Métricas de evaluación: accuracy, precision, recall, F1-score, matriz de confusión, sensitivity, specificity.
- [x] Resultados y evidencias de ejecución incluidos en el notebook (gráficas y métricas reales).
- [x] Código fuente funcional, comentado y documentado.
- [x] Notebook ejecutado de extremo a extremo sin errores.
- [x] Publicado en repositorio GitHub con enlace funcional.
- [x] Documento técnico en PDF con código, explicaciones y resultados.

## Autor

**Joan Schneider Beltrán Delgado**
Especialización en Inteligencia Artificial — Deep Learning, Universidad de Cundinamarca
