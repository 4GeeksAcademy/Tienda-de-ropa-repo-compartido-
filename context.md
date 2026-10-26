# 📌 Contexto del Proyecto y Requisitos de Negocio

## 🏢 Información del Cliente
- **Cliente:** Marca de ropa de alta reputación / prét-à-porter con sede en Francia.
- **Proyecto:** Prototipo visual y funcional para su próxima tienda e-commerce.
- **Entregable:** Prototipo navegable de 5 vistas clave optimizadas para dispositivos móviles, tablets y escritorios.

## 🎯 Objetivos de Negocio
1. **Demostración de marca:** Transmitir elegancia, modernidad y minimalismo acorde con la moda francesa.
2. **Posicionamiento SEO:** Estructura de código pensada para una rápida indexación por motores de búsqueda.
3. **Conversión y UX:** Flujo de navegación intuitivo desde la atracción (Home/Catálogo) hasta la compra (Checkout en 3 pasos).

## 🛠️ Stack Tecnológico Permitido
- **HTML5:** Marcado semántico y accesible.
- **Tailwind CSS v4 por CDN:** Estilizado visual responsive servido exclusivamente vía CDN. Sin build o compilación local.
  - Incluir en el `<head>` de cada página:
    ```html
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    ```
  - Responsive mediante utilidades nativas de Tailwind (`sm:`, `md:`, `lg:`, `xl:`).
- **JavaScript:** Únicamente vanilla mínimo e inline (menú móvil, carrito, pasos de checkout). Prohibidos frameworks y dependencias externas.
- **Imágenes:** Unsplash / Placeholder URLs con temáticas de moda francesa elegante.

---

## 📐 Especificación Detallada de Vistas

### 1. Página de Inicio (Home)
- **Header / Navbar (Reutilizable):**
  - Logo de la marca.
  - Barra de búsqueda (Search Bar).
  - Menú de cuenta / usuario (Iconos de usuario, favoritos, carrito).
- **Hero Section:** Banner de alto impacto visual destacando colecciones o campañas de temporada.
- **Listados Horizontales de Productos (Cards):**
  - Sección 1: *Nuevos Lanzamientos* (Nouveautés).
  - Sección 2: *Más Vendidos* (Les Incontournables).
- **Footer (Reutilizable):**
  - Categorías: Calzado, Camisas, Pantalones, Accesorios.
  - Legal: Términos y condiciones, Política de privacidad, Sobre la marca.
  - Contacto & Newsletter.

### 2. Catálogo (Catalogue)
- **Navbar & Footer** integrados.
- **Barra de Filtros Superior:**
  - Filtro por categoría (Calzado, Camisas, etc.).
  - Filtro por talla (XS, S, M, L, XL).
- **Grid de Productos:**
  - Rejilla responsive de 4 columnas × 5 filas (20 productos en total).

### 3. Vista de Producto (Product Detail Page)
- **Layout principal (2 columnas en desktop):**
  - *Columna Izquierda (~50%):* Galería / Fotografía principal del producto.
  - *Columna Derecha:*
    - Nombre del producto.
    - Código/Referencia (SKU).
    - Talla (Selector interactivo/radio buttons).
    - Precio (€ EUR).
    - Selector de cantidad.
    - Botón prioritario "Agregar al carrito" (Ajouter au panier).
- **Sección Inferior:**
  - Detalles de materiales y composición.
  - Recomendaciones de uso y styling/escenarios.

### 4. Carrito (Cart)
- **Vista completa de página** (no drawer ni modal).
- **Tabla / Listado de ítems (con 3 productos de ejemplo):**
  - Imagen miniatura, nombre, precio unitario, selector de cantidad y subtotal por fila.
- **Cuadro de Resumen de Compra:**
  - Subtotal.
  - Impuestos (TVA Francia / 20% indicado).
  - Total final.
  - Botón destacado "Comprar / Proceder al pago".

### 5. Formulario de Pago (Checkout)
- **Flujo visual por pasos (Stepped Layout):**
  - **Paso 1:** Datos personales (Nombre, email, teléfono).
  - **Paso 2:** Dirección de entrega (Dirección, ciudad, código postal, país).
  - **Paso 3:** Datos de pago con tarjeta (Número de tarjeta, fecha de expiración, CVC).

---

## 📄 Entregables Propuestos
- Un archivo HTML por vista: `index.html` (Home), `catalogue.html`, `product.html`, `cart.html` y `checkout.html`.
- Enlaces funcionales entre vistas para recorrer el flujo completo de compra.
- Datos de ejemplo (productos, tallas, precios en EUR) coherentes entre vistas.