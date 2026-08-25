# Laboratorio 1 — [Nombre del equipo]

> Repo creado a partir del template de la cátedra para el Laboratorio 1: _Python for Data Analysis_ (3rd Ed).

## 📌 Datos del equipo

- **Equipo:** `Loompy`
- **Capítulo(s) asignado(s):** `14: Simple Linear Regression - Grus`
- **Integrantes:** `Castro, Mauricio Nicolás`, `Lopez Gutierrez, Daniel Benjamin`, `López, Tomas Agustin`, `Martínez, Agustín Francisco`, `Peralta Ruiz, Nadine Andrea`

## 🎯 Objetivos de la clase

Comprender e implementar los fundamentos teóricos y prácticos de la **Regresión Lineal Simple** aplicados al análisis inmobiliario del conjunto de datos de Properati. Al finalizar la clase, se espera que el resto del curso pueda:

- **El modelo de regresión lineal:** modelar la relación entre una variable independiente (x) y una dependiente (y) mediante **y = α + βx + ε**, interpretando el significado práctico de la pendiente (β) y la ordenada al origen (α).
- **El error de predicción y la suma de errores al cuadrado (RSS):** cuantificar los residuos (y − ŷ) y entender por qué se utiliza RSS como función de costo (evita la cancelación de signos y penaliza desvíos grandes).
- **El método de mínimos cuadrados (OLS):** calcular de forma exacta y directa la recta óptima (α y β) a partir de las medias, varianzas y la covarianza entre las variables de la muestra.
- **El coeficiente de determinación (R²):** medir qué porcentaje de la varianza total es explicada por el modelo y usar esta métrica para comparar y seleccionar la mejor variable independiente.
- **Optimización mediante descenso del gradiente:** implementar un enfoque iterativo para encontrar la recta óptima y comprobar cómo llega al mismo resultado que mínimos cuadrados al escalar adecuadamente las variables.
- **Estimación de máxima verosimilitud (MLE):** comprender el sustento probabilístico del modelo y por qué minimizar RSS equivale a maximizar la verosimilitud asumiendo errores con distribución normal.

## 📂 Estructura del repositorio

```
.
├── notebooks/
│   ├── demo_equipo.ipynb        # Notebook demostrativo
│   └── ejercicios_equipo.ipynb  # Ejercicios guiados para el resto de la clase
├── slides/
│   └── PLACEHOLDER.md            # Espacio reservado para las diapositivas
├── requirements.txt              # Dependencias del proyecto
└── README.md                     # Documentación e informe del laboratorio
```

## 🗂️ Dataset usado

- **Nombre / fuente:** [Properati Argentina Dataset](https://www.kaggle.com/datasets/alejandroczernikier/properati-argentina-dataset), disponible en Kaggle.
- **Descripción del escenario:** Se analizarán propiedades publicadas en Argentina para estudiar la relación entre la superficie de una propiedad y su precio. En el escenario hipotético, una persona que busca comprar una propiedad quiere obtener una estimación inicial del precio a partir de los metros cuadrados, utilizando una regresión lineal simple. Se explorarán los datos, se limpiarán los registros necesarios y se evaluará qué tan bien explica la superficie la variación observada en los precios.

## ▶️ Cómo ejecutar

1. Clona el repositorio y abre la carpeta del proyecto.
2. Crea y activa un entorno virtual de Python:

   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

3. Instala las dependencias del proyecto:

   ```powershell
   python -m pip install --upgrade pip
   pip install -r requirements.txt
   ```

4. En el IDE, selecciona el intérprete de Python ubicado en `.venv` y abre el notebook correspondiente desde la carpeta `notebooks/`.
5. Ejecuta las celdas en orden. Se recomienda comenzar con `demo_equipo.ipynb` y luego resolver `ejercicios_equipo.ipynb`.

### Ejecución en Google Colab

También pueden ejecutar los notebooks en Google Colab sin instalar Python localmente:

1. Abran `demo_equipo.ipynb` o `ejercicios_equipo.ipynb` en Colab desde el repositorio, o súbanlo manualmente desde la opción **File > Upload notebook**.
2. Ejecuten las celdas en orden. Si trabajan con `ejercicios_equipo.ipynb`, comiencen por la celda de configuración para descargar y preparar el dataset de Properati.

### Organización del trabajo

Para este laboratorio no definimos una estrategia específica de ramas. Como las tareas tenían un flujo de trabajo acotado y lineal, trabajamos directamente sobre el repositorio y coordinamos los cambios entre nosotros según las necesidades del proyecto.

## 🧩 Ejercicio para el resto de la clase

En la notebook `ejercicios_equipo.ipynb` proponemos aplicar los conceptos de regresión lineal simple al dataset de Properati mediante una serie de ejercicios guiados. Primero, deberán implementar las funciones para calcular la pendiente y la ordenada al origen a partir de la cantidad de habitaciones y el precio de las propiedades. Luego, utilizarán esos parámetros para estimar el precio de una propiedad de tres habitaciones.

Como desafío final, les pedimos comparar dos modelos: uno que use la cantidad de habitaciones y otro que use la superficie total para predecir el precio. Para ello, deberán calcular los parámetros de ambos modelos, representar los datos junto con sus rectas de regresión y analizar cuál de las dos variables explica mejor la variación del precio. Como cierre, incluimos un cuestionario de opción múltiple para repasar y consolidar los principales conceptos de regresión lineal simple, como RSS, estimaciones, OLS, R² y MLE.

## 🙌 Créditos

- Libro base: _Python for Data Analysis, 3rd Edition_ — Wes McKinney, O'Reilly.
- Dataset: [Properati Argentina Dataset](https://www.kaggle.com/datasets/alejandroczernikier/properati-argentina-dataset), publicado en Kaggle por Alejandro Czernikier.
- Material complementario: curso _Regression Analysis: Simplify Complex Data Relationships_, perteneciente al programa Google Advanced Data Analytics Professional Certificate de Coursera.
