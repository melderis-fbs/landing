# Capturas de social proof

Acá van las 30 capturas que se muestran en el mosaico de `index.html`.

## Nombres

Numeradas de `01` a `30`, con cero delante en las de un dígito:

```
01.jpg  02.jpg  03.jpg  …  29.jpg  30.jpg
```

La extensión puede ser `.jpg`, `.png` o `.jpeg` indistintamente: la página prueba las tres,
así que no hace falta convertir ni renombrar nada más allá del número.

## Cómo se sirven

Desde el CDN de jsDelivr, que lee este repo directamente:

```
https://cdn.jsdelivr.net/gh/melderis-fbs/landing/assets/social-proof/01.jpg
```

No hay que subirlas a la Media Library de GHL ni copiar URLs de a una.

Dos cosas a tener en cuenta:

- **Caché.** jsDelivr cachea la rama por varios días. Si reemplazás una imagen por otra con
  el mismo nombre, puede seguir viéndose la vieja un tiempo. Para forzar la actualización,
  subila con otro número.
- **El repo tiene que seguir siendo público.** Si pasa a privado, el CDN deja de servir las
  imágenes y el mosaico queda vacío.

## Peso

Conviene que cada captura no pase de ~300 KB. Son capturas de pantalla, así que con
1080 px de ancho sobra. Treinta imágenes de 300 KB son 9 MB en total, pero como todas
cargan de forma diferida el visitante sólo baja las que ve.
