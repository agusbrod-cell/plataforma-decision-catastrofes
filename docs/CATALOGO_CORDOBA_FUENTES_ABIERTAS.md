# Catálogo de fuentes abiertas para gestión de catástrofes en Córdoba

**Proyecto:** Plataforma de apoyo a decisiones públicas ante catástrofes  
**Jurisdicción prioritaria:** Provincia de Córdoba, Argentina  
**Revisión:** 25 de julio de 2026  
**Estado:** auditoría exhaustiva en curso; primera consolidación verificada

## 1. Objetivo

Este documento concentra la auditoría provincial prioritaria. Su propósito no es reunir enlaces, sino identificar recursos que puedan sostener decisiones reproducibles ante incendios, inundaciones, sequías, tormentas, movimientos en masa, emergencias ambientales y fallas de servicios esenciales.

La aspiración de cobertura completa se implementa mediante una matriz cerrable: cada organismo y dominio debe quedar en uno de estos estados:

- **VERDE-PORTAL:** infraestructura oficial y accesible anónimamente; cada capa conserva evaluación individual.
- **VERDE-DATO:** producto individual con acceso anónimo, licencia o régimen abierto inequívoco, metadatos, fecha, método y funcionamiento verificados.
- **AMARILLO:** recurso relevante al que le falta demostrar al menos una condición.
- **ROJO:** requiere credenciales, convenio, pago o tiene licencia incompatible, datos sensibles o restricciones de reutilización.
- **NO LOCALIZADO:** organismo o dominio auditado sin recurso público estructurado encontrado; no equivale a inexistencia.

Ningún recurso se considera apto para una decisión crítica solamente por estar publicado en un visor.

## 2. Infraestructura geoespacial provincial

| Estado | Fuente | Autoridad | Evidencia verificada | Utilidad | Control pendiente |
|---|---|---|---|---|---|
| VERDE-PORTAL | Mapas Córdoba / IDECOR | Gobierno de la Provincia de Córdoba | geoportal público; WMS, WFS y WCS; descargas; metadatos compatibles con recomendaciones de IDERA | infraestructura transversal para cartografía, ambiente, riesgo, agua, catastro, agro, ciudades e infraestructura | auditar licencia, fecha, escala, linaje y autoridad de cada capa |
| VERDE-DATO CONDICIONAL | Endpoint WFS IDECOR | IDECOR | endpoint documentado públicamente: `https://idecor-ws.mapascordoba.gob.ar/geoserver/idecor/wfs`; permite consulta y descarga vectorial | automatización de conectores SIG | inventariar capas y conservar respuesta GetCapabilities, licencia y metadatos por capa |
| VERDE-PORTAL | Portal de Datos Abiertos de la Provincia | Gobierno de Córdoba | catálogo público por categorías | datos administrativos, territoriales, sanitarios, sociales y económicos | verificar licencia, formato, responsable y actualización por recurso |
| VERDE-PORTAL | Portal de Datos Abiertos y Portal de Mapas de la Municipalidad de Córdoba | Municipalidad de Córdoba | catálogo y mapas públicos de salud, catastro, barrios, escuelas, comisarías, espacios verdes, residuos, movilidad y servicios | exposición y capacidad de respuesta en la capital | no extrapolar a toda la provincia; auditar descarga y licencia por dataset |

### Evidencia institucional principal

- IDECOR documenta que sus recursos pueden consultarse, descargarse y consumirse mediante servicios OGC.
- En 2025 Mapas Córdoba informó 230 mapas y casi 1.000 geoservicios; la cantidad es dinámica y no debe usarse como inventario estable.
- El mapa base provincial identifica como productores competentes a Catastro, Vialidad Provincial y APRHI, e incorpora metadatos de fecha, escala, sistema de referencia, distribución y linaje.

## 3. Cartografía base, jurisdicciones y catastro

| Estado | Producto o familia | Productor | Variables principales | Decisiones que apoya | Observaciones |
|---|---|---|---|---|---|
| VERDE-DATO CONDICIONAL | Mapa Base Córdoba | Catastro, Vialidad Provincial, APRHI e IDECOR | límite provincial, departamentos, pedanías, localidades, áreas urbanas, radios municipales, red vial, embalses, cuerpos y cursos de agua | referencia territorial, accesibilidad, jurisdicción y exposición | verificar versión y metadatos de cada capa antes del conector |
| VERDE-DATO CONDICIONAL | Radios municipales y límites de localidades | Catastro / IDECOR | jurisdicciones y áreas de competencia local | coordinación municipal y asignación territorial | conservar fecha y norma o autoridad de delimitación |
| VERDE-DATO CONDICIONAL | Parcelario y estructura catastral pública | Dirección General de Catastro / IDECOR | parcelas, manzanas, nomenclatura y estructura territorial | exposición física y planificación | excluir titulares, domicilios personales y atributos protegidos |
| AMARILLO | Catastro de la Ciudad de Córdoba | Municipalidad de Córdoba | datos catastrales urbanos | análisis urbano de la capital | el portal declara publicación y actualización en 2017; verificar recurso actual, licencia y vigencia real |
| AMARILLO | Planeamiento urbano, barrios y límites administrativos de la capital | Municipalidad de Córdoba | barrios, zonificación y estructura urbana | evacuación, exposición y logística | auditar cada versión descargable |

## 4. Incendios forestales y rurales

Este es el dominio provincial con mayor madurez pública localizada hasta ahora.

| Estado | Producto | Autoridad y participantes | Frecuencia / período | Acceso comprobado | Uso correcto y limitaciones |
|---|---|---|---|---|---|
| VERDE-DATO CONDICIONAL | Áreas afectadas por incendios 2021–2026 | Dirección de Gestión de Riesgos, Gestión Integral de Manejo del Fuego e IDECOR; mesa técnica interinstitucional | series anuales; 2025 y 2026 con actualizaciones durante el año | mapas, descargas y geoservicios OGC declarados; polígonos y atributos | perímetro postevento; no equivale a foco activo ni a estado operativo del incendio |
| VERDE-DATO CONDICIONAL | Índice Meteorológico de Peligro de Incendios — FWI | SGRCCyPC, OHMC e IDECOR | diario | mapa público provincial | índice meteorológico; debe conservar hora, corrida, método y vigencia |
| VERDE-DATO CONDICIONAL | Código de Humedad del Combustible Fino — FFMC | SGRCCyPC, OHMC e IDECOR | diario | mapa público provincial | componente del sistema FWI; no es medición directa de humedad en campo |
| VERDE-DATO CONDICIONAL | Índice de Propagación Inicial — ISI | SGRCCyPC, OHMC e IDECOR | diario | mapa público provincial | indicador de comportamiento potencial; no reemplaza observación operativa |
| VERDE-DATO CONDICIONAL | Riesgo local ante incendios forestales | Dirección de Gestión de Riesgos / IDECOR | producto territorial | descarga y geoservicios declarados | integra amenaza, vulnerabilidad y riesgo; registrar metodología y alcance espacial |
| VERDE-DATO CONDICIONAL | Cuarteles y jurisdicciones de Bomberos Voluntarios | SGRCCyPC / IDECOR | inventario territorial | mapa público | ubicación y jurisdicción no prueban dotación, disponibilidad ni capacidad operativa actual |
| AMARILLO | Recursos operativos de combate, ETAC, móviles, personal y disponibilidad | organismos de respuesta | tiempo real o casi real | no localizado como dataset abierto estructurado | información potencialmente sensible; integrar solo agregada y con evaluación de seguridad |

### Atributos confirmados en los mapas de áreas quemadas

Los productos anuales informan, según edición:

- extensión en hectáreas;
- fecha de ocurrencia o detección;
- departamento;
- jurisdicción de Bomberos Voluntarios;
- cuenca hídrica;
- localidad próxima y sitio de referencia;
- coordenadas centrales;
- pendiente, altitud y orientación;
- zona de riesgo establecida por la Ley Provincial 8.751;
- grilla de referencia del Plan Nacional de Manejo del Fuego;
- coberturas y usos del suelo afectados.

## 5. Riesgo local, inundaciones y peligros geomorfológicos

| Estado | Producto localizado | Productor | Cobertura | Utilidad | Pendiente |
|---|---|---|---|---|---|
| VERDE-DATO CONDICIONAL | Riesgo de inundación de Villa Allende | SGRCCyPC, municipio e IDECOR | local | amenaza, vulnerabilidad y riesgo | verificar edición, informe técnico y geoservicios actuales |
| VERDE-DATO CONDICIONAL | Riesgo por inundación de Unquillo | Municipalidad de Unquillo / IDECOR | local | planificación y prevención | auditar metodología, fecha y escala |
| VERDE-DATO CONDICIONAL | Peligrosidad geomorfológica de Villa Carlos Paz | Municipalidad de Villa Carlos Paz / IDECOR | local | movimientos en masa, erosión y ordenamiento | verificar clases, metodología y vigencia |
| VERDE-DATO CONDICIONAL | Plan de Manejo Contra el Fuego Regional de Anisacate | Municipalidad de Anisacate / IDECOR | regional/local | prevención, coordinación y recursos territoriales | distinguir cartografía pública de información operativa sensible |
| AMARILLO | Mapa provincial continuo de amenaza de inundación | organismos provinciales | provincial | planificación y alerta | no se confirmó todavía un producto único con cobertura provincial completa |
| AMARILLO | Susceptibilidad provincial a movimientos en masa | SEGEMAR, provincia, academia | provincial | prevención y ordenamiento | localizar producto oficial, escala, licencia y descarga |

Los productos locales no deben extrapolarse fuera de su ámbito metodológico.

## 6. Hidrología, cuencas y recursos hídricos

| Estado | Fuente / producto | Autoridad | Evidencia | Uso | Pendiente |
|---|---|---|---|---|---|
| VERDE-DATO CONDICIONAL | Cuencas hídricas, embalses, cuerpos y cursos de agua publicados en Mapas Córdoba | APRHI / IDECOR | incluidos en mapa base y productos temáticos con geoservicios | modelación preliminar, referencia hidrográfica y exposición | verificar escala, fecha, topología y linaje |
| VERDE-PORTAL | APRHI como productor provincial | Administración Provincial de Recursos Hídricos | autoridad temática identificada en metadatos y productos IDECOR | agua superficial, subterránea, obras y cuencas | catalogar todos los datasets públicos fuera y dentro de IDECOR |
| AMARILLO | Series de estaciones hidrológicas, niveles, caudales, precipitaciones y embalses | APRHI / OHMC | se confirma participación institucional, pero no se cerró auditoría de descargas estructuradas | alerta y modelación | comprobar histórico, API/archivo, unidades, control de calidad, latencia y licencia |
| AMARILLO | Pozos, perforaciones, acuíferos y calidad de agua | APRHI y otros organismos | publicación variable | sequía, abastecimiento y riesgo sanitario | evaluar sensibilidad, cobertura y licencia |

## 7. Meteorología y observación hidrometeorológica

| Estado | Fuente | Variables | Utilidad | Clasificación prudente |
|---|---|---|---|---|
| VERDE-DATO CONDICIONAL | Mapas diarios FWI, FFMC e ISI | índices derivados de condiciones meteorológicas | incendios | acceso público confirmado; falta cerrar endpoint, licencia y archivo histórico |
| AMARILLO | Observatorio Hidro-Meteorológico de Córdoba — OHMC | precipitación, temperatura, humedad, viento y productos derivados | tormentas, inundaciones, sequías e incendios | autoridad y participación confirmadas; auditar estaciones, datos crudos, histórico y licencia |
| AMARILLO | Estaciones SMN en Córdoba | observaciones, alertas y pronósticos | referencia meteorológica nacional | se auditarán dentro del catálogo argentino y luego se filtrarán espacialmente para Córdoba |
| AMARILLO | Estaciones INTA de la provincia | agroclima, precipitación y suelo | sequía, incendios y producción | localizar productos individuales, acceso anónimo y licencia |
| AMARILLO | Redes universitarias y municipales | variables locales | densificación territorial | no usar como evidencia única sin calibración, documentación y continuidad |

## 8. Ambiente, bosques, cobertura y biodiversidad

| Estado | Producto / familia | Autoridad | Utilidad | Control requerido |
|---|---|---|---|---|
| VERDE-DATO CONDICIONAL | Áreas Naturales Protegidas y Regiones Naturales | Ministerio de Ambiente y Economía Circular / IDECOR | exposición ambiental, prioridades de protección y recuperación | versión, norma, escala y metadatos |
| VERDE-DATO CONDICIONAL | Cobertura y Uso del Suelo provincial | IDECOR y organismos técnicos participantes | combustible, erosión, infiltración, exposición y evaluación de daños | edición 2020–2021 o 2022–2023 según producto; no mezclar años |
| AMARILLO | Ordenamiento Territorial de Bosques Nativos | autoridad ambiental provincial | restricción de usos, valores de conservación e incendios | verificar capa vigente, ley asociada, descarga y atributos |
| AMARILLO | Bosques nativos, inventarios forestales y restauración | autoridad ambiental / INTA / academia | prevención y recuperación | catalogar series y metodologías |
| AMARILLO | Humedales, flora, fauna y biodiversidad | autoridad ambiental, universidades y CONICET | impacto ecológico y priorización | comprobar datos abiertos individuales y sensibilidad de especies |
| AMARILLO | Policía Ambiental: actuaciones, infracciones o sitios degradados agregados | Policía Ambiental | riesgos secundarios y cumplimiento | publicar solo datos anonimizados y jurídicamente reutilizables |

## 9. Relieve, suelos y geología

| Estado | Fuente / producto | Productor | Utilidad | Pendiente |
|---|---|---|---|---|
| VERDE-DATO CONDICIONAL | Modelos de elevación y derivados publicados en Mapas Córdoba | IDECOR y productores identificados en metadatos | pendiente, orientación, cuencas, propagación y accesibilidad | resolución, fecha, correcciones y licencia por producto |
| VERDE-DATO CONDICIONAL | Mapas de suelos y capacidad de uso publicados | organismos provinciales, INTA e IDECOR | erosión, infiltración, producción y recuperación | edición, escala, clases y metodología |
| AMARILLO | Cartas geológicas, fallas y peligros geológicos de Córdoba | SEGEMAR | movimientos en masa, sismicidad y materiales | se auditarán en el catálogo nacional con recorte provincial |
| AMARILLO | Canteras y actividad minera | autoridad minera provincial / SEGEMAR | riesgo tecnológico, taludes y logística | evaluar actualización, sensibilidad y licencia |

## 10. Infraestructura, transporte y capacidad de respuesta

| Estado | Producto | Fuente | Utilidad | Advertencia |
|---|---|---|---|---|
| VERDE-DATO CONDICIONAL | Red vial provincial | Vialidad Provincial / IDECOR | evacuación, acceso y logística | geometría no informa transitabilidad actual |
| VERDE-DATO CONDICIONAL | Escuelas, centros educativos y edificios públicos publicados | Provincia, municipios e IDECOR | refugios potenciales y exposición | “edificio existente” no equivale a refugio habilitado |
| VERDE-DATO CONDICIONAL | Centros de salud y hospitales municipales de Córdoba Capital | Municipalidad de Córdoba | capacidad sanitaria urbana | versión 2024 localizada; verificar descarga, licencia y actualización |
| VERDE-DATO CONDICIONAL | Comisarías, subcomisarías y unidades judiciales de Córdoba Capital | Municipalidad de Córdoba | coordinación urbana | cobertura limitada a la capital y posible desactualización |
| VERDE-DATO CONDICIONAL | Centros operativos, CPC, parques educativos y puntos Wi-Fi de la capital | Municipalidad de Córdoba | coordinación, comunicación y apoyo comunitario | verificar aptitud real durante emergencias |
| AMARILLO | Hospitales y CAPS provinciales | Ministerio de Salud / IDECOR / datos provinciales | respuesta sanitaria | construir inventario provincial completo con especialidad, nivel y vigencia |
| AMARILLO | Puentes, alcantarillas y obras viales | Vialidad / Infraestructura | vulnerabilidad de rutas | localizar dataset abierto y fecha de inspección; evitar inferir condición estructural |
| AMARILLO | Aeródromos, helipuertos y pistas | organismos aeronáuticos / provincia | logística aérea | auditar autoridad, operatividad y restricciones |
| AMARILLO | Refugios y centros de evacuación habilitados | Defensa Civil y municipios | evacuación | dato temporal; exigir fecha de validación y responsable |

## 11. Servicios críticos y riesgos tecnológicos

| Estado | Dominio | Productores candidatos | Regla |
|---|---|---|---|
| AMARILLO | energía eléctrica | EPEC, cooperativas, ente regulador e IDECOR | integrar infraestructura pública no sensible; estado operativo requiere fuente temporal oficial |
| AMARILLO | gas | distribuidoras y organismos reguladores | generalizar infraestructura sensible y revisar licencia |
| AMARILLO | agua y saneamiento | prestadores, municipios y APRHI | separar redes públicas, plantas, captaciones y calidad; aplicar evaluación de seguridad |
| AMARILLO | telecomunicaciones | organismos nacionales, prestadores y municipios | cobertura declarada no prueba disponibilidad durante un evento |
| AMARILLO | industrias peligrosas, depósitos y sustancias | autoridades ambientales, laborales y municipales | no publicar detalles que aumenten riesgo; usar categorías y niveles de exposición cuando corresponda |
| ROJO | planos detallados, controles, credenciales o vulnerabilidades de infraestructura crítica | cualquier productor | fuera del núcleo abierto |

## 12. Población, salud y vulnerabilidad social

| Estado | Fuente | Utilidad | Pendiente |
|---|---|---|---|
| VERDE-PORTAL | Datos Abiertos provinciales y municipales | salud, educación, población, sociedad y administración | auditar recursos individuales |
| AMARILLO | Cartografía censal y Censo 2022 filtrados para Córdoba | INDEC | exposición y vulnerabilidad | se aprobarán dentro del catálogo nacional y se generará recorte reproducible |
| AMARILLO | Estadísticas sanitarias agregadas | Ministerio de Salud provincial | vulnerabilidad y demanda | licencia, periodicidad, unidad geográfica y anonimización |
| ROJO | domicilios o condiciones individuales de personas vulnerables y pacientes | cualquier organismo | fuera del núcleo abierto |

## 13. Municipios y comunas

La cobertura provincial al 100 % exige auditar los gobiernos locales, pero no es correcto asumir que todos poseen portales abiertos.

Para cada municipio o comuna se registrará:

1. portal oficial;
2. portal de datos o geoportal;
3. límites y barrios;
4. calles y caminos;
5. centros de evacuación;
6. salud y educación;
7. bomberos y seguridad;
8. agua, saneamiento y residuos;
9. planes de riesgo y ordenamiento;
10. datasets descargables, licencia, fecha y responsable.

Los mapas municipales ya indexados en IDECOR son candidatos prioritarios porque permiten localizar productos de Unquillo, Río Ceballos, Villa Allende, La Granja, Anisacate y Villa Carlos Paz, entre otros. Cada uno debe auditarse como producto local, sin extrapolarlo al resto de Córdoba.

## 14. Universidades, CONICET e instituciones científico-técnicas

| Estado | Productor candidato | Dominios | Próxima acción |
|---|---|---|---|
| AMARILLO | Universidad Nacional de Córdoba | geografía, geología, ambiente, clima, salud, urbanismo y sensores remotos | localizar repositorios de datos, anexos de investigación, geoportales y licencias |
| AMARILLO | Instituto Gulich — CONAE/UNC | observación de la Tierra, incendios, agua y riesgo | auditar productos de descarga anónima distintos de plataformas autenticadas |
| AMARILLO | CONICET Córdoba | biodiversidad, ecología, hidrología, geología y vulnerabilidad | buscar datasets en repositorios institucionales con DOI y licencia abierta |
| AMARILLO | INTA Centro Regional Córdoba y estaciones experimentales | suelos, cultivos, clima, cobertura e incendios | inventariar Manfredi, Marcos Juárez y otros nodos relevantes |
| AMARILLO | INA-CIRSA | hidrología regional, calidad de agua y modelación | auditar series, mapas, informes y datos descargables |

Un artículo científico abierto no convierte automáticamente sus datos subyacentes en abiertos. Solo se incorporarán datasets con archivo, licencia y metadatos propios.

## 15. Brechas críticas identificadas

Todavía no puede afirmarse cobertura provincial completa. Las brechas prioritarias son:

- series hidrometeorológicas crudas e históricas de APRHI/OHMC;
- cartografía provincial continua de inundaciones;
- inventario provincial actualizado de hospitales, CAPS y capacidades sanitarias;
- puentes, obras de drenaje y transitabilidad en tiempo real;
- refugios habilitados y centros de evacuación con vigencia;
- infraestructura eléctrica, agua, saneamiento y telecomunicaciones bajo criterios de seguridad;
- incendios activos y recursos operativos estructurados sin credenciales;
- riesgos tecnológicos e industrias peligrosas en forma agregada y segura;
- datasets abiertos de universidades, CONICET, INTA e INA-CIRSA;
- auditoría sistemática de los 427 gobiernos locales reconocidos por la provincia, usando el padrón oficial vigente como universo de control.

## 16. Criterio de cierre de Córdoba

Córdoba podrá marcarse como **cobertura exhaustiva v1.0** solamente cuando:

- todos los organismos provinciales con competencia material hayan sido auditados;
- todos los dominios críticos tengan al menos una fuente primaria o conste formalmente la brecha;
- los municipios y comunas estén inventariados mediante un universo oficial y un estado explícito;
- cada recurso verde tenga evidencia reproducible;
- los enlaces y endpoints sean comprobados automáticamente;
- exista fecha de última verificación;
- las fuentes amarillas y rojas estén justificadas;
- una revisión humana independiente no encuentre categorías institucionales omitidas.

La expresión “100 %” significará **100 % del universo y de la matriz de control definidos**, no conocimiento absoluto de todo archivo existente.

## 17. Fuentes oficiales consultadas en esta consolidación

- IDECOR, Mapas Córdoba y documentación de geoservicios WFS/WCS.
- IDECOR, Mapa Base Córdoba.
- IDECOR y Mesa Técnica de Áreas Afectadas por Incendios Forestales y Rurales.
- IDECOR, mapas de riesgo y desastres naturales.
- Gobierno de la Provincia de Córdoba, portales y organismos productores identificados en metadatos.
- Municipalidad de Córdoba, Portal de Datos Abiertos y Portal de Mapas.

## 18. Próxima auditoría provincial

La siguiente incorporación debe cerrar tres bloques antes de ampliar Argentina:

1. **agua y meteorología:** APRHI, OHMC, INA-CIRSA, SMN e INTA;
2. **ambiente y territorio:** bosques nativos, áreas protegidas, biodiversidad, suelos, geología y ordenamiento;
3. **respuesta y exposición:** salud, bomberos, rutas, puentes, refugios, energía, agua, saneamiento y municipios.
