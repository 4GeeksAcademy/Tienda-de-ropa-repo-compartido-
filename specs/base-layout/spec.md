# Spec: Plantilla Base Común (base.html)

> **Propósito:** Definir los requisitos del documento de referencia `docs/reference/base.html`, la plantilla HTML común para las 5 vistas del proyecto. Este spec describe qué debe contener y cómo debe comportarse; **no implementa código** (el HTML final vive en `docs/reference/base.html`).

## 1. Objetivo
Servir de punto de partida idéntico para todas las vistas (Home, Catálogo, Producto, Carrito, Checkout), garantizando:
- Consistencia de estructura, estilos y componentes compartidos.
- Cumplimiento del stack técnico y de las reglas de SEO/Accesibilidad.
- Una integración sencilla por parte del equipo (roles 2, 3 y 4 de `agents.md`).

## 2. Ubicación y convención de archivos
- El documento de referencia se guarda en **`docs/reference/base.html`**.
- El spec de este documento vive en **`specs/base-layout/spec.md`**.
- Cada vista debe partir de esta plantilla copiando su contenido y completando su `<main>` y sus metadatos.

## 3. Stack técnico (obligatorio)
- **HTML5** semántico.
- **Tailwind CSS v4 por CDN**, cargado en el `<head>` mediante el script oficial del navegador:
  - `<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>`
- **Sin frameworks de JavaScript** (React, Vue, etc.) ni dependencias externas.
- **Sin build ni compilación local**: solo CDN.
- Documentar como comentario dónde se insertaría el JS vanilla mínimo si una vista lo necesita (menú móvil, carrito, checkout).

## 4. Estructura general del documento
La plantilla debe definir una estructura de alto nivel con estas regiones, en este orden:
1. **`<!DOCTYPE html>`** y `<html lang="fr">` (idioma de la marca) con `<head>` completo.
2. **`<header>`** con el navbar reutilizable.
3. **`<main>`** vacío (contenido por vista).
4. **`<footer>`** reutilizable.
5. (Opcional) bloque `<script>` vanilla mínimo ubicado antes de `</body>`, comentado/vacío por defecto.

## 5. Requisitos del `<head>`
Debe incluir, como mínimo:
- `<meta charset="UTF-8">`.
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`.
- `<title>` con el patrón **"Página — Maison [Nombre]"** (placeholder en la plantilla).
- `<meta name="description">` con placeholder.
- Etiquetas **Open Graph** básicas (og:type, og:title, og:description, og:image) con placeholders.
- Enlace **canonical** (`<link rel="canonical">`) como placeholder.
- El **script de Tailwind v4 por CDN** (obligatorio).
- Favicon opcional con placeholder.

## 6. Navbar (reutilizable) — en `<header>`
- Logo de la marca (texto o imagen placeholder con `alt`).
- Barra de búsqueda (`<input>` vinculado a su `<label>` con `for`/`id`, o `aria-label`).
- Enlaces de navegación del menú: Inicio, Catálogo, y acceso a las 5 vistas del proyecto.
- Iconos de cuenta/usuario, favoritos y carrito (con accesos al carrito y checkout).
- Envolver los enlaces de menú en la etiqueta **`<nav>`** (regla A11y de `design.md`).
- **Responsive mobile-first**: ocultar/replegar el menú en móvil (`sm:`) y mostrarlo en escritorio. Comentar el punto de inserción del JS minimal para el toggle móvil.
- Estilado según la paleta y tipografía de `design.md` (primario `slate-900`, fondo blanco, bordes finos `neutral-200`).

## 7. Contenido principal — `<main>`
- **Vacío en la plantilla**, con un comentario indicando que cada vista debe insertar aquí su contenido.
- La etiqueta `<h1>` de cada vista (única por página) se colocará dentro de este `<main>`.
- No incluir contenido ficticio ni secciones de ejemplo de producto en la plantilla.

## 8. Footer (reutilizable) — en `<footer>`
Debe contener columnas de contenido, estructuradas semánticamente:
- **Categorías:** Calzado, Camisas, Pantalones, Accesorios.
- **Legal:** Términos y condiciones, Política de privacidad, Sobre la marca.
- **Contacto y Newsletter** (input vinculado a su label).
- Enlaces de redes sociales (placeholder).
- Año y nombre de la marca (texto de copyright).
- Fondo en tono oscuro (`slate-900`) con texto claro, acorde a la paleta de `design.md`.

## 9. Contenedor principal de layout
- Las vistas deben usar el contenedor definido en `design.md`:
  - `max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`
- La plantilla debe documentar este contenedor como referencia (no incluye un `<main>` con contenedor obligatorio fijo; cada vista decide dónde aplicarlo dentro de su `<main>`).

## 10. Reglas SEO y Accesibilidad (obligatorias)
- **Un único `<h1>` por página** (la plantilla lo deja listo dentro de `<main>` para cada vista).
- Menú dentro de `<nav>`, footer dentro de `<footer>`.
- Toda `<img>` con `alt` descriptivo.
- Todo `<input>` vinculado a su `<label>` (`for`/`id`) o con `aria-label`.
- Uso de `aria-*` apropiado en menús e inputs (según `agents.md`).
- Jerarquía de encabezados lógica y semántica.

## 11. Restricciones y prohibiciones
- No usar frameworks, librerías JS, ni dependencias externas.
- No añadir CSS propio en `<style>` salvo que sea estrictamente necesario; priorizar utilidades de Tailwind.
- No incluir contenido de negocio (productos reales) en la plantilla: solo componentes estructurales reutilizables.
- No implementar lógica de carrito/checkout en la plantilla: solo dejar los puntos de extensión documentados.

## 12. Criterios de aceptación
La plantilla `docs/reference/base.html` se considera correcta cuando:
1. Abre correctamente en navegador mostrando solo navbar + `main` vacío + footer.
2. Carga Tailwind v4 por CDN sin build local.
3. No contiene framework JS alguno.
4. Cada vista copiada de la plantilla conserva navbar y footer idénticos.
5. El markup cumple las reglas SEO/A11y de la sección 10.
6. Responsive: navbar y layout base se ven correctos en móvil y escritorio (breakpoints `sm:`/`lg:`).