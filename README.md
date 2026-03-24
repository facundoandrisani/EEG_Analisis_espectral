# 🌊 Detección de Crisis Epilépticas: Análisis Espectral y de Frecuencia

Este proyecto aborda el procesamiento de series temporales de electroencefalogramas (EEG) desde el dominio de la frecuencia. A través de técnicas de procesamiento digital de señales, buscamos aislar y comprender cómo varía la energía de las distintas bandas cerebrales durante un evento epiléptico.

## 🎯 ¿Qué hace este proyecto?
A partir de la ingesta de registros de la **CHBMIT Scalp EEG Database**, el código segmenta la actividad en periodos pre-ictales, ictales y post-ictales. El núcleo del proyecto consiste en aplicar transformaciones matemáticas complejas:
* **Estimación Espectral:** Cálculo comparativo de la Transformada Rápida de Fourier (FFT) y la Densidad Espectral de Potencia (PSD).
* **Descomposición por Bandas:** Generación de espectrogramas dividiendo la señal en los rangos biológicos clásicos: Delta (0-4 Hz), Theta (4-8 Hz), Alpha (8-12 Hz), Beta (12-30 Hz) y Gamma (30-64 Hz).
* **Análisis de Ventanas:** Uso de periodogramas y la Transformada de Fourier a Corto Plazo (STFT) iterando sobre distintas ventanas y configuraciones de superposición (*overlapping*).

## 🔍 ¿Qué buscamos?
El objetivo es aislar las "firmas frecuenciales" de la epilepsia para optimizar su detección. En este análisis buscamos:
1. **Limpieza de Señal:** Identificar visualmente frecuencias parasitarias (no deseadas) y aplicar filtros sin alterar la señal cerebral original.
2. **Optimización de Parámetros:** Determinar cuáles son las mejores combinaciones de ventanas, solapamientos y canales para detectar la crisis con mayor precisión.
3. **Discriminación Visual:** Encontrar diferencias significativas entre los distintos segmentos temporales mapeando los resultados espectrales en *scatterplots*.
4. **Eficiencia Computacional:** Analizar la complejidad de las rutinas de procesamiento de señales.

## 🛠️ Tecnologías y Herramientas
* Python (`pyedflib` para procesamiento de archivos `.edf`).
* Análisis digital de señales (FFT, PSD, STFT).
* Visualización avanzada (Espectrogramas y Periodogramas).
