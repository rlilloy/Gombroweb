# Gombro — Manual

*inventando palabras*

`v0.0.5-beta`

## Índice

1. [¿Qué es Gombro?](#capítulo-1--qué-es-gombro)
2. [Primeros pasos](#capítulo-2--primeros-pasos)
3. [El Editor](#capítulo-3--el-editor)
4. [La CmdBar](#capítulo-4--la-cmdbar)
5. [El Explorador](#capítulo-5--el-explorador)
6. [Búsqueda y Colecciones](#capítulo-6--búsqueda-y-colecciones)
7. [Versiones de párrafo](#capítulo-7--versiones-de-párrafo)
8. [Notas del proyecto](#capítulo-8--notas-del-proyecto)
9. [Baraja y cut-up](#capítulo-9--baraja-y-cut-up)
10. [Vista de Grafo](#capítulo-10--vista-de-grafo)
11. [Hashtags](#capítulo-11--hashtags)
12. [Importar y exportar](#capítulo-12--importar-y-exportar)
13. [Álgebra Borgiana](#capítulo-13b--álgebra-borgiana)
14. [El Diario](#capítulo-13c--el-diario)
15. [Modo Schrödinger](#capítulo-13d--modo-schrödinger)
16. [Plan de escritura](#capítulo-13e--plan-de-escritura)
17. [Notas de sesión y badges](#capítulo-13f--notas-de-sesión-y-badges)
18. [Filtro por hashtag](#capítulo-13g--filtro-por-hashtag-en-el-explorador)
19. [Escala de texto](#capítulo-13h--escala-de-texto)
20. [Libreta Obsidian](#capítulo-13i--libreta-obsidian)
21. [Respaldo y recuperación](#capítulo-13j--respaldo-y-recuperación)
22. [Flujo de trabajo recomendado](#capítulo-14--flujo-de-trabajo-recomendado)
23. [Atajos de teclado](#atajos-de-teclado)
24. [Sobre el autor](#sobre-el-autor)
25. [Índice Alfabético](#índice-alfabético)

---

## Capítulo 1 — ¿Qué es Gombro?

Gombro es una máquina de escribir centrada en una sola cosa: la invención humana de la palabra.

No la palabra pulida. No la palabra optimizada. La **palabra en movimiento** — siguiendo la deriva del pensamiento, el accidente del orden, la sorpresa de lo que viene después cuando nada se fuerza.

No hay IA aquí. Sin autocompletado, sin sugerencias, sin mano invisible dirigiendo tus frases hacia lo probable. Gombro es una herramienta enteramente al servicio del flujo del escritor.

Cada sesión de escritura en Gombro es una **improvisación de jazz** — una sesión en el sentido musical. Abrís el instrumento, tocás, parás. Lo que dejaste atrás es un registro de la sesión: crudo, vivo, recuperable.

### Los escritores que habrían usado Gombro

Gombro es el procesador de texto que Kafka habría usado para fragmentar sus diarios sin resolverlos. Que Jacques Vaché habría usado para cortar cartas que nunca envió. Que Gombrowicz habría usado para barajar capítulos hasta que la forma misma se volviera el argumento. Que Joyce habría usado para redactar Nighttown en ráfagas desconectadas y recombinarlas a las 3am. Que Néstor Sánchez habría usado para escribir *Siberia Blues* una astilla a la vez. Que Philip K. Dick habría usado para escribir *El hombre en el castillo* o *VALIS* — novelas donde la realidad misma se niega a mantenerse quieta.

### Lo que Gombro no es

- No es un procesador de texto para formateo final
- No es un gestor de proyectos con carpetas, estados o plazos
- No se conecta a la nube ni a ningún servicio externo
- **No contiene ninguna IA de ningún tipo**

### Los dos conceptos centrales

| Concepto | Qué es |
|----------|--------|
| **Proyecto** | Un contenedor para un cuerpo de trabajo — una novela, un ciclo de cuentos, un cuaderno |
| **Sesión** | Una improvisación dentro de un proyecto — una escena, un fragmento, una deriva |

---

## Capítulo 2 — Primeros pasos

### La interfaz de un vistazo

```
┌────────────────────────────────────────────────────────────┐
│  Gombro                                        [ES]  [?]   │
├──────────────────────┬─────────────────────────────────────┤
│                      │                                     │
│  EXPLORADOR          │  EDITOR                             │
│  ──────────          │  ─────────────────────────          │
│  Sesiones            │                                     │
│                      │   Seleccioná una sesión para        │
│  (vacío)             │   empezar a escribir.               │
│                      │                                     │
│  [+]  [↑]            │                                     │
└──────────────────────┴─────────────────────────────────────┘
```

```
  Cómo se conecta todo:

  ┌─────────────┐
  │   PROYECTO  │  ← tu cuerpo de trabajo (novela, ciclo, cuaderno)
  └──────┬──────┘
         │  contiene
    ┌────┴────┬────────┬─────────┐
    ▼         ▼        ▼         ▼
  Sesión   Sesión   Sesión    Sesión
    │         │
    │  contiene
    ▼
  Párrafo ── versión ── versión ── versión
    │
    ├── hashtag
    ├── destino de baraja
    └── nodo de grafo
```

### Paso 1 — Crear el primer proyecto

Presioná `:` para abrir la CmdBar y escribí:

```
crear proyecto Don Quijote
```

Presioná `Enter`. El proyecto se crea y queda activo.

### Paso 2 — Crear la primera sesión

Presioná `Ctrl+N`, o abrí la CmdBar y escribí:

```
nuevo Capítulo Uno
```

### Paso 3 — Empezar a escribir

Hacé clic en el área del Editor y empezá a escribir. Eso es todo.

### Cosas clave antes de seguir

| Qué | Cómo |
|-----|------|
| Abrir la CmdBar | `:` o `/` |
| Crear una sesión | `Ctrl+N` o `nuevo <nombre>` en la CmdBar |
| Abrir la ayuda | Botón `[?]`, `F1`, o `ayuda` en la CmdBar |
| Cambiar idioma | Chip `[ES]` en la barra superior o `lang en` en la CmdBar |
| Cerrar cualquier modal | `Esc` |

---

## Capítulo 3 — El Editor

El Editor es donde todo sucede. Es intencionalmente austero — sin barras de herramientas, sin botones de formato, sin reglas. Solo el texto y vos.

Cada bloque de texto separado por una línea en blanco es un **párrafo** — la unidad fundamental en Gombro. Los párrafos se guardan, versionan, barajan y etiquetan individualmente.

### Menú contextual

Hacé clic derecho en cualquier parte del editor:

```
┌─────────────────────────┐
│  Deshacer               │
│  ─────────────────────  │
│  Seleccionar todo       │
│  Cortar / Copiar / Pegar│
│  ─────────────────────  │
│  Insertar               │
│  Agregar variante       │
│  ─────────────────────  │
│  Mostrar en Binder      │
│  Barajar (Baraja)       │
│  Versiones de párrafo   │
└─────────────────────────┘
```

### Modo frase

Activalo con `modo frase` en la CmdBar. Cada `.` aísla la frase actual — de a una, el resto desaparece. Escribís, ponés punto, se bloquea y se abre la siguiente.

```
  MODO FRASE — solo una frase visible a la vez:

  ┌─────────────────────────────────────────────────────┐
  │  Capítulo Uno            [modo frase] [Selec. todo]  │
  ├─────────────────────────────────────────────────────┤
  │                                                     │
  │  · · · · · · · · · · · · · · · · · · · · · · · ·   │  ← bloqueada
  │                                                     │
  │  En un lugar de la Mancha, de cuyo nombre no        │
  │  quiero acordarme, no ha mucho que vivía...         │  ← activa
  │                                                     │
  │  · · · · · · · · · · · · · · · · · · · · · · · ·   │  ← bloqueada
  │                                                     │
  └─────────────────────────────────────────────────────┘

  escribís → punto [.] → se bloquea → se abre la siguiente
```

### Layout — tres paneles

Gombro tiene tres zonas permanentes:

```
  ┌────────┬───────────────────────────────────┐
  │EXPLOR. │            EDITOR                 │
  │        │                                   │
  │sesión1 │  texto...                         │
  │sesión2 │                                   │
  │sesión3 │                                   │
  │        │                                   │
  ├────────┴───────────────────────────────────┤
  │  :/                                        │  ← CmdBar / terminal
  └────────────────────────────────────────────┘
```

- **Explorador** (izquierda) — lista de sesiones del proyecto activo.
- **Editor** (centro/derecha) — área de escritura.
- **CmdBar** (abajo) — terminal de comandos. Abrila con `:` o `/`. Presioná `Ctrl+T` para la paleta flotante.

### Modo zen

Expande el editor a pantalla completa. Activalo con `zen` en la CmdBar, o presionando `Esc` en reposo.

```
  NORMAL                        ZEN
  ──────────────────────        ────────────────────────────────────────
  ┌────────┬───────────┐        ┌────────────────────────────────────────┐
  │EXPLOR. │  EDITOR   │   →    │                                        │
  │        │           │        │        En un lugar de la Mancha,       │
  │sesión1 │  texto... │        │        de cuyo nombre no quiero        │
  │sesión2 │           │        │        acordarme, no ha mucho que      │
  │sesión3 │           │        │        vivía un hidalgo...             │
  │        │           │        │                                        │
  ├────────┴───────────┤        └────────────────────────────────────────┘
  │  :/               │           sin paneles · sin chrome · solo la palabra
  └───────────────────┘
```

### Referencia de teclado

| Acción | Cómo |
|--------|------|
| Abrir CmdBar | `:` o `/` |
| Paleta flotante | `Ctrl+T` |
| Búsqueda flotante | `Ctrl+F` |
| Nueva sesión | `Ctrl+N` |
| Sesión del diario de hoy | `Ctrl+D` |
| Post-it de la sesión activa | `F4` |
| Ayuda | `F1` |
| Seleccionar todo | Botón `[Seleccionar todo]` o clic derecho |
| Activar Modo Frase | `modo frase` en CmdBar |
| Activar Modo Zen | `zen` en CmdBar · `Esc` en reposo |
| Cerrar CmdBar / búsqueda / activar Zen | `Esc` (en cascada) |

---

## Capítulo 4 — La CmdBar

Presioná `:` o `/` para abrir. `Esc` para cerrar. Todos los comandos funcionan en inglés y en español.

### Escritura

| Comando | Qué hace |
|---------|----------|
| `nuevo <nombre>` · `new <name>` | Crear una nueva sesión |
| `modo frase` · `sentence mode` | Activar/desactivar modo frase |
| `zen` | Activar/desactivar modo zen |

### Proyectos

| Comando | Qué hace |
|---------|----------|
| `crear proyecto <nombre>` | Crear un nuevo proyecto |
| `abrir` · `ver proyectos` | Ver la lista de proyectos |

### Búsqueda

| Comando | Qué hace |
|---------|----------|
| `buscar <término>` | Buscar en todas las sesiones |
| `buscar <término> en frases` | Búsqueda mostrando frases individuales |

### Exportar

| Comando | Qué hace |
|---------|----------|
| `compilar` · `compile` | Exportar todas las sesiones a .docx |
| `compilar <nombre>` | Exportar con nombre personalizado |

### Interfaz

| Comando | Qué hace |
|---------|----------|
| `ayuda` · `help` | Abrir el modal de ayuda |
| `lang es` · `lang en` | Cambiar idioma de la interfaz |

---

## Capítulo 5 — El Explorador

El Explorador es el panel izquierdo — tu lista de sesiones, tu binder. Cada sesión del proyecto activo vive aquí.

- `[+]` — crear una nueva sesión (al final de la lista)
- `[↑]` — importar un archivo (.md, .docx, .txt)
- Las estadísticas al pie muestran totales del proyecto activo

### Agregar sesión o párrafo en posición

Clic derecho en una sesión o en un párrafo del outline expandido para insertar contenido nuevo **exactamente debajo** del elemento clickeado:

| Gesto | Qué hace |
|-------|----------|
| Clic derecho en sesión → **Agregar sesión abajo** | Crea una sesión nueva inmediatamente debajo de esa sesión, lista para renombrar |
| Clic derecho en párrafo (outline) → **Agregar párrafo abajo** | Inserta un párrafo vacío debajo del párrafo seleccionado — aparece "nuevo párrafo" en el explorador hasta que escribís |

### Reordenar párrafos

En el outline expandido de una sesión podés reordenar párrafos con drag & drop, igual que las sesiones:

| Gesto | Qué hace |
|-------|----------|
| Arrastrar párrafo del outline → soltar en otra posición | Mueve el párrafo a esa posición, guarda en DB y recarga el editor |

### Navegar a un párrafo

| Gesto | Qué hace |
|-------|----------|
| Clic en párrafo del outline | El cursor del editor se posiciona en ese párrafo y titila listo para escribir |
| `Enter` en el editor | Crea un párrafo nuevo debajo del cursor (equivalente a "Agregar párrafo abajo") |

### Estadísticas del proyecto

| Estadística | Qué mide |
|-------------|----------|
| **Días** | Cuántos días escribiste en este proyecto |
| **Palabras** | Total de palabras en todas las sesiones |
| **Oraciones** | Total de oraciones |
| **Comas** | Proxy de complejidad y ritmo de las frases |

### Selección múltiple

En el Explorador podés seleccionar varias sesiones a la vez:

| Gesto | Qué hace |
|-------|----------|
| `Ctrl+clic` | Agrega o quita una sesión de la selección |
| `Shift+clic` | Selecciona el rango desde la última sesión clickeada hasta esta |
| `Delete` | Elimina todas las sesiones seleccionadas de una vez |

### Menú contextual de sesión

Clic derecho sobre cualquier sesión:

```
┌─────────────────────────┐
│  Agregar sesión abajo   │
│  ───────────────────    │
│  Renombrar              │
│  Duplicar               │
│  ───────────────────    │
│  Barajar (Abarajar)     │
│  Deshacer barajada      │
│  ───────────────────    │
│  Subir                  │
│  Bajar                  │
│  ───────────────────    │
│  Mover a <proyecto>     │
│  ───────────────────    │
│  Eliminar               │
└─────────────────────────┘
```

**Subir / Bajar** — reordenar sesiones dentro del proyecto. El orden persiste. También podés **arrastrar y soltar** sesiones directamente en la lista.

---

## Capítulo 6 — Búsqueda y Colecciones

La búsqueda recorre el texto completo de cada párrafo en el proyecto activo.

```
buscar hidalgo
```

Usá el modo frase para resultados a nivel de oración:

```
buscar hidalgo en frases
```

### Colecciones

Una Colección es una búsqueda guardada. Después de cualquier búsqueda, hacé clic en **+ Guardar como colección**. Ponele nombre, guardala, y aparece en el Explorador — un clic para volver a ejecutarla.

```
  ┌──────────────────────┐
  │  Sesiones      [↑]   │
  │  ────────────────    │
  │  La Mancha           │
  │  El Caballero        │
  │  Olla y Renta        │
  │  El Ama              │
  │  ────────────────    │
  │  COLECCIONES         │  ← búsquedas guardadas, siempre a un clic
  │  ▸ El arco del hidalgo│
  │  ▸ Comida e ingresos  │
  │  ▸ Debate de nombres  │
  └──────────────────────┘
```

---

## Capítulo 7 — Versiones de párrafo

Cada vez que un párrafo cambia, Gombro guarda una copia automáticamente. Es un historial por párrafo — no un deshacer.

**Acceso:** clic derecho en un párrafo → *Versiones de párrafo*, o posate sobre una sesión en el Explorador → clic en el ícono del reloj.

```
  LÍNEA DE TIEMPO — párrafo 1:

  ┌──────────────────────────────────────────────────────┐
  │  Versiones · párrafo 1                     [Cerrar]  │
  ├──────────────────────────────────────────────────────┤
  │                                                      │
  │  ● ACTUAL                                            │
  │    En un lugar de la Mancha, de cuyo nombre          │
  │    no quiero acordarme...                            │
  │                                                      │
  │  ── 17 abr · 11:42am ──────────────────────────────  │
  │    En un lugar de la Mancha — prefiero no nombrar    │
  │    cuál — vivió no hace mucho un hidalgo...          │
  │                              [Restaurar esta versión]│
  │                                                      │
  │  ── 16 abr · 9:15pm ───────────────────────────────  │
  │    En la Mancha, en algún lugar, vivió un hombre.    │
  │                              [Restaurar esta versión]│
  │                                                      │
  │  ── 15 abr · 3:30pm ───────────────────────────────  │
  │    Había un hombre en la Mancha.                     │
  │                              [Restaurar esta versión]│
  └──────────────────────────────────────────────────────┘

  nada se borra — cada borrador es recuperable
```

Hacé clic en **Restaurar esta versión** para volver atrás. El texto actual se convierte en una nueva versión — nada se pierde permanentemente.

---

## Capítulo 8 — Notas del proyecto

Presioná `Ctrl+P` para abrir un bloc de notas adjunto al proyecto activo. Escribí libremente — se guarda automáticamente. Presioná `Esc` para cerrar.

La nota no aparece en el Explorador, no se compila al exportar, y no tiene versiones. Es una mesa auxiliar al lado de tu escritorio.

---

## Capítulo 9 — Baraja y cut-up

Baraja toma un párrafo que escribiste y lo **mezcla con un párrafo aleatorio de otro lugar del proyecto**. Esta es la técnica del cut-up — colisión automatizada, el escritor decide qué queda.

```
  ANTES DE BARAJAR:

  sesión "Capítulo Uno"          sesión "El Caballero"
  ──────────────────────         ───────────────────────────
  En un lugar de la Mancha,      Frisaba la edad de nuestro
  de cuyo nombre no quiero       hidalgo con los cincuenta
  acordarme, no ha mucho         años; era de complexión
  que vivía un hidalgo...        recia, seco de carnes,
                                 enjuto de rostro.

                 ↓  clic derecho → Barajar (Baraja)  ↓

  DESPUÉS — los dos colisionan:
  ────────────────────────────────────────────────────────
  En un lugar de la Mancha, seco de carnes, enjuto de
  rostro — de cuyo nombre no quiero acordarme, no ha
  mucho que vivía un hidalgo de los de lanza en astillero,
  adarga antigua. Frisaba los cincuenta años y madrugaba mucho.
  ────────────────────────────────────────────────────────
  algo nuevo apareció. no lo planeaste.
```

Clic derecho en cualquier párrafo → **Barajar (Baraja)**.

Si el resultado no te interesa: clic derecho en la sesión → **Deshacer barajada**.

### Cuándo usar Baraja

- Cuando un párrafo se siente atascado
- Cuando querés conexiones inesperadas entre sesiones
- Cuando la siguiente frase lógica es lo último que querés escribir

> Baraja no es un generador aleatorio. Es un **estímulo desde tu propia escritura** — todo lo que extrae viene de texto que vos mismo escribiste.

---

## Capítulo 10 — Vista de Grafo

Un mapa visual de tu proyecto. Párrafos como nodos, conexiones que dibujás a mano. En el Explorador, hacé clic en la pestaña **Grafo**.

```
  VISTA DE GRAFO — El Proceso · Objetos y personas:

                   [Cap.1 · El Arresto]
                    /       |        \
              Josef K.   la puerta  los guardianes
                /           |             \
       [Cap.3 · Tribunal] [Cap.2 · K.]──[Cap.7 · Abogado]
            |    \          |               |
         Josef K. la sala  Leni          Josef K.
            |        \      |               |
    [Cap.5 · Flagelador] \ [Cap.4 · Leni]  [Cap.8 · Mercader]
                          \    \               /
                       el látigo Leni────Josef K.
                              \      \       /
                           [Cap.9 · Sacerdote]
                                   |
                            [Cap.10 · La Muerte]

  clic en un nodo → abre el párrafo en el Editor
  Ctrl+clic en varios → los abre todos juntos
```

- Hacé clic en **+ Nuevo grafo** para crear uno (podés tener varios por proyecto)
- Agregá nodos desde tus sesiones
- Clic en un nodo y luego en otro para conectarlos
- Mantené `Ctrl` y hacé clic en varios nodos para abrirlos juntos

---

## Capítulo 11 — Hashtags

Etiquetas que asignás manualmente a párrafos individuales. Rastreá personajes, objetos, motivos recurrentes — encontralos todos al instante.

Clic derecho en un párrafo → **# (panel de hashtags)**. Activá o desactivá etiquetas, creá nuevas.

Buscá por etiqueta igual que cualquier término:

```
buscar #ama
```

---

## Capítulo 12 — Importar y exportar

### Importar

Hacé clic en `[↑]` en el encabezado del Explorador. Acepta `.txt`, `.md`, `.docx`. Cada párrafo/sección se convierte en una sesión en un nuevo proyecto.

### Exportar

```
compilar
compilar Don Quijote — Primer Borrador
```

Todas las sesiones visibles, en el orden del Explorador, exportadas como un único archivo `.docx` en `Documents/gombro/{nombreProyecto}/`. Los **senderos** del proyecto se incluyen automáticamente al final, cada uno con su nombre como título.

---

## Capítulo 13 — Piso 13

> Este capítulo fue dejado intencionalmente en blanco por razones supersticiosas. Si estás leyendo esto, aún no pasó nada malo. Todavía.

---

## Capítulo 13b — Álgebra Borgiana

El Álgebra Borgiana es el sistema de Gombro para escribir con alternativas abiertas — inspirado directamente en la forma en que Borges corregía sus manuscritos: no borrando, sino **ramificando**.

En los borradores manuscritos de Borges se puede ver una palabra tachada con tres alternativas escritas al lado, unidas por una llave. No las resolvía de inmediato. Las dejaba coexistir en la página hasta que la correcta se volvía obvia — o hasta que la ambigüedad misma se convertía en el punto.

### Insertar un fragmento pendiente

1. Hacé clic para posicionar el cursor (o seleccioná una palabra/frase)
2. Clic derecho → **Insertar**
3. Escribí tu texto en el panel — admite múltiples líneas
4. Presioná **ok** (o `Ctrl+Enter`) para insertar como bloque Borgiano pendiente

Si cerrás el panel sin presionar ok, no se inserta nada. El bloque queda pendiente hasta que lo confirmés.

```
  FLUJO DE INSERCIÓN:

  cursor aquí ↓
  ...vivía un hidalgo ▌ de los de lanza...

      clic derecho → Insertar
      ┌─────────────────────────────────┐
      │  de cuyo nombre prefiero        │  ← escribí acá
      │  no acordarme,                  │
      │                      [ok]       │
      └─────────────────────────────────┘
      presioná ok (o Ctrl+Enter)

  resultado — bloque pendiente insertado:
  ...vivía un hidalgo ╔═══════════════════════════╗ de los de lanza...
                       ║ de cuyo nombre prefiero  ║
                       ║ no acordarme,             ║
                       ╚═══════════════════════════╝
                         (pendiente — confirmalo o dejalo abierto)
```

### Crear una variante desde una selección

1. Seleccioná cualquier palabra o frase
2. Clic derecho → **Agregar variante**
3. Escribí la alternativa y presioná `Enter`

El texto seleccionado se convierte en la primera opción. Tu nuevo texto es la segunda. Ambos aparecen como un bloque visual:

```
  SELECCIONAR → clic derecho → Agregar variante:

  ...el perro estaba [muerto]
                       ↓
  escribí la alternativa: "vivo"
                       ↓
  ...el perro estaba ┌─────────────┐
                     │ muerto      │  ← original
                     │ vivo        │  ← nueva variante
                     └─────────────┘  ...ladrando todavía

  agregá más variantes cuando quieras → clic derecho en bloque → Agregar variante
```

### Agregar sub-variantes

Podés ramificar una opción dentro de un bloque borgiano — crear una variante de una variante. Así se reproduce la estructura arbórea de los manuscritos de Borges: cada rama puede bifurcarse en nuevas ramas.

1. Clic derecho sobre una fila específica del bloque
2. Elegí **Agregar sub-variante**
3. Escribí la alternativa y presioná `Ctrl+Enter`

La opción elegida se convierte en un nuevo bloque anidado con dos ramas — la original y la nueva:

```
  SUB-VARIANTE — ramificar una opción existente:

  ┌──────────────────────────┐
  │ el perro caminaba        │  ← clic derecho → Agregar sub-variante
  │ el perro venía           │
  └──────────────────────────┘
              ↓
  ┌──────────────────────────┐
  │ ┌────────────────────┐   │
  │ │ el perro caminaba  │   │  ← sub-bloque anidado
  │ │ el perro trotaba   │   │
  │ └────────────────────┘   │
  │ el perro venía           │
  └──────────────────────────┘

  Sintaxis interna: {el perro venía|{el perro caminaba|el perro trotaba}}
```

No hay límite de profundidad — cada rama puede seguir bifurcándose.

### Resolver una rama

```
  RESOLUCIÓN — al estilo Borges (tachado, no borrado):

  clic derecho en "muerto" → Elegir ésta:
  ┌─────────────┐        ┌─────────────┐
  │ muerto      │   →    │ muerto      │  ← elegida
  │ vivo        │        │ ~~vivo~~    │  ← tachada (sigue visible)
  │ inconsciente│        │ ~~inconsciente~~ │
  └─────────────┘        └─────────────┘

  clic derecho → Confirmar (colapsar) → texto plano: "muerto"
  las alternativas desaparecen solo cuando VOS lo decidís.
```

Clic derecho en cualquier fila del bloque:

| Acción | Efecto |
|--------|--------|
| **Elegir ésta** | Tacha todas las demás opciones |
| **Tachar ésta** | Marca esta opción como descartada |
| **Confirmar (colapsar)** | Colapsa el bloque a texto plano (si hay una sola opción viva) |

### Sintaxis

Internamente se guarda como `{opción1|opción2|~~tachada~~}`. Nunca lo ves mientras escribís — el editor renderiza el bloque visual automáticamente.

### La filosofía

> El Álgebra Borgiana es una forma de **mantener las contradicciones abiertas** — de escribir un texto que contiene sus propias alternativas sin forzar una resolución.
>
> Borges escribió: *"El tiempo se bifurca perpetuamente hacia innumerables futuros."* El Álgebra Borgiana es el procesador de texto que le cree.

---

## Capítulo 13c — El Diario

El Diario es un proyecto especial que Gombro mantiene separado de tus proyectos de escritura. Una sesión por día, con nombre automático según la fecha. Presioná `Ctrl+D` desde cualquier lugar para abrirlo.

```
  EXPLORADOR — el diario siempre al final:

  ┌──────────────────────────┐
  │  ▸ PROYECTO: Don Quixote │
  │    La Mancha             │
  │    El Caballero          │
  │  ──────────────────────  │
  │  ▸ PROYECTO: DIARIO      │  ← siempre al fondo
  │    Mié, 22 abril, 26     │  ← hoy (creada automáticamente)
  │    Mar, 21 abril, 26     │
  │    Lun, 20 abril, 26     │
  └──────────────────────────┘
```

### Cómo funciona

- `Ctrl+D` desde cualquier lugar — abre la sesión de hoy, creándola si no existe
- Los nombres de sesión son fechas literarias: *Mié, 22 abril, 26*
- `Ctrl+N` está deshabilitado en modo diario — una sesión por día, creada automáticamente
- A medianoche, Gombro cambia automáticamente a la sesión del día siguiente
- También disponible desde el menú slash: escribí `/` → *diario* o *diary*

```
  FLUJO:

  Presionás Ctrl+D desde cualquier lugar
         ↓
  ¿Existe la sesión de hoy?
    ┌────┴─────┐
    SÍ         NO
    ↓          ↓
  quedás     se crea sola
  ahí     "Mié, 22 abr, 26"
              ↓
          se abre en el editor
              ↓
  escribís libremente — se guarda solo
              ↓
  medianoche → se abre la sesión del día siguiente
```

> El diario no es un proyecto — es un hábito. Gombro lo mantiene fuera del camino de tu ficción, siempre al fondo de la lista, siempre a un atajo de distancia.

---

## Capítulo 13d — Modo Schrödinger

En 1935 Erwin Schrödinger describió un gato encerrado en una caja: sin abrir la caja, el gato está simultáneamente vivo *y* muerto. Solo al observarlo colapsa en uno de los dos estados.

El Modo Schrödinger de Gombro aplica esa lógica al texto: hay fragmentos que todavía no son ni una cosa ni la otra. Están escritos, pero no decididos.

### ¿Qué es texto en estado cuántico?

En Gombro, un párrafo está en estado Schrödinger cuando contiene alguno de estos elementos:

| Tipo | Cómo se ve | Qué significa |
|------|------------|---------------|
| **Tachado** | ~~texto tachado~~ | Marcado para posible borrado — todavía no decidiste |
| **Variante borgiana** | `{opción A|opción B}` | Texto en superposición — dos futuros posibles sin colapsar |

El tachado dice: *"puede que esto sobre."*
La variante dice: *"puede que esto sea esto, o aquello."*
Ninguno de los dos es definitivo. El texto sigue abierto.

### Cómo tachar texto

Seleccioná cualquier fragmento → clic derecho → **Tachar**. El texto queda visible pero cruzado.

```
  ┌───────────────────────────────────────────────────┐
  │  ...en un lugar de la Mancha, de cuyo             │
  │  nombre ~~no quiero acordarme~~, no ha mucho...   │
  └───────────────────────────────────────────────────┘
         ↑ en el editor se ve con tachado visual,
           los ~~ están ocultos pero guardados
```

Luego, clic derecho sobre el texto tachado:

```
  ┌──────────────────────┐
  │  Borrar              │  ← elimina el fragmento
  │  Editar              │  ← quita el tachado, editás
  └──────────────────────┘
```

**Editar** es la opción borgiana: no borrás el pensamiento, lo transformás. Escribís la variante, Enter, y queda limpio sin tachadura.

### El botón ⚛ Schrödinger

Al pie del Explorador, sobre las Colecciones, aparece siempre el botón Schrödinger:

```
  ┌──────────────────────────────────┐
  │  sesión 1                        │
  │  sesión 2                        │
  │  sesión 3                        │
  │  ──────────────────────────────  │
  │  ⚛ Schrödinger           [3]    │  ← badge amarillo = párrafos pendientes
  │  ──────────────────────────────  │
  │  📁 mi colección                 │
  └──────────────────────────────────┘
```

- El **badge** se actualiza automáticamente cuando cambiás de proyecto o guardás
- Hacé **clic** para ver la lista de párrafos en estado cuántico
- Hacé clic en cualquier párrafo del resultado para ir directo a él en el editor

### La lista Schrödinger

Al hacer clic en ⚛, el panel del Explorador muestra los párrafos pendientes agrupados por sesión — igual que los resultados de búsqueda:

```
  ⚛ Schrödinger  [3]              [✕ cerrar]
  ──────────────────────────────────────────
  Capítulo Uno
    ~~no quiero acordarme~~, no ha mucho...
  ──────────────────────────────────────────
  Capítulo Dos
    ...vivía un hidalgo {de los de lanza|con
    lanza} en astillero...
  ──────────────────────────────────────────
  Epílogo
    ~~Esta parte sobra~~ · La historia que...
```

### Schrödinger y el compilar

Cuando compilás a `docx` o `md`, Gombro escanea el proyecto. Si hay párrafos en estado Schrödinger, aparece un aviso antes de generar el archivo:

```
  ⚛  3 párrafos en estado Schrödinger
     (tachaduras o variantes sin resolver)
```

Podés compilar igual — es solo un recordatorio. El texto tachado saldrá tachado en el docx; las variantes borgianas sin colapsar aparecerán en su forma cruda.

### El flujo completo

```
  ESCRIBÍS           DUDÁS              DECIDÍS
  ────────           ─────              ───────
  texto normal  →  Tachar o Variante  →  ⚛ Schrödinger
                                           ↓
                                      clic en párrafo
                                           ↓
                                   clic derecho → Borrar
                                               → Editar
                                           ↓
                                      badge llega a 0
                                           ↓
                                      compilar limpio
```

> Borges tachaba pero no borraba. Dejaba visible lo descartado, como una prueba de que el pensamiento había estado ahí. El Modo Schrödinger es eso: un espacio para la duda antes de la decisión.

### Referencia

| Acción | Cómo |
|--------|------|
| Tachar selección | Seleccioná → clic derecho → `Tachar` |
| Borrar tachado | Clic derecho sobre tachado → `Borrar` |
| Editar tachado | Clic derecho sobre tachado → `Editar` → escribís → Enter |
| Ver párrafos pendientes | Clic en `⚛ Schrödinger` en el Explorador |
| Comando directo | `schrodinger` en la CmdBar |

---

## Capítulo 13e — Plan de escritura

El Plan de escritura es un panel que muestra cuánto escribiste — hoy, esta semana, y en los meses anteriores. No es una herramienta de productividad. Es un espejo.

### Cómo abrirlo

Escribí `/` en la CmdBar y seleccioná **Plan de escritura**. El panel aparece a la derecha del Explorador.

### Qué muestra

- **Hoy** — palabras escritas hoy, con un objetivo diario opcional. Hacé clic en `set` para definir tu meta.
- **Esta semana** — gráfico de barras de los últimos 7 días.
- **Semanas** — totales semanales de los meses anteriores.
- **Meses** — totales mensuales.

### El objetivo diario

Podés definir una meta de palabras por día. Gombro cuenta todo lo que escribís en el proyecto activo. Cuando alcanzás la meta, la barra se llena. Sin alarmas, sin notificaciones — solo un registro silencioso.

> Un plan de escritura no es un plazo. Es un hábito hecho visible.

### Referencia

| Acción | Cómo |
|--------|------|
| Abrir Plan de escritura | `/plan` en la CmdBar |
| Definir objetivo diario | Clic en `set` junto al campo Objetivo |
| Cerrar el panel | Clic en `✕` en el encabezado del panel |

---

## Capítulo 13f — Notas de sesión y badges

Cada sesión del Explorador puede tener su propia nota — una anotación libre visible de un vistazo. Un badge (`✎`) aparece en las sesiones que tienen notas, para saber de un vistazo cuáles tienen contexto.

### Cómo agregar una nota a una sesión

1. Hacé clic derecho en el nombre de la sesión en el Explorador.
2. Seleccioná **Anotar sesión**.
3. Se abre un pequeño panel. Escribís tu nota.
4. La nota se guarda sola.

Las notas también se pueden anclar a párrafos específicos usando `F4` mientras escribís.

### El badge

Las sesiones con al menos una nota muestran un badge `✎` en el Explorador. Sirve para marcar sesiones que necesitan atención, tienen contexto, o están en progreso — sin tener que abrirlas.

### Referencia

| Acción | Cómo |
|--------|------|
| Agregar nota a sesión | Clic derecho en sesión → `Anotar sesión` |
| Agregar nota a párrafo | `F4` con el cursor en el párrafo |
| Ver todas las notas | `/nota ver` en la CmdBar |

---

## Capítulo 13g — Filtro por hashtag en el Explorador

Si tu proyecto usa hashtags, podés filtrar la lista de sesiones por hashtag directamente desde el Explorador — sin abrir el panel de búsqueda.

### Cómo funciona

En la parte inferior del Explorador, los hashtags del proyecto aparecen como etiquetas pequeñas. Hacé clic en una para mostrar solo las sesiones que contienen ese hashtag. Hacé clic de nuevo para quitar el filtro.

Es útil cuando un proyecto tiene muchas sesiones y querés enfocarte en las que corresponden a un personaje, lugar o tema específico.

### Referencia

| Acción | Cómo |
|--------|------|
| Filtrar por hashtag | Clic en la etiqueta de hashtag en el Explorador |
| Quitar el filtro | Clic de nuevo en el hashtag activo |
| Gestionar hashtags | `/tag` en la CmdBar |

---

## Capítulo 13h — Escala de texto

Podés ajustar el tamaño del texto en el editor sin cambiar la tipografía ni el estilo. Es solo para comodidad de lectura — como el nivel de zoom en un procesador de texto.

### Cómo cambiar la escala

Escribí `/escala` (o `/scale`) en la CmdBar. Ingresá un número entre 50 y 300. El número representa un porcentaje: `100` es el tamaño por defecto, `125` agranda el texto un 25%, `80` lo achica.

```
  /escala 125   →  texto más grande (25% sobre el defecto)
  /escala 80    →  texto más chico (20% bajo el defecto)
  /escala 100   →  vuelve al tamaño original
```

La configuración se guarda automáticamente y persiste cuando volvés a abrir Gombro.

> Esto no cambia la tipografía, el interlineado ni el estilo de los títulos. Solo escala el tamaño base — como acercar o alejar la página.

### Referencia

| Acción | Cómo |
|--------|------|
| Cambiar escala de texto | `/escala [50–300]` en la CmdBar |
| Volver al tamaño original | `/escala 100` |

---

## Capítulo 13i — Libreta Obsidian

Obsidian es una aplicación de notas para escritores y pensadores. Guarda las notas como archivos de texto plano (`.md`) en tu computadora — sin nube, sin suscripción. Podés descargarlo gratis en [obsidian.md](https://obsidian.md).

Si usás Obsidian junto con Gombro, la **Libreta Obsidian** te permite traer tus notas de Obsidian a tu proyecto de escritura en forma automática.

### Cómo funciona la conexión

Obsidian y Gombro corren en tu computadora. Gombro encuentra tu vault de Obsidian automáticamente — no hace falta configurar rutas ni ajustes.

La conexión se basa en **hashtags**. Si tu proyecto en Gombro se llama *Kolon*, Gombro va a buscar las notas de Obsidian que contengan `#kolon`. Cada nota que coincida aparece en la Libreta Obsidian.

### Flujo típico

1. Estás afuera, leyendo, pensando. Abrís Obsidian en el celular o la notebook y escribís: *"El uniforme del coronel roza el suelo cuando camina. #kolon"*
2. De vuelta en tu escritorio, abrís Gombro y abrís el proyecto Kolon.
3. Aparece una notificación: **"Tenés notas nuevas en Obsidian."**
4. Escribís `/obsidian` en la CmdBar. Se abre la Libreta Obsidian.
5. Ves la nota. La copiás a tu sesión. Listo.

### El panel Libreta Obsidian

- Muestra solo las notas **nuevas o modificadas** desde la última vez que las revisaste.
- Cada nota tiene dos botones: **⎘ Copiar** (copia el contenido al portapapeles y la saca de la vista) y **✕ Borrar** (marca como leída — no vuelve a aparecer salvo que la notes cambie en Obsidian).
- Hacé clic en **Actualizar** para volver a escanear el vault.

### Múltiples proyectos

El hashtag se deriva del nombre del proyecto en forma automática. Proyecto *Quixote* → busca `#quixote`. Podés usar múltiples hashtags en una misma nota de Obsidian para enviarla a varios proyectos.

### Referencia

| Acción | Cómo |
|--------|------|
| Abrir Libreta Obsidian | `/obsidian` en la CmdBar |
| Copiar una nota | Clic en `⎘` — copia al portapapeles, sale de la vista |
| Descartar una nota | Clic en `✕` — marca como leída, no vuelve a aparecer |
| Actualizar | Clic en **Actualizar** en el panel |
| Descargar Obsidian | [obsidian.md](https://obsidian.md) (gratis) |

---

## Capítulo 13j — Respaldo y recuperación

Gombro guarda todo en un único archivo SQLite: `gombro.db`. Un respaldo es simplemente una copia de ese archivo. Recuperar es reemplazarlo por una copia anterior.

### Cómo funciona

**Respaldo automático** — cada vez que cerrás Gombro, se guarda un backup automáticamente. No requiere configuración.

**Respaldo manual** — escribí `respaldo` en la CmdBar en cualquier momento para guardar un snapshot inmediato.

**Recuperación** — escribí `recuperar` en la CmdBar para abrir la lista de backups. Seleccioná uno y hacé clic en **Restaurar seleccionado**.

### Dónde se guardan

Por defecto, los backups van a una carpeta llamada `backup_gombro` junto al archivo de base de datos:

```
%AppData%\gombro\backup_gombro\
    gombro-2026-04-29_10-00-00.db
    gombro-2026-04-30_09-15-00.db
```

### Cambiar la carpeta

Abrí el modal de recuperación (`recuperar`) y hacé clic en **Cambiar...** — se abre un diálogo nativo para elegir carpeta. Podés elegir cualquier carpeta: Dropbox, Google Drive, un disco externo. El ajuste se guarda y se aplica a todos los backups posteriores, incluidos los automáticos al cerrar. Podés cambiarlo en cualquier momento.

### Rotación de backups

Gombro conserva los **10 backups más recientes**. Cuando se crea uno nuevo y se supera ese límite, el más viejo se elimina automáticamente.

### Restaurar un backup

1. Escribí `recuperar` en la CmdBar.
2. Seleccioná un backup de la lista.
3. Hacé clic en **Restaurar seleccionado**.

Gombro cierra la base de datos, la reemplaza con el backup elegido y recarga todo de inmediato. No hace falta reiniciar.

### Referencia de comandos

| Comando | Acción |
|---------|--------|
| `respaldo` | Guardar un snapshot ahora |
| `recuperar` | Abrir lista de backups y restaurar |

---

## Capítulo 13k — Senderos (Laberintos narrativos)

Un **Sendero** es una bifurcación. Desde cualquier párrafo podés abrir un camino alternativo — una versión de la historia que se separa en ese punto exacto y sigue su propio rumbo. La imagen es la de un jardín con senderos: el texto se bifurca, no se reemplaza.

### Crear un sendero

Hacé clic derecho en el párrafo donde querés bifurcar y elegí **🌿 Senderear desde aquí**. Gombro crea el sendero y lo registra en el panel Explorer bajo la sección **SENDEROS**.

El nombre del sendero se genera automáticamente: `Ses: [nombre de sesión] — párrafo: [primeras palabras]`. Podés renombrarlo con clic derecho en el Explorer.

### Abrir un sendero

Hacé clic en el sendero en el Explorer. Se abre como una sesión propia — con el contenido heredado hasta el punto de bifurcación — lista para que escribas hacia adelante. Lo que escribas en el sendero no toca la sesión original.

### El banner de origen

Cuando un sendero está abierto, aparece una barra verde arriba del editor:

```
🌿 Ses: Historia 1 — párrafo: era un día de invierno...
```

Ese texto es **clickeable**: al hacer clic volvés a la sesión de origen en el punto de bifurcación.

### Senderos y el compilar

Al compilar el proyecto (`compilar` o `compilar .md`), los senderos se incluyen automáticamente al final del documento, cada uno con su nombre como título. No necesitás hacer nada extra.

### Referencia

| Acción | Cómo |
|--------|------|
| Crear sendero | Clic derecho en párrafo → **🌿 Senderear desde aquí** |
| Abrir sendero | Clic en el sendero en el Explorer |
| Volver al origen | Clic en el banner verde arriba del editor |
| Renombrar | Clic derecho en el sendero → Renombrar |
| Eliminar | Clic derecho en el sendero → Eliminar sendero |

---

## Capítulo 14 — Flujo de trabajo recomendado

De proyecto en blanco a borrador exportado — una sugerencia, no una regla.

### Fase 1 — Abrir el instrumento

```
crear proyecto Don Quijote
nuevo La Mancha
```

Escribí hasta que la sesión esté lista, luego creá otra. No organices todavía.

### Fase 2 — Dejar que el azar trabaje

Elegí un párrafo que se sienta atascado. Clic derecho → Barajar. Quedáte con lo que te sorprendió. Deshacé lo que no funcionó. Usá el **Modo Frase** para ir más despacio.

### Fase 3 — Etiquetar y mapear

Etiquetá elementos recurrentes. Abrí el Grafo, construí un mapa visual de conexiones.

### Fase 4 — Buscar y coleccionar

Buscá elementos para rastrear. Guardá las búsquedas más útiles como Colecciones. Usá las Versiones de Párrafo para comparar y restaurar.

### Fase 5 — Exportar

Ordená las sesiones en el Explorador como querés que aparezcan en el documento. Luego:

```
compilar Don Quijote — Primer Borrador
```

Abrí el `.docx` para el formateo final y la entrega.

---

## Atajos de teclado

| Atajo | Acción |
|-------|--------|
| `:` o `/` | Abrir CmdBar |
| `Ctrl+T` | Abrir paleta de comandos flotante |
| `Ctrl+F` | Abrir búsqueda flotante |
| `Ctrl+N` | Nueva sesión (deshabilitado en modo diario) |
| `Ctrl+D` | Abrir la sesión del diario de hoy |
| `Ctrl+Q` | Modo Schrödinger — ver párrafos con texto cuántico |
| `F4` | Alternar post-it de nota para la sesión activa |
| `F1` | Abrir ayuda |
| `Esc` | Cerrar CmdBar → cerrar búsqueda → activar Zen |
| `F2` | Renombrar sesión seleccionada en el Explorador |
| `Delete` | Eliminar sesión seleccionada (o todas las multi-seleccionadas) |
| `↑ ↓` | Navegar sesiones en el Explorador |
| `Enter` | Abrir sesión seleccionada en el Explorador |
| `Ctrl+clic` | Multi-seleccionar sesiones en el Explorador |
| `Shift+clic` | Seleccionar rango de sesiones en el Explorador |

---

## Sobre el autor

**Raúl Lilloy** es el creador de Gombro. Cree que escribir debe ser un acto de descubrimiento, no de producción. Construyó la herramienta que quería usar — sin nube, sin IA, sin agenda.

```
        .-------.
       /  o   o  \
      |     ^     |
      |   \___/   |
       \  -----  /
        '-.___..-'
       /|         |\
      / |  RAÚL   | \
     /  |  LILLOY |  \
    /   '---------'   \
        |  ☕  💻  |
        |   Gombro  |
        |  v0.0.5β  |
        '~~~~~~~~~~~'

  "Escribir es... no sé.
   Por eso escribo."
```

---

## Índice Alfabético

| Concepto / Acción | Cómo | Capítulo |
|-------------------|------|----------|
| Abarajar (mezclar frases) | `abarajar` | 9 |
| Backup / Recuperación | `respaldo` · `recuperar` | 13j |
| Álgebra Borgiana | Seleccioná texto → clic derecho → Agregar variante · `/senderos` | 13b |
| Ayuda | `ayuda` · `F1` | — |
| Baraja (cut-up) | Clic derecho en párrafo → Baraja | 9 |
| Borgiano — insertar | Clic derecho → Insertar | 13b |
| Búsqueda | `buscar <termino>` · `Ctrl+F` | 6 |
| Búsqueda en frases | `buscar <termino> en frases` | 6 |
| CmdBar | `:` o `/` | 4 |
| Colecciones | Búsqueda → + Guardar como colección | 6 |
| Compilar / Exportar | `compilar [nombre]` | 12 |
| Crear proyecto | `crear proyecto <nombre>` | 2 |
| Diario | `diario` · `Ctrl+D` | 13c |
| Escala de texto | `escala [50–300]` | 13h |
| Explorador | Panel izquierdo — sesiones, proyectos, grafo | 5 |
| Grafo | Explorador → pestaña Grafo → Nuevo grafo | 10 |
| Grafo — multi-selección | `Ctrl+clic` en nodos | 10 |
| Grafo — búsqueda | Barra de búsqueda del grafo | 10 |
| Hashtags | Clic derecho en párrafo → # (panel de hashtags) | 11 |
| Hashtag — filtro en Explorador | Clic en etiqueta de hashtag en el Explorador | 13g |
| Importar archivo | ↑ (cabecera del Explorador) — .md / .docx / .txt | 12 |
| Libreta Obsidian | `obsidian` | 13i |
| Modo frase | `modo frase` | 3 |
| Modo Schrödinger | `schrodinger` · `Ctrl+Q` | 13d |
| Modo zen | `zen` | 3 |
| Notas (proyecto) | `F4` · clic derecho sesión → Anotar sesión | 8 |
| Notas — badges de sesión | Clic derecho sesión → Anotar sesión | 13f |
| Plan de escritura | `plan` | 13e |
| Párrafo — versiones | Clic derecho en párrafo → Versiones | 7 |
| Proyectos — lista | `abrir` · `ver proyectos` | 5 |
| Revelar origen (tras Baraja) | Explorador → ✂ revelar naipe | 9 |
| Revelar sesión en Explorador | Clic derecho en párrafo → Revelar en Binder | 5 |
| Sesiones — nueva | `nuevo [nombre]` · `Ctrl+N` | 5 |
| Sesiones — nueva abajo | Clic derecho sesión → Agregar sesión abajo | 5 |
| Sesiones — reordenar | Clic derecho → Mover arriba / abajo · Arrastrar y soltar | 5 |
| Sesiones — multi-selección | `Ctrl+clic` en sesiones | 5 |
| Párrafos — agregar abajo | Clic derecho párrafo (outline) → Agregar párrafo abajo · `Enter` | 5 |
| Párrafos — reordenar | Arrastrar párrafo en el outline y soltar | 5 |
| Párrafos — navegar | Clic en párrafo del outline → cursor titila en el editor | 5 |
| Deshacer mezcla | Clic derecho sesión → Deshacer mezcla | 9 |
