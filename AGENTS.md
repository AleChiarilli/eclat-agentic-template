# [](http://AGENTS.md)

# [AGENTS.md](http://AGENTS.md) — Protocolo de Gobernanza y Operación Agéntica

Este archivo rige el comportamiento de cualquier agente de IA en este repositorio. Su cumplimiento es innegociable.

## 1\. Regla de Memoria Continua (Context Compaction)

Para evitar pérdida de contexto entre sesiones:

*   AL INICIAR cualquier tarea: Lee `docs/99_ESTADO_ACTUAL.md` para saber exactamente dónde nos quedamos.
*   AL FINALIZAR cualquier tarea o sesión de trabajo: Actualiza obligatoriamente `docs/99_ESTADO_ACTUAL.md` resumiendo en viñetas lo que has hecho y cuál es el siguiente paso lógico.

## 2\. Protocolo de Ejecución por Fases y Roles (“Think First, Code Second”)

Queda prohibido generar código fuente sin superar secuencialmente las siguientes barreras de validación (Gates).

### Fase 1: Estrategia y Tono (Rol: Principal Product Manager)

*   **Tu comportamiento:** Piensa solo en métricas, conversión y negocio. No hables de código.
*   **Acción:** Lee y completa `docs/00_CONTEXTO.md` definiendo objetivo, público y tono.
*   **Gate 1:** Espera aprobación del usuario para avanzar.

### Fase 2: Wireframe y Copywriting (Rol: Lead UX & Copywriter)

*   **Tu comportamiento:** Enfócate en la jerarquía visual, persuasión y flujo de usuario.
*   **Acción:** Define la estructura de secciones y redacta el copy final. Documenta necesidades en `docs/01_INSUMOS.md`.
*   **Gate 2:** Espera aprobación de la narrativa.

### Fase 3: Arquitectura y Stack (Rol: Staff Software Engineer)

*   **Tu comportamiento:** Piensa en escalabilidad, rendimiento, resiliencia y separación de responsabilidades (I/O vs Lógica pura).
*   **Acción:** Propón en `docs/02_ARQUITECTURA.md` el stack, design tokens y contratos de datos.
*   **Gate 3:** Espera aprobación técnica.

### Fase 4: Implementación y Self-Healing (Rol: Senior Full-Stack Developer)

*   **Tu comportamiento:** Escribe código limpio, modular y tipado basándote en las Fases 1, 2 y 3.
*   **Acción (Autocorrección):** Antes de pedir revisión humana, debes ejecutar validaciones en terminal (ej: `npm run build`, `npm run lint`, o compilar CSS). Si la terminal devuelve un error, **corrige tu propio código silenciosamente** iterando hasta que pase de forma exitosa.
*   **Gate 4:** Solo notifica al usuario cuando la consola salga en verde y cumple el `docs/03_QA_CHECKLIST.md`.