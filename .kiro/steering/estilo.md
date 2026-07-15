---
inclusion: always
---

# Reglas de estilo y contexto — San Fernando ITT

## Contexto del proyecto
- Este proyecto pertenece al Instituto Tecnológico de Tlajomulco, enfocado en el análisis de datos del Corredor San Fernando.
- El objetivo principal es estandarizar, limpiar y visualizar datos geoespaciales y tabulares.

## Estilo de código
- Usar Python 3.10+ como lenguaje principal.
- Preferir pandas y geopandas para manipulación de datos.
- Nombres de variables y funciones en snake_case y en español cuando sea descriptivo.
- Comentarios en español.
- Documentar cada celda relevante en los notebooks con markdown explicativo.

## Convenciones de datos
- Seguir el esquema definido en `Data/esquema_datos_comunes.txt`.
- Los archivos de salida (mapas HTML, CSV limpios) van en `Outputs/`.
- No subir datos crudos al repositorio (ver .gitignore).

## Comunicacion
- No usar emojis en codigo, comentarios, documentacion ni respuestas.

## Entorno
- Usar **uv** como gestor de paquetes y entornos virtuales.
- No usar pip, conda ni virtualenv directamente.
