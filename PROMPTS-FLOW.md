# Prompts de Flow — escena de los camiones (Raiza & Orlando)

Cinco clips que cubren la idea completa del cliente: llegan los camiones, bajan los
novios, se encuentran, se besan y un destello da paso a la invitación.

## Ajustes en Flow (iguales para los 5 clips)

| Ajuste | Valor |
|---|---|
| Relación de aspecto | **9:16 vertical** (igual que `sobre.mp4`: 720×1280, 24 fps, 8 s) |
| Modo | **Ingredients to Video** en el clip 1; **Frames to Video / Extend** en los demás |
| Ingredientes | Subir `novia.png` y `novio.png` (están en esta carpeta) como referencia de personaje |
| Negative prompt | `text, letters, watermark, logo, subtitles, distorted faces, extra limbs, extra fingers, blurry, low quality, shaky camera, lens flare artifacts, modern city, cars, crowd, photorealistic human skin pores` |

**Consistencia:** pegar el bloque `[PERSONAJES]` **literal** en los cinco prompts. Es lo que
mantiene a la novia pelirroja y al novio calvo con barba iguales de clip a clip.

**Encadenado:** exportar el **último frame** de cada clip y usarlo como *first frame* del
siguiente (Frames to Video). Así no “saltan” la luz ni la posición.

---

## [PERSONAJES] — bloque fijo, va en los 5 prompts

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
Both are the same height ratio: the groom is slightly taller than the bride.
```

## [ESTILO] — bloque fijo, va en los 5 prompts

```
STYLE: elegant wedding-invitation animation, soft cinematic lighting, warm golden hour glow.
Colour palette strictly champagne cream (#F7E7CE), sage green (#a8b8a9) and soft silver
(#C0C0C0). Dreamy shallow depth of field, gentle film grain, floating specks of light.
Smooth, slow, romantic motion. Vertical 9:16 framing. No text anywhere.
```

---

## CLIP 1 · Llegan los camiones (8 s)

```
[ESTILO]
[PERSONAJES]

SHOT: Locked-off wide shot, camera static at street level. An empty pale champagne-cream
street under soft morning light, blurred sage-green foliage arching over the top of the
frame. Two vintage rounded 1950s touring buses drive in slowly from opposite sides of the
frame — a champagne-cream bus with a silver roof enters from the left facing right, a
sage-green bus with a champagne roof enters from the right facing left. They glide to a
gentle stop in the centre, parked front to front with a small gap between them, suspension
settling with a soft bounce. Tiny motes of light drift through the air. No people visible yet.
```

## CLIP 2 · Bajan los novios (8 s)

```
[ESTILO]
[PERSONAJES]

SHOT: Same locked-off wide shot, same two buses parked front to front in the centre.
The folding door of the champagne-cream bus on the left opens and the BRIDE steps down onto
the street, holding her bouquet, smoothing her gown. At the same moment the door of the
sage-green bus on the right opens and the GROOM steps down, adjusting his bow tie. Both pause
and look toward the centre of the frame. Warm light catches the satin of the gown and the
bride's red hair. Slow, elegant motion.
```

## CLIP 3 · Caminan y se encuentran (8 s)

```
[ESTILO]
[PERSONAJES]

SHOT: Same street, same two buses parked in the background, slightly out of focus.
The BRIDE walks slowly from the left and the GROOM walks slowly from the right, both toward
the centre of the frame, eyes locked on each other, smiling wider as they get closer. Her
gown and veil sway with each step. The camera pushes in very slowly. They stop face to face
in the centre, close enough to touch, and he gently takes her free hand. Soft petals and
light motes drift past. The moment holds.
```

## CLIP 4 · El beso (8 s)

```
[ESTILO]
[PERSONAJES]

SHOT: Medium shot, camera slowly circling a few degrees around the couple standing face to
face in the centre of the street, the two buses soft and blurred behind them. The GROOM
gently cups the BRIDE's cheek, they lean in and share a tender romantic kiss. Her veil lifts
slightly in the breeze, her bouquet held at her side. Warm backlight rims their silhouettes.
Soft silver and champagne sparkles begin to rise around them. Tender, unhurried, romantic.
```

## CLIP 5 · El destello (8 s)

```
[ESTILO]

SHOT: The silhouetted couple kissing in the centre of the frame, seen against warm champagne
light. A cloud of delicate silver and champagne sparkles swirls upward around them and a soft
elegant burst of warm white light blooms outward from between them, growing until it fills the
entire frame and everything dissolves into a clean soft cream-white. The frame ends on a plain
warm cream-white surface, completely empty and evenly lit. No text, no objects.
```

> El clip 5 termina en crema plano a propósito: así empalma sin corte con el fondo champán
> de la invitación.

---

## Si se quiere más corto

Una intro de invitación aguanta ~15 s. Recortar cada clip a **3 s** en la edición
(5 × 3 = 15 s) o quedarse con tres: **1 + 3 + 4-5 fusionados**.

## Cuando estén los clips

Dejarlos en Descargas y avisarme. Los concateno con ffmpeg en un solo `escena.mp4`
(720×1280, H.264, ~2 MB) y lo pongo en lugar de la animación GSAP `startBusScene()`,
conservando el botón **Saltar** y las dos redes de seguridad que hacen que la invitación
siempre aparezca.
