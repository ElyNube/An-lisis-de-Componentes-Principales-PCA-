# Análisis de Componentes Principales (PCA) para Compresión de Imágenes

## 📌 Objetivo del Proyecto
Aplicar el Análisis de Componentes Principales (PCA) para reducir la dimensionalidad y comprimir una imagen digital, evaluando el equilibrio entre la calidad visual de la reconstrucción y el ratio de compresión.
Este proceso permite identificar cuántos componentes son necesarios para mantener la estructura esencial de la imagen ahorrando el máximo espacio de almacenamiento posible sin pérdida perceptible para el ojo humano.

## 🛠️ Herramientas Utilizadas
* **Python:** Lenguaje principal utilizado para el desarrollo matemático y analítico.
* **NumPy:** Utilizado para el cálculo estructurado de la matriz de covarianza, autovalores, autovectores y proyecciones de álgebra lineal.
* **Matplotlib:** Para la visualización gráfica de los resultados, incluyendo el "Scree Plot" (gráfico de codo), MSE y la comparación visual de las imágenes reconstruidas.
* **Scikit-Image & Scikit-Learn:** Para la importación del dataset de prueba (imagen "Camera") y la implementación algorítmica de PCA.

## 📊 Hallazgos Principales
* Se determinó que el primer componente principal (PC1) captura por sí solo el **52.41%** de toda la información (varianza) de la imagen original.
* El análisis del gráfico de codo demostró una alta redundancia espacial, logrando retener más del **90%** de la información visual con apenas 10 componentes.
* Se concluyó que $k=50$ es el número óptimo de componentes, ya que retiene un **97.83%** de la varianza original y ofrece un ahorro de espacio de almacenamiento del **80.27%**.
* A partir de los 50 componentes se entra en un punto de rendimientos decrecientes, donde añadir más variables (por ejemplo, llegar a 100) reduce el error muy poco pero desploma el ahorro de espacio al **60.74%**.
