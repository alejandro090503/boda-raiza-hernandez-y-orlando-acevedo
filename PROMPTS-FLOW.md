# Prompts de Flow — escena de los camiones (Raiza & Orlando)

**Dos clips, vertical 9:16, animación 2D dibujada a mano** (acuarela/gouache, tipo cuento
ilustrado). Los camiones son **camiones americanos medianos** (cabina sencilla, sin dormitorio),
blancos con cromo — **dibujados en 2D**, no renders 3D ni fotografía. Llegan **de los lados** (uno por la izquierda, otro por la derecha), se topan
**de frente entre ellos**, y la cámara mira **desde el borde de la carretera** para que las
puertas queden a la vista.

## Qué salió mal en el intento anterior y cómo se corrige

| Problema | Causa | Corrección en el prompt |
|---|---|---|
| Los novios salían del cofre, del espejo y de la parrilla | Los camiones quedaron **de frente a la cámara**; las puertas van en el costado y nunca estuvieron en cuadro, así que Veo inventó por dónde salir | Cámara **al borde de la carretera**: los camiones se ven **de perfil**, se topan de frente entre ellos, y la puerta del costado que da a cámara queda **a la vista** |
| Los personajes se materializaban de la nada | El prompt nunca describió la mecánica | Se describe paso a paso: la puerta **se abre hacia la cámara** → aparecen **parados en el hueco de la puerta** → bajan **los escalones** → pisan el suelo |
| Look de render 3D | El estilo pedía "3D animated" | Estilo nuevo: **animación 2D dibujada a mano** |

## Ajustes en Flow (iguales para los 2 clips)

| Ajuste | Valor |
|---|---|
| **Relación de aspecto** | **9:16 vertical** — seleccionarlo en Flow; el prompt solo no basta |
| Resolución / duración | 720×1280, 24 fps, 8 s |
| Modo | **Ingredients to Video** en el clip 1; **Frames to Video** en el 2 |
| Ingredientes | `novia.png`, `novio.png` y la foto del camión blanco (solo como referencia de look; el tamaño va **mediano**) |
| Negative prompt | `trucks facing the viewer, trucks side by side, parallel trucks, giant truck, oversized truck, long sleeper cab, monster truck, 3d render, cgi, pixar style, photorealistic, photograph, live action, hyperrealistic, real people, skin pores, front view of truck, truck facing camera, character emerging from hood, character on the bumper, character on the grille, floating people, bus, minibus, van, trailer, horizontal composition, landscape framing, letterbox, black bars, text, letters, watermark, logo, subtitles, extra limbs, extra fingers, blurry, shaky camera, crowd` |

**Consistencia:** pegar `[PERSONAJES]`, `[CAMIONES]` y `[ESTILO]` **literal** en los dos prompts.

**Encadenado:** último frame del clip 1 como *first frame* del clip 2.

---

## [ESTILO] — bloque fijo, va en los 2 prompts

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

## [PERSONAJES] — bloque fijo, va en los 2 prompts

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

## [CAMIONES] — bloque fijo, va en los 2 prompts

```
TRUCKS (keep identical in every shot) — HAND-DRAWN 2D illustrations of MEDIUM-SIZE American
trucks. IMPORTANT: these are MEDIUM trucks, NOT giant long-haul rigs. Keep them modest and
friendly in scale — roughly two and a half times the height of a person, small enough that a
person standing next to the cab reaches above the wheel.
DAY CAB, NO SLEEPER BOX behind the cab. Moderately short hood, not an extra-long nose.
They keep the classic American look: upright chrome bar grille, chrome front bumper, chrome
sun visor over the windshield, and two modest chrome exhaust stacks behind the cab.
No trailer attached.
Each cab has a CLEARLY DRAWN DOOR on each side, with a window, a door handle, a grab
rail, and two chrome climbing steps below it. The door is an obvious, visible feature.
Both trucks are pearl-white with chrome, painted in watercolour with ink outlines. The
BRIDE's truck has champagne-cream pinstriping; the GROOM's truck has silver pinstriping.
They are trucks, not buses and not vans — and medium-sized, never oversized.
```

---

## CLIP 1 · Llegan los camiones y bajan los novios (8 s)

```
[ESTILO]
[CAMIONES]
[PERSONAJES]

ACTION FIRST: two medium white trucks drive toward each other along a road and stop grille to
grille in the middle of the frame. One arrives FROM THE LEFT EDGE driving rightwards, the
other arrives FROM THE RIGHT EDGE driving leftwards. THE TRUCKS FACE EACH OTHER — they do NOT
face the camera. Their two grilles point at one another across a small gap in the centre.

CAMERA: we are standing AT THE EDGE OF THE ROAD, watching from the side, camera static. So we
see both trucks IN PROFILE, side-on, travelling horizontally across the tall frame. Because we
see them from the side, THE DOOR ON THE SIDE OF EACH CAB THAT FACES THE CAMERA IS FULLY
VISIBLE, with its window, handle, grab rail and climbing steps. Upper third of the tall frame:
warm champagne sky with painted flowers and sage-green branches hanging down from the top.
Lower two thirds: the pale road.

0-4 s: the champagne-striped truck rolls in from the left and the silver-striped truck rolls
in from the right, both seen in profile, and they come to a gentle stop nose to nose in the
centre with a gap between them. They are medium trucks, modest in size, not towering. They
settle, chrome glinting.

4-8 s: THE DOORS OPEN AND THE CHARACTERS CLIMB OUT THROUGH THEM. First the cab door of the
left truck — the one facing the camera — swings open outward toward us. Only then does the BRIDE appear, STANDING
INSIDE THE OPEN DOORWAY on the top chrome step, holding the grab rail with one hand and her
bouquet in the other. She climbs down the two chrome steps, one foot at a time, and her shoes
touch the road. At the same time the cab door of the right truck swings open toward the camera and the GROOM
appears STANDING IN THAT DOORWAY, then climbs down his steps to the road. Both doors stay
open behind them. They turn and look toward each other across the gap.

MECHANICS — follow exactly: the characters are NOT visible anywhere before their door opens.
They must come out THROUGH THE OPEN DOOR OF THE CAB, standing on the steps, and climb down to
the ground. They must NEVER appear on the hood, on the bumper, on the grille, on the fender,
on the roof, through the windshield, or float in the air. The door opens FIRST, the person
appears SECOND.

The trucks must be MEDIUM-SIZED, with a day cab and no sleeper box — never giant long-haul
rigs. The bride's hair must be BRIGHT RED. The groom must be BALD with a FULL BEARD.
```

## CLIP 2 · Caminan, se encuentran, se besan y el destello (8 s)

```
[ESTILO]
[CAMIONES]
[PERSONAJES]

VERTICAL 9:16 PORTRAIT SHOT. Same road, camera still at the edge of the road watching from
the side. The two medium white trucks stay parked IN PROFILE, facing each other nose to nose,
at the left and right edges of the tall frame, their cab doors still open, painted softly in
the background. Upper third: champagne sky with painted flowers
and sage branches hanging down.

0-4 s: the BRIDE walks slowly in from the left and the GROOM walks slowly in from the right,
both toward the centre of the tall frame, seen full body, eyes locked on each other, smiling
wider as they get closer. Her gown and veil sway with each step. The camera pushes in slowly.

4-6 s: they stop face to face in the centre, he gently cups her cheek, they lean in and share
a tender romantic kiss. Framing is now full-body-to-waist, the couple centred, the painted
trucks framing them left and right. Her veil lifts in the breeze.

6-8 s: the kiss holds while a cloud of hand-painted silver and champagne sparkles swirls
upward around them, and a soft warm glow grows from between them, brightening the whole
frame. Tender and unhurried.

Keep both faces exactly as in the previous shot. The trucks stay MEDIUM-SIZED. The bride's
hair must be BRIGHT RED. The groom must be BALD with a FULL BEARD. Nobody climbs on the
trucks.
```

> El fundido final a blanco lo pongo yo con ffmpeg al unir los dos clips: sale mas limpio
> que pedirselo a Veo, y empalma exacto con el fondo champán de la invitación.

---

## Recorte sugerido

| Clip | Recorte | Se queda con |
|---|---|---|
| 1 | 0:00 → 0:06 | llegada + bajan |
| 2 | 0:00 → 0:08 | caminata + beso + resplandor |

≈ **14 s** en total, mas el fundido a blanco del final.

## Cuando estén los clips

Dejarlos en Descargas y avisarme. Los uno con ffmpeg en `escena.mp4` (720×1280, H.264), con
cross-dissolve entre clips y fundido final a blanco, y reemplazo el actual.
