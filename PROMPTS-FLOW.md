# Prompts de Flow — escena de los camiones (Raiza & Orlando)

**Tres clips, formato vertical 9:16.** Todo es **animación 3D tipo película animada**, no
imagen real. Los camiones son **tractocamiones americanos de trompa larga tipo Peterbilt 389,
blancos con cromo** (la referencia que mandó el cliente) pero **dibujados**, no fotográficos.

| Clip | Qué pasa | Tiempos dentro del clip |
|---|---|---|
| 1 | Llegan los camiones y bajan los novios | 0-4 s llegan y se estacionan · 4-8 s se abren las puertas y bajan |
| 2 | Caminan, se encuentran y se besan | 0-5 s caminan al centro · 5-8 s se encuentran y se besan |
| 3 | El destello que da paso a la invitación | 0-3 s el beso sostenido · 3-8 s chispas y destello a blanco |

## Ajustes en Flow (iguales para los 3 clips)

| Ajuste | Valor |
|---|---|
| **Relación de aspecto** | **9:16 vertical** — hay que seleccionarlo en Flow, el prompt solo no basta |
| Resolución / duración | 720×1280, 24 fps, 8 s (igual que `sobre.mp4`) |
| Modo | **Ingredients to Video** en el clip 1; **Frames to Video** en el 2 y el 3 |
| Ingredientes | Subir `novia.png`, `novio.png` y **la foto del Peterbilt blanco** como referencia |
| Negative prompt | `photorealistic, photograph, live action footage, hyperrealistic, real people, documentary, cctv, skin pores, bus, minibus, van, vintage bus, coach, trailer, semi trailer, cargo box, horizontal composition, landscape framing, letterbox, black bars, text, letters, watermark, logo, subtitles, distorted faces, extra limbs, extra fingers, blurry, low quality, shaky camera, modern city, traffic, crowd` |

**Consistencia:** pegar `[PERSONAJES]`, `[CAMIONES]` y `[ESTILO]` **literal** en los tres
prompts. Si los parafraseas, Veo devuelve otra cara y otro camión.

**Encadenado:** exportar el último frame del clip 1 y usarlo como *first frame* del clip 2, y
lo mismo del 2 al 3. Sin eso saltan la luz y las posiciones.

---

## [PERSONAJES] — bloque fijo, va en los 3 prompts

```
CHARACTERS (keep identical in every shot) — ANIMATED CARTOON CHARACTERS, like a 3D animated
feature film. Charming and elegant, never photorealistic.
BRIDE — stylized animated woman with soft rounded features: LONG VIVID RED-COPPER HAIR, fair
skin, rosy cheeks, big expressive blue eyes, warm gentle smile. Fitted ivory-white satin
wedding gown with off-shoulder neckline and a small train, sheer veil, pearl necklace,
holding a compact bouquet of champagne-cream roses with sage green leaves.
GROOM — stylized animated man with soft rounded features: COMPLETELY BALD smooth head, FULL
well-groomed dark brown beard and moustache, warm skin, kind blue eyes, friendly smile.
Black slim tuxedo, black bow tie, crisp white shirt, white pocket square.
The groom is slightly taller than the bride. Both are clearly drawn/rendered characters with
smooth matte shading — no skin pores, no photographic detail.
```

## [CAMIONES] — bloque fijo, va en los 3 prompts

```
TRUCKS (keep identical in every shot) — STYLIZED ANIMATED VERSIONS, not photoreal models:
Two AMERICAN LONG-NOSE SHOW SEMI TRUCKS drawn in the same cartoon 3D style as the characters,
with softly rounded edges and chunky friendly proportions. Classic Peterbilt 389 shape: very long squared
hood, tall vertical chrome bar grille, massive polished chrome front bumper, chrome sun
visor over the windshield, TWO TALL POLISHED CHROME EXHAUST STACKS rising vertically behind
the cab, large square sleeper box behind the cab, polished aluminium wheels with chrome hubs.
BOBTAIL — no trailer attached, just the tractor unit.
Both trucks are glossy pearl-white, immaculate, with abundant bright stylized chrome —
rendered like a cartoon, clean and simplified, never like a photograph of a real truck.
The BRIDE's truck carries delicate champagne-cream pinstriping; the GROOM's truck carries
delicate sage-green pinstriping. Nothing else differs between them.
These are big rigs, not buses and not vans.
```

## [ESTILO] — bloque fijo, va en los 3 prompts

```
FORMAT: vertical 9:16 portrait video, tall frame. Compose for a phone screen: the action sits
in the lower-middle third, with open sky and overhanging foliage filling the upper third.
Never compose this as a wide horizontal shot.

STYLE — THIS IS A 3D ANIMATED CARTOON, NOT LIVE ACTION AND NOT PHOTOREALISTIC.
Look and feel of a modern animated feature film (Pixar / Disney style): stylized characters
and vehicles with soft rounded forms, clean simplified surfaces, slightly exaggerated
proportions, big expressive eyes, smooth matte shading, no skin pores, no photographic
texture, no real people. Everything is rendered, illustrated, charming and warm.

Elegant wedding-invitation animation, soft cinematic lighting, warm golden hour glow.
Colour palette strictly champagne cream (#F7E7CE), sage green (#a8b8a9) and soft silver
(#C0C0C0), with bright stylized chrome on the trucks. Dreamy shallow depth of field, floating
specks of light. Smooth, slow, romantic motion. No text anywhere.
```

---

## CLIP 1 · Llegan los camiones y bajan los novios (8 s)

```
[ESTILO]
[CAMIONES]
[PERSONAJES]

VERTICAL 9:16 PORTRAIT SHOT. Locked-off camera, static, low at street level, tilted slightly
up so the trucks look tall and imposing. Tall frame: the upper third is soft champagne sky
with sage-green eucalyptus branches arching in from the top corners; the lower two thirds is
an empty pale champagne-cream road.

First half of the shot: the two white long-nose show semi trucks roll slowly into the frame
from opposite sides — the champagne-pinstriped one from the left, the sage-pinstriped one
from the right — and come to a gentle stop NOSE TO NOSE in the centre with a gap between
them, front three-quarter view so the tall chrome grilles and the big chrome bumpers face
each other. Only the front halves of the trucks fit inside the narrow vertical frame; the
chrome exhaust stacks rise past the top of the cabs. Air brakes settle with a soft bounce,
chrome glinting.

Second half of the shot: the high cab door of the left truck swings open and the BRIDE climbs
down the chrome steps onto the road — she has LONG VIVID RED HAIR, bright red-copper, clearly
visible, and wears an elegant ivory-white satin wedding gown with a sheer veil, holding her
bouquet, lifting her skirt slightly as she steps down. At the same moment the cab door of the
right truck opens and the GROOM climbs down — he is COMPLETELY BALD, with a FULL DARK BEARD,
and wears an elegant black wedding tuxedo with a black bow tie, adjusting it as he lands.
Both are seen full body, small against the big rigs, and turn to look toward the centre.
Tiny motes of light drift down through the air.

IMPORTANT, do not deviate: the vehicles must be AMERICAN LONG-NOSE SEMI TRUCKS with tall
chrome exhaust stacks and a long squared hood — never a bus or a van, and no trailer behind.
The bride's hair must be RED. The groom must be BALD with a BEARD — no hair on his head at
all. Both must wear elegant formal wedding attire.
```

## CLIP 2 · Caminan, se encuentran y se besan (8 s)

```
[ESTILO]
[CAMIONES]
[PERSONAJES]

VERTICAL 9:16 PORTRAIT SHOT. Tall frame, camera at chest height pushing in very slowly.
Upper third: champagne sky and overhanging sage eucalyptus branches. Lower two thirds: the
champagne-cream road, with the chrome grille and bumper of each parked white semi truck just
visible at the left and right edges, soft and out of focus.

First part of the shot: the BRIDE walks slowly in from the left edge and the GROOM walks
slowly in from the right edge, both toward the centre of the tall frame, seen full body, eyes
locked on each other, smiling wider as they get closer. Her gown and veil sway with each step.

Final part of the shot: they stop face to face in the centre of the vertical frame, he gently
cups her cheek, they lean in and share a tender romantic kiss. The camera has pushed in to a
full-body-to-waist framing, the couple centred, the blurred chrome of the two trucks framing
them left and right, foliage still arching overhead. Her veil lifts slightly in the breeze.
Soft petals and light motes drift past. Tender and unhurried.

IMPORTANT, do not deviate: the vehicles at the edges are AMERICAN LONG-NOSE SEMI TRUCKS with
chrome grilles — never buses or vans. The bride's hair must be RED. The groom must be BALD
with a BEARD — no hair on his head at all. Keep both faces exactly as in the previous shot.
```

## CLIP 3 · El destello que da paso a la invitación (8 s)

```
[ESTILO]
[CAMIONES]
[PERSONAJES]

VERTICAL 9:16 PORTRAIT SHOT. Tall frame, medium shot of the BRIDE and GROOM kissing, centred
in the lower-middle of the frame, the chrome fronts of the two white semi trucks soft and
blurred at the left and right edges, warm backlight rimming their silhouettes, open champagne
space above their heads.

First part of the shot: the kiss holds, and a cloud of delicate silver and champagne sparkles
swirls upward through the tall frame, rising from the couple toward the top of the screen,
catching on the blurred chrome.

Final part of the shot: a soft elegant burst of warm white light blooms outward from between
them, expanding up and down the vertical frame until it fills the whole screen and everything
dissolves into a clean soft cream-white. The shot ends on a plain warm cream-white surface,
completely empty and evenly lit, edge to edge. No text, no objects.

IMPORTANT, do not deviate: the vehicles are AMERICAN LONG-NOSE SEMI TRUCKS — never buses.
The bride's hair must be RED. The groom must be BALD with a BEARD. Keep both faces exactly
as in the previous shot.
```

> El clip 3 termina en crema plano a propósito: así empalma sin corte con el fondo champán
> de la invitación.

---

## Recorte sugerido

| Clip | Recorte | Se queda con |
|---|---|---|
| 1 | 0:00 → 0:05 | llegada + bajan |
| 2 | 0:01 → 0:06 | caminata + beso |
| 3 | 0:02 → 0:07 | chispas + destello |

≈ **15 s** en total. Si se quiere aún más corto, bajar cada uno a 4 s (≈12 s).

## Cuando estén los clips

Dejarlos en Descargas y avisarme. Los uno con ffmpeg en `escena.mp4` (720×1280, H.264),
con cross-dissolve entre clips y fundido final a blanco, y reemplazo el actual — que todavía
tiene los autobuses.
