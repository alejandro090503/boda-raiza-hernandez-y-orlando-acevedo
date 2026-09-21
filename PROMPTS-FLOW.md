# Prompts de Flow — escena de los camiones (Raiza & Orlando)

Basado en el clip que sí funcionó (`Bride_and_groom_exiting_trucks_...145957.mp4`): los
camiones vienen **de frente hacia la cámara** por la carretera, uno por carril, y las puertas
se abren **hacia nosotros**. Eso es lo que hace que la bajada se vea natural.

**Ajustes en Flow:** 9:16 vertical (seleccionarlo, el prompt solo no basta) · 8 s ·
*Ingredients to Video* con `novia.png` y `novio.png`. El clip 2 sale del último frame
(*Frames to Video*).

**Negative prompt:**

```
trucks in profile, side view of truck, trucks facing each other, giant truck, long sleeper
cab, trailer, bus, van, character on the hood, character on the bumper, floating people,
photorealistic, live action, real people, horizontal composition, black bars, text,
watermark, extra fingers, blurry, shaky camera
```

---

## CLIP 1 — un solo prompt

```
Vertical 9:16. Warm watercolour storybook illustration, hand-painted and charming, never
photorealistic. Cream and gold background, white blossoms and green leaves hanging from the
top of the frame, golden sparkles floating in the air.

CAMERA: low, at road level, looking STRAIGHT DOWN THE ROAD toward the horizon. The road
recedes to a vanishing point with dashed yellow centre lines.

Two MEDIUM vintage cream-and-white trucks — round headlights, chrome grille, short day cab,
two chrome exhaust stacks, no trailer — drive TOWARD THE CAMERA from the far distance, one in
each lane, SIDE BY SIDE, their fronts facing us. They roll closer and stop near the camera,
filling the lower half of the tall frame.

Then BOTH CAB DOORS SWING OPEN OUTWARD TOWARD THE CAMERA. Only after the doors are open do
the characters appear, each standing in their open doorway on the step: in the LEFT truck a
BRIDE with long bright red hair, ivory satin gown and veil, holding a bouquet; in the RIGHT
truck a GROOM, completely bald with a full dark beard, in a cream suit and tie. Each steps
down onto the road, doors still open on either side of them, and they turn to look at each
other.

The doors open FIRST, the people appear SECOND. Nobody ever appears on the hood, bumper,
grille or roof.
```

## CLIP 2 — desde el último frame del clip 1

```
Same scene, same characters, same two cream trucks with their doors open.

The BRIDE and the GROOM walk toward each other into the gap between the two open doors, eyes
on each other, smiling. They meet face to face, he cups her cheek and they share a tender
romantic kiss. Golden sparkles rise around them and a soft warm glow grows between them,
brightening the frame.

Keep both faces identical. Bride: bright red hair. Groom: bald with a full beard. Nobody
climbs on the trucks.
```

---

## Notas

- **Por qué de frente a cámara y no de perfil:** era mi error. De perfil los camiones se
  topan entre ellos pero la bajada queda de lado y la IA la resuelve mal. De frente, con las
  puertas abriéndose hacia el espectador, la salida se lee perfecto — es justo lo que pasa en
  el clip que ya salió bien.
- **Por qué "las puertas se abren primero":** sin esa frase los personajes se materializan.
- El **estilo del prompt es acuarela**, copiado del clip que funcionó. Si lo quieres en 3D,
  cambia sólo la primera línea por: `Vertical 9:16. Charming 3D animated film style, like a
  modern animated feature — stylized and rendered, never photorealistic.`
- El **fundido final a blanco** lo pongo con ffmpeg al unir los clips; empalma exacto con el
  fondo champán de la invitación.

## Cuando estén los clips

Dejarlos en Descargas y avisarme. Los uno en `escena.mp4` (720×1280, H.264) con
cross-dissolve y fundido a blanco, y reemplazo el actual.
