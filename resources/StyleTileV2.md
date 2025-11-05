# Style Tile - ¿Estás Becado? (Implementación Actual)

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

| Estado | RGBA | Hex aproximado |
|--------|------|----------------|
| **Aprobado (Verde)** | `rgba(68,95,8,1)`, `rgba(75,88,15,1)`, `rgba(65,98,5,1)` | `#445f08`, `#4b580f`, `#416205` |
| **En Evaluación (Púrpura/Rosa)** | `rgba(118,63,108,1)`, `rgba(122,67,104,1)`, `rgba(115,60,111,1)` | `#763f6c`, `#7a4368`, `#733c6f` |
| **Rechazado (Rojo)** | `rgba(175,4,4,1)` | `#af0404` |

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

/* Títulos principales (h2) */
font-family: 'Poppins';
font-weight: SemiBold;
font-size: 40px;
text-align: center;

/* Títulos secundarios */
font-family: 'Poppins';
font-weight: SemiBold;
font-size: 28px;

/* Subtítulos de sección (home) */
font-family: 'Poppins';
font-weight: SemiBold;
font-size: 25px;

/* Navegación */
font-family: 'Inter';
font-weight: Semi Bold;
font-size: 16px;

/* Cuerpo de texto */
font-family: 'Inter' (implícito);
font-size: 16px;
font-weight: Regular;

/* Labels de formulario */
font-family: 'Inter';
font-weight: Semi Bold;
font-size: 15px;

/* Inputs y selects */
font-family: 'Inter';
font-weight: Regular;
font-size: 16px;

/* Botones */
font-family: 'Inter';
font-weight: Semi Bold;
font-size: 16px;

/* Nombres de becas en cards */
font-family: 'Inter';
font-weight: Semi Bold;
font-size: 15px;

/* Tabla contenido */
font-family: 'Inter';
font-weight: Regular;
font-size: 14px;

/* Tabla headers */
font-family: 'Inter';
font-weight: Semi Bold;
font-size: 14px;

/* Logo placeholder */
font-family: 'Inter';
font-weight: Regular;
font-size: 12px;

/* Footer */
font-family: 'Inter';
font-weight: Regular;
font-size: 14px;
```

---

## 3. Componentes UI

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

### Tarjetas (Cards)

**Tarjeta de Beca:**
```css
width: 281px;
height: 187px;
background: rgba(255,255,255,1);
padding: 25px 25px;
border-radius: 12px;
```

### Inputs y Formularios

**Campo de texto/Select:**
```css
background: rgba(255,255,255,1);
padding: 13px 17px; /* o 13px 21px */
border-radius: 8px;
font-size: 16px;
```

---

## 4. Notas de Implementación

*   **Código Auto-generado:** El HTML y CSS parecen haber sido exportados desde una herramienta de diseño. Usan clases no semánticas (ej. `v1_17`, `v7_28`) y posicionamiento absoluto, lo que hace que el sitio no sea responsivo.
*   **Inconsistencias:** Existen variaciones en los colores y estilos entre las diferentes páginas (`home`, `busqueda`, `becas_disponibles`). Por ejemplo, el color del botón principal y los colores de estado de las becas no son uniformes.
*   **Funcionalidad Faltante:** No hay interactividad. Los botones de "hover", los "focus" en los inputs y el toggle de modo oscuro no están implementados.
*   **Tipografía:** Las familias tipográficas (Poppins e Inter) son consistentes, pero los tamaños y pesos varían ligeramente entre elementos similares en diferentes páginas.
