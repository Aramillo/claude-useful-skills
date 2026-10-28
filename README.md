# mis-skills

Biblioteca de **referencias** a skills de Claude Code.

- **Skills de terceros:** no se guardan copias. En `EXTERNAS.md` se registra solo la URL del repo, para qué la uso y el comando de instalación. Se instalan desde su origen, después de revisar su `SKILL.md`.
- **Skills propias:** son las únicas que viven aquí, dentro de las carpetas de categorías.

`CLAUDE.md` le explica a Claude Code cómo actuar cuando pido una skill: buscar la referencia en `EXTERNAS.md`, mostrarme el `SKILL.md` de origen y solo instalar tras mi confirmación.

## Estructura

```
mis-skills/
├── EXTERNAS.md      referencias a skills de terceros (URL, uso, instalación; nunca copias)
├── CLAUDE.md        instrucciones para Claude Code sobre cómo usar este repo
├── dev/             skills propias de desarrollo (Flutter, Spring Boot, etc.)
├── seguridad/       skills propias de auditorías y revisiones de seguridad
├── entrevistas/     skills propias de preparación técnica y discurso de proyectos
└── _plantilla/      plantilla para crear una skill propia nueva
```

Las carpetas de categorías son solo para skills propias. Cada skill propia es una carpeta con un `SKILL.md` adentro.

## Índice de skills propias

| Skill | Categoría | Qué hace | Estado |
|-------|-----------|----------|--------|
| _(aún ninguna)_ | | | |

## Instalar una skill de terceros

Copiar el comando de la columna "Instalación" de `EXTERNAS.md`, después de revisar el `SKILL.md` en su repo de origen. O pedírselo a Claude Code en este repo ("instala la skill de seguridad").

## Cómo usar las skills propias

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
- Skills de terceros: no se copian aquí, se anotan en `EXTERNAS.md` (URL, uso, comando y fecha de registro).
- Skills de un solo proyecto van en el repo del proyecto, en `.claude/skills/`.
- Hacer commit cada vez que se ajuste una skill.
