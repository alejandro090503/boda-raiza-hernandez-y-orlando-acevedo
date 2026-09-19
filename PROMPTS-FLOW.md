# Prompts de Flow — escena de los camiones (Raiza & Orlando)

**Tres clips** que cubren la secuencia completa. Cada clip lleva dos tiempos, así que la
animación entera cabe en ~12-15 s ya recortada.

| Clip | Qué pasa | Tiempos dentro del clip |
|---|---|---|
| 1 | Llegan los camiones y bajan los novios | 0-4 s llegan y se estacionan · 4-8 s se abren las puertas y bajan |
| 2 | Caminan, se encuentran y se besan | 0-5 s caminan al centro · 5-8 s se encuentran y se besan |
| 3 | El destello que da paso a la invitación | 0-3 s el beso sostenido · 3-8 s chispas y destello a blanco |

## Ajustes en Flow (iguales para los 3 clips)

| Ajuste | Valor |
|---|---|
| Relación de aspecto | **9:16 vertical** (igual que `sobre.mp4`: 720×1280, 24 fps, 8 s) |
| Modo | **Ingredients to Video** en el clip 1; **Frames to Video** en el 2 y el 3 |
| Ingredientes | Subir `novia.png` y `novio.png` (están en esta carpeta) como referencia de personaje |
| Negative prompt | `text, letters, watermark, logo, subtitles, distorted faces, extra limbs, extra fingers, blurry, low quality, shaky camera, modern city, cars, crowd, photorealistic skin pores` |

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
STYLE: elegant wedding-invitation animation, soft cinematic lighting, warm golden hour glow.
Colour palette strictly champagne cream (#F7E7CE), sage green (#a8b8a9) and soft silver
(#C0C0C0). Dreamy shallow depth of field, gentle film grain, floating specks of light.
Smooth, slow, romantic motion. Vertical 9:16 framing. No text anywhere.
```

---

## CLIP 1 · Llegan los camiones y bajan los novios (8 s)

```
[ESTILO]
[PERSONAJES]

SHOT: Locked-off wide shot, camera static at street level. An empty pale champagne-cream
street under soft morning light, blurred sage-green foliage arching over the top of the frame.

First half of the shot: two vintage rounded 1950s touring buses drive in slowly from opposite
sides of the frame — a champagne-cream bus with a silver roof enters from the left facing
right, a sage-green bus with a champagne roof enters from the right facing left. They glide
to a gentle stop in the centre, parked front to front with a gap between them, suspension
settling with a soft bounce.

Second half of the shot: the folding door of the champagne-cream bus opens and the BRIDE
steps down onto the street holding her bouquet; at the same moment the door of the sage-green
bus opens and the GROOM steps down adjusting his bow tie. Both turn and look toward the centre
of the frame. Tiny motes of light drift through the air.
```

## CLIP 2 · Caminan, se encuentran y se besan (8 s)

```
[ESTILO]
[PERSONAJES]

SHOT: Same champagne-cream street, the two buses parked front to front in the background,
slightly out of focus. The camera pushes in very slowly throughout the shot.

First part of the shot: the BRIDE walks slowly from the left and the GROOM walks slowly from
the right, both toward the centre of the frame, eyes locked on each other, smiling wider as
they get closer. Her gown and veil sway with each step.

Final part of the shot: they stop face to face in the centre, he gently cups her cheek, they
lean in and share a tender romantic kiss. Her veil lifts slightly in the breeze. Soft petals
and light motes drift past. Tender and unhurried.
```

## CLIP 3 · El destello que da paso a la invitación (8 s)

```
[ESTILO]
[PERSONAJES]

SHOT: Medium shot of the BRIDE and GROOM kissing in the centre of the street, the two buses
soft and blurred behind them, warm backlight rimming their silhouettes.

First part of the shot: the kiss holds, and a cloud of delicate silver and champagne sparkles
begins to swirl upward around them.

Final part of the shot: a soft elegant burst of warm white light blooms outward from between
them, growing until it fills the entire frame and everything dissolves into a clean soft
cream-white. The shot ends on a plain warm cream-white surface, completely empty and evenly
lit. No text, no objects.
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
