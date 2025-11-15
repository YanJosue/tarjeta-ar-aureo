# Tarjetas en RA

Descripción
- Proyecto que muestra una presentación de tarjetas en Realidad Aumentada (RA) para visualizar contenido enriquecido sobre tarjetas físicas o marcadores.
- Objetivo: ofrecer una experiencia interactiva y accesible desde navegador móvil compatible con WebAR.

Características principales
- Visualización de tarjetas en RA sobre marcadores o sin marcadores (markerless).
- Soporte para texto, imágenes y modelos 3D por tarjeta.
- Interacción básica: girar, ampliar, reproducir contenido multimedia.
- Compatible con A-Frame / AR.js / WebXR (según la configuración).

Requisitos
- Navegador con soporte WebXR o WebAR (Chrome/Firefox en Android, Safari en iOS con WebAR polyfills).
- Conexión local o servidor estático para servir archivos (no funciona desde file://).

Instalación rápida
1. Clonar o copiar el repositorio al equipo.
2. Instalar servidor estático opcional:
    - npm install -g serve
3. Levantar servidor en la carpeta del proyecto:
    - serve . -p 8080
4. Abrir en el dispositivo móvil o emulador: http://<tu-ip>:8080

Estructura sugerida
- index.html — entrypoint con la escena RA.
- assets/
  - images/ — imágenes de las tarjetas.
  - models/ — modelos 3D (glTF/GLB).
  - markers/ — patrones de marcador (si aplica).
- src/
  - main.js — lógica de interacción y carga de contenido.
  - styles.css — estilos de la presentación.
- README.md — esta documentación.

Cómo usar
- Preparar las tarjetas físicas (imprimir marcadores) o usar la opción markerless.
- Acceder a la URL desde el dispositivo y permitir cámara.
- Apuntar al marcador o al plano detectado para que aparezca la tarjeta RA.
- Interactuar con el contenido táctilmente (gestos de giro/zoom o botones en la UI).

Personalización rápida
- Añadir nuevas tarjetas: colocar recursos en assets/ y registrar la tarjeta en main.js o JSON de configuración.
- Cambiar modelos: reemplazar archivos en models/ y actualizar rutas.
- Ajustes de rendimiento: reducir tamaño de texturas y complejidad de modelos 3D.

Buenas prácticas
- Optimizar modelos y texturas para móviles.
- Probar en múltiples dispositivos y condiciones de luz.
- Proveer instrucciones impresas junto a las tarjetas para usuarios finales.

Licencia y contacto
- Incluir licencia en LICENSE (recomendado MIT).
- Contacto: añadir correo o enlace al repositorio/autor en el archivo.

Notas finales
- Esta presentación está pensada como base para demos de RA con tarjetas; adaptar stacks (AR.js, A-Frame, Three.js o WebXR) según necesidades técnicas y compatibilidad.
- Probar siempre desde servidor y con permisos de cámara habilitados.