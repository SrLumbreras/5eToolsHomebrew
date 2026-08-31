# Decisiones de estilo por criatura

Notas puntuales sobre una criatura concreta que un asistente debería conocer
**antes de volver a editarla** — no son inventario ni se actualizan cuando se
añaden monstruos nuevos; solo se tocan cuando la decisión en sí cambia.

## Hjoölvir — reacción Ice Armor

La salvación de la rotura de hielo se mantiene como **una sola frase en
prosa** ("...must succeed on a {@dc 18} Dexterity saving throw or take 13
({@damage 3d8}) Cold damage.") en vez de un bloque `{@actSave}` /
`{@actSaveFail}` aparte, aunque el resto del fichero use vocabulario 2024
completo. Es una preferencia de redacción explícita de Raul (2026-08-31): no
la "corrijas" al formato partido si vuelves a tocar esta reacción.

## Sephek Kaltro / Eva, Winter Acolyte — spellcasting

Su spellcasting se reestructuró de texto suelto con viñetas a la estructura
`spellcasting` propia del esquema de 5e.tools, pero **conservando los mismos
hechizos y slots de siempre** (2026-08-31). No se rediseñó al estilo 2024
"sin slots" (At Will / X-Day Each con lista recortada) — eso implica decidir
qué hechizos se quedan fuera, y sigue pendiente como decisión de contenido de
Raul si algún día lo pide explícitamente.
