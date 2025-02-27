# **#Representación en forma matricial de la transformada de Fourier**

La Transformada de Fourier puede expresarse en forma matricial, donde la transformación se realiza a través de la multiplicación de una matriz por un vector de datos. Para una secuencia discreta de $N$ puntos, la Transformada Discreta de Fourier (DFT) en forma matricial puede representarse como:

    $X = W_N \cdot x$

Donde:

$X:$ Es un vector columna que contiene los coeficientes de la DFT: $X[0], X[1], ...,X[N-1]$.

$x:$ Es la señal original de la entrada.

$W$: Es la matriz de transformación de dimensión $N×N$

La matriz de transformación $ W$ se puede definir como: $W = \frac{\omega^{jk}}{\sqrt{N}}$

## **Qué pasa si la matriz no es cuadrada?**

Si la matriz de Fourier no es cuadrada $( M \times N ),$ implica que el número de puntos de entrada $ N $ y salida $ M $ son diferentes. Esto tiene implicaciones matemáticas y prácticas:

#### Transformación no invertible

Una matriz no cuadrada no tiene inversa exacta. Esto significa que no podríamos recuperar exactamente la señal original a partir de su transformada.

#### Sobremuestreo o submuestreo

- Si \(M > N\) (más filas que columnas), se produce un **sobremuestreo** en el dominio de la frecuencia, generando redundancia.
- Si \(M < N\) (más columnas que filas), ocurre un **submuestreo**, lo que lleva a pérdida de información.

#### Transformación rectangular

Este tipo de transformación se utiliza en aplicaciones específicas como:

- **Compresión de datos** (cuando \(M < N\))
- **Análisis espectral con mayor resolución** (cuando \(M > N\))
- **Zero-padding** (cuando se añaden ceros para aumentar la resolución frecuencial)
