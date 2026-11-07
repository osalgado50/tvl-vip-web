# TVL VIP Transfers — web de reservas

Reglas compartidas para todas las IA que trabajan en este repositorio (ChatGPT/Codex y Claude Code) y para las
personas. **Léelo entero antes de tocar nada.**

## El proyecto

Web de reservas de **TVL VIP Transfers** (Transfers Vip Luxe, Salou, Costa Dorada): traslados privados y VTC.
La web corporativa actual, transfersvipluxe.com (WordPress), **no se toca**: esta web nueva se enlaza desde ella.

Alcance y decisiones: [docs/REQUISITOS.md](docs/REQUISITOS.md). Guía de diseño: [diseno/README.md](diseno/README.md).

## Quién hace qué

| Quién | Se encarga de | Trabaja en |
|---|---|---|
| **ChatGPT** | Diseño: estilo (colores, tipografías, espaciados), logos e iconos, fotografías e ilustraciones, maquetas de pantallas | `diseno/` |
| **Claude Code** | Código, textos SEO y traducciones, integraciones (Stripe, correo, WhatsApp), pruebas, despliegue | Todo lo demás |
| **Oscar (responsable)** | Aprueba y fusiona los cambios | Pull requests en GitHub |

- ChatGPT no cambia código; si una maqueta necesita algo de código, lo describe en la PR o en una tarea (issue).
- Claude no inventa diseño: aplica lo que hay en `diseno/`. Si falta algo, abre una tarea para ChatGPT.

## Cómo se trabaja

1. Cada cambio en **su propia rama**: `diseno/<tema>` (ChatGPT) o `codigo/<tema>` (Claude).
2. Se propone con una **pull request** contra `main`, explicando qué cambia y por qué. Si cierra una tarea, enlázala.
3. **Solo Oscar fusiona en `main`.** Lo que entra en `main` se publica automáticamente en la web: nunca empujes
   directamente a `main`.
4. Commits pequeños, con mensajes en castellano que digan qué cambia.

## Reglas fijas

- **Nada de claves, contraseñas ni datos personales reales** en el repositorio. Los secretos van en `.env` (ignorado);
  en el repo solo va `.env.example` con nombres de variables y valores vacíos.
- Idiomas de la web: **castellano (por defecto), catalán, inglés, alemán, francés y ruso**. Todo texto visible tiene
  que existir en los seis.
- Marca: logo «VIP LUXE» (icono azul) y escudo «TVL VIP TRANSFERS». No se cambia el logo sin aprobación de Oscar.
- La web tiene que ser rápida y funcionar perfectamente en el móvil (la mayoría de clientes reservan desde ahí).
- Accesibilidad básica: contraste suficiente, textos alternativos en las imágenes, formularios con etiquetas.
- Imágenes: solo propias de TVL, generadas para el proyecto o con licencia que permita uso comercial. Indica el origen
  en `diseno/imagenes/ORIGEN.md`.

## Técnica

- Next.js 15 (App Router) + TypeScript + Tailwind CSS 4. Node 20 o superior.
- `npm run dev` (desarrollo), `npm run build` (comprobación antes de cada PR), `npm run lint`.
- Despliegue: VPS de Hostinger de TVL.
