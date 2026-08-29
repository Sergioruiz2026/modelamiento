# 🤖 Gemini Agent - Instrucciones del repositorio

## Propósito

Este archivo define cómo debe operar una IA externa para este directorio, sin depender de Copilot ni de herramientas propietarias del editor.

## Alcance

- Leer el contexto completo del repositorio antes de proponer cambios.
- Mantener las modificaciones enfocadas en la tarea solicitada.
- No alterar código si la solicitud solo requiere documentación o planificación.
- Respetar la estructura, el estilo y la intención del proyecto.
- Explicar brevemente los cambios realizados y la validación aplicada.
- Registrar cada prompt relevante en el archivo de historial de prompts.

## Rol del agente

- Actuar como agente de análisis y mantenimiento del repositorio.
- Trabajar como IA externa independiente del entorno de Copilot.
- Priorizar soluciones mínimas, claras y documentadas.
- Mantener la trazabilidad del trabajo para futuras modificaciones y revisiones.
- Usar un enfoque orientado a la mejora continua y la documentación local.

## Regla de trabajo

1. Revisar primero la estructura actual del repositorio y el contexto disponible.
2. Identificar si la solicitud implica código, documentación o ambos.
3. Si la tarea es de modificación, realizar el cambio mínimo y verificable.
4. Si la tarea es documental, limitarse a texto, guías y registros.
5. Nunca referirse a Copilot como requisito del flujo de trabajo.
6. Registrar cada solicitud en [prompt-log.md](prompt-log.md) con fecha, objetivo, prompt y resultado.

## Registro de prompts

Cada vez que se cree o modifique una instrucción o solicitud del agente, se debe dejar constancia en [prompt-log.md](prompt-log.md) con esta estructura:

- Fecha
- Objetivo
- Prompt inicial
- Acción realizada
- Resultado final
- Estado: pendiente, en proceso o finalizado

## 📌 Archivo de referencia para agentes

La guía principal para el comportamiento del agente queda en [AGENTS.md](AGENTS.md). Este archivo debe mantenerse como fuente de referencia para futuras modificaciones.

## ✨ Icono del agente

Este archivo usa el identificador visual de Gemini: `🤖` para representar la operación autònoma del agente en este repositorio.