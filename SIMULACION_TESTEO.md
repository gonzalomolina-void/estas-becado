# Simulación de Test de Usabilidad

Este documento contiene los resultados de dos simulaciones de test de usabilidad basadas en personas para el prototipo "¿Estás Becado?".

---

## Persona 1: Sofía (Usuaria Principiante)

*   **Perfil:** 18 años, recién graduada de secundaria. Busca becas por primera vez. Representa al usuario promedio, con conocimientos básicos de tecnología. Valora la claridad y la facilidad de uso.

### 1.1. Narración de la Simulación ("Pensando en voz alta")

*   **Tarea 1 (Primera Impresión):** "Ok, veo una foto de estudiantes y un título grande: 'Tu camino hacia una beca comienza aquí'. Es bastante claro, es un sitio para encontrar becas. Hay un botón azul grande que dice 'Descubrir Becas Disponibles', supongo que ahí es donde debo empezar. Parece fácil."
*   **Tarea 2 (Navegación Principal):** "Haría clic en el botón azul grande. *[Hace clic]*. Ok, me llevó a una página nueva con muchas tarjetas de becas. El título dice 'Becas disponibles'. El enlace del menú '¿A qué Becas puedo aplicar?' ahora está resaltado en azul, así que sé dónde estoy. Funcionó como esperaba."
*   **Tarea 3 (Filtrado de Becas):** "Veo el formulario a la derecha. Lleno mi edad, 18. En 'Nivel de estudios', elijo 'Licenciatura'. Dejo lo demás como está y hago clic en el botón 'Buscar'. ... *[Pausa]* ... Hmm, no pasó nada. La página no cambió. ¿Funcionó? ¿O las becas que se muestran ya son las filtradas? No estoy segura. Me siento un poco confundida. Esperaba que la lista de tarjetas de la izquierda se actualizara o me mostrara un mensaje." **(Punto de fricción identificado)**
*   **Tarea 4 (Consulta de Estado):** "Vuelvo al menú de arriba y veo 'Estado de Becas'. Hago clic ahí. Me aparece una tabla. Busco la columna 'Nombre del postulante' y leo hasta encontrar 'Giacomo Guillizon'. Al lado dice 'Aprobado' en verde. ¡Eso es genial! El color verde lo hace muy fácil de identificar. Esto fue muy claro."
*   **Tarea 5 (Funcionalidad Adicional):** "En el menú de arriba, al final, veo un icono de una luna. La luna normalmente significa 'noche' o 'modo oscuro'. Voy a hacer clic. *[Hace clic]*. ¡Sí! Todo se puso oscuro y el icono cambió a un sol. Si lo vuelvo a presionar, vuelve a la normalidad. Es muy intuitivo."

### 1.2. Evidencia: Plantilla de Recolección de Datos (Sofía)

| Tarea | ¿Completada con Éxito? | Tiempo (aprox.) | Observaciones del Moderador (Dudas, errores) | Comentarios del Usuario (en voz alta) |
| :--- | :--- | :--- | :--- | :--- |
| **Tarea 1** | Sí | 15 seg | Comprendió la propuesta de valor inmediatamente. El botón de CTA fue el punto focal. | "Es bastante claro, es un sitio para encontrar becas." |
| **Tarea 2** | Sí | 10 seg | Navegó al lugar correcto sin dudar. Notó el estado `active` del menú. | "Funcionó como esperaba." |
| **Tarea 3** | **Parcial** | 45 seg | **Fricción:** El usuario no recibió feedback visual después de presionar "Buscar" en el formulario. | "¿Funcionó? No estoy segura. Esperaba que la lista se actualizara." |
| **Tarea 4** | Sí | 20 seg | Encontró la información rápidamente. El color de estado fue una gran ayuda visual. | "El color verde lo hace muy fácil de identificar." |
| **Tarea 5** | Sí | 10 seg | Reconoció el icono de la luna inmediatamente y entendió su función. | "¡Sí! Todo se puso oscuro... Es muy intuitivo." |

### 1.3. Preguntas Post-Test (Respuestas simuladas de Sofía)
1.  **Facilidad de uso (1-5):** "Le daría un 4. Fue muy fácil, excepto por el formulario de búsqueda que me confundió un poco."
2.  **¿Qué fue lo que más te gustó?:** "Me gustó que es muy limpio y no tiene muchas cosas que distraigan. Los colores son agradables."
3.  **¿Qué fue lo que menos te gustó?:** "Lo del botón 'Buscar' que no hizo nada. Me hizo dudar si había hecho algo mal."
4.  **¿Algo que esperabas encontrar y no encontraste?:** "Quizás en las tarjetas de las becas, me gustaría ver la fecha límite de aplicación sin tener que entrar."
5.  **¿Tienes alguna sugerencia para mejorar el sitio?:** "Cuando buscas en el formulario, la página debería mostrar un mensaje como 'Mostrando 3 becas para ti' o algo así."

---

## Persona 2: Martín (Usuario Intermedio)

*   **Perfil:** 25 años, estudiante de 3er año de Ingeniería. Pragmático, familiarizado con la web y valora la eficiencia.

### 2.1. Narración de la Simulación ("Pensando en voz alta")

*   **Tarea 1 (Primera Impresión):** "Entendido. Página de aterrizaje estándar. Título, párrafo explicativo y un Call to Action (CTA) primario. El diseño es limpio y va al grano. Sé que el objetivo es hacer clic en 'Descubrir Becas'."
*   **Tarea 2 (Navegación Principal):** "*[Hace clic en el CTA]*. Bien, me lleva a `/becas.html`. La URL es limpia. La página muestra una grilla de becas y un formulario de filtros. El layout es de dos columnas en escritorio, es lógico. El menú de navegación resalta la sección activa. Todo en orden."
*   **Tarea 3 (Filtrado de Becas):** "Voy al formulario. Selecciono 'Licenciatura'. Presiono 'Buscar'. *[Observa la pantalla por un momento]*. No hay recarga de página, no hay una petición de red, no hay feedback visual. El botón no está conectado, es un dead-end en la UI. Para que esto funcione, esperaría que la grilla de la izquierda se actualice dinámicamente (usando JavaScript) o que la página recargue con los parámetros del filtro en la URL. Es el principal fallo funcional que veo." **(Punto de fricción identificado)**
*   **Tarea 4 (Consulta de Estado):** "Voy a 'Estado de Becas' en el menú. Veo una tabla con los datos. Podría usar `Ctrl+F` para encontrarlo, pero veo una barra de búsqueda arriba. Voy a probarla. *[Escribe 'Giacomo' en el input]*. Ok, al igual que el otro formulario, este tampoco funciona. Es solo un elemento visual. Encuentro a Giacomo manually en la tabla. El estado 'Aprobado' en verde es claro, eso está bien. Pero la funcionalidad de búsqueda y filtrado, que es clave en una tabla así, no está implementada." **(Punto de fricción identificado)**
*   **Tarea 5 (Funcionalidad Adicional y Responsividad):** "El toggle de dark mode (luna/sol) es estándar, funciona bien. Ahora, por curiosidad, voy a ver cómo se comporta la tabla en móvil. *[Simula achicar la ventana del navegador]*. Ok, la tabla se convierte en tarjetas. Es una solución común para la responsividad, mejora la legibilidad al no tener que hacer scroll horizontal. Sin embargo, se pierde la capacidad de comparar filas rápidamente. Si quisiera ver todos los aprobados, tendría que hacer mucho scroll. Para este tipo de datos, a veces es preferible mantener la estructura de tabla y permitir el scroll horizontal. Es un debate de diseño, pero es una decisión con consecuencias." **(Observación de diseño avanzado)**

### 2.2. Evidencia: Plantilla de Recolección de Datos (Martín)

| Tarea | ¿Completada con Éxito? | Tiempo (aprox.) | Observaciones del Moderador (Dudas, errores) | Comentarios del Usuario (en voz alta) |
| :--- | :--- | :--- | :--- | :--- |
| **Tarea 1** | Sí | 5 seg | Entendió el propósito y la acción principal de inmediato. | "Diseño limpio, va al grano." |
| **Tarea 2** | Sí | 10 seg | Navegación predecible y estándar. | "Todo en orden." |
| **Tarea 3** | **No** | 30 seg | **Fricción Crítica:** Identificó que el formulario de filtro no es funcional y lo describió como un "dead-end". | "No hay recarga, no hay petición... El botón no está conectado." |
| **Tarea 4** | **Parcial** | 35 seg | **Fricción Crítica:** Intentó usar la barra de búsqueda de la tabla y confirmó que tampoco era funcional. | "Este tampoco funciona. Es solo un elemento visual." |
| **Tarea 5** | Sí | 40 seg | Encontró el toggle de tema fácilmente. Realizó un análisis crítico del diseño responsivo de la tabla. | "Se pierde la capacidad de comparar filas rápidamente." |

### 2.3. Preguntas Post-Test (Respuestas simuladas de Martín)
1.  **Facilidad de uso (1-5):** "Le doy un 2. El diseño visual es claro, pero las funciones más importantes (buscar y filtrar) no existen en el prototipo. Así que, en la práctica, no es muy usable para cumplir el objetivo."
2.  **¿Qué más te gustó?:** "La limpieza del diseño y la buena implementación del modo oscuro."
3.  **¿Qué menos te gustó?:** "Que los controles de búsqueda y filtro sean solo elementos visuales sin funcionalidad. Es lo más importante de una plataforma así."
4.  **¿Algo que falte?:** "Paginación en la tabla de becas y en la de estados. Si hay miles de resultados, la página sería lentísima."
5.  **¿Sugerencias?:** "Implementar los filtros con JavaScript para que la actualización sea instantánea. Para la tabla en móvil, consideren dar la opción de scroll horizontal como alternativa a las tarjetas."
