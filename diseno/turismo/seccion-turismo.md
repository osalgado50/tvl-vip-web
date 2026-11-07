# Descubre la Costa Dorada — propuesta de sección

Estado: diseño para aprobación de Oscar. Fecha: 2026-11-07. Relacionado con #4; no cierra todavía las maquetas de artículos y fichas completas. Claude implementa y prepara las traducciones; Oscar aprueba y fusiona.

## Referencia visual y alcance

Referencia visual verificada: https://app.transfersvipluxe.com/ (2026-11-07). La versión publicada usa fondo azul noche, títulos Playfair Display, texto sans serif y acciones doradas. Se mantiene ese lenguaje visual y la prioridad del formulario. La sección se sitúa después de «Viaja tranquilo» y antes del pie, sin alterar el hero ni la reserva. La ilustración de la portada no se repite: la sección usa un fondo oscuro liso para dar descanso visual. El main de GitHub consultado está menos actualizado que esta versión publicada. No se cambia el logo ni el formulario.

Entregables: esta especificación, catálogo editorial en catalogo.md y maquetas PNG turismo-movil.png (390 px) y turismo-escritorio.png (1440 px). Las maquetas representan el resumen de inicio, no un catálogo completo ni una web funcional. Los textos son propuestas para diseño; Claude desarrolla los definitivos y las seis traducciones.

## Entrada y composición

En la navegación: «Descubre». En móvil, dentro del menú existente; no añadir una segunda barra. En inicio, después de «Viaja tranquilo», insertar un único bloque editorial. La reserva conserva prioridad.

Título: «Tu viaje empieza aquí».
Entradilla: «Playas, historia y planes en familia. Descubre la Costa Dorada y encuentra tu próximo destino.»

Orden de lectura:
1. «Lugares para descubrir»: cuatro tarjetas, Salou y Cambrils, Tarragona, PortAventura y Ferrari Land, Playas de la Costa Dorada. Enlace «Ver todos los lugares» hacia la guía turística.
2. «Del aeropuerto a tus vacaciones»: lista compacta de Reus, Barcelona-El Prat y Girona-Costa Brava; enlace adicional a Camp de Tarragona y Barcelona Sants. Lleida-Alguaire figura en el catálogo secundario, recuperado de la web anterior.
3. «Un servicio para cada viaje»: Familias y grupos; Hoteles y apartamentos; Empresas y congresos; Bodas y eventos. Resumen en dos columnas de texto, sin otra galería.
4. «Excursiones a tu ritmo»: dos tarjetas destacadas de ideas: Priorat y bodegas; Minas de Bellmunt. Enlace «Ver ideas de excursiones». En el catálogo completo añadir Tarragona, Siurana, Delta del Ebro y PortAventura con vuelta.
5. Cierre: «¿Tienes otro plan en mente?» / «Cuéntanos dónde quieres ir y prepararemos una propuesta de traslado.» / acción «Consultar mi viaje».

## Interacciones para Claude, expresadas sin código

- Lugar: «Descubrir» abre la ficha editorial; al final, «Organizar mi traslado» lleva al flujo de reserva con destino propuesto y editable. No tomar automáticamente el aeropuerto como origen.
- Aeropuerto o estación: «Reservar traslado» abre el flujo con ese punto como origen editable y permite invertir el sentido. No asociar terminales, horas ni disponibilidad sin datos.
- Servicios: «Consultar servicio» abre la consulta del servicio seleccionado. Solo usar reserva directa si existe tarifa y capacidad configuradas.
- Excursión propuesta: «Consultar excursión» inicia una solicitud, nunca el pago. Puede convertirse en pack reservable cuando TVL confirme itinerario, duración, precio, disponibilidad, inclusiones y cancelación.
- Excursión aprobada y configurada: «Ver excursión» abre ficha; «Reservar» solo cuando el catálogo y las integraciones estén operativos.
- No inventar enlaces activos, precios «desde», descuentos, reseñas, acuerdos con parques ni badges de disponibilidad.

## Diseño medible provisional

Paleta de continuidad con la web publicada, concretada para la sección: fondo #0B1020; cabecera y cierre #080D19; tarjetas #131A2D; títulos #FFFFFF; texto secundario #CBD5E1; bordes #334155; enlaces y acento #F5D565; botón #F5D565 con texto #0B1020; botón encima #FFE58A; foco #F5D565 con separación de 2 px y contorno de 3 px. Texto claro sobre oscuro y texto oscuro sobre dorado. Mantener las variables equivalentes existentes si Claude dispone del código desplegado. Los bordes decorativos no deben ser la única señal para identificar un control. No comunicar estados solo por color.

Títulos: Google Fonts Playfair Display, peso 700, como la web publicada. Texto y controles: Noto Sans 400/600 como propuesta de Google Fonts equivalente al sans serif existente, con soporte cirílico; mantener el sans serif existente si Oscar quiere continuidad exacta. No cambiar globalmente las fuentes desde esta tarea. Texto 16/26 px; etiquetas 14/20 px; botones 16/24 px. Título principal móvil 32/40 px, escritorio 44/54 px; sección 24/32 móvil y 30/40 escritorio; títulos de tarjeta 20/28 px. Playfair Display y Noto Sans deberán cargarse con cobertura cirílica al implementar.

Móvil 390 px: márgenes laterales 20 px, contenido 350 px; una columna, con dos tarjetas destacadas y dos enlaces compactos a los otros destinos; separación entre bloques 48 px, tarjetas 16 px; padding de tarjeta 20 px; fotos 350 × 180 px; controles de al menos 48 px de alto. No usar carruseles ni deslizamiento horizontal para acceder a contenido esencial. Los listados largos muestran un resumen y enlace al catálogo, sin ocultar contenido tras hover.

Escritorio 1440 px: contenido máximo 1200 px centrado, márgenes 120 px; cuatro destinos en columnas de 282 px con huecos de 24 px, fotos de 282 × 160 px. Aeropuertos y servicios comparten una franja de dos columnas; excursiones en dos columnas de 588 px. Padding vertical 64 px. Radios: tarjeta 12 px, foto 12 px arriba, botón 8 px. Sin sombras fuertes; el fondo de esta sección será liso y oscuro. El botón puede heredar el degradado dorado existente; las maquetas muestran su equivalente liso. Espaciado: 4, 8, 12, 16, 24, 32, 48, 64 px.

Tarjetas: altura según contenido; títulos y descripciones completos, sin truncar. En la misma fila, alinear acciones al pie. Normal: borde #334155; encima: borde #F5D565 sin mover la tarjeta; foco visible en la acción; no hacer la tarjeta entera clicable si contiene otras acciones.

## Seis idiomas y accesibilidad

Castellano, catalán, inglés, alemán, francés y ruso. Reservar expansión de texto de aproximadamente 40%; es margen de diseño, no garantía. Botones de alto mínimo, no fijo: admitir dos líneas. En móvil, todos los textos pueden crecer verticalmente; en escritorio reducir columnas antes que texto. Verificar alemán y ruso en la implementación. No fijar altura a tarjetas ni limitar títulos a dos líneas.

Las fotografías de destino tendrán alternativas descriptivas sin sobreprometer accesibilidad del lugar. Imágenes decorativas con alternativa vacía; encabezados jerárquicos, enlaces con propósito claro, navegación por teclado. Formularios con etiquetas persistentes y mensajes asociados. No afirmar que un vehículo está adaptado para silla de ruedas sin confirmación; distinguir transportar una silla plegada de llevar un pasajero en su silla.

## Imágenes

Las maquetas usan fotografías recuperadas de la web actual, solo como referencia de composición. Ver diseno/imagenes/ORIGEN.md: selección no equivale a acreditación de licencia. No convertir una foto genérica en prueba de un destino específico. PortAventura usa su imagen recuperada; Tarragona, el anfiteatro; la tarjeta general de playas, una playa de la galería antigua. Salou/Cambrils se ilustra con el paseo recuperado, sin identificarlo como Cambrils. Los packs nuevos llevan recuadros editoriales de texto hasta disponer de fotografías verificadas; no utilizar una playa como si fuera una bodega.

Conservar las tres imágenes Mercedes-Benz elegidas por el cliente en la sección de flota existente. No duplicarlas en cada tarjeta turística ni atribuir modelos, plazas o accesibilidad no confirmados.

## Límites comerciales

El área de partida es Salou, Cambrils y La Pineda. Tarragona, Reus, PortAventura y las conexiones aeroportuarias proceden de la web antigua. Priorat, Siurana, Bellmunt y Delta son propuestas geográficas plausibles de excursión desde esa base; no constituyen radio operativo, cobertura ni disponibilidad confirmados por TVL. Barcelona puede plantearse bajo consulta. No fijar kilómetros ni tiempos de carretera sin ruta y tráfico reales. No asumir guías, entradas, comidas, catas o espera del conductor incluidas.

## Criterios para aprobar e implementar

Oscar revisa composición y selección de propuestas; TVL confirma cobertura, servicios y condiciones. Claude incorpora los componentes existentes de la web nueva, textos definitivos y seis idiomas; conecta consultas y reservas con datos reales; comprueba 390 y 1440 px, teclado, expansión de texto y carga de imágenes. No publicar packs nuevos como comprables hasta su validación. Esta entrega no modifica código ni publica la web.
