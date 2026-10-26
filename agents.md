# Guía de agentes y colaboración

## Objetivo
Crear en equipo un prototipo visual, responsive y funcional para la tienda online de una marca francesa de ropa. El alcance es un prototipo de frontend, sin backend ni pagos reales.

## Restricciones técnicas
- Usar únicamente HTML5 semántico y Tailwind CSS v3 o superior, mediante CDN o CLI.
- No usar React, Vue, Angular, Svelte, otros frameworks ni dependencias JavaScript externas.
- Usar JavaScript vanilla mínimo solo cuando sea imprescindible para interacciones del prototipo, como el menú móvil, el carrito o los pasos del checkout.
- Mantener las cinco vistas requeridas: Home, Catálogo, Producto, Carrito y Checkout.
- Asegurar el comportamiento responsive con utilidades de Tailwind (`sm:`, `md:`, `lg:`, `xl:`).
- Seguir `design.md` como fuente de verdad para estilos y componentes. Si aún no existe, acordar el sistema visual antes de crear estilos propios.

## Roles principales

### 1. Frontend e integración
- Define la estructura de archivos, las convenciones HTML y el esqueleto común de las páginas.
- Mantiene consistentes la navegación, el encabezado y el pie de página en las cinco vistas.
- Integra el trabajo de los demás y resuelve conflictos de estructura o estilos compartidos.
- Comprueba que el marcado siga las restricciones técnicas y el sistema visual acordado.

### 2. Experiencia de descubrimiento: Home y Catálogo
- Implementa las vistas Home y Catálogo, incluyendo navegación hacia productos y categorías.
- Construye las cuadrículas, tarjetas y controles de catálogo con clases responsive de Tailwind.
- Mantiene consistentes la presentación de productos y los patrones de interacción acordados con el equipo.

### 3. Experiencia de compra: Producto y Carrito
- Implementa las vistas Producto y Carrito, incluidos estados vacíos y contenido de ejemplo.
- Conecta las acciones de añadir al carrito, cambiar cantidades y eliminar productos usando solo JavaScript vanilla mínimo cuando sea necesario.
- Mantiene visible y coherente el resumen de compra y el acceso al checkout.

### 4. Checkout, accesibilidad y calidad
- Implementa el Checkout en tres pasos y sus estados de avance, formularios y validaciones básicas de prototipo.
- Revisa de forma transversal la accesibilidad, la semántica y el SEO de las cinco vistas.
- Comprueba el flujo completo desde el catálogo hasta la confirmación simulada, además de los estados responsive y vacíos.
- Registra defectos y coordina su corrección con la persona responsable de cada vista.

## Criterios compartidos de calidad
- Usar un único `<h1>` por página y una jerarquía lógica de encabezados.
- Preferir etiquetas semánticas como `<header>`, `<nav>`, `<main>`, `<section>`, `<article>` y `<footer>`.
- Añadir textos `alt` descriptivos a las imágenes y etiquetas accesibles a controles, menús e inputs.
- Incluir metadatos básicos por página y etiquetas Open Graph apropiadas para el prototipo.
- Probar las cinco vistas en tamaños móvil y escritorio; comprobar también navegación, carrito y flujo de checkout.
- Mantener las clases de Tailwind legibles y explicar brevemente las decisiones de layout no evidentes en las entregas.

## Coordinación
- Cada persona es responsable de la implementación de las vistas asignadas; las revisiones transversales no trasladan esa propiedad.
- Acordar primero cualquier cambio en navegación, pie de página, estilos globales o convenciones compartidas.
- Antes de integrar, verificar que los enlaces entre vistas funcionen y que no se hayan añadido frameworks o dependencias no permitidos.
- Si una interacción requiere JavaScript, mantenerla pequeña, sin dependencias y limitada al comportamiento necesario para demostrar el flujo.