# Fase 4: Checklist de Calidad y Validación Autónoma

Antes de entregar el código al usuario, el agente debe verificar y superar todos los puntos de este checklist mediante autocorrección (*Self-Healing*):

## 1. Validación de Comandos y Estándares (Terminal)
- [ ] Ejecutar linting o formateo (`npm run lint` o equivalente sin errores).
- [ ] Ejecutar comprobación de tipos (`npx tsc --noEmit` si aplica).
- [ ] Ejecutar build de producción exitoso (`npm run build`).
- [ ] Imágenes implementadas en formatos modernos (WebP/AVIF), sin estilos inline y con separación de carpetas respetada.

## 2. Auditoría de Diseño y Movimiento (Protocolo Impeccable & Emil Rules)
- [ ] **Critique & Layout:** Sin clichés de IA (sin palabras sueltas coloreadas en H1, sin eyebrows en mayúsculas innecesarias, sin tarjetas clónicas).
- [ ] **Motion Pass:** Todas las animaciones usan `ease-out`, duran `< 300ms`, los botones tienen feedback `scale(0.97)` y ningún modal escala desde `0`.

## 3. Bucle de Pruebas en Navegador Real (Playwright MCP)
Ejecutar servidor local y verificar con Playwright en **1440px (Desktop)** y **375px (Mobile)**:
- [ ] **Capturas e inspección visual:** Sin textos superpuestos, cortados ni elementos desalineados en ambas resoluciones.
- [ ] **Cero Scroll Horizontal:** Verificado en vista móvil de 375px (`document.documentElement.scrollWidth <= window.innerWidth`).
- [ ] **Interactividad total:** Todos los botones, enlaces, acordeones de FAQ y menús móviles clicados y funcionando. Tamaño táctil adecuado en móvil.
- [ ] **Flujo de Formulario:** Formulario probado con datos de test hasta alcanzar el estado o página de confirmación.
- [ ] **Consola Limpia:** Cero errores de JavaScript o recursos rotos en la consola del navegador.

## 4. Prueba de Estrés Destructiva (Break-UI Protocol)
- [ ] **Contenido extremo:** La interfaz no se rompe al inyectar titulares o nombres un 200% más largos, cifras grandes o listas con un único elemento.

## 5. SEO Técnico e Imágenes
- [ ] `title` y `meta description` únicos y específicos para la página, más imagen OpenGraph configurada.
- [ ] Archivos `sitemap.xml`, `robots.txt` y marcado `Schema.org` (ej. `LocalBusiness` o `Product`) inyectados.
- [ ] Imágenes optimizadas en formato WebP (< 200KB) con atributos `alt` descriptivos.