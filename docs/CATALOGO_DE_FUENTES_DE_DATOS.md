# Catálogo maestro de fuentes de datos

**Proyecto:** Plataforma de apoyo a decisiones públicas ante catástrofes  
**Verificación inicial:** 25 de julio de 2026  
**Alcance:** incendios forestales, inundaciones y tornados; prioridad territorial Córdoba y Villa Yacanto.

## Propósito

Este catálogo registra fuentes candidatas y verificadas. Cada conector deberá conservar organismo, URL, producto, fecha de consulta, cobertura, resolución, licencia, transformación y nivel de calidad. Una URL activa no garantiza que el esquema, la frecuencia o la licencia permanezcan estables.

## Estados

- **Apta para integración:** API, descarga estructurada o geoservicio utilizable.
- **Integración condicionada:** requiere cuenta, token, convenio, licencia o autorización.
- **Consulta manual:** fuente útil sin interfaz automatizable confirmada.
- **Pendiente local:** requiere inventario, responsable y validación institucional.
- **Complementaria:** útil para contraste, no como única evidencia.

## Reglas

1. Priorizar al organismo productor oficial.
2. No modificar silenciosamente el dato original.
3. Separar observaciones, detecciones, pronósticos y modelos.
4. Mostrar fecha y calidad de cada dato.
5. No confundir una detección satelital con un daño confirmado.
6. Implementar tolerancia a fallos y registrar cambios de esquema.
7. Revisar el catálogo cada seis meses y antes de producción.

# Fuentes nacionales

## Datos Argentina

- **Portal:** https://www.datos.gob.ar/
- **APIs:** https://www.datos.gob.ar/apis
- **Acceso:** CKAN, API Georef, Series de Tiempo y descargas por dataset.
- **Uso:** descubrimiento de datos, normalización territorial e indicadores públicos.
- **Estado:** **apta para integración**.
- **Límite:** calidad y actualización dependen de cada organismo publicador.

## Servicio Meteorológico Nacional

- **Alertas:** https://www.smn.gob.ar/alertas
- **Datos:** https://www.smn.gob.ar/descarga-de-datos
- **Productos:** alertas, observaciones, radares, satélite, modelos y clima.
- **Uso:** tormentas, viento, lluvias, condiciones para incendios e inundaciones.
- **Estado:** **verificada; integración técnica condicionada**.
- **Límite:** no se debe usar scraping como conector estable; hay que confirmar interfaces oficiales por producto. Una alerta no confirma daños ni un tornado observado.

## Instituto Geográfico Nacional

- **Documentación OGC:** https://www.ign.gob.ar/NuestrasActividades/InformacionGeoespacial/ServiciosOGC
- **WMS:** https://wms.ign.gob.ar/geoserver/ows?service=wms&version=1.3.0&request=GetCapabilities
- **WFS:** https://wms.ign.gob.ar/geoserver/ows?service=wfs&version=1.1.0&request=GetCapabilities
- **Riesgo WMS:** https://wms.ign.gob.ar/geoserver/ign_riesgo/ows?service=wms&version=1.3.0&request=GetCapabilities
- **Uso:** límites, localidades, caminos, hidrografía, relieve, cobertura y cartografía base.
- **Estado:** **apta para integración**.
- **Límite:** revisar escala, productor y fecha de cada capa.

## CONAE

- **Acceso:** https://www.argentina.gob.ar/ciencia/conae/aplicaciones-de-la-informacion-satelital/acceso-la-informacion-satelital
- **SAOCOM:** https://www.argentina.gob.ar/ciencia/conae/productos-saocom/catalogo-de-imagenes
- **Uso:** inundaciones, incendios, humedad de suelo y emergencias ambientales.
- **Estado:** **integración condicionada**.
- **Límite:** búsqueda pública, pero descarga, procesamiento o nuevas adquisiciones pueden requerir registro, licencia o convenio.

## Instituto Nacional del Agua

- **SIyAH:** https://alerta.ina.gob.ar/
- **Mapa público:** https://alerta.ina.gob.ar/pub/mapa
- **Alerta Cuenca del Plata:** https://www.ina.gob.ar/alerta/
- **Productos:** niveles hidrométricos, tendencias, series, alertas e informes.
- **Formatos observados:** tablas, JSON, GeoJSON, KML y CSV según producto.
- **Estado:** **apta para integración por producto**.
- **Límite:** cobertura desigual y umbrales locales definidos por autoridades competentes.

## SEGEMAR — SIGAM

- **Portal:** https://sigam.segemar.gov.ar/
- **Acceso:** catálogo, WMS, WFS y CSW.
- **Uso:** geología, geomorfología, peligrosidad, erosión y recuperación.
- **Estado:** **apta para integración**.
- **Límite:** escala y actualización variables; no reemplaza estudios locales.

## INDEC

- **Portal geoestadístico:** https://www.indec.gob.ar/indec/web/Nivel4-Tema-1-16-81
- **Productos:** marco geoestadístico e indicadores del Censo 2022.
- **Uso:** población expuesta, vivienda, servicios y vulnerabilidad estructural.
- **Estado:** **apta para integración por descargas**.
- **Límite:** no representa desplazamientos ni afectación en tiempo real.

## INTA

- **Uso:** suelos, cobertura, aptitud, erosión y recuperación.
- **Estado:** **prioritaria, pendiente de relevamiento dataset por dataset**.
- **Regla:** no tratar un portal genérico como una API única; registrar cada producto y licencia.

# Provincia de Córdoba

## IDECOR — Mapas Córdoba

- **Portal:** https://www.idecor.gob.ar/mapas-cordoba/
- **WFS:** https://idecor-ws.mapascordoba.gob.ar/geoserver/idecor/wfs
- **WMS:** https://idecor-ws.mapascordoba.gob.ar/geoserver/idecor/wms
- **Acceso:** WMS, WFS, WCS y descargas.
- **Uso:** catastro, límites, suelo, ambiente, infraestructura, hidrografía y capas temáticas provinciales.
- **Estado:** **apta para integración**.
- **Límite:** validar nombre, productor, escala, licencia y actualización de cada capa.

## APRHI

- **Uso esperado:** cuencas, cursos, captaciones, perforaciones, infraestructura y monitoreo hídrico.
- **Estado:** **pendiente de inventario institucional**.
- **Límite:** no se confirmó una API pública general; parte de la información puede estar en IDECOR y otra requerir solicitud o convenio.

## Manejo del Fuego y Defensa Civil

- **Uso esperado:** riesgo, focos reportados, perímetros, recursos y estado operativo.
- **Estado:** **integración condicionada**.
- **Regla:** separar información pública de información operativa restringida y no inventar endpoints.

# Fuentes municipales y regionales

## Villa Yacanto

Datos prioritarios:

- captaciones, tanques y redes principales de agua;
- caminos, puentes, alcantarillas y puntos de corte;
- centros de salud, escuelas, edificios y refugios;
- barrios y población vulnerable;
- maquinaria, personal y recursos disponibles;
- residuos, sitios de disposición y saneamiento;
- relevamientos de campo y perímetros verificados.

**Estado:** **pendiente de inventario local**. Cada conjunto deberá tener responsable, fecha, método, sensibilidad, autorización y procedimiento de actualización.

## Cooperativas y prestadores

- **Datos:** agua, saneamiento, interrupciones, capacidad y calidad.
- **Estado:** **requiere convenio y clasificación de seguridad**.
- **Regla:** no publicar infraestructura sensible sin autorización.

# Fuentes internacionales

## NASA FIRMS

- **Portal:** https://firms.modaps.eosdis.nasa.gov/active_fire/
- **Productos:** MODIS, VIIRS y Landsat disponibles; datos recientes y archivo.
- **Acceso:** archivos, WMS, WFS y API por área.
- **Estado:** **apta para integración con credenciales cuando correspondan**.
- **Límite:** una detección térmica no es un perímetro quemado ni confirma por sí sola un incendio; existen restricciones de resolución, nubosidad y temporalidad.

## Copernicus Emergency Management Service

- **Portal:** https://emergency.copernicus.eu/
- **Datos:** https://emergency.copernicus.eu/data/
- **Productos:** mapeo, GloFAS, Global Flood Monitoring, incendios, sequías y exposición.
- **Estado:** **apta para integración por módulos**.
- **Límite:** algunos productos bajo demanda sólo pueden ser activados por usuarios autorizados, aunque los productos publicados sean accesibles.

## Copernicus Data Space

- **Portal:** https://dataspace.copernicus.eu/
- **Productos:** Sentinel-1, Sentinel-2 y otras misiones.
- **Estado:** **apta para integración condicionada a cuenta y procesamiento**.
- **Límite:** requiere búsqueda y procesamiento; las imágenes ópticas pueden estar afectadas por nubes.

## USGS EarthExplorer

- **Portal:** https://earthexplorer.usgs.gov/
- **Uso:** Landsat, cambios de cobertura, incendios e inundaciones.
- **Estado:** **complementaria**.
- **Límite:** no es una alerta inmediata y requiere procesamiento.

## GDACS

- **Portal:** https://www.gdacs.org/
- **Uso:** alertas y contexto internacional.
- **Estado:** **plataforma verificada; integración técnica pendiente**.
- **Límite:** no reemplaza alertas nacionales ni evaluación local.

## Humanitarian Data Exchange

- **Portal:** https://data.humdata.org/
- **Acceso:** CKAN y descargas por dataset.
- **Uso:** población, límites, infraestructura y datos humanitarios.
- **Estado:** **complementaria y automatizable**.
- **Límite:** verificar productor, fecha, licencia y precisión territorial.

## ReliefWeb

- **Portal:** https://reliefweb.int/
- **API:** https://apidoc.reliefweb.int/
- **Uso:** informes y documentos de situación.
- **Estado:** **apta para integración documental**.
- **Límite:** no es una fuente primaria de medición territorial.

## OpenStreetMap

- **Portal:** https://www.openstreetmap.org/
- **Acceso:** Overpass API y extractos.
- **Uso:** caminos, edificios, cursos de agua y puntos de interés.
- **Estado:** **complementaria y automatizable**.
- **Límite:** calidad heterogénea; no reemplaza cartografía oficial. Registrar fecha y licencia ODbL.

# Prioridad de implementación

## Prioridad 1

1. IGN.
2. IDECOR.
3. SMN mediante interfaz oficial estable.
4. NASA FIRMS.
5. INA SIyAH.
6. INDEC.
7. Datos municipales validados.
8. OpenStreetMap como complemento identificado.

## Prioridad 2

1. Copernicus CEMS y Data Space.
2. CONAE y SAOCOM.
3. SEGEMAR.
4. Cartas de suelo IDECOR/INTA.
5. GDACS, HDX y ReliefWeb.

## Mediante convenios

1. APRHI.
2. Manejo del Fuego y Defensa Civil.
3. Prestadores de agua y saneamiento.
4. Salud con protección de datos personales.
5. Infraestructura crítica y recursos operativos.

# Pruebas obligatorias de un conector

1. URL disponible.
2. Autenticación documentada.
3. Licencia compatible.
4. Campos y tipos conocidos.
5. Cobertura espacial y temporal definida.
6. Frecuencia y retraso medidos.
7. Nulos, duplicados, geometrías inválidas y valores extremos controlados.
8. Sistema de coordenadas identificado.
9. Fecha, versión y checksum registrados.
10. Manejo de caídas, timeout y cambios de esquema.
11. Significado de variables validado.
12. Comparación humana con casos conocidos.

# Pendientes

- catálogo detallado de APRHI;
- canales automatizables de Manejo del Fuego y Defensa Civil de Córdoba;
- inventario municipal de Villa Yacanto;
- responsables y permisos de prestadores;
- fuentes sanitarias agregadas;
- recursos y capacidades interinstitucionales;
- datasets específicos para tornados y daños por viento;
- evaluación jurídica de licencias y datos sensibles.

## Conclusión

El pool no debe ser una lista estática de enlaces. Debe convertirse en un registro versionado de fuentes y conectores con metadatos, controles de calidad, historial de disponibilidad y alertas de falla. Cuando una fuente no esté disponible, el sistema debe informarlo y reducir explícitamente la confianza del análisis.
