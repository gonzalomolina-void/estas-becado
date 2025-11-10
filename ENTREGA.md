# Entrega Final: Prototipo "¿Estás Becado?"

**Proyecto:** Plataforma de búsqueda de becas argentinas
**Cátedra:** Diseño Gráfico
**Universidad:** UNComa
**Fecha:** Noviembre 2025

---

## 1. Introducción y Visión del Proyecto

### 1.1. El Problema

Encontrar la beca adecuada puede ser un proceso abrumador y fragmentado. Los estudiantes a menudo navegan por innumerables sitios web, lidiando con información desactualizada y sistemas de búsqueda poco intuitivos. Esta dificultad provoca que muchos aspirantes talentosos pierdan oportunidades valiosas que podrían impulsar su futuro académico y profesional.

### 1.2. Nuestra Solución: ¿Estás Becado?

**¿Estás Becado?** es una plataforma centralizada y amigable, diseñada para simplificar y democratizar el acceso a oportunidades de becas. Nuestra misión es conectar a los estudiantes con el apoyo financiero que necesitan de una manera rápida, eficiente y sin estrés.

Este prototipo funcional demuestra las características esenciales de nuestra visión:

*   **Inicio Atractivo:** Una página principal que comunica claramente nuestra propuesta de valor e invita a la acción.
*   **Catálogo de Becas:** Una vista de todas las becas disponibles, con filtros inteligentes para que los usuarios puedan segmentar las oportunidades.
*   **Búsqueda y Estado:** Un motor de búsqueda dedicado y una tabla para consultar el estado de las postulaciones.

### 1.3. Visión a Futuro

Este prototipo es solo el comienzo. Planeamos evolucionar **¿Estás Becado?** para incluir perfiles de usuario personalizados, un sistema de aplicación simplificado y alianzas con instituciones para asegurar que nuestra base de datos sea la más completa y actualizada.

---

## 2. Guía Visual y de Estilo

Esta guía define los elementos visuales y de interacción que aseguran una experiencia de usuario coherente y estéticamente agradable en toda la plataforma.

### 2.1. Paleta de Colores

La paleta está diseñada para ser clara, accesible y profesional, con un modo oscuro para mejorar la comodidad visual en condiciones de poca luz.

#### Colores Principales (Light Mode)

| Color | Hex | Variable CSS | Uso | Muestra |
|---|---|---|---|---|
| **Azul Principal** | `#004aa3` | `--color-accent` | Accent, botones primarios, enlaces | ![#004aa3](https://dummyimage.com/80x40/004aa3/004aa3.png) |
| **Texto Oscuro** | `#222224` | `--color-text` | Texto principal, títulos | ![#222224](https://dummyimage.com/80x40/222224/222224.png) |
| **Texto Secundario**| `#4f4f4f` | `--color-secondary`| Texto de apoyo, subtítulos | ![#4f4f4f](https://dummyimage.com/80x40/4f4f4f/4f4f4f.png) |
| **Fondo Claro** | `#ffffff` | `--color-bg` | Fondo principal | ![#ffffff](https://dummyimage.com/80x40/ffffff/ffffff.png) |
| **Borde** | `#e0e0e0` | `--color-border` | Bordes, divisores | ![#e0e0e0](https://dummyimage.com/80x40/e0e0e0/e0e0e0.png) |

#### Paleta Oscura (Dark Theme)

| Color | Hex | Variable CSS | Uso |
|---|---|---|---|
| **Fondo Oscuro** | `#222224` | `--color-bg` | Fondo principal |
| **Texto Claro** | `#f8f8f8` | `--color-text` | Texto principal |
| **Texto Secundario**| `#bdbdbd` | `--color-secondary`| Texto de apoyo |
| **Borde Oscuro** | `#3a3a3a` | `--color-border` | Bordes y divisores |
| **Fondo Contenedor**| `#2c2c2c` | N/A | Fondo de `nav`, `cards`, `form`, etc. |

#### Colores de Estado

Se utilizan para comunicar el resultado de las postulaciones de manera clara e inmediata.

| Estado | Hex | Variable CSS | Uso |
|---|---|---|---|
| **Aprobado** | `#22c55e` | `--color-success` | Estados de éxito, confirmaciones |
| **En Evaluación**| `#eab308` | `--color-warning` | Alertas, estados pendientes |
| **Rechazado** | `#ef4444` | `--color-danger` | Errores, estados de rechazo |

### 2.2. Tipografía

La combinación de **Poppins** para títulos y **Inter** para el cuerpo de texto crea una jerarquía visual clara y una excelente legibilidad.

*   **Títulos (Poppins):** Aporta un carácter moderno y amigable, ideal para captar la atención.
*   **Cuerpo (Inter):** Es una fuente sans-serif altamente legible en pantalla, perfecta para párrafos y elementos de UI.

#### Jerarquía Tipográfica

| Elemento | Familia | Tamaño | Peso |
|---|---|---|---|
| Logo | `Poppins` | `2.25rem` | `600` |
| Títulos (h2) | `Poppins` | `2.5rem` | `400` |
| Subtítulos (h3) | `Poppins` | `1.75rem` | `400` |
| Cuerpo de texto | `Inter` | `1.05rem` | `400` |
| Navegación/Botones | `Inter` | `1rem` | `600` |

### 2.3. Componentes UI

Los componentes son los bloques de construcción de la interfaz. Su diseño consistente es clave para la usabilidad.

*   **Botones (`.btn`):** Usan el color de acento para destacar las acciones principales. El cambio de color en `:hover` proporciona feedback inmediato al usuario.
*   **Tarjetas (`.beca-card`):** Agrupan la información de cada beca. El sutil `box-shadow` y la animación en `:hover` las hacen parecer interactivas y elevadas del fondo.
*   **Formularios:** Los campos tienen un padding generoso y un borde que cambia de color en `:focus`, guiando al usuario y mostrando claramente el campo activo.
*   **Tabla (`.table-container`):** Diseñada para ser legible. En móvil, se transforma en un formato de "tarjetas" por fila usando `data-label` para mantener la legibilidad en pantallas pequeñas, una excelente práctica de diseño responsivo y accesible.

### 2.4. Iconografía

Se utiliza la biblioteca **Lucide Icons** por su estilo limpio, ligero y consistente. Los iconos (`search`, `moon`, `sun`, etc.) son universalmente reconocidos y refuerzan la funcionalidad sin necesidad de texto.

### 2.5. Layout y Espaciado

El diseño se basa en un ancho máximo (`1200px`) y un sistema de espaciado consistente (`gap`, `padding`, `margin`) que crea un ritmo visual ordenado y aireado, evitando la sobrecarga cognitiva.

---

## 3. Justificación del Diseño

Las decisiones de diseño no son arbitrarias. Se fundamentan en principios de percepción visual, usabilidad y accesibilidad para crear una experiencia efectiva y agradable.

### 3.1. Principios de Percepción Visual (Gestalt)

*   **Ley de Proximidad:** Los elementos relacionados se agrupan visualmente. Esto es evidente en los formularios, donde cada `label` está junto a su `input`, y en las tarjetas (`.beca-card`), donde el logo y el nombre de la beca forman una unidad cohesiva.
*   **Ley de Similaridad:** Los elementos que comparten características visuales se perciben como relacionados. Todos los botones de acción principal (`.btn`) son azules, y todos los enlaces de navegación tienen el mismo estilo, creando consistencia y previsibilidad.
*   **Jerarquía Visual:** Se guía la atención del usuario hacia los elementos más importantes. El tamaño y peso de los títulos (`h2`, `h3`) los distingue del texto de párrafo. El color de acento en el botón "Descubrir Becas" en la página de inicio lo convierte en el punto focal principal.

### 3.2. Principios de Usabilidad

*   **Consistencia y Estándares:** La navegación, el footer y los estilos de los componentes se mantienen consistentes a través de las tres páginas (`index.html`, `becas.html`, `busqueda.html`). Esto reduce la carga cognitiva del usuario, que no tiene que aprender a usar la interfaz en cada página.
*   **Feedback del Sistema:** La interfaz comunica constantemente su estado.
    *   El estado `:hover` en botones y tarjetas.
    *   El enlace `.active` en la navegación, que muestra al usuario dónde se encuentra.
    *   Los colores de estado (`Aprobado`, `En evaluación`, `Rechazado`) en la tabla de búsqueda.
    *   El cambio de icono (luna/sol) en el botón de tema.
*   **Diseño Estético y Minimalista:** La interfaz evita la información irrelevante. El uso generoso de espacios en blanco (`margin`, `padding`) y una paleta de colores limitada ayudan a que el contenido sea el protagonista, facilitando la concentración del usuario en su tarea.
*   **Reconocimiento sobre Recuerdo:** En la página de becas, en lugar de forzar al usuario a recordar y escribir los filtros, se le presentan opciones claras en menús desplegables (`select`), facilitando el proceso de búsqueda.

### 3.3. Principios de Accesibilidad (A11y)

*   **Contraste de Color:** La paleta de colores fue elegida para asegurar un buen contraste entre el texto y el fondo (ej. texto `#222224` sobre fondo `#ffffff`), lo cual es crucial para usuarios con discapacidades visuales.
*   **Navegación por Teclado:** El estado `:focus` visible en los campos de formulario (`border-color: var(--color-accent)`) permite a los usuarios que navegan con teclado saber siempre dónde se encuentran.
*   **HTML Semántico:** El uso correcto de etiquetas como `<main>`, `<nav>`, `<header>`, `<footer>`, y `<label for="...">` estructura el documento de forma lógica, permitiendo que los lectores de pantalla interpreten el contenido correctamente.
*   **Accesibilidad en Componentes:**
    *   El menú de hamburguesa en móvil utiliza atributos `aria-label` y `aria-expanded` para comunicar su propósito y estado a las tecnologías de asistencia.
    *   El uso de `data-label` en la tabla responsiva permite que los lectores de pantalla anuncien el encabezado de cada celda, manteniendo el contexto en la vista móvil.
    *   Las imágenes, como el logo, incluyen un atributo `alt` descriptivo.

---

## 4. Plan de Validación y Testeo

Para asegurar que el diseño no solo es estético sino también funcional, se propone el siguiente plan de validación con usuarios. Este documento sirve como evidencia del proceso de testeo.

### 4.1. Objetivos del Test

1.  Evaluar la facilidad con la que un nuevo usuario puede encontrar las becas disponibles.
2.  Determinar si los filtros del formulario "¿A qué becas califico?" son intuitivos y útiles.
3.  Verificar si los usuarios entienden la información presentada en la tabla de "Estado de Becas".
4.  Identificar puntos de fricción o confusión en el flujo de navegación general.
5.  Recoger feedback sobre la percepción general del diseño y la claridad de la propuesta de valor.

### 4.2. Perfil de Usuario para Testeo

*   **Grupo Principal:** Estudiantes de entre 17 y 25 años, cursando el último año de secundaria o los primeros años de una carrera universitaria.
*   **Grupo Secundario:** Estudiantes de posgrado o profesionales jóvenes (25-35 años) buscando becas de especialización.
*   **Criterio:** Poca o ninguna familiaridad previa con el prototipo "¿Estás Becado?".

### 4.3. Metodología

Se propone un **Test de Usabilidad Moderado**. Un moderador guiará al participante a través de una serie de tareas, observando sus acciones y animándolo a "pensar en voz alta". Las sesiones se realizarán de forma remota, compartiendo pantalla.

### 4.4. Guion de Tareas

Se le presentará al usuario el prototipo y se le pedirá que realice las siguientes tareas:

*   **Tarea 1 (Primera Impresión):** "Estás en la página de inicio. Sin hacer clic en nada todavía, descríbeme qué crees que puedes hacer en este sitio web."
*   **Tarea 2 (Navegación Principal):** "Imagina que quieres ver todas las becas que ofrece el sitio. ¿Qué harías?"
*   **Tarea 3 (Filtrado de Becas):** "Ahora estás en la sección de becas. Eres un estudiante de licenciatura. Usa el formulario para ver a qué becas podrías calificar."
*   **Tarea 4 (Consulta de Estado):** "Un amigo tuyo, Giacomo Guillizon, aplicó a una beca. Ve a la sección correspondiente y dime cuál es el estado de su postulación."
*   **Tarea 5 (Funcionalidad Adicional):** "Explora el sitio libremente por un minuto. ¿Hay algo que te sorprenda o te confunda? Intenta cambiar el sitio a modo oscuro."

### 4.5. Plantilla de Recolección de Datos

Para cada participante, se utilizará una tabla como la siguiente para registrar las observaciones.

| Tarea | ¿Completada con Éxito? (Sí/No/Parcial) | Tiempo (aprox.) | Observaciones del Moderador (Dudas, errores, clics incorrectos) | Comentarios del Usuario (en voz alta) |
|---|---|---|---|---|
| **Tarea 1** | | | | |
| **Tarea 2** | | | | |
| **Tarea 3** | | | | |
| **Tarea 4** | | | | |
| **Tarea 5** | | | | |

**Preguntas Post-Test:**
1. En una escala de 1 a 5 (donde 1 es muy difícil y 5 es muy fácil), ¿qué tan fácil te resultó usar el sitio?
2. ¿Qué fue lo que más te gustó del diseño?
3. ¿Qué fue lo que menos te gustó o lo que te pareció más confuso?
4. ¿Hay algo que esperabas encontrar y no encontraste?
5. ¿Tienes alguna sugerencia para mejorar el sitio?
