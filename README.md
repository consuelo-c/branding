# Banquetes Consuelo C — Marca

La marca de **Banquetes Consuelo C**, una empresa de Medellín que alquila menaje y mobiliario para eventos: bodas, quinceañeros, fiestas empresariales. Lo que comparte cualquier producto de la empresa, para que todos se lean como la misma empresa: el logo, los colores, la fuente, la voz y la forma de los mensajes.

Este repositorio no sabe nada de los proyectos que lo usan. Cada proyecto copia los valores que necesita de [`tokens.json`](tokens.json) y los archivos de [`assets/`](assets/), y agrega sus propias reglas encima: las diagramaciones, los componentes, los tamaños y los espaciados son de cada proyecto.

**Un cambio de marca se hace primero aquí** y luego se copia a cada proyecto. Un proyecto nunca cambia un valor de marca por su cuenta.

## Contenido

- [`tokens.json`](tokens.json) — los colores, la familia tipográfica y sus pesos, y los radios y las sombras, cada uno con su uso
- [`assets/`](assets/) — los archivos del logo
- Este archivo — las reglas para usarlos

## Logo

- `assets/logo.svg` es el logotipo caligráfico «Banquetes Consuelo C», de 80×22 (3,6:1), totalmente trazado, con `fill=currentColor`. Es muy delgado, así que dale un tamaño mínimo y nunca lo pongas sobre amarillo.
- `assets/c-logo.svg` es la «C» ornamentada (14×17), con `fill=currentColor`. Representa la marca donde el logotipo no cabe, como en el ícono de una app: C blanca sobre #333, al 58 % de la altura.
- La caligrafía del logo es la fuente Flaemische Kanzleischrift (`flaemische-kanzleischrift-400-normal`, peso 400, estilo normal). Los SVG ya vienen trazados, así que no necesitas la fuente para usar el logo; sirve solo para rehacerlo o ampliarlo.
- Los `*-ink.svg` van rellenos de #333 y los `*-white.svg` de blanco, para donde no se puede usar `currentColor`.
- `assets/source/` guarda los SVG originales de la marca tal como se entregaron (`fill="black"`). Los demás archivos son los mismos trazos con otro color. No los redibujes.
- El logo nunca compone texto: la caligrafía es solo el logo.

## Color

- **Marca:** amarillo `#FFD313`, tinta `#333333`, blanco. Un solo esquema claro.
- **El amarillo nunca es texto sobre blanco** (1,5:1). Es un relleno, un borde o una línea. El texto sobre amarillo es tinta.
- **Texto oscuro sobre fondo claro, con alto contraste.** El texto principal es tinta sobre blanco; el secundario es `#6B6B6B`, nunca más claro. `#A3A3A3` es solo para texto deshabilitado.
- **Los neutros** van `#F7F7F7` / `#E5E5E5` / `#A3A3A3` / `#6B6B6B`, con `#1E1E1E` como la única superficie oscura.
- **Los pares semánticos** son texto sobre un relleno del mismo tono: éxito, advertencia, error e información (ver [Mensajes](#mensajes)). El ámbar de advertencia es a propósito más apagado que el amarillo de la marca, para que una advertencia nunca se lea como la marca.
- **Los enlaces** son `#1D4ED8`, y `#1B3FAE` al pasar el cursor.

## Tipografía

**Work Sans**, pesos 400, 500, 600 y 700, para todo el texto. Mayúscula inicial solo en la primera palabra para títulos, botones y etiquetas («Nuevo pedido», «Fecha del evento»); los títulos de documentos impresos van en MAYÚSCULAS («RECIBO DE CAJA»).

## Forma

Sombras en vez de bordes: una sombra suave (`0 1px 3px rgba(51, 51, 51, 0.12)`) es el contorno por defecto de las tarjetas, y una más marcada (`0 8px 24px rgba(51, 51, 51, 0.16)`) levanta lo que flota encima, como diálogos y menús. Los campos son la excepción: llevan un borde de 1,5px `#E5E5E5`, que se vuelve `error-fg` cuando el campo no es válido. Las esquinas son redondeadas, desde 6px en controles pequeños hasta 16px en diálogos, con píldoras a 20px; los valores son los radios y las sombras de `tokens.json`. Superficies planas: sin degradados ni texturas.

## Íconos

Un juego de íconos SVG en línea, de trazo, al estilo [Lucide](https://lucide.dev): retícula de 24, trazo de 2px, terminaciones y uniones redondeadas, `currentColor`. Sin fuentes de íconos, sin íconos PNG, sin emojis.

## Voz

- **Español colombiano.** Háblale de «tú» al lector («Puedes continuar igual»). Nunca «usted» ni «vos».
- **Sencilla y directa**, con las palabras que usa la empresa: *Separado, Recogida, Novedad, Menaje*. Sin relleno publicitario y **sin signos de exclamación**.
- **Los botones son verbo + objeto:** «Guardar pago», «Ver pedido».
- **Números:**
  - El dinero en COP, con punto de miles y sin decimales: $1.180.000. Los negativos usan un signo menos verdadero: −$104.000. Los precios ya incluyen todo; no hay línea de IVA.
  - Las horas «2:00 p.m.», nunca «2:00 p. m.».
  - Las fechas «vie 14 ago 2026», o «14 ago · 2:00 p.m.» con hora.
  - Los datos en una misma línea se unen con « · »: «Transferencia · 12 ago 2026».
- **Glifos, no emojis:** ✓ para hecho, ⚠ para una advertencia, × en «120 × Silla».

## Mensajes

Lo que un producto le responde a su usuario: una advertencia, un error, una confirmación, una nota.

### Los cuatro tipos

| Tipo | Cuándo | Texto sobre relleno |
| --- | --- | --- |
| Éxito | Algo se hizo | `#1B7F4B` sobre `#DCFCE7` |
| Advertencia | Algo no parece estar bien, y el usuario aún puede continuar | `#B45309` sobre `#FEF3C7` |
| Error | Algo bloquea: no se puede hacer hasta corregirlo | `#B3261E` sobre `#FEE2E2` |
| Información | Algo se explica, sin nada que corregir | `#1D4ED8` sobre `#DBEAFE` |

### Cómo se ven

- Texto sobre un relleno del mismo tono (`success-fg` sobre `success-bg`, y así con los demás): sin borde, sin sombra, esquinas `radius-md` (8px).
- Una advertencia puede empezar con ⚠. Ningún otro ícono ni emoji.
- El error de un campo va debajo del campo, en `error-fg`, y el borde del campo se vuelve `error-fg`.

### Cómo se escriben

- **Di qué pasó o qué hacer**, en una o dos frases cortas: «Revisa el número de celular», no «Error de validación».
- **Las advertencias aconsejan y lo dicen:** «⚠ Supera el inventario disponible. Puedes continuar igual.»
- **Las acciones irreversibles lo dicen sin rodeos:** «Los pagos no se pueden corregir después.»
- **Sin signos de exclamación**, ni siquiera en los de éxito: «Pedido guardado», no «¡Pedido guardado!».
- «Tú», como el resto de la voz.

<!-- vim: spelllang=es
-->
