# Diseño — guía para ChatGPT

Esta carpeta es el espacio de diseño. Claude Code convierte lo que hay aquí en la web, así que **todo lo que entregues
tiene que estar en un formato que se pueda aplicar directamente**.

## Punto de partida

- Web actual del cliente (solo como referencia de marca, no hay que copiarla): https://transfersvipluxe.com
  Usa cabecera negra, barra azul, fotos de vehículos Mercedes y de la Costa Dorada.
- Logos disponibles en `marca/`:
  - `vip-luxe-icono-512.jpg`: icono cuadrado azul «VIP LUXE» con un coche (512 × 512 px).
  - `tvl-escudo-blanco.png`: escudo blanco «TVL VIP TRANSFERS · Costa Dorada», para fondos oscuros.
- Tono: traslados privados **de lujo pero cercanos**, para turistas y familias (Salou, Cambrils, PortAventura,
  aeropuertos de Reus, Barcelona y Girona, estación del AVE).

## Qué necesitamos (por orden)

1. **`estilo.md`**: la guía de estilo.
   - Colores en hexadecimal con su uso (principal, secundario, fondo, texto, éxito, error…).
   - Tipografías de Google Fonts (títulos y texto) con tamaños y pesos.
   - Radios de esquinas, sombras, espaciado y estilo de botones, tarjetas y formularios.
2. **Logos en vectorial** (`marca/*.svg`): redibujar en SVG el icono «VIP LUXE» y el escudo TVL, en versión para
   fondo claro y para fondo oscuro, más un favicon.
3. **Maquetas** (`maquetas/*.png`, ancho 1440 px escritorio y 390 px móvil) de:
   - Inicio con el formulario de reserva.
   - Pasos de la reserva: trayecto → vehículo y extras → datos → pago → confirmación.
   - Packs y excursiones (listado y ficha de un pack).
   - Guía turística (listado y artículo).
4. **Imágenes** (`imagenes/`, en WebP, 1600 px de ancho como máximo): portada, vehículos, packs (PortAventura,
   bodegas, minas, playas…). Apunta en `imagenes/ORIGEN.md` de dónde sale cada una (generada, del cliente o con
   licencia comercial).
5. **Iconos** de servicios y extras (silla de bebé, silla de ruedas, mascota, maletas, parada intermedia…) en SVG.

## Cómo entregar

- En una rama `diseno/<tema>` y con una pull request contra `main`.
- Nombres de fichero en minúsculas, sin espacios ni acentos (`portada-salou.webp`).
- Si no puedes subir ficheros a GitHub, entrégalos a Oscar y él los pasa al repositorio.
