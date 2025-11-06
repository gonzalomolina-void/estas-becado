# Style Tile - ¿Estás Becado? (v3)

**Proyecto:** Plataforma de búsqueda de becas argentinas
**Sprint:** 5 - Prototipo v3
**Fecha:** Noviembre 2025
**Universidad:** UNComa

---

## 1. Paleta de Colores

### Colores Principales (Light Mode)

| Color | Hex | Variable CSS | Uso | Muestra |
|---|---|---|---|---|
| **Azul Principal** | `#004aa3` | `--color-accent` | Accent, botones primarios, enlaces | ![#004aa3](https://dummyimage.com/80x40/004aa3/004aa3.png) |
| **Texto Oscuro** | `#222224` | `--color-text` | Texto principal, títulos | ![#222224](https://dummyimage.com/80x40/222224/222224.png) |
| **Texto Secundario**| `#4f4f4f` | `--color-secondary`| Texto de apoyo, subtítulos | ![#4f4f4f](https://dummyimage.com/80x40/4f4f4f/4f4f4f.png) |
| **Fondo Claro** | `#ffffff` | `--color-bg` | Fondo principal | ![#ffffff](https://dummyimage.com/80x40/ffffff/ffffff.png) |
| **Borde** | `#e0e0e0` | `--color-border` | Bordes, divisores | ![#e0e0e0](https://dummyimage.com/80x40/e0e0e0/e0e0e0.png) |

### Colores de Estado

| Estado | Hex | Variable CSS | Uso |
|---|---|---|---|
| **Aprobado** | `#22c55e` | `--color-success` | Estados de éxito, confirmaciones |
| **En Evaluación**| `#eab308` | `--color-warning` | Alertas, estados pendientes |
| **Rechazado** | `#ef4444` | `--color-danger` | Errores, estados de rechazo |

### Colores Secundarios (Light Mode)

| Elemento | Hex | Uso |
|---|---|---|
| **Fondo Navegación** | `#f8f8f8` | Background del menú de navegación |
| **Fondo Footer** | `#fafafa` | Background del pie de página |
| **Hover Azul Oscuro**| `#003366` | Estado hover de botones primarios |

---

## 2. Modo Oscuro (Dark Theme)

### Paleta Oscura

| Color | Hex | Variable CSS | Uso |
|---|---|---|---|
| **Fondo Oscuro** | `#222224` | `--color-bg` | Fondo principal |
| **Texto Claro** | `#f8f8f8` | `--color-text` | Texto principal |
| **Texto Secundario**| `#bdbdbd` | `--color-secondary`| Texto de apoyo |
| **Borde Oscuro** | `#3a3a3a` | `--color-border` | Bordes y divisores |
| **Fondo Contenedor Oscuro**| `#2c2c2c` | N/A | Fondo de `nav`, `cards`, `calificacion-section`, `thead`, `tbody tr:hover` |
| **Fondo Footer Oscuro** | `#2a2a2a` | N/A | Fondo del pie de página en modo oscuro |
| **Fondo Contenedor Tabla Oscuro** | `#222224` | N/A | Fondo de `.table-container` en modo oscuro |
| **Input Background**| `#3a3a3a` | N/A | Campos de formulario |

---

## 3. Tipografía

### Familias Tipográficas

**Google Fonts:**
- **Inter** (400, 600) - Usada para el cuerpo de texto, párrafos y elementos de UI.
- **Poppins** (400, 600) - Usada para títulos y el logo.

### Jerarquía Tipográfica

```css
/* Logo */
font-family: 'Poppins', sans-serif;
font-size: 2.25rem; /* 36px */
font-weight: 600;

/* Títulos principales (h2) */
font-family: 'Poppins', sans-serif;
font-size: 2.5rem; /* 40px */
font-weight: normal; /* 400 */

/* Subtítulos (h3) */
font-family: 'Poppins', sans-serif;
font-size: 1.75rem; /* 28px */
font-weight: normal; /* 400 */

/* Cuerpo de texto */
font-family: 'Inter', sans-serif;
font-size: 1.05rem; /* ~17px */
line-height: 1.6;

/* Navegación */
font-family: 'Inter', sans-serif;
font-weight: 600;

/* Botones */
font-family: 'Inter', sans-serif;
font-weight: 600;
```

---

## 4. Componentes UI

### Botones

**Botón Primario (`.btn`):**
- **Fondo:** `var(--color-accent)`
- **Color Texto:** `white`
- **Padding:** `0.75rem 1.5rem`
- **Border Radius:** `8px`
- **Hover:** Fondo `#003366`

**Botón de Navegación (`nav a`):**
- **Padding:** `0.75rem 1.25rem`
- **Border Radius:** `8px`
- **Estado Activo/Hover:** Fondo `var(--color-accent)`, Color `white`

### Tarjetas (`.beca-card`)

- **Borde:** `1px solid var(--color-border)`
- **Border Radius:** `12px`
- **Padding:** `1.5rem`
- **Hover:** `transform: translateY(-4px)`, `box-shadow: 0 8px 16px rgba(0,0,0,0.1)`

### Formularios (`.form-group`)

- **Inputs/Selects:**
  - **Padding:** `0.75rem 1rem`
  - **Borde:** `1px solid var(--color-border)`
  - **Border Radius:** `8px`
  - **Focus:** `border-color: var(--color-accent)`

### Tabla

- **Contenedor (`.table-container`):**
  - `overflow-x: auto`
  - `border: 1px solid var(--color-border)`
  - `border-radius: 8px`
  - `background-color: var(--color-bg)`
  - **Dark Mode:** `background-color: #222224`

- **Tabla (`table`):**
  - `width: 100%`
  - `border-collapse: collapse`
  - `font-size: 0.9rem`

- **Encabezado (`thead`):**
  - `background-color: #f8f8f8`
  - **Dark Mode:** `background-color: #2c2c2c`

- **Celdas de Encabezado (`th`):**
  - `font-weight: 600`
  - `padding: 1rem`
  - `text-align: left`
  - `border-bottom: 1px solid var(--color-border)`

- **Celdas de Datos (`td`):**
  - `padding: 1rem`
  - `text-align: left`
  - `border-bottom: 1px solid var(--color-border)`

- **Fila Hover (`tbody tr:hover`):**
  - `background-color: #fafafa` (Light Mode)
  - `background-color: #2c2c2c` (Dark Mode)

- **Última Fila (`tbody tr:last-child td`):**
  - `border-bottom: none`

- **Estados (`.status`):**
  - `font-weight: 600`
  - **Aprobado (`.status-aprobado`):** `color: var(--color-success)`
  - **En Evaluación (`.status-evaluacion`):** `color: var(--color-warning)`
  - **Rechazado (`.status-rechazado`):** `color: var(--color-danger)`
---

## 5. Iconografía

- **Biblioteca:** Lucide Icons
- **CDN:** `https://unpkg.com/lucide@latest`
- **Iconos Utilizados:** `moon`, `sun`, `search`, `facebook`, `twitter`, `instagram`, `linkedin`.
- **Interacción:** El color de los íconos sociales cambia a `var(--color-accent)` en hover.

---

## 6. Layout y Espaciado

- **Ancho Máximo:** `1100px` - `1200px`
- **Márgen Principal:** `3rem auto` (Desktop), `1.5rem auto` (Mobile)
- **Padding Contenedor:** `0 1.5rem`
- **Gaps Comunes:** `0.5rem`, `1rem`, `1.5rem`, `2rem`, `3rem`

---

## 7. Branding

### Logo

- **Tipografía:** Poppins, 600
- **Concepto:** Texto simple con la palabra "Becado" resaltada en el color de acento (`--color-accent`).
- **Implementación:**
  ```html
  <a href="..." class="logo">
    ¿Estás <span>Becado?</span>
  </a>
  ```

---

## 8. Responsive Design

### Breakpoints

- **Mobile:** `< 768px` (Layout de una sola columna, navegación apilada)
- **Tablet:** `768px` - `1023px` (Grids y formularios de 2 columnas)
- **Desktop:** `> 1024px` (Layouts de 2 columnas con sidebar)

### Ajustes Notables

- **Títulos:** Reducen su tamaño en mobile (`h2`: `2rem`, `h3`: `1.5rem`).
- **Navegación:** Pasa de horizontal a vertical en mobile.
- **Hero Section:** Pasa de `flex-direction: row` a `column` en mobile.
