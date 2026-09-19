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
| `sobre.jpg` / `sobre.mp4` | Sobre del cliente: champán con sello de cera sage "R&O" |
| `novia.png` / `novio.png` | Personajes ilustrados de la escena de los camiones |
| `camion-novia.png` / `camion-novio.png` | Los dos camiones (champán y sage) |
| `hero-bg.jpg`, `bg-sage-1..4.jpg` | Fondos botánicos: eucalipto acuarela sobre champán, siempre por reducción desde la fuente (nunca ampliados, o se ven borrosos) |
| `venue-1.jpg` / `venue-2.jpg` | Restaurante Columbia (exterior / interior) |
| `gal-1..4.jpg` | Galería ilustrada |
| `og.jpg` | Open Graph 1200×630 — encuadre cerrado al sobre y al sello |

## Escena de los camiones

Pedido explícito del cliente. Corre entre el video del sobre y la invitación
(`startBusScene()` en `index.html`): los dos camiones llegan de lados opuestos y se
estacionan de frente, bajan los novios, caminan al centro, se besan y un destello da paso
a la invitación. Tiene botón **Saltar** y dos redes de seguridad (GSAP + `setTimeout`) para
que la invitación siempre aparezca aunque `requestAnimationFrame` se congele.

## Música

El mp3 **nunca** va en el repo: se sirve desde Supabase Storage con `preload="none"`.

```
https://bsjoelxktbvlavfoozhk.supabase.co/storage/v1/object/public/fotos-clientes/audio/boda-raiza-hernandez-y-orlando-acevedo/cancion.mp3
```

## RSVP

Confirmaciones vía [panel-invitados.vercel.app](https://panel-invitados.vercel.app).
Sin WhatsApp. Cada invitado abre `?para=Nombre&pases=N`. Fecha límite: 25 de septiembre de 2026.

## Pendientes

- Padres de los novios y padrinos (hoy "Por confirmar").
- Link real del álbum compartido para el QR.
- Fotos reales de la pareja (la galería usa las ilustraciones).
