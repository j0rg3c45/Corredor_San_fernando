# Data — Documentación

## Contenido de esta carpeta

Esta carpeta contiene los esquemas y documentación relacionada con los datos del proyecto San Fernando ITT.

### Archivos

- **esquema_datos_comunes.txt**: Define el esquema estandarizado que deben seguir todos los datasets del proyecto.

## Lineamientos

- Los datos crudos (CSV, Excel, shapefiles) **no** se suben al repositorio.
- Solo se versionan esquemas, diccionarios de datos y documentación.
- Los datos procesados y listos para visualización se exportan a `Outputs/`.

## Cómo agregar un nuevo dataset

1. Verificar que cumple con el esquema en `esquema_datos_comunes.txt`.
2. Documentar la fuente y fecha de obtención.
3. Procesar en un notebook dentro de `Notebooks/`.
4. Exportar resultados a `Outputs/`.
