# Entrega Final: Prototipo "¿Estás Becado?"

**Proyecto:** Plataforma de búsqueda de becas argentinas
**Sprint:** 5 - Integración, Movimiento y Evaluación Final
**Fecha:** Noviembre 2025
**Universidad:** UNComa

---

## 1. Prototipo Navegable

Se entrega un prototipo navegable compuesto por tres páginas principales:

1.  **Home (`index.html`):** Página de bienvenida y punto de partida.
2.  **Becas Disponibles (`becas.html`):** Muestra las becas en formato de tarjetas y un formulario de filtrado.
3.  **Búsqueda / Estado (`busqueda.html`):** Presenta el estado de las postulaciones en una tabla responsiva.

El prototipo incluye un *toggle* para modo oscuro, es completamente responsivo y sigue las guías de estilo definidas.

---

## 2. Guía Visual Actualizada (Style Tile)

Esta sección se basa en el archivo `STYLE_TILE.md`.

### 2.1. Paleta de Colores

#### Colores Principales (Light Mode)

| Color | Hex | Variable CSS | Uso | Muestra |
|---|---|---|---|---|
| **Azul Principal** | `#004aa3` | `--color-accent` | Accent, botones primarios, enlaces | ![#004aa3](https://dummyimage.com/80x40/004aa3/004aa3.png) |
| **Texto Oscuro** | `#222224` | `--color-text` | Texto principal, títulos | ![#222224](https://dummyimage.com/80x40/222224/222224.png) |
| **Texto Secundario**| `#4f4f4f` | `--color-secondary`| Texto de apoyo, subtítulos | ![#4f4f4f](https://dummyimage.com/80x40/4f4f4f/4f4f4f.png) |
| **Fondo Claro** | `#ffffff` | `--color-bg` | Fondo principal | ![#ffffff](https://dummyimage.com/80x40/ffffff/ffffff.png) |
| **Borde** | `#e0e0e0` | `--color-border` | Bordes, divisores | ![#e0e0e0](https://dummyimage.com/80x40/e0e0e0/e0e0e0.png) |

#### Colores de Estado

| Estado | Hex | Variable CSS | Uso |
|---|---|---|---|
| **Aprobado** | `#22c55e` | `--color-success` | Estados de éxito, confirmaciones |
| **En Evaluación**| `#eab308` | `--color-warning` | Alertas, estados pendientes |
| **Rechazado** | `#ef4444` | `--color-danger` | Errores, estados de rechazo |

### 2.2. Modo Oscuro (Dark Theme)

| Color | Hex | Variable CSS | Uso |
|---|---|---|---|
| **Fondo Oscuro** | `#222224` | `--color-bg` | Fondo principal |
| **Texto Claro** | `#f8f8f8` | `--color-text` | Texto principal |
| **Texto Secundario**| `#bdbdbd` | `--color-secondary`| Texto de apoyo |
| **Borde Oscuro** | `#3a3a3a` | `--color-border` | Bordes y divisores |

### 2.3. Tipografía

- **Inter:** Usada para el cuerpo de texto, párrafos y elementos de UI. Aporta legibilidad.
- **Poppins:** Usada para títulos y el logo. Aporta un toque moderno y amigable.

### 2.4. Iconografía

- **Biblioteca:** Lucide Icons, por su diseño limpio, ligero y consistente.

---

## 3. Justificación del Diseño

### 3.1. Estilo Visual y Coherencia

Se optó por un **estilo visual minimalista y limpio (Flat Design)**. Esta decisión busca reducir la carga cognitiva del usuario, permitiendo que se enfoque en la tarea principal: encontrar información sobre becas. La coherencia se mantiene mediante el uso riguroso de la paleta de colores, la tipografía y el espaciado definidos en la guía de estilo en todas las páginas.

### 3.2. Movimiento y Microinteracciones

El movimiento en la interfaz se utiliza con tres propósitos principales: **orientación, feedback y naturalidad**.

- **Orientación del Usuario:**
  - El estado `:active` en los enlaces de navegación, que cambia el fondo a azul, le confirma al usuario en qué sección del sitio se encuentra.

- **Feedback Visual:**
  - **Hover en Botones y Tarjetas:** Los botones se oscurecen y las tarjetas se elevan ligeramente al pasar el cursor. Esto comunica que son elementos interactivos.
  - **Toggle de Modo Oscuro:** El ícono cambia de luna a sol, proporcionando un feedback inmediato y claro del cambio de estado.
  - **Focus en Formularios:** El borde de los campos de input se resalta con el color de acento (`--color-accent`) cuando el usuario hace clic en ellos, guiando su atención.

- **Naturalidad y Fluidez:**
  - Se utilizan transiciones (`transition: all 0.3s ease`) en los efectos hover para que los cambios de estado no sean bruscos, sino suaves y agradables a la vista.

### 3.3. Accesibilidad y Usabilidad

- **Contraste de Color:** Se verificó que las combinaciones de color entre texto y fondo cumplen con los ratios de contraste recomendados por la WCAG, tanto en modo claro como oscuro.
- **Diseño Responsivo:** El layout se adapta a diferentes tamaños de pantalla, asegurando una experiencia consistente en móvil y escritorio.
- **Navegación Clara:** La estructura de navegación es simple y predecible.

---

## 4. Tabla de Patrones Aplicados

| Patrón de Diseño UI | Implementación en el Prototipo | Justificación |
| :--- | :--- | :--- |
| **Navegación Principal** | Menú horizontal en la cabecera (`<nav>`). | Proporciona acceso rápido y consistente a las secciones clave del sitio desde cualquier página. |
| **Llamada a la Acción (CTA)** | Botón "Descubrir Becas Disponibles" en la Home. | Guía al usuario hacia la acción principal y el propósito del sitio de manera clara e inmediata. |
| **Cards (Tarjetas)** | Grilla de becas en `becas.html`. | Permiten presentar información heterogénea de forma modular, escaneable y visualmente atractiva. |
| **Formulario de Filtros** | Formulario en la barra lateral de `becas.html`. | Mejora la usabilidad al permitir a los usuarios acotar la búsqueda de becas según sus criterios, reduciendo la sobrecarga de información. |
| **Tabla de Datos** | Lista de postulantes en `busqueda.html`. | Es el método más efectivo para mostrar datos tabulares y comparables, como el estado de una postulación. |
| **Toggle (Interruptor)** | Icono de luna/sol para el modo oscuro. | Ofrece una forma intuitiva y visual de cambiar entre dos estados (tema claro/oscuro), mejorando la personalización. |
| **Footer (Pie de página)** | Pie de página con enlaces a redes sociales. | Proporciona un espacio estándar para información secundaria y de contacto sin interferir con el contenido principal. |

---

## 5. Registro de Testeo

Esta sección se basa en el archivo `SIMULACION_TESTEO.md`.

### 5.1. Resumen de Hallazgos

Se realizaron dos simulaciones de testeo con las personas "Sofía" (principiante) y "Martín" (intermedio). Ambos usuarios valoraron positivamente la **limpieza del diseño** y la **claridad de la interfaz**. Sin embargo, se identificó un **punto de fricción crítico y recurrente**:

- **Funcionalidad Inactiva:** Tanto el formulario de filtro en la página de becas como la barra de búsqueda en la tabla de estados son elementos visuales sin funcionalidad. Esto generó confusión en la usuaria principiante ("¿Funcionó?") y frustración en el usuario intermedio ("Es un dead-end en la UI").

### 5.2. Mejoras Aplicadas y Sugerencias

- **Mejora Directa (No implementada en prototipo):** La principal mejora a realizar es **conectar la UI con lógica de JavaScript** para que los filtros y la búsqueda sean funcionales.
- **Sugerencia de Sofía:** Añadir feedback visual después de filtrar, como un texto "Mostrando 3 becas para ti".
- **Sugerencia de Martín:** Considerar mantener el scroll horizontal en la tabla en móviles para facilitar la comparación de datos, como alternativa a la vista de tarjetas.

---

## 6. Checklist de Estándares

| Criterio | Estado | Observaciones |
| :--- | :--- | :--- |
| **Accesibilidad** | | |
| Contraste de color adecuado | ✅ | Verificado en ambos temas (claro/oscuro). |
| Texto alternativo en imágenes | ⚠️ | Parcialmente implementado. Falta revisar imágenes decorativas. |
| Navegación por teclado | ✅ | La estructura del DOM permite una navegación lógica con Tab. |
| Semántica HTML | ✅ | Se utiliza HTML5 semántico (`<header>`, `<main>`, `<footer>`, `<nav>`). |
| **Usabilidad** | | |
| Navegación clara y consistente | ✅ | El menú principal es consistente en todas las páginas. |
| Feedback al usuario | ⚠️ | Buen feedback en microinteracciones (hover, focus), pero ausente en funciones clave (filtros). |
| Diseño responsivo | ✅ | El sitio se adapta correctamente a dispositivos móviles y de escritorio. |
| **Coherencia Visual** | | |
| Consistencia en colores | ✅ | Se usan las variables CSS definidas en toda la web. |
| Consistencia en tipografía | ✅ | La jerarquía y familias tipográficas se respetan. |
| Consistencia en espaciado | ✅ | Se mantiene un ritmo vertical y espaciado consistentes. |
| **Movimiento** | | |
| Transiciones suaves | ✅ | Los cambios de estado (hover) son fluidos. |
| Feedback con movimiento | ✅ | El hover en tarjetas y botones proporciona feedback. |
| Animaciones no intrusivas | ✅ | Las animaciones son sutiles y no distraen del contenido. |
