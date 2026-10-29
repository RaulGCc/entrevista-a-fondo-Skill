---
name: "entrevista-a-fondo"
description: "Úsala cuando el usuario quiera que le hagas muchas preguntas sobre un tema para dejarlo todo claro antes de empezar (requisitos, ideas, decisiones, planes)."
---

# Entrevista a fondo

Objetivo: sacar de la cabeza del usuario todo lo necesario sobre un tema, mediante preguntas ordenadas, hasta que no quede nada ambiguo. Al final se entrega un resumen claro de decisiones, supuestos y puntos pendientes.

Idioma: el del usuario (por defecto, español).

## 1. Arranque

1. Identifica el **tema**. Si el usuario no lo ha dicho, pregúntalo antes de nada.
2. Pregunta (en una sola ronda con AskUserQuestion):
   - **Para qué** quiere aclararlo: tomar una decisión, escribir una especificación para programar, planificar un trabajo/documento, ordenar ideas...
   - **Profundidad**: Rápida (~10 preguntas), Normal (~25, recomendada), A fondo (40+).
3. Revisa el contexto disponible (conversación, archivos adjuntos, memoria del proyecto) y NO preguntes lo que ya sabes. Si das algo por supuesto, dilo.

## 2. Mapa de áreas

Antes de preguntar, construye una lista de áreas a cubrir adaptada al tipo de tema y enséñasela al usuario en 3-6 líneas para que añada o quite. Áreas típicas:

- Objetivo y problema que resuelve
- Usuarios / personas implicadas y qué necesita cada uno
- Alcance: qué entra y, muy importante, qué NO entra
- Funcionamiento detallado / flujos / casos de uso
- Casos límite y errores (¿qué pasa si...?)
- Restricciones: tiempo, dinero, tecnología, normativa, datos personales
- Prioridades: imprescindible vs. deseable vs. futuro
- Criterios de éxito: cómo sabremos que está bien hecho
- Riesgos y dependencias
- Alternativas consideradas y por qué se descartan

Para temas de software añade: datos y entidades, roles y permisos, pantallas, integraciones, tecnología, despliegue, pruebas.

## 3. Rondas de preguntas

- Usa **AskUserQuestion** con 1-4 preguntas por ronda, opciones concretas y mutuamente excluyentes. Si tienes una recomendación, ponla primero con "(Recomendado)". El usuario siempre puede escribir su propia respuesta.
- Si AskUserQuestion no está disponible, pregunta en texto numerado, máximo 4 por mensaje.
- Ve de lo general a lo concreto: primero objetivo y alcance, luego detalles, luego casos límite.
- Una idea por pregunta. Sin preguntas tendenciosas.
- Cuando una respuesta sea vaga ("depende", "no sé", "lo normal"): repregunta con opciones concretas o propone un valor por defecto y pide confirmación.
- Si detectas una **contradicción** con algo dicho antes, señálala y pide que se resuelva.
- Lleva internamente tres listas: **Decidido**, **Supuesto** (lo que asumes y el usuario no ha confirmado) y **Pendiente**.
- Cada 3 rondas, haz un mini resumen (3-5 líneas) de lo decidido y lo que falta, para que el usuario corrija a tiempo.
- Si el usuario dice "basta", "suficiente" o similar, pasa directamente al cierre.

## 4. Cuándo parar

Para cuando todas las áreas del mapa estén cubiertas para la profundidad elegida, o cuando el usuario lo pida. Antes de cerrar, haz una última ronda de "¿se nos escapa algo?" con 1-2 preguntas sobre las áreas más flojas.

## 5. Cierre

Entrega un resumen estructurado:

1. **Resumen en 2-3 frases** del tema tal como ha quedado.
2. **Decisiones** tomadas, agrupadas por área.
3. **Supuestos** que conviene confirmar.
4. **Pendientes** / preguntas abiertas, con quién o cómo resolverlas.
5. **Siguiente paso** recomendado.

Si el objetivo era programar, añade una sección "Especificación para el desarrollo" con requisitos numerados y criterios de aceptación, lista para pasársela a Claude Code.

Ofrece guardar el resumen como documento para conservarlo y compartirlo.