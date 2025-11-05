# Style Tile - ¿Estás Becado? (IMPLEMENTACIÓN ACTUAL)

**Proyecto:** Plataforma de búsqueda de becas argentinas
**Sprint:** 3 - Diseño Gráfico
**Fecha:** Octubre 2025
**Universidad:** UNComa

Este documento refleja los estilos **realmente implementados** en las carpetas `home/`, `busqueda/` y `becas_disponibles/`.

---

## 1. Paleta de Colores

### Colores Principales Implementados

| Color | Hex/RGBA | Uso | Carpeta |
|-------|----------|-----|---------|
| **Azul Principal (variante 1)** | `rgba(3,84,180,1)` / `#0354b4` | Botón "Descubrir Becas" | home |
| **Azul Principal (variante 2)** | `rgba(0,87,183,1)` / `#0057b7` | Botón "Buscar" | becas_disponibles |
| **Púrpura Oscuro** | `rgba(54,33,129,1)` / `#362181` | Botón "Filtros" | busqueda |
| **Texto Principal** | `rgba(34,34,36,1)` / `#222224` | Títulos, texto principal | todas |
| **Texto Secundario 1** | `rgba(50,50,50,1)` / `#323232` | Subtítulos, cuerpo | home |
| **Texto Secundario 2** | `rgba(80,80,80,1)` / `#505050` | Placeholder búsqueda | busqueda |
| **Texto Secundario 3** | `rgba(81,81,81,1)` / `#515151` | Texto de apoyo | home |
| **Texto Muted** | `rgba(94,94,94,1)` / `#5e5e5e` | Iconos, borders, placeholders | todas |
| **Texto Footer** | `rgba(60,60,60,1)` / `#3c3c3c` | Copyright | home |
| **Fondo Blanco** | `rgba(255,255,255,1)` / `#ffffff` | Background principal, cards, inputs | todas |
| **Fondo Navegación** | `rgba(248,248,248,1)` / `#f8f8f8` | Nav bar, header de tabla | todas |
| **Fondo Form/Footer** | `rgba(250,250,250,1)` / `#fafafa` | Form containers, footer | becas_disponibles |
| **Fondo Logo Placeholder** | `rgba(240,240,240,1)` / `#f0f0f0` | Placeholder logos becas | becas_disponibles |

### Colores de Estado (Implementación en Búsqueda)

| Estado | RGBA | Hex aproximado | Diferencia con STYLE_TILE.md |
|--------|------|----------------|------------------------------|
| **Aprobado (Verde)** | `rgba(68,95,8,1)`, `rgba(75,88,15,1)`, `rgba(65,98,5,1)` | `#445f08`, `#4b580f`, `#416205` | ❌ Más oscuros que `#22c55e` especificado |
| **En Evaluación (Púrpura/Rosa)** | `rgba(118,63,108,1)`, `rgba(122,67,104,1)`, `rgba(115,60,111,1)` | `#763f6c`, `#7a4368`, `#733c6f` | ❌ Color completamente diferente (debería ser amarillo `#eab308`) |
| **Rechazado (Rojo)** | `rgba(175,4,4,1)` | `#af0404` | ✅ Similar a `#ef4444` pero más oscuro |

---

## 2. Tipografía

### Familias Tipográficas

**Google Fonts:**
- **Poppins** (Regular, SemiBold) - Logo, títulos principales
- **Inter** (Regular, Semi Bold) - Navegación, cuerpo, inputs

### Jerarquía Tipográfica Implementada

```css
/* Logo principal */
font-family: 'Poppins';
font-weight: Regular;
font-size: 36px;
color: rgba(34,34,36,1);

/* Títulos principales (h2) */
font-family: 'Poppins';
font-weight: SemiBold;
font-size: 40px;        /* busqueda, becas_disponibles */
color: rgba(34,34,36,1);
text-align: center;

/* Títulos secundarios */
font-family: 'Poppins';
font-weight: SemiBold;
font-size: 28px;        /* becas_disponibles */
color: rgba(34,34,36,1);

/* Subtítulos de sección (home) */
font-family: 'Poppins';
font-weight: SemiBold;
font-size: 25px;
color: rgba(34,34,36,1);

/* Navegación */
font-family: 'Inter';
font-weight: Semi Bold;
font-size: 16px;
color: rgba(34,34,36,1);

/* Cuerpo de texto */
font-family: 'Inter' (implícito);
font-size: 16px;
font-weight: Regular;
color: rgba(50,50,50,1) - rgba(81,81,81,1);

/* Labels de formulario */
font-family: 'Inter';
font-weight: Semi Bold;
font-size: 15px;
color: rgba(34,34,36,1);

/* Inputs y selects */
font-family: 'Inter';
font-weight: Regular;
font-size: 16px;
color: rgba(34,34,36,1);

/* Botones */
font-family: 'Inter';
font-weight: Semi Bold;
font-size: 16px;
color: rgba(255,255,255,1);

/* Nombres de becas en cards */
font-family: 'Inter';
font-weight: Semi Bold;
font-size: 15px;
color: rgba(34,34,36,1);

/* Tabla contenido */
font-family: 'Inter';
font-weight: Regular;
font-size: 14px;
color: rgba(34,34,36,1);

/* Tabla headers */
font-family: 'Inter';
font-weight: Semi Bold;
font-size: 14px;
color: rgba(34,34,36,1);

/* Logo placeholder */
font-family: 'Inter';
font-weight: Regular;
font-size: 12px;
color: rgba(94,94,94,1);

/* Footer */
font-family: 'Inter';
font-weight: Regular;
font-size: 14px;
color: rgba(60,60,60,1) / rgba(50,50,50,1) / rgba(94,94,94,1);
```

---

## 3. Sistema de Espaciado

### Valores Implementados

```css
/* Padding - Botones */
padding: 12px 24px;     /* Botón principal (home) */
padding: 12px 40px;     /* Botón buscar (becas_disponibles) */
padding: 12px 20px;     /* Nav items */

/* Padding - Containers */
padding: 24px 860px;    /* Header */
padding: 9px 8px;       /* Nav bar */
padding: 48px 24px;     /* Main content (home) */
padding: 48px 442px;    /* Main content (becas_disponibles) */
padding: 25px 25px;     /* Cards de becas */
padding: 32px 33px;     /* Form container */
padding: 39px 16px;     /* Footer */

/* Padding - Inputs/Fields */
padding: 13px 17px;     /* Search input */
padding: 13px 21px;     /* Select/dropdown */
padding: 16px 16px;     /* Table cells */

/* Margins */
margin: 8px;            /* Nav bar, form fields */
margin: 32px;           /* Sections, cards grid */
margin: 16px;           /* Social icons, footer elements */
margin: 24px;           /* Form sidebar */

/* Gaps (implícito en posicionamiento) */
/* Cards grid: ~25-26px gap vertical/horizontal */
/* Form fields: ~23px gap vertical */
```

### Contenedores

```css
/* No hay max-width definido - layouts con position absolute */
/* Widths fijos por diseño:
   - Logo: 200px × 60px
   - Nav items: 163px, 263px, 166px
   - Cards: 281px × 187px
   - Form: 400px
   - Content principal: variable con padding
*/
```

---

## 4. Componentes UI

### Botones

**Botón Primario Azul (home):**
```css
background-color: rgba(3,84,180,1);     /* #0354b4 */
color: rgba(255,255,255,1);
padding: 12px 24px;
font-size: 16px;
font-weight: Semi Bold;
border-radius: 8px;
```

**Botón Primario Azul (becas_disponibles):**
```css
background-color: rgba(0,87,183,1);     /* #0057b7 */
color: rgba(255,255,255,1);
padding: 12px 40px;
font-size: 16px;
font-weight: Semi Bold;
border-radius: 8px;
```

**Botón Filtros (busqueda):**
```css
background-color: rgba(54,33,129,1);    /* #362181 - Púrpura */
color: rgba(255,255,255,1);
padding: 12px 24px;
font-size: 16px;
font-weight: Semi Bold;
border-radius: 8px;
```

**Botones Navegación:**
```css
background: url("../images/..."); /* Con imagen de fondo */
padding: 12px 20px;
border-radius: 8px;
color: rgba(34,34,36,1);
font-size: 16px;
font-weight: Semi Bold;
```

### Tarjetas (Cards)

**Tarjeta de Beca:**
```css
width: 281px;
height: 187px;
background: rgba(255,255,255,1);
padding: 25px 25px;
margin: -1px;
border-radius: 12px;

/* Logo placeholder */
width: 231px;
height: 100px;
background: rgba(240,240,240,1);
border-radius: 8px;

/* Nombre beca */
font-family: 'Inter';
font-weight: Semi Bold;
font-size: 15px;
color: rgba(34,34,36,1);
text-align: center;
```

### Inputs y Formularios

**Campo de texto numérico (Edad):**
```css
width: 334px;
height: 45px;
background: rgba(255,255,255,1);
padding: 13px 17px;
border-radius: 8px;
font-size: 16px;
color: rgba(34,34,36,1);
```

**Select/Dropdown:**
```css
width: 334px;
height: 48px;
background: rgba(255,255,255,1);
padding: 13px 21px;
border-radius: 8px;
font-size: 16px;
color: rgba(34,34,36,1);
```

**Search Input:**
```css
width: 100%;  /* Variable */
height: 42px;
background: rgba(255,255,255,1);
padding: 9px 17px;
border-radius: 8px;
font-size: 16px;
color: rgba(80,80,80,1);    /* Placeholder */
```

**Form Container:**
```css
width: 400px;
background: rgba(250,250,250,1);
padding: 32px 33px;
border-radius: 12px;
```

### Tabla

**Tabla de Becas:**
```css
/* Container */
width: 100%;
background: rgba(255,255,255,1);
padding: 1px 1px;
border-radius: 8px;

/* Header */
background: rgba(248,248,248,1);
padding: 16px 16px;
font-weight: Semi Bold;
font-size: 14px;
color: rgba(34,34,36,1);

/* Cells */
padding: 16px 16px;
font-weight: Regular;
font-size: 14px;
color: rgba(34,34,36,1);

/* Estado colors */
color: rgba(68,95,8,1);      /* Aprobado - verde oscuro */
color: rgba(118,63,108,1);   /* En evaluación - púrpura */
color: rgba(175,4,4,1);      /* Rechazado - rojo oscuro */
```

---

## 5. Bordes y Sombras

### Border Radius Implementado

```css
.radius-sm: 8px;   /* Inputs, botones, nav items, placeholders */
.radius-md: 12px;  /* Cards, form containers, hero images (home) */
```

### Box Shadows

```css
/* Sombra suave (hero image en home) */
box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.08);
```

**Nota:** No se observan sombras en hover en la implementación actual (solo CSS estático).

### Borders

```css
/* Iconos sociales */
border: 2px solid rgba(94,94,94,1);

/* No hay borders visibles en inputs/containers - solo backgrounds */
```

---

## 6. Iconografía

### Sistema de Iconos

**Iconos como bordes SVG:**
- Facebook, Twitter, Instagram, LinkedIn implementados con `border: 2px solid rgba(94,94,94,1)`
- Ícono de búsqueda: `border: 2px solid rgba(34,34,36,1)`
- Emoji toggle modo oscuro: 🌙 (texto, 19px)

**Color:**
```css
color: rgba(94,94,94,1);      /* Iconos sociales */
color: rgba(34,34,36,1);      /* Icono búsqueda */
```

---

## 7. Logo y Branding

### Logo Principal

```css
/* Texto "¿Estás Becado?" */
font-family: 'Poppins';
font-weight: Regular;
font-size: 36px;
/* Color: definido por imagen PNG */
width: 200px;
height: 60px;
```

**Nota:** El logo usa `color: url("../images/...")` que no es válido en CSS - sugiere que el diseño depende de imágenes PNG en lugar de texto estilizado.

---

## 8. Navegación

### Estructura del Header

**Elementos:**
1. Logo (200px × 60px, centrado)
2. Barra de navegación con items:
   - ¿Estás Becado? (163px)
   - ¿A qué Becas puedo aplicar? (263px)
   - Trabajos Finales (166px)
3. Toggle modo oscuro (🌙 emoji, 36px × 31px, derecha)

**Estilos:**
```css
/* Header */
width: 100%;
height: 93px;
padding: 24px 860px;  /* Centrado fijo */

/* Nav */
width: 100%;
height: 68px;
background: rgba(248,248,248,1);
padding: 9px 8px;
margin: 8px;

/* Nav items */
padding: 12px 20px;
border-radius: 8px;
font-family: 'Inter';
font-weight: Semi Bold;
font-size: 16px;
color: rgba(34,34,36,1);
```

---

## 9. Footer

### Estructura

**Elementos:**
1. Copyright notice
2. Iconos de redes sociales (Facebook, Twitter, Instagram, LinkedIn)

**Estilos:**
```css
/* Footer (home) */
width: 100%;
height: 124px;
background: rgba(255,255,255,1);
padding: 39px 16px;
margin: 14px;

/* Footer (becas_disponibles, busqueda) */
background: rgba(250,250,250,1);

/* Copyright */
font-family: 'Inter';
font-weight: Regular;
font-size: 14px;
color: rgba(60,60,60,1);      /* home */
color: rgba(50,50,50,1);      /* busqueda */
color: rgba(94,94,94,1);      /* becas_disponibles */
text-align: center;

/* Social icons */
width: 24px;
height: 24px;
margin: 16px (spacing);
border: 2px solid rgba(94,94,94,1);
```

---

## 10. Modo Oscuro

**Estado:** ❌ NO IMPLEMENTADO

El emoji 🌙 está presente pero no hay:
- CSS para `body.dark`
- Variables CSS alternativas
- JavaScript para toggle

---

## 11. Variables CSS

**Estado:** ❌ NO IMPLEMENTADAS

No se encontró uso de CSS custom properties (`:root`). Todos los valores están hardcoded con `rgba()`.

---

## 12. Accesibilidad

### Observaciones

❌ No hay estados de focus visibles
❌ No hay transiciones implementadas
❌ No hay estados hover
❌ Color como URL inválida en logo
❌ Nombres de clase no semánticos (v1_2, v7_3, v13_161)
✅ Border radius consistente (8-12px)
⚠️ Contraste: algunos grises pueden estar por debajo de WCAG AA

---

## 13. Diferencias Clave con STYLE_TILE.md Original

### Colores

| Elemento | STYLE_TILE.md | Implementación Actual | ¿Coincide? |
|----------|---------------|----------------------|------------|
| Azul Principal | `#0057b7` | `#0354b4` (home), `#0057b7` (becas_disp) | ⚠️ Parcial |
| Estado Aprobado | `#22c55e` (verde brillante) | `#445f08` (verde oscuro) | ❌ No |
| Estado En Evaluación | `#eab308` (amarillo) | `#763f6c` (púrpura/rosa) | ❌ No |
| Estado Rechazado | `#ef4444` (rojo) | `#af0404` (rojo oscuro) | ⚠️ Similar |
| Botón Filtros | N/A | `#362181` (púrpura) | ❌ No especificado |
| Fondo Footer | `#fafafa` | `#ffffff` (home), `#fafafa` (otros) | ⚠️ Parcial |

### Tipografía

| Elemento | STYLE_TILE.md | Implementación Actual | ¿Coincide? |
|----------|---------------|----------------------|------------|
| h2 | 2.5rem (40px) ✅ | 40px | ✅ Sí |
| h3 | 1.75rem (28px) ✅ | 28px | ✅ Sí |
| Cuerpo | 1.05rem (~17px) | 16px | ⚠️ Cercano |
| Nav | 1rem (16px) ✅ | 16px | ✅ Sí |
| Tabla | N/A | 14px | ⚠️ No especificado |
| Nombres becas | 0.95rem (~15px) ✅ | 15px | ✅ Sí |

### Funcionalidades

| Feature | STYLE_TILE.md | Implementación Actual |
|---------|---------------|----------------------|
| Modo Oscuro | ✅ Especificado | ❌ No implementado |
| Variables CSS | ✅ Especificado | ❌ No implementadas |
| Transiciones | ✅ 0.2-0.3s | ❌ No implementadas |
| Hover States | ✅ Especificados | ❌ No implementados |
| Responsive | ✅ Mobile-first | ⚠️ Layout fijo con position absolute |

---

## 14. Notas de Implementación

### Stack Tecnológico Actual

- HTML5 básico (no semántico)
- CSS3 con valores hardcoded
- Imágenes PNG para backgrounds/logos
- Sin JavaScript visible
- Sin Google Fonts CDN en CSS (links en HTML)
- Sin Lucide Icons (iconos como borders SVG)

### Estilo de Código

- **Nombres de clase:** Generados automáticamente (v1_X, v7_X, v13_X)
- **Posicionamiento:** `position: absolute` con coordenadas fijas
- **Responsividad:** ❌ No implementada (layouts fijos)
- **Reutilización:** ❌ Sin clases utilitarias
- **Mantenibilidad:** ⚠️ Baja (hardcoded values, nombres no descriptivos)

### Apariencia del código

Este código parece haber sido **generado por una herramienta de diseño visual** (posiblemente Figma, Adobe XD, o similar con export to HTML/CSS), ya que:

1. Nombres de clase auto-generados
2. Todo posicionado con `position: absolute`
3. Referencias a imágenes PNG para backgrounds
4. Sin uso de Flexbox o Grid
5. Sin semántica HTML

---

## 15. Recomendaciones

### Prioridad Alta

1. **Unificar color azul principal** → usar `#0057b7` en todas las páginas
2. **Corregir colores de estado** → implementar verde `#22c55e`, amarillo `#eab308`, rojo `#ef4444`
3. **Implementar variables CSS** → facilitar mantenimiento
4. **Refactorizar HTML/CSS** → usar clases semánticas y Flexbox/Grid

### Prioridad Media

5. **Agregar estados hover/focus** → mejorar UX
6. **Implementar transiciones** → suavizar interacciones
7. **Agregar modo oscuro funcional** → según especificación
8. **Responsive design** → media queries mobile-first

### Prioridad Baja

9. Optimizar imágenes/icons
10. Agregar animaciones sutiles
11. Mejorar accesibilidad (ARIA, contraste)

---

**Versión:** 1.0 (Análisis de implementación actual)
**Última actualización:** 2025-10-28
**Estado:** Documentación de código existente
**Herramienta:** Análisis manual de HTML/CSS
