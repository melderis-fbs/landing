# Identificación de los 7 vídeos pre-llamada

Tabla para reconocer cada archivo por su primera frase y pegar la URL cuando esté colgado.
El orden de la columna "Nº en la página" es el que aparece en `index.html`.

---

## 01 · ¿Qué es Founders y para quién es?

- **Línea de apoyo en la portada:** Mi historia y por qué existe esto
- **Arranca con:** «Hola, soy Vicky y hoy te voy a contar una historia que no cuento muy seguido.»
- **Duración aprox.:** 7:25 — es el más largo de los siete
- **Cómo lo reconocés:** la marca de ropa Bechi, la nota de Infobae, marzo de 2020, "tenía 24 años",
  y el bloque final de "Founders es para vos si… / Founders no es para vos si…"
- **Orden en que me lo mandaste:** 5º
- **Loom:** `2343363fe0f84add8d66d9ea8bdb2de1` — ya aplicado en `index.html`

## 02 · ¿Qué resultados consiguen, y cómo?

- **Línea de apoyo:** +80 casos documentados · ROD y APM
- **Arranca con:** «Hoy quiero hacer algo que no hago seguido, hablar de los resultados.»
- **Duración aprox.:** 5:10
- **Cómo lo reconocés:** los nombres Fer, Jessica, Trin, Pilar y Mauro, y la explicación de
  ROD (demanda orgánica reprimida) y APM (autoridad de posicionamiento en el mercado)
- **Orden en que me lo mandaste:** 6º
- **Loom:** `ce887e26bf134940b9009b4db30981ee` — ya aplicado en `index.html`

## 03 · Un caso real, de principio a fin

- **Línea de apoyo:** Alex: de vocación pura a negocio con estructura
- **Arranca con:** «Un tipo de profesional que me motiva profundamente a hacer esto…»
- **Duración aprox.:** 4:40
- **Cómo lo reconocés:** es el único con dos personas en cámara. Alex es profesora de inglés y
  coach de comunicación. Aparecen las tres preguntas que le hacés a todo el que llega
- **Orden en que me lo mandaste:** 2º
- **Loom:** `f295615ad1ad4a5893cbc9787a39f691` — ya aplicado en `index.html`

## 04 · ¿Y si no tengo tiempo para esto?

- **Línea de apoyo:** La paradoja más cara que existe
- **Arranca con:** «¿No tengo tiempo para construir el sistema que me daría tiempo?»
- **Duración aprox.:** 2:05 — el más corto
- **Cómo lo reconocés:** la nutricionista con lista de espera de tres meses, las 4 o 5 horas
  semanales que podía dedicarle, y las 15 horas semanales que el sistema le liberó
- **Orden en que me lo mandaste:** 1º
- **Loom:** `7129cf1c49e44b99ad81531705a1dbc2` — ya aplicado en `index.html`

## 05 · Ya invertí antes y no me funcionó

- **Línea de apoyo:** Por qué esta vez sería distinto
- **Arranca con:** «Si llegaste a nosotros habiendo invertido antes en algo que no te dio resultado…»
- **Duración aprox.:** 2:20
- **Cómo lo reconocés:** las cuatro categorías de por qué falló lo anterior (programa genérico,
  acompañamiento escaso, timing incorrecto, no ejecutaste) y **la garantía de los 4 meses**
- **Orden en que me lo mandaste:** 3º
- **Loom:** `3b3fb2c0aa03491f8c489a6239cbeaee` — ya aplicado en `index.html`

## 06 · ¿No me conviene contratar una agencia?

- **Línea de apoyo:** Primero una cosa, después la otra
- **Arranca con:** «Si estás evaluando contratar una agencia para hacer crecer tu negocio…»
- **Duración aprox.:** 3:10
- **Cómo lo reconocés:** el caso de María, consultora con 8 años de experiencia que pagó
  6 meses de agencia, y la imagen de "poner altavoces en una canción que todavía no terminaste
  de escribir"
- **Orden en que me lo mandaste:** 4º
- **Loom:** `d7b8d7db244a4c128f8d17d8333fa455` — ya aplicado en `index.html`

## 07 · ¿Esto va a ser una llamada de venta?

- **Línea de apoyo:** Cómo es el proceso desde el primer contacto
- **Arranca con:** «Algo que escucho seguido cuando hablo con alguien por primera vez es esto…»
- **Duración aprox.:** 5:25
- **Cómo lo reconocés:** habla de las estructuras de comisión, la "oferta que vence hoy",
  la falsa urgencia, y cierra con «si la primera conversación no te dejó algo valioso,
  fallamos nosotros como empresa, no vos»
- **Orden en que me lo mandaste:** 7º
- **Loom:** `a772db6d39cb4a44a7b4ff93f3a98e7b` — ya aplicado en `index.html`

---

## Hero · vídeo de bienvenida

Grabado y colgado. El hero también es una fachada: el reproductor de Loom se carga al hacer
click sobre el overlay "hacé click para escuchar".

- **Loom:** `2e26b0b914944987aa2770d0cf3af3f2` — ya aplicado en `index.html`

---

## Cómo pegar cada URL

En `index.html`, cada tarjeta está marcada con su número (`<!-- ── 01 ── -->`).

**Si el vídeo está en Loom** — añadí `data-loom` al div y borrá el `<video>`:

```html
<div class="qa-media" data-loom="a1b2c3d4e5f6">
```

**Si es un MP4 en la Media Library de GHL** — cambiale el `src` al `<video>`:

```html
<video preload="none" playsinline src="https://assets.cdn.filesafe.space/..."></video>
```

## Cómo nombrar los archivos en Drive

Para no volver a perderlos, conviene renombrarlos con el número de la página delante:

```
01-que-es-founders.mp4
02-resultados-rod-apm.mp4
03-caso-alex.mp4
04-no-tengo-tiempo.mp4
05-ya-inverti-antes.mp4
06-agencia.mp4
07-llamada-de-venta.mp4
```

---

## Testimonios · 10 vídeos de YouTube

No hacen falta miniaturas. El grid está en 16:9, que es exactamente la proporción de la
miniatura que genera YouTube, así que encaja sin recorte. Encima va una capa de marca en
HTML: velo degradado, botón de play beige, nombre y profesión.

Para cada uno hay que reemplazar tres cosas en `index.html`:

| Placeholder | Qué va |
|---|---|
| `ID_YOUTUBE_01..10` | Sólo el ID, lo que va después de `v=` o de `/shorts/` |
| `NOMBRE 01..10` + `Profesión` | Van sobre la portada, abajo a la izquierda |
| `«Frase corta que resuma su resultado.»` | Va debajo del vídeo |

Si algún testimonio fuera vertical, cambiá `aspect-ratio:16/9` por `9/16` en `.win-media`
— es una línea. Pero en ese caso la miniatura de YouTube sí se recorta y conviene una
portada propia en `data-poster`.
