# Prompts de Flow — escena de los camiones (Raiza & Orlando)

**Tres clips, formato vertical 9:16.** Cada clip lleva dos tiempos, así que la animación
completa cabe en ~15 s ya recortada.

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
| Ingredientes | Subir `novia.png` y `novio.png` (están en esta carpeta) como referencia de personaje |
| Negative prompt | `horizontal composition, landscape framing, letterbox, black bars, text, letters, watermark, logo, subtitles, distorted faces, extra limbs, extra fingers, blurry, low quality, shaky camera, modern city, cars, crowd, photorealistic skin pores` |

**Consistencia:** pegar `[PERSONAJES]` y `[ESTILO]` **literal** en los tres prompts. Si los
parafraseas, Veo devuelve otra cara.

**Encadenado:** exportar el último frame del clip 1 y usarlo como *first frame* del clip 2, y
lo mismo del 2 al 3. Sin eso saltan la luz y las posiciones.

---

## [PERSONAJES] — bloque fijo, va en los 3 prompts

```
CHARACTERS (keep identical in every shot):
BRIDE — elegant stylized 3D caricature of a real woman, refined and tasteful, not cartoonish:
long vivid red-copper hair, fair skin, soft rosy cheeks, large expressive blue eyes, gentle
smile. Fitted ivory-white satin wedding gown with off-shoulder neckline and a small train,
sheer veil, pearl necklace, holding a compact bouquet of champagne-cream roses with sage
green leaves.
GROOM — elegant stylized 3D caricature of a real man, refined and tasteful: completely bald
smooth head, full well-groomed dark brown beard and moustache, warm skin, kind blue eyes,
slight smile. Black slim tuxedo, black bow tie, crisp white shirt, white pocket square.
The groom is slightly taller than the bride.
```

## [ESTILO] — bloque fijo, va en los 3 prompts

```
FORMAT: vertical 9:16 portrait video, tall frame. Compose for a phone screen: the action sits
in the lower-middle third, with open sky and overhanging foliage filling the upper third.
Never compose this as a wide horizontal shot.

STYLE: elegant wedding-invitation animation, soft cinematic lighting, warm golden hour glow.
Colour palette strictly champagne cream (#F7E7CE), sage green (#a8b8a9) and soft silver
(#C0C0C0). Dreamy shallow depth of field, gentle film grain, floating specks of light.
Smooth, slow, romantic motion. No text anywhere.
```

---

## CLIP 1 · Llegan los camiones y bajan los novios (8 s)

```
[ESTILO]
[PERSONAJES]

VERTICAL 9:16 PORTRAIT SHOT. Locked-off camera, static, at street level, tilted slightly down.
Tall frame: the upper third is soft champagne sky with sage-green eucalyptus branches arching
in from the top corners; the lower two thirds is an empty pale champagne-cream street.

First half of the shot: two vintage rounded 1950s touring buses roll slowly into the lower
part of the tall frame from opposite sides — a champagne-cream bus with a silver roof comes
in from the left facing right, a sage-green bus with a champagne roof comes in from the right
facing left. Only the front halves of the buses fit inside the narrow vertical frame; they
glide to a gentle stop facing each other with a gap in the centre, suspension settling with
a soft bounce.

Second half of the shot: the folding door of the champagne-cream bus opens and the BRIDE steps
down onto the street holding her bouquet; at the same moment the door of the sage-green bus
opens and the GROOM steps down adjusting his bow tie. Both are seen full body, small in the
tall frame, and turn to look toward the centre. Tiny motes of light drift down through the air.
```

## CLIP 2 · Caminan, se encuentran y se besan (8 s)

```
[ESTILO]
[PERSONAJES]

VERTICAL 9:16 PORTRAIT SHOT. Tall frame, camera at chest height pushing in very slowly.
Upper third: champagne sky and overhanging sage eucalyptus branches. Lower two thirds: the
champagne-cream street with the front of each parked bus just visible at the left and right
edges, soft and out of focus.

First part of the shot: the BRIDE walks slowly in from the left edge and the GROOM walks
slowly in from the right edge, both toward the centre of the tall frame, seen full body, eyes
locked on each other, smiling wider as they get closer. Her gown and veil sway with each step.

Final part of the shot: they stop face to face in the centre of the vertical frame, he gently
cups her cheek, they lean in and share a tender romantic kiss. The camera has pushed in to a
full-body-to-waist framing, the couple centred, foliage still arching overhead. Her veil lifts
slightly in the breeze. Soft petals and light motes drift past. Tender and unhurried.
```

## CLIP 3 · El destello que da paso a la invitación (8 s)

```
[ESTILO]
[PERSONAJES]

VERTICAL 9:16 PORTRAIT SHOT. Tall frame, medium shot of the BRIDE and GROOM kissing, centred
in the lower-middle of the frame, the two buses soft and blurred at the left and right edges,
warm backlight rimming their silhouettes, open champagne space above their heads.

First part of the shot: the kiss holds, and a cloud of delicate silver and champagne sparkles
swirls upward through the tall frame, rising from the couple toward the top of the screen.

Final part of the shot: a soft elegant burst of warm white light blooms outward from between
them, expanding up and down the vertical frame until it fills the whole screen and everything
dissolves into a clean soft cream-white. The shot ends on a plain warm cream-white surface,
completely empty and evenly lit, edge to edge. No text, no objects.
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

Dejarlos en Descargas y avisarme. Los concateno con ffmpeg en un solo `escena.mp4`
(720×1280, H.264, ~2 MB) y lo pongo en lugar de la animación GSAP `startBusScene()`,
conservando el botón **Saltar** y las dos redes de seguridad que hacen que la invitación
siempre aparezca.
