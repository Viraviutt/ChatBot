# ChatBot

Este repositorio contiene un proyecto de chatbot basado en Gradio y Python. El chatbot utiliza modelos de lenguaje para generar respuestas a las consultas del usuario. Este proyecto está diseñado para ser fácil de configurar y ejecutar.

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

   Si no tienes un archivo `requirements.txt`, asegúrate de incluir las siguientes dependencias:
   - `gradio`
   - Cualquier otra biblioteca utilizada en el proyecto.

   Para generar un archivo `requirements.txt`, puedes usar:
   ```bash
   pip freeze > requirements.txt
   ```

4. **Verifica la instalación**:
   Asegúrate de que las dependencias se hayan instalado correctamente ejecutando:
   ```bash
   pip list
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

- `ChatBot.ipynb`: Notebook principal que contiene la lógica del chatbot.
- `chat_funct.py`: Archivo Python con funciones auxiliares.
- `gradio_local.py`: Archivo local que no debe interferir con la biblioteca oficial de Gradio.
- `README.md`: Este archivo.
- `__pycache__/`: Carpeta generada automáticamente para almacenar archivos compilados.

## Notas

- Si encuentras errores relacionados con la biblioteca `gradio`, asegúrate de que no haya un archivo local llamado `gradio.py` que pueda estar interfiriendo con la biblioteca oficial.
- Reinicia el kernel de Jupyter Notebook después de realizar cambios en el código para evitar conflictos.

## Contribuciones

Las contribuciones son bienvenidas. Si deseas contribuir, por favor abre un issue o envía un pull request.

## Licencia

Este proyecto está bajo la licencia [MIT](LICENSE).