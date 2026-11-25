# Casa Artazu · visor 3D

Visor web del modelo 3D de la casa de C/ Mayor 18–20 (Artazu, Navarra), propuesta C.

Es una sola página (`index.html`) con el modelo incluido dentro: no necesita servidor ni compilación. Las librerías (three.js y SheetJS) se cargan desde CDN, así que hace falta conexión a internet para abrirlo.

## Publicarlo con GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `artazu-visor`).
2. Sube el contenido de esta carpeta (`index.html`, `README.md` y `.nojekyll`) a la rama `main`.
   - Desde la web: *Add file → Upload files* y arrastra los archivos.
   - Desde la terminal:
     ```bash
     git init
     git add .
     git commit -m "Visor 3D casa Artazu"
     git branch -M main
     git remote add origin https://github.com/TU_USUARIO/artazu-visor.git
     git push -u origin main
     ```
3. En el repositorio: *Settings → Pages → Build and deployment → Source: Deploy from a branch*, rama `main`, carpeta `/ (root)`, *Save*.
4. Al cabo de un minuto el visor estará en `https://TU_USUARIO.github.io/artazu-visor/`.

> Ojo: con una cuenta gratuita, GitHub Pages solo publica repositorios **públicos**, y la página la puede ver cualquiera que tenga el enlace.

## Qué incluye

- Modelo completo: casas A, B y C, entorno del pueblo e instalaciones.
- Estilos de vista (línea, masa, material), axonometrías, alzados y planta.
- Explotado por plantas, secciones horizontales y verticales.
- Selector **Cubierta A**: *Dos aguas* (actual) o *Terraza* (opción 2: solo faldón norte y cubierta plana transitable al sur).
- Mediciones por capas, con exportación a Excel, y exportación de la vista a SVG y PNG.

Al abrirse arranca en estilo masa, axonometría SE, plantas explotadas 4,2 m y cubierta A a dos aguas.

## Diferencias con la versión de Claude

Fuera de claude.ai no existen la base de datos compartida ni la identificación de usuarios, así que:

- **Notas**: el botón *Nota +* y la lista de notas no aparecen.
- **Precios del presupuesto**: se pueden escribir, pero no se guardan; se pierden al recargar.
- **Descargas** (Excel, SVG, PNG): se descargan directamente con el navegador.

## Actualizar el modelo

Basta con sustituir `index.html` por la versión nueva y volver a hacer *commit* y *push*. GitHub Pages lo vuelve a publicar solo.

Modelo de origen: `casa_3d_2026-11-12b.3dm` (Rhino 8), con la opción de terraza de `casa_3d_2026-11-25_cubierta_A_opcion2.3dm`.
