# 🎨 Design System & UI Guidelines

## 🇫🇷 Concepto de Diseño
Estética **Elegante, Minimalista y Editorial**, inspirada en casas de moda francesas contemporáneas. Uso amplio de espacios en blanco (whitespace), tipografías refinadas y contrastes limpios.

## 🎨 Paleta de Colores (Tailwind Color Palette)
- **Color Primario (Dominante):** Neutral Slate / Dark Charcoal (`bg-slate-900`, `text-slate-900`)
- **Color Secundario (Acentos):** Cream / Soft Warm Beige (`bg-stone-100`, `bg-amber-50`)
- **Color Acciones / CTAs:** Black & Deep Indigo (`bg-black hover:bg-neutral-800 text-white`)
- **Textos Secundarios / Meta:** Neutral Muted Gray (`text-gray-500`, `text-slate-600`)
- **Fondo General:** Pure White (`bg-white`) / Warm Slate Gray light (`bg-slate-50`)
- **Bordes & Divisores:** Fine Neutral Lines (`border-neutral-200`)

## 🔤 Tipografía
- **Titulares (`<h1>`, `<h2>`, `<h3>`):** Font Serif elegante (`font-serif` o `font-sans` con tracking amplio `tracking-wide` / `tracking-tight`).
- **Cuerpo de texto & UI Buttons:** Font Sans limpia y legible (`font-sans`).

## 📐 Layout & Responsive Breakpoints
- **Mobile First:** Diseño pensado de origen para pantallas móviles.
- **Breakpoints Tailwind:**
  - `sm:` (640px) - Mobiles horizontales / Tablets pequeñas.
  - `md:` (768px) - Tablets en vertical.
  - `lg:` (1024px) - Portátiles / Laptops (Grid de catálogo pasa a 3-4 cols).
  - `xl:` (1280px) - Escritorios grandes (Grid de catálogo 4×5).
- **Contenedor Principal:** `max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`.

## 🧩 Componentes UI Patrón (Design Specifications)

### 1. Botones (CTA Buttons)
- **Primario:** `bg-slate-900 text-white px-6 py-3 rounded-none hover:bg-slate-800 transition-colors duration-200 uppercase text-xs font-semibold tracking-widest`
- **Secundario:** `border border-slate-900 text-slate-900 px-6 py-3 hover:bg-slate-900 hover:text-white transition-colors duration-200 uppercase text-xs font-semibold tracking-widest`

### 2. Tarjeta de Producto (Product Card)
- Aspect ratio de imagen vertical (`aspect-[3/4] object-cover`).
- Efecto hover suave de zoom o sombra en la imagen (`group-hover:scale-105 transition-transform duration-300`).
- Estructura limpia: Marca/Categoría pequeña, Nombre en semi-bold, Precio destacado.

### 3. Formularios & Inputs
- Estilo minimalista con bordes finos: `border border-gray-300 focus:border-slate-900 focus:ring-1 focus:ring-slate-900 rounded-none px-4 py-2 text-sm outline-none transition-all`.

---

## 🔍 Reglas SEO & Accesibilidad (A11y)
1. **Jerarquía HTML:** Cada archivo HTML debe contener exactamente **un único `<h1>`** que represente el título de la vista.
2. **Navegación:** Menú principal dentro de la etiqueta `<nav>`, footer en `<footer>`.
3. **Imágenes:** Toda etiqueta `<img>` debe contar con atributo `alt=""` descriptivo.
4. **Formularios:** Todos los `<input>` deben estar explícitamente vinculados a su `<label>` correspondiente (`for=""` e `id=""`).