# PROJECT BIBLE

## Plataforma de apoyo a decisiones públicas ante catástrofes

**Estado del documento:** versión inicial para revisión humana  
**Naturaleza:** documento rector del proyecto  
**Repositorio:** `agusbrod-cell/plataforma-decision-catastrofes`

---

## 1. Por qué existe este proyecto

La plataforma nace de una preocupación concreta de gestión pública: después de una catástrofe, los impactos ambientales, sanitarios, sociales e institucionales se superponen y evolucionan con rapidez.

La experiencia observada en La Guaira mostró cómo, luego de un evento destructivo, pueden coexistir grandes volúmenes de residuos y escombros, descargas de efluentes, fallas cloacales, contaminación del mar y del agua, afectación epidemiológica, riesgos para la salud pública y un aumento de la vulnerabilidad social.

El problema no es solamente la falta de información. Muchas veces existen datos, mapas, imágenes, registros, informes y conocimiento técnico, pero están dispersos, tienen diferentes formatos, distintas escalas, calidades desiguales y no llegan al funcionario en una forma útil para decidir.

Esta plataforma busca transformar evidencia territorial y técnica en información priorizada, comprensible, trazable y accionable para la gestión pública.

---

## 2. Propósito central

Construir una plataforma web robusta que integre datos abiertos, información geoespacial, imágenes satelitales o aéreas, datos municipales y conocimiento técnico estructurado para apoyar la priorización de problemas socioambientales ante catástrofes.

La plataforma deberá ayudar a responder, con claridad:

1. ¿Qué está ocurriendo?
2. ¿Dónde está ocurriendo?
3. ¿Qué población, ecosistemas, servicios e infraestructuras están expuestos?
4. ¿Qué problemas requieren atención prioritaria?
5. ¿Qué riesgos pueden agravarse en cascada?
6. ¿Qué información falta verificar?
7. ¿Qué áreas institucionales deberían coordinarse?
8. ¿Qué capacidades y recursos existen?
9. ¿Qué brechas limitan la respuesta?
10. ¿Qué lineamientos generales de intervención pueden evaluarse?
11. ¿Qué evidencia respalda cada resultado?
12. ¿Qué nivel de confianza tiene el análisis?

---

## 3. Principio rector

> La plataforma no reemplaza la decisión pública. Organiza evidencia para mejorarla.

La plataforma no debe emitir órdenes automáticas ni sustituir el criterio profesional, administrativo, político, operativo o legal de los funcionarios.

Debe contribuir a:

- identificar problemas;
- ordenar prioridades;
- explicar riesgos en cascada;
- mostrar evidencia;
- señalar datos faltantes;
- sugerir coordinación institucional;
- presentar lineamientos posibles;
- registrar incertidumbre;
- facilitar trazabilidad y auditoría.

La decisión final siempre debe permanecer bajo responsabilidad humana.

---

## 4. Problema que busca resolver

Después de una catástrofe, diferentes áreas de gobierno deben decidir con rapidez mientras enfrentan:

- información incompleta;
- datos dispersos;
- falta de interoperabilidad;
- presión operativa;
- múltiples problemas simultáneos;
- escasez de recursos;
- incertidumbre territorial;
- posibles consecuencias en cascada;
- necesidad de justificar decisiones;
- coordinación entre organismos con competencias diferentes.

La plataforma debe ayudar a convertir ese escenario complejo en una lectura inicial simple y progresiva.

No debe mostrar primero toda la complejidad técnica. Debe mostrar primero lo que el funcionario necesita comprender para actuar.

---

## 5. Usuarios principales

Los usuarios previstos incluyen:

- áreas municipales de Ambiente;
- Defensa Civil;
- Obras Públicas;
- Salud;
- Desarrollo Social;
- servicios de agua y saneamiento;
- centros de operaciones de emergencia;
- autoridades municipales;
- equipos técnicos;
- organismos provinciales o regionales;
- instituciones que colaboren en la respuesta.

La plataforma debe asumir que la gestión es interinstitucional.

No debe diseñarse como si una sola persona o una sola dependencia resolviera el evento.

---

## 6. Eventos piloto

La primera etapa deberá contemplar tres tipos de eventos:

- incendios forestales;
- inundaciones;
- tornados.

La arquitectura deberá permitir agregar más adelante:

- terremotos;
- deslizamientos;
- sequías;
- olas de calor;
- tormentas severas;
- otros eventos ambientales o tecnológicos.

Los eventos no deben quedar codificados de forma rígida dentro de la interfaz. Cada nuevo evento deberá poder incorporarse mediante configuraciones, reglas, fuentes y módulos de conocimiento sin reescribir el núcleo de la plataforma.

---

## 7. Alcance temporal

La plataforma podrá contribuir en tres momentos:

### 7.1. Preparación

- reconocimiento de vulnerabilidades;
- identificación de infraestructura crítica;
- conocimiento territorial;
- revisión de capacidades locales;
- preparación para temporadas de riesgo.

### 7.2. Respuesta

- consolidación de información actualizada;
- identificación de prioridades;
- visualización territorial;
- coordinación entre áreas;
- registro de información faltante.

### 7.3. Recuperación

- priorización de problemas ambientales postcatástrofe;
- seguimiento de residuos, efluentes, agua, suelo y ecosistemas;
- reducción de riesgos secundarios;
- prevención del aumento de vulnerabilidad social;
- trazabilidad de medidas y resultados.

La plataforma no debe confundirse con un sistema de despacho de emergencias ni con un centro de comando en tiempo real durante su primera versión.

---

## 8. Qué debe hacer la plataforma

La plataforma deberá poder:

- registrar o seleccionar un evento;
- asociarlo a una jurisdicción y un territorio;
- incorporar datos abiertos y geoespaciales;
- incorporar datos municipales validados;
- mostrar imágenes y productos derivados;
- identificar elementos expuestos;
- representar riesgos en cascada;
- ordenar prioridades;
- diferenciar criticidad y confianza;
- identificar información pendiente;
- sugerir áreas para coordinación;
- mostrar lineamientos de intervención;
- explicar por qué se obtuvo cada resultado;
- identificar todas las fuentes utilizadas;
- conservar historial de transformaciones y versiones;
- producir mapas, gráficos, fichas y reportes comprensibles.

---

## 9. Qué no debe hacer

La plataforma no debe:

- reemplazar a autoridades o técnicos;
- decidir automáticamente por el gobierno;
- emitir órdenes obligatorias;
- presentar predicciones como certezas;
- ocultar información faltante;
- inventar datos;
- inventar fuentes;
- inventar normativa;
- inventar reglas científicas;
- mezclar datos demostrativos con datos operativos;
- modificar silenciosamente datos originales;
- mostrar una categoría sin explicar su fundamento;
- usar inteligencia artificial como autoridad final;
- priorizar solamente por un índice opaco;
- sobrecargar la pantalla inicial con información técnica;
- depender exclusivamente del color para comunicar riesgos;
- utilizar datos personales sensibles sin una justificación, protección y marco legal adecuados.

---

## 10. Filosofía de experiencia de usuario

La referencia tomada de plataformas simples de coordinación humanitaria es su practicidad, no su funcionalidad exacta ni su diseño propietario.

La plataforma debe ser más robusta por detrás y más clara por delante.

> La complejidad técnica debe quedar detrás del sistema. La claridad debe quedar delante del usuario.

La interfaz debe seguir esta secuencia:

1. Qué ocurre.
2. Qué es prioritario.
3. Qué puede agravarse.
4. Dónde ocurre.
5. Qué falta verificar.
6. Quiénes deberían coordinarse.
7. Por qué el sistema muestra ese resultado.
8. Cómo se obtuvo técnicamente.

---

## 11. Lectura progresiva

La información deberá organizarse en tres niveles.

### Nivel 1: lectura inmediata

Debe comprenderse en menos de un minuto.

Incluye:

- estado general;
- criticidad;
- tres a cinco prioridades principales;
- dos o tres riesgos en cascada relevantes;
- mapa operativo simplificado;
- población, servicios o infraestructura expuesta;
- alertas;
- información pendiente;
- nivel de confianza.

### Nivel 2: detalle operativo

Incluye:

- descripción del problema;
- consecuencias posibles;
- áreas sugeridas para coordinación;
- recursos disponibles;
- brechas;
- lineamientos de intervención;
- evidencia utilizada;
- incertidumbre;
- acciones de validación.

### Nivel 3: fundamento técnico

Incluye:

- fuentes;
- variables;
- reglas activadas;
- metodología;
- transformaciones;
- fecha de actualización;
- resolución;
- limitaciones;
- referencias;
- historial y trazabilidad.

---

## 12. Salidas principales

La plataforma deberá producir salidas simples de interpretar y técnicamente auditables.

### 12.1. Criticidad general

Categorías iniciales:

- crítica;
- alta;
- moderada;
- baja;
- información insuficiente.

La criticidad representa la importancia y urgencia del problema.

### 12.2. Confianza

Categorías iniciales:

- alta;
- media;
- baja;
- no evaluable.

La confianza representa la calidad y suficiencia de la evidencia disponible.

**Criticidad y confianza son conceptos diferentes y nunca deben fusionarse.**

Un problema puede ser crítico y tener confianza baja. En ese caso, la plataforma deberá mostrar que la posible gravedad exige verificación urgente.

### 12.3. Riesgos en cascada

Ejemplo:

```text
Incendio
→ pérdida de cobertura vegetal
→ erosión
→ arrastre de cenizas y sedimentos
→ deterioro del agua
→ posible interrupción del servicio
→ aumento de vulnerabilidad social
```

La plataforma deberá diferenciar:

- situación observada;
- consecuencia probable;
- consecuencia posible;
- dato pendiente de verificación.

### 12.4. Mapa operativo

El mapa inicial deberá mostrar únicamente las capas relevantes para la decisión actual.

Ejemplos:

- área afectada;
- zonas críticas;
- población expuesta;
- caminos relevantes;
- cursos y captaciones de agua;
- infraestructura crítica;
- puntos de intervención;
- áreas pendientes de verificación.

Las capas técnicas adicionales deberán estar disponibles en un nivel secundario.

### 12.5. Gráficos

Los gráficos deberán responder una pregunta concreta y evitar decoración innecesaria.

Ejemplos:

- población expuesta;
- infraestructura afectada;
- prioridades por criticidad;
- capacidad disponible frente a necesidad estimada;
- evolución temporal;
- porcentaje de datos verificados;
- calidad de evidencia.

Cada gráfico deberá incluir título, unidad, fuente, fecha y una breve interpretación.

---

## 13. Estructura mínima de una prioridad

Cada prioridad deberá contener:

- identificador;
- título;
- criticidad;
- confianza;
- resumen breve;
- situación detectada;
- riesgo principal;
- elementos expuestos;
- sensibilidad temporal;
- riesgos en cascada relacionados;
- evidencia utilizada;
- información faltante;
- áreas sugeridas para coordinación;
- recursos disponibles;
- brechas;
- lineamientos de intervención;
- limitaciones;
- fuentes;
- fecha de actualización;
- estado de validación.

---

## 14. Datos de entrada

La plataforma deberá integrar cuatro grandes grupos de información.

### 14.1. Datos abiertos

Ejemplos:

- límites administrativos;
- relieve;
- pendientes;
- hidrografía;
- cuencas;
- cobertura del suelo;
- bosque nativo;
- áreas protegidas;
- caminos;
- centros de salud;
- escuelas;
- población;
- infraestructura crítica;
- meteorología;
- focos de calor;
- precipitaciones;
- antecedentes históricos.

### 14.2. Datos municipales

Ejemplos:

- estado de caminos;
- maquinaria disponible;
- brigadas;
- camiones cisterna;
- centros de evacuación;
- captaciones de agua;
- interrupciones de servicios;
- daños observados;
- residuos generados;
- fotografías y relevamientos de campo.

### 14.3. Imágenes

Ejemplos:

- imágenes satelitales;
- imágenes aéreas;
- fotografías georreferenciadas;
- productos ráster;
- comparaciones temporales;
- resultados de clasificación o detección.

### 14.4. Conocimiento técnico estructurado

Incluye:

- reglas causales;
- relaciones de cascada;
- normativa;
- protocolos oficiales;
- bibliografía científica;
- guías operativas;
- lineamientos de intervención;
- experiencias verificadas.

---

## 15. Principios de calidad de datos

La información debe ser fehaciente, precisa, verificable y apropiada para el uso previsto.

Cada fuente deberá registrar, cuando corresponda:

- organismo productor;
- nombre del conjunto de datos;
- identificador o URL;
- licencia;
- fecha de publicación;
- fecha de actualización;
- fecha de consulta;
- cobertura geográfica;
- resolución espacial;
- resolución temporal;
- sistema de referencia de coordenadas;
- formato;
- método de acceso;
- versión;
- controles de calidad;
- limitaciones;
- condiciones de uso.

No todos los datos abiertos tienen la misma calidad. La plataforma deberá evaluar la aptitud del dato para cada uso concreto.

---

## 16. Trazabilidad y procedencia

Cada resultado deberá poder responder:

- ¿Qué fuente se utilizó?
- ¿Qué versión?
- ¿Cuándo se consultó?
- ¿Qué transformación recibió?
- ¿Qué regla utilizó ese dato?
- ¿Qué resultado produjo?
- ¿Qué limitaciones tenía?
- ¿Hubo validación humana?

La cadena de trazabilidad deberá conservar:

1. referencia al dato original;
2. copia o huella verificable cuando corresponda;
3. dato normalizado;
4. transformaciones aplicadas;
5. versión de cada proceso;
6. responsable o proceso que lo generó;
7. resultado derivado;
8. historial de actualizaciones.

Ninguna transformación deberá ocurrir de manera silenciosa.

---

## 17. Procesamiento de imágenes

El procesamiento de imágenes deberá estar desacoplado de la interfaz.

Todo producto derivado deberá registrar:

- imagen de origen;
- proveedor;
- fecha de adquisición;
- cobertura;
- resolución;
- bandas utilizadas;
- porcentaje de nubes cuando corresponda;
- preprocesamiento;
- algoritmo;
- parámetros;
- versión del algoritmo;
- archivo resultante;
- métricas de calidad;
- incertidumbre;
- validación humana.

Los resultados derivados de imágenes no deberán mostrarse como hechos confirmados si todavía requieren verificación.

---

## 18. Motor de decisión

El corazón de la plataforma será un motor de priorización explicable.

El motor deberá integrar, entre otros elementos:

- gravedad potencial;
- urgencia temporal;
- población expuesta;
- vulnerabilidad social;
- ecosistemas afectados;
- infraestructura crítica;
- servicios esenciales;
- posibilidad de consecuencias en cascada;
- reversibilidad;
- capacidad institucional;
- recursos disponibles;
- calidad de la evidencia;
- incertidumbre.

La lógica puede combinar reglas, umbrales, puntuaciones y validación humana, pero nunca deberá convertirse en una caja negra.

Toda prioridad deberá explicar por qué fue generada.

No se implementarán reglas reales hasta contar con validación técnica, fuentes y casos de prueba.

---

## 19. Uso de inteligencia artificial

La inteligencia artificial puede utilizarse como apoyo para:

- clasificación preliminar;
- detección de patrones;
- procesamiento de imágenes;
- resumen de información;
- asistencia documental;
- generación de explicaciones;
- búsqueda de inconsistencias.

No deberá utilizarse como autoridad final para:

- declarar una emergencia;
- asignar responsabilidades legales;
- ordenar evacuaciones;
- definir acciones obligatorias;
- confirmar contaminación sin evidencia;
- reemplazar validación profesional;
- ocultar incertidumbre.

Toda salida generada o asistida por IA deberá ser identificable, trazable y revisable.

---

## 20. Arquitectura conceptual

La plataforma deberá mantener separadas las siguientes capas:

```text
Interfaz web
↓
API
↓
Motor de decisión
↓
Base de conocimiento
↓
Servicios geoespaciales y procesamiento de imágenes
↓
Conectores de datos abiertos y datos municipales
↓
Fuentes originales
```

La interfaz no deberá contener lógica de decisión crítica.

Los conectores no deberán decidir prioridades.

El motor de decisión no deberá modificar datos originales.

La base de conocimiento deberá poder versionarse.

---

## 21. Principios técnicos

El desarrollo deberá priorizar:

- modularidad;
- mantenibilidad;
- tipado;
- validación de datos;
- pruebas automatizadas;
- interoperabilidad;
- accesibilidad;
- seguridad;
- documentación;
- versionado;
- observabilidad;
- cambios pequeños y revisables.

Las decisiones técnicas importantes deberán documentarse mediante ADR en `docs/decisions/`.

---

## 22. Datos demostrativos y datos operativos

La plataforma deberá diferenciar explícitamente:

- `demo`: datos ficticios utilizados para diseño y pruebas;
- `operational`: datos reales utilizados en un entorno autorizado.

Todo entorno demo deberá mostrar una advertencia persistente:

> DATOS DEMOSTRATIVOS — NO UTILIZAR PARA DECISIONES REALES.

Los datos demo no deberán mezclarse con datos reales ni presentarse como información oficial.

---

## 23. Caso piloto inicial

El primer prototipo utilizará un escenario simulado:

- jurisdicción: Villa Yacanto, Córdoba, Argentina;
- evento: incendio forestal;
- estado general: crítico;
- datos: exclusivamente demostrativos.

El caso podrá incluir:

- posible riesgo para una captación de agua;
- erosión y arrastre de sedimentos;
- afectación por humo;
- caminos comprometidos;
- población rural potencialmente aislada;
- coordinación entre Ambiente, Defensa Civil, Obras Públicas, Salud y prestadores de servicios.

Este caso servirá para probar la experiencia de uso, los modelos y la arquitectura. No representará una evaluación real del municipio.

---

## 24. Seguridad y privacidad

La plataforma deberá:

- evitar secretos en el repositorio;
- utilizar variables de entorno;
- aplicar controles de acceso;
- registrar cambios sensibles;
- minimizar datos personales;
- preferir información agregada;
- proteger ubicaciones sensibles cuando corresponda;
- cumplir los marcos legales aplicables;
- diferenciar información pública, interna y restringida.

No se incorporarán datos individuales de salud ni seguimiento de personas en la primera etapa.

---

## 25. Accesibilidad y comunicación

La plataforma deberá ser utilizable por personas con diferentes niveles técnicos.

Requisitos mínimos:

- lenguaje claro;
- navegación por teclado;
- compatibilidad con lectores de pantalla;
- etiquetas accesibles;
- contraste suficiente;
- diseño adaptable;
- mensajes de error comprensibles;
- iconos acompañados por texto;
- colores no utilizados como único canal de información;
- unidades y fechas claramente expresadas.

---

## 26. Gobernanza del proyecto

Los roles iniciales serán:

### Dirección funcional

Responsable de definir necesidades reales de gestión pública, prioridades del producto y validación de utilidad.

### Arquitectura y documentación

Responsable de traducir necesidades funcionales en especificaciones, modelos, reglas de calidad y criterios de aceptación.

### Desarrollo asistido por Codex

Responsable de implementar tareas delimitadas, documentadas y revisables en ramas separadas.

### Revisión humana

Ningún cambio relevante deberá incorporarse a `main` sin revisión.

---

## 27. Forma de trabajo con GitHub

Principios:

- `main` debe permanecer estable;
- cada tarea se desarrolla en una rama;
- cada cambio relevante se revisa mediante pull request;
- los commits deben ser claros;
- las pruebas deben ejecutarse antes del merge;
- las limitaciones deben quedar documentadas;
- no se habilitará merge automático en la etapa inicial;
- los documentos rectores deben mantenerse actualizados.

Flujo recomendado:

```text
Necesidad pública
→ especificación funcional
→ tarea técnica
→ rama
→ implementación
→ pruebas
→ pull request
→ revisión
→ merge
```

---

## 28. Reglas permanentes para Codex y otros agentes

Antes de modificar el proyecto, cualquier agente deberá:

1. leer `PROJECT_BIBLE.md`;
2. leer `AGENTS.md` cuando exista;
3. revisar los documentos de `/docs`;
4. inspeccionar el repositorio;
5. indicar el alcance exacto;
6. explicitar supuestos;
7. no ampliar la tarea sin autorización;
8. trabajar en una rama separada;
9. agregar pruebas;
10. actualizar documentación cuando corresponda.

Está prohibido:

- inventar datos;
- inventar fuentes;
- inventar normativa;
- inventar reglas científicas;
- implementar fórmulas no aprobadas;
- ocultar fallos;
- declarar completada una tarea con pruebas fallidas;
- introducir dependencias sin justificar;
- colocar secretos en el código;
- mezclar lógica de dominio con presentación;
- hacer merge automático.

---

## 29. Criterios para considerar útil una primera versión

Una primera versión será útil cuando un funcionario pueda, en menos de un minuto:

- reconocer el estado general;
- identificar las prioridades principales;
- comprender los riesgos en cascada;
- localizar zonas críticas en un mapa;
- conocer qué información falta;
- reconocer qué áreas deberían coordinarse;
- acceder al fundamento de cada resultado;
- distinguir entre criticidad y confianza;
- verificar las fuentes utilizadas.

La utilidad no se medirá por la cantidad de datos mostrados, sino por la calidad de la decisión que la plataforma ayuda a estructurar.

---

## 30. Primera etapa de desarrollo

La primera etapa deberá limitarse a:

- documentación;
- estructura del repositorio;
- modelos conceptuales iniciales;
- API de demostración;
- datos demo centralizados;
- tablero de evento;
- tarjetas de prioridad;
- riesgos en cascada;
- mapa con GeoJSON demostrativo;
- información pendiente;
- coordinación institucional;
- pruebas básicas.

No incluirá todavía:

- datos oficiales reales;
- conectores productivos;
- procesamiento real de imágenes;
- inteligencia artificial operativa;
- algoritmo definitivo de priorización;
- autenticación completa;
- despliegue productivo.

---

## 31. Decisiones pendientes de validación

Las siguientes decisiones deberán definirse progresivamente:

- nombre público definitivo de la plataforma;
- licencia del repositorio;
- organismos y usuarios piloto;
- fuentes oficiales prioritarias;
- estrategia de actualización de datos;
- metodología definitiva de priorización;
- reglas técnicas por evento;
- umbrales de criticidad;
- políticas de validación humana;
- arquitectura de autenticación;
- infraestructura de despliegue;
- marco legal y responsabilidades;
- tratamiento de datos sensibles;
- estrategia de mantenimiento y gobernanza.

Hasta que sean aprobadas, deberán figurar como **PENDIENTE DE VALIDACIÓN**.

---

## 32. Declaración final

Esta plataforma debe ser rigurosa sin ser confusa, robusta sin ser inaccesible y técnicamente avanzada sin desplazar la responsabilidad humana.

Su valor no estará solamente en procesar datos o imágenes, sino en convertir evidencia compleja en una lectura pública clara, verificable y útil para priorizar decisiones ante catástrofes.
