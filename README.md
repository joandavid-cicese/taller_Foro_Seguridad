# 🤖 Prácticas de Ciberseguridad con Inteligencia Artificial y Machine Learning

¡Bienvenido/a! Este repositorio contiene los materiales prácticos y cuadernos de código desarrollados para el taller **"Ciberseguridad Inteligente: Machine Learning para detectar Phishing, Spam y Ataques de Ingeniería Social"**, presentado en el **10º Foro de Seguridad de la Información del CICESE**.

El objetivo de estas prácticas es proporcionar una introducción práctica y aplicada sobre cómo las técnicas de Machine Learning (supervisado y no supervisado) y la Inteligencia Artificial Generativa (con la API de Gemini) pueden ser utilizadas para detectar y analizar ciberamenazas modernas.

---

## 📚 Contenido del Repositorio

Este repositorio se divide en tres prácticas principales, cada una abordando un aspecto diferente de la ciberseguridad inteligente.

###  práctica-01-aprendizaje-supervisado/
**🎯 Objetivo:** Construir un detector de URLs de phishing desde cero utilizando un modelo de clasificación supervisado.

Este notebook cubre un flujo de trabajo completo de Machine Learning, incluyendo:
* **Ingeniería de Características (Feature Engineering):** Extracción de atributos relevantes de las URLs (longitud, presencia de símbolos, número de subdominios, etc.).
* **Entrenamiento del Modelo:** Uso de `RandomForestClassifier` para clasificar URLs como 'legítimas' o 'phishing'.
* **Evaluación de Métricas:** Análisis detallado del rendimiento del modelo con métricas clave en ciberseguridad: Precisión, Recall, F1-Score y Matriz de Confusión.
* **Optimización de Hiperparámetros:** Búsqueda del mejor modelo utilizando `GridSearchCV` para mejorar el rendimiento.
* **Inferencia:** Uso del modelo entrenado para predecir nuevas URLs.

### práctica-02-aprendizaje-no-supervisado/
**🎯 Objetivo:** Detectar anomalías en el tráfico de red utilizando algoritmos de aprendizaje no supervisado.

Esta práctica se enfoca en un escenario donde no tenemos etiquetas claras y buscamos comportamientos atípicos:
* **Preprocesamiento de Datos:** Preparación del dataset NSL-KDD, incluyendo escalado y codificación One-Hot.
* **Modelado y Comparación:** Implementación y análisis de dos algoritmos populares: **K-Means** e **Isolation Forest**.
* **Análisis Crítico:** Se demuestra un caso realista donde la configuración inicial de los modelos no es óptima y se guía al usuario en el proceso de **ajuste fino (fine-tuning)** para mejorar drásticamente la capacidad de detección.

### práctica-03-ia-generativa-gemini-api/
**🎯 Objetivo:** Utilizar modelos de lenguaje avanzados (LLMs) como Gemini para tareas ofensivas y defensivas en ciberseguridad.

Este cuaderno explora el uso práctico de la API de Gemini de Google AI Studio para:
* **Generación de Phishing Polimórfico:** Creación de correos de phishing convincentes y variados ajustando parámetros como la `temperatura`.
* **Análisis de Amenazas:** Uso de Gemini como un analista de seguridad para detectar "banderas rojas" en textos y correos sospechosos.
* **Análisis Multimodal (Gemini Vision):** Detección de enlaces maliciosos y señales de phishing directamente desde **imágenes de códigos QR** y **capturas de pantalla**.
* **Integración con APIs Externas:** Conexión con la API de **VirusTotal** para un análisis de reputación de URLs en tiempo real.
* **Seguridad de la IA:** Se discuten conceptos como el **jailbreaking** y se realiza una auditoría de costos para concienciar sobre la importancia de proteger las API Keys.

---

## 🛠️ Tecnologías y Librerías Utilizadas

* **Lenguaje:** Python 3
* **Machine Learning:** Scikit-learn
* **Manipulación de Datos:** Pandas, NumPy
* **Visualización:** Matplotlib, Seaborn
* **IA Generativa:** Google Generative AI (Gemini API)
* **Frameworks Adicionales:** LangChain (conceptualizado)
* **Otros:** Joblib, Requests, KaggleHub

---

## 🚀 Cómo Empezar

Sigue estos pasos para configurar el entorno y ejecutar las prácticas.

### Prerrequisitos

* Tener una cuenta de Google para acceder a Google Colab y Google AI Studio.
* Conocimientos básicos de Python.

### Instalación y Configuración

1.  **Clona el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/tu-repositorio.git](https://github.com/tu-usuario/tu-repositorio.git)
    cd tu-repositorio
    ```

2.  **Crea un archivo `.env`:**
    Para la Práctica 3, necesitarás claves de API. Crea un archivo llamado `.env` en la raíz del proyecto y añade tus claves. **Nunca subas este archivo a GitHub.**

    **`.env.example`:**
    ```
    MY_API_KEY="AIzaSy... (tu clave de Gemini API)"
    VIRUS_TOTAL_KEY="abcdef... (tu clave de VirusTotal)"
    ```

3.  **Instala las dependencias:**
    Se recomienda crear un entorno virtual. Luego, instala las librerías necesarias:
    ```bash
    pip install -r requirements.txt
    ```

    **`requirements.txt`:**
    ```
    google-generativeai
    scikit-learn
    pandas
    numpy
    matplotlib
    seaborn
    joblib
    requests
    kagglehub
    python-dotenv
    ```

### Ejecución de las Prácticas

La forma más sencilla de ejecutar los cuadernos es subiéndolos a **Google Colab**. Esto asegura un entorno consistente y acceso a GPUs si es necesario.

1.  Abre [Google Colab](https://colab.research.google.com/).
2.  Sube cada archivo `.ipynb`.
3.  Para la Práctica 3, configura tus API Keys usando la función de "Secrets" (secreto) de Colab, como se indica en el cuaderno.

---

## 👤 Autor

* **M. en C. Joan David González Franco**
* [cite_start]**LinkedIn:** [https://www.linkedin.com/in/joandgonzalezf/](https://www.linkedin.com/in/joandgonzalezf/)
* [cite_start]**Correo:** [joandavid@cicese.edu.mx](mailto:joandavid@cicese.edu.mx)

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.
