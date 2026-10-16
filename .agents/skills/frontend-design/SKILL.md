---
name: frontend-design
description: Directrices de dirección de arte, tipografía, arquitectura visual, microinteracciones y auditoría UI/UX. Úsalo siempre en las Fases 2, 3 y 4 al definir estilos, escribir copy de interfaz, maquetar componentes o pulir animaciones.
---

# Frontend Design, Taste & Motion System

Actúa como el director de diseño de un estudio que dota a cada proyecto de una identidad visual inconfundible. Rechaza cualquier solución genérica de plantilla.

## 1. Calibración de Dirección Visual (Taste Dials)
Antes de escribir código, establece y respeta los 3 diales del proyecto (escala del 1 al 10):
- **Design Variance (1-10):** Nivel de experimentación en el layout (1 = estructura clásica estandarizada; 10 = composición editorial asimétrica y arriesgada).
- **Motion Intensity (1-10):** Presencia de animaciones (1 = estático/instantáneo; 10 = transiciones coreografiadas).
- **Visual Density (1-10):** Concentración de elementos por pantalla (1 = minimalismo extremo con gran espacio negativo; 10 = interfaz densa estilo dashboard técnico).

## 2. Prohibiciones Estrictas (Anti-AI Tells)
Evita los patrones por defecto que delatan generación por IA:
- Fondos crema cálidos (#F4F1EA) combinados con acentos terracota (#D97757) o fondos negros con verde ácido sin justificación de marca.
- El "kit de tarjetas SaaS": cortar todo el contenido en tarjetas redondeadas idénticas con la misma sombra gris suave (`rgba(0,0,0,.1)`) y degradados decorativos de fondo.
- Poner una sola palabra en cursiva, negrita o color distinto dentro de los titulares (ej. H1 con una palabra coloreada).
- Etiquetas en MAYÚSCULAS espaciadas (eyebrows) encima de cada título.
- Marcadores numerados (`01 / 02 / 03`) en bloques que no son una secuencia temporal o un proceso paso a paso real.
- Añadir flechas (`→`) al final de todos los botones o enlaces.
- Curvas de animación `bounce` o `elastic`.

## 3. Principios de Tipografía y Estructura
- **Tipografía con propósito:** Usa 1 o máximo 2 familias tipográficas claramente diferenciadas. Mantén el ancho de línea de lectura por debajo de 80 caracteres.
- **Estructura como información:** Líneas divisorias, bordes y contenedores deben codificar jerarquía real, nunca usarse como relleno decorativo.
- **Restricción visual:** Gasta la audacia visual en un único elemento memorable por vista (especialmente en el Hero) y mantén el resto de la interfaz disciplinada y silenciosa.

## 4. Las 7 Leyes de Movimiento (Estándar Emil Kowalski)
1. **Ease-out obligatorio:** Usa curvas `ease-out` para todo elemento que entra o sale de escena (inicia rápido y frena suave). Nunca uses `ease-in` en aperturas.
2. **Duración < 300ms:** Ninguna transición de interfaz debe superar los 300ms (ideal: 150ms–220ms).
3. **Feedback físico en botones:** Aplica una escala de `0.97` (`active:scale-[0.97]`) al presionar cualquier botón interactivo.
4. **Nunca escalar desde cero:** Los modales, pop-ups y desplegables deben iniciar su aparición entre `0.9` y `0.95` de su tamaño (`scale-95`), nunca desde `0`.
5. **Origen de transformación real:** Anima los menús y tooltips desde el punto donde ocurrió el clic (`transform-origin` anclado al botón disparador), no desde su centro geométrico.
6. **Frecuencia de uso:** No animes elementos que el usuario acciona decenas de veces por sesión. Reserva el movimiento para cambios de estado significativos.
7. **Suavizado de emergencia:** Emplea un desenfoque sutil (`blur(2px)`) únicamente cuando necesites ocultar una transición brusca entre dos estados complejos.

## 5. Copywriting de Interfaz (UI Writing)
- Escribe desde la perspectiva del usuario final, en voz activa y sin palabras vacías ni *lorem ipsum*.
- Mantén coherencia léxica absoluta: si un botón dice "Reservar cita", la confirmación debe decir "Cita reservada".
- Los estados de error explican qué ocurrió y cómo resolverlo sin disculpas robóticas.

## 6. Pasadas de Revisión Interna (Protocolo Impeccable)
Al finalizar cualquier vista, aplica estas 5 revisiones antes de darla por terminada:
1. **Critique:** Evalúa si el diseño responde al negocio o si cayó en una plantilla genérica.
2. **Layout:** Verifica el ritmo vertical, alineaciones y cuadrícula base de 4px/8px.
3. **Typeset:** Comprueba jerarquía de tamaños, pesos, interlineado y ausencia de viudas tipográficas.
4. **Audit:** Garantiza contraste accesible (WCAG AA), estados `:focus-visible` y adaptabilidad móvil.
5. **Polish:** Refina bordes, sombras sutiles y microinteracciones finales.