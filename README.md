# Proyecto_Final_AASMA_2026
#  Stanford Cars: Deep Clustering & Unsupervised Learning

Este repositorio contiene la implementación completa del proyecto final para la asignatura de **Aprendizaje No Supervisado** (Maestría en IA - FIUNA). El objetivo fue agrupar autónomamente 8,144 imágenes de 196 clases de vehículos sin utilizar etiquetas.

##  Metodología Implementada
El proyecto sigue un pipeline moderno de visión artificial:

1.  **Feature Extraction:** Comparativa entre pesos supervisados (**ResNet50**) y modelos fundacionales autosupervisados (**DINOv2**).
2.  **Manifold Learning:** Optimización del espacio latente mediante **UMAP** (fiel a la topología original vs. el colapso observado en LLE/Isomap).
3.  **Clustering Avanzado:**
    * **GMM:** Aproximación probabilística.
    * **HDBSCAN:** Detección de ruido y anomalías.
    * **DEC (Deep Embedded Clustering):** Optimización conjunta de pesos y clústeres mediante divergencia KL.

##  Resultados Destacados
* **Métrica SOTA:** La arquitectura **DEC** logró la mejor cohesión espacial y representatividad semántica.
* **Visualización:** El espacio latente optimizado permite identificar patrones morfológicos (ej. distinción de camionetas pickup) sin intervención humana.

##  Estructura del Repositorio
- `notebooks/`: Cuaderno de Jupyter con el pipeline completo de entrenamiento.
- `reporte/`: Informe técnico final en PDF.
- `assets/`: Gráficos comparativos y proyecciones UMAP.

##  Tecnologías
- **PyTorch** (Implementación de DEC).
- **Scikit-learn** (Métricas y clustering clásico).
- **UMAP-learn** (Reducción dimensional).
- **DINOv2** (Feature extraction).

---
*Proyecto realizado por: Juan Miguel Martínez Muñoz*
