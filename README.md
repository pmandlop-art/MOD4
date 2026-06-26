<img width="300" height="150" alt="mermaid-diagram-2026-06-26-101846" src="https://github.com/user-attachments/assets/2b784fb1-0e4f-425b-a2fc-f0de602a34d0" /> 
FinAdvise - AI Personal Finance Assistant 💸💸

**FinAdvise** es un asistente financiero inteligente y agéntico desarrollado en Python que simplifica la gestión del dinero y la consulta de mercados en tiempo real. 

A diferencia de los chatbots convencionales lineales, este sistema utiliza arquitecturas de IA avanzadas basadas en grafos de conocimiento y flujos de trabajo asíncronos para ofrecer respuestas dinámicas y adaptativas según el perfil del usuario.

<img width="1338" height="984" alt="image" src="https://github.com/user-attachments/assets/8edd93a2-ab51-4791-a68c-3cb11e3b3bbc" />


https://github.com/user-attachments/assets/85776457-8eb9-45bf-b3f9-089ab28a3397

---

## 🚀 Características Clave (Tech Stack & Capabilities)

*   **Orquestación de Agentes Inteligentes:** Desarrollado con **LangGraph** utilizando `StateGraph` para la gestión avanzada del estado de la conversación, memoria a corto/largo plazo y enrutamiento condicional basado en intenciones.
*   **Detección de Intenciones (Intent Detection):** Clasificación automática de consultas mediante **Groq API** empleando modelos de última generación (`llama-3.3-70b-versatile`).
*   **Integración de Datos Financieros:** Conexión en tiempo real con los mercados de valores mediante la API de **Alpha Vantage** con manejo robusto de errores y extracción de símbolos.
*   **Human-in-the-Loop (HITL):** Mecanismo de seguridad que detecta y mitiga de forma simulada consultas de alto riesgo financiero (ej. *"¿Debo liquidar mi cuenta de retiro?"*).
*   **Interfaz de Usuario Interactiva:** Panel conversacional limpio, amigable y responsivo diseñado con **Streamlit**.

---

## 🛠️ Requisitos Previos

*   **Python:** Versión 3.8 o superior.
*   **API Keys Necesarias:**
    *   Groq API Key (Procesamiento del lenguaje natural).
    *   Alpha Vantage API Key (Datos bursátiles).

---

## 📦 Instrucciones de Instalación y Uso

Sigue estos pasos en tu terminal para clonar y ejecutar el asistente localmente:

### 1. Clonar el proyecto y acceder a la carpeta
```bash
git clone <tu-repository-url>
cd finadvise
2. Crear y activar el entorno virtual (env4)
En Windows:

Bash
python -m venv env4
env4\Scripts\activate
En macOS/Linux:

Bash
python3 -m venv env4
source env4/bin/activate
3. Instalar las dependencias del sistema
Bash
pip install -r requirements.txt
4. Configurar las Variables de Entorno
Crea un archivo .gitignore para omitir el entorno y tus llaves, y genera un archivo .env en la raíz del proyecto agregando tus credenciales de la siguiente forma:

Plaintext
GROQ_API_KEY=tu_api_key_aquí
ALPHA_VANTAGE_API_KEY=tu_api_key_aquí
5. Lanzar la aplicación
Bash
streamlit run app.py
El panel se abrirá automáticamente en tu navegador web en la dirección http://localhost:8501.

📈 Casos de Uso (Ejemplos en el Chat)
Puedes interactuar con el bot realizando consultas simuladas como:

Actualizar Perfil: "Tengo 30 años y gano $50,000 al año, mi meta es ahorrar para un coche."

Consulta de Acciones: "¿Cuál es el precio actual de las acciones de AAPL?"

Gestión de Gastos: "Añade un gasto de $50 en supermercado."

📂 Estructura del Repositorio
Plaintext
finadvise/
├── env4/                       # Entorno virtual de Python (Excluido de Git)
├── .env                        # Variables de entorno secretas (Excluido de Git)
├── .gitignore                  # Filtro de protección de archivos privados
├── app.py                      # Código fuente principal de la aplicación Streamlit
├── requirements.txt            # Dependencias del proyecto
└── README.md                   # Presentación del portafolio profesional
💡 Nota de Desarrollo: Este proyecto fue construido con fines prácticos para demostrar la viabilidad de sistemas multi-agente en entornos de finanzas personales. La capa gratuita de Alpha Vantage cuenta con un límite estándar de 5 llamadas por minuto.
