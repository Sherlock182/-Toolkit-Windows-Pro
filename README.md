✨ TOOLKIT WINDOWS PRO

Centro integral de mantenimiento y diagnóstico para Windows, empaquetado en una interfaz moderna con Python 3 y Tkinter.



Tabla de contenidos

Descripción

Características principales

Capturas de pantalla

Requisitos

Instalación (modo desarrollo)

Uso

Construir ejecutable .exe

Crear instalador setup.exe

Contribuir

Licencia

Autor

Descripción

Toolkit Windows Pro reúne en una sola ventana las utilidades más frecuentes de reparación, limpieza y diagnóstico de Windows. Cada función se ejecuta mediante scripts por lotes o PowerShell elevados automáticamente, eliminando la necesidad de recordar comandos o navegar entre menús del sistema.

Objetivo : facilitar el mantenimiento preventivo y correctivo a usuarios y técnicos, ahorrando tiempo y reduciendo errores.

Características principales

Categoría

Funciones incluidas

Integridad del sistema

CHKDSK, SFC, DISM, verificación de firmas digitales

Seguridad

Escaneo rápido/off‑line con Windows Defender, listado de amenazas detectadas

Limpieza y optimización

Eliminación de temporales (Temp y %TEMP%), limpieza de sistema, desactivación de servicios innecesarios, optimización de inicio

Información y diagnósticos

Eventos recientes, SMART del disco, información de red/IP, procesos activos, detalles de licencia Windows, systeminfo

UI moderna

Paleta Nord Theme, botones con hover, scrollbar personalizado, ventana fija (700×750 px)

Agregar o modificar herramientas es tan simple como editar el diccionario SCRIPTS en Toolkit_Windows_Pro.py.

Capturas de pantalla

Menú principal

Scroll con herramientas





Guarda las imágenes en la carpeta docs/ para que se muestren correctamente.

Requisitos

Windows 10 / 11 (x64)

Python 3.9 o superior (probado con 3.13.4)

No se requieren dependencias externas; todo el GUI es Tkinter estándar.

Instalación (modo desarrollo)

# 1. Clona el repositorio
$ git clone https://github.com/tu-usuario/toolkit-windows-pro.git
$ cd toolkit-windows-pro

# 2. (Opcional) Crea y activa un entorno virtual
$ python -m venv .venv
$ .venv\Scripts\activate    # PowerShell

# 3. Ejecuta la aplicación
$ python Toolkit_Windows_Pro.py

Uso

Ejecuta la aplicación.

Selecciona la herramienta deseada haciendo clic en el botón correspondiente.

Confirma el cuadro de diálogo UAC (ejecución como administrador).

Sigue las instrucciones que aparezcan en la consola.

Cada script se ejecuta en una ventana separada, de modo que puedes supervisar la salida y cerrar cuando haya finalizado.

Construir ejecutable .exe

Se utiliza PyInstaller para generar un único archivo portátil.

# Instala PyInstaller
$ pip install pyinstaller

# Empaqueta con icono personalizado
$ pyinstaller --onefile --icon=uno.ico Toolkit_Windows_Pro.py

# El ejecutable aparecerá en la carpeta dist/

Agregar/actualizar el icono después de compilar

Si necesitas cambiar el icono de un .exe ya generado, usa Resource Hacker:

Abre el .exe en Resource Hacker ➜ Action → Replace Icon…

Selecciona tu archivo .ico ➜ Replace ➜ Save.

Crear instalador setup.exe (opcional)

Puedes distribuir la aplicación en formato instalador usando Inno Setup:

Descarga e instala Inno Setup desde https://jrsoftware.org/isdl.php

Crea un script .iss apuntando al ejecutable generado en dist/.

Compila y obtén tu setup.exe listo para compartir.

Ejemplo de sección [Files]:

[Files]
Source: "dist\Toolkit_Windows_Pro.exe"; DestDir: "{app}"; Flags: ignoreversion

Contribuir

¡Las mejoras y pull requests son bienvenidas! Sigue estos pasos:

Abre un issue describiendo tu propuesta.

Crea una rama temática (git checkout -b feature/nueva-funcion).

Asegúrate de que el código pase flake8 / black (si se habilitan).

Haz commit siguiendo el formato Conventional Commits.

Envía tu PR 🎉.

Licencia

Distribuido bajo la licencia MIT. Consulta el archivo LICENSE para más detalles.

Autor

Nahun Montalvo R.Desarrollador y entusiasta de la automatización de sistemas Windows.LinkedIn • Facebook

Toolkit Windows Pro nace con el objetivo de simplificar el día a día de quienes mantienen equipos Windows. ¡Pruébalo y aporta tu herramienta favorita! ✨

