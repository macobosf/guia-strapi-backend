# Backend — Guía Strapi v5 + Angular 21

API REST construida con Strapi v5 que expone una colección de tareas. Forma parte de un proyecto demo que muestra cómo integrar Strapi v5 con un frontend Angular 21.

---

> **Documentación completa**
>
> La guía de instalación local, configuración, deploy en Strapi Cloud y solución de problemas está en el repositorio del frontend:
> [https://github.com/macobosf/guia-strapi-frontend](https://github.com/macobosf/guia-strapi-frontend)

---

## Inicio rápido

```bash
pnpm install
pnpm approve-builds
pnpm develop
```

Una vez que el servidor esté en marcha:

1. Abrir [http://localhost:1337/admin](http://localhost:1337/admin) y crear el usuario administrador.
2. Crear el Content-Type **Tarea** con los siguientes campos:

   | Campo        | Tipo          | Opciones                  |
   |--------------|---------------|---------------------------|
   | `titulo`     | Short text    |                           |
   | `descripcion`| Long text     |                           |
   | `completada` | Boolean       |                           |
   | `prioridad`  | Enumeration   | `baja`, `media`, `alta`   |

3. En **Settings → Roles → Public**, habilitar los permisos `find`, `findOne`, `create`, `update` y `delete` para la colección Tarea.

## Endpoint principal

```
GET     /api/tareas
POST    /api/tareas
GET     /api/tareas/:id
PUT     /api/tareas/:id
DELETE  /api/tareas/:id
```

## Stack

- Strapi v5.48.0 (JavaScript)
- Node 24
- pnpm
- SQLite (desarrollo local) / PostgreSQL (Strapi Cloud)

## Repositorio relacionado

Frontend Angular 21: [https://github.com/macobosf/guia-strapi-frontend](https://github.com/macobosf/guia-strapi-frontend)

## Licencia

[MIT](LICENSE)
