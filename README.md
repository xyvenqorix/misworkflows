🎨 misworkflows — SVG automáticos

Repositorio de workflows de GitHub Actions para generar y guardar archivos SVG animados automáticamente.

✨ ¿Qué puedes obtener?

Este proyecto incluye dos diseños SVG:

- Carita simple: una carita animada con ojos, brillos, cachetes y boca.
- XYVENQORIX artwork: un diseño pixel art con el nombre XYVENQORIX, partículas y efectos de brillo.

Los archivos SVG se generan mediante GitHub Actions y se guardan automáticamente en la carpeta "assets/" del repositorio.

📁 Archivos generados

misworkflows/
├── .github/
│   └── workflows/
│       ├── carita.yml
│       └── xyvenqorix.yml
└── assets/
    ├── carita.svg
    └── xyvenqorix.svg

⚙️ ¿Cómo obtener los SVG?

1. Entra al repositorio: "misworkflows" (https://github.com/xyvenqorix/misworkflows)
2. Abre la pestaña Actions.
3. Selecciona el workflow que quieras ejecutar.
4. Pulsa Run workflow y confirma la ejecución.
5. Cuando termine correctamente, entra en la carpeta "assets/".
6. Abre el archivo ".svg" generado para visualizarlo, copiar su código o utilizarlo en tu página web.

También puedes descargar el SVG desde GitHub y utilizarlo en tus proyectos.

🔐 Configurar permisos de GitHub Actions

Para que los workflows puedan crear o actualizar archivos SVG dentro del repositorio, debes configurar los permisos de escritura.

Paso 1: Entrar en Settings

En tu repositorio, abre:

Settings → Actions → General

Paso 2: Configurar Workflow permissions

Busca la sección Workflow permissions y selecciona:

«Read and write permissions»

Esto permite que el workflow pueda leer y modificar archivos del repositorio mediante "GITHUB_TOKEN".

Si aparece la opción:

«Allow GitHub Actions to create and approve pull requests»

No es necesaria para estos workflows, porque los SVG se guardan directamente en la rama "main" mediante la API de GitHub.

Pulsa Save si aparece el botón.

Paso 3: Permiso en el workflow

Los archivos YAML deben incluir:

permissions:
  contents: write

Este permiso autoriza al workflow a crear o actualizar los archivos SVG en la carpeta "assets/".

🚀 Ejecución automática

Los workflows se ejecutan cuando haces un "push" a la rama "main", excepto cuando el cambio solamente afecta al SVG que genera el propio workflow.

También puedes ejecutarlos manualmente con "workflow_dispatch".

Esto evita que la actualización del SVG provoque una ejecución repetitiva del mismo workflow.

🖥️ Visualizar y copiar el SVG

Puedes abrir los archivos SVG directamente en el navegador para ver sus animaciones.

Para copiar el código completo, abre el archivo en GitHub y utiliza la opción de copiar el contenido del archivo. También puedes incorporar un botón tipo pantallita en una página web para mostrar el SVG y copiar su código.

📌 Repositorio

"https://github.com/xyvenqorix/misworkflows" (https://github.com/xyvenqorix/misworkflows)

---

Creado por XYVENQORIX.
