# POLÍTICA DE DATOS ABIERTOS

## Política de datos abiertos de la plataforma

**Estado:** política rectora inicial  
**Alcance:** núcleo funcional de la plataforma  
**Principio:** prioridad por datos abiertos

---

## 1. Propósito

La plataforma se construirá bajo una filosofía de prioridad por datos abiertos.

Toda funcionalidad esencial deberá apoyarse en fuentes de datos abiertas, oficiales, documentadas y públicamente accesibles, provenientes de organismos nacionales e internacionales.

La plataforma buscará que sus resultados puedan ser reproducidos, auditados y comprendidos por terceros sin depender de acuerdos privados, servicios comerciales, cuentas de usuario, claves, tokens ni credenciales institucionales.

Para este proyecto, un dato no se considerará verdaderamente abierto si su acceso operativo exige registrarse, autenticarse, solicitar autorización individual o gestionar una credencial, aunque el contenido sea gratuito o su licencia permita determinados usos.

---

## 2. Definición estricta de dato abierto

Una fuente se considerará abierta para el núcleo únicamente cuando cumpla simultáneamente:

- licencia abierta, explícita y compatible con reutilización, procesamiento, publicación de resultados derivados y atribución;
- acceso anónimo y directo, sin cuenta, token, clave, convenio, pago ni autorización individual;
- documentación pública del producto y de su mecanismo de acceso;
- posibilidad de que cualquier tercero reproduzca la consulta o descarga;
- formatos procesables o servicios interoperables;
- identificación clara de organismo, producto, versión, cobertura y fecha;
- ausencia de restricciones incompatibles sobre redistribución o generación de derivados.

**Gratuito no equivale a abierto.**  
**Públicamente visible no equivale a descargable.**  
**Licencia abierta no compensa un acceso cerrado.**

---

## 3. Principio de admisión

Una fuente podrá incorporarse al núcleo cuando cumpla los siguientes criterios:

- provenir de un organismo público, institución científica o iniciativa abierta reconocida;
- contar con una licencia abierta o términos inequívocamente compatibles con consulta, procesamiento, integración y reutilización pública;
- disponer de acceso anónimo y reproducible por terceros;
- ofrecer API pública sin autenticación, servicios OGC —WMS, WFS, WCS o WMTS—, descarga oficial directa u otro mecanismo abierto documentado;
- poseer metadatos suficientes para interpretar correctamente los datos;
- permitir identificar origen, fecha, versión, cobertura y transformaciones;
- contar con una estabilidad institucional razonable;
- permitir una atribución clara y verificable.

Ante dos fuentes técnicamente equivalentes, siempre se priorizará la alternativa abierta, oficial, documentada, anónima y reproducible.

---

## 4. Dependencias excluidas del núcleo

La plataforma no dependerá para su funcionamiento esencial de:

- convenios institucionales;
- credenciales privadas o públicas;
- cuentas de usuario obligatorias;
- registro previo obligatorio;
- claves de API;
- tokens de acceso, aunque sean gratuitos;
- aceptación individual de condiciones para descargar;
- servicios comerciales;
- datos con restricciones incompatibles con un proyecto abierto;
- información cuyo acceso no pueda ser reproducido anónimamente por terceros;
- datasets con términos ambiguos respecto del uso, procesamiento o redistribución;
- datos personales sensibles sin base legal, protección y gobernanza adecuadas.

Las fuentes que requieran autenticación, autorización, registro, licencias restrictivas o acceso cerrado no formarán parte del núcleo.

Podrán citarse como antecedentes científicos o alternativas externas, pero no se diseñarán conectores esenciales para ellas ni se presentarán como datos abiertos operativos de la plataforma.

---

## 5. Clasificación operativa

### Verde — núcleo abierto

Fuente con:

- licencia abierta explícita;
- acceso anónimo;
- documentación suficiente;
- mecanismo técnico público y reproducible;
- formatos procesables;
- atribución clara.

Ejemplos de acceso aceptable:

- API pública sin token;
- WMS, WFS, WCS o WMTS anónimo;
- descarga directa oficial en CSV, GeoJSON, GeoTIFF, NetCDF, KML o shapefile;
- catálogo STAC cuyos activos también sean descargables anónimamente;
- feed público documentado.

### Amarillo — candidato abierto pendiente de validación

Fuente que podría ser abierta, pero aún requiere verificar alguno de estos aspectos:

- licencia exacta del producto;
- descarga anónima real;
- estabilidad del enlace o servicio;
- documentación técnica;
- posibilidad de redistribuir derivados;
- calidad, resolución o vigencia.

Una fuente amarilla no puede convertirse en dependencia del núcleo hasta superar la validación.

### Rojo — fuera del núcleo

Fuente con:

- registro o cuenta obligatoria;
- token, clave o credencial;
- acceso cerrado;
- licencia restrictiva o no comercial;
- convenio obligatorio;
- términos de uso ambiguos;
- dependencia de un proveedor comercial;
- imposibilidad de reproducir el acceso de manera anónima;
- prohibición de redistribución o de generación de derivados compatibles con la plataforma.

---

## 6. Datos locales

Los municipios y organismos podrán cargar información propia, por ejemplo:

- infraestructura crítica;
- recursos y maquinaria;
- refugios y centros operativos;
- captaciones y redes de agua;
- caminos y accesos;
- inventarios de servicios;
- relevamientos de campo;
- observaciones técnicas verificadas.

Estos datos serán complementarios.

El núcleo de la plataforma deberá funcionar aun cuando una jurisdicción no disponga de información local propia.

La ausencia de datos locales deberá mostrarse como una limitación o brecha de información y nunca deberá ocultarse.

Los datos locales no se publicarán automáticamente como datos abiertos. Su apertura requerirá decisión del organismo responsable, licencia, evaluación de privacidad, seguridad y sensibilidad operativa.

---

## 7. Requisitos de registro de cada fuente

Toda fuente integrada deberá documentar, como mínimo:

- organismo responsable;
- nombre del portal, servicio o dataset;
- URL oficial;
- licencia o términos de uso;
- confirmación de acceso anónimo;
- cobertura territorial;
- cobertura temporal;
- variables disponibles;
- formato;
- modalidad de acceso;
- frecuencia de actualización;
- fecha de última verificación;
- limitaciones conocidas;
- clasificación operativa: verde, amarillo o rojo;
- uso previsto dentro de la plataforma;
- atribución requerida;
- transformaciones aplicadas;
- fuente alternativa, cuando exista.

---

## 8. Prueba obligatoria de apertura

Antes de aprobar una fuente como verde deberá comprobarse:

1. acceso desde una sesión anónima y sin credenciales almacenadas;
2. descarga o consulta exitosa mediante una URL o servicio documentado;
3. licencia visible y aplicable al producto concreto;
4. permiso de reutilización y generación de derivados;
5. disponibilidad de metadatos mínimos;
6. posibilidad de repetir la operación desde otro entorno;
7. ausencia de dependencia de cookies de sesión, claves temporales o aceptación personal.

La prueba deberá registrar fecha, endpoint, respuesta obtenida, formato, licencia y evidencia de acceso anónimo.

---

## 9. Regla de arquitectura

La indisponibilidad de una fuente nunca deberá bloquear toda la plataforma.

Cada conector deberá:

- manejar errores de red y cambios de esquema;
- registrar la última conexión exitosa;
- mostrar la fecha y vigencia del dato;
- impedir que datos vencidos parezcan actuales;
- informar el impacto de la ausencia de la fuente sobre la confianza del análisis;
- ofrecer fuentes abiertas alternativas cuando existan;
- conservar trazabilidad de las transformaciones;
- permitir desactivar el conector sin afectar el núcleo.

---

## 10. Prioridad geográfica

La selección de fuentes seguirá este orden general:

1. fuentes abiertas nacionales de Argentina;
2. fuentes abiertas provinciales o regionales;
3. fuentes abiertas internacionales;
4. datos locales cargados voluntariamente por cada jurisdicción.

Las fuentes internacionales complementarán la información nacional y local, pero no deberán ocultar la falta de información territorial más específica.

---

## 11. Identidad del proyecto

La plataforma buscará sostener estos atributos:

- basada en datos abiertos;
- con acceso anónimo a sus fuentes esenciales;
- reproducible;
- auditable;
- interoperable;
- portable entre jurisdicciones;
- sin dependencia obligatoria de proveedores privados ni credenciales;
- compatible con colaboración pública, académica y científica.

---

## 12. Principio final

> El núcleo de la plataforma utilizará exclusivamente datos abiertos, oficiales, documentados y accesibles de manera anónima y reproducible. Ninguna funcionalidad esencial dependerá de cuentas, registros, claves, tokens, convenios institucionales, credenciales restringidas o servicios comerciales.