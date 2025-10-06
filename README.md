# ChatBot

Este repositorio contiene un proyecto de chatbot basado en Gradio y Python. El chatbot utiliza múltiples modelos de lenguaje y proveedores para generar respuestas a las consultas del usuario, incluyendo traducción, resúmenes y generación de imágenes.

## Características

- **Múltiples proveedores**: OpenAI, Hugging Face, Local (Stable Diffusion), Ollama
- **Múltiples tareas**: Traducción, resúmenes, generación de imágenes
- **Procesamiento local**: Soporte para modelos locales con Ollama y Stable Diffusion
- **Interfaz intuitiva**: Interfaz web con Gradio
- **Métricas de uso**: Sistema de seguimiento de rendimiento
- **Soporte multimodal**: Carga de archivos PDF, DOCX y TXT

## Requisitos Previos

Antes de comenzar, asegúrate de tener instalados los siguientes requisitos:

1. **Python**: Asegúrate de tener Python 3.8 o superior instalado en tu sistema. Puedes verificar tu versión de Python ejecutando:
   ```bash
   python --version
   ```
2. **Pip**: El gestor de paquetes de Python debe estar instalado. Generalmente viene incluido con Python.

## Instalación

Sigue estos pasos para configurar el entorno y ejecutar el proyecto:

1. **Clona el repositorio**:
   ```bash
   git clone https://github.com/Viraviutt/ChatBot.git
   cd ChatBot
   ```

2. **Crea un entorno virtual** (opcional pero recomendado):
   ```bash
   python -m venv venv
   ```
   Activa el entorno virtual:
   - En Windows:
     ```bash
     .\venv\Scripts\activate
     ```
   - En macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

3. **Instala las dependencias**:
   Ejecuta el siguiente comando para instalar las bibliotecas necesarias:
   ```bash
   pip install -r requirements.txt
   ```

   Las dependencias principales incluyen:
   - `gradio` - Interfaz web
   - `openai` - API de OpenAI y compatibles
   - `transformers` - Modelos de Hugging Face
   - `torch` - PyTorch para modelos locales
   - `requests` - Comunicación con Ollama
   - `PyMuPDF`, `docx2txt` - Procesamiento de documentos

4. **Configura las API Keys** (opcional):
   Crea un archivo `.env` en la raíz del proyecto con tus claves de API:
   ```
   OPEN_ROUTER_API_KEY=tu_clave_aqui
   GEMINI_API_KEY=tu_clave_aqui
   GROQ_API_KEY=tu_clave_aqui
   HF_TOKEN=tu_token_aqui
   ```

4. **Verifica la instalación**:
   Asegúrate de que las dependencias se hayan instalado correctamente ejecutando:
   ```bash
   pip list
   ```

## Configuración de Ollama (Opcional)

Ollama permite ejecutar modelos de lenguaje grandes localmente para mayor privacidad y sin límites de API.

### Instalación de Ollama

1. **Instalar Ollama**:
   - **Windows**: Descarga desde https://ollama.ai
   - **Linux/Mac**: 
     ```bash
     curl -fsSL https://ollama.ai/install.sh | sh
     ```

2. **Descargar modelos recomendados**:
   ```bash
   ollama pull llama3.1:8b   
   ollama pull mistral:7b    
   ```

3. **Modelos adicionales opcionales**:
   ```bash
   ollama pull qwen2:7b       
   ollama pull codellama:7b   
   ollama pull phi3:mini      
   ```

4. **Iniciar Ollama**:
   ```bash
   ollama serve
   ```

5. **Verificar instalación**:
   ```bash
   ollama list
   ```


## Ejecución

1. **Ejecuta el notebook**:
   Abre el archivo `ChatBot.ipynb` en Jupyter Notebook o VS Code y ejecuta las celdas en orden.

2. **Ejecuta el script (opcional)**:
   Si tienes un script Python para ejecutar el chatbot, como `chat_funct.py`, puedes ejecutarlo directamente:
   ```bash
   python chat_funct.py
   ```

3. **Interfaz Gradio**:
   Una vez que el chatbot esté en ejecución, se abrirá una interfaz de usuario basada en Gradio en tu navegador. Desde allí, puedes interactuar con el chatbot.

## Estructura del Proyecto

- `ChatBot.ipynb`: Notebook principal que contiene la lógica del chatbot
- `requirements.txt`: Lista de dependencias del proyecto
- `README.md`: Este archivo de documentación
- `images/`: Carpeta donde se guardan las imágenes generadas
- `.env`: Archivo de configuración de API keys (crear manualmente)

## Proveedores y Modelos Disponibles

### OpenAI-Compatible
- **Gemini** (Google): Traducción y conversación general
- **Groq**: Procesamiento rápido para resúmenes
- **OpenRouter**: Acceso a múltiples modelos

### Hugging Face
- **Helsinki-NLP**: Traducción inglés → español
- **Stability AI**: Generación de imágenes con SDXL

### Local
- **RunwayML**: Stable Diffusion local para imágenes
- **Ollama**: Modelos de lenguaje ejecutados localmente

### Tareas Disponibles
1. **Traducción**: Traducir texto entre idiomas
2. **Resúmenes**: Resumir documentos y texto largo
3. **Imágenes**: Generar imágenes desde descripciones de texto

## Notas

- **API Keys**: Las claves de API son opcionales. Sin ellas, solo funcionarán los modelos locales (Ollama, RunwayML)
- **Ollama**: Debe estar ejecutándose como servicio (`ollama serve`) para funcionar
- **GPU**: Se recomienda GPU para mejor rendimiento con modelos locales
- **Archivos**: Soporta carga de PDF, DOCX y TXT para procesamiento
- **Métricas**: El sistema incluye métricas de uso y rendimiento en tiempo real

## Solución de Problemas

### Problemas comunes:

1. **Ollama no se conecta**:
   ```bash
   # Verificar que Ollama esté corriendo
   ollama serve
   # En otra terminal
   ollama list
   ```

2. **Error de GPU con PyTorch**:
   ```bash
   # Reinstalar PyTorch con soporte CUDA
   pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
   ```

3. **Errores de API**:
   - Verificar que las API keys estén configuradas correctamente
   - Comprobar límites de uso de las APIs

4. **Problemas de memoria**:
   - Usar modelos más pequeños (phi3:mini para Ollama)
   - Cerrar otras aplicaciones que consuman GPU/RAM

## Contribuciones

Las contribuciones son bienvenidas. Si deseas contribuir, por favor abre un issue o envía un pull request.

## Licencia

Este proyecto está bajo la licencia [MIT](LICENSE).