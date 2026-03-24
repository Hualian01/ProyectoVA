# Proyecto Final de Visión Artificial
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter%20Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-27338e?style=for-the-badge&logo=OpenCV&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Numpy](https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white)

El siguiente trabajo trata sobre el desarrollo de una aplicación móvil para la identificación de especies de mariposas en Panamá, utilizando Python, OpenCV, y un modelo de aprendizaje automático. El proyecto busca facilitar el acceso a información sobre el estado de conservación de las mariposas y contribuir a su preservación. 

## Objetivos
- Desarrollar un algoritmo de detección y clasificación de mariposas utilizando OpenCV en Python.
- Crear una base de datos con imágenes etiquetadas de mariposas para entrenar el modelo.
- Implementar el sistema de reconocimiento de especies en una aplicación móvil utilizando Android Studio.
- Evaluar la precisión del modelo mediante pruebas de campo.
- Optimizar la experiencia de usuario y la eficiencia del sistema en dispositivos móviles.

## Resultados
### Construcción y Desarrollo del Prototipo
El objetivo del prototipo desarrollado fue crear un modelo de clasificación de mariposas que pudiera identificar 10 especies distintas a partir de imágenes. Para lograrlo, se utilizó la biblioteca de aprendizaje profundo TensorFlow, junto con un conjunto de datos que contenía más de 700 imágenes de referencia. Este prototipo se diseñó para ser implementado en una aplicación Android mediante una API en la nube, permitiendo así la clasificación en tiempo real desde dispositivos móviles.

### Arquitectura del Modelo en TensorFlow
El modelo fue diseñado utilizando una arquitectura de red neuronal convolucional (CNN), adecuada para tareas de clasificación de imágenes debido a su capacidad de extraer patrones visuales. La red incluyó capas convolucionales para la extracción de características, seguidas de capas de agrupamiento (pooling) y capas densas para la clasificación. Para la función de activación, se empleó ReLU en las capas intermedias, y Softmax en la capa de salida, dado que se trata de una clasificación multicategoría. La función de pérdida utilizada fue la entropía cruzada categórica, y el modelo fue evaluado en términos de precisión y pérdida durante el entrenamiento.

### Despliegue del modelo
Tras el entrenamiento, el modelo fue convertido al formato TensorFlow Lite para optimizar su uso en dispositivos móviles. Dado que el modelo pesaba 600 MB, superando el límite de 200 MB para aplicaciones Android, se optó por desplegarlo en la nube y crear una API usando Flask. Esta API permite a la aplicación Android enviar imágenes al servidor, donde el modelo procesa la predicción y envía los resultados de vuelta a la aplicación en tiempo real. 

![G](https://github.com/Hualian01/ProyectoVA/blob/main/img/imagen1.png)

![Z](https://github.com/Hualian01/ProyectoVA/blob/main/img/imagen2.png)

![X](https://github.com/Hualian01/ProyectoVA/blob/main/img/imagen3.png)

### Metodología de prueba 
Las pruebas se realizaron utilizando el 20% de las imágenes disponibles, seleccionadas como conjunto de prueba. Las métricas utilizadas para evaluar el desempeño incluyeron la precisión por especie, la tasa de error y el tiempo de respuesta para cada predicción.

### Resultados obtenidos
En general, el modelo alcanzó una precisión promedio del 92% en la clasificación de las especies de mariposas. Sin embargo, se observaron variaciones en el desempeño según la especie: mientras que algunas especies presentaron una precisión cercana al 95%, otras se clasificaron con un margen de error mayor.

### Análisis de resultados
El modelo logró una alta precisión en la mayoría de las especies, cumpliendo con los objetivos de identificación propuestos. Sin embargo, algunas especies con patrones visuales similares mostraron mayor tasa de error. Esto sugiere que la precisión del modelo podría mejorar aún más con un conjunto de datos más amplio o al incorporar más técnicas de aumento de datos para reducir la similitud entre clases.

Otro factor relevante fue la calidad de las imágenes: se observó que imágenes con mayor resolución produjeron mejores resultados en comparación con aquellas de baja calidad. Además, el tiempo de respuesta promedio fue adecuado para el uso en tiempo real, demostrando que el modelo, al ser implementado en la nube, es viable para aplicaciones móviles.

## Conclusión
Este proyecto logró el desarrollo de un modelo de clasificación de mariposas, con una precisión promedio del 92% en la identificación de 10 especies diferentes. Este modelo, al estar implementado en la nube, permite el acceso desde una aplicación Android, facilitando la identificación en tiempo real.

Aunque la aplicación es funcional, existen limitaciones relacionadas con la dependencia de la conexión a internet y la calidad de las imágenes. En futuros desarrollos, sería beneficioso explorar métodos de compresión para permitir la ejecución en dispositivos móviles o incorporar un módulo de preprocesamiento de imágenes.

## Autor
Rebeca Mendoza, <b>[LinkedIn](https://www.linkedin.com/in/rebeca-mendoza-240401375/)</b> y
Enrique Vega, <b>[LinkedIn](https://www.linkedin.com/in/enrique-vega-pty14/)</b>
