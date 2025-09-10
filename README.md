# Laboratorio: Muestreo Digital y Análisis FFT con Raspberry Pi Pico

![MicroPython](https://img.shields.io/badge/MicroPython-1.19%2B-green.svg) ![Data Analysis](https://img.shields.io/badge/Analysis-Python/MATLAB-blue.svg)

Este repositorio contiene todos los archivos de datos, resultados y reportes generados durante el laboratorio de **Comunicaciones Digitales**, centrado en el muestreo de señales y el análisis espectral mediante la Transformada Rápida de Fourier (FFT) en una Raspberry Pi Pico.

---

## 📂 Contenido del Repositorio

Aquí encontrarás los informes finales, los datos crudos obtenidos del microcontrolador y los datos procesados de la FFT para cada uno de los casos de prueba.

### 📄 Informes Finales

*   **`CD5.pdf`**: Informe del laboratorio.
*   **`CORTE2INF1.pdf`**: Archivo que documenta el procedimiento por medio de imagenes para este laboratorio.

### 📊 Archivos de Datos de la FFT

Los archivos `.csv` contienen los datos procesados de la Transformada Rápida de Fourier (FFT), listos para ser graficados. La nomenclatura utilizada es la siguiente:

**`fft<N>f<F>.csv`**

Donde:
*   `<N>` es el **número de puntos de la FFT** (ej: `64`, `256`, `2048`).
*   `<F>` es un índice que representa la **frecuencia de la señal de entrada**:
    *   `f1`: Corresponde a la señal de **100 Hz**.
    *   `f2`: Corresponde a la señal de **900 Hz**.
    *   `f3`: Corresponde a la señal de **1800 Hz** (caso de aliasing).

**Ejemplo:** El archivo `fft256f3.csv` contiene los datos del espectro de la señal de **1800 Hz** analizada con una FFT de **256 puntos**.

### 📝 Archivos de Datos Crudos

Estos son los archivos generados directamente por los scripts de MicroPython en la Raspberry Pi Pico.

*   `muestras.txt`: Contiene las muestras de la señal en el **dominio del tiempo** (Tiempo vs. Voltaje).
*   `fft.txt`: Contiene los datos del espectro en el **dominio de la frecuencia** (Frecuencia vs. Magnitud).
*   `datos_fft.csv`: Archivo de datos de la FFT generado por el script de la Parte 2.

---

### 🔬 Conceptos Clave Analizados

*   **Teorema de Nyquist-Shannon:** Se validó experimentalmente, demostrando el fenómeno de **aliasing** con la señal de 1800 Hz.
*   **Resolución de la FFT:** Se analizó cómo el número de puntos de la FFT (`N_FFT`) afecta la precisión en la detección de la frecuencia dominante.
*   **Jitter en Muestreo:** Se estudió el impacto de la inestabilidad en los tiempos de muestreo sobre la calidad del espectro.

---

### 🛠️ Herramientas Utilizadas

*   **Hardware:** Raspberry Pi Pico
*   **Software Embebido:** MicroPython
*   **Análisis y Visualización:** MATLAB y/o Python (con Pandas, NumPy, Matplotlib).

---

### Autor

*   **Andrey Peña**
*   *Universidad Militar Nueva Granada*
