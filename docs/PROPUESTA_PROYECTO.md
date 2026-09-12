# Propuesta de Proyecto de Portafolio
## Monitoreo de regeneración natural post-incendio con Planet NICFI: de la investigación técnica a la demo de preventa

**Preparado por:** Stephanie Leitón Ramírez
**Contexto:** Postulación al puesto de Arquitecto/a de Soluciones, Latinoamérica — Planet Labs

[![Asistido por IA [Claude]](https://img.shields.io/badge/asistido%20por-IA-purple)]()
---

## 1. Justificación

Este puesto no evalúa solo conocimiento técnico geoespacial — evalúa la capacidad de **traducir ese conocimiento en valor de negocio para un cliente** dado el interés en el tema de restauración forestal en Guanacaste, Costa Rica.

Este proyecto de portafolio estudia el comportamiento de la **regeneración** de zonas afectadas por incendios forestales en Guanacaste, usando el analisis de series de tiempo satelitales. 

Es un caso de uso real y verificable (sin necesidad de simular ninguna intervención), que demuestra exactamente la pieza que la oferta pide: convertir trabajo técnico geoespacial en una demo, una narrativa y una propuesta de solución — el tipo de entregable que un Solutions Architect de preventa produce para un cliente real.

## 2. Objetivo del proyecto

Construir un análisis reproducible del comportamiento de la **regeneración de la vegetación** en un área quemada real del Área de Conservación Guanacaste (identificada vía el Sistema Nacional de Información Territorial (SNIT)), usando series de tiempo de basemaps y empaquetarlo como una demo de preventa que responde a la pregunta: *"¿cómo se recupera la vegetación de esta zona después de un incendio, y qué evidencia satelital tenemos de ese proceso?"* Dirigido a dos audiencias distintas:

1. **Una entidad gubernamental** (p. ej. SINAC/Área de Conservación) interesada en monitorear la recuperación de zonas afectadas por incendios con evidencia objetiva y sin necesidad de patrullajes terrestres constantes.
2. **Una organización de conservación/ONG** interesada en identificar qué zonas se regeneran más lento y podrían necesitar intervención activa.
3. **Una entidad privada** colaboradora que necesita invetigar el comportamiento los cambios a tracés del tiempo en la zona de estudio, afectada por los eventos, mediante heramientas automatizadas e innovación tecnológica. 

## 3. Fuente de datos

- **Planet NICFI Basemaps** — acceso gratuito para investigación/monitoreo forestal tropical, cubre toda Latinoamérica en resolución alta (~4.7m), con mosaicos mensuales/bimensuales. Solicitud de acceso vía [Planet NICFI Program](https://www.planet.com/nicfi/).
- Complementario: imágenes Sentinel-2 (Copernicus, ya tengo experiencia con esta plataforma) para contraste y validación.

## 4. Metodología

1. **Definición del área de estudio:** extracción de un polígono real de área quemada en Guanacaste desde el Sistema Nacional de Información Territorial (SNIT), recortado en QGIS a un área representativa y manejable.
2. **Descarga y preprocesamiento:** acceso a basemaps NICFI vía API, recorte al área de interés (GDAL/rasterio).
3. **Análisis de cambio temporal:** cálculo de índices de vegetación (NDVI u otro índice disponible según bandas NICFI) en una serie de tiempo desde el incendio hasta la fecha más reciente disponible, para caracterizar la trayectoria de regeneración natural (velocidad de recuperación, posibles estancamientos).
4. **Visualización:** mapas comparativos y serie temporal, pensados para una audiencia no técnica (cliente), no solo para publicación científica.
5. **Empaquetado como demo de preventa:** un guion corto de presentación (5-7 minutos) explicando qué le mostraría a un cliente, qué preguntas anticipar, y cómo se conecta con los productos reales de Planet (NICFI, Planet Insights Platform).

## 5. Entregables

| Entregable | Descripción |
|---|---|
| Repositorio GitHub | Código, notebook de análisis, README documentado |
| Notebook de análisis | Jupyter notebook con el flujo completo (descarga → procesamiento → visualización) |
| Documento de "demo de preventa" | 1-2 páginas: narrativa de cliente, capturas de los mapas, propuesta de valor |
| Publicación en LinkedIn/sitio web | Resumen del proyecto enlazando al repo, para visibilidad ante reclutadores |

## 6. Habilidades que este proyecto demuestra directamente para la oferta

- Uso práctico de datos y (potencialmente) API de Planet
- Python para procesamiento de imágenes satelitales (GDAL/rasterio)
- Capacidad de traducir análisis técnico geoespacial en una narrativa orientada a negocio
- Conexión genuina con investigación previa propia (continuidad y autenticidad, no un ejercicio artificial)
- Comunicación bilingüe (versión del resumen en español e inglés)

## 7. Cronograma estimado

| Etapa | Actividad |
|---|---|
| 1 | Solicitar acceso a NICFI, definir área de estudio, preprocesar datos |
| 2 | Análisis de cambio temporal, primeros mapas |
| 3 | Refinar visualizaciones, redactar narrativa de demo |
| 4 | Publicar repo, escribir resumen para LinkedIn/portafolio, practicar presentación en inglés |


