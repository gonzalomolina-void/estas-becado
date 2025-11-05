# Style Tile - ¿Estás Becado?

**Proyecto:** Plataforma de búsqueda de becas argentinas
**Sprint:** 3 - Diseño Gráfico
**Fecha:** Octubre 2025
**Universidad:** UNComa

---

## 1. Paleta de Colores

### Colores Principales

| Color | Hex | Uso | Muestra |
|-------|-----|-----|---------|
| **Azul Principal** | `#0057b7` | Accent, botones primarios, enlaces destacados | ![#0057b7](https://dummyimage.com/80x40/0057b7/0057b7.png) |
| **Texto Oscuro** | `#222224` | Texto principal, títulos | ![#222224](https://dummyimage.com/80x40/222224/222224.png) |
| **Texto Secundario** | `#5e5e5e` | Texto de apoyo, subtítulos | ![#5e5e5e](https://dummyimage.com/80x40/5e5e5e/5e5e5e.png) |
| **Fondo Claro** | `#ffffff` | Fondo principal (modo claro) | ![#ffffff](https://dummyimage.com/80x40/ffffff/ffffff.png) |
| **Borde** | `#e0e0e0` | Bordes, divisores, líneas | ![#e0e0e0](https://dummyimage.com/80x40/e0e0e0/e0e0e0.png) |

### Colores de Estado

| Estado | Hex | Uso |
|--------|-----|-----|
| **Aprobado** (Verde) | `#22c55e` | Becas aprobadas, confirmaciones |
| **En Evaluación** (Amarillo) | `#eab308` | Becas en proceso, alertas |
| **Rechazado** (Rojo) | `#ef4444` | Becas rechazadas, errores |

### Colores Secundarios

| Elemento | Hex | Uso |
|----------|-----|-----|
| **Fondo Navegación** | `#f8f8f8` | Background de menú de navegación |
| **Fondo Footer** | `#fafafa` | Background del pie de página |
| **Hover Azul Oscuro** | `#00429a` | Estados hover de botones |

---

## 2. Modo Oscuro (Dark Theme)

### Paleta Oscura

| Color | Hex | Uso |
|-------|-----|-----|
| **Fondo Oscuro** | `#222224` | Fondo principal |
| **Texto Claro** | `#f8f8f8` | Texto principal |
| **Texto Secundario Claro** | `#bdbdbd` | Texto de apoyo |
| **Borde Oscuro** | `#3a3a3a` | Bordes y divisores |
| **Navegación Oscura** | `#2c2c2c` | Fondo de navegación |
| **Cards Oscuras** | `#2c2c2c` | Tarjetas y contenedores |
| **Footer Oscuro** | `#2a2a2a` | Pie de página |
| **Input Background** | `#1a1a1a` | Campos de formulario |

---

## 3. Tipografía

### Familias Tipográficas

**Google Fonts:**
- **Inter** (400, 600) - Texto de cuerpo
- **Poppins** (400, 600) - Títulos y encabezados

### Jerarquía Tipográfica

```css
/* Títulos principales (h2) */
font-family: 'Poppins', sans-serif;
font-size: 2.5rem;        /* 40px */
font-weight: 600;
color: var(--color-text);
text-align: center;

/* Subtítulos (h3) */
font-family: 'Poppins', sans-serif;
font-size: 1.75rem;       /* 28px */
font-weight: 600;
color: var(--color-text);

/* Cuerpo de texto */
font-family: 'Inter', sans-serif;
font-size: 1.05rem;       /* ~17px */
font-weight: 400;
line-height: 1.6;
color: var(--color-secondary);

/* Navegación */
font-family: 'Inter', sans-serif;
font-size: 1rem;
font-weight: 600;
color: var(--color-text);

/* Botones */
font-family: 'Inter', sans-serif;
font-size: 1rem;
font-weight: 600;
color: #ffffff;

/* Nombres de becas */
font-family: 'Inter', sans-serif;
font-size: 0.95rem;
font-weight: 600;
color: var(--color-text);

/* Footer */
font-family: 'Inter', sans-serif;
font-size: 0.9rem;
font-weight: 400;
color: var(--color-secondary);
```

### Responsive Typography

**Mobile (<768px):**
- h2: `1.75rem` (28px)
- h3: `1.5rem` (24px)
- Reducción general en tamaños

**Tablet (768px - 1023px):**
- Tamaños intermedios

**Desktop (1024px+):**
- Tamaños completos

---

## 4. Sistema de Espaciado

### Valores Base

```css
/* Espaciado interno (padding) */
.padding-xs: 0.5rem;   /* 8px */
.padding-sm: 1rem;     /* 16px */
.padding-md: 1.5rem;   /* 24px */
.padding-lg: 2rem;     /* 32px */
.padding-xl: 3rem;     /* 48px */

/* Espaciado externo (margin) */
.margin-xs: 0.5rem;
.margin-sm: 1rem;
.margin-md: 1.5rem;
.margin-lg: 2rem;
.margin-xl: 3rem;

/* Gaps */
.gap-xs: 0.5rem;
.gap-sm: 1rem;
.gap-md: 1.5rem;
.gap-lg: 2rem;
.gap-xl: 3rem;
```

### Contenedores

```css
/* Ancho máximo de contenido */
max-width: 1100px - 1200px;
margin: 3rem auto;
padding: 0 1.5rem;
```

---

## 5. Componentes UI

### Botones

**Botón Primario:**
```css
background-color: #0057b7;
color: white;
padding: 0.75rem 1.5rem;
border-radius: 8px;
font-weight: 600;
transition: background 0.3s;

/* Hover */
background-color: #00429a;
```

**Botón Secundario (Navegación):**
```css
color: var(--color-text);
padding: 0.75rem 1.25rem;
font-weight: 600;
border-radius: 8px;
transition: background 0.2s, color 0.2s;

/* Hover */
background-color: var(--color-accent);
color: #fff;
```

### Tarjetas (Cards)

**Tarjeta de Beca:**
```css
background-color: #fff;
border: 1px solid var(--color-border);
border-radius: 12px;
padding: 1.5rem;
transition: transform 0.2s, box-shadow 0.2s;

/* Hover */
transform: translateY(-4px);
box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
```

### Inputs y Formularios

**Campos de texto:**
```css
padding: 0.75rem 1rem;
border: 1px solid var(--color-border);
border-radius: 8px;
font-size: 1rem;
background-color: var(--color-bg);
transition: border-color 0.2s;

/* Focus */
outline: none;
border-color: var(--color-accent);
```

### Tabla

**Tabla de Becas:**
```css
/* Container */
border: 1px solid var(--color-border);
border-radius: 8px;
background-color: #fff;
overflow-x: auto;

/* Header */
background-color: #f8f8f8;
padding: 1rem;
font-weight: 600;
border-bottom: 1px solid var(--color-border);

/* Cells */
padding: 1rem;
border-bottom: 1px solid var(--color-border);

/* Row Hover */
background-color: #fafafa;
```

---

## 6. Iconografía

### Sistema de Iconos

**Biblioteca:** Lucide Icons (CDN)
**CDN:** `https://unpkg.com/lucide@latest`

**Iconos utilizados:**
- `search` - Búsqueda
- `facebook` - Red social
- `twitter` - Red social
- `instagram` - Red social
- `linkedin` - Red social

**Estilo:**
```css
font-size: 1.25rem;
color: var(--color-secondary);
transition: color 0.3s;

/* Hover */
color: var(--color-accent);
```

### Toggle Modo Oscuro

```css
🌙 - Modo claro (cambiar a oscuro)
☀️ - Modo oscuro (cambiar a claro)

font-size: 1.2rem;
cursor: pointer;
```

---

## 7. Logo y Branding

### Logo Principal

```html
<svg viewBox="0 0 200 60">
  <text font-family="Poppins" font-size="36">
    ¿Estás <tspan fill="#0057b7">Becado?</tspan>
  </text>
</svg>
```

**Características:**
- Tipografía: Poppins
- Color base: `currentColor` (adapta a tema)
- Color "Becado": `#0057b7`
- Altura: 60px
- Formato: SVG inline

---

## 8. Bordes y Sombras

### Border Radius

```css
.radius-sm: 8px;   /* Inputs, botones, nav items */
.radius-md: 12px;  /* Cards, containers */
```

### Box Shadows

```css
/* Sombra suave (cards) */
box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);

/* Sombra hover (cards) */
box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
```

### Borders

```css
border: 1px solid var(--color-border);
border-top: 1px solid var(--color-border);
border-bottom: 1px solid var(--color-border);
```

---

## 9. Transiciones y Animaciones

### Duraciones Estándar

```css
/* Rápidas (hover, focus) */
transition: background 0.2s, color 0.2s;
transition: transform 0.2s, box-shadow 0.2s;
transition: border-color 0.2s;

/* Medianas (theme toggle) */
transition: background 0.3s, color 0.3s;
transition: background 0.3s;
transition: color 0.3s;
```

### Efectos Comunes

**Hover elevación:**
```css
transform: translateY(-4px);
box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
```

**Color change:**
```css
background-color: var(--color-accent);
color: #fff;
```

---

## 10. Responsive Breakpoints

### Sistema de Breakpoints

```css
/* Mobile First - Base Styles */
/* Móvil: < 768px */

/* Tablet */
@media (min-width: 768px) and (max-width: 1023px) {
  /* Grid: 2-3 columnas */
  /* Formularios: 2 columnas */
}

/* Desktop */
@media (min-width: 1024px) {
  /* Layout de 2 columnas */
  /* Grid: 2x4 para becas */
  /* Formulario: columna fija 400px */
}
```

### Layouts por Dispositivo

**Móvil (<768px):**
- 1 columna
- Stack vertical
- Navegación vertical
- Grid de becas: 1 columna

**Tablet (768-1023px):**
- 1-2 columnas
- Grid de becas: 3 columnas
- Formularios: 2 columnas
- Navegación horizontal

**Desktop (1024px+):**
- 2 columnas (contenido + sidebar)
- Grid de becas: 2x4
- Formulario fijo: 400px
- Navegación horizontal completa

---

## 11. Variables CSS (Root)

```css
:root {
  --color-bg: #ffffff;
  --color-text: #222224;
  --color-secondary: #5e5e5e;
  --color-accent: #0057b7;
  --color-border: #e0e0e0;
}

body.dark {
  --color-bg: #222224;
  --color-text: #f8f8f8;
  --color-secondary: #bdbdbd;
  --color-border: #3a3a3a;
}
```

---

## 12. Navegación

### Estructura del Header

**Elementos:**
1. Logo (SVG centrado)
2. Barra de navegación con links:
   - ¿Estás Becado?
   - ¿A qué Becas puedo aplicar?
   - Trabajos Finales
3. Toggle de modo oscuro (derecha)

**Estilos:**
```css
/* Header */
text-align: center;
padding: 1.5rem 1rem 0.5rem;
border-bottom: 1px solid var(--color-border);

/* Nav */
display: flex;
justify-content: center;
align-items: center;
background-color: #f8f8f8;
border-top: 1px solid var(--color-border);
border-bottom: 1px solid var(--color-border);
flex-wrap: wrap;
gap: 0.5rem;
padding: 0.5rem;
```

---

## 13. Footer

### Estructura

**Elementos:**
1. Copyright notice
2. Iconos de redes sociales (Facebook, Twitter, Instagram, LinkedIn)

**Estilos:**
```css
border-top: 1px solid var(--color-border);
text-align: center;
padding: 1.5rem 1rem;
font-size: 0.9rem;
color: var(--color-secondary);
background-color: #fafafa;

/* Social icons */
display: flex;
justify-content: center;
gap: 1rem;
margin-top: 0.5rem;
```

---

## 14. Uso de Imágenes

### Imágenes Hero

**Fuente:** Unsplash (placeholder)
```css
background: url('...') center/cover no-repeat;
border-radius: 12px;
min-height: 320px;
box-shadow: 0 4px 12px rgba(0,0,0,0.08);
```

### Logos de Becas

**Placeholder:**
```css
width: 100%;
height: 100px;
background-color: #f0f0f0;
border-radius: 8px;
border: 2px dashed var(--color-border);
font-size: 0.8rem;
color: var(--color-secondary);
```

---

## 15. Accesibilidad

### Consideraciones

✓ Variables CSS para temas
✓ Contraste WCAG AA (mínimo)
✓ Focus states visibles
✓ Transiciones suaves
✓ Iconos complementados con texto
✓ Formularios con labels explícitos
✓ Border radius consistente (8-12px)
✓ Modo oscuro completo

### Estados de Focus

```css
input:focus,
select:focus {
  outline: none;
  border-color: var(--color-accent);
}

nav a:hover {
  background-color: var(--color-accent);
  color: #fff;
}
```

---

## 16. Notas de Implementación

### Stack Tecnológico
- HTML5 semántico
- CSS3 (Variables + Grid + Flexbox)
- JavaScript vanilla (toggle theme, Lucide icons)
- Google Fonts (CDN)
- Lucide Icons (CDN)

### Convenciones de Código
- Variables CSS en `:root` y `body.dark`
- Mobile-first approach
- Grid y Flexbox para layouts
- Transiciones para interactividad
- Sin preprocesadores CSS
- Sin framework JS (vanilla)

### Consistencia Entre Páginas
Todas las páginas comparten:
- Sistema de colores
- Tipografía (Inter + Poppins)
- Header y navegación
- Footer con redes sociales
- Toggle de modo oscuro
- Border radius (8-12px)
- Transiciones (0.2-0.3s)

---

## 17. Referencias de Diseño

**PDF de Diseño:** `Diseño Gráfico 2025.pdf`
**Carpeta Drive:** Ver `Sprint3Guia2LinkCarpeta.txt`

**Páginas implementadas:**
1. ✅ Página de inicio (home)
2. ✅ Página de búsqueda (tabla de becas)
3. ✅ Página de becas disponibles (grid + formulario)
4. ⏳ Trabajos Finales (pendiente)

---

**Versión:** 1.0
**Última actualización:** 2025-10-20
**Estado:** En desarrollo - Sprint 3
