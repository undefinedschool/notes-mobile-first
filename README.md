# notes-mobile-first

## responsive design

técnica de maquetado que tiene el objetivo de desarrollar versiones _adaptables_ de los sitios/apps a diferentes resoluciones (tablet, mobile, etc) sin necesidad de tener que invertir en aplicaciones nativas o tener que diseñar diferentes versiones.

- flexbox
- grids
- responsive images
- media-queries

### ventajas

- se reducen mucho los tiempos y costos de implementación
- evitar tener _al menos_ dos versiones de un sitio, uno mobile y otro desktop, ahorrando así tiempo en mantenimiento y simplificando mucho la base de código, ya que reutilizamos el HTML y gran parte del CSS.
- mejoras a nivel **UX**: le damos una mejor experiencia a les usuaries que navegan nuestro sitio desde mobile, sin necesidad de desarrollar aplicaciones nativas (+ complejidad, costo y tiempo)

## mobile-first

_tendencia_ dentro del diseño responsive, en la que **primero pensamos el diseño/layout para mobile y luego lo vamos adaptando para resoluciones más altas** (tablet/desktop).

### ventajas

- mejor UX: **el tráfico mobile de los sitios supera al del resto de los dispositivos** (analytics: google analytics, plausible, simple analytics, https://umami.is/, fullstory/hotjar)
- favorece el SEO (Google) vs _desktop-first_

### cómo implementamos mobile-first

- media-queries: nos permiten setear diferentes condiciones basadas en [_breakpoints_](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries), a partir de las cuales aplicamos diferentes estilos (width, height, orientation, color-scheme, etc)

### tips

- tener en cuenta que aplica la regla de la cascada a la hora se setear los diferentes breakpoints
- usar las dev tools del browser
- responsiveley app
