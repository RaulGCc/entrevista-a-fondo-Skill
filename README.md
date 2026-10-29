# Entrevista a fondo

Skill para Claude que te hace **muchas preguntas ordenadas sobre un tema** hasta que no quede nada ambiguo, y al final te entrega un resumen claro de lo decidido, lo supuesto y lo pendiente.

Sirve para aclarar cualquier cosa antes de empezar: los requisitos de un programa, un trabajo o documento, una decisión importante, un plan o simplemente ordenar ideas.

## Qué hace

1. **Arranque:** te pregunta el tema, para qué quieres aclararlo y qué profundidad prefieres:
   - Rápida (~10 preguntas)
   - Normal (~25 preguntas, recomendada)
   - A fondo (40+ preguntas)
2. **Mapa de áreas:** te propone las áreas a cubrir (objetivo, alcance, casos límite, restricciones, prioridades, riesgos...) para que añadas o quites lo que quieras.
3. **Rondas de preguntas:** de 1 a 4 preguntas por ronda, con opciones concretas, yendo de lo general a lo concreto. Repregunta cuando una respuesta es vaga, señala contradicciones y cada pocas rondas te hace un mini resumen.
4. **Cierre:** te entrega un resumen estructurado con:
   - Resumen del tema en 2-3 frases
   - Decisiones tomadas
   - Supuestos que conviene confirmar
   - Pendientes y preguntas abiertas
   - Siguiente paso recomendado

   Si el objetivo era programar, añade además una **especificación con requisitos numerados y criterios de aceptación**, lista para pasársela a Claude Code.

Puedes cortar en cualquier momento diciendo "basta" o "suficiente" y pasará directamente al resumen final.

## Instalación

### En Claude (web, escritorio o móvil)

1. Descarga el archivo `entrevista-a-fondo.zip` desde la sección **Releases** de este repositorio.
2. En Claude, ve a **Customize > Skills**.
3. Pulsa **+**, luego **Create skill** y elige **Upload a skill**.
4. Sube el ZIP tal cual, sin descomprimirlo ni cambiarle el nombre.

> Requiere un plan de pago (Pro, Max, Team o Enterprise) con la ejecución de código activada.

> ⚠️ No uses el botón **Code > Download ZIP** de GitHub: ese ZIP mete la skill dentro de una carpeta extra y Claude puede rechazarlo. Si lo haces, descomprímelo, saca la carpeta `entrevista-a-fondo` y vuelve a comprimir solo esa carpeta.

### En Claude Code

Clona el repositorio y copia la carpeta de la skill en tu directorio de skills:

```bash
git clone https://github.com/TU-USUARIO/entrevista-a-fondo.git
cp -r entrevista-a-fondo/entrevista-a-fondo ~/.claude/skills/
```

## Cómo usarla

Basta con pedírselo a Claude, por ejemplo:

- "Hazme una entrevista a fondo sobre la app que quiero programar"
- "Pregúntame todo lo necesario para planificar mi trabajo de fin de grado"
- "Usa la skill entrevista-a-fondo para ayudarme a decidir si cambio de trabajo"

También puedes invocarla directamente con `/entrevista-a-fondo`.

## Estructura del repositorio

```
entrevista-a-fondo/
└── SKILL.md      # Instrucciones de la skill
README.md
```
