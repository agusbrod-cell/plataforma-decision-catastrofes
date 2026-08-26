# Metodología de indicadores para incendios forestales en Córdoba

**Proyecto:** Plataforma de apoyo a decisiones públicas ante catástrofes  
**Jurisdicción piloto:** Provincia de Córdoba, Argentina  
**Estado:** especificación metodológica inicial para validación  
**Principio rector:** el número es interno; la decisión explicada es el producto.

## 1. Propósito

Esta metodología transforma datos abiertos, información territorial declarada por la jurisdicción y conocimiento operacional verificado en cuatro salidas separadas y comprensibles para la toma de decisiones públicas ante incendios forestales, rurales y de interfase.

La metodología no pretende reemplazar el mando operativo ni producir un índice universal. Busca ordenar evidencia en condiciones de presión temporal, hacer visibles las vulnerabilidades socioambientales y ayudar a asignar atención y recursos de manera trazable.

## 2. Identidad metodológica

La plataforma adopta cinco principios:

1. **Prioridad socioambiental.** La gravedad no se limita a la intensidad del fuego: incluye personas, servicios esenciales, ecosistemas y funciones territoriales potencialmente comprometidas.
2. **No compensación.** Una condición crítica no desaparece porque otra dimensión tenga buen desempeño. Una alta capacidad de respuesta no borra una exposición crítica.
3. **Utilidad pública.** Ninguna variable se incorpora solo porque pueda calcularse; debe mejorar una decisión, reducir incertidumbre o anticipar un riesgo.
4. **Trazabilidad.** Toda salida debe conservar dato, fecha, fuente, regla aplicada, limitación y organismo competente.
5. **Incertidumbre visible.** La ausencia o baja calidad de información reduce la confianza del diagnóstico; nunca se rellena con supuestos silenciosos.

## 3. Cuatro salidas independientes

### 3.1 Criticidad Socioambiental (CSA)

Pregunta: **¿qué tan comprometido está el territorio si el evento evoluciona con las condiciones observadas?**

Integra cinco dimensiones normalizadas entre 0 y 1:

- P: peligro y comportamiento potencial;
- E: exposición humana e infraestructura;
- V: vulnerabilidad territorial y social;
- A: sensibilidad ambiental;
- T: conectividad territorial crítica.

En fase experimental puede calcularse un valor base:

`CSA_base = wP·P + wE·E + wV·V + wA·A + wT·T`

con `Σw = 1`.

Los pesos **no se fijan definitivamente en esta versión**. Deben estimarse mediante evidencia, consulta experta documentada y validación retrospectiva. Para Córdoba podrá evaluarse AHP como antecedente metodológico, dado su uso en cartografía provincial de riesgo, sin asumir que sus pesos son transferibles a este motor.

#### Regla de no compensación

El valor base se somete a banderas críticas. Una bandera puede elevar el nivel mínimo de CSA aunque el promedio ponderado sea inferior.

Ejemplos candidatos a validación:

- población o infraestructura sensible directamente expuesta;
- única vía funcional de acceso/egreso comprometida;
- captación de agua o abastecimiento humano potencialmente afectado;
- ecosistema de alta sensibilidad o protección legal afectado;
- combinación de interfase urbano-forestal y propagación hacia área poblada.

Estas banderas no se activarán en producción hasta contar con definición operacional y evidencia suficiente.

### 3.2 Suficiencia de Respuesta (SR)

Pregunta: **¿la jurisdicción declara capacidad suficiente para sostener las necesidades identificadas?**

No mide la existencia nominal de instituciones. Compara necesidades del incidente con recursos efectivamente declarados disponibles.

Dimensiones iniciales:

- personal operativo declarado;
- medios de combate y abastecimiento hídrico;
- maquinaria y logística;
- accesibilidad y movilidad;
- comunicaciones/coordinación;
- apoyo sanitario y protección de población;
- posibilidad de relevo y sostenimiento temporal.

Para cada recurso o función `j`:

`S_j = min(disponibilidad_j / necesidad_j, 1)`

solo cuando la necesidad pueda estimarse mediante protocolo o método validado. Si no existe base válida para estimar necesidad, el sistema no inventará un cociente: mostrará **capacidad declarada** y **necesidad no cuantificada**.

La SR global se expresará preferentemente mediante perfil de brechas y categoría ordinal, no como falsa precisión decimal.

Categorías preliminares:

- suficiente;
- tensionada;
- insuficiente;
- indeterminada por falta de datos.

### 3.3 Confianza de Evidencia (CE)

Pregunta: **¿cuánto podemos confiar en este diagnóstico con la información disponible?**

La CE es independiente de la gravedad del evento.

Para cada variable se registran al menos:

- autoridad y trazabilidad de la fuente;
- actualidad;
- resolución espacial/temporal;
- cobertura territorial;
- completitud;
- consistencia con otras fuentes;
- condición de dato observado, modelado o declarado.

Una formulación inicial para experimentación es:

`CE = Σ(q_i · r_i) / Σr_i`

Donde `q_i` es calidad normalizada de la variable y `r_i` su relevancia para la salida evaluada.

La CE no podrá ser alta si falta una variable definida como crítica para esa decisión. Esta es otra regla de no compensación.

Salida:

- alta;
- media;
- baja;
- insuficiente para concluir.

La interfaz mostrará además qué datos faltantes podrían modificar materialmente el resultado.

### 3.4 Riesgo en Cascada (RC)

Pregunta: **¿qué consecuencias secundarias o posteriores requieren atención desde ahora?**

No se reduce inicialmente a un único promedio. Se modela como una red causal de secuencias plausibles respaldadas por evidencia.

Ejemplo:

`incendio → pérdida de cobertura → precipitación → escorrentía/erosión → sedimentos y cenizas → captación de agua → impacto sanitario/social`

Cada cadena registra:

- evento iniciador;
- condición habilitante;
- receptor expuesto;
- consecuencia potencial;
- horizonte temporal;
- evidencia;
- acción de evaluación o mitigación permitida.

La salida principal será el riesgo en cascada prioritario y, secundariamente, su categoría cualitativa.

## 4. Escalas y normalización

Las variables continuas deben transformarse a una escala común solo cuando exista justificación técnica. Se priorizarán:

1. clases oficiales existentes;
2. percentiles o distribución histórica local;
3. funciones continuas calibradas con datos de Córdoba;
4. criterio experto estructurado, documentado y sujeto a revisión.

Se evita introducir umbrales arbitrarios solo para completar una fórmula.

## 5. Banderas críticas

Las banderas son condiciones que merecen atención inmediata y pueden modificar el piso de prioridad. Deben cumplir cuatro requisitos:

- definición inequívoca;
- dato necesario identificable;
- evidencia o norma verificable;
- salida permitida explícita.

Una bandera no equivale automáticamente a una orden operativa. Por ejemplo, detectar exposición poblacional puede elevar prioridad y recomendar evaluación por la autoridad competente, pero no ordenar evacuación.

## 6. Tratamiento de datos faltantes

El sistema distingue:

- **0:** valor observado igual a cero;
- **desconocido:** dato necesario no disponible;
- **no aplica:** variable irrelevante para ese caso;
- **no actualizado:** existe dato pero excede su vigencia definida.

Nunca se sustituye `desconocido` por cero.

Si falta una variable crítica:

1. se reduce CE;
2. se identifica la brecha;
3. se indica qué decisión queda limitada;
4. se solicita el dato al usuario institucional cuando pueda aportarlo.

## 7. Salida orientada a decisiones

La pantalla principal debe priorizar lectura rápida:

- **Criticidad socioambiental:** baja / media / alta / muy alta;
- **Suficiencia de respuesta:** suficiente / tensionada / insuficiente / indeterminada;
- **Confianza:** alta / media / baja / insuficiente;
- **Riesgo en cascada prioritario:** descripción breve + horizonte temporal;
- hasta cinco factores determinantes;
- hasta cinco prioridades sugeridas;
- áreas u organismos que deberían evaluar o intervenir;
- datos faltantes críticos.

Los valores numéricos internos estarán disponibles en el detalle técnico y en los registros de auditoría, pero no dominarán la interfaz.

## 8. Gobernanza de la recomendación

Cada recomendación debe almacenar:

- identificador;
- fecha/hora;
- jurisdicción;
- datos utilizados y versiones;
- reglas activadas;
- nivel de evidencia;
- resultado de CSA, SR, CE y RC;
- banderas críticas;
- datos faltantes;
- texto mostrado;
- limitaciones;
- organismo o área competente.

Esto permite reconstruir por qué el sistema mostró una prioridad determinada.

## 9. Validación y backtesting

Antes de fijar pesos o umbrales se utilizarán incendios históricos documentados de Córdoba.

Para cada caso se reconstruirá, en la medida en que los datos históricos lo permitan:

1. información que habría estado disponible en ese momento;
2. condiciones territoriales;
3. población y elementos expuestos;
4. capacidad de respuesta conocida o documentada;
5. evolución observada;
6. impactos ambientales y sociales posteriores.

El objetivo no es demostrar retrospectivamente que el sistema “adivinaba” el incendio, sino evaluar si habría identificado correctamente prioridades, brechas y riesgos relevantes.

### 9.1 Métricas preliminares

- sensibilidad para detectar situaciones posteriormente críticas;
- tasa de alertas injustificadas;
- estabilidad ante pequeñas variaciones de datos;
- concordancia con evaluaciones expertas;
- porcentaje de recomendaciones trazables a evidencia;
- porcentaje de casos donde datos faltantes fueron correctamente señalados.

### 9.2 Análisis de sensibilidad

Los pesos y funciones candidatas se someterán a perturbaciones sistemáticas. Si pequeños cambios producen saltos grandes e injustificados de categoría, el modelo deberá revisarse.

### 9.3 Tres sigma

El criterio de tres sigma podrá explorarse únicamente para variables con distribución empírica suficientemente caracterizada y cuando la distribución lo justifique. No se utilizará como regla universal ni para forzar normalidad en variables territoriales que no la presentan.

## 10. Criterio ASG/ESG adaptado a función pública

La plataforma adopta ASG como lente transversal, no como puntuación corporativa:

- **Ambiental:** ecosistemas, agua, suelo, biodiversidad, emisiones, restauración y resiliencia;
- **Social:** población expuesta, salud, accesibilidad, servicios esenciales, grupos y territorios vulnerables;
- **Gobernanza:** competencias, coordinación, trazabilidad, calidad de datos, uso de recursos, rendición de cuentas y evidencia de la decisión.

No se sumarán A+S+G para producir una nota decorativa. Se utilizarán para comprobar que la decisión no omita dimensiones esenciales.

## 11. Límites

La metodología no:

- predice con certeza la evolución del incendio;
- sustituye al Comando del Incidente ni a organismos especializados;
- inventa recursos disponibles;
- convierte correlaciones históricas en causalidad;
- extrapola modelos extranjeros sin validación local;
- utiliza un buen promedio para ocultar una condición crítica;
- transforma automáticamente una recomendación en una orden.

## 12. Estado de desarrollo

Esta versión define la arquitectura matemática mínima. Los pesos, umbrales, banderas y funciones de normalización permanecen **candidatos a validación** hasta completar evidencia, consulta experta y backtesting con casos de Córdoba.

El objetivo metodológico es conservar una plataforma simple en su uso, pero rigurosa en su interior: **menos números sin contexto y más decisiones explicables, territoriales y responsables**.
