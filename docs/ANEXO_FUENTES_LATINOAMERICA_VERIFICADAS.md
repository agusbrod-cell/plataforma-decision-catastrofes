# Anexo de fuentes latinoamericanas verificadas

**Proyecto:** Plataforma de apoyo a decisiones públicas ante catástrofes  
**Revisión:** 25 de julio de 2026  
**Estado:** inventario auditado en expansión

## 1. Alcance y advertencia metodológica

Este anexo registra infraestructuras, catálogos y servicios oficiales de América Latina cuya existencia, autoridad institucional y modalidad técnica de acceso fueron comprobadas.

La inclusión de un portal en este documento **no convierte automáticamente en abierta a cada una de sus capas**. Antes de implementar un conector se debe verificar, para el producto concreto:

1. acceso anónimo real;
2. licencia abierta explícita o régimen público inequívoco;
3. permiso de reutilización y generación de productos derivados;
4. endpoint funcional;
5. metadatos, escala, fecha, versión y organismo productor;
6. utilidad efectiva para la decisión ante desastres.

### Estados utilizados

- **VERDE-PORTAL:** infraestructura oficial, pública y accesible sin autenticación para descubrimiento o consumo de servicios. Cada capa requiere auditoría individual.
- **VERDE-DATO:** dataset individual con licencia, descarga anónima, metadatos y funcionamiento verificados.
- **AMARILLO:** falta confirmar licencia, descarga, estabilidad, documentación o acceso anónimo del producto individual.
- **ROJO:** cuenta, token, pago, autorización, licencia restrictiva o términos incompatibles.

## 2. Infraestructuras nacionales de datos geoespaciales verificadas

| Estado | País | Fuente oficial | Autoridad | Acceso comprobado | Valor para gestión del riesgo | Restricción de admisión |
|---|---|---|---|---|---|---|
| VERDE-PORTAL | Perú | Infraestructura de Datos Espaciales del Perú — IDEP | Presidencia del Consejo de Ministros / Instituto Geográfico Nacional | catálogo público, geoportales, visores, WMS, WFS, WCS y descargas | cartografía base, límites, hidrografía, fisiografía, transportes, imágenes, riesgo, ambiente y nodos sectoriales | auditar licencia y vigencia de cada capa antes de usarla como VERDE-DATO |
| VERDE-PORTAL | Colombia | Infraestructura Colombiana de Datos Espaciales — ICDE | Gobierno de Colombia / IGAC y entidades productoras | catálogo público, visor, WMS, WFS, WMTS y CSW | amenaza sísmica, suelos, cartografía, ortoimágenes, víctimas, ambiente, catastro e infraestructura | la ICDE agrega servicios de múltiples productores; revisar licencia, fecha y calidad por recurso |
| VERDE-PORTAL | Chile | Infraestructura de Datos Geoespaciales de Chile — IDE Chile / SNIT | Ministerio de Bienes Nacionales | geoportal, catálogo, descargas, WMS, WFS, formatos SIG y metadatos | amenazas, cartografía territorial, ambiente, agricultura, infraestructura y exposición | gratuidad declarada no reemplaza la comprobación de licencia abierta de cada producto |
| VERDE-PORTAL | Uruguay | Infraestructura de Datos Espaciales de Uruguay — IDEuy | Gobierno de Uruguay | descargas públicas y servicios WMS, WFS y WMTS | mapa base, áreas pobladas, ejes de calle, hipsografía, ortofotos y referencia territorial | confirmar licencia, actualización y autoridad temática del dataset concreto |
| VERDE-PORTAL | México | INEGI — servicios geográficos y GeoServer | Instituto Nacional de Estadística y Geografía | acceso anónimo a WMS, WFS, WCS, WMTS/TMS y numerosas capas | hidrografía, relieve, infraestructura, localidades, uso del suelo, geología y exposición | el servicio técnico es anónimo; documentar licencia, edición, escala y capa utilizada |
| VERDE-PORTAL | Argentina | IDERA y nodos oficiales | organismos nacionales, provinciales y municipales | catálogo, nodos, WMS, WFS, WMTS, WCS y descargas según productor | cartografía, ambiente, riesgo, hidrología, infraestructura y exposición | conservar la auditoría por organismo productor y producto |
| VERDE-PORTAL | Brasil | Infraestrutura Nacional de Dados Espaciais — INDE / Diretório Brasileiro de Dados Geoespaciais | Gobierno Federal de Brasil; gobernanza actualizada por Decreto 12.402/2025 | infraestructura legal y técnica de catálogo, metadatos y geoservicios distribuidos; WMS y WFS oficiales comprobados en nodos como ICMBio | cartografía, biodiversidad, áreas protegidas, ambiente, territorio y descubrimiento de productos federales, estaduales y municipales | la existencia en INDE no prueba licencia abierta individual; auditar cada productor y recurso |
| VERDE-PORTAL | Ecuador | Infraestructura y Geoportal del Instituto Geográfico Militar / IEDG | Instituto Geográfico Militar y Presidencia de Ecuador | directorios públicos de WMS, WFS, WMTS y TMS; cartografía y metadatos consultables | cartografía base, elevación, hidrografía, clima, vulnerabilidad, riesgos y referencia territorial | varias descargas exigen registro o usan licencias no comerciales; solo productos anónimos y compatibles pueden ser VERDE-DATO |
| VERDE-PORTAL | Bolivia | Infraestructura de Datos Espaciales del Estado Plurinacional — IDE-EPB / GeoBolivia | Vicepresidencia del Estado Plurinacional de Bolivia | catálogo público, datos abiertos, capas base, geovisor, atlas y servicios WMS declarados | recursos hídricos, ambiente, infraestructura, energía, salud, transportes, bosques y planificación territorial | “gratuito” o “datos abiertos” debe confirmarse mediante licencia y descarga por cada capa |
| VERDE-PORTAL | Paraguay | Geoportal MITIC | Ministerio de Tecnologías de la Información y Comunicación | catálogo GeoNode público y documentación de WMS, WFS, WCS y CSW | descubrimiento de datasets, mapas y documentos gubernamentales; referencia territorial e infraestructura pública | la documentación técnica no prueba licencia ni vigencia de cada recurso; mantener capas en AMARILLO hasta auditoría individual |

## 3. Fuentes sectoriales de Perú identificadas mediante IDEP

La IDEP publica o enlaza servicios de organismos con alta utilidad para catástrofes. Se registran como **candidatos AMARILLOS** hasta auditar cada capa y licencia.

| Estado | Organismo / nodo | Temas relevantes | Acceso localizado | Próxima verificación |
|---|---|---|---|---|
| AMARILLO | CENEPRED | peligros, vulnerabilidad, escenarios y riesgo | servicios WMS en el directorio IDEP | licencia, metadatos, escala y vigencia por capa |
| AMARILLO | INDECI | respuesta, emergencias y cartografía operativa | servicios WMS en el directorio IDEP | disponibilidad histórica, licencia y estructura de atributos |
| AMARILLO | Autoridad Nacional del Agua | cuencas, cuerpos de agua, hidrología y recursos hídricos | servicios WMS en IDEP | distinguir observación, inventario y modelación; comprobar descarga vectorial |
| AMARILLO | INGEMMET | geología, volcanes, movimientos en masa y peligros geológicos | servicios WMS en IDEP | escala, actualización, metodología y licencia |
| AMARILLO | Ministerio del Ambiente | ecosistemas, cobertura, ambiente y exposición | servicios WMS y geoportal | licencia por producto y posibilidad de descarga anónima |
| AMARILLO | Geobosques | pérdida y cambio de cobertura forestal | enlace oficial desde IDEP | método, periodicidad, formatos y licencia |
| AMARILLO | Ministerio de Transportes y Comunicaciones | rutas, puentes, conectividad y logística | servicios WMS en IDEP | actualización y atributos operativos |
| AMARILLO | SERNANP | áreas naturales protegidas | servicios WMS en IDEP | licencia, restricciones de redistribución y fecha |

## 4. Fuentes sectoriales de Colombia identificadas mediante ICDE

| Estado | Organismo / fuente | Temas relevantes | Evidencia técnica | Próxima verificación |
|---|---|---|---|---|
| AMARILLO | Servicio Geológico Colombiano | amenaza sísmica, volcanes, geología y movimientos en masa | capas WMS y WFS indexadas por ICDE | licencia, escala, versión y uso permitido del producto concreto |
| AMARILLO | IGAC | cartografía, suelos, coberturas, ortoimágenes y catastro | numerosos WMS, WFS y WMTS indexados | licencia individual, fecha y nivel de generalización |
| AMARILLO | IDECA Bogotá | topografía, cartografía urbana y servicios | WMS y WFS indexados por ICDE | alcance territorial, licencia y actualización |
| AMARILLO | entidades ambientales y territoriales | ambiente, cuencas, infraestructura y exposición | catálogo distribuido ICDE | autoridad temática y licencia por dataset |

## 5. Auditoría de Brasil

| Estado | Organismo / fuente | Temas relevantes | Evidencia comprobada | Restricción o próxima prueba |
|---|---|---|---|---|
| VERDE-PORTAL | INDE / DBDG | catálogo nacional y armonización de geoinformación | creada por Decreto 6.666/2008 y actualizada por Decreto 12.402/2025; el marco contempla almacenamiento, acceso, intercambio y difusión de datos geoespaciales | auditar endpoint, licencia y fecha de cada recurso del productor |
| AMARILLO | IBGE | límites, población, cartografía, relieve, hidrografía y exposición | autoridad estadística y geográfica; coautor del Perfil de Metadatos Geoespaciales de Brasil compatible con ISO 19115-1 | localizar y probar productos individuales de descarga anónima y licencia compatible |
| AMARILLO | ICMBio | áreas protegidas, cavernas, áreas embargadas y conservación | WMS y WFS oficiales anónimos en INDE; descargas SHP publicadas | el sitio general usa CC BY-ND 3.0; verificar licencia específica de cada dataset y si permite derivados |
| AMARILLO | INPE | incendios, deforestación, cobertura y observación de la Tierra | organismo científico competente con productos operativos conocidos | comprobar licencia, descarga anónima, latencia y condiciones por producto antes de clasificar |
| AMARILLO | CEMADEN | alertas, precipitaciones, estaciones y riesgo hidrometeorológico | organismo federal competente para monitoreo y alertas | verificar APIs o descargas anónimas, histórico, licencia y estabilidad |
| AMARILLO | ANA | hidrología, cuencas, estaciones y recursos hídricos | autoridad nacional del agua | auditar servicios y licencia por dataset |
| AMARILLO | SGB / CPRM | geología, hidrogeología, movimientos en masa y peligros | servicio geológico federal | auditar endpoints, escalas, métodos y licencia por producto |

## 6. Auditoría de Ecuador

| Estado | Organismo / producto | Temas relevantes | Evidencia comprobada | Clasificación prudente |
|---|---|---|---|---|
| VERDE-DATO CONDICIONAL | IGM — Cartografía Base Continua 1:1.000.000, edición 2024 | límites, red vial, hidrografía, asentamientos y cartografía base | publicación oficial de libre acceso; GPKG, SHP, metadatos y geoservicios WMS/WFS/WMTS declarados | conservar como condicional hasta documentar texto completo de licencia y probar descarga anónima del archivo exacto |
| AMARILLO | IGM — cartografía 1:50.000 y 1:250.000 histórica | cartografía base y análisis territorial | SHP, metadatos y geoservicios públicos; ediciones visibles de 2013 | antigüedad significativa; verificar cobertura, licencia y pertinencia operativa |
| ROJO PARA EL NÚCLEO | Proyecto Nacional de geoinformación 1:25.000 | suelos, geomorfología, clima, hidrología, producción, vulnerabilidad y riesgos | productos bajo CC BY-NC 4.0 | cláusula no comercial incompatible con la política general del núcleo |
| ROJO PARA EL NÚCLEO | Descargas GNSS sujetas a registro | geodesia y posicionamiento | exige creación de cuenta, aceptación individual y declara uso exclusivo, intransferible y sin fines de lucro | no cumple acceso anónimo ni reutilización amplia |
| AMARILLO | Redes gravimétricas liberadas | geodesia, modelos de elevación y referencia | licencia publicada permite uso, transformación, redistribución y explotación comercial con atribución | el portal visible utiliza formulario de registro; comprobar si existe descarga verdaderamente anónima |
| AMARILLO | IEDG / directorio de geoservicios nacionales | múltiples sectores oficiales | lista WMS, WFS, WMTS y TMS de instituciones, incluyendo escalas cartográficas y DTM de 40 m | auditar productor, licencia, vigencia y respuesta de cada endpoint |

## 7. Auditoría de Bolivia

| Estado | Organismo / fuente | Temas relevantes | Evidencia comprobada | Próxima verificación |
|---|---|---|---|---|
| VERDE-PORTAL | IDE-EPB / GeoBolivia | catálogo nacional multisectorial | plataforma oficial de Vicepresidencia; declara datos abiertos, capas base descargables, catálogo con metadatos, geovisor y WMS | comprobar licencia y descarga anónima por cada capa |
| AMARILLO | SERGEOMIN IDE | geología, minería, hidrogeología y peligros geológicos | geoportal oficial con servicios OGC, WMS, metadatos y sistema hidrogeológico | probar endpoints, escala, actualización, licencia y posibilidad de derivados |
| AMARILLO | Geoportal de Electricidad y Energías Renovables | centrales, generación e infraestructura energética | GeoNode público con cientos de capas y descargas en formatos estándar declaradas | revisar sensibilidad, licencia, fecha y acceso de cada capa |
| AMARILLO | ABT mediante IDE-EPB | desmontes, plantaciones forestales y cobertura | IDE-EPB informa actualización de capas a 2024 | localizar dataset, metodología, licencia y descarga directa |
| AMARILLO | unidades hidrográficas del MMAyA | cuencas y gestión hídrica | actualización comunicada en IDE-EPB | comprobar versión, geometría, resolución y licencia |

## 8. Auditoría de Paraguay

| Estado | Organismo / fuente | Temas relevantes | Evidencia comprobada | Próxima verificación |
|---|---|---|---|---|
| VERDE-PORTAL | Geoportal MITIC | catálogo gubernamental, mapas, documentos y geoservicios | GeoNode público; documentación técnica describe WMS, WFS, WCS y CSW sin requerir credenciales para consulta | identificar autoridad productora, licencia, fecha y descarga de cada dataset |
| AMARILLO | Portal de Datos Abiertos Gubernamentales | datos administrativos, sociales y territoriales | reconocido por el portal oficial de Gobierno Electrónico | auditar datasets geográficos útiles para riesgo, licencia y formatos |
| AMARILLO | INE Paraguay | población, hogares y exposición | autoridad estadística nacional | localizar cartografía censal, licencia, año, escala y descarga anónima |
| AMARILLO | MADES | ambiente, áreas protegidas, agua y biodiversidad | autoridad ambiental competente | verificar geoservicios y licencias de productos concretos |
| AMARILLO | INFONA | bosques, cobertura, incendios y uso forestal | autoridad forestal competente | verificar acceso, metodología, periodicidad y licencia |
| AMARILLO | DINAC / meteorología | observaciones, pronósticos, tormentas y aviación | organismo competente | comprobar fuentes estructuradas, histórico, licencia y automatización permitida |

## 9. Reglas para no sobreafirmar

1. Un **WMS** prueba visualización pública, pero no necesariamente permite descargar o redistribuir datos vectoriales.
2. Un **WFS/WCS** prueba acceso técnico a entidades o coberturas, pero no reemplaza la licencia.
3. Un portal gubernamental no vuelve automáticamente oficial a todos los recursos de terceros que indexa.
4. La palabra “gratuito” no equivale por sí sola a licencia abierta.
5. Una capa sin fecha, escala, metodología o responsable no puede alimentar decisiones críticas.
6. Una fuente regional o global no debe reemplazar una fuente nacional o local más competente.
7. Ninguna fuente se clasifica como VERDE-DATO hasta completar la prueba anónima desde una sesión sin credenciales.
8. Una licencia **no comercial**, **sin derivados**, de uso exclusivo o intransferible impide la admisión al núcleo, aunque el archivo pueda descargarse sin costo.
9. La licencia del sitio web no debe confundirse con la licencia del dataset.

## 10. Prueba mínima por dataset

Para promover un recurso de AMARILLO a VERDE-DATO se debe conservar evidencia de:

- URL oficial del producto;
- URL directa del endpoint o archivo;
- respuesta anónima satisfactoria;
- fecha y hora de verificación;
- licencia y atribución;
- organismo productor;
- formato y protocolo;
- sistema de referencia espacial;
- cobertura y resolución;
- fecha o versión del dato;
- variables y unidades;
- metodología y controles de calidad;
- limitaciones;
- decisión concreta que puede apoyar;
- fuente alternativa.

## 11. Fuentes oficiales consultadas en esta ronda

- Brasil, Presidencia de la República: Decreto 6.666/2008 y Decreto 12.402/2025 sobre INDE.
- Brasil, IBGE: Perfil de Metadatos Geoespaciales de Brasil, versión 2.0.
- Brasil, ICMBio: datos geoespaciales, descargas SHP y geoservicios WMS/WFS alojados en INDE.
- Ecuador, IGM: Geoportal, geoservicios, cartografía de libre acceso, licencias de descargas y Proyecto Nacional 1:25.000.
- Ecuador, Presidencia: directorio IEDG de geoservicios WMS, WFS, WMTS y TMS.
- Bolivia, Vicepresidencia: IDE-EPB / GeoBolivia, catálogo, documentación y anuncios institucionales.
- Bolivia, SERGEOMIN y Viceministerio de Electricidad: geoportales sectoriales.
- Paraguay, MITIC: Geoportal, documentación para desarrolladores y Portal de Gobierno Electrónico.

## 12. Próximas jurisdicciones de auditoría

La siguiente ronda debe cubrir, sin promover recursos sin evidencia:

- Centroamérica: Guatemala, Belice, Honduras, El Salvador, Nicaragua, Costa Rica y Panamá;
- Caribe: República Dominicana, Cuba, Haití, Jamaica, Puerto Rico y Estados insulares;
- norte de Sudamérica: Venezuela, Guyana, Surinam y Guayana Francesa;
- redes regionales: CEPREDENAC, GEOSUR, SIRGAS, UN-GGIM Américas, CIIFEN y plataformas regionales de alerta;
- auditoría sectorial profunda: servicios meteorológicos, hidrológicos, geológicos, sísmicos, volcánicos, forestales y de protección civil de cada país.

Estas jurisdicciones permanecen pendientes hasta completar la misma auditoría jurídica, técnica, científica y operativa.