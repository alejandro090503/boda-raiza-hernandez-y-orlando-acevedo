# Prompts de Flow — escena de los camiones (Raiza & Orlando)

**Puesta en escena correcta** (la del clip de referencia): los camiones se ven **de perfil**,
entran uno por la izquierda y otro por la derecha, y se detienen **nariz con nariz** dejando un
hueco al centro. La puerta que se abre es la del **lado de la cámara**; los novios bajan hacia
adelante y quedan parados delante de su propio camión.

**Ajustes en Flow:** 9:16 vertical (seleccionarlo, el prompt solo no basta) · 8 s ·
*Ingredients to Video* con `novia.png` y `novio.png`. El clip 2 sale del último frame
(*Frames to Video*).

**Negative prompt:**

```
truck facing the camera, front view of truck, trucks driving toward the viewer, road vanishing
point, dashed lane lines, giant truck, sleeper cab, trailer, character on the hood, character
on the grille, floating people, photorealistic, live action, real people, horizontal
composition, black bars, text, watermark, extra fingers, blurry, shaky camera
```

---

## CLIP 1 — un solo prompt

```
Vertical 9:16. Warm watercolour storybook illustration, hand-painted, soft and elegant, never
photorealistic. Plain cream and beige background, no sky and no buildings. Eucalyptus branches
with green leaves hang from the top of the frame. Soft golden light.

SIDE VIEW, camera at eye level, static. Two MEDIUM vintage trucks seen fully in PROFILE —
rounded cream and sage-green bodies, chrome trim, round headlights, short cab, no trailer.

One truck drives IN FROM THE LEFT edge facing RIGHT. The other drives IN FROM THE RIGHT edge
facing LEFT. They roll toward each other and STOP NOSE TO NOSE, their front grilles almost
touching at the centre of the frame, leaving a small gap between them.

Then the CAB DOOR OF EACH TRUCK — the door on the side facing the camera — SWINGS OPEN toward
us. Only after the doors are open do the characters appear: from the LEFT truck a BRIDE with
long bright red wavy hair, ivory satin gown and veil, holding a white bouquet; from the RIGHT
truck a GROOM, completely bald with a full dark beard, in a black tuxedo with bow tie. Each
steps down and stands on the ground in front of their own truck, then turns to look at the
other across the gap.

The doors open FIRST, the people appear SECOND. Nobody appears on the hood, grille or roof.
The trucks stay in profile the whole time.
```

## CLIP 2 — desde el último frame del clip 1

```
Same scene, same characters, same two cream trucks stopped nose to nose with their doors open.

The BRIDE and the GROOM walk toward each other into the gap between the two trucks, smiling,
eyes locked. They meet at the centre, he cups her cheek and they share a tender romantic kiss.
Golden sparkles rise around them and a soft warm glow grows, brightening the frame.

Keep both faces identical. Bride: bright red hair. Groom: bald with a full beard. The trucks
stay in profile and nobody climbs on them.
```

---

## Notas

- **"De frente" = entre ellos, no hacia la cámara.** Los camiones se topan nariz con nariz,
  vistos de perfil. La versión "hacia la cámara por la carretera" fue un error de lectura mío.
- **Por qué "las puertas se abren primero":** sin esa frase los personajes se materializan
  atravesando la carrocería o aparecen encima del cofre.
- **Por qué "no sky, no buildings":** el clip que funcionó tiene fondo crema plano; en cuanto
  la IA mete carretera y horizonte, gira los camiones hacia el frente.
- El **fundido final a blanco** lo pongo con ffmpeg al unir los clips; empalma exacto con el
  fondo champán de la invitación.

## Cuando estén los clips

Dejarlos en Descargas y avisarme. Los uno en `escena.mp4` (720×1280, H.264) con
cross-dissolve y fundido a blanco, y reemplazo el actual.
