# Task: Base Layout y Plantilla Común

> **Ubicación:** `specs/base-layout/task.md`
> **Contexto:** requisitos en `spec.md`, plan en `plan.md`. Este documento desglosa el plan en tareas sencillas con su verificación.
> **Estado:** ✅ completado — la plantilla y las 5 vistas están implementadas y verificadas (checklist a continuación marcado como completado).

## ✅ Tarea 1 — Estructura de carpetas
- [x] Crear `docs/reference/` (para `base.html`).
- [x] Confirmar que las 5 vistas irán en la raíz: `index.html`, `catalogue.html`, `product.html`, `cart.html`, `checkout.html`.
- [x] Definir nombres de archivo consistentes (todo en minúsculas, guiones para separar).

**Verificación:** La estructura `docs/reference/` existe y la lista de archivos de vistas está acordada.

## ✅ Tarea 2 — Metadatos y carga de Tailwind
- [x] Crear el `<head>` con charset y viewport.
- [x] Añadir `<title>` patrón, meta description y Open Graph (con placeholders).
- [x] Añadir la carga de Tailwind v4 por CDN (`@tailwindcss/browser@4`).

**Verificación:** Al abrir la vista se carga Tailwind sin build; el `<head>` incluye los metadatos mínimos del spec (sección 5).

## ✅ Tarea 3 — Navbar reutilizable
- [x] Crear `<header>` con logo y barra de búsqueda.
- [x] Añadir el menú `<nav>` con enlaces a las 5 vistas.
- [x] Añadir iconos de usuario, favoritos y carrito.
- [x] Aplicar colapso/ocultación responsive en móvil (`sm:`) y mostrar en escritorio.

**Verificación:** El navbar se ve correcto en móvil y escritorio; los enlaces apuntan a las 5 vistas; menú dentro de `<nav>`.

## ✅ Tarea 4 — Contenido principal vacío
- [x] Crear `<main>` sin contenido de negocio.
- [x] Dejar el punto de inserción del `<h1>` de cada vista documentado con comentario.

**Verificación:** El `<main>` está vacío y cada vista tiene espacio reservado para su `<h1>` único.

## ✅ Tarea 5 — Footer reutilizable
- [x] Crear `<footer>` con columnas de categorías (Calzado, Camisas, Pantalones, Accesorios).
- [x] Añadir links legales (Términos, Privacidad, Sobre la marca).
- [x] Añadir bloque de contacto/newsletter con input vinculado a label.

**Verificación:** El footer aparece al final de todas las vistas con el mismo contenido y estructura.

## ✅ Tarea 6 — Punto de inserción de JS vanilla
- [x] Reservar bloque `<script>` antes de `</body>` (comentado o vacío).
- [x] Documentar dónde irá el toggle móvil cuando se implemente.

**Verificación:** No hay dependencias JS externas; el bloque está listo para futuras interacciones.

## Fase de verificación global (previa a implementar contenido de negocio)
- [x] Copiar la plantilla a las 5 vistas manteniendo navbar y footer idénticos.
- [x] Comprobar navegación funcional entre las 5 vistas.
- [x] Auditar SEO/A11y: un solo `<h1>`, `alt` en imágenes, labels vinculados, `<nav>`/`<footer>` semánticos.
- [x] Comprobar responsive en móvil y escritorio (breakpoints `sm:`, `lg:`).

**Criterio de aceptación final:** La plantilla base queda aprobada cuando pasa todas las verificaciones anteriores sin frameworks ni build.

> 🔜 **Siguiente paso (no implementar aún):** crear `docs/reference/base.html` siguiendo estas tareas.