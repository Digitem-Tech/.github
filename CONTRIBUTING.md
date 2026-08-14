# Convenciones de colaboración — Digitem-Tech

Estas reglas sirven como base común para los repositorios de Digitem. Si un repositorio tiene instrucciones más específicas, prevalecen las de ese proyecto.

## Repositorios y alcance

Cada repositorio debe tener una responsabilidad clara. No se duplican datos de clientes dentro de documentación corporativa y no se mezcla código reutilizable con información específica de un cliente.

- `digitem-*`: activos, herramientas y documentación propios de Digitem.
- `demo-*`: demostraciones comerciales ficticias y autocontenidas.
- repositorios de cliente: contexto, datos, código y documentación de ese cliente únicamente.

## Ramas y cambios

Usar nombres breves y autoexplicativos:

- `feature/...` para funcionalidad nueva;
- `fix/...` para correcciones;
- `docs/...` para documentación;
- `chore/...` para mantenimiento.

Las ramas temporales deben cerrarse o dejar de considerarse fuente de verdad una vez integrado el trabajo. La rama por defecto del repositorio es la referencia canónica.

## Pull requests

Toda PR debe explicar:

1. qué cambia;
2. por qué cambia;
3. cómo se ha validado;
4. riesgos o trabajo pendiente, si existe.

No mantener PRs abiertas cuando el cambio ya fue integrado por otra vía: cerrarlas indicando que quedaron superadas.

## Datos y seguridad

Nunca versionar:

- `.env`, API keys, tokens, contraseñas o credenciales;
- dumps de bases de datos sin sanitizar;
- pedidos, clientes o cualquier PII sin anonimizar;
- backups de producción;
- URLs privadas que incorporen secretos;
- configuración local de herramientas (`settings.local.*`, caches, outputs temporales).

Los datos brutos de cliente solo se almacenan cuando sean necesarios, en el repositorio privado correspondiente y después de revisar que no contienen información personal o secretos innecesarios.

## READMEs

Todo repositorio activo debe tener un README que responda, como mínimo, a:

- qué es el repositorio;
- qué pertenece aquí y qué no;
- estado o propósito actual;
- estructura principal;
- cómo ejecutar o utilizar el proyecto cuando aplique;
- dónde está la fuente de verdad de la documentación relacionada.
