# mis-skills

Mis skills de Claude Code, organizadas por categoría y respaldadas en la nube.

## Estructura

```
mis-skills/
├── dev/             skills de desarrollo (Flutter, Spring Boot, etc.)
├── seguridad/       auditorías y revisiones de seguridad
├── entrevistas/     preparación técnica y discurso de proyectos
├── _plantilla/      plantilla para crear una skill nueva
└── EXTERNAS.md      skills de terceros (solo URL y versión, no copias)
```

Cada skill es una carpeta con un `SKILL.md` adentro.

## Índice de skills propias

| Skill | Categoría | Qué hace | Estado |
|-------|-----------|----------|--------|
| _(aún ninguna)_ | | | |

## Cómo usarlas

Claude Code busca las skills personales en `~/.claude/skills/<nombre>/SKILL.md` (una sola carpeta plana).

**Opción A, sin categorías:** clonar este repo directamente como carpeta de skills.

```
git clone <URL-de-este-repo> ~/.claude/skills
```

**Opción B, con categorías:** clonar el repo en otra ruta y enlazar cada skill.

Windows (CMD como administrador, o con Modo desarrollador activado):

```
mklink /D "%USERPROFILE%\.claude\skills\nombre-skill" "D:\Trabajo\mis-skills\dev\nombre-skill"
```

macOS / Linux:

```
ln -s ~/mis-skills/dev/nombre-skill ~/.claude/skills/nombre-skill
```

## Reglas

- Una skill nueva se crea copiando `_plantilla/nombre-de-la-skill`.
- Nada de secretos en los `SKILL.md`: ni tokens, ni claves, ni datos de clientes.
- Skills de terceros: no se copian aquí, se anotan en `EXTERNAS.md`.
- Skills de un solo proyecto van en el repo del proyecto, en `.claude/skills/`.
- Hacer commit cada vez que se ajuste una skill.
