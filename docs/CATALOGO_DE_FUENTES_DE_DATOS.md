# Inventario maestro de fuentes de datos abiertos

**Proyecto:** Plataforma de apoyo a decisiones públicas ante catástrofes  
**Revisión:** 25 de julio de 2026  
**Alcance inicial:** incendios forestales, inundaciones, tornados y riesgos socioambientales asociados  
**Prioridad territorial:** Argentina, provincia de Córdoba y municipios; cobertura internacional complementaria

---

## 1. Propósito

Este documento registra y clasifica fuentes de información candidatas para el núcleo abierto de la plataforma. No es una lista promocional de portales: cada fuente debe superar una evaluación jurídica, técnica, científica y operativa antes de convertirse en un conector.

El objetivo es que toda información incorporada sea:

- confiable y trazable;
- producida o mantenida por una institución competente;
- públicamente accesible;
- reutilizable bajo una licencia abierta o un régimen público inequívoco;
- documentada;
- interoperable o descargable en formatos procesables;
- adecuada para el uso previsto;
- reproducible por terceros;
- reemplazable si el servicio deja de estar disponible.

---

## 2. Regla de admisión

Una fuente se incorpora al núcleo solamente cuando se verifican, como mínimo:

1. **Autoridad:** organismo público, universidad, organismo científico, agencia internacional o iniciativa técnica reconocida.
2. **Licencia:** licencia abierta explícita o régimen de reutilización pública inequívoco.
3. **Acceso:** consulta o descarga sin convenio privado, pago, autorización individual ni credencial institucional restringida.
4. **Trazabilidad:** organismo, producto, versión, fecha y método de acceso identificables.
5. **Documentación:** descripción de variables, unidades, resolución, metodología y limitaciones.
6. **Funcionalidad:** recurso accesible y técnicamente consumible.
7. **Rigor:** metodología compatible con el uso científico, técnico o estadístico previsto.
8. **Proporcionalidad:** resolución espacial y temporal útil para la decisión que se intenta apoyar.

La gratuidad no equivale a apertura. Una fuente gratuita puede quedar excluida si exige registro obligatorio, token, licencia no comercial, aceptación individual, prohíbe la redistribución o no declara licencia.

---

## 3. Estados del inventario

- **VERDE — núcleo abierto:** cumple los criterios generales y puede diseñarse un conector.
- **AMARILLO — revisión o uso complementario:** es científicamente valiosa, pero requiere revisar licencia por producto, condiciones de redistribución, estabilidad o acceso.
- **ROJO — fuera del núcleo:** exige cuenta, token, convenio, pago, licencia restrictiva, permiso especial o presenta términos incompatibles o ambiguos.

Ninguna fuente amarilla o roja puede transformarse en dependencia esencial.

---

## 4. Metadatos obligatorios por fuente

Cada conector deberá conservar:

- identificador interno;
- nombre del organismo y producto;
- jurisdicción y cobertura;
- fenómeno o dominio;
- variables y unidades;
- formato y protocolo;
- sistema de referencia espacial;
- resolución espacial;
- resolución temporal;
- frecuencia de actualización;
- fecha de consulta;
- versión o edición;
- licencia y atribución;
- URL de datos y documentación;
- transformaciones aplicadas;
- controles de calidad;
- limitaciones conocidas;
- decisiones que puede apoyar;
- fuente alternativa o mecanismo de respaldo.

---

# 5. Fuentes argentinas nacionales

| Estado | Fuente / producto | Organismo | Dominio y utilidad | Acceso | Observaciones |
|---|---|---|---|---|---|
| VERDE | Base de Datos Geográfica Institucional y Argenmap | Instituto Geográfico Nacional (IGN) | límites, localidades, red vial, hidrografía, infraestructura, toponimia y cartografía base | WMS, WFS, WMTS, TMS/XYZ y descargas SIG | Referencia geoespacial oficial. Prioridad máxima. |
| VERDE | IG-GIRD, información geoespacial para la gestión integral del riesgo | IGN | amenazas, vulnerabilidad y riesgo de desastres | WMS y WFS | Validar fecha y metodología de cada capa. |
| VERDE | Modelos digitales de elevaciones y ortomosaicos publicados | IGN | relieve, pendientes, escorrentía, accesibilidad y análisis territorial | WMS, WMTS y descargas | Verificar resolución y cobertura por producto. |
| VERDE | Cobertura de suelo y vegetación | IGN | combustible vegetal, erosión, infiltración y exposición ambiental | WMS/WMTS y descargas | Complementar con productos satelitales recientes. |
| VERDE | API Georef | Jefatura de Gabinete / Datos Argentina | normalización de provincias, departamentos, municipios, localidades y direcciones | API REST / OpenAPI | Útil para interoperabilidad territorial, no para análisis físico del riesgo. |
| VERDE | Portal Datos Argentina | Estado Nacional | catálogo transversal de datos públicos | API de catálogo y descargas | Admitir únicamente datasets con licencia explícita, responsable y actualización verificables. |
| VERDE | Infraestructura de Datos Espaciales de la República Argentina | IDERA | descubrimiento de geoservicios oficiales federales | catálogo y nodos institucionales | Es un punto de descubrimiento; la licencia debe verificarse en el organismo productor. |
| VERDE | IDE Ambiental | autoridad ambiental nacional | áreas protegidas, biodiversidad, bosques, suelos, agua y otras capas ambientales | WMS, WFS y descargas | Priorizar capas con metadatos completos y autoridad temática definida. |
| VERDE | Sistema Nacional de Información Hídrica | autoridad hídrica nacional | estaciones, niveles, caudales, embalses y variables hidrológicas | consulta y descargas públicas según producto | Confirmar frecuencia, unidades, calidad y continuidad de cada serie. |
| VERDE | Información y pronósticos hidrológicos | Instituto Nacional del Agua (INA) | crecidas, niveles, caudales, inundaciones y modelación | productos y servicios públicos | No confundir pronóstico con observación; registrar horizonte y fecha de emisión. |
| VERDE | Información geológica y geoambiental | SEGEMAR | geología, geomorfología, peligrosidad geológica, remoción en masa y suelos | geoportal, mapas y descargas | Fuente oficial temática; verificar escala de cada carta o capa. |
| VERDE | Censo Nacional y cartografía estadística | INDEC | población, hogares, vivienda, vulnerabilidad y exposición | tablas, cartografía y descargas | Usar la edición censal y unidad geográfica correctas; documentar desactualización intercensal. |
| VERDE | Red de estaciones y datos meteorológicos abiertos publicados | Servicio Meteorológico Nacional (SMN) | precipitación, temperatura, viento, alertas y clima | descargas y servicios públicos por producto | Fuente primaria argentina. Separar observaciones, alertas, pronósticos y climatologías. |
| VERDE | Sistema de Alerta Temprana | SMN | alertas oficiales de tormenta, viento, lluvia, nieve y otros fenómenos | publicación pública estructurada cuando esté disponible | Las alertas son productos operativos con vigencia, no capas históricas permanentes. |
| VERDE | Estadísticas vitales y establecimientos públicos publicados con licencia | Ministerio de Salud / Datos Argentina | exposición sanitaria, capacidad territorial y vulnerabilidad | CSV y otros formatos | Rechazar recursos sin licencia especificada o con actualización obsoleta. |
| VERDE | Datos energéticos abiertos | Secretaría de Energía | infraestructura energética, generación, combustibles y servicios | portal y descargas | Incorporar únicamente capas con localización y licencia verificadas. |
| VERDE | Datos de transporte abiertos | organismos nacionales de transporte | rutas, ferrocarriles, puertos, aeródromos y movilidad | descargas y servicios según organismo | Contrastar con IGN y datos provinciales; registrar responsable de actualización. |
| VERDE | Bosques nativos y ordenamiento territorial publicados | autoridad ambiental nacional y provincias | combustible forestal, conservación, erosión y recuperación | IDE Ambiental y descargas | No asumir homogeneidad metodológica entre provincias. |
| AMARILLO | Imágenes y productos de CONAE | CONAE | observación de la Tierra, radar y productos de emergencia | acceso variable según misión y producto | Incluir solo productos con licencia abierta y descarga anónima demostrada. Los que exigen registro quedan fuera del núcleo. |

---

# 6. Fuentes de la provincia de Córdoba

| Estado | Fuente / producto | Organismo | Dominio y utilidad | Acceso | Observaciones |
|---|---|---|---|---|---|
| VERDE | Mapas Córdoba | IDECOR | catastro, límites, ambiente, infraestructura, producción, riesgo y territorio | WMS, WFS, WCS, descargas y visores | Principal infraestructura geoespacial provincial. Verificar licencia por mapa o capa. |
| VERDE | Radios municipales y límites oficiales de localidades | IDECOR / Gobierno de Córdoba | jurisdicción, competencia municipal y análisis territorial | WMS, WFS y KML | Prioridad alta para interoperabilidad municipal. |
| VERDE | Modelos de elevación, relieve y variables derivadas publicados | IDECOR | pendientes, cuencas, escorrentía, exposición y accesibilidad | WCS, WMS y descargas | Registrar resolución y fecha del modelo utilizado. |
| VERDE | Coberturas y mapas de uso del suelo publicados | IDECOR y organismos provinciales | vegetación, agricultura, urbanización, incendios y erosión | geoservicios y descargas | Revisar metodología, fecha y clases. |
| VERDE | Gobierno Abierto Córdoba | Gobierno de Córdoba | catálogo estadístico y administrativo provincial | descargas abiertas | Solo admitir recursos con licencia, responsable y periodicidad verificables. |
| VERDE | Datos públicos de ambiente y recursos naturales publicados en Mapas Córdoba | autoridad ambiental provincial / IDECOR | bosque nativo, áreas protegidas, cobertura, suelos y recursos | WMS/WFS/descargas | La autoridad temática debe constar en los metadatos. |
| VERDE | Infraestructura vial provincial publicada | Vialidad Provincial / IDECOR | rutas, caminos y accesibilidad | geoservicios o descargas | Contrastar con IGN; la condición operativa de un camino requiere dato temporal adicional. |
| VERDE | Parcelas, localidades y estructura territorial pública | Catastro / IDECOR | exposición, referencia espacial y planificación | WMS/WFS según capa | Evitar publicar datos personales o atributos catastrales sensibles. |
| AMARILLO | Datos de incendios y manejo del fuego provinciales | organismos provinciales competentes | perímetros, ocurrencias, recursos y respuesta | publicación variable | Incorporar solo datasets públicos, abiertos y documentados; no depender de sistemas internos. |
| AMARILLO | Datos hidrometeorológicos provinciales | APRHI y organismos provinciales | niveles, cuencas, presas, perforaciones y recursos hídricos | publicación variable | Excluir cualquier recurso que requiera convenio o permiso individual. |
| AMARILLO | Inventarios de Defensa Civil, salud, agua, energía y telecomunicaciones | organismos provinciales y prestadores | capacidad de respuesta e infraestructura crítica | generalmente parcial | Solo como módulos locales voluntarios cuando exista licencia y publicación abierta. |

---

# 7. Datos municipales y comunitarios

Los datos municipales no forman parte automática del catálogo abierto. Pueden incorporarse cuando el municipio es titular o responsable, define condiciones de uso y evita información personal o sensible.

| Estado | Fuente / producto | Utilidad | Condición mínima |
|---|---|---|---|
| VERDE | límites, barrios, calles y nomencladores municipales publicados | referencia territorial | publicación oficial, licencia abierta y versión |
| VERDE | refugios, centros de evacuación y edificios públicos | respuesta y accesibilidad | ubicación validada y fecha de revisión |
| VERDE | maquinaria, recursos y capacidades agregadas | planificación | sin datos personales ni información operativa sensible |
| VERDE | captaciones, tanques y redes públicas no sensibles | continuidad de servicios | evaluación previa de seguridad y calidad |
| VERDE | puntos de residuos, transferencia y tratamiento | recuperación y riesgos secundarios | autoridad municipal y actualización |
| VERDE | relevamientos de daños anonimizados | priorización | protocolo, fecha, autor y nivel de validación |
| AMARILLO | fotografías y reportes ciudadanos | evidencia complementaria | consentimiento, geolocalización, fecha y verificación |
| ROJO | datos personales, domicilios de población vulnerable o infraestructura estratégica sensible | — | no se incorporan al núcleo abierto |

---

# 8. Fuentes internacionales de cartografía y límites

| Estado | Fuente / producto | Organismo | Utilidad | Licencia / acceso | Observaciones |
|---|---|---|---|---|---|
| VERDE | OpenStreetMap | OpenStreetMap Foundation y comunidad | caminos, edificios, servicios y puntos de interés | ODbL; API y extractos | Muy útil, pero no es autoridad oficial. Debe conservar atribución y reglas de base derivada. |
| VERDE | Natural Earth | comunidad mantenedora con apoyo institucional | cartografía global de pequeña escala | dominio público | Adecuado para mapas regionales o globales, no para decisiones locales. |
| VERDE | geoBoundaries | William & Mary geoLab | límites administrativos globales | CC BY 4.0 | Útil como respaldo internacional; priorizar límites oficiales argentinos. |
| VERDE | Global Human Settlement Layer (GHSL) | Comisión Europea, JRC | asentamientos, urbanización, población y superficie construida | reutilización abierta con atribución | Producto científico global; validar edición y resolución. |
| VERDE | WorldPop | Universidad de Southampton y socios | población gridded, edad y sexo | CC BY 4.0; algunos derivados ODbL | No reemplaza al censo oficial; útil para exposición espacial y escenarios. |
| AMARILLO | Humanitarian Data Exchange (HDX) | OCHA | catálogo humanitario multisectorial | licencia por dataset | Admitir solo datasets cuyo recurso individual tenga licencia abierta y productor confiable. |

---

# 9. Observación de la Tierra y cobertura del suelo

| Estado | Fuente / producto | Organismo | Utilidad | Acceso / licencia | Observaciones |
|---|---|---|---|---|---|
| VERDE | Landsat Collection 2, productos de acceso abierto mediante repositorios públicos sin credencial | USGS / NASA | incendios, agua, vegetación, cambio territorial y series históricas | datos públicos; usar canal anónimo verificado | Algunos portales exigen cuenta. El conector solo puede usar una vía anónima y legalmente clara. |
| VERDE | JRC Global Surface Water | Comisión Europea, JRC | ocurrencia, estacionalidad y cambios de agua superficial | libre con reconocimiento de Copernicus/JRC | Serie histórica derivada de Landsat; no representa por sí sola una inundación actual. |
| VERDE | ESA WorldCover | Agencia Espacial Europea y consorcio WorldCover | cobertura global de suelo | CC BY 4.0 | Adecuado para contexto y exposición; comprobar año de referencia. |
| VERDE | Copernicus Global Land Service, productos con descarga abierta verificable | Copernicus | cobertura, vegetación, humedad y variables biofísicas | licencia Copernicus por producto | Registrar licencia específica y mecanismo de acceso. |
| VERDE | MODIS y VIIRS mediante repositorios públicos anónimos autorizados | NASA / NOAA | vegetación, temperatura, fuego y cobertura | datos públicos; acceso depende del repositorio | Earthdata puede exigir cuenta; no usar endpoints autenticados como dependencia del núcleo. |
| AMARILLO | Sentinel-1, Sentinel-2, Sentinel-3 y Sentinel-5P | Copernicus / ESA | radar, óptico, temperatura, atmósfera y cambio territorial | datos libres y abiertos; descarga principal puede exigir cuenta | Científicamente prioritarios, pero el conector del núcleo exige una vía anónima estable. |
| AMARILLO | Copernicus Data Space STAC | Unión Europea / ESA | descubrimiento interoperable de productos Sentinel y Copernicus | catálogo STAC público; acceso a activos puede requerir autenticación | El catálogo puede usarse para descubrimiento; validar la descarga de cada activo. |
| AMARILLO | Dynamic World | Google / World Resources Institute | cobertura del suelo casi en tiempo real | CC BY 4.0; acceso habitual mediante plataformas con cuenta | No incorporar hasta disponer de acceso reproducible sin credenciales. |
| ROJO | imágenes comerciales o productos con cláusulas de no redistribución | proveedores privados | alta resolución | licencia comercial | Fuera del núcleo abierto. |

---

# 10. Elevación, relieve, hidrografía y agua

| Estado | Fuente / producto | Organismo | Utilidad | Licencia / acceso | Observaciones |
|---|---|---|---|---|---|
| VERDE | modelos digitales oficiales publicados por IGN | IGN | pendiente, cuencas, escorrentía y accesibilidad | geoservicios y descargas públicas | Primera opción para Argentina cuando la cobertura y resolución sean suficientes. |
| VERDE | JRC Global Surface Water | Comisión Europea, JRC | dinámica histórica del agua superficial | reutilización abierta con atribución | Complementar con hidrografía oficial y observaciones actuales. |
| VERDE | HydroBASINS / HydroRIVERS cuando su licencia permita el uso y producto derivado previsto | HydroSHEDS / WWF | cuencas y red hidrográfica global | licencia específica HydroSHEDS | Revisar restricciones de redistribución antes de incorporarlo como verde definitivo. |
| AMARILLO | HydroSHEDS core | WWF y socios científicos | hidrografía y cuencas globales | uso científico, educativo y comercial permitido bajo licencia específica | La licencia no es una licencia abierta estándar; mantener en amarillo hasta revisión jurídica. |
| AMARILLO | Copernicus DEM | Copernicus | elevación global | términos propios y acceso variable | Usar solo si existe descarga abierta y redistribución compatible. |
| AMARILLO | FABDEM | Universidad de Bristol y socios | elevación corregida por edificios y vegetación | licencia con restricciones según edición | No usar si impone no comercial o compartir igual incompatible con el proyecto. |
| AMARILLO | Global Flood Awareness System (GloFAS) | Copernicus EMS / ECMWF | pronóstico y monitoreo global de inundaciones | acceso y licencia por producto; frecuentemente requiere cuenta | Valioso científicamente, pero no debe ser dependencia abierta esencial. |

---

# 11. Meteorología y clima

| Estado | Fuente / producto | Organismo | Utilidad | Acceso / licencia | Observaciones |
|---|---|---|---|---|---|
| VERDE | observaciones y alertas oficiales argentinas | SMN | estado y evolución meteorológica nacional | publicación pública por producto | Prioridad operativa para Argentina. |
| VERDE | GHCN Daily y otros archivos climáticos públicos | NOAA NCEI | observaciones históricas globales de estaciones | acceso público; API/descargas | Verificar cobertura argentina, control de calidad y latencia. |
| VERDE | NOAA NCEI Web Services, OPeNDAP y THREDDS públicos | NOAA | clima, satélite, radar y modelos | servicios públicos en JSON, CSV, NetCDF y OGC | Algunos endpoints pueden exigir token; solo usar los anónimos. |
| VERDE | NOAA Physical Sciences Laboratory, datos climáticos gridded | NOAA PSL | precipitación, temperatura, reanálisis e índices | descargas y THREDDS públicos | Verificar licencia y fuente original de cada dataset hospedado. |
| VERDE | CHIRPS mediante repositorio oficial público | USGS / Climate Hazards Center | precipitación histórica y casi en tiempo real | descarga pública | Producto modelado con estaciones; no reemplaza pluviómetros oficiales locales. |
| VERDE | GFS mediante repositorios públicos oficiales | NOAA NCEP | pronóstico meteorológico global | datos públicos | Registrar corrida, horizonte, resolución y variable. |
| AMARILLO | ERA5 y ERA5-Land | Copernicus Climate Change Service / ECMWF | reanálisis atmosférico y terrestre | licencia abierta con atribución, pero CDS exige cuenta/aceptación | Científicamente excelente para análisis histórico; fuera del conector anónimo esencial. |
| AMARILLO | Open-Meteo | proveedor de agregación y modelos abiertos | acceso simplificado a pronósticos | licencia y fuente por modelo | Puede servir como prototipo o respaldo, no como fuente científica primaria única. |
| AMARILLO | Meteostat | proyecto abierto | observaciones históricas agregadas | CC BY-NC 4.0 en parte de sus productos | La cláusula no comercial impide incorporarlo al núcleo general. |

---

# 12. Incendios forestales

| Estado | Fuente / producto | Organismo | Utilidad | Acceso / licencia | Observaciones |
|---|---|---|---|---|---|
| VERDE | focos, perímetros o estadísticas oficiales publicados por organismos argentinos | organismos nacionales y provinciales competentes | detección, antecedentes y validación territorial | datos públicos abiertos cuando existan | Priorizar la fuente oficial local y conservar fecha de detección. |
| VERDE | productos MODIS/VIIRS de fuego disponibles por descarga pública anónima oficial | NASA / NOAA | detecciones térmicas y antecedentes | acceso público por producto | Detección no equivale a perímetro ni superficie quemada. |
| AMARILLO | NASA FIRMS API | NASA | focos activos y áreas quemadas | API operativa requiere MAP_KEY | No se integra al núcleo sin credenciales. Puede documentarse como fuente manual o futura. |
| AMARILLO | Copernicus Emergency Management Service Mapping | Comisión Europea | mapas rápidos y de riesgo | productos públicos; términos por servicio | Solo incorporar productos con descarga y licencia verificadas. |
| AMARILLO | Global Wildfire Information System | Comisión Europea / Copernicus | monitoreo global de incendios | acceso y licencia por producto | Verificar endpoint, descarga y atribución antes de automatizar. |

---

# 13. Biodiversidad, ecosistemas y conservación

| Estado | Fuente / producto | Organismo | Utilidad | Licencia / acceso | Observaciones |
|---|---|---|---|---|---|
| VERDE | GBIF API y descargas de ocurrencias | Global Biodiversity Information Facility | especies, ocurrencias y evidencia de biodiversidad | datasets CC0, CC BY o CC BY-NC identificados individualmente | El núcleo solo debe usar registros CC0 o CC BY. Excluir CC BY-NC para mantener reutilización amplia. |
| VERDE | áreas protegidas oficiales argentinas | autoridad ambiental nacional y provincias | exposición de valores de conservación | IDE Ambiental y geoservicios oficiales | Prioridad sobre bases globales para Argentina. |
| AMARILLO | Protected Planet / base mundial de áreas protegidas | UNEP-WCMC / IUCN | contraste internacional y cobertura global | API con token y restricciones, descarga bajo términos propios | No cumple el criterio de acceso anónimo irrestricto del núcleo. |
| AMARILLO | Lista Roja de UICN | IUCN | estado de conservación | términos y acceso propios | Útil como referencia científica, no como dependencia abierta sin revisión jurídica. |

---

# 14. Población, vulnerabilidad y salud

| Estado | Fuente / producto | Organismo | Utilidad | Licencia / acceso | Observaciones |
|---|---|---|---|---|---|
| VERDE | Censo Nacional y cartografía censal | INDEC | población, hogares, vivienda y vulnerabilidad | publicación oficial | Fuente primaria nacional. |
| VERDE | WorldPop | Universidad de Southampton y socios | población espacial y estructura demográfica | CC BY 4.0; algunos derivados ODbL | Usar como estimación modelada, con incertidumbre explícita. |
| VERDE | GHSL Population y Built-up | Comisión Europea, JRC | población, urbanización y superficie construida | reutilización abierta con atribución | Útil para comparación y zonas sin cartografía local reciente. |
| VERDE | establecimientos de salud del IGN con licencia abierta verificada | IGN | exposición y accesibilidad sanitaria | SHP, JSON, CSV y geoservicios según producto | Confirmar fecha y fuente temática original. |
| AMARILLO | datasets sanitarios nacionales sin licencia declarada | organismos de salud / Datos Argentina | capacidad y vulnerabilidad sanitaria | descarga pública | No integrar hasta que la licencia se explicite. |
| ROJO | datos nominales de pacientes, domicilios o condiciones individuales | cualquier organismo | — | restringido | Fuera del núcleo abierto. |

---

# 15. Infraestructura, transporte y servicios críticos

| Estado | Fuente / producto | Organismo | Utilidad | Licencia / acceso | Observaciones |
|---|---|---|---|---|---|
| VERDE | red vial, ferrocarriles, puertos, aeródromos y edificios públicos | IGN | accesibilidad, exposición y logística | WMS/WFS/descargas | Referencia nacional primaria. |
| VERDE | infraestructura provincial publicada | IDECOR y organismos provinciales | rutas, edificios, servicios y equipamiento | geoservicios y descargas | Verificar responsable y actualización. |
| VERDE | OpenStreetMap | OSMF y comunidad | detalle complementario de caminos, edificios y servicios | ODbL | Requiere control de completitud y fecha. |
| VERDE | Global Power Plant Database cuando su edición vigente conserve licencia abierta | World Resources Institute | generación eléctrica y exposición | licencia abierta por edición | No representa redes de distribución ni estado operativo. |
| AMARILLO | datos de prestadores de agua, energía y telecomunicaciones | empresas y entes reguladores | continuidad de servicios | publicación variable | Solo integrar datasets abiertos; nunca depender de inventarios internos. |
| ROJO | ubicación detallada de infraestructura crítica sensible | organismos o prestadores | — | sensible | Debe protegerse o generalizarse. |

---

# 16. Información humanitaria y eventos

| Estado | Fuente / producto | Organismo | Utilidad | Acceso / licencia | Observaciones |
|---|---|---|---|---|---|
| VERDE | ReliefWeb API: desastres, países y metadatos de reportes | OCHA | identificación y seguimiento documental de eventos | API pública, sin costo | El contenido de informes puede conservar derechos del productor; usar metadatos y enlaces, no republicar textos completos. |
| VERDE | GDACS, productos públicos con condiciones compatibles | Naciones Unidas / Comisión Europea | alertas y eventos globales | feeds y servicios públicos | Útil para contexto internacional; no reemplaza alertas argentinas. |
| AMARILLO | HDX | OCHA | descubrimiento de datos humanitarios | licencia por dataset | Revisar cada recurso, productor y licencia. |
| AMARILLO | Copernicus EMS Rapid Mapping | Comisión Europea | cartografía postevento | activación y producto variables | Incorporar únicamente productos abiertos y técnicamente documentados. |

---

# 17. Fuentes excluidas del núcleo por política

Quedan fuera como dependencias esenciales:

- API que requieran token, clave o cuenta personal;
- productos sujetos a pago o convenios;
- datasets con licencia no comercial;
- servicios que prohíban redistribución o productos derivados necesarios;
- portales que indiquen “sin licencia especificada”;
- fuentes comunitarias sin trazabilidad suficiente como única evidencia;
- imágenes comerciales;
- datos personales o sensibles;
- inventarios internos no publicados;
- modelos o índices sin metodología documentada;
- contenido de noticias como evidencia primaria;
- datos cuya escala no sea adecuada para decisiones locales.

Ejemplos que deben mantenerse en amarillo o rojo hasta resolver sus condiciones: NASA FIRMS API con MAP_KEY, CDS/ERA5 con cuenta y aceptación individual, descargas Sentinel que exijan autenticación, Protected Planet API con token y restricciones, datasets CC BY-NC, y recursos de Datos Argentina sin licencia explícita.

---

# 18. Jerarquía de evidencia

Cuando varias fuentes describen el mismo elemento, se aplicará esta prioridad general:

1. observación o registro oficial local validado;
2. organismo provincial competente;
3. organismo nacional competente;
4. producto científico internacional oficial;
5. producto científico global modelado;
6. base colaborativa abierta;
7. reporte ciudadano verificado;
8. fuente periodística o documental secundaria.

La jerarquía puede variar por dominio. Un modelo global no debe desplazar una medición local confiable, y una capa oficial antigua no debe ocultar una observación reciente validada.

---

# 19. Pruebas obligatorias antes de aprobar un conector

Cada fuente deberá superar:

- prueba de disponibilidad;
- prueba de descarga o consulta anónima;
- revisión de licencia y atribución;
- validación de esquema;
- validación de sistema de coordenadas;
- validación de geometrías;
- control de unidades y valores imposibles;
- control de cobertura territorial;
- control de resolución espacial y temporal;
- revisión de actualización y latencia;
- comparación con una fuente independiente;
- prueba de caída y mecanismo de respaldo;
- registro de procedencia y transformaciones;
- revisión de privacidad y seguridad;
- prueba de reproducibilidad.

---

# 20. Prioridad de implementación

## Prioridad 1 — base territorial argentina

- IGN: Argenmap, WMS/WFS, límites, red vial, hidrografía e infraestructura;
- API Georef;
- IDE Ambiental;
- IDECOR / Mapas Córdoba;
- INDEC;
- SMN;
- INA y Sistema Nacional de Información Hídrica;
- SEGEMAR.

## Prioridad 2 — exposición y contexto global abierto

- OpenStreetMap;
- WorldPop;
- GHSL;
- geoBoundaries;
- Natural Earth;
- JRC Global Surface Water;
- ESA WorldCover;
- GBIF con registros CC0/CC BY;
- NOAA NCEI y PSL mediante endpoints anónimos;
- CHIRPS.

## Prioridad 3 — productos avanzados sujetos a comprobación de acceso

- Sentinel y Copernicus Data Space;
- ERA5 / ERA5-Land;
- GloFAS;
- NASA FIRMS;
- Copernicus EMS;
- HydroSHEDS;
- Protected Planet.

Estos productos no deben entrar al núcleo hasta demostrar acceso sin credenciales y compatibilidad de licencia con el uso, almacenamiento, visualización y redistribución previstos.

---

# 21. Decisiones que este inventario debe apoyar

El inventario no se evalúa por cantidad de enlaces, sino por su capacidad para apoyar preguntas concretas:

- ¿dónde ocurrió el evento y cuál es su extensión?
- ¿qué población y viviendas están expuestas?
- ¿qué caminos y servicios podrían quedar interrumpidos?
- ¿qué cursos, captaciones y superficies de agua pueden afectarse?
- ¿qué pendientes y cuencas favorecen riesgos en cascada?
- ¿qué cobertura vegetal o combustible existe?
- ¿qué ecosistemas y áreas protegidas están expuestos?
- ¿qué establecimientos de salud, escuelas y refugios se encuentran cerca?
- ¿qué evidencia es observada, modelada o inferida?
- ¿qué dato falta y cuánto reduce la confianza?

---

# 22. Regla de mantenimiento

Este inventario es un documento vivo. Toda revisión deberá registrar:

- fecha de comprobación;
- responsable de la revisión;
- cambio de URL, esquema o versión;
- cambio de licencia;
- alta, baja o degradación del servicio;
- motivo para cambiar el estado verde, amarillo o rojo;
- impacto sobre conectores y análisis existentes.

Una fuente verde que cambie sus condiciones debe desactivarse preventivamente hasta completar una nueva revisión.