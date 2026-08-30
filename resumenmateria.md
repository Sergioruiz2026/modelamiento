
# 📚 Resumen — Levantamiento y análisis de requerimientos

## 📋 Índice de contenidos

1. [Unidad 1: Requerimientos y UML](#unidad-1-requerimientos-y-uml)
2. [Unidad 2: Casos de uso y modelo de datos](#unidad-2-casos-de-uso-y-modelo-de-datos)
3. [Unidad 3: Flujo, interfaz y planificación](#unidad-3-flujo-interfaz-y-planificación)

---

# Unidad 1: Requerimientos y UML

## Enfoque de la asignatura

Durante el semestre se trabaja como si fuéramos una consultora informática contratada por un cliente.

**El objetivo no es programar, sino:**
- Entender qué necesita el cliente
- Levantar y analizar los requerimientos
- Definir qué debe construir el sistema
- Documentar la solución
- Elaborar modelos y diagramas UML
- Diseñar bocetos de interfaz y procesos

La asignatura trabaja con un mismo proyecto durante las tres unidades, agregando nuevas capas en cada etapa.

### Objetivos de la Unidad 1

- Realizar una toma de requerimientos
- Analizar los resultados obtenidos
- Elaborar diagramas de casos de uso
- Elaborar un modelo de datos
- Elaborar diagramas de flujo
- Estructurar el informe y el Kanban

La evaluación de esta unidad considera principalmente el informe de requerimientos y modelado UML.

---

## Qué es un requerimiento

Un requerimiento describe una necesidad que el sistema debe satisfacer.

Puede indicar:
- Qué debe hacer el sistema
- Quién realiza una acción
- En qué situación se realiza
- Qué condiciones debe cumplir

**Ejemplo:**  
El sistema deberá permitir registrar un pedido indicando cliente, dirección y productos solicitados.

Lo importante es que el requerimiento sea claro, específico y verificable.

---

## Tipos de requerimientos

### Requerimientos funcionales

Indican qué debe hacer el sistema.

**Ejemplos:** Registrar pedidos, Asignar repartidores, Consultar estado de pedidos, Generar liquidaciones

### Requerimientos no funcionales

Indican cómo debe funcionar el sistema o qué características debe cumplir.

**Ejemplos:** Seguridad, Rendimiento, Disponibilidad, Usabilidad, Compatibilidad

---

## Levantamiento de requerimientos

El levantamiento consiste en obtener información directamente del cliente o de otras fuentes para comprender sus necesidades reales.

### Principales técnicas

| Técnica | ¿Qué aporta? |
|---------|-------------|
| Entrevista | Permite conocer detalles y problemas del negocio |
| Cuestionario | Permite obtener información de varias personas |
| Observación | Permite conocer cómo se realiza realmente un proceso |
| Análisis documental | Permite revisar formularios, reglas y documentos |
| Prototipo | Ayuda a hacer más concreta una idea |

👉 **Importante:** Ninguna técnica es suficiente por sí sola. Lo recomendable es combinar al menos dos técnicas y comparar los resultados.

### Cómo realizar una entrevista

**Antes:**
- Definir qué información se necesita
- Revisar documentos existentes
- Preparar preguntas abiertas
- Organizar el tiempo

**Durante:**
- Preguntar primero por el proceso actual, no por la solución
- Pedir ejemplos concretos
- Preguntar por situaciones excepcionales
- Utilizar y registrar el vocabulario del cliente

---

## Análisis de requerimientos

Después de levantar información, hay que analizarla.

Analizar significa transformar lo que dijo el cliente en información organizada y útil para construir el sistema.

### Principales tareas

- Clasificar los requerimientos
- Detectar duplicados o contradicciones
- Identificar información que falta
- Priorizar los requerimientos
- Definir criterios que permitan comprobar si se cumplen
- Establecer la trazabilidad entre necesidades y solución

---

## Criterios y herramientas de análisis

### Método MoSCoW

Sirve para priorizar requerimientos.

| Prioridad | Significado | Ejemplo |
|-----------|------------|---------|
| **MUST** | Obligatorio | Registrar y asignar un pedido |
| **SHOULD** | Importante, pero existe alternativa | Consultar estado del pedido |
| **COULD** | Deseable | Reporte de rentabilidad |
| **WON'T** | No se realizará en esta versión | Optimización de rutas |

**Para recordarlo:** MUST = Tiene que estar | SHOULD = Debería estar | COULD = Sería bueno tenerlo | WON'T = No estará ahora

### Criterios de aceptación

Un requerimiento debe poder comprobarse con un formato:

> **Dado** una situación inicial,  
> **cuando** ocurre una acción,  
> **entonces** el sistema debe producir un resultado determinado.

### Matriz de trazabilidad

Permite relacionar cada requerimiento con su identificador, descripción, origen y prioridad.

| ID | Requerimiento | Origen | Prioridad |
|----|---------------|--------|-----------|
| RF-01 | Registrar pedido | Entrevista | MUST |
| RF-04 | Listar repartidores disponibles | Entrevista | MUST |
| RF-10 | Consultar estado del pedido | Entrevista | SHOULD |
| RF-11 | Generar liquidación quincenal | Regla de negocio | MUST |

### Del requerimiento al modelo

**Lo que se obtiene durante el levantamiento alimenta directamente los diagramas posteriores.**

| Información obtenida | Se utiliza para |
|----------------------|-----------------|
| Verbos + quién ejecuta la acción | Casos de uso |
| Sustantivos + información que se almacena | Modelo de datos |
| Secuencias y decisiones | Diagrama de flujo |
| Tareas que debe realizar el usuario | Bocetos de interfaz |

---

# Unidad 2: Casos de uso y modelo de datos

## Introducción a UML

UML (Unified Modeling Language) es un lenguaje estándar para representar y documentar sistemas mediante diagramas.

**No es:** Un lenguaje de programación, Un programa, Una base de datos

En esta asignatura UML se utiliza principalmente para modelar y comunicar la solución antes de programarla.

### Objetivo de la Unidad 2

Transformar los requerimientos obtenidos en modelos formales:
- **Diagrama de casos de uso:** muestra qué hace el sistema y quién lo utiliza
- **Modelo de datos:** muestra qué información necesita guardar el sistema y cómo se relaciona

```
Requerimientos → Casos de uso + Modelo de datos
```

---

## Diagrama de casos de uso

### Concepto fundamental

Un caso de uso representa una funcionalidad u objetivo que un usuario puede realizar utilizando el sistema.

**¿Quién utiliza el sistema y qué puede hacer con él?**

### Elementos principales

- **Actor:** persona, organización o sistema externo que interactúa con el sistema
- **Caso de uso:** funcionalidad que ofrece el sistema
- **Frontera del sistema:** delimita qué pertenece al sistema y qué es externo
- **Asociaciones:** conectan actores con casos de uso

---

## Identificación de actores y casos de uso

### Cómo identificar actores

¿Quién utiliza el sistema diariamente? ¿Quién administra o mantiene el sistema? ¿Qué otros sistemas intercambian información? ¿Quién recibe información del sistema aunque no lo opere directamente?

👉 **Importante:** Los actores son externos al sistema.

### Cómo nombrar un caso de uso

Debe representar una acción u objetivo, normalmente usando: **Verbo + objeto**

**Ejemplos correctos:** Registrar pedido, Asignar repartidor, Consultar estado del pedido, Generar liquidación

❌ **No como pantallas:** "Pantalla de pedidos"

---

## Relaciones en casos de uso

### Include (<<include>>)

Se utiliza cuando un comportamiento es obligatorio y reutilizado por otro caso de uso.

```
Registrar pedido → <<include>> → Validar datos
```

### Extend (<<extend>>)

Se utiliza cuando un comportamiento es opcional o depende de una condición.

```
Consultar pedido ← <<extend>> ← Solicitar notificación
```

### Errores frecuentes

❌ Modelar navegación entre pantallas
❌ Crear un caso de uso para cada operación CRUD
❌ Poner actores dentro de la frontera del sistema
❌ Usar flechas en asociación actor–caso de uso
❌ Representar orden temporal en el diagrama
❌ Encadenar casos de uso como diagrama de flujo

**Recuerda:** El caso de uso muestra objetivos, no pantallas ni secuencias.

### Especificación textual

El diagrama muestra qué existe, la especificación textual explica cómo funciona.

**Contiene:** Identificador, Actor principal, Precondición, Flujo principal, Flujos alternativos, Postcondición, Requerimientos relacionados

**Ejemplo:**

**CU-02 — Asignar repartidor**
- **Actor:** Coordinador de operaciones
- **Precondición:** Existe un pedido recibido
- **Flujo:**
  1. Coordinador selecciona un pedido
  2. Sistema muestra repartidores disponibles
  3. Coordinador selecciona un repartidor
  4. Sistema asigna el pedido y notifica al repartidor
- **Postcondición:** El pedido queda asignado

---

## Modelo de datos

### Concepto fundamental

El modelo de datos representa: **¿Qué información necesita almacenar el sistema y cómo se relaciona?**

Se parte de los sustantivos de los requerimientos.

### Clase, atributos y operaciones

Para modelar datos, interesa principalmente:
- **Entidades + atributos + relaciones + claves**

### Multiplicidad

Indica cuántos elementos pueden relacionarse entre sí.

| Multiplicidad | Significado |
|---------------|------------|
| 1 | Exactamente uno |
| 0..1 | Cero o uno |
| 1..* | Uno o varios |
| 0..* | Cero o varios |

### Tres niveles del modelo de datos

**Nivel 1 — Conceptual:** Entidades + Relaciones (sin tipos de datos ni claves)

**Nivel 2 — Lógico:** Agrega Atributos + Claves primarias + Claves foráneas + Normalización

**Nivel 3 — Físico:** Tablas + Tipos de datos + Índices + Restricciones

👉 **Para recordar:** Conceptual = qué existe | Lógico = cómo se organiza | Físico = cómo se implementa

### Claves primarias y foráneas

**Clave primaria (PK):** Identifica de manera única un registro

**Clave foránea (FK):** Permite relacionar una tabla con otra

### Relaciones 1:N y N:N

**Relación 1:N:** Un elemento se relaciona con muchos elementos (la FK se coloca en el lado N)

**Relación N:N:** Muchos elementos se relacionan con muchos elementos
- Se crea una tabla intermedia: `Pedido → DetallePedido ← Producto`

### Normalización

Busca organizar correctamente los datos para:
- Evitar información repetida
- Evitar inconsistencias
- Facilitar la actualización
- Mantener información ordenada

---

# Unidad 3: Flujo, interfaz y planificación

## Diagrama de flujo

Un diagrama de flujo representa la secuencia de pasos de un proceso, incluyendo decisiones y diferentes caminos.

### Pasos antes de dibujarlo

1. Analizar el proceso
2. Escribir la secuencia de pasos
3. Identificar decisiones
4. Definir qué ocurre cuando la respuesta es Sí o No
5. Construir el diagrama

### Símbolos principales

| Símbolo | Significado |
|---------|------------|
| ⭕ | Inicio o fin |
| ▭ | Proceso o acción |
| ▭ | Entrada/Salida |
| ◇ | Decisión o condición |
| 📄 | Documento |
| ⊗ | Conector |

⭐ **Una decisión debe tener diferentes salidas (Sí/No) y cada camino debe continuar hasta llegar nuevamente al flujo o terminal.**

### Errores frecuentes

❌ Utilizar rombo sin decisión real
❌ Dejar símbolos sin salida
❌ No etiquetar salidas de decisión
❌ Mezclar diferentes niveles de detalle

**El flujo debe mantenerse en un nivel coherente.**

### Diagrama de actividad UML

Alternativa que permite organizar actividades en calles (swimlanes) según quién realiza cada acción.

```
Cliente | Sistema | Coordinador
```

---

## Bocetos de interfaz

Después de definir casos de uso, se diseñan las pantallas necesarias.

```
Caso de uso → Tarea → Pantalla
```

### Wireframe, mockup y prototipo

| Concepto | ¿Qué representa? |
|----------|-----------------|
| **Wireframe** | Estructura y distribución de pantalla |
| **Mockup** | Diseño visual más completo |
| **Prototipo** | Permite navegar entre pantallas |

### Wireframe se concentra en

- Qué elementos tendrá la pantalla
- Dónde estarán ubicados
- Campos, botones, menús, información

### Relación entre modelo de datos e interfaz

**Los campos de la pantalla deben estar relacionados con los atributos del modelo de datos.**

**Regla para recordar:**
```
Atributos → Campos de pantalla
Casos de uso → Acciones/Botones
```

---

## Kanban y planificación

Kanban es una herramienta para planificar y controlar el trabajo mediante un tablero visual.

```
Pendiente → En proceso → En revisión → Terminado
```

Cada requerimiento se transforma en una tarjeta: `RF-01 — Registrar pedido`

### Límite de trabajo en curso (WIP)

Indica cuántas tareas pueden estar simultáneamente en una columna.

```
En proceso — WIP: 2
```

Significa máximo 2 tarjetas trabajando al mismo tiempo en esa columna.

### Políticas y métricas

**Política:** Una tarea pasa a "Terminado" cuando fue revisada y cumple los criterios de aceptación

**Métricas:**
- **Tiempo de ciclo:** Tiempo desde que una tarea comienza hasta que termina
- **Rendimiento:** Cantidad de tareas terminadas durante un período

---

## Evaluación sumativa

### Evaluación Sumativa Nº 1: 20 % — Informe de requerimientos y modelado UML

| Criterio | Qué se evalúa |
|----------|---------------|
| 1.1.1 | Toma de requerimientos |
| 1.1.2 | Análisis de requerimientos |
| 1.1.3 | Diagrama de casos de uso |
| 1.1.4 | Diagrama de base de datos |
| 1.1.5 | Diagrama de flujo |
| 1.1.6 | Informe estructurado + Kanban |

### La lógica completa de la Unidad 1

**Clase 1:** Cliente → Levantamiento → Requerimientos → Análisis

**Clase 2:** Requerimientos → Casos de uso + Modelo de datos

**Clase 3:** Casos de uso + Modelo de datos → Flujo + Interfaz + Kanban

**Resultado final:** Todo → Informe final

---

## 🎯 Lo más importante para recordar

### 🔄 Diagrama de flujo
Representa cómo se desarrolla un proceso.

### 🖥️ Interfaz
Los campos vienen del modelo de datos y las acciones vienen de los casos de uso.

### 📋 Kanban
Cada requerimiento puede convertirse en una tarjeta y debe existir un flujo de trabajo con límites WIP.

### 📄 Informe
Debe demostrar los seis criterios de evaluación, no solamente contener diagramas.

---

## 🎯 Idea central de toda la Unidad 1

> **"Modelar no consiste en dibujar: consiste en decidir qué se construye y qué queda fuera."**

Cada elemento del informe debe poder justificarse a partir de los requerimientos y necesidades del cliente.

---

## 🧠 Resumen ultra corto

- Los **requerimientos** dicen qué necesita el cliente
- Los **casos de uso** muestran qué puede hacer cada actor
- El **modelo de datos** muestra qué información guardar el sistema
- El **diagrama de flujo** describe cómo funcionan los procesos
- Los **bocetos de interfaz** muestran las pantallas necesarias
- El **Kanban** organiza y controla el trabajo

1. [Unidad 1: Requerimientos y UML](#unidad-1-requerimientos-y-uml)
   - [Enfoque de la asignatura](#enfoque-de-la-asignatura)
   - [Qué es un requerimiento](#qué-es-un-requerimiento)
   - [Tipos de requerimientos](#tipos-de-requerimientos)
   - [Levantamiento de requerimientos](#levantamiento-de-requerimientos)
   - [Análisis de requerimientos](#análisis-de-requerimientos)
   - [Criterios y herramientas de análisis](#criterios-y-herramientas-de-análisis)

2. [Unidad 2: Casos de uso y modelo de datos](#unidad-2-casos-de-uso-y-modelo-de-datos)
   - [Introducción a UML](#introducción-a-uml)
   - [Diagrama de casos de uso](#diagrama-de-casos-de-uso)
   - [Identificación de actores y casos de uso](#identificación-de-actores-y-casos-de-uso)
   - [Relaciones en casos de uso](#relaciones-en-casos-de-uso)
   - [Modelo de datos](#modelo-de-datos)

3. [Unidad 3: Flujo, interfaz y planificación](#unidad-3-flujo-interfaz-y-planificación)
   - [Diagrama de flujo](#diagrama-de-flujo)
   - [Bocetos de interfaz](#bocetos-de-interfaz)
   - [Kanban y planificación](#kanban-y-planificación)
   - [Evaluación sumativa](#evaluación-sumativa)

---

# Unidad 1: Requerimientos y UML

## Enfoque de la asignatura

Durante el semestre se trabaja como si fuéramos una consultora informática contratada por un cliente.

El objetivo no es programar, sino:

Entender qué necesita el cliente.
Levantar y analizar los requerimientos.
Definir qué debe construir el sistema.
Documentar la solución.
Elaborar modelos y diagramas UML.
Diseñar bocetos de interfaz y procesos.

La asignatura trabaja con un mismo proyecto durante las tres unidades, agregando nuevas capas en cada etapa.

### Objetivos de la Unidad 1

En la Unidad 1 se debe aprender a:
- Realizar una toma de requerimientos
- Analizar los resultados obtenidos
- Elaborar diagramas de casos de uso
- Elaborar un modelo de datos
- Elaborar diagramas de flujo
- Estructurar el informe y el Kanban

La evaluación de esta unidad considera principalmente el informe de requerimientos y modelado UML.

---

## Qué es un requerimiento

Un requerimiento describe una necesidad que el sistema debe satisfacer.

Puede indicar:
- Qué debe hacer el sistema
- Quién realiza una acción
- En qué situación se realiza
- Qué condiciones debe cumplir

### Ejemplo

El sistema deberá permitir registrar un pedido indicando cliente, dirección y productos solicitados.

Lo importante es que el requerimiento sea claro, específico y verificable.

---

## Tipos de requerimientos
   Requerimientos funcionales

Indican qué debe hacer el sistema.

**Ejemplos:**
- Registrar pedidos
- Asignar repartidores
- Consultar estado de pedidos
- Generar liquidaciones

### Requerimientos no funcionales

Indican cómo debe funcionar el sistema o qué características debe cumplir.

**Ejemplos:**
- Seguridad
- Rendimiento
- Disponibilidad
- Usabilidad
- Compatibilidad

---

## Levantamiento de requerimientos

El levantamiento consiste en obtener información directamente del cliente o de otras fuentes para comprender sus necesidades reales.

Principales técnicas
Técnica	¿Qué aporta?
Entrevista	Permite conocer detalles y problemas del negocio
Cuestionario	Permite obtener información de varias personas
Observación	Permite conocer cómo se realiza realmente un proceso
Análisis documental	Permite revisar formularios, reglas y documentos
Prototipo	Ayuda a hacer más concreta una idea

👉 Importante: ninguna técnica es suficiente por sí sola. Lo recomendable es combinar al menos dos técnicas y comparar los resultados.

6. 👤 ¿Cómo realizar una entrevista?
   Antes
   Definir qué información se necesita.
   Revisar documentos existentes.
   Preparar preguntas abiertas.
   Organizar el tiempo.
   Durante
   Preguntar primero por el proceso actual, no por la solución.
   Pedir ejemplos concretos.
   Preguntar por situaciones excepcionales.
   Utilizar y registrar el vocabulario del cliente.


Después de levantar información, hay que analizarla.

Analizar significa transformar lo que dijo el cliente en información organizada y útil para construir el sistema.

### Principales tareas

- Clasificar los requerimientos
- Detectar duplicados o contradicciones
- Identificar información que falta
- Priorizar los requerimientos
- Definir criterios que permitan comprobar si se cumplen
- Establecer la trazabilidad entre necesidades y solución

---

## Criterios y herramientas de análisis

Sirve para priorizar requerimientos.

Prioridad	Significado	Ejemplo
MUST	Obligatorio	Registrar y asignar un pedido
SHOULD	Importante, pero existe alternativa	Consultar estado del pedido
COULD	Deseable	Reporte de rentabilidad
WON'T	No se realizará en esta versión	Optimización de rutas
Para recordarlo fácilmente:

MUST = Tiene que estar
SHOULD = Debería estar
COULD = Sería bueno tenerlo
WON'T = No estará ahora

9. ✅ Criterios de aceptación

Un requerimiento debe poder comprobarse.

Una forma de expresarlo es:

Dado una situación inicial,
cuando ocurre una acción,
entonces el sistema debe producir un resultado determinado.

Esto permite saber objetivamente si el requerimiento está cumplido.

10. 🔗 Matriz de trazabilidad

Permite relacionar cada requerimiento con:

Su identificador.
La descripción.
Su origen.
Su prioridad.

Ejemplo:

ID	Requerimiento	Origen	Prioridad
RF-01	Registrar pedido	Entrevista	MUST
RF-04	Listar repartidores disponibles	Entrevista	MUST
RF-10	Consultar estado del pedido	Entrevista	SHOULD
RF-11	Generar liquidación quincenal	Regla de negocio	MUST

La trazabilidad ayuda a demostrar de dónde salió cada requerimiento y por qué existe.

11. 🏗️ Del requerimiento al modelo

Esta es una de las ideas más importantes de la clase:

Lo que se obtiene durante el levantamiento alimenta directamente los diagramas posteriores.

Información obtenida	Se utiliza para
Verbos + quién ejecuta la acción	Casos de uso
Sustantivos + información que se almacena	Modelo de datos
Secuencias y decisiones	Diagrama de flujo
Tareas que debe realizar el usuario	Bocetos de interfaz

Por eso, si el requerimiento está mal definido, los diagramas también pueden quedar mal.



📚 Resumen Clase 2 — Casos de uso y modelo de datos
🎯 Objetivo de la clase

La idea principal es transformar los requerimientos obtenidos en la clase anterior en modelos formales:

Diagrama de casos de uso: muestra qué hace el sistema y quién lo utiliza.
Modelo de datos: muestra qué información necesita guardar el sistema y cómo se relaciona.

La secuencia sería:

Requerimientos → Casos de uso + Modelo de datos

1. UML

UML (Unified Modeling Language) es un lenguaje estándar para representar y documentar sistemas mediante diagramas.

No es:

Un lenguaje de programación.
Un programa.
Una base de datos.

En esta asignatura UML se utiliza principalmente para modelar y comunicar la solución antes de programarla.

2. 👤 Diagrama de casos de uso

Un caso de uso representa una funcionalidad u objetivo que un usuario puede realizar utilizando el sistema.

Responde principalmente a:

¿Quién utiliza el sistema y qué puede hacer con él?

Elementos principales
Actor: persona, organización o sistema externo que interactúa con el sistema.
Caso de uso: funcionalidad que ofrece el sistema.
Frontera del sistema: delimita qué pertenece al sistema y qué es externo.
Asociaciones: conectan actores con casos de uso.
Ejemplo

Actor: Coordinador de operaciones
Caso de uso: Asignar repartidor

3. 👥 ¿Cómo identificar actores?

Hay que preguntarse:

¿Quién utiliza el sistema diariamente?
¿Quién administra o mantiene el sistema?
¿Qué otros sistemas intercambian información?
¿Quién recibe información del sistema aunque no lo opere directamente?

👉 Importante: los actores son externos al sistema.

4. ✏️ ¿Cómo nombrar un caso de uso?

Debe representar una acción u objetivo, normalmente usando:

Verbo + objeto

Ejemplos:

Registrar pedido.
Asignar repartidor.
Consultar estado del pedido.
Generar liquidación.

❌ No conviene nombrarlos como pantallas:

"Pantalla de pedidos"

Porque un caso de uso representa lo que el usuario quiere lograr, no una ventana de la aplicación.

5. 🔗 Include y Extend
   <<include></include>>

Se utiliza cuando un comportamiento es obligatorio y reutilizado por otro caso de uso.

Ejemplo:

Registrar pedido
→ <<include></include>> → Validar datos

La validación forma parte obligatoria del proceso.

<<extend></extend>>

Se utiliza cuando un comportamiento es opcional o depende de una condición.

Ejemplo:

Consultar pedido
← <<extend></extend>> ← Solicitar notificación

👉 Para la evaluación es importante justificar por qué se utiliza include o extend.

6. ⚠️ Errores frecuentes en casos de uso

No hay que:

❌ Modelar la navegación entre pantallas.
❌ Crear un caso de uso para cada operación CRUD.
❌ Poner los actores dentro de la frontera del sistema.
❌ Usar flechas en la asociación actor–caso de uso.
❌ Representar el orden temporal de las acciones en el diagrama.
❌ Encadenar casos de uso como si fuera un diagrama de flujo.

Recuerda:

El caso de uso muestra objetivos, no pantallas ni secuencias.

7. 📄 Especificación textual

El diagrama muestra qué existe, pero la especificación textual explica cómo funciona el caso de uso.

Normalmente contiene:

Identificador.
Actor principal.
Precondición.
Flujo principal.
Flujos alternativos o excepciones.
Postcondición.
Requerimientos relacionados.
Ejemplo

CU-02 — Asignar repartidor

Actor: Coordinador de operaciones.

Precondición: Existe un pedido recibido.

Flujo:

El coordinador selecciona un pedido.
El sistema muestra repartidores disponibles.
El coordinador selecciona un repartidor.
El sistema asigna el pedido y notifica al repartidor.

Postcondición: El pedido queda asignado.

8. 🔗 Matriz de trazabilidad

En esta clase la matriz incorpora una nueva columna:

Requerimiento → Caso de uso

Ejemplo:

ID	Requerimiento	Prioridad	Caso de uso
RF-01	Registrar pedido	MUST	CU-01
RF-04	Listar repartidores	MUST	CU-02
RF-10	Consultar estado	SHOULD	CU-05
RF-13	Reporte de rentabilidad	COULD	—

Esto permite comprobar que los casos de uso realmente vienen de los requerimientos levantados.

9. 🗄️ Modelo de datos

El modelo de datos representa:

¿Qué información necesita almacenar el sistema y cómo se relaciona?

Para construirlo se parte de los sustantivos de los requerimientos.

Por ejemplo:

"El coordinador registra un pedido para un comercio y asigna un repartidor."

Podemos identificar entidades como:

Pedido.
Comercio.
Repartidor.
10. 📦 Clase, atributos y operaciones

En un diagrama de clases normalmente encontramos:

1. Nombre

Ejemplo:

Pedido

2. Atributos

Ejemplo:

idPedido
fecha
estado
dirección
3. Operaciones

Ejemplo:

registrar()
actualizarEstado()

Pero cuando se utiliza UML para modelar datos, normalmente interesa principalmente:

Entidades + atributos + relaciones + claves.

11. 🔢 Multiplicidad

La multiplicidad indica cuántos elementos pueden relacionarse entre sí.

Multiplicidad	Significado
1	Exactamente uno
0..1	Cero o uno
1..*	Uno o varios
0..*	Cero o varios
Ejemplo

Un pedido puede tener 0 o 1 repartidor:

Pedido 0..1 → Repartidor

Un pedido debe contener uno o más productos:

Pedido 1.. → Producto*

12. 🏗️ Tres niveles del modelo de datos
    Nivel 1 — Conceptual

Muestra:

Entidades.
Relaciones.

No se preocupa todavía de tipos de datos o claves.

Nivel 2 — Lógico

Agrega:

Atributos.
Claves primarias.
Claves foráneas.
Normalización.
Nivel 3 — Físico

Define aspectos específicos de la base de datos:

Tablas.
Tipos de datos.
Índices.
Restricciones.

👉 Para recordar:

Conceptual = qué existe
Lógico = cómo se organiza
Físico = cómo se implementa

13. 🔑 Claves primarias y foráneas
    Clave primaria (PK)

Identifica de manera única un registro.

Ejemplo:

Pedido

idPedido ← PK
Clave foránea (FK)

Permite relacionar una tabla con otra.

Ejemplo:

Pedido

idPedido ← PK
idComercio ← FK

idComercio indica a qué comercio pertenece el pedido.

14. 🔄 Relaciones 1:N y N:N
    Relación 1:N

Un elemento se relaciona con muchos elementos.

Ejemplo:

Un comercio → muchos pedidos

La clave foránea se coloca en el lado N.

Relación N:N

Muchos elementos se relacionan con muchos elementos.

Ejemplo:

Un pedido contiene muchos productos y un producto puede aparecer en muchos pedidos.

No se deja directamente como N:N en una base de datos relacional.

Se crea una tabla intermedia:

Pedido → DetallePedido ← Producto

15. 📋 ¿Qué es DetallePedido?

La tabla intermedia no solamente sirve para conectar las entidades.

También puede guardar información propia de la relación.

Por ejemplo:

DetallePedido

idPedido
idProducto
cantidad
precio

La cantidad y el precio al momento de la venta pertenecen al detalle de esa relación.

Esto es importante porque el precio podría cambiar posteriormente, pero el pedido debe conservar el precio histórico.

16. 🧹 Normalización

La normalización busca organizar correctamente los datos para:

Evitar información repetida.
Evitar inconsistencias.
Facilitar la actualización.
Mantener la información ordenada.

Por ejemplo, si una Zona tiene información propia, es mejor tener una entidad Zona que repetir los mismos datos como texto en muchos registros.

⭐ Lo más importante para estudiar

Si tienes que preparar una prueba o tu informe, recuerda estas ideas:

Casos de uso

Actor + Caso de uso + Sistema

Actor = quién utiliza o interactúa.
Caso de uso = qué objetivo realiza.
Sistema = frontera que contiene las funcionalidades.
Modelo de datos

Entidades + atributos + relaciones + multiplicidades + claves

🧠 Resumen ultra corto

Los requerimientos dicen qué necesita el cliente.
Los casos de uso muestran qué puede hacer cada actor con el sistema.
El modelo de datos muestra qué información debe guardar el sistema y cómo se relaciona.

Y la transformación principal de esta clase es:

Requerimientos → Verbos → Casos de uso

Requerimientos → Sustantivos → Entidades

Entidades → Atributos + Relaciones + Claves → Modelo de datos



Resumen Clase 3 — Flujo, interfaz y planificación
🎯 Objetivo de la clase

La tercera clase busca completar la propuesta de solución utilizando tres elementos:

Diagrama de flujo → representa cómo funciona un proceso.
Bocetos de interfaz → muestran cómo serán las pantallas.
Kanban → permite planificar y controlar el trabajo.

Todo esto finalmente se incorpora al informe de la Evaluación Sumativa N.º 1.

1. 🔄 Diagrama de flujo

Un diagrama de flujo representa la secuencia de pasos de un proceso, incluyendo decisiones y diferentes caminos.

Antes de dibujarlo

Primero hay que:

Analizar el proceso.
Escribir la secuencia de pasos.
Identificar decisiones.
Definir qué ocurre cuando la respuesta es Sí o No.
Después recién construir el diagrama.
🔷 Símbolos principales
Símbolo	Significado
Terminal	Inicio o fin
Proceso	Acción o transformación
Entrada/Salida	Datos que entran o salen
Decisión	Pregunta o condición
Documento	Informe o comprobante
Conector	Unión entre secciones
⭐ Regla importante

Una decisión debe tener diferentes salidas, normalmente:

Sí / No

Y cada camino debe continuar hasta llegar nuevamente al flujo o a un terminal.

⚠️ Errores frecuentes

❌ Utilizar un rombo cuando no existe una decisión.
❌ Dejar símbolos sin salida.
❌ No etiquetar las salidas de una decisión.
❌ Mezclar diferentes niveles de detalle.

Por ejemplo, no conviene mezclar:

"El cliente solicita un pedido"

con:

"El sistema ejecuta una consulta SQL".

El flujo debe mantenerse en un nivel coherente.

2. 🧩 Diagrama de actividad UML

Una alternativa al diagrama de flujo es el diagrama de actividad de UML.

La diferencia importante es que permite organizar las actividades en calles (swimlanes) según quién realiza cada acción.

Por ejemplo:

Cliente | Sistema | Coordinador

Esto ayuda a visualizar claramente quién hace cada paso.

3. 🖥️ Bocetos de interfaz

Después de definir los casos de uso, se pueden diseñar las pantallas que necesitará el sistema.

La idea es pasar de:

Caso de uso → Tarea → Pantalla

Wireframe, mockup y prototipo
Concepto	¿Qué representa?
Wireframe	Estructura y distribución de la pantalla
Mockup	Diseño visual más completo
Prototipo	Permite recorrer/navegar entre pantallas
📌 Wireframe

Se concentra en:

Qué elementos tendrá la pantalla.
Dónde estarán ubicados.
Campos.
Botones.
Menús.
Información.

No se preocupa todavía demasiado por colores o diseño visual.

4. 🔗 Relación entre modelo de datos e interfaz

Esta parte es muy importante para el informe.

Los campos de una pantalla deben estar relacionados con los atributos del modelo de datos.

Por ejemplo:

Si tienes la entidad:

Pedido

idPedido
fecha
estado
dirección

La pantalla de registro de pedido podría tener:

ID del pedido.
Fecha.
Estado.
Dirección.

Además, las acciones de la pantalla deben corresponder a los casos de uso.

Regla para recordar:

Atributos → Campos de pantalla

Casos de uso → Acciones/Botones

5. 📋 Kanban

Kanban es una herramienta para planificar y controlar el trabajo de un proyecto mediante un tablero visual.

Un tablero puede tener, por ejemplo:

Pendiente → En proceso → En revisión → Terminado

Cada requerimiento se transforma en una tarjeta.

Ejemplo:

RF-01 — Registrar pedido

6. 🚦 Límite de trabajo en curso (WIP)

El WIP (Work In Progress) indica cuántas tareas pueden estar simultáneamente en una columna.

Por ejemplo:

En proceso — WIP: 2

Significa que no deberían existir más de 2 tarjetas trabajando al mismo tiempo en esa columna.

👉 Esto es una característica importante que diferencia Kanban de un simple tablero de tareas.

7. 📊 Políticas y métricas

El tablero debe tener políticas explícitas, por ejemplo:

Una tarea pasa a "Terminado" cuando fue revisada y cumple los criterios de aceptación.

También se pueden utilizar métricas:

Tiempo de ciclo

Tiempo desde que una tarea comienza hasta que termina.

Rendimiento

Cantidad de tareas terminadas durante un determinado período.

8. 📄 Informe de la Evaluación Sumativa N.º 1

La evaluación corresponde a:

20 % — Informe de requerimientos y modelado UML.

Los criterios se distribuyen de esta manera:

Criterio	Qué se evalúa
1.1.1	Toma de requerimientos
1.1.2	Análisis de requerimientos
1.1.3	Diagrama de casos de uso
1.1.4	Diagrama de base de datos
1.1.5	Diagrama de flujo
1.1.6	Informe estructurado + Kanban
🧠 La lógica completa de la Unidad 1

Las tres clases están conectadas:

Clase 1

Cliente → Levantamiento → Requerimientos → Análisis

Clase 2

Requerimientos → Casos de uso + Modelo de datos

Clase 3

Casos de uso + Modelo de datos → Flujo + Interfaz + Kanban

Y finalmente:

Todo → Informe final

⭐ Lo más importante para recordar

Si tienes que estudiar para una prueba o revisar tu informe, recuerda estas reglas:

🔄 Diagrama de flujo

Representa cómo se desarrolla un proceso.

🖥️ Interfaz

Los campos vienen del modelo de datos y las acciones vienen de los casos de uso.

📋 Kanban

Cada requerimiento puede convertirse en una tarjeta y debe existir un flujo de trabajo con límites WIP.

📄 Informe

Debe demostrar los seis criterios de evaluación, no solamente contener diagramas.

🎯 Idea central de toda la Unidad 1

“Modelar no consiste en dibujar: consiste en decidir qué se construye y qué queda fuera.”

En otras palabras, los diagramas no se hacen porque sí. Cada elemento del informe debe poder justificarse a partir de los requerimientos y necesidades del cliente.
