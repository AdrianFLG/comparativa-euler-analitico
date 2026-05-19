# comparativa-euler-analitico
# Comparación de Soluciones Analíticas y Numéricas

Este repositorio contiene la resolución de una ecuación diferencial ordinaria (EDO) mediante dos enfoques: el método analítico exacto por **separación de variables** y la aproximación numérica usando el **método de Euler**.

## Descripción del Problema

Se modela la **Ley de Enfriamiento de Newton**, la cual establece que la tasa de cambio de la temperatura de un objeto es proporcional a la diferencia entre su propia temperatura y la temperatura del medio ambiente.

### Ecuación Diferencial:
dT/dt = -k * (T - Ta)

**Parámetros utilizados:**
* Temperatura inicial (t = 0): T(0) = 80 °C
* Temperatura ambiente: Ta = 20 °C
* Constante de enfriamiento: k = 1.5
* Intervalo de tiempo: t de [0, 1]
* Tamaño del paso numérico: h = 0.2

---

## Solución Analítica (Separación de Variables)

Partiendo de la ecuación diferencial, separamos las variables e integramos en ambos lados:

1. dT / (T - Ta) = -k * dt
2. ln|T - Ta| = -k * t + C
3. T - Ta = C * e^(-k * t)

Aplicando la condición inicial T(0) = T0, encontramos que C = T0 - Ta. Por lo tanto, la **solución exacta** es:

T(t) = Ta + (T0 - Ta) * e^(-k * t)

---

## Solución Numérica (Método de Euler)

El método de Euler aproxima el siguiente valor de la variable dependiente utilizando la pendiente actual del sistema multiplicada por el tamaño del paso $h$:

T_(n+1) = T_n + h * (-k * (T_n - Ta))

---

## Requisitos para Ejecución

El script está escrito en **Python 3** y requiere las siguientes librerías estándar de ciencia de datos:
* numpy
* matplotlib

Puedes clonar este repositorio y ejecutar el archivo directamente en tu entorno local o en Google Colab:
```bash
git clone <URL_DE_TU_REPOSITORIO>
