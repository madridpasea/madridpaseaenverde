# 🌿 Madrid Pasea en Verde

> Descubre rutas de paseo más saludables en Madrid, priorizando zonas con mejor calidad del aire y mayor densidad de arbolado urbano.

**[➜ Abrir la aplicación](https://madridpasea.github.io/madridpaseaenverde/)**

---

## ¿Qué puedes hacer?

| Funcionalidad | Descripción |
|---|---|
| 🗺️ **Paseo verde** | Marca origen y destino, obtén una ruta alternativa por un parque cercano y compárala con la directa en tiempo, distancia y score verde |
| 📍 **Mapa de calidad del aire** | Explora las 24 estaciones de medición con su ISR, superpuestas con la densidad de arbolado y los 203 parques, con capas activables |
| 🏆 **Rankings** | Distritos y estaciones ordenados por ISR medio, filtrables por tipo (tráfico, fondo, suburbana) |
| 📊 **Análisis histórico** | 7 años de datos (2019–2026): tendencia anual, comparativa interanual mes a mes y efecto COVID-2020 |

---

## Datos

Basada íntegramente en datos abiertos del **[Portal de Datos Abiertos del Ayuntamiento de Madrid](https://datos.madrid.es)**:

- 📁 [Calidad del aire — datos horarios](https://datos.madrid.es/dataset/201200-0-calidad-aire-horario) — 8,4M registros (2019–2026)
- 📁 [Estaciones de control atmosférico](https://datos.madrid.es/dataset/212629-0-estaciones-control-aire) — 24 estaciones
- 📁 [Arbolado detallado (Shapefile)](https://datos.madrid.es/dataset/300761-0-arbolado-especies) — 793.047 árboles
- 📁 [Parques y jardines](https://datos.madrid.es/dataset/200761-0-parques-jardines) — 203 parques

Fuentes complementarias: [OSRM](https://project-osrm.org) (routing peatonal) · [CARTO](https://carto.com/basemaps) (cartografía base) · [Umbrales OMS 2021](https://www.who.int/publications/i/item/9789240034228) 

---

## Uso

La aplicación es un **fichero HTML autocontenido** (~300 KB). No requiere instalación, servidor ni base de datos.

**[Visita la herramienta online.](https://madridpasea.github.io/madridpaseaenverde/)** O descarga el archivo en local `index.html` y ábrelo en cualquier navegador.

> Para el cálculo de rutas se necesita conexión a internet (petición a OSRM).

---

## Metodología

El **Índice de Salud Respiratoria (ISR)** es un índice compuesto (0–100) que pondera 5 contaminantes según su impacto en la salud, calibrado con los umbrales de la OMS 2021:

| Contaminante | Umbral OMS | Peso |
|---|---|---|
| PM2.5 | 25 µg/m³ | 30% |
| NO₂ | 200 µg/m³ | 25% |
| PM10 | 50 µg/m³ | 20% |
| O₃ | 120 µg/m³ | 15% |
| SO₂ | 350 µg/m³ | 10% |

El **score verde** de cada ruta combina el ISR (60%) con la densidad real de arbolado (40%), muestreada punto a punto a lo largo del recorrido.

---

Proyecto presentado a los II Premios a la Reutilización de Datos Abiertos del Ayuntamiento de Madrid 2026.
