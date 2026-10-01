# ⚡ The Éclat Agentic Boilerplate

Un framework de gobernanza documental minimalista para desarrollo de software e integraciones asistido por IA (optimizado para IDEs agenticos como Antigravity, Cline, RooCode, Cursor o Windsurf).

## 🧠 La Filosofía: Anti-Overkill

La industria está obsesionada con enjambres multiagente complejos (CrewAI, LangGraph) que consumen miles de tokens debatiendo entre sí para tareas sencillas. Para agencias, desarrolladores individuales y creadores de automatizaciones, esto destruye la rentabilidad.

**The Éclat Boilerplate** resuelve esto mediante un enfoque de **Agente Único con Cambio de Roles (Sequential Role-Playing)**. En lugar de orquestar código en Python, gobernamos al modelo de lenguaje (ej. Claude 3.5 Sonnet) a través de un sistema estricto de archivos Markdown que actúan como memoria, guardarraíles y barreras de ejecución.

### ¿Qué problema resuelve?
- ❌ **Zero-Shot Code:** Evita que la IA escupa código genérico de golpe inventando colores, copies o arquitecturas.
- ❌ **Pérdida de Contexto:** Elimina la necesidad de reexplicar en qué punto te quedaste.
- ❌ **Alucinaciones de API:** Prohíbe al agente programar integraciones sin haber definido un contrato de datos primero.

---

## 🏗️ Estructura del Framework

El sistema se basa en un contrato maestro (`AGENTS.md`) y una memoria fragmentada en 5 archivos:

```text
eclat-agentic-template/
├── AGENTS.md                  # El motor de reglas innegociables para la IA
└── docs/
    ├── 00_CONTEXTO.md         # Estrategia, objetivo y tono (Fase 1)
    ├── 01_INSUMOS.md          # Branding, wireframes y contratos (Fase 2)
    ├── 02_ARQUITECTURA.md     # Stack técnico y decisiones (Fase 3)
    ├── 03_QA_CHECKLIST.md     # Criterios de validación y self-healing (Fase 4)
    └── 99_ESTADO_ACTUAL.md    # Memoria continua (Context Compaction)
```

---

## 🚦 El Pipeline de 4 Fases ("Think First, Code Second")

El agente tiene estrictamente prohibido escribir código sin antes superar 4 barreras de validación (Gates) donde el usuario debe dar su aprobación explícita:

1. **Fase 1 (Estratega):** Define objetivo, métricas y tono de voz.
2. **Fase 2 (UX/Copywriter):** Estructura el esqueleto visual y redacta el copy definitivo. Exige los colores y tipografías.
3. **Fase 3 (Arquitecto):** Define el stack tecnológico, los Design Tokens y los contratos de datos.
4. **Fase 4 (Desarrollador):** Escribe el código, ejecuta validaciones en terminal (*Self-Healing*) y realiza QA.

---

## 🚀 Cómo usarlo

1. **Haz un Fork / Clon** de este repositorio o utiliza la plantilla para tu nuevo proyecto.
2. Abre la carpeta en tu editor agentico preferido.
3. Rellena 1 o 2 líneas en `docs/00_CONTEXTO.md` con la idea general del cliente.
4. Abre el chat de tu IA y lanza este único prompt inicial:

> *"Iniciamos proyecto. Lee estrictamente el `AGENTS.md`, revisa en qué punto estamos en `docs/99_ESTADO_ACTUAL.md` y arranca la Fase 1."*

A partir de ahí, el agente tomará el control, te pedirá los insumos faltantes y documentará sus propias decisiones sin que tengas que microgestionarlo.

---

## 🤝 Contribuciones y Forks
Este boilerplate nace de la experiencia iterando proyectos reales de alta conversión y despliegues ligeros. Si quieres hacer un fork, adaptarlo a tu propio stack (Next.js, Astro, Python) o proponer mejoras a los guardarraíles del `AGENTS.md`, siéntete libre. 

*Work smart, prompt strictly.*
