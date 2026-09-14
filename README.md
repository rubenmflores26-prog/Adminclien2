# AdminClientes V2 — Supabase + GitHub Pages

Esta versión conserva la interfaz de AdminClientes y la conecta a Supabase para autenticación, clientes, pagos y fotografías privadas.

## Configuración ya incluida
- Project URL: `https://dwijfgznbzhuhrdrwdri.supabase.co`
- Publishable key de Supabase integrada en `index.html`.
- Bucket de fotos: `Fotos-clientes`.
- La aplicación NO usa secret key ni service_role.

## Base de datos requerida
Ya se creó en Supabase con el SQL indicado durante la configuración: `clientes`, `pagos` y políticas RLS.

## Publicar en GitHub Pages
1. Descomprime este ZIP.
2. Reemplaza en tu repositorio los archivos `index.html`, `manifest.json` y `sw.js`.
3. Haz Commit changes.
4. Espera a que GitHub Pages publique el cambio.
5. Abre tu aplicación y recarga.
6. Inicia sesión con el usuario creado en Supabase.

## Funciones V2
- Inicio de sesión con correo y contraseña.
- Clientes almacenados en Supabase.
- Pagos almacenados en Supabase.
- Fotos subidas al bucket privado.
- Selección desde Galería/Mis archivos y cámara.
- GPS y Google Maps.
- Historial de pagos.
- Exportación CSV.
- Sincronización manual desde Configuración.

## Seguridad
La aplicación usa la Publishable key, que está diseñada para aplicaciones cliente. La seguridad real se aplica mediante RLS y las políticas de Storage configuradas en Supabase. Nunca publiques una secret key o `service_role` en GitHub.

## Importante
Si cambias el nombre/ID del bucket de fotografías, debes cambiar `PHOTO_BUCKET` en `index.html` y las políticas de Storage para que coincidan.
