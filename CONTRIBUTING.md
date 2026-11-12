# Cómo contribuir

Convenciones de trabajo de la organización **GrupoMO**. Se aplican a todos los
repositorios de conocimiento salvo que un proyecto defina lo contrario.

## Modelo de ramas

| Rama | Propósito | Sale de |
|---|---|---|
| `main` | Versión publicada y estable | — |
| `docs/<tema>` | Documentación o método común | `main` |
| `skill/<nombre>` | Skill nueva o cambio de una existente | `main` |
| `runbook/<proceso>` | Runbook nuevo o actualización | `main` |
| `fix/<tema>` | Corrección de un error | `main` |
| `chore/<tema>` | Mantenimiento, catálogo o CI | `main` |

Nada se sube directamente a `main`: todo entra por pull request revisada.

## Commits

Formato [Conventional Commits](https://www.conventionalcommits.org/es/v1.0.0/):

```text
<tipo>(<alcance>): <descripción en imperativo>

<cuerpo opcional>

refs OTA-123
```

Tipos habituales: `feat`, `fix`, `docs`, `chore`, `ci`.

- Un commit = un cambio lógico.
- Mensaje en imperativo: describe el qué y el por qué.
- Referencia el ticket de Linear cuando exista.
- Nunca incluyas secretos, credenciales, precios ni datos personales.

## Pull requests

- PRs pequeños y enfocados.
- Rellena la plantilla: resumen, ticket, tipo, validación y checklist de
  seguridad.
- Al menos **una aprobación** de otra persona del equipo; **dos** si el cambio
  toca datos sensibles, seguridad o el repositorio compartido.
- Nadie aprueba su propio cambio.
- CI en verde antes del merge.
- Merge con *squash* e historial lineal.

## Conocimiento y skills

- Cada skill vive en `skills/<nombre>/SKILL.md` con frontmatter: `name`,
  `description`, `version`, dueño y fecha de revisión.
- Cada runbook sigue la plantilla canónica del `master` correspondiente.
- El owner valida el contenido antes de publicarlo.
- Otra persona debe poder ejecutar el runbook sin ayuda del autor.
- Actualiza `catalog.md` y el índice del master en el mismo PR.
- Cita siempre la fuente: skill, referencia, versión y fecha.

## Clasificación

| Nivel | Qué puede contener | Dónde vive |
|---|---|---|
| Público | Material ya publicado | Repo o SharePoint público |
| Interno | Procedimientos y sistemas internos | Repo de la empresa |
| Confidencial | Precios, márgenes, clientes, contratos | Fuera de Hermes |
| Restringido | Credenciales, datos personales, RRHH | Fuera del repo |

Si un procedimiento necesita un dato confidencial, se documenta el paso y se
indica el sistema seguro donde se consulta. El dato no se copia.

## Repositorio compartido

Solo entra material común, revisado y sin datos de empresa:

1. Propuesta con enlace al original.
2. Revisión de un owner de Otazu y otro de Maploca.
3. Eliminación de referencias a una empresa concreta.
4. Registro en `catalog.md`.

## Seguridad

- Sin secretos en el repositorio ni en el historial. Si uno se filtra, se
  considera comprometido: **rótalo**, no basta con borrar el commit.
- gitleaks y el validador se ejecutan en local y en CI.
- No abras una issue pública para vulnerabilidades: sigue
  [SECURITY.md](SECURITY.md).

## Documentación

Cada tema tiene **una sola** página canónica. Si algo cambia, se actualiza la
existente en lugar de duplicarla.
