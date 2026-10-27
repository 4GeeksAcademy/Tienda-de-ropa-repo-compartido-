# Plan: Menú (Navbar y Footer)

> **Ubicación:** `specs/menu/plan.md`
> **Relacionado con:** `specs/menu/spec.md` (requisitos) y `specs/menu/task.md` (tareas).

## 🎯 Objetivo
Asegurar que la navbar y el footer sean idénticos en todas las vistas, añadiendo la sección Contacto y los microdatos Schema.org.

## 📋 Fases del plan

### Fase 1 — Referencia (Role 1: Frontend e integración)
- [x] Añadir la sección Contacto al footer de `docs/reference/base.html`.
- [x] Ajustar la distribución de columnas del footer (Categorías, Legal, Contacto, Newsletter).
- **Entregable:** `docs/reference/base.html` con footer completo.

### Fase 2 — Replicación en Home (Role 2: Descubrimiento)
- [x] Crear `home.html` con la navbar y el footer de la referencia.
- [x] Activar el toggle del menú móvil en `home.html`.
- **Entregable:** `home.html` con el menú idéntico a la referencia.

### Fase 3 — Verificación (Role 4: Calidad / A11y / SEO)
- [ ] Comprobar en navegador la navbar en móvil y escritorio.
- [ ] Comprobar que el toggle móvil abre y cierra el menú.
- [ ] Validar los microdatos Schema.org con una herramienta de test de datos estructurados.
- **Entregable:** checklist de verificación completado.

### Fase 4 — Replicación en el resto de vistas (Roles 2, 3 y 4)
- [ ] Copiar navbar y footer actualizados a `catalogue.html`, `product.html`, `cart.html` y `checkout.html`.
- [ ] Activar el toggle móvil en cada vista que lo necesite.
- **Entregable:** las cinco vistas con el mismo menú.

## 👥 Asignación de roles
| Fase | Responsable | Rol |
|------|-------------|-----|
| 1 | Integración y estructura | Role 1 |
| 2 | Descubrimiento | Role 2 |
| 3 | Calidad / A11y / SEO | Role 4 |
| 4 | Todas las vistas | Roles 2, 3 y 4 |

## ✅ Criterios de aceptación (resumen)
1. Navbar y footer idénticos entre `docs/reference/base.html` y todas las vistas.
2. Footer con Categorías, Legal, Contacto y Newsletter.
3. Menú móvil funcional sin dependencias externas.
4. Microdatos Schema.org válidos.
