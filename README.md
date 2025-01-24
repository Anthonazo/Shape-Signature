# Clasificación de Imágenes Basada en Shape-Signature

Este proyecto tiene como finalidad desarrollar un modelo de clasificación de imágenes utilizando la representación de forma (shape-signature). El objetivo principal es predecir la categoría de una imagen, medir la confianza de las predicciones y evaluar el desempeño del modelo mediante métricas como la matriz de confusión.

## Categorías Analizadas
Se trabajó con cinco categorías de imágenes para realizar la clasificación:
- **bottle**
- **children**
- **personal_car**
- **flatfish**
- **pencil**

## Descripción del Proyecto

1. **Preparación de Datos**  
   - Se recopilaron imágenes correspondientes a cada categoría.
   - Las imágenes fueron organizadas en un archivo comprimido `.zip` para su análisis en Google Colab.
   - Se generaron dos archivos `.csv` con las firmas de las imágenes:
     - Un archivo de **entrenamiento** con 6 valores por categoría.
     - Un archivo de **prueba** con 4 valores por categoría.

2. **Método Utilizado**  
   - Se utilizó la representación de forma (shape-signature) de las imágenes para clasificar las categorías. Esta técnica se basa en la extracción de características relacionadas con la forma de cada objeto en la imagen.
   - El modelo fue entrenado con las firmas del archivo de entrenamiento y probado con el archivo de prueba para evaluar su precisión.

3. **Visualización y Evaluación**  
   - Se generó una matriz de confusión para analizar el rendimiento del modelo.
   - Las predicciones erróneas fueron revisadas visualmente, comprobando que las firmas de las imágenes con errores eran similares a las de las categorías predichas incorrectamente.

## Resultados

- **Precisión General**: El modelo logró una precisión del **75%**, clasificando correctamente 15 de las 20 imágenes analizadas.
- **Errores Detectados**:
  - Las categorías **flatfish** y **personal_car** presentaron errores significativos debido a similitudes en las firmas de las imágenes.
  - En la categoría **pencil**, una imagen fue clasificada erróneamente como **personal_car**.
- **Análisis de Firmas**:
  - Las firmas de las imágenes con errores mostraron gran similitud con las de otras categorías, destacando la necesidad de aumentar la variedad de datos de entrenamiento para mejorar la precisión.

## Conclusiones

1. **Similitud entre Firmas**  
   Las predicciones erróneas del modelo se explican por similitudes visuales entre las formas de ciertas categorías, especialmente entre **flatfish** y **personal_car**.

2. **Necesidad de Más Datos**  
   Para mejorar el desempeño del modelo, es necesario ampliar el conjunto de datos de entrenamiento, incorporando firmas más diversas y representativas de cada categoría.

3. **Potencial del Método**  
   A pesar de los errores, la técnica basada en shape-signature demostró ser efectiva para clasificar imágenes con formas distintivas. Con un mayor volumen y variedad de datos, el modelo puede alcanzar resultados más robustos y confiables.

## Reproducción del Proyecto

1. **Requisitos Previos**
   - Python 3.x
   - Librerías necesarias:
     ```bash
     pip install numpy pandas matplotlib opencv-python
     ```

2. **Ejecución**
   - Subir el archivo comprimido `.zip` con las imágenes a Google Colab.
   - Descomprimir las imágenes y generar los archivos `.csv` de firmas.
   - Entrenar el modelo con los datos del archivo de entrenamiento.
   - Evaluar el modelo con los datos del archivo de prueba.
   - Generar la matriz de confusión y analizar los resultados.

3. **Código Principal**
   El código principal para reproducir este proyecto está disponible en el archivo [`Shape_Signature.ipynb`](Shape_Signature.ipynb). Este incluye la carga de datos, entrenamiento del modelo, evaluación y visualización de resultados.

## Matriz de Confusión

A continuación, se presenta la matriz de confusión generada durante el análisis:

![matrix](https://github.com/user-attachments/assets/e53e3d13-3c31-44ec-9fdf-5edefb8b3f91)

## Próximos Pasos

1. **Ampliar el Conjunto de Datos**  
   - Recopilar más imágenes con mayor variabilidad en las formas de cada categoría.
   - Realizar un preprocesamiento adicional para mejorar la calidad de las firmas.

2. **Optimización del Modelo**  
   - Probar algoritmos de clasificación más avanzados, como redes neuronales o SVM.
   - Implementar técnicas de ajuste fino para mejorar la precisión en categorías con errores significativos.

3. **Evaluación Extendida**  
   - Utilizar métricas adicionales, como la precisión, el recall y el F1-score, para evaluar el rendimiento del modelo de manera más detallada.

