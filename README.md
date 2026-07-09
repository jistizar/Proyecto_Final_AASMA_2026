# Proyecto_Final_AASMA_2026
# 🚗 Stanford Cars: Deep Clustering & Unsupervised Learning

Este repositorio contiene la implementación completa del proyecto final para la asignatura de **Aprendizaje No Supervisado** (Maestría en IA - FIUNA). El objetivo fue agrupar autónomamente 8,144 imágenes de 196 clases de vehículos sin utilizar etiquetas.

## 📁 Dataset
El proyecto utiliza la base de datos pública **Stanford Cars**.
- **Enlace de acceso:** [Stanford Car Dataset by classes folder (Kaggle)](https://www.kaggle.com/datasets/jutrera/stanford-car-dataset-by-classes-folder)
- **Nota de implementación:** Para la ejecución de este *pipeline* y los resultados documentados, se utilizó exclusivamente el conjunto de entrenamiento (`train`), procesando directamente las imágenes distribuidas en sus 196 carpetas de clases.

## 🧠 Metodología Implementada
El proyecto sigue un pipeline moderno de visión artificial:

1.  **Feature Extraction:** Comparativa entre pesos supervisados (**ResNet50**) y modelos fundacionales autosupervisados (**DINOv2**).
2.  **Manifold Learning:** Optimización del espacio latente mediante **UMAP** (fiel a la topología original vs. el colapso observado en LLE/Isomap).
3.  **Clustering Avanzado:**
    * **GMM:** Aproximación probabilística.
    * **HDBSCAN:** Detección de ruido y anomalías topológicas.
    * **DEC (Deep Embedded Clustering):** Optimización conjunta de pesos y clústeres mediante divergencia KL.

## 📊 Resultados Destacados
* **Métrica SOTA:** La arquitectura **DEC** demostró una alta competitividad semántica, supliendo las deficiencias del extractor base.
* **Visualización:** El espacio latente optimizado permite identificar patrones morfológicos (ej. el aislamiento visual de camionetas pickup) prescindiendo totalmente de intervención humana.

## 📂 Estructura del Repositorio
- `notebooks/`: Cuaderno de Jupyter (`.ipynb`) con el código fuente y el pipeline completo de entrenamiento.
- `reporte/`: Informe técnico final documentando la investigación en formato PDF.
- `presentacion/`: Diapositivas utilizadas para la defensa del proyecto (Beamer/PDF).
- `assets/`: Gráficos comparativos, mapas topológicos (UMAP) y fronteras de decisión de los algoritmos.

## 🛠️ Tecnologías
- **PyTorch** (Implementación profunda de DEC y extracción de características).
- **Scikit-learn** (Métricas de evaluación y clustering clásico).
- **UMAP-learn** (Reducción dimensional y manifold learning).
- **DINOv2** (Modelos fundacionales para extracción de features autosupervisada).

---
*Proyecto realizado por: Juan Miguel Martínez Muñoz*
