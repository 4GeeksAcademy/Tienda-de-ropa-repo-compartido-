# Spec: Menú (Navbar y Footer)

> **Propósito:** Definir los requisitos de la navbar y el footer reutilizables, tal como se implementan en `docs/reference/base.html` y se replican en `home.html`.
> **Relacionado con:** `specs/base-layout/spec.md` (plantilla base) y `specs/menu/plan.md`, `specs/menu/task.md`.

## 1. Alcance
- Navbar (`<header>`) con logo, barra de búsqueda, menú de navegación y menú de cuenta de usuario.
- Footer (`<footer>`) con secciones Categorías, Legal, Contacto y Newsletter.
- Ambos se reutilizan idénticos en las cinco vistas del prototipo.

## 2. Navbar
- **Logo:** enlace a `index.html` con el nombre de marca.
- **Barra de búsqueda:** `<input type="search">` vinculado a su `<label>` (`for`/`id`). Visible desde `md:`.
- **Navegación:** `<nav>` con enlaces a Accueil, Catalogue, Produit, Panier y Paiement.
- **Menú de cuenta de usuario:** icono de cuenta con `aria-label`, junto a favoritos y carrito.
- **Móvil:** el menú se oculta bajo el botón `#menu-toggle` (`md:hidden`) y se despliega con JS vanilla mínimo (`aria-expanded`).

## 3. Footer
- **Categorías:** Chaussures, Chemises, Pantalons, Accessoires (enlazan a `catalogue.html`).
- **Légal:** Conditions générales, Politique de confidentialité, À propos de la marque.
- **Contact:** dirección, correo y teléfono con microdatos `Organization` y `PostalAddress`.
- **Newsletter:** input de correo vinculado a su `<label>` y botón de suscripción.
- **Pie inferior:** copyright y enlaces a redes sociales (placeholder).

## 4. Datos estructurados (Schema.org, microdatos HTML)
- Contacto del footer: `itemscope itemtype="https://schema.org/Organization"` con `name`, `address`, `email` y `telephone`.
- Solo el bloque de contacto del footer lleva microdatos; la navbar no los necesita.

## 5. Reglas de estilo y accesibilidad
- Paleta y tipografía según `design.md` (navbar blanca con `border-neutral-200`; footer `slate-900` con texto claro).
- Contenedor `max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`.
- Un único `<h1>` por página (dentro de `<main>`); los títulos del footer son `<h2>`.
- Todas las imágenes con `alt`; todos los inputs con `<label>`.

## 6. Criterios de aceptación
1. La navbar y el footer de `home.html` coinciden con `docs/reference/base.html`.
2. El footer incluye la sección Contacto además de Categorías, Legal y Newsletter.
3. El menú móvil se abre y cierra con el botón de la navbar.
4. Los microdatos Schema.org son válidos en el bloque de contacto.
5. Sin frameworks ni dependencias JS externas.
