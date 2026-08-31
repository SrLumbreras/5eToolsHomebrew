# 5eToolsHomebrew
Storage for homebrew entries on 5e tools

Homebrew Repository URL:
https://raw.githubusercontent.com/SrLumbreras/5eToolsHomebrew/main/

Main 5e.tools Repository URL:
https://github.com/5etools-mirror-3/5etools-src/tree/main/data

## Estructura del repositorio

Ramas:
- **main**: rama única con todo el contenido consolidado. Es la que se apunta desde 5e.tools (Homebrew > Custom URL) para cargar el contenido.
- **wip**: rama de trabajo para nuevas fichas/monstruos/notas antes de pasarlos a `main`. Se mergea a `main` cuando el contenido está listo.

Carpetas relevantes en `main`:
- `creature/`: contenido de campaña terminado (monstruos, PNJs, objetos base...), en formato homebrew válido para 5e.tools. Sigue el convenio del repo oficial de homebrew (`TheGiddyLimit/homebrew`): un fichero por fuente, nombrado `Autor; Descripción.json`, ubicado en la carpeta del tipo de contenido principal — el fichero puede incluir varios props (`monster`, `baseitem`, etc.) a la vez.
- `WIP/`: fichas y aventuras en borrador, todavía no listas para pulir del todo (pueden no pasar la validación de esquema). Puede no existir si no hay borradores activos: git no versiona carpetas vacías.
- `_notes/`: notas de partida (incluye `Jarlmoot/` con las mazmorras de cada runa).
- `_img/`: imágenes vinculadas a fuentes (`sources`) declaradas en el contenido homebrew — esta carpeta la valida el propio tooling de 5e.tools.
- `_homebrew_images/`: retratos y assets de PNJ usados en documentos de Homebrewery. No son contenido homebrew cargable por 5e.tools, así que viven fuera de `_img/` para no romper esa validación.
- `_node/` y `_test/`: scripts de utilidad (`5etools-utils`) para generar índices y validar el contenido (`npm test`).

Antiguo contenido de la rama `main` original (screens del DM, fichas antiguas de Adan/Eva en `Sources/`, notas sueltas en `notasRol`) quedó descartado porque ya estaba superado por las fichas actuales en `WIP/`; solo se rescataron los retratos de PNJ.
