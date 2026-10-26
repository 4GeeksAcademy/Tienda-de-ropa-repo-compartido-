# Plan: Base Layout y Plantilla Común

> **Ubicación:** `specs/base-layout/plan.md`
> **Relacionado con:** `specs/base-layout/spec.md` (requisitos) y `docs/reference/base.html` (plantilla a crear).

## 🎯 Objetivo
Implementar la plantilla HTML común (`docs/reference/base.html`) y dejarla lista para que las 5 vistas (Home, Catálogo, Producto, Carrito, Checkout) se construyan copiándola. Esta fase es el esqueleto del prototipo: sin contenido de negocio, solo estructura, estilos y componentes reutilizables.

## 📋 Fases del plan

### Fase 1 — Preparación (Role 1: Frontend e integración)
- [x] Confirmar la estructura de carpetas del proyecto (raíz con los 5 HTML, `docs/reference/`, `specs/`).
- [x] Definir convenciones de nomenclatura de archivos y nombres de clase de las vistas.
- [x] Acordar la marca de ejemplo (nombre/logo) para el navbar y footer.
- **Entregable:** estructura de carpetas creada y convenciones documentadas.

### Fase 2 — Plantilla base `base.html` (Role 1)
- [x] Crear `docs/reference/base.html` siguiendo `specs/base-layout/spec.md`.
- [x] Incluir `<head>` completo: metadatos, Open Graph, canonical, título patrón y Tailwind v4 por CDN.
- [x] Implementar `<header>` con navbar reutilizable (logo, búsqueda, menú `<nav>`, iconos).
- [x] Implementar `<main>` vacío con comentario de inserción por vista.
- [x] Implementar `<footer>` reutilizable (categorías, legal, contacto/newsletter).
- [x] Dejar bloque JS vanilla mínimo comentado (toggle móvil y futuras interacciones).
- **Entregable:** `docs/reference/base.html`.

### Fase 3 — Validación de la plantilla (Role 4: Checkout, A11y y calidad)
- [x] Verificar carga de Tailwind v4 por CDN desde navegador (sin build).
- [x] Auditar SEO/A11y: un solo `<h1>` por página, `<nav>`/`<footer>` semánticos, `alt`, labels vinculados.
- [x] Comprobar responsive del navbar en móvil/tablet/escritorio (`sm:`, `lg:`).
- **Entregable:** checklist de validación completado contra `specs/base-layout/spec.md` (criterios de aceptación).

### Fase 4 — Replicación en las 5 vistas (Roles 2 y 3 en paralelo)
- [x] Role 2: crear `index.html` (Home) y `catalogue.html` desde la plantilla.
- [x] Role 3: crear `product.html` y `cart.html` desde la plantilla.
- [x] Role 4: crear `checkout.html` desde la plantilla.
- [x] Actualizar enlaces de navbar/footer por vista (navegación funcional).
- **Entregable:** las 5 vistas partiendo del mismo esqueleto.

### Fase 5 — Revisión de integración (Role 1 + Role 4)
- [x] Verificar que navbar y footer son idénticos entre vistas.
- [x] Validar el flujo de navegación completo entre las 5 vistas.
- [x] Resolver conflictos de estructura o estilos compartidos.
- **Entregable:** flujo navegable base, previo a contenido de negocio.

## 👥 Asignación de roles
| Fase | Responsable | Rol |
|------|-------------|-----|
| 1 y 2 | Integración y estructura | Role 1 |
| 3 | Calidad / A11y / SEO | Role 4 |
| 4 (Home, Catálogo) | Descubrimiento | Role 2 |
| 4 (Producto, Carrito) | Compra | Role 3 |
| 4 (Checkout) | Checkout | Role 4 |
| 5 | Integración + QA | Roles 1 y 4 |

## ✅ Criterios de aceptación (resumen)
1. `base.html` abre en navegador mostrando navbar + `main` vacío + footer.
2. Tailwind v4 cargado por CDN, sin build ni frameworks.
3. Navbar y footer idénticos al replicarse en las 5 vistas.
4. Cumple reglas SEO/A11y de la sección 10 de `specs/base-layout/spec.md`.
5. Responsive correcto en móvil y escritorio.