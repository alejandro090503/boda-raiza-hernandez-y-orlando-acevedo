# Prompts de Flow — escena de los camiones (Raiza & Orlando)

**Puesta en escena correcta**: los trailers se ven **de perfil**, entran uno por la izquierda y
otro por la derecha, y se detienen **nariz con nariz** dejando un hueco al centro. La puerta que
se abre es la del **lado de la cámara**; los novios bajan hacia adelante y quedan parados delante
de su propio camión. Estilo **animación 3D**.

**Ajustes en Flow:** 9:16 vertical (seleccionarlo, el prompt solo no basta) · 8 s ·
*Ingredients to Video* con `novia.png` y `novio.png`. El clip 2 sale del último frame
(*Frames to Video*).

**Negative prompt:**

```
truck facing the camera, front view of truck, trucks driving toward the viewer, road vanishing
point, dashed lane lines, bobtail without trailer, bus, van, character on the hood, character
on the grille, floating people, 2D drawing, flat illustration, photorealistic, live action,
real people, horizontal composition, black bars, text, watermark, extra fingers, blurry,
shaky camera
```

---

## CLIP 1 — un solo prompt

```
Vertical 9:16. Charming 3D animated film style, like a modern animated feature — stylized,
smooth shading, soft depth of field, never photorealistic. Plain warm cream and beige
background, no sky and no buildings. Eucalyptus branches with green leaves hang from the top
of the frame. Soft golden light, tiny sparkles in the air.

SIDE VIEW, camera at eye level, static. Two SEMI TRUCKS with their TRAILERS attached, seen
fully in PROFILE — classic long-nose chrome-grilled tractor pulling a clean trailer, cream and
sage-green paint, polished chrome stacks and wheels.

One rig drives IN FROM THE LEFT edge facing RIGHT. The other drives IN FROM THE RIGHT edge
facing LEFT. They roll toward each other and STOP NOSE TO NOSE, their front grilles almost
touching at the centre of the frame, leaving a small gap between them. The long trailers
stretch off both edges of the frame.

Then the CAB DOOR OF EACH TRUCK — the door on the side facing the camera — SWINGS OPEN toward
us. Only after the doors are open do the characters appear: from the LEFT truck a BRIDE with
long bright red wavy hair, ivory satin gown and veil, holding a white bouquet; from the RIGHT
truck a GROOM, completely bald with a full dark beard, in a black tuxedo with bow tie. Each
climbs down the cab steps and stands on the ground in front of their own truck, then turns to look at the
other across the gap.

The doors open FIRST, the people appear SECOND. Nobody appears on the hood, grille or roof.
Both rigs stay in profile the whole time.
```

## CLIP 2 — desde el último frame del clip 1

```
Same 3D animated scene, same characters, same two rigs stopped nose to nose with their cab
doors open.

The BRIDE and the GROOM walk toward each other into the gap between the two trucks, smiling,
eyes locked. They meet at the centre, he cups her cheek and they share a tender romantic kiss.
Golden sparkles rise around them and a soft warm glow grows, brightening the frame.

Keep both faces identical. Bride: bright red hair. Groom: bald with a full beard. The rigs
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
- **Riesgo del tráiler completo:** de perfil el rig es larguísimo y en 9:16 las cajas se salen
  por los lados, dejando a los novios diminutos. Si pasa, quitar `and their TRAILERS attached`
  y dejar sólo el tractor — la referencia que funcionó era sin caja.
- El **fundido final a blanco** lo pongo con ffmpeg al unir los clips; empalma exacto con el
  fondo champán de la invitación.

## Cuando estén los clips

Dejarlos en Descargas y avisarme. Los uno en `escena.mp4` (720×1280, H.264) con
cross-dissolve y fundido a blanco, y reemplazo el actual.
