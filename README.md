# 🧭 Proyecto local de agente Gemini

Este repositorio está preparado para funcionar como un agente local de IA externa, independiente de Copilot y de cualquier herramienta propietaria del editor.

## Objetivo

Actuar como una ayuda autónoma para:

- revisar el contexto del repositorio,
- identificar tareas puntuales,
- realizar cambios mínimos y trazables,
- documentar cada solicitud y su resultado.

## Archivos clave

- [AGENTS.md](AGENTS.md): guía principal del agente.
- [gemini.md](gemini.md): instrucciones específicas para este repositorio.
- [changelog.md](changelog.md): historial principal de prompts y resultados.
- [prompt-log.md](prompt-log.md): archivo eliminado; se consolidó la trazabilidad en changelog.md.

## Principios del agente

- Leer antes de modificar.
- Mantener cambios pequeños y específicos.
- No inventar estructura ajena al proyecto.
- Priorizar documentación clara y verificable.
- Registrar cada solicitud de trabajo.
- Trabajar sin depender de Copilot.

## Flujo recomendado

1. Revisar el contexto actual del repositorio.
2. Determinar si la tarea requiere documentación, análisis o cambios.
3. Ejecutar solo la acción necesaria para resolver el objetivo.
4. Registrar el prompt y el resultado en [changelog.md](changelog.md).
5. Dejar evidencia clara del trabajo realizado.

## Registro de prompts

Toda solicitud nueva debe dejarse documentada en [changelog.md](changelog.md), con:

- fecha,
- objetivo,
- prompt original,
- acción realizada,
- resultado,
- estado.

## Estado

El repositorio queda preparado para actuar como agente de modificaciones con trazabilidad local y flujo de trabajo reproducible.
