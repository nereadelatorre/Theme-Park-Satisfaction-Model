# Disneyland Paris Queue & Satisfaction Simulation

Este proyecto desarrolla un modelo de simulación de eventos discretos para analizar y optimizar los tiempos de espera en las atracciones de **Disneyland París**. Además de modelar las colas físicas, el proyecto incorpora un **modelo de satisfacción del usuario** que cuantifica cómo la espera, la fatiga y las expectativas afectan a la experiencia del visitante.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![SimPy](https://img.shields.io/badge/Library-SimPy-orange)
![Data Science](https://img.shields.io/badge/Analysis-Pandas%20%7C%20Seaborn-green)

## Descripción
El objetivo principal es entender las dinámicas de flujo de visitantes y proponer mejoras en la gestión de colas. A diferencia de modelos tradicionales que solo miden tiempos, este proyecto:
1.  **Simula la operativa real** de atracciones específicas (ej. *Big Thunder Mountain*) considerando capacidad de vehículos, tiempos de carga y averías.
2.  **Calcula la satisfacción subjetiva**, diferenciando entre el tiempo real y el tiempo percibido por el cliente.
3.  **Calibra el modelo** utilizando datos reales de valoraciones y tiempos de espera.

## Librerias utilizadas
* **Simulación:** `SimPy` (Event Discrete Simulation).
* **Análisis de Datos:** `Pandas`, `NumPy`.
* **Visualización:** `Matplotlib`, `Seaborn`.
* **Entorno:** Jupyter Notebooks.

## Estructura del Proyecto
El repositorio contiene el informe completo (`Experiència_usuari_complet.pdf`) y los siguientes módulos de código:

### 1. Simulación Base
* `simulacio_temps_espera.ipynb`: Implementación del núcleo de la simulación. Define la llegada de visitantes, la lógica de las colas (FIFO) y la dinámica de carga de las atracciones. Compara los tiempos esperados vs. simulados.

### 2. Modelo de Satisfacción
* `simulacio_amb_satisfaccio.ipynb`: Expande la simulación introduciendo variables psicológicas (paciencia media, coeficiente de fatiga). Genera métricas de satisfacción final para cada usuario.

### 3. Validación y Verificación
* `ValidacioVerificacioTempsEspera.ipynb`: Scripts de validación para asegurar que el modelo se comporta de manera lógica (ej. análisis de tasas de abandono y consistencia estadística de los resultados).

### 4. Calibración (Inferencia)
* `inferencia.ipynb`: Utiliza técnicas de búsqueda (Grid Search) para inferir el valor óptimo del factor de calibración `k`, ajustando las predicciones del modelo a las valoraciones reales de los usuarios.

## Resultados Destacados
Según el análisis detallado en el informe:
* **Percepción del Tiempo:** La satisfacción no depende linealmente del tiempo de espera; factores como el tipo de atracción y las expectativas previas juegan un papel crucial.
* **Gestión de Expectativas:** Se demostró que mejorar la información en colas largas de atracciones infantiles puede tener un impacto positivo en el rating final.
* **Ajuste del Modelo:** La introducción del factor `k` permitió reducir el error entre la satisfacción simulada y la real.

## Instalación y Uso
1.  Clona el repositorio:
    ```bash
    git clone [https://github.com/tu-usuario/Disneyland-Queue-Simulation-SimPy.git](https://github.com/tu-usuario/Disneyland-Queue-Simulation-SimPy.git)
    ```
2.  Instala las dependencias:
    ```bash
    pip install simpy pandas numpy matplotlib seaborn
    ```
3.  Ejecuta los notebooks en orden (empezando por la simulación de tiempos de espera) para reproducir los experimentos.

## Autores
Trabajo realizado por:
* Nerea de la Torre
* Nora Alquézar
* Adrián Prego
* Laia Sjöberg

Matemática Computacional y Análisis de Datos, UAB

