# Prompts de Flow — escena de los camiones (Raiza & Orlando)

Un prompt para el **clip 1**. El **clip 2** sale del último frame del clip 1 (*Frames to
Video*) con un prompt corto. Animación 3D, vertical 9:16, 8 s.

**Ajustes en Flow:** 9:16 vertical (seleccionarlo, el prompt solo no basta) · 8 s ·
*Ingredients to Video* con `novia.png` y `novio.png`.

**Negative prompt:**

```
trucks facing the viewer, trucks side by side, giant truck, long sleeper cab, trailer, bus,
van, character on the hood, character on the bumper, floating people, photorealistic, live
action, real people, horizontal composition, black bars, text, watermark, extra fingers,
blurry, shaky camera
```

---

## CLIP 1 — un solo prompt

```
Vertical 9:16. Charming 3D animated film style, like a modern animated feature — stylized and
rendered, never photorealistic. Warm golden light, champagne-cream and soft silver palette,
sage foliage and flowers hanging from the top of the frame.

Camera static AT THE EDGE OF THE ROAD, level with the trucks, so we see them from the side.

Two MEDIUM white trucks with chrome grilles and short day cabs (no sleeper box, no trailer).
The LEFT truck enters from the left edge with its FRONT BUMPER POINTING RIGHT. The RIGHT
truck enters from the right edge with its FRONT BUMPER POINTING LEFT. They drive straight at
each other and brake, until THE TWO FRONT BUMPERS ALMOST TOUCH IN THE EXACT CENTRE OF THE
FRAME, headlights aimed at each other, one metre apart. They are head to head, not parallel,
not side by side.

Then the cab door facing the camera on each truck swings open. Only after the door is open
does a character appear, standing in the open doorway on the step, and climbs down to the
road: from the left truck a BRIDE with long bright red hair, ivory satin wedding gown and
veil, holding a bouquet; from the right truck a GROOM, completely bald with a full dark
beard, in a cream suit and tie. Both doors stay open. They turn and look at each other.

Nobody ever appears on the hood, bumper, grille or roof. The door opens first, the person
appears second.
```

## CLIP 2 — desde el último frame del clip 1

```
Same scene, same characters, same medium white trucks parked in profile facing each other.

The BRIDE walks in from the left and the GROOM from the right, toward the centre, eyes on
each other, smiling. They meet face to face, he cups her cheek and they share a tender
romantic kiss. Silver and champagne sparkles rise around them and a soft warm glow grows
between them, brightening the frame.

Keep both faces identical. Bride: bright red hair. Groom: bald with a full beard. Nobody
climbs on the trucks.
```

---

## Notas

- **Por qué la cámara va al borde de la carretera:** es la única posición donde se ve el
  frente a frente de los camiones Y la puerta del costado. De frente a cámara las puertas
  quedan fuera de cuadro y la IA inventa la salida (en un intento sacó a los novios del cofre
  y de la parrilla).
- **Por qué "la puerta se abre primero":** sin esa frase los personajes se materializan.
- El **fundido final a blanco** lo pongo con ffmpeg al unir los clips; sale más limpio que
  pedírselo a Veo y empalma exacto con el fondo champán de la invitación.

## Cuando estén los clips

Dejarlos en Descargas y avisarme. Los uno en `escena.mp4` (720×1280, H.264) con
cross-dissolve y fundido a blanco, y reemplazo el actual.
