# Registro de móviles · El Pino Ltda.

Aplicación web (un solo archivo `index.html`) que reemplaza la base de Access
`NUEVO_REGISTRO_EL_PINO.accdb`. Permite crear, editar y eliminar móviles,
completar los datos del conductor y subir sus 9 documentos/fotos.

## Cómo publicarla en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `registro-el-pino`).
2. Sube **solo** `index.html`, `README.md` y `.gitignore`.
   **No subas** `respaldo_inicial_el_pino.json` ni el `.accdb`: contienen
   cédulas, licencias y fotos de los conductores.
3. En el repositorio: *Settings → Pages → Build and deployment →
   Source: Deploy from a branch*, rama `main`, carpeta `/ (root)`. Guarda.
4. En uno o dos minutos la app queda en
   `https://TU-USUARIO.github.io/registro-el-pino/`.

## Primer uso

1. Abre la página y pulsa **Importar respaldo**.
2. Elige `respaldo_inicial_el_pino.json` (lo tienes en tu computador, no en GitHub).
3. Listo: aparecen los 100 móviles con sus datos y fotos.

## Dónde quedan los datos

GitHub Pages solo entrega la página; **no guarda datos**. Los registros se
guardan en el navegador del computador donde se usa (IndexedDB). Por eso:

- Cada computador/navegador tiene su propia copia.
- Usa **Exportar → Respaldo completo (.json)** con frecuencia y guarda el
  archivo en un lugar seguro (pendrive, Drive privado).
- Para pasar los datos a otro equipo: exporta el respaldo e impórtalo allá.
- Borrar el historial/datos de navegación de ese sitio borra el registro.

## Funciones

- Buscar por móvil, nombre, RUT o teléfono; filtrar por con/sin conductor o
  documentos faltantes.
- Crear, editar (incluido cambiar el número de móvil) y eliminar registros.
- Subir, cambiar, ver, descargar y quitar fotos (botón o arrastrando).
  Las fotos se reducen a 1600 px para ahorrar espacio.
- Aviso si el dígito verificador del RUT no coincide.
- Exportar planilla CSV para Excel (sin fotos).
- `Ctrl + S` guarda los cambios.
