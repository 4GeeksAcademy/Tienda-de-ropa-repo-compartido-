# Spec: Catálogo (catalogue.html)

> **Propósito:** Definir los requisitos de la vista Catálogo, que muestra los productos con barra de filtros y rejilla responsive.
> **Relacionado con:** `specs/base-layout/spec.md` (plantilla base), `specs/menu/spec.md` (navbar y footer) y `specs/catalogue/plan.md`, `specs/catalogue/task.md`.

## 1. Alcance
- Vista `catalogue.html` con la navbar y el footer reutilizables (idénticos a `docs/reference/base.html`).
- Barra de filtros por categoría y por talla.
- Rejilla de productos 4 columnas × 5 filas (20 productos de referencia).

## 2. Navbar y footer
- Se reutilizan sin cambios según `specs/menu/spec.md`.

## 3. Barra de filtros
- **Categoría:** `<select>` vinculado a su `<label>` con opciones: todas, Chaussures, Chemises, Pantalons, Accessoires.
- **Talla:** grupo de opciones (`<fieldset>` con `<legend>` "Taille") con valores Toutes, XS, S, M, L, XL. Cada opción es un radio oculto con su `<label>` visible.
- **Resultados:** contador de productos visibles con `aria-live="polite"`.
- **Reinicio:** botón que restablece ambos filtros.
- Responsive: columna en móvil, fila en `lg:`.

## 4. Filtrado (JS vanilla mínimo)
- Cada tarjeta lleva `data-category` y `data-sizes`.
- Al cambiar un filtro se ocultan las tarjetas que no cumplen ambos criterios (atributo `hidden`).
- Sin dependencias externas.

## 5. Rejilla de productos
- `<ul>` con `role="list"` y microdatos `ItemList`.
- Columnas: 2 en móvil, 2 en `sm:`, 3 en `lg:`, 4 en `xl:` (4 × 5 con 20 productos).
- Cada tarjeta es un `<article>` con microdatos `Product` y `Offer` (nombre, imagen, categoría, precio en EUR, disponibilidad), y enlaza a `product.html`.
- Imágenes placeholder con `alt` descriptivo.

## 6. Datos structurados y SEO/A11y
- Un único `<h1>` (Catalogue) dentro de `<main>`; los nombres de producto son `<h2>`.
- Filtros con etiquetas asociadas y grupo con `role="group"` y `aria-label`.
- `<main>` con `id="site-main"`.

## 7. Criterios de aceptación
1. Navbar y footer idénticos a `docs/reference/base.html`.
2. La barra de filtros permite filtrar por categoría y por talla, por separado o combinados.
3. Con todos los filtros en "Toutes", se muestran los 20 productos en rejilla 4 × 5 en `xl:`.
4. El contador de resultados refleja las tarjetas visibles.
5. Responsive correcto en móvil y escritorio.
6. Sin frameworks ni dependencias JS externas.
