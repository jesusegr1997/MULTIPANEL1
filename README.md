# MultiPanel 0.1 — prototipo Android

Proyecto Android nativo para Redmi 13C / HyperOS 2.0.

## Qué incluye
- Pestaña lateral superpuesta y discreta en el borde derecho.
- Panel estrecho con una sola columna vertical de iconos, sin nombres.
- Lista las aplicaciones instaladas que tienen una actividad de inicio.
- Al tocar un icono aparecen las acciones «Ventana flotante» y «Pantalla dividida».
- La pestaña se puede mover verticalmente manteniendo y arrastrando.

## Importante sobre multitarea
La interfaz y el listado son nativos. Android no ofrece una API pública universal para forzar ventanas flotantes. Los botones envían una solicitud mediante `ActivityOptions.setLaunchBounds` y `FLAG_ACTIVITY_LAUNCH_ADJACENT`; HyperOS puede ignorarla o limitarla según la app y la versión del sistema. Si no funciona, usa la opción de ventanas flotantes/pantalla dividida de HyperOS desde Recientes.

## Compilar APK con GitHub Actions
1. Sube el contenido de esta carpeta al repositorio `MultiPanel` en la rama `main`.
2. Abre **Actions** y selecciona **Build MultiPanel APK**.
3. Pulsa **Run workflow**.
4. Cuando termine correctamente, abre la ejecución y descarga **MultiPanel-debug-apk** en Artifacts.
5. Descomprime el ZIP y abre `app-debug.apk` en el Redmi 13C.

Requisitos de compilación: JDK 17, Gradle 8.9, Android Gradle Plugin 8.7.3.
