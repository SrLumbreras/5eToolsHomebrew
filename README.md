# 5eToolsHomebrew
Storage for homebrew entries on 5e tools

Homebrew Repository URL:
https://raw.githubusercontent.com/SrLumbreras/5eToolsHomebrew/main/

Main 5e.tools Repository URL:
https://github.com/5etools-mirror-3/5etools-src/tree/main/data

## Estructura del repositorio

Ramas:
- **main**: única rama permanente, con todo el contenido consolidado. Es la que se apunta desde 5e.tools (Homebrew > Custom URL) para cargar el contenido. Nunca se comitea directamente en ella.
- **Una rama corta por petición**, creada desde `main` actualizado y con nombre `<tipo>/<nombre>` en minúsculas, sin tildes ni espacios, con guiones:
  - `pnj/<nombre>`: PNJs y monstruos (si llevan un objeto exclusivo, va en la misma rama).
  - `item/<nombre>`: objetos, armas, baseitems.
  - `spell/<nombre>`: hechizos.
  - `fix/<qué>`: retoques a algo ya existente.
  - `notes/<qué>`: cambios solo en `_notes/`.
- Cada rama se integra en `main` con una PR usando **squash and merge** y después se borra. Una rama ya mergeada no se reutiliza: para la siguiente petición se crea otra desde `main`.
- Todo el contenido de campaña vive en un solo JSON y lo nuevo se añade al final de cada array. Si hay dos ramas abiertas a la vez, la segunda en mergearse chocará en ese punto: antes de su PR se actualiza con `main` y el conflicto se resuelve quedándose con las dos entradas.
- La antigua rama `wip` ya no se usa.
- Tras mergear, en 5e.tools hay que borrar el brew y volver a cargarlo: los ficheros cargados no se actualizan solos.

Carpetas relevantes en `main`:
- `creature/`: contenido de campaña terminado (monstruos, PNJs, objetos base...), en formato homebrew válido para 5e.tools. Sigue el convenio del repo oficial de homebrew (`TheGiddyLimit/homebrew`): un fichero por fuente, nombrado `Autor; Descripción.json`, ubicado en la carpeta del tipo de contenido principal — el fichero puede incluir varios props (`monster`, `baseitem`, etc.) a la vez.
- `WIP/`: fichas y aventuras en borrador, todavía no listas para pulir del todo (pueden no pasar la validación de esquema). Puede no existir si no hay borradores activos: git no versiona carpetas vacías.
- `_notes/`: notas de partida (incluye `Jarlmoot/` con las mazmorras de cada runa).
- `_img/`: imágenes vinculadas a fuentes (`sources`) declaradas en el contenido homebrew — esta carpeta la valida el propio tooling de 5e.tools.
- `_homebrew_images/`: retratos y assets de PNJ usados en documentos de Homebrewery. No son contenido homebrew cargable por 5e.tools, así que viven fuera de `_img/` para no romper esa validación.
- `_node/` y `_test/`: scripts de utilidad (`5etools-utils`) para generar índices y validar el contenido (`npm test`).

Antiguo contenido de la rama `main` original (screens del DM, fichas antiguas de Adan/Eva en `Sources/`, notas sueltas en `notasRol`) quedó descartado porque ya estaba superado por las fichas actuales en `WIP/`; solo se rescataron los retratos de PNJ.
