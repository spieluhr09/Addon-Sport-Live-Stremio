Aviso legal: Este complemento es un proyecto de prueba y su creador no se responsabiliza de su uso. El usuario es el único responsable del contenido al que acceda y del cumplimiento de las leyes de derechos de autor.



---

## Videotutorial de instalación e instalador sencillo

¿Tienes problemas para instalar este complemento? He creado un videotutorial paso a paso y un instalador (archivo .bat) para simplificar el proceso.






https://github.com/user-attachments/assets/4013acab-c5c4-4bba-9403-7419817a5da2




Para una instalación más sencilla, puedes usar el archivo **INSTALLER.bat** disponible en la [sección de lanzamientos](https://github.com/WebStaticCS/Addon-Sport-Live-Stremio/releases/tag/v1.0).

---

# Sports Live Stremio Addon

Este complemento de Stremio te permite ver eventos deportivos en vivo, próximos y finalizados, obteniendo información de una fuente JSON y proporcionando transmisiones de varios proveedores.

### Requirements

-   Node.js (v14+ recommended)

-   npm (included with Node.js)

### Installation

1.  **Clone:**

    ```
    git clone [https://github.com/WebStaticCS/Addon-Sport-Live-Stremio](https://github.com/WebStaticCS/Addon-Sport-Live-Stremio)
    cd Addon-Sport-Live-Stremio
    ```

2.  **Install dependencies:**

    ```
    npm install
    ```

### Configuration (config.js)

Abra config.js y ajuste estas variables. Puede usar variables de entorno para producción.

-   ADDON_PORT: Puerto donde se ejecutará el complemento (default: 7000).

-   IMAGE_GENERATOR_BASE_URL: URL de su servidor de generación de imágenes. Necesario para carteles dinámicos. Implementar desde:
    [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https%3A%2F%2Fgithub.com%2FWebStaticCS%2FImage-Generator.git&project-name=image-generator&repo-name=Image-Generator)

    Utilice la URL de implementación de Vercel (e.g., https://your-generator.vercel.app/api/generate-image).

-   TIMEZONE_OFFSET_HOURS: Desplazamiento UTC para mostrar las horas de los eventos (valor predeterminado: -5).
-   Note: Puede agregar más imágenes de eventos a poster_data.js si es necesario

### Running the Addon

1.  **Start:**

    ```
    node app.js
    ```

2.  La consola mostrará la URL de instalación (p. ej., http://127.0.0.1:7000/manifest.json). Péguela en Stremio > Complementos > Instalar complemento.

### Important Notes

-   Streams: Los problemas de reproducción generalmente se deben a CORS.

-   Cache: Si no aparecen los cambios, borre el caché del complemento en Stremio o reinstale el complemento.

-   Environment Variables: Para la implementación de producción (por ejemplo, Vercel), utilice variables de entorno para las configuraciones.
