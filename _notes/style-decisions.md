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

## Eva Elohim (antes "Eva, Winter Acolyte") — spellcasting

El 2026-08-31 su spellcasting pasó a la estructura `spellcasting` de 5e.tools
conservando los hechizos y slots clásicos. **El 2026-09-24 Raul decidió
pasarlo al formato 2024 sin slots**, con acción de Spellcasting por
frecuencia y lista recortada al tope de nivel 3 propio de un CR 5:
At Will *Command, Spare the Dying, Thaumaturgy*; 2/Day Each *Bless, Hold
Person*; 1/Day Each *Bestow Curse, Dispel Magic, Spirit Guardians*. El daño
fiable va en el ataque propio **Rime Flare** (patrón 2024 de "ataque firma en
vez de cantrip"). Se quitaron Guidance, Sacred Flame, Cure Wounds, Spiritual
Weapon, Banishment, Guardian of Faith y Flame Strike. Si alguna vez vuelve un
hechizo de nivel 4+, hay que revisar el CR.

Al pasar a no muerta, su Channel Divinity se quedó solo con la curación
(acción **Chilling Blessing (2/Day)**); se quitó Turn Undead.
