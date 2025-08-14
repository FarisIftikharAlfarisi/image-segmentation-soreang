<p align="center">
  <b>Satellite Image Segmentation Using Unsupervised Learning for Land Cover Analysis in Soreang with Spatial–Spectral Feature Optimization</b>  
</p>
---

<p align="center">
  <i>Segmentasi Citra Satelit Menggunakan Metode Unsupervised Learning untuk Analisis Tutupan Lahan di Soreang dengan Optimasi Berbasis Fitur Spasial–Spektral</i>  
</p>

<p align="center">
  <b>Faris Iftikhar Alfarisi</b>  
</p>
<p align="center">
<a href="https://www.instagram.com/frs.alfrs_/"><img src="https://img.shields.io/badge/Instagram-faris__awesome-orange?logo=instagram" alt="Instagram"></a>
<a href="mailto:faris.workingspace@gmail.com"><img src="https://img.shields.io/badge/Email-faris%40example.com-blue?logo=gmail" alt="Email"> individual email :  faris.workingspace@gmail.com </a>
<a href="mailto:faris.10122050@mahasiswa.unikom.ac.id "><img src="https://img.shields.io/badge/Email-faris%40example.com-blue?logo=gmail" alt="Email"> institutional email :  faris.10122050@mahasiswa.unikom.ac.id </a>
</p>

---

## Objective
This project aims to develop a satellite image segmentation system based on *unsupervised learning* to analyze land cover in the Soreang region. The approach focuses on identifying settlements, forests, and agricultural land by leveraging a combination of spatial and spectral features, ensuring effectiveness even with a limited dataset.

---

## Methodology Approach
The study began with the collection of RGB satellite images from Google Earth for the years 2001 and 2024. The data underwent a *preprocessing* stage that included color intensity normalization (0–1) and conversion to grayscale to support texture and edge feature extraction. The segmentation process utilized the SLIC superpixel method, which divides the image into hundreds of homogeneous segments, allowing for more precise feature extraction.

Feature extraction covered five main categories:  
1. **Color**, represented in the CIELAB space (L*, a*, b*).  
2. **Texture**, using entropy and variance metrics.  
3. **Spatial frequency**, via Fast Fourier Transform (FFT Mean and FFT Std).  
4. **Edges**, using Sobel Edge Density.  
5. **Spatial position**, represented by centroid X and Y coordinates.  

All extracted features were combined into high-dimensional vectors and clustered using the K-Means algorithm. Hyperparameter optimization was performed, with the best configuration achieved at k = 4 clusters, `k-means++` initialization, and the Lloyd algorithm. Evaluation using Silhouette Score (0.5219), Calinski-Harabasz Index (1054.65), and Davies-Bouldin Index (0.5480) indicated balanced segmentation performance in terms of compactness and separation.

---

## Results
The segmentation results demonstrate the model's capability to effectively distinguish between settlement areas and vegetated regions. Forests and conservation areas were clearly identified, while settlements were separated from agricultural land. The main challenge was differentiating between active and post-harvest paddy fields, as both share similar spectral characteristics, often resulting in them being grouped within the same cluster.

---

## 📌 Conclusion
The K-Means-based segmentation method, combined with color, texture, frequency, edge, and spatial position features, proved effective for label-free land cover mapping, especially with small datasets. The use of SLIC superpixels significantly enhanced segmentation boundary precision. In the future, this system could be extended with temporal data integration for seasonal change detection, automated calculation of land cover area, and the application of *deep clustering* techniques to improve adaptability to complex spatial patterns.

---

## 📚 Keywords
`K-Means` `Image Segmentation` `Unsupervised Learning` `Land Cover` `Satellite Imagery` `SLIC Superpixel`

---

<p align="center">
  <i>This project was developed as part of the Supply Chain Management course, Bachelor of Informatics Engineering, Universitas Komputer Indonesia</i>
</p>
