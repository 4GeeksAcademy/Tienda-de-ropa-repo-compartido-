# Task: Catálogo (catalogue.html)

> **Ubicación:** `specs/catalogue/task.md`
> **Contexto:** requisitos en `spec.md`, plan en `plan.md`.

## ✅ Tarea 1 — Navbar y footer
- [x] Mantener la navbar de la referencia en `catalogue.html`.
- [x] Añadir la columna Contact y el grid de cuatro columnas al footer.

**Verificación:** navbar y footer coinciden con `docs/reference/base.html`.

## ✅ Tarea 2 — Barra de filtros
- [x] Crear el `<select>` de categoría con su `<label>`.
- [x] Crear el grupo de talla (XS, S, M, L, XL) con `<fieldset>` y `<legend>`.
- [x] Añadir contador de resultados (`aria-live`) y botón de reinicio.

**Verificación:** la barra es responsive y cada control tiene etiqueta accesible.

## ✅ Tarea 3 — Rejilla de productos
- [x] Crear 20 tarjetas con `data-category` y `data-sizes`.
- [x] Aplicar microdatos `Product`, `Offer` e `ItemList`.
- [x] Definir columnas 2 / 3 / 4 según breakpoints.

**Verificación:** 20 tarjetas en rejilla 4 × 5 en `xl:`.

## ✅ Tarea 4 — Filtrado con JS vanilla
- [x] Filtrar por categoría y talla, separados o combinados.
- [x] Actualizar el contador de resultados.
- [x] Restablecer filtros con el botón de reinicio.

**Verificación:** cada combinación muestra solo las tarjetas que cumplen los criterios.

## ⬜ Tarea 5 — Verificación en navegador
- [ ] Probar filtros en móvil (375px) y escritorio (1280px).
- [ ] Validar los microdatos con una herramienta de datos estructurados.

**Criterio de aceptación final:** catálogo funcional con filtros y rejilla responsive.
