# .github

Repositorio de **ficheros de comunidad por defecto** de la organización
[GrupoMO](https://github.com/Grupo-MO).

GitHub usa estos ficheros en cualquier repositorio de la organización que no
tenga el suyo propio, **incluidos los privados**. Cambiar una plantilla aquí la
cambia en todos los proyectos de golpe.

## Contenido

| Ruta | Para qué sirve |
|---|---|
| `profile/README.md` | Portada pública de la organización |
| `SECURITY.md` | Canal y procedimiento para reportar vulnerabilidades |
| `CONTRIBUTING.md` | Modelo de ramas, commits, PR y publicación de conocimiento |
| `.github/PULL_REQUEST_TEMPLATE.md` | Checklist por defecto de los PR |
| `.github/ISSUE_TEMPLATE/` | Plantillas de issue (error, skill, seguridad) |
| `CODEOWNERS` | Revisión de los cambios de este repositorio |

## Repositorios de la organización

| Repositorio | Contenido | Acceso |
|---|---|---|
| `otazu-knowledge` | Skills y runbooks de Otazu | Equipo de Otazu |
| `maploca-knowledge` | Skills y runbooks de Maploca | Equipo de Maploca |
| `shared-knowledge` | Métodos y plantillas comunes | Ambos equipos |
| `.github` | Este repositorio | Público |

## Reglas

- Este repositorio debe seguir siendo **público**: GitHub solo hereda los
  ficheros de comunidad desde un `.github` público.
- Si un proyecto necesita una plantilla distinta, la define en su propio
  repositorio y esta se ignora para ese proyecto.
- Los cambios se hacen por pull request, como en el resto de repositorios.
- `CODEOWNERS` **no** se hereda: cada repositorio debe tener el suyo.
- Este repositorio no contiene secretos, datos de clientes, precios ni
  información personal.
