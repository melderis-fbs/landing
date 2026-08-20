# Portadas de los vídeos de Loom

Los 7 vídeos pre-llamada y el de bienvenida buscan su portada **acá primero**. Es la vía
fiable: el archivo lo controlamos nosotros, no depende de que Loom exponga nada.

## Nombres

Uno por vídeo, con el número que tiene en la página:

```
hero.jpg   ← vídeo de bienvenida
01.jpg     ← ¿Qué es Founders y para quién es?
02.jpg     ← ¿Qué resultados consiguen, y cómo?
03.jpg     ← Un caso real, de principio a fin
04.jpg     ← ¿Y si no tengo tiempo para esto?
05.jpg     ← Ya invertí antes y no me funcionó
06.jpg     ← ¿No me conviene contratar una agencia?
07.jpg     ← ¿Esto va a ser una llamada de venta?
```

La extensión puede ser `.jpg`, `.png` o `.jpeg`, en minúscula o mayúscula: la página prueba
todas. Sólo importa el número.

## Cómo sacar la captura

1. Abrí el vídeo en Loom y pausalo en un fotograma donde se te vea bien.
2. Captura de pantalla del área del vídeo, sin los controles del reproductor.
3. Recortala a **16:9** y guardala con el nombre de arriba.

No hace falta que sea grande: 1280x720 alcanza y sobra.

## La alternativa sin capturas

Loom permite elegir la portada de cada vídeo desde su propio panel (en la configuración del
vídeo, "Thumbnail"). Si la definís ahí, la portada queda buena en Loom **y** puede empezar a
funcionar el camino automático de la página, sin subir nada a este repo. Vale la pena
probarlo antes de hacer las ocho capturas a mano.

## Orden en que la página busca

1. Esta carpeta, por CDN de jsDelivr.
2. El CDN de Loom, con tres patrones conocidos de nombre de archivo.
3. El oEmbed de Loom, que devuelve la URL correcta en un JSON (depende de que Loom permita
   la consulta desde otro dominio).
4. Si nada responde, la portada dibujada en CSS: degradado oscuro con brillo beige, filete
   interior, número, título y botón de play. Nunca queda un recuadro negro.
