# Requisitos de la web de reservas

Contratado por TVL VIP Transfers el 07/11/2026: **solo la web de reservas** (el centro de control y la app del
conductor quedan para más adelante). Plazo comprometido: **10 días o menos**.

## Funciones

| # | Función | Notas |
|---|---|---|
| 1 | Web con la imagen de TVL en **6 idiomas**: es (por defecto), ca, en, de, fr, ru | Enlazada desde transfersvipluxe.com |
| 2 | **Reserva** con cálculo de ruta y **precio al momento** | Origen, destino, fecha y hora, pasajeros, maletas, vehículo, vuelo |
| 3 | **Tarifas** por trayecto o zona y por tipo de vehículo (sedán, monovolumen, minibús) | Las fija TVL |
| 4 | **Extras con precio**: silla de bebé, silla de ruedas, mascota… | Configurables sin tocar código |
| 5 | **Parada intermedia** con su coste | P. ej. aeropuerto → oficina de llaves → alojamiento |
| 6 | **Clientes habituales**: al escribir el teléfono se rellenan sus datos | Con consentimiento (RGPD) |
| 7 | **Capacidad**: máximo 30 servicios al día; la web deja de aceptar reservas ese día | |
| 8 | **Pago con tarjeta (Stripe)**, con reembolso al cancelar | Cuenta de Stripe a nombre de TVL, **en modo de pruebas** hasta que TVL decida activarla |
| 9 | **Reservas del mismo día** (mínimo 15 min de antelación): solo efectivo y aviso inmediato al responsable | |
| 10 | **Avisos de cada reserva al responsable por correo y WhatsApp**; confirmación al cliente por correo | No hay centro de control: las reservas llegan así |
| 11 | **Packs y excursiones**: información y venta (PortAventura desde el hotel, bodegas, minas…), con reserva y pago | |
| 12 | **Guía turística** de la Costa Dorada (playas, parques, pueblos, gastronomía) | Para atraer visitas de Google |
| 13 | **SEO**: velocidad, móvil, textos, etiquetas, datos estructurados, mapa del sitio, ficha de Google, en los 6 idiomas | |
| 14 | Páginas legales: aviso legal, privacidad y cookies | RGPD |

## Decisiones técnicas

- **Base de datos**: hace falta una pequeña (tarifas, extras, packs, clientes habituales, recuento diario de reservas,
  estado del pago). Supabase Pro, incluida en el mantenimiento.
- **Servidor**: VPS Hostinger KVM 2 contratado por TVL.

## Pendiente de decidir con TVL

- Dirección de la web nueva (p. ej. `reservas.transfersvipluxe.com`).
- Tarifas reales, lista de extras con precios y lista de packs.
- WhatsApp: número que recibe los avisos y si se usa la API oficial de WhatsApp Business (coste por mensaje) o un
  aviso más sencillo.
- Textos legales (razón social, NIF y dirección de TVL).
