# Raiza Hernandez & Orlando Acevedo · 11 de octubre de 2026

Invitación digital (HTML estático + GSAP) para la celebración de la unión civil de
**Raiza & Orlando** — Restaurante Columbia, Celebration, Florida.

- **URL:** https://boda-raiza-hernandez-y-orlando-acevedo.vercel.app
- **Base:** clon de `boda-carolina-y-alfonso`, repintado a la paleta del cliente
  (champán `#F7E7CE`, sage green `#a8b8a9`, plata `#C0C0C0`).

## Estructura

Todo vive en `index.html` (markup + CSS + JS). No hay build: Vercel sirve la carpeta tal cual
(`vercel.json` con `outputDirectory: "."`).

| Archivo | Uso |
|---|---|
| `sobre.jpg` / `sobre.mp4` | Sobre del cliente: champán con sello de cera sage "R&O" (8 s) |
| `escena.mp4` | Escena del cliente en video (10 s): los camiones entran de costado por ambos lados y quedan encarados, bajan los novios, caminan al centro y se besan; funde a blanco |
| `novia.png` / `novio.png` | Personajes ilustrados de la escena de los camiones |
| `camion-novia.png` / `camion-novio.png` | Los dos camiones del respaldo GSAP: Peterbilt 389 bobtail repintado champán y sage (el modelo que pidió el cliente) |
| `hero-bg.jpg`, `bg-floral-1..5.jpg` | Fondos botánicos del cliente (sep 2026): marco de rosas blancas con hojas plateadas sobre champán, follaje colgante, marcos dorados y arco de jazmín. Siempre por reducción desde la fuente (nunca ampliados, o se ven borrosos) |
| `bg-sage-2.jpg` | Único fondo de la tanda anterior que se conserva: el del código de vestimenta |
| `symphony.woff` | Symphony Pro, la caligráfica de los nombres y los títulos (tomada de `boda-victoria-y-eduardo`) |
| `venue-1.jpg` / `venue-2.jpg` | Restaurante Columbia (exterior / interior) |
| `caballero.png` / `dama.png` | Figuras del código de vestimenta |
| `og.jpg` | Open Graph 1200×630 — encuadre cerrado al sobre y al sello |

## Escena de los camiones

Pedido explícito del cliente. Corre entre el video del sobre y la invitación.

`startBusScene()` reproduce **`escena.mp4`** (un solo clip generado en Flow, con fundido
final a blanco anadido con ffmpeg). Si el video no puede reproducirse — autoplay
bloqueado, 404, codec — cae a `startBusSceneFallback()`, la misma escena animada con GSAP
y PNGs (`novia.png`, `novio.png`, `camion-*.png`).

Botón **Saltar** y tres redes de seguridad para que la invitación aparezca siempre:
`setTimeout(hand, 12500)` (mayor que los 10 s del video), el respaldo GSAP, y dentro de
`dismissLoader()` un `setTimeout(initMain, 1800)` por si `requestAnimationFrame` se congela
y el `onComplete` de GSAP nunca corre.

## Música

El mp3 **nunca** va en el repo: se sirve desde Supabase Storage con `preload="none"`.

```
https://bsjoelxktbvlavfoozhk.supabase.co/storage/v1/object/public/fotos-clientes/audio/boda-raiza-hernandez-y-orlando-acevedo/cancion.mp3
```

## Tipografía y adornos

Basados en `boda-victoria-y-eduardo`, que es la referencia de "elegante" que pidió la novia:

- **Cinzel** (Google Fonts) para la estructura — rótulos, datos, cuerpo. Grabada y en
  versalitas; reemplazó a Cormorant Garamond.
- **Symphony Pro** (`symphony.woff`) **solo en los rótulos decorativos grandes**: nombres
  del hero, títulos de sección, título del RSVP, dress code y el pie. Ningún dato que el
  invitado tenga que leer va en caligrafía — la novia pidió expresamente corregirlo
  ("ni yo las leo... va a haber mucha gente más adulta"). Por eso la fecha del Save the Date,
  las horas del itinerario, el "pm" y la frase de la lluvia de sobres están en Cinzel.
- Cinzel no tiene cursiva real, así que se retiró `font-style:italic` de todo lo que quedó
  en Cinzel — la cursiva sintética sale torcida.
- **Adornos nupciales**: cuatro separadores SVG (corazón con vid, tulipán, hojas, rizos),
  simétricos por espejo, en lugar de las `.gline`. Heredan el color con `currentColor`.

## Secciones traídas de otras invitaciones

| Sección | Base | Nota |
|---|---|---|
| Código de vestimenta | `boda-fabiola-y-fernando` | Figuras caballero/dama + círculos de colores a evitar |
| Lluvia de sobres | `boda-jeffersson-y-vanessa` | Sobres que caen; uno aterriza al entrar la sección y se abre al tocarlo. Sello R&O en sage |

La galería se eliminó a pedido de la novia: no tienen sesión de fotos todavía y la quiere para
la boda religiosa del año que viene. La card de "Cena" que estaba en regalos se eliminó; el dato de las bebidas pasó al
itinerario, bajo la Cena de las 7:30.

## Ubicación

Además del botón "Cómo llegar" con pin, la tarjeta de la ceremonia lleva el **mapa embebido**
a la vista (`maps.google.com/maps?q=...&output=embed`, sin API key, `loading="lazy"`): la novia
no encontraba el enlace.

## RSVP

Confirmaciones vía [panel-invitados.vercel.app](https://panel-invitados.vercel.app).
Sin WhatsApp. Cada invitado abre `?para=Nombre&pases=N`. Fecha límite: 25 de septiembre de 2026.

## Pendientes

- Padres de los novios y padrinos (hoy "Por confirmar").
- Link real del álbum compartido para el QR.
- Fotos reales de la pareja (la galería usa las ilustraciones).
