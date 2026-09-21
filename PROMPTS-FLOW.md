# Prompts de Flow — escena de los camiones (Raiza & Orlando)

**Tres clips, vertical 9:16, animación 2D dibujada a mano** (acuarela/gouache, tipo cuento
ilustrado). Los camiones son tractocamiones americanos de trompa larga tipo **Peterbilt 389**,
blancos con cromo — pero **dibujados en 2D**, no renders 3D ni fotografía.

## Qué salió mal en el intento anterior y cómo se corrige

| Problema | Causa | Corrección en el prompt |
|---|---|---|
| Los novios salían del cofre, del espejo y de la parrilla | Los camiones quedaron **de frente a la cámara**; las puertas van en el costado y nunca estuvieron en cuadro, así que Veo inventó por dónde salir | La cámara se planta **al costado de la carretera**: los camiones se ven **de perfil**, con la puerta del conductor de cara a nosotros |
| Los personajes se materializaban de la nada | El prompt nunca describió la mecánica | Se describe paso a paso: la puerta **se abre hacia la cámara** → aparecen **parados en el hueco de la puerta** → bajan **los escalones** → pisan el suelo |
| Look de render 3D | El estilo pedía "3D animated" | Estilo nuevo: **animación 2D dibujada a mano** |

## Ajustes en Flow (iguales para los 3 clips)

| Ajuste | Valor |
|---|---|
| **Relación de aspecto** | **9:16 vertical** — seleccionarlo en Flow; el prompt solo no basta |
| Resolución / duración | 720×1280, 24 fps, 8 s |
| Modo | **Ingredients to Video** en el clip 1; **Frames to Video** en el 2 y el 3 |
| Ingredientes | `novia.png`, `novio.png` y la foto del Peterbilt blanco |
| Negative prompt | `3d render, cgi, pixar style, photorealistic, photograph, live action, hyperrealistic, real people, skin pores, front view of truck, truck facing camera, character emerging from hood, character on the bumper, character on the grille, floating people, bus, minibus, van, trailer, horizontal composition, landscape framing, letterbox, black bars, text, letters, watermark, logo, subtitles, extra limbs, extra fingers, blurry, shaky camera, crowd` |

**Consistencia:** pegar `[PERSONAJES]`, `[CAMIONES]` y `[ESTILO]` **literal** en los tres prompts.

**Encadenado:** último frame del clip 1 como *first frame* del clip 2, y del 2 al 3.

---

## [ESTILO] — bloque fijo, va en los 3 prompts

```
FORMAT: vertical 9:16 portrait video, tall frame. Compose for a phone screen: the action sits
in the lower-middle third, sky and overhanging flowers fill the upper third. Never compose
this as a wide horizontal shot.

STYLE — 2D HAND-DRAWN ANIMATION. This is a traditional hand-drawn cartoon, like an animated
storybook or a classic 2D animated film. Flat 2D artwork: clean confident ink outlines, soft
watercolour and gouache washes, visible paper texture, simple painted shapes, flat cel
shading with gentle gradients. Absolutely NOT 3D, NOT CGI, NOT a render, NOT photorealistic —
no plastic surfaces, no ray-traced reflections, no lens depth-of-field blur.

Elegant wedding-invitation illustration, warm golden light painted into the artwork.
Colour palette strictly champagne cream (#F7E7CE) and soft silver (#C0C0C0), with sage green
foliage. Plenty of hand-painted flowers framing the frame. Hand-painted sparkles. Smooth,
slow, romantic motion. No text anywhere.
```

## [PERSONAJES] — bloque fijo, va en los 3 prompts

```
CHARACTERS (keep identical in every shot) — 2D hand-drawn animated characters, elegant and
charming, painted in watercolour with clean ink outlines.
BRIDE — LONG BRIGHT TRUE-RED HAIR, vivid crimson red, dyed red (not orange, not ginger, not
auburn), fair skin, rosy cheeks, large expressive eyes, warm gentle smile. Fitted ivory-white
satin wedding gown with off-shoulder neckline and a small train, sheer veil, pearl necklace,
holding a compact bouquet of champagne-cream roses with sage green leaves.
GROOM — COMPLETELY BALD smooth head, FULL well-groomed dark brown beard and moustache, warm
skin, kind eyes, friendly smile. Elegant cream-beige suit with a tie and a crisp white shirt.
The groom is slightly taller than the bride. Both are drawn, never photographic.
```

## [CAMIONES] — bloque fijo, va en los 3 prompts

```
TRUCKS (keep identical in every shot) — HAND-DRAWN 2D illustrations of American long-nose
show semi trucks, classic Peterbilt 389 shape: very long squared hood, tall vertical chrome
bar grille, big chrome front bumper, chrome sun visor over the windshield, TWO TALL CHROME
EXHAUST STACKS rising vertically behind the cab, large square sleeper box behind the cab,
chrome wheels. BOBTAIL — no trailer attached, just the tractor unit.
Each cab has a CLEARLY DRAWN DRIVER DOOR on its side, with a window, a door handle, a grab
rail, and two chrome climbing steps below it. The door is an obvious, visible feature.
Both trucks are pearl-white with chrome, painted in watercolour with ink outlines. The
BRIDE's truck has champagne-cream pinstriping; the GROOM's truck has silver pinstriping.
These are big rigs, not buses and not vans.
```

---

## CLIP 1 · Llegan los camiones y bajan los novios (8 s)

```
[ESTILO]
[CAMIONES]
[PERSONAJES]

VERTICAL 9:16 PORTRAIT SHOT. THE CAMERA STANDS AT THE SIDE OF THE ROAD, NOT IN FRONT OF THE
TRUCKS. We see the trucks FROM THE SIDE, in profile, so that the DRIVER DOOR OF EACH CAB
FACES THE CAMERA and fills a good part of the frame. Never show the trucks head-on; the
grilles point left and right, away from us. Upper third of the tall frame: warm champagne sky
with painted flowers and sage-green branches hanging down from the top. Lower two thirds: a
pale road.

0-4 s: the two white long-nose semi trucks drive in from opposite sides, seen in profile, and
stop side by side in the centre of the frame with a gap between them — the champagne-striped
truck on the left, the silver-striped truck on the right. Their cabs and the two driver doors
are now clearly facing the camera. The trucks settle, chrome glinting.

4-8 s: THE DOORS OPEN AND THE CHARACTERS CLIMB OUT THROUGH THEM. First the driver door of the
left truck swings open outward toward the camera. Only then does the BRIDE appear, STANDING
INSIDE THE OPEN DOORWAY on the top chrome step, holding the grab rail with one hand and her
bouquet in the other. She climbs down the two chrome steps, one foot at a time, and her shoes
touch the road. At the same time the driver door of the right truck swings open and the GROOM
appears STANDING IN THAT DOORWAY, then climbs down his steps to the road. Both doors stay
open behind them. They turn and look toward each other across the gap.

MECHANICS — follow exactly: the characters are NOT visible anywhere before their door opens.
They must come out THROUGH THE OPEN DOOR OF THE CAB, standing on the steps, and climb down to
the ground. They must NEVER appear on the hood, on the bumper, on the grille, on the fender,
on the roof, through the windshield, or float in the air. The door opens FIRST, the person
appears SECOND.

The bride's hair must be BRIGHT RED. The groom must be BALD with a FULL BEARD.
```

## CLIP 2 · Caminan, se encuentran y se besan (8 s)

```
[ESTILO]
[CAMIONES]
[PERSONAJES]

VERTICAL 9:16 PORTRAIT SHOT. Same road, camera still at the side. The two white semi trucks
stay parked in profile at the left and right edges of the tall frame, their driver doors
still open, painted softly in the background. Upper third: champagne sky with painted flowers
and sage branches hanging down.

0-5 s: the BRIDE walks slowly in from the left and the GROOM walks slowly in from the right,
both toward the centre of the tall frame, seen full body, eyes locked on each other, smiling
wider as they get closer. Her gown and veil sway with each step. The camera pushes in slowly.

5-8 s: they stop face to face in the centre, he gently cups her cheek, they lean in and share
a tender romantic kiss. Framing is now full-body-to-waist, the couple centred, the painted
trucks framing them left and right. Her veil lifts in the breeze. Hand-painted petals and
sparkles drift past. Tender and unhurried.

Keep both faces exactly as in the previous shot. The bride's hair must be BRIGHT RED. The
groom must be BALD with a FULL BEARD. Nobody climbs on the trucks.
```

## CLIP 3 · El destello que da paso a la invitación (8 s)

```
[ESTILO]
[CAMIONES]
[PERSONAJES]

VERTICAL 9:16 PORTRAIT SHOT. Medium shot of the BRIDE and GROOM kissing, centred in the
lower-middle of the tall frame, the painted white semi trucks soft at the left and right
edges, warm light behind the couple, painted flowers above their heads.

0-3 s: the kiss holds while a cloud of hand-painted silver and champagne sparkles swirls
upward through the tall frame, rising from the couple toward the top of the screen.

3-8 s: a soft burst of warm white light blooms outward from between them and expands up and
down the vertical frame until it fills the whole screen; everything dissolves into a clean
soft cream-white. The shot ENDS ON A PLAIN WARM CREAM-WHITE SURFACE, completely empty and
evenly lit, edge to edge. No text, no objects.

Keep both faces exactly as in the previous shot.
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

≈ **15 s** en total.

## Cuando estén los clips

Dejarlos en Descargas y avisarme. Los uno con ffmpeg en `escena.mp4` (720×1280, H.264), con
cross-dissolve entre clips y fundido final a blanco, y reemplazo el actual.
