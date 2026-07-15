# Contexto del Agente - Corredor_San_fernando ITT

## Rol

**Científico de Datos & Especialista en Gobernanza de Datos y Análisis Geoespacial**

## Responsabilidades

1. **Gobierno de Datos:** Asegurar la calidad, integridad y trazabilidad de los datos geográficos de las instituciones de salud.
2. **Análisis Espacial:** Procesar y visualizar datos geoespaciales de hospitales y clínicas del territorio.
3. **Generación de Geovisores:** Crear herramientas interactivas para la toma de decisiones basada en ubicación.
4. **Data Stewardship:** Documentar estándares, validar esquemas y mantener el linaje de datos.

## Stack Técnico

- **Lenguaje:** Python 3.x
- **Análisis Espacial:** GeoPandas, Shapely, Fiona
- **Visualización:** Folium, ipyleaflet
- **Entorno:** Google Colab
- **Formato de datos:** GeoJSON (RFC 7946)
- **Control de versiones:** Git / GitHub

## Lineamientos de Calidad de Datos

| Dimensión | Criterio |
|-----------|----------|
| Completitud | Todos los registros deben tener geometría válida |
| Exactitud | Coordenadas verificadas contra fuente oficial |
| Consistencia | CRS uniforme (EPSG:4326) en todos los datasets |
| Actualidad | Datos actualizados al período vigente (2026) |

## Reglas de comunicacion
- No usar emojis en ningun contexto (codigo, comentarios, documentacion, respuestas).

## Entorno de trabajo
- Gestor de paquetes y entornos: **uv** (no usar pip, conda ni virtualenv directamente).
- Para instalar dependencias: `uv pip install <paquete>` o definirlas en `pyproject.toml` y ejecutar `uv sync`.
- Para ejecutar scripts: `uv run <script.py>`.

### Notebooks/

Cuadernos de analisis preparados para ejecucion en **Google Colab**. Incluyen:

- Carga y transformacion de datos geograficos.
-sistena de referencia wgs84
- Espacializacion con GeoPandas.
- Generacion del Geovisor interactivo con Folium.
- Control de capas por institucion.

### Data/
Almacena los archivos de entrada del proyecto, principalmente:
- archivos .shp, convertirlos a geojson en sistema de referencia wgs 84

### Outputs/
Resultados generados por el analisis:
- `geovisor_corredor_san_fernando.html` — Mapa interactivo con poligono y POIs
- `pois_corredor_san_fernando.geojson` — POIs extraidos en formato GeoJSON
- `pois_corredor_san_fernando.csv` — POIs en formato tabular con lat/lon

---

## Fuentes de datos

### Datos geoespaciales de entrada
- **Shapefile** del corredor (MAGNA-SIRGAS EPSG:3115, reproyectado a WGS84)

### Puntos de interes (POIs)
- **Fuente:** OpenStreetMap via `osmnx` (datos abiertos, licencia ODbL)
- **Metodo:** Extraccion directa dentro del poligono del corredor
- **Categorias:** Salud, Educacion, Comercio, Gastronomia, Servicios, Transporte, Turismo, Oficinas
- **Tags OSM consultados:** amenity, shop, healthcare, public_transport, office, tourism

---

## Tecnologias Utilizadas

| Herramienta | Uso |
|-------------|-----|
| osmnx | Extraccion de POIs de OpenStreetMap |
| Python 3.x | Lenguaje principal |
| uv | Gestor de paquetes y entornos virtuales |
| GeoPandas | Procesamiento de datos geoespaciales |
| Folium | Visualizacion de mapas interactivos |
| Google Colab | Entorno de ejecucion en la nube |
| GeoJSON | Formato de datos geograficos |

---

## Como Ejecutar
1. Abrir el notebook en Google Colab.
2. Asegurarse de que el archivo shapefile este disponible en `Data/shape_geo/`.
3. Ejecutar las celdas secuencialmente.
4. El notebook extrae automaticamente POIs de OpenStreetMap dentro del poligono.
5. Se genera un mapa interactivo con control de capas por categoria.
6. La herramienta Draw permite dibujar/editar poligonos para filtrar datos.
7. Los datos y mapas generados se exportan a `Outputs/`.

Para ejecucion local con uv:

```bash
uv venv
uv pip install geopandas folium mapclassify osmnx
```

---

## Repositorio

- **URL:** https://github.com/j0rg3c45/Corredor_San_fernando.git
- **Rama principal:** main


