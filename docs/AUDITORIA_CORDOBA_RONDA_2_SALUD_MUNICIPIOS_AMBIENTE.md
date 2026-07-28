# Auditoría Córdoba — ronda 2: salud, municipios, ambiente e infraestructura abierta

**Proyecto:** Plataforma de apoyo a decisiones públicas ante catástrofes  
**Jurisdicción:** Provincia de Córdoba, Argentina  
**Fecha de verificación:** 25 de julio de 2026  
**Estado:** consolidación auditada; pendiente validación automática de endpoints y licencias por capa

## 1. Alcance

Esta ronda profundiza cuatro dominios prioritarios del catálogo provincial:

1. salud pública y capacidad territorial;
2. municipios, comunas y normativas urbanas;
3. ambiente, áreas protegidas e infraestructura verde;
4. madurez y alcance real de IDECOR como repositorio de datos abiertos.

La inclusión de una fuente no implica que sus datos representen capacidad operativa en tiempo real. Ubicación, existencia física y jurisdicción deben distinguirse de disponibilidad, dotación, estado estructural o aptitud durante una emergencia.

## 2. Madurez de Mapas Córdoba / IDECOR

| Estado | Evidencia verificada | Resultado para el catálogo | Limitación |
|---|---|---|---|
| VERDE-PORTAL | Mapas Córdoba se identifica como el geoportal oficial de la IDE provincial y declara consulta, descarga y consumo mediante geoservicios | se consolida como infraestructura principal de descubrimiento y distribución provincial | cada capa conserva evaluación individual de licencia, fecha, escala, linaje y productor |
| VERDE-PORTAL | IDECOR informó en octubre de 2025 más de 460 capas de datos abiertos agrupadas en 15 ejes temáticos | el universo de auditoría debe partir del inventario de capas, no solamente de los mapas visibles | la cifra es dinámica y debe capturarse mediante inventario versionado |
| VERDE-PORTAL | En enero de 2026 se informaron 230 mapas y casi 1.000 geoservicios | confirma alta madurez técnica e interoperabilidad | cantidad de servicios no equivale a cantidad de datasets únicos ni vigentes |
| VERDE-DATO CONDICIONAL | Endpoint WFS general documentado por IDECOR | permite diseñar cosecha automatizada de GetCapabilities y capas | promover capa por capa después de conservar licencia, metadatos y prueba anónima |

### Decisión técnica

Se debe crear un inventario automático y versionado de `GetCapabilities` para WFS, WMS y WCS. Cada capa deberá registrar como mínimo:

- nombre técnico;
- título;
- resumen;
- productor;
- sistema de referencia;
- cobertura espacial;
- formatos;
- fecha de cosecha;
- metadatos asociados;
- licencia o régimen de uso;
- estado de respuesta;
- dominio de riesgo;
- última revisión humana.

## 3. Salud pública provincial

| Estado | Producto | Productor | Evidencia comprobada | Utilidad | Limitación operativa |
|---|---|---|---|---|---|
| VERDE-DATO CONDICIONAL | Mapa de Centros de Salud Públicos de Córdoba | Ministerio de Salud de Córdoba / DGIS e IDECOR | cobertura de todo el territorio provincial; descarga en distintos formatos; geoservicios; metadatos; publicación declarada como datos abiertos | accesibilidad sanitaria, exposición, planificación territorial y proximidad de atención | la edición original localizada es de 2020; debe comprobarse actualización y vigencia por establecimiento |
| VERDE-DATO CONDICIONAL | Red de 833 centros identificada en la publicación inicial | Ministerio de Salud / IDECOR | 2 centros nacionales, 57 provinciales y 774 municipales en la edición publicada | inventario base para respuesta sanitaria | el número no debe presentarse como cifra actual sin verificar la versión vigente |
| AMARILLO | Nivel de complejidad, guardias, camas, especialidades, ambulancias y disponibilidad | Ministerio de Salud y efectores | no se confirmó como dataset abierto provincial integrado | derivación, evacuación y capacidad real | dato dinámico; exige fuente operativa oficial, fecha y controles de seguridad |
| ROJO | datos nominales de pacientes o domicilios vinculados con condiciones sanitarias | cualquier productor | información personal sensible | ninguno para el núcleo abierto | exclusión obligatoria |

### Corrección del catálogo principal

La entrada genérica “Hospitales y CAPS provinciales — AMARILLO” debe dividirse:

- **ubicación e identificación de centros públicos:** VERDE-DATO CONDICIONAL;
- **capacidad y disponibilidad operativa:** AMARILLO;
- **datos personales sanitarios:** ROJO.

## 4. Bomberos y capacidad de respuesta

| Estado | Producto | Evidencia | Uso correcto | Advertencia |
|---|---|---|---|---|
| VERDE-DATO CONDICIONAL | Cuarteles y jurisdicciones de Bomberos Voluntarios | IDECOR declara consulta, descarga y geoservicios en diversos formatos; la publicación fue presentada expresamente como datos abiertos | cobertura territorial, asignación jurisdiccional y planificación de proximidad | no informa dotación, personal disponible, móviles, agua, combustible ni capacidad actual |
| AMARILLO | ETAC, móviles, brigadas, personal y recursos operativos | no localizado como dataset abierto estructurado y estable | coordinación operativa | información dinámica y potencialmente sensible |

## 5. Municipios, comunas e IDECOR Ciudades

### 5.1 Universo provincial

Córdoba posee **427 localidades oficiales** en el universo cartográfico informado por Catastro e IDECOR. Los radios municipales y comunales pueden visualizarse, descargarse y consumirse mediante geoservicios OGC. Los atributos publicados incluyen nombre y nomenclatura oficial, legislación constitutiva, superficie y tipo de gobierno.

Esta capa se incorpora como **VERDE-DATO CONDICIONAL** y debe utilizarse como universo maestro para la auditoría de gobiernos locales.

### 5.2 Gobiernos locales con datos publicados

| Estado | Recurso | Evidencia vigente | Cobertura | Limitación |
|---|---|---|---|---|
| VERDE-PORTAL | IDECOR Ciudades | programa provincial para publicar datos territoriales locales abiertos e interoperables | en enero de 2026 se informaron 43 gobiernos locales y 97 mapas | la página institucional puede listar participantes adicionales; congelar el universo por fecha y no mezclar cifras de distintas ediciones |
| VERDE-DATO CONDICIONAL | Normativas urbanas | mapa abierto actualizado en junio de 2026 con datos de 42 localidades | uso, ocupación y fraccionamiento del suelo; edificación; urbanización; áreas ambientales, paisajísticas, de riesgo o preservación | no reemplaza el texto jurídico vigente de cada ordenanza |
| VERDE-DATO CONDICIONAL | Catastros, planeamiento, infraestructura y servicios locales | mapas abiertos publicados por localidades participantes | exposición urbana, redes, accesibilidad y ordenamiento | cobertura desigual entre municipios; auditar contenido y fecha de cada mapa |

### 5.3 Localidades identificadas por la página institucional

Se registran como participantes o con productos asociados:

Aldea Santa María, Alta Gracia, Anisacate, Arroyito, Bell Ville, Chilibroste, Colonia Caroya, Corralito, Córdoba, Cosquín, Elena, Embalse, Hernando, Huanchilla, Icho Cruz, Jesús María, Justiniano Posse, La Calera, La Falda, La Granja, Laguna Larga, Las Higueras, Las Varillas, Los Surgentes, Mayu Sumaj, Mina Clavero, Monte Buey, Morteros, Nono, Oncativo, Porteña, Río Ceballos, Río Cuarto, Salsipuedes, San Antonio de Arredondo, San Basilio, San Francisco, San Isidro–La Quintana, Santa Rosa de Calamuchita, Unquillo, Vicuña Mackenna, Villa Allende, Villa Carlos Paz, Villa de Las Rosas, Villa General Belgrano, Villa Giardino, Villa María y Villa Nueva.

La lista institucional no debe utilizarse como prueba de que todas las localidades mantienen hoy un mapa activo o la misma cantidad de productos. Cada localidad requiere ficha propia.

### 5.4 Matriz local obligatoria

Para alcanzar cobertura exhaustiva, los 427 gobiernos locales deben quedar con uno de estos estados:

- datos abiertos en IDECOR Ciudades;
- portal local abierto independiente;
- publicaciones no estructuradas;
- acceso restringido o licencia incompatible;
- sin dataset localizado;
- organismo pendiente de verificación.

## 6. Ambiente y áreas protegidas

| Estado | Producto | Productor | Evidencia comprobada | Uso | Control |
|---|---|---|---|---|---|
| VERDE-DATO CONDICIONAL | Áreas Naturales Protegidas y Regiones Naturales | Ministerio de Ambiente y Economía Circular / IDECOR | actualización publicada en septiembre de 2025; integra áreas nacionales, provinciales, municipales, Reservas Naturales de la Defensa, reservas arqueológicas y corredores biogeográficos | exposición ambiental, prioridades de protección, evaluación de daños y restauración | conservar instrumento de creación, superficie, fecha, límites y versión |
| VERDE-DATO CONDICIONAL | Regiones Naturales de Córdoba | autoridad ambiental / IDECOR | 19 unidades territoriales definidas mediante parámetros biofísicos y socioambientales | regionalización ambiental y priorización | no usar como sustituto de cobertura actual del suelo |
| AMARILLO | Ordenamiento Territorial de Bosques Nativos vigente | autoridad ambiental provincial | relevancia y autoridad confirmadas | incendios, restricciones de uso, conservación y restauración | localizar capa vigente, norma, fecha, categorías y licencia exacta |
| AMARILLO | inventarios de flora, fauna y especies sensibles | provincia, UNC, CONICET y otros | fuentes dispersas | impacto ecológico | generalizar o restringir localizaciones sensibles |

## 7. Municipalidad de Córdoba como nodo específico

| Estado | Fuente | Evidencia | Alcance | Limitación |
|---|---|---|---|---|
| VERDE-PORTAL | Portal de Gobierno Abierto de la Municipalidad | declara datos públicos en formatos abiertos para usar, transformar y compartir; registra cientos de conjuntos y recursos | ciudad de Córdoba | auditar licencia y vigencia por dataset |
| VERDE-PORTAL | Portal ambiental municipal e Instituto de Protección Ambiental y Animal | declara observatorio ambiental y trazabilidad de arbolado, espacios verdes, basurales, residuos y enterramiento | ambiente urbano, residuos, agua, suelo y aire | verificar qué variables están realmente publicadas en formato descargable y no solo descriptas |
| AMARILLO | Plataforma de Gestión Ambiental municipal | se declara integración con el sistema de datos abiertos | monitoreo y fiscalización | localizar endpoints, series históricas, licencia y periodicidad |

## 8. Brechas que permanecen abiertas

Esta ronda no permite cerrar todavía:

1. series crudas e históricas de APRHI y OHMC;
2. capacidad sanitaria operativa y actualizada;
3. puentes, alcantarillas, estado y transitabilidad de rutas;
4. refugios y centros de evacuación con fecha de habilitación;
5. infraestructura y estado operativo de energía, agua, saneamiento y telecomunicaciones;
6. Ordenamiento Territorial de Bosques Nativos vigente como dataset plenamente auditado;
7. cobertura de los 427 municipios y comunas;
8. datasets abiertos científicos de UNC, CONICET, INTA, Instituto Gulich e INA-CIRSA.

## 9. Próxima ronda obligatoria

La ronda 3 debe concentrarse en:

- APRHI y OHMC: estaciones, niveles, caudales, lluvia, embalses y calidad;
- Vialidad Provincial: rutas, puentes, alcantarillas, caminos y estado;
- ambiente: OTBN, bosque nativo, humedales, biodiversidad y sitios degradados;
- servicios críticos: EPEC, ERSeP, agua, saneamiento, gas y telecomunicaciones;
- ciencia abierta: UNC, CONICET Córdoba, INTA Córdoba, INA-CIRSA e Instituto Gulich.

## 10. Fuentes oficiales de esta ronda

- IDECOR, Mapas Córdoba y sección de descargas de la IDE provincial.
- IDECOR, Mapa de Centros de Salud Públicos.
- IDECOR, Cuarteles de Bomberos Voluntarios.
- IDECOR, IDECOR Ciudades y publicaciones institucionales 2024–2026.
- IDECOR y Dirección General de Catastro, límites oficiales de localidades.
- IDECOR y Ministerio de Ambiente y Economía Circular, Áreas Naturales Protegidas y Regiones Naturales.
- Municipalidad de Córdoba, Portal de Gobierno Abierto y portales ambientales oficiales.
