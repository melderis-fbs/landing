# Landing pre-llamada · Founders · Business Strategists

Página de "prepará tu llamada" en un único archivo HTML autocontenido, lista para
pegar en un bloque **Custom Code / HTML** de GoHighLevel.

## Identidad aplicada

Los tokens salen de `synoma/index.html`, así que la página es coherente con el resto
del ecosistema Founders.

| Token | Valor | Uso |
|---|---|---|
| `--black` | `#111111` | Fondo de secciones oscuras, botones, titulares sobre claro |
| `--ink` | `#1c1c1c` | Texto de cuerpo sobre fondo claro |
| `--carbon` | `#191919` | Fondo de tarjetas sobre negro |
| `--paper` | `#FAFAF8` | Fondo de la sección de vídeos pre-llamada |
| `--cream` | `#F2EEE9` | Fondo de casos de éxito y CTA final |
| `--beige` | `#C4B49A` | Acento principal (sobre fondo oscuro) |
| `--beige-d` | `#A8946F` | Acento sobre fondo claro (contraste) |
| `--border` | `#E6E1DA` | Bordes de tarjetas claras |

**Tipografía:** Inter 400–900, cargada desde Google Fonts.
**Formas:** botones y badges en pill (`border-radius: 99px`), tarjetas a 18px,
kickers en mayúscula beige con `letter-spacing: .28em` — igual que en Synoma.

## Estructura

1. **Header** sticky con logo centrado.
2. **Hero** negro: kicker con punto pulsante, titular en mayúsculas con destacado beige,
   subtítulo y **player principal** con overlay "hacé click para escuchar" y control de
   velocidad (1x → 2x).
3. **Marquee** beige a sangre con las frases de prueba social.
4. **"Algunas preguntas frecuentes respondidas"** sobre fondo papel: grid de
   **7 vídeos numerados 01–07** en 16:9, con título y bajada.
5. **Bloque demo** sobre negro: titular a dos pesos y vídeo ancho tipo grabación de pantalla.
6. **"+280 personas trabajando con nosotros"** sobre crema: grid de **vídeos verticales 9:16**
   con badge "Activá el sonido".
7. **Testimonios en tarjeta** sobre negro: marco beige interior, comillas grandes en outline,
   captura de WhatsApp/Instagram (o cita escrita con resaltado beige), foto circular,
   nombre y 5 estrellas.
8. **CTA final** sobre crema con checklist de preparación y botón al calendario.
9. **Footer**.

## Cómo montarla en GHL

1. Subí tus assets a **Settings → Media Library** de GHL y copiá cada URL.
2. Abrí `index.html` y reemplazá los placeholders (están todos en MAYÚSCULAS y con
   comentarios `<!-- REEMPLAZAR: ... -->` encima):

   | Placeholder | Qué va |
   |---|---|
   | `URL_LOGO_FOUNDERS_BLANCO.png` | Logo en blanco (aparece 2 veces: header y footer) |
   | `URL_VIDEO_PRINCIPAL.mp4` / `URL_POSTER_VIDEO_PRINCIPAL.jpg` | Vídeo del hero |
   | `URL_VIDEO_01..07.mp4` / `URL_POSTER_01..07.jpg` | Los 7 vídeos pre-llamada |
   | `URL_VIDEO_DEMO.mp4` / `URL_POSTER_DEMO.jpg` | Grabación de pantalla del proceso |
   | `URL_VIDEO_WIN_01..06.mp4` / `URL_POSTER_WIN_01..06.jpg` | Testimonios verticales |
   | `URL_CAPTURA_TESTIMONIO_01..02.jpg` | Capturas de WhatsApp/Instagram |
   | `URL_FOTO_PERSONA_01..04.jpg` | Fotos de perfil de los testimonios |
   | `URL_CALENDARIO_GHL` | Link del calendario / confirmación |

3. En el editor de la página, insertá un elemento **Custom Code (HTML)** a ancho completo
   y pegá el archivo entero.
4. En **Page Settings → Custom CSS** conviene añadir esto para que GHL no meta sus propios
   márgenes ni fondos blancos alrededor del bloque:

   ```css
   body, .hl_page-preview--content { background: #111111 !important; }
   .c-section, .c-row, .c-column { padding: 0 !important; margin: 0 !important; }
   ```

5. Publicá y revisá en móvil: los grids bajan a 1 columna por debajo de 560–768px.

## Notas de implementación

- **Embeds externos.** Si los vídeos están en Loom, Vimeo o YouTube en lugar de MP4 propios,
  borrá la etiqueta `<video>` y pegá el `<iframe>` del embed dentro del mismo contenedor
  (`.qa-media`, `.demo-frame`, `.win-media`). El contenedor ya fija la relación de aspecto,
  así que el iframe se adapta solo. Al hacerlo se pierden el badge de sonido y el control
  de velocidad, porque son reproductores ajenos.
- **Un vídeo a la vez.** El script pausa cualquier otro vídeo cuando arranca uno nuevo.
- **Autoplay con sonido.** Los navegadores lo bloquean, por eso el hero arranca en mute con
  overlay y los verticales llevan el badge "Activá el sonido". Es el mismo patrón de las
  referencias.
- **Secciones a sangre.** La clase `.bleed` estira cada sección a `100vw` aunque GHL la
  envuelva en un contenedor con `max-width`. Requiere `overflow-x: hidden` en `body`,
  que ya está puesto.
- **Marquee.** Las frases están duplicadas a propósito: la animación desplaza `-50%`, así que
  las dos mitades tienen que ser idénticas para que el bucle no dé saltos.
- **Añadir o quitar tarjetas.** Duplicá el bloque `<article>` correspondiente. Los grids son
  `repeat(2, 1fr)` en preguntas y testimonios, y `repeat(3, 1fr)` en casos de éxito.
