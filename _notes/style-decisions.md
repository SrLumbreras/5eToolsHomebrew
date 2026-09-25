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

## Eva Elohim — Sending

Tiene *Sending* aunque no se use en combate: es importante para la campaña.
No lo quites al rebalancear.

## Convenciones generales (aplican a todo el fichero de campaña)

Estas decisiones no dependen de una criatura en concreto: fijan cómo se
escribe contenido nuevo a partir de ahora. `test:json` no las detecta
(son de estilo, no de esquema).

- **Sentidos en minúscula**: `"darkvision 60 ft."`, no `"Darkvision 60 ft."`.
  Copper Knobberknocker, Dzaan y Krintaas quedaron en mayúscula por error —
  pendiente de corregir.
- **Tags de reglas 2024 con sufijo de fuente en minúscula**: `{@condition
  restrained|xphb}`, `{@spell command|xphb}`, no `|XPHB` ni Title Case en el
  nombre. Dzaan (y sueltos en Anselmo/Elta Bernero) quedaron en Title Case +
  `|XPHB` — pendiente de homogeneizar. Además, once `{@condition}` del
  fichero no llevan sufijo de fuente en absoluto (Reghed Hunter, Peñalba's
  Soldier, Hjoölvir, Haumea, Sabrae Lylyl, Elta Bernero): sin sufijo pueden
  resolver contra la redacción de 2014.
- **`{@variantrule}`/`{@action}` para términos de reglas** (Hit Points,
  Speed, Disadvantage, Opportunity Attack, Dash, Disengage, Hide...): Adan
  Elohim, Copper Knobberknocker, Dzaan y Krintaas los enlazan; las trece
  fichas anteriores los dejan en texto plano. Pendiente: ¿se retroetiqueta
  el resto, o se documenta el corte y se deja como estaba?
- **`isNpc: true` en todo PNJ con nombre propio**: falta en Sephek Kaltro,
  Eva Elohim, Adan Elohim, Charon, Haumea, Yggdra Arlaggath y Sabrae Lylyl.
- **Un objeto mágico que reproduce una habilidad ya tageada en un
  statblock usa los mismos tags inline que el statblock**, no texto plano.
  Scarfall y Ebonrose lo incumplen ahora mismo (ver más abajo).

## Scarfall / Ebonrose — texto sin tagear

Scarfall repite en prosa la habilidad de herida de Sabrae Lylyl ("1d4
Necrotic damage", "DC 15 Constitution saving throw", "DC 15 Wisdom
(Medicine) check") en vez de `{@damage 1d4}`, `{@dc 15}`, `{@skill
Medicine}`. Ebonrose tiene "spell save DC 17" en vez de `{@dc 17}`. No es
una elección deliberada — pendiente de arreglar.

## Fallen General Shadow — sin `isNamedCreature` ni `fluff`

Jefe único sin `isNamedCreature: true` y sin ningún `fluff` (ni texto ni
imagen). Su inmunidad a golpe/perforante/cortante, condicionada al estado
del Altar de Runas según su propio rasgo Conditioned Immunity, no lleva
`"cond": true` ni una `note` que lo explique. Si su historia se cuenta solo
en notas de partida, dejarlo dicho aquí; si no, pendiente de completar.

## Charon, the Protector / Haumea, the 2nd Pillar — fluff sin texto

Ambos tienen `hasFluff`/`hasFluffImages` en `true` pero `fluff.entries`
vacío (solo la imagen compartida `Charon_and_Harumea.webp`). Si el lore de
los Pilares vive en otro sitio, confirmarlo aquí para no "rellenarlo" sin
que haga falta.

## Dzaan / Krintaas — arte y token reciclados del módulo oficial

A diferencia del resto del fichero (token oficial vía `"token":
{name, source}`, o arte propio subido a los releases de GitHub), Dzaan usa
`hasToken` + `tokenHref` de tipo `"internal"` apuntando a un asset propio de
5e.tools (`bestiary/tokens/IDRotF/Dzaan.webp`), y tanto Dzaan como Krintaas
reutilizan imágenes internas de Rime of the Frostmaiden en su fluff. Tiene
sentido si es porque son PNJ reciclados del módulo oficial y no creaciones
nuevas — dejarlo dicho para que no se "corrija" a subir arte propio sin
necesidad.
