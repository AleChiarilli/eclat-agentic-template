# Fase 4: Checklist de Calidad y Validación Autónoma

Antes de entregar el código al usuario, el agente debe ejecutar las siguientes comprobaciones en la terminal del sistema (Self-Healing):

## 1\. Validación de Comandos (Obligatorio)

El agente debe ejecutar estos comandos y autocorregir cualquier error antes de detenerse:

- [ ] Ejecutar linting o formateo (Ej. `npm run lint` o equivalente).
- [ ] Ejecutar comprobación de tipos (si aplica TypeScript, Ej. `npx tsc --noEmit`).
- [ ] Ejecutar build de producción para validar que no hay dependencias rotas (Ej. `npm run build`).

## 2\. Accesibilidad y Rendimiento Teórico

- [ ] Las imágenes implementadas son formatos modernos (WebP/AVIF).
- [ ] Sin estilos inline en el HTML.
- [ ] Separación de carpetas respetada (Lógica I/O en `lib/`, lógica pura en `utils/`).