<div align="center">

# 🐍 Práctica N.º 3 · El Perceptrón

**Clasificación binaria con una unidad de decisión lineal, implementada desde cero**

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/xErnyx/Practica_3_El_Perceptron/blob/main/Practica_3_El_Perceptron.ipynb)

</div>

---

## 📌 Descripción

Práctica 3 de **Inteligencia Artificial** (Universidad Salesiana del Ecuador, Sede Sur). El perceptrón se programa **a mano**, sin librerías de machine learning: función de activación, propagación hacia adelante y regla de actualización de pesos. Después se entrena sobre un dataset de 23 puntos en el plano, se dibuja cómo se mueve la frontera de decisión durante el aprendizaje y se compara el efecto de la tasa de aprendizaje.

Cada fase presenta el fundamento teórico, el código paso a paso y las respuestas a las preguntas guía con los resultados reales de la ejecución.

## 🎯 Objetivos

- Implementar manualmente la activación, la propagación hacia adelante y la regla de aprendizaje.
- Entrenar un perceptrón sin librerías de machine learning.
- Visualizar la frontera de decisión y su evolución durante el entrenamiento.
- Analizar la influencia de la tasa de aprendizaje en la convergencia.
- Evaluar el modelo con instancias nuevas que no se usaron para entrenar.

## 🗂️ Contenido

| Fase | Tema | Qué se hace |
|:---:|---|---|
| 1 | Exploración del dataset | Conteo de instancias y clases con ciclos, gráfica de los puntos |
| 2 | Fundamento del perceptrón | `initialize_weights()`, `activation(z)`, `perceptron_compute(x, w)` |
| 3 | Frontera de decisión | `perceptron_plot()` con el caso especial $w_2 = 0$ |
| 4 | Entrenamiento | `perceptron_learning()` con registro de error y de pesos por época |
| 5 | Entrenamiento con `lr = 0.5` | Convergencia y frontera final |
| 6 | Predicción | Clasificación de 3 instancias nuevas y dataset extendido |
| 7 | Evolución de la frontera | Seis estados del entrenamiento (inicial, 20 %, 40 %, 60 %, 80 %, final) |
| 8 | Evolución del error | `plot_error()` y análisis de convergencia |
| 9 | Comparación de tasas | `lr = 0.3`, `0.5` y `0.8` con los mismos pesos iniciales |

## 📊 Resultados destacados

**Dataset:** 23 instancias, 2 variables de entrada ($x_1$, $x_2$), 2 clases (14 de la clase −1 y 9 de la clase +1).

**Entrenamiento con `lr = 0.5`** (semilla 42): convergió en **133 épocas** y **411 actualizaciones**, con pesos finales `[-71.1255, 3.4507, 7.2320]` y error final 0. Los pesos iniciales aleatorios cometían 14 errores de 23.

**Predicciones de instancias nuevas:**

| Instancia | Salida predicha |
|:---:|:---:|
| `[5, 5]` | −1 |
| `[10, 6]` | +1 |
| `[6, 10]` | +1 |

**Comparación de tasas de aprendizaje** (mismos pesos iniciales):

| lr | Épocas | Actualizaciones | Error final |
|:---:|:---:|:---:|:---:|
| 0.3 | 315 | 1019 | 0.0 |
| 0.5 | 133 | 411 | 0.0 |
| 0.8 | 105 | 337 | 0.0 |

> Con otras semillas el orden de las tasas cambia, así que la mejor tasa depende también de los pesos iniciales. El notebook lo comprueba con cinco semillas.

## 🚀 Cómo ejecutarlo

**En Google Colab (recomendado):** pulsa el botón **Abrir en Colab** de arriba. Las librerías ya vienen instaladas.

**En local:**

```bash
git clone https://github.com/xErnyx/Practica_3_El_Perceptron.git
cd Practica_3_El_Perceptron
pip install numpy matplotlib pandas jupyter
jupyter notebook Practica_3_El_Perceptron.ipynb
```

Antes de revisar los resultados, ejecuta **Runtime → Restart and run all** para confirmar que no hay errores. Los pesos iniciales usan `np.random.seed(42)`, por lo que las salidas son reproducibles.

## 🛠️ Tecnologías

- **Python 3**
- **NumPy**: arrays y operaciones numéricas
- **Matplotlib**: gráficas de la frontera de decisión y del error
- **pandas**: solo para presentar tablas de resultados
- **Jupyter Notebook / Google Colab**

## 📁 Estructura

```
Practica_3_El_Perceptron/
├── Practica_3_El_Perceptron.ipynb   # Notebook completo con código, gráficas y respuestas
├── README.md
└── LICENSE
```

## 👤 Autor

**Juan D. Figueroa** · [@xErnyx](https://github.com/xErnyx)
Ciencias de la Computación, Universidad Salesiana del Ecuador, Sede Sur
Docente: Ing. Rodrigo Tufiño, MSc.

## 📚 Referencias

- Harris, C. R., Millman, K. J., van der Walt, S. J., Gommers, R., Virtanen, P., Cournapeau, D., ... Oliphant, T. E. (2020). Array programming with NumPy. <i>Nature, 585</i>(7825), 357–362. https://doi.org/10.1038/s41586-020-2649-2
- Hunter, J. D. (2007). Matplotlib: A 2D graphics environment. <i>Computing in Science &amp; Engineering, 9</i>(3), 90–95. https://doi.org/10.1109/MCSE.2007.55
- Tufiño, R. (2026). <i>Guía de práctica de laboratorio N.° 03: El perceptrón</i> [Material de clase, Inteligencia Artificial]. Universidad Salesiana del Ecuador - Sede sur.

## 📄 Licencia

Distribuido bajo la licencia **MIT**. Consulta el archivo `LICENSE` para más información.

---

<div align="center">

### ⭐ ¿Te sirvió este proyecto?

Si te ayudó a entender cómo aprende un perceptrón, deja una **estrella** al repositorio. ¡Se agradece mucho!

</div>
