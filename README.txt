COMPARADOR DE PRECIOS — PWA OFFLINE
====================================

Qué incluye
- Comparación de 2, 3 o 4 productos.
- Unidades: g, kg, ml, L y piezas.
- Precio unitario y ranking automático.
- Guarda el formulario y un historial local (hasta 30 comparaciones).
- Service worker que almacena los archivos para funcionar sin internet.
- No usa servicios externos, analítica ni cuentas.

IMPORTANTE
Para instalar una PWA en Android y usarla offline, el sitio debe abrirse por HTTPS (o localhost).
Abrir index.html directamente como archivo no activa el service worker ni la instalación PWA.
Después de publicar y abrir la página con internet, espera a que cargue por completo; vuelve a abrirla una vez si hace falta. Luego usa Chrome > menú ⋮ > "Instalar app" o "Añadir a pantalla de inicio". Abre la app una vez y comprueba el modo avión.

PUBLICAR GRATIS CON GITHUB PAGES
1. Entra en https://github.com y crea una cuenta gratis si no tienes.
2. Crea un repositorio nuevo. Ponle, por ejemplo, comparador-precios.
3. Si te ofrece visibilidad, selecciona Public (necesario para GitHub Pages en el plan gratuito).
4. Sube TODOS los archivos y carpetas de este ZIP a la raíz del repositorio. Debe quedar index.html en la raíz, junto a app.js, styles.css, manifest.json y sw.js; también la carpeta icons.
   En GitHub: Add file > Upload files > arrastra los archivos extraídos y pulsa Commit changes.
5. En el repositorio abre Settings > Pages.
6. En "Build and deployment", selecciona "Deploy from a branch". Elige la rama main y la carpeta /(root), y guarda.
7. Espera a que GitHub Pages publique el sitio. La dirección será parecida a:
   https://TU-USUARIO.github.io/comparador-precios/
   (usa la URL exacta que muestre GitHub; no copies literalmente TU-USUARIO).
8. Abre esa URL en Chrome en tu Android con internet. Espera a que cargue.
9. En Chrome pulsa ⋮ > "Instalar app" o "Añadir a pantalla de inicio". Si aparece el botón "Instalar app" dentro de la página, también puedes usarlo.
10. Abre la app instalada mientras tienes internet y espera unos segundos. Después activa modo avión y prueba comparar productos.
11. Si no funciona offline, desactiva modo avión, vuelve a abrir la URL con Chrome, espera unos segundos y prueba otra vez. El service worker debe completar el almacenamiento inicial.

USO
- Selecciona 2, 3 o 4 productos.
- Elige una unidad común a todos.
- Introduce nombre, cantidad y precio. Acepta decimales usando punto o coma.
- El precio unitario y el ganador se actualizan automáticamente.
- "Guardar comparación actual" guarda la comparación en el almacenamiento local del navegador.
- "Cargar" restaura una comparación guardada.
- "Limpiar" borra los campos actuales, no el historial.
- "Borrar" en Historial elimina el historial.

PRIVACIDAD Y LIMITACIONES
- Los cálculos y el historial se guardan en el almacenamiento local del navegador de este dispositivo.
- No hay sincronización entre dispositivos. Si borras los datos del sitio/navegador, podrías perder el historial.
- Si publicas en un repositorio público, el código de la app será público; no incluye información personal.
- Para actualizar la app en el futuro, reemplaza los archivos del repositorio y sube la versión de CACHE_NAME en sw.js (por ejemplo, v2) para forzar una caché nueva.
