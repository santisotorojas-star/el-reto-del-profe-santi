# El Profe Santi te reta - proyecto Android

Este proyecto envuelve el juego (carpeta `www`) en una app de Android con Capacitor.
NO incluye el APK ya compilado: hay que construirlo con uno de estos dos caminos.

## Camino A: con Android Studio (en tu computador)
1. Instala Node.js (versión 18 o superior) y Android Studio.
2. En una terminal, dentro de esta carpeta:
   - `npm install`
   - `npx cap add android`
   - `npx @capacitor/assets generate --android`   (pone el icono; es opcional)
   - `npx cap sync android`
   - `npx cap open android`
3. En Android Studio, espera a que termine de sincronizar y ve a
   **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. Al terminar, pulsa «locate» para ver el archivo `app-debug.apk`.

## Camino B: sin instalar nada, con GitHub
1. Crea una cuenta gratis en github.com y un repositorio nuevo.
2. Sube todo el contenido de esta carpeta (incluida la carpeta oculta `.github`).
3. Ve a la pestaña **Actions**, elige **Construir APK** y pulsa **Run workflow**.
4. Cuando termine (unos minutos), abre la ejecución y descarga `profe-santi-te-reta-apk`
   (dentro está `app-debug.apk`).

## Instalar el APK en el celular
Pasa el archivo al celular, ábrelo y, si Android lo pide, permite
«instalar apps de origen desconocido» para esa aplicación.

## Para Google Play
Este APK es de prueba (debug). Para publicar en Google Play hace falta un archivo AAB
firmado (en Android Studio: Build > Generate Signed Bundle) y una cuenta de desarrollador.

## Cambiar el juego
Edita `www/index.html` (las preguntas están en la lista `Q` al inicio del script)
y vuelve a construir el APK.
