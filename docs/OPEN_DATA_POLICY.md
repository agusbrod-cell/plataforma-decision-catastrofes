# OPEN DATA POLICY

## Política de datos abiertos de la plataforma

**Estado:** política rectora inicial  
**Alcance:** núcleo funcional de la plataforma  
**Principio:** Open Data First

---

## 1. Propósito

La plataforma se construirá bajo una filosofía **Open Data First**.

Toda funcionalidad esencial deberá apoyarse, prioritariamente, en fuentes de datos abiertas, oficiales, documentadas y públicamente accesibles, provenientes de organismos nacionales e internacionales.

La plataforma buscará que sus resultados puedan ser reproducidos, auditados y comprendidos por terceros sin depender de acuerdos privados, servicios comerciales o credenciales institucionales restringidas.

---

## 2. Principio de admisión

Una fuente podrá incorporarse al núcleo cuando cumpla, preferentemente, con los siguientes criterios:

- provenir de un organismo público, institución científica o iniciativa abierta reconocida;
- contar con una licencia abierta o términos compatibles con consulta, procesamiento e integración pública;
- disponer de acceso reproducible por terceros;
- ofrecer API pública, servicios OGC —WMS, WFS o WMTS—, descarga oficial u otro mecanismo abierto documentado;
- poseer metadatos suficientes para interpretar correctamente los datos;
- permitir identificar origen, fecha, versión, cobertura y transformaciones;
- contar con una estabilidad institucional razonable;
- permitir una atribución clara y verificable.

Ante dos fuentes técnicamente equivalentes, siempre se priorizará la alternativa abierta, oficial, documentada y reproducible.

---

## 3. Dependencias excluidas del núcleo

La plataforma no dependerá para su funcionamiento esencial de:

- convenios institucionales;
- credenciales privadas;
- cuentas cerradas;
- tokens de acceso restringido;
- servicios comerciales;
- datos con restricciones incompatibles con un proyecto abierto;
- información cuyo acceso no pueda ser reproducido por terceros;
- datasets con términos ambiguos respecto del uso, procesamiento o redistribución;
- datos personales sensibles sin base legal, protección y gobernanza adecuadas.

Las fuentes que requieran autorizaciones especiales, licencias restrictivas o acceso cerrado no formarán parte del núcleo.

En una etapa futura podrán incorporarse únicamente como módulos opcionales y desacoplados, sin afectar la portabilidad, transparencia, reproducibilidad ni funcionamiento básico del sistema.

---

## 4. Clasificación operativa

### Verde — integración inmediata

Fuente abierta con acceso técnico público, documentación suficiente y licencia compatible.

Ejemplos de acceso:

- API pública;
- WMS, WFS o WMTS;
- descarga oficial en CSV, GeoJSON, GeoTIFF, NetCDF o shapefile;
- feed público documentado.

### Amarillo — integración con trabajo técnico

Fuente abierta y jurídicamente utilizable, pero que requiere:

- normalización;
- conversión de formato;
- reproyección;
- procesamiento geoespacial;
- control de calidad;
- armonización temporal;
- interpretación técnica adicional.

### Rojo — no incorporar al núcleo

Fuente con:

- acceso cerrado;
- licencia restrictiva;
- convenio obligatorio;
- credenciales privadas obligatorias;
- términos de uso ambiguos;
- dependencia de un proveedor comercial;
- imposibilidad de reproducir el acceso.

---

## 5. Datos locales

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

---

## 6. Requisitos de registro de cada fuente

Toda fuente integrada deberá documentar, como mínimo:

- organismo responsable;
- nombre del portal, servicio o dataset;
- URL oficial;
- licencia o términos de uso;
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

## 7. Regla de arquitectura

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

## 8. Prioridad geográfica

La selección de fuentes seguirá este orden general:

1. fuentes abiertas nacionales de Argentina;
2. fuentes abiertas provinciales o regionales;
3. fuentes abiertas internacionales;
4. datos locales cargados voluntariamente por cada jurisdicción.

Las fuentes internacionales complementarán la información nacional y local, pero no deberán ocultar la falta de información territorial más específica.

---

## 9. Identidad del proyecto

La plataforma buscará sostener estos atributos:

- basada en datos abiertos;
- reproducible;
- auditable;
- interoperable;
- portable entre jurisdicciones;
- sin dependencia obligatoria de proveedores privados;
- compatible con colaboración pública, académica y científica.

---

## 10. Principio final

> El núcleo de la plataforma utilizará datos abiertos, oficiales, documentados y reproducibles. Ninguna funcionalidad esencial dependerá de fuentes privadas, convenios institucionales, credenciales restringidas o servicios comerciales.
