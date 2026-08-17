# Modelo de decisión para incendios forestales en Córdoba

**Proyecto:** Plataforma de apoyo a decisiones públicas ante catástrofes  
**Jurisdicción piloto:** Provincia de Córdoba, Argentina  
**Estado:** especificación funcional inicial basada en evidencia  
**Fecha de revisión:** 17 de agosto de 2026

## 1. Propósito

Este documento define el primer modelo de decisión de la plataforma para incendios forestales, rurales y de interfase en Córdoba. Su objetivo es transformar datos abiertos, cartografía, observaciones territoriales y conocimiento operacional documentado en salidas claras, trazables y útiles para funcionarios públicos y equipos interdisciplinarios.

El sistema es un apoyo a la decisión. No sustituye a la autoridad competente, al Comando del Incendio, al Comando Unificado, a Bomberos Voluntarios, ETAC, Protección Civil, DUAR ni a otros organismos operativos.

## 2. Principio central

Cada salida debe poder responder cuatro preguntas:

1. ¿Qué datos sustentan el resultado?
2. ¿Qué regla, protocolo, norma o evidencia se aplicó?
3. ¿Qué limitaciones tiene la recomendación?
4. ¿Qué área u organismo debería evaluar o ejecutar la acción?

La inteligencia artificial puede resumir y explicar. No debe inventar umbrales, tácticas ni procedimientos operativos.

## 3. Arquitectura lógica

### 3.1 Capa de datos abiertos

Incluye, cuando estén disponibles y auditados:

- Índice Meteorológico de Peligro de Incendios (FWI) y componentes.
- temperatura, humedad, viento y precipitación;
- focos o anomalías térmicas;
- polígonos de áreas quemadas;
- riesgo local de incendio;
- amenaza y vulnerabilidad territorial;
- cobertura y uso del suelo;
- bosque nativo y áreas protegidas;
- pendientes y relieve;
- cuencas, cursos de agua y embalses;
- red vial y accesibilidad;
- localidades, población y urbanización;
- centros de salud;
- cuarteles y jurisdicciones de Bomberos Voluntarios;
- infraestructura pública y crítica cuando su publicación sea compatible con seguridad y privacidad.

### 3.2 Capa de datos aportados por el usuario institucional

Permite incorporar información que los datos abiertos no pueden conocer en tiempo real:

- ubicación y estado conocido del evento;
- recursos efectivamente disponibles;
- cortes o restricciones de caminos;
- problemas de abastecimiento de agua;
- población evacuada o con necesidad de evacuación;
- infraestructura afectada;
- observaciones de campo;
- disponibilidad de maquinaria y logística;
- necesidades de coordinación interáreas.

### 3.3 Base de conocimiento

Se nutre de:

- Ley Provincial 8.751 de Córdoba;
- Ley Nacional 26.815 y modificatorias;
- niveles de actuación del Sistema Federal de Manejo del Fuego;
- estándares nacionales de funciones en estructuras de combate;
- protocolos y materiales oficiales de Bomberos Voluntarios;
- documentos oficiales de ETAC y DUAR que puedan verificarse;
- metodologías provinciales de mapas de riesgo local;
- literatura científica y técnica revisada;
- antecedentes de sistemas de apoyo a decisiones como WFDSS/RMA;
- conocimiento post-incendio sobre erosión, inundaciones, remoción en masa, agua, restauración y recuperación.

## 4. Modelo conceptual de decisión

El sistema evalúa seis dimensiones separadas:

### A. Peligro del incendio

Describe qué tan favorable es el ambiente para el comportamiento peligroso del fuego.

Variables posibles: FWI, viento, humedad, temperatura, sequedad, pendiente, combustible y pronóstico.

### B. Amenaza territorial

Describe dónde puede producirse o propagarse un evento con potencial de daño.

Variables posibles: cobertura, pendiente, accesos, proximidad a vegetación combustible, antecedentes y mapas provinciales de amenaza.

### C. Exposición

Describe qué personas, bienes, ecosistemas e infraestructura se encuentran potencialmente afectados.

Variables posibles: población, viviendas, escuelas, centros de salud, rutas, áreas protegidas, bosque nativo, cursos de agua e infraestructura crítica.

### D. Vulnerabilidad

Describe la susceptibilidad del territorio y la población frente al daño.

Variables posibles: interfase urbano-forestal, accesibilidad, aislamiento, dependencia de una sola ruta, condiciones sociales, proximidad a centros de respuesta y sensibilidad ecológica.

### E. Capacidad de respuesta

Describe con qué recursos cuenta efectivamente la jurisdicción en ese momento.

Esta dimensión no debe inferirse desde la mera existencia de un cuartel. La plataforma debe diferenciar infraestructura disponible de capacidad operativa real.

### F. Riesgos en cascada

Incluye consecuencias secundarias o posteriores:

- erosión;
- crecidas e inundaciones post-incendio;
- flujos de detritos o remoción en masa;
- deterioro de calidad del agua;
- afectación de captaciones;
- pérdida de bosque nativo;
- afectación de biodiversidad;
- residuos y materiales quemados;
- afectación económica y social;
- restricciones legales de uso post-incendio.

## 5. Reglas de decisión iniciales

Las reglas completas se almacenan en `data/MATRIZ_REGLAS_DECISION_INCENDIOS_CORDOBA.csv`.

### 5.1 Escalamiento institucional

La Ley 26.815 establece tres niveles de actuación. El sistema puede recomendar **evaluar escalamiento**, pero no declarar por sí mismo un Nivel II o III.

- **Nivel I:** ataque inicial y responsabilidad jurisdiccional.
- **Nivel II:** cuando la capacidad de respuesta jurisdiccional se encuentra comprometida o agotada, la autoridad competente puede solicitar apoyo regional.
- **Nivel III:** cuando la magnitud, duración, complejidad o multiplicidad de incidentes supera la capacidad regional, puede solicitarse apoyo extrarregional/nacional.

**Salida permitida:** “La información ingresada indica posible compromiso de capacidad local. Evaluar solicitud de apoyo conforme al esquema de niveles de actuación de la Ley 26.815.”

**Salida no permitida:** “Activar Nivel II automáticamente.”

### 5.2 Comando y coordinación

Cuando intervienen múltiples organismos, la normativa nacional prevé la continuidad de la autoridad competente y la posibilidad de Comando Unificado.

**Salida permitida:** advertir que la complejidad interinstitucional requiere coordinación formal y recomendar verificar la activación del esquema de comando correspondiente.

### 5.3 Peligro meteorológico

El FWI provincial es un índice de peligro, no una probabilidad de ignición. La plataforma debe mostrarlo como condición de comportamiento potencial del fuego y nunca traducirlo directamente en “habrá incendio”.

### 5.4 Riesgo territorial local

Los mapas provinciales de riesgo local combinan amenaza y vulnerabilidad y fueron desarrollados mediante metodologías reproducibles, incluyendo ponderación de variables mediante Proceso de Análisis Jerárquico en sus versiones actualizadas.

**Uso permitido:** priorizar áreas para vigilancia, preparación, análisis de exposición y planificación.

**Límite:** no extrapolar una cartografía local fuera de su zona de estudio.

### 5.5 Protección de población

Si un incendio amenaza población o infraestructura sensible, la plataforma debe elevar la prioridad socioambiental y mostrar:

- población potencialmente expuesta;
- centros de salud cercanos;
- accesos y rutas alternativas;
- cursos o cuerpos de agua relevantes;
- jurisdicción de respuesta;
- incertidumbres de los datos.

Las órdenes de evacuación corresponden a la autoridad competente. La plataforma puede recomendar **evaluar necesidad de evacuación** y mostrar factores que justifican la evaluación.

### 5.6 Protección ambiental

Cuando el área potencialmente afectada intersecta bosque nativo, áreas protegidas, humedales, cuencas o ambientes de alta sensibilidad, el sistema debe elevar la prioridad ambiental y preparar automáticamente un bloque de recuperación post-incendio.

## 6. Post-incendio como parte del incidente

La plataforma no debe considerar finalizada la gestión ambiental cuando el fuego queda extinguido.

### 6.1 Primeras preguntas

- ¿qué superficie fue afectada?
- ¿qué coberturas fueron afectadas?
- ¿qué proporción corresponde a bosque nativo?
- ¿intersecta áreas protegidas?
- ¿qué cuencas fueron afectadas?
- ¿qué pendientes existen?
- ¿hay localidades, rutas o infraestructura aguas abajo?
- ¿se pronostican precipitaciones intensas?

### 6.2 Riesgo hidrológico post-incendio

La evidencia científica internacional demuestra que los incendios pueden alterar de forma importante la respuesta hidrológica de cuencas quemadas y aumentar el riesgo de crecidas repentinas y flujos de detritos ante lluvias posteriores.

La plataforma debe generar una **alerta de evaluación post-incendio** cuando coincidan, al menos conceptualmente:

- área quemada relevante;
- pendientes fuertes;
- cuenca o cauce conectado;
- elementos expuestos aguas abajo;
- pronóstico de precipitación.

En la primera versión, esta regla será cualitativa salvo que se implemente y valide un modelo cuantitativo específico para Córdoba.

### 6.3 Agua y saneamiento

Si el incendio afecta una cuenca de abastecimiento, captación, embalse o curso próximo a población, la plataforma debe recomendar evaluación de:

- turbidez y sedimentos;
- cenizas y material particulado;
- continuidad de captaciones;
- posibles contaminantes asociados a estructuras o residuos quemados;
- necesidad de monitoreo reforzado.

### 6.4 Restauración y restricciones de uso

La Ley 26.815 y su modificación por Ley 27.604 establecen obligaciones de recomposición y restricciones al cambio de uso de superficies incendiadas. El sistema debe advertir estas condiciones cuando detecte intersección con bosques, áreas protegidas, humedales, pastizales u otras categorías alcanzadas por la normativa.

La plataforma no debe equiparar “restauración” con “plantar árboles”. Debe indicar que la estrategia depende del ecosistema, severidad, regeneración natural, suelo, agua y objetivos de conservación.

## 7. Tipos de salida

La interfaz inicial debe producir, en este orden:

1. **Criticidad:** baja, media, alta o muy alta.
2. **Confianza del análisis:** separada de la criticidad.
3. **Factores determinantes:** máximo 5 en la vista principal.
4. **Mapa de situación.**
5. **Riesgos en cascada.**
6. **Prioridades sugeridas.**
7. **Áreas u organismos a involucrar.**
8. **Fuentes utilizadas.**
9. **Datos faltantes que podrían cambiar la evaluación.**
10. **Fundamento técnico ampliado.**

## 8. Niveles de evidencia

Cada regla debe tener un nivel de evidencia independiente de su prioridad.

- **E1 — Norma obligatoria:** ley, decreto, resolución o norma vigente.
- **E2 — Protocolo oficial:** procedimiento o doctrina institucional verificada.
- **E3 — Método oficial aplicado:** metodología técnica utilizada por organismo competente.
- **E4 — Evidencia científica fuerte:** literatura revisada por pares o informe científico reconocido.
- **E5 — Evidencia de apoyo:** antecedente técnico útil pero no suficiente como única base.

Una recomendación puede tener prioridad alta y evidencia baja; en ese caso la interfaz debe hacerlo visible.

## 9. Reglas prohibidas

El motor no debe:

- inventar umbrales meteorológicos;
- inferir disponibilidad de personal desde la ubicación de un cuartel;
- ordenar evacuaciones;
- ordenar maniobras tácticas de combate;
- declarar niveles de actuación institucional;
- reemplazar al Comando del Incendio;
- presentar un foco satelital como incendio confirmado sin validación;
- presentar un polígono quemado como incendio activo;
- extrapolar metodologías locales a toda Córdoba sin validación;
- confundir peligro, amenaza, vulnerabilidad, exposición y riesgo;
- ocultar datos faltantes o incertidumbre.

## 10. Antecedentes utilizados

### Córdoba

- Ley Provincial 8.751 — Normas y procedimiento para el manejo del fuego.
  - https://www.argentina.gob.ar/normativa/provincial/ley-8751-123456789-0abc-defg-157-8000ovorpyel/actualizacion
- IDECOR — Riesgo Local para Incendios Forestales.
  - https://www.idecor.gob.ar/informes/mapa-de-riesgo-local-para-incendios-forestales/
- IDECOR — Metodología y utilidad del mapa de riesgo local.
  - https://www.idecor.gob.ar/utilidad-del-mapa-de-riesgo-de-incendio-local/
- IDECOR — Mapas de Riesgo Local ante Incendios Forestales.
  - https://www.idecor.gob.ar/mapas-de-riesgo-local-ante-incendios-forestales/
- IDECOR — Índice Meteorológico de Peligro de Incendios.
  - https://www.idecor.gob.ar/nueva-version-del-mapa-diario-de-indice-de-riesgo-de-incendio/
- IDECOR — Áreas afectadas por incendios 2025.
  - https://www.idecor.gob.ar/incendios-forestales-y-rurales-en-2025-los-datos-oficiales-del-mapeo-provincial/
- Federación de Bomberos Voluntarios de Córdoba — estructura educativa y capacitación.
  - https://www.bomberoscordoba.com.ar/capacitacion/estructura-educativa.php

### Argentina

- Ley Nacional 26.815 — Manejo del Fuego.
  - https://www.argentina.gob.ar/normativa/nacional/207401/actualizacion
- Servicio Nacional de Manejo del Fuego — niveles de actuación.
  - https://www.argentina.gob.ar/ambiente/fuego/niveles-actuacion
- Resolución 1437/2002 — Estándar Nacional de Funciones en Estructuras de Combate.
  - https://www.argentina.gob.ar/normativa/nacional/resoluci%C3%B3n-1437-2002-80923/texto
- Administración de Parques Nacionales — funciones de combatientes y rehabilitación ecológica.
  - https://www.argentina.gob.ar/parquesnacionales/combatientes-de-incendios-forestales/que-es-un-combatiente-de-incendios-forestales

### Antecedentes científicos internacionales

- USDA Forest Service — Decision making for wildfires: A guide for applying a risk management process at the incident level.
  - https://research.fs.usda.gov/treesearch/43638
- USDA Forest Service — Strategic wildfire response decision support and Risk Management Assistance.
  - https://research.fs.usda.gov/treesearch/63429
- USDA Forest Service — Wildland Fire Decision Support System (WFDSS).
  - https://research.fs.usda.gov/firelab/products/dataandtools/wildland-fire-decision-support-system-wfdss
- USGS — Post-Wildfire Debris-Flow Hazard Assessment Collection.
  - https://www.usgs.gov/data/post-wildfire-debris-flow-hazard-assessment-pwfdf-collection
- USGS — Postfire debris-flow hazard assessment data.
  - https://www.usgs.gov/programs/landslide-hazards/science/postfire-debris-flow-hazard-assessment-data

## 11. Próximos pasos

1. Validar y ampliar la matriz de reglas.
2. Verificar protocolos institucionales específicos de ETAC, DUAR y Bomberos cuando exista fuente primaria pública.
3. Definir el esquema de datos del motor.
4. Definir una fórmula de criticidad transparente sin mezclarla con confianza.
5. Diseñar un escenario de prueba en Villa Yacanto / Calamuchita y otro en Sierras Chicas.
6. Implementar pruebas con eventos históricos conocidos antes de habilitar recomendaciones en producción.
7. Mantener todas las reglas versionadas, trazables y revisables.