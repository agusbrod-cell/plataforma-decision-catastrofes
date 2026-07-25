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

## 5. Reglas para no sobreafirmar

1. Un **WMS** prueba visualización pública, pero no necesariamente permite descargar o redistribuir datos vectoriales.
2. Un **WFS/WCS** prueba acceso técnico a entidades o coberturas, pero no reemplaza la licencia.
3. Un portal gubernamental no vuelve automáticamente oficial a todos los recursos de terceros que indexa.
4. La palabra “gratuito” no equivale por sí sola a licencia abierta.
5. Una capa sin fecha, escala, metodología o responsable no puede alimentar decisiones críticas.
6. Una fuente regional o global no debe reemplazar una fuente nacional o local más competente.
7. Ninguna fuente se clasifica como VERDE-DATO hasta completar la prueba anónima desde una sesión sin credenciales.

## 6. Prueba mínima por dataset

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

## 7. Próximas jurisdicciones de auditoría

La siguiente ronda debe cubrir, sin promover recursos sin evidencia:

- Brasil: INDE, IBGE, INPE, CEMADEN, ANA, SGB/CPRM y MapBiomas;
- Ecuador: IGM, SNGRE, INAMHI, IIGE y geoportales ambientales;
- Bolivia: IDE-EPB, IGM, SENAMHI, SERGEOMIN y ABT;
- Paraguay: IDE Paraguay, INE, MADES, INFONA y DINAC;
- Centroamérica y Caribe: IDE nacionales, CEPREDENAC, CATHALAC, institutos meteorológicos, geológicos e hidrológicos;
- redes regionales: GEOSUR, SIRGAS, UN-GGIM Américas y plataformas de cooperación para riesgo.

Estas jurisdicciones permanecen pendientes hasta completar la misma auditoría jurídica, técnica, científica y operativa.