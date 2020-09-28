# notes-mobile-first

## responsive design

técnica de maquetado que tiene el objetivo de desarrollar versiones _adaptables_ de los sitios/apps a diferentes resoluciones (tablet, mobile, etc) sin necesidad de tener que invertir en aplicaciones nativas o tener que diseñar diferentes versiones.

- flexbox
- grids
- responsive images
- media-queries

Hoy en día el diseño responsive no es un plus, es un _requisito_.

### ventajas

- se reducen mucho los tiempos y costos de implementación
- evitar tener _al menos_ dos versiones de un sitio, uno mobile y otro desktop, ahorrando así tiempo en mantenimiento y simplificando mucho la base de código, ya que reutilizamos el HTML y gran parte del CSS.
- mejoras a nivel **UX**: le damos una mejor experiencia a les usuaries que navegan nuestro sitio desde mobile, sin necesidad de desarrollar aplicaciones nativas (+ complejidad, costo y tiempo)

## mobile-first

_tendencia_ dentro del diseño responsive, en la que **primero pensamos el diseño/layout para mobile y luego lo vamos adaptando para resoluciones más altas** (tablet/desktop).

### ventajas

- mejor UX: **el tráfico mobile de los sitios supera al del resto de los dispositivos** (analytics: google analytics, plausible.io, simpleanalytics.com, https://umami.is/, fullstory/hotjar).
- favorece el SEO (Google) vs _desktop-first_.
- es más difícil simplificar una versión desktop a mobile que pasar de mobile a desktop. Diseñar para mobile suele ser más difícil, por lo que tomamos decisiones sobre qué contenido es el más importante al principio, ahorrando tiempo después.
- al cargar inicialmente sólo el CSS necesario para mobile, la carga del sitio es más rápida.

### cómo implementamos mobile-first

- **media-queries:** nos permiten setear diferentes condiciones basadas en [_breakpoints_](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries), a partir de las cuales aplicamos diferentes estilos (width, height, orientation, color-scheme, etc)
- **breakpoints:** es un 'punto' o condición determinada en la que el contenido/diseño de un sitio se va a adaptar de cierta forma, para mejorar la UX.

### breakpoints más comunes

[A Guide to Responsive Breakpoints ~ 2020](https://uxtricks.design/blogs/ux-design/responsive-design/)

### tips

- en mobile tenemos menos espacio (screen size) disponible para el contenido que queremos mostrar, por lo que nos fuerza a planificar mejor previamente (wireframing & prototyping) y **pensar cuáles son las _core features_ (mvp) que necesitamos**
- en mobile los requisitos de les usuaries pueden ser diferentes, en cuanto a contenido y ux (tmb tablets). De nuevo, cobra mucha importancia la planificación previa y pensar diferentes escenarios, no se trata simplemente de aplicar media queries para cmabiar la orientación de un layout, puede cambiar el contexto y el contenido.
- tener en cuenta que aplica la regla de la cascada a la hora se setear los diferentes breakpoints
- **cuidar la legibilidad del contenido**: si el texto se vuelve difícil de leer o se altera mucho el flujo/queda desalineado, agregar un breakpoint para cambiar el tamaño y optimizar las tipografías para la lectura
  - es preferible usar `rem` a `em` para trabajar con textos.
- usar herramientas de _analytics_ para tener insights y métricas sobre qué resoluciones deberíamos priorizar, testear en las mismas y si es necesario, agregar los breakpoints correspondientes.
- en mobile, testear tmb en landscape, no sólo en vertical.
- una técnica común es mostrar/ocultar ciertos elementos en ciertos breakpoints.
- **usar imágenes de menor resolución para mobile.**
  - UX tmb implica que el sitio cargue rápido (performance), PNGs y JPGs escalan en cuanto a tamaño, pero el filesize se mantiene. Lo mejor es usar diferentes versiones de las mismas imágenes, según el target.
  - usando SVGs cuando sea posible (ej: íconos) evitamos la necesidad de múltiples versiones de la misma imagen
- **asegurarse de que los botones son fáciles de usar en mobile.**

### mobile-friendly tests

- usar las dev tools del browser para testear en diferentes resoluciones.
- https://bluetree.ai/screenfly/
- https://responsively.app/
