# Plan: Catálogo (catalogue.html)

> **Ubicación:** `specs/catalogue/plan.md`
> **Relacionado con:** `specs/catalogue/spec.md` (requisitos) y `specs/catalogue/task.md` (tareas).

## 🎯 Objetivo
Implementar la vista Catálogo con navbar y footer reutilizables, barra de filtros (categoría y talla) y una rejilla responsive de 20 productos.

## 📋 Fases del plan

### Fase 1 — Menú en la vista (Role 1: Frontend e integración)
- [x] Actualizar el footer de `catalogue.html` con la columna Contact y el grid de cuatro columnas.
- [x] Verificar que la navbar coincide con la referencia.
- **Entregable:** navbar y footer idénticos a `docs/reference/base.html`.

### Fase 2 — Barra de filtros (Role 2: Descubrimiento)
- [x] Añadir filtro por categoría (`<select>`).
- [x] Añadir filtro por talla (grupo de opciones XS a XL).
- [x] Añadir contador de resultados y botón de reinicio.
- **Entregable:** barra de filtros responsive y accesible.

### Fase 3 — Rejilla de productos (Role 2: Descubrimiento)
- [x] Crear 20 tarjetas con microdatos `Product` y `Offer`.
- [x] Definir rejilla 2 / 3 / 4 columnas según breakpoints (`sm:`, `lg:`, `xl:`).
- [x] Conectar el filtrado con JS vanilla mínimo.
- **Entregable:** rejilla 4 × 5 funcional con filtros.

### Fase 4 — Verificación (Role 4: Calidad / A11y / SEO)
- [ ] Probar filtros por separado y combinados en navegador.
- [ ] Comprobar la rejilla en móvil, tablet y escritorio.
- [ ] Validar los microdatos con una herramienta de datos estructurados.
- **Entregable:** checklist de verificación completado.

## 👥 Asignación de roles
| Fase | Responsable | Rol |
|------|-------------|-----|
| 1 | Integración y estructura | Role 1 |
| 2 y 3 | Descubrimiento | Role 2 |
| 4 | Calidad / A11y / SEO | Role 4 |

## ✅ Criterios de aceptación (resumen)
1. Navbar y footer idénticos a la referencia.
2. Filtros por categoría y talla funcionales, separados o combinados.
3. Rejilla 4 × 5 con 20 productos en `xl:`.
4. Responsive y sin dependencias externas.
