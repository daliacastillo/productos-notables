# Productos notables · demostración geométrica interactiva

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23195334.svg)](https://doi.org/10.5281/zenodo.23195334)
[![Licencia: CC BY-NC-SA 4.0](https://img.shields.io/badge/Licencia-CC%20BY--NC--SA%204.0-blue.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es)

Actividad web interactiva para el tema **productos notables**, pensada para la unidad 2 de
*Tópicos de Matemáticas* (Licenciatura en Matemáticas, Universidad Autónoma de Nayarit).

Cada identidad algebraica se **demuestra geométricamente**: el estudiante mueve deslizadores,
separa piezas y comprueba que la suma de las áreas (o de los volúmenes) reproduce exactamente
la fórmula. No es una lámina ilustrada: las figuras se recalculan con los valores que el
estudiante elige.

Además, la pestaña **⑥ Resolver** acepta cualquier binomio o trinomio que el estudiante escriba y
devuelve el resultado junto con el **nombre del patrón** y la **fórmula que se está aplicando**,
la sustitución, el paso a paso y una comprobación numérica — lo mismo para desarrollar que para
factorizar.

---

## Contenido

| Pestaña | Identidad | Qué puede hacer el estudiante |
|---|---|---|
| ① | (a + b)² = a² + 2ab + b² | Mover a y b, separar las cuatro piezas, activar la cuadrícula de unidades y pasar el puntero por cada región para ver a qué término corresponde |
| ② | (a − b)² = a² − 2ab + b² | Avanzar los cinco pasos del recorte y ver **por qué** la identidad termina sumando b²: porque esa esquina se restó dos veces |
| ③ | a² − b² = (a + b)(a − b) | Arrastrar la pieza recortada (o animarla) hasta reacomodarla en el rectángulo de lados a + b y a − b |
| ④ | (x + p)(x + q) = x² + (p + q)x + pq | Ver por qué el coeficiente lineal es la **suma** y el término independiente el **producto**, y resolver un reto de factorización ajustando p y q |
| ⑤ | (a + b)³ = a³ + 3a²b + 3ab² + b³ | Separar las ocho piezas del cubo en proyección isométrica y contar por qué los coeficientes son 1, 3, 3, 1 |
| ⑥ | Resolver | Escribir cualquier binomio o trinomio y obtener el resultado, el **nombre del patrón**, la **fórmula que se aplica**, la sustitución, el paso a paso y una comprobación numérica |
| ⑦ | Práctica | Serie de diez reactivos generados al azar, con marcador y racha |

### La pestaña ⑥ Resolver

El estudiante escribe una expresión y el programa decide por sí mismo si hay que **desarrollar** o
**factorizar**. No es una calculadora que entrega el resultado: lo que muestra es el **razonamiento**.

- **Desarrolla** cuadrado de una suma y de una diferencia, cubo de una suma y de una diferencia,
  cuadrado de un trinomio, binomios conjugados y binomios con término común. Cuando la expresión
  no encaja en ningún producto notable, lo dice y la desarrolla por la propiedad distributiva.
- **Factoriza** factor común, diferencia de cuadrados, suma y diferencia de cubos, trinomio
  cuadrado perfecto y trinomios de segundo grado (x² + bx + c y ax² + bx + c con raíces racionales).
  Si el polinomio no se factoriza con los patrones de la unidad, lo declara en lugar de inventar
  una respuesta: por ejemplo, `x² + 4` queda sin factorizar.
- Cada respuesta trae: la **etiqueta del patrón** reconocido, la **fórmula general** con los
  términos coloreados igual que en las figuras, la **sustitución** (quién es *a*, quién es *b*),
  la tabla de **pasos**, el resultado y una **comprobación numérica independiente** (evalúa la
  expresión original y el resultado con valores concretos y compara).
- Un botón lleva a la pestaña con la **demostración geométrica** del patrón reconocido, de modo que
  el estudiante pase del cálculo a la figura y no al revés.

El cálculo es **aritmética exacta con fracciones**, no de punto flotante: `(x/2 + 3)²` devuelve
`x²/4 + 3x + 9` sin errores de redondeo. Acepta `^2`, `²`, `*`, multiplicación implícita (`2x`,
`3(x+1)`), corchetes y el signo menos tipográfico (−).

Ejemplos que se pueden teclear tal cual: `(2x+3)^2`, `(3a−2b)³`, `(x+5)(x−5)`,
`(x+2)(x+7)`, `(a+b+c)^2`, `x^2+10x+25`, `27x³−8`, `6x²+7x−3`.

---

En la sección de práctica **cada distractor corresponde a un error frecuente identificado**
(olvidar el doble producto, no elevar el coeficiente, confundir suma con producto al factorizar,
creer que el último término de (a − b)² es negativo). La retroalimentación dice qué se hizo mal,
no sólo que la respuesta es incorrecta.

---

## Cómo publicarla en GitHub Pages

1. Cree un repositorio nuevo en GitHub, por ejemplo `productos-notables`.
2. Suba los archivos de esta carpeta a la raíz del repositorio (`index.html`, `README.md`,
   `CITATION.cff`, `LICENSE`).
   Desde la web: **Add file → Upload files**, arrastrar y **Commit changes**.
3. Entre a **Settings → Pages**.
4. En *Source* elija **Deploy from a branch**; en *Branch* elija `main` y la carpeta `/ (root)`.
   Guarde con **Save**.
5. Espere un minuto. La página quedará publicada en:

   ```
   https://daliacastillo.github.io/productos-notables/
   ```

   Ese enlace se puede compartir con los estudiantes o pegarse en la plataforma del curso.

Desde la terminal, el equivalente es:

```bash
git init
git add .
git commit -m "Actividad interactiva de productos notables"
git branch -M main
git remote add origin https://github.com/daliacastillo/productos-notables.git
git push -u origin main
```

---

## Sugerencias de uso en clase

- **Antes de la fórmula.** Proyecte la pestaña ① con la cuadrícula activada y pida contar los
  cuadritos de cada región antes de escribir ninguna identidad. La fórmula aparece como un
  resumen de lo que ya contaron.
- **El error de (a + b)² = a² + b².** Pida que ajusten a y b para que las dos piezas anaranjadas
  valgan cero. Al no conseguirlo, el error queda desacreditado por la figura, no por la autoridad
  del docente.
- **La pestaña ② como argumento, no como receta.** El paso 3 es el momento didáctico: la esquina
  b² se restó dos veces y hay que devolverla. Conviene detenerse ahí antes de avanzar.
- **La pestaña ④ como puente a factorizar.** El reto pide construir un trinomio dado moviendo p y q.
  Es exactamente el razonamiento de la factorización de x² + bx + c, pero visto como un rectángulo.
- **La pestaña ⑤ y el triángulo de Pascal.** Las tres piezas de volumen a²b corresponden a las tres
  maneras de elegir cuál arista mide b. De ahí salen los coeficientes del binomio de Newton.
- **La pestaña ⑥ para verificar, no para resolver.** Pida que el estudiante haga el ejercicio en el
  cuaderno y sólo después lo teclee. El valor está en comparar *su* paso a paso con el del programa:
  donde difieren está el error. Una variante útil es dar el resultado y pedir que escriba la
  expresión original que lo produce.
- **Tarea.** La serie de práctica puede pedirse como evidencia: captura de pantalla del marcador
  final con 8 o más aciertos.

---

## Notas técnicas

- **Un solo archivo.** Todo (HTML, CSS, SVG y JavaScript) está en `index.html`. No hay dependencias,
  no se carga nada de internet y funciona sin conexión: basta abrir el archivo en cualquier navegador.
- **Sin build ni instalación.** No requiere Node, npm ni ningún compilador.
- **Figuras generadas por código.** Todas las ilustraciones son SVG dibujado en tiempo real a partir
  de los valores de los deslizadores, incluida la proyección isométrica del cubo.
- **Álgebra propia, sin bibliotecas.** El resolvedor de la pestaña ⑥ es un pequeño sistema de
  álgebra simbólica escrito desde cero: racionales exactos → polinomios multivariados →
  analizador por descenso recursivo → reconocimiento de patrones sobre el árbol sintáctico.
  No usa `eval` ni ninguna biblioteca externa, y toda la aritmética es exacta (fracciones, no
  punto flotante).
- **Responsiva.** Funciona en computadora, tableta y teléfono (probada hasta 390 px de ancho).
- **Tema claro y oscuro**, con botón de cambio y respeto a la preferencia del sistema.
- **Sin almacenamiento.** No guarda datos, no usa cookies ni `localStorage` y no envía nada a
  ningún servidor; el marcador vive sólo mientras la pestaña está abierta.
- **Citable.** Lleva metadatos de citación en el `<head>` (Dublin Core, etiquetas `citation_*` de
  Google Académico y `JSON-LD` de schema.org) y un archivo `CITATION.cff` en la raíz.

### Cómo modificarla

Los parámetros didácticos están al principio de cada bloque del script:

- `S1`, `S2`, `S3`, `S4`, `S5` guardan el estado inicial de cada demostración (valores de a, b, p, q).
- `RETOS` es la lista de parejas (p, q) con que se generan los retos de factorización de la pestaña ④.
- `generadores()` contiene los cinco tipos de reactivo de la práctica. Para agregar uno nuevo basta
  añadir una función que devuelva `{ q, ops, exp }`, con la respuesta correcta en la posición 0;
  el programa baraja las opciones por sí mismo.
- La paleta completa son variables CSS en `:root` (`--c-a2`, `--c-ab`, `--c-b2`, `--c-ab2`).
- En el resolvedor, `FORMULA_HTML` guarda la fórmula general que se muestra para cada patrón;
  `identificaDesarrollo()` reconoce los productos notables y `factoriza()` los casos de
  factorización. Para añadir un patrón nuevo basta agregar su caso en una de esas dos funciones
  y su fórmula en `FORMULA_HTML`.

---

## Cómo citar

Este repositorio incluye un archivo `CITATION.cff`, de modo que GitHub muestra el botón
**Cite this repository** en la columna derecha de la página del repositorio y genera
automáticamente la cita en APA y en BibTeX. La propia actividad lleva un bloque de créditos
al pie, con botones para copiar la cita.

**APA (7.ª edición)**

> Castillo Márquez, D. I. (2026). *Productos notables: la demostración que se ve*
> (Versión 1.1) [Material didáctico interactivo]. Universidad Autónoma de Nayarit,
> Unidad Académica de Ciencias Básicas e Ingenierías. https://doi.org/10.5281/zenodo.23195334

**BibTeX**

```bibtex
@misc{castillo2026productosnotables,
  author       = {Castillo Márquez, Dalia Imelda},
  title        = {{Productos notables: la demostración que se ve}},
  year         = {2026},
  version      = {1.1},
  howpublished = {Material didáctico interactivo},
  institution  = {Universidad Autónoma de Nayarit, Unidad Académica de Ciencias Básicas e Ingenierías},
  doi          = {10.5281/zenodo.23195334},
  url          = {https://daliacastillo.github.io/productos-notables/},
  note         = {ORCID: 0000-0002-5890-0437. Licencia CC BY-NC-SA 4.0}
}
```

> Las direcciones ya apuntan a la cuenta `daliacastillo`. Si alguna vez cambia el nombre del
> repositorio, actualice `CITATION.cff`, `LICENSE` y la constante `OBRA.urlFija` del script, al
> final de `index.html`. Cuando la página se sirve por HTTPS (GitHub Pages), la dirección real se
> detecta sola y el bloque de créditos la muestra actualizada.

### DOI (Zenodo)

La obra está archivada en Zenodo, de modo que su cita es permanente aunque el repositorio cambie
de nombre o de lugar. Hay **dos DOI** y conviene saber cuál usar:

| DOI | Qué identifica | Cuándo usarlo |
|---|---|---|
| [10.5281/zenodo.23195334](https://doi.org/10.5281/zenodo.23195334) | Todas las versiones (*concept DOI*) | **El de uso general.** Siempre resuelve a la versión más reciente; es el que va en la cita, en la insignia y en el currículum |
| [10.5281/zenodo.23195335](https://doi.org/10.5281/zenodo.23195335) | Sólo la versión 1.1.0 | Cuando haga falta citar exactamente la versión que se usó, por ejemplo en un artículo que reporte resultados obtenidos con ella |

Zenodo toma la autoría, el resumen, las palabras clave y la licencia del archivo `CITATION.cff`,
así que ese archivo es la fuente de la que depende la calidad del registro.

**Para publicar una versión nueva** basta crear otra *release* en GitHub (por ejemplo `v1.2.0`):
Zenodo la archiva sola, emite un DOI de versión nuevo y el DOI de concepto pasa a apuntar a ella.
Antes de hacerlo conviene actualizar `version:` y `date-released:` en `CITATION.cff`.

**Enlazarlo al perfil ORCID:** en [orcid.org](https://orcid.org) → *Works → Add works → Search & link*,
elija **DataCite** y busque el DOI; o bien *Add manually* pegando el DOI. Zenodo también puede
hacerlo solo si en su perfil de Zenodo está conectada la cuenta ORCID.

## Metadatos incluidos

- `CITATION.cff` — citación legible por máquina (botón *Cite this repository* de GitHub).
- Etiquetas `citation_*` y `DC.*` en el `<head>` — las usan Google Académico y los recolectores
  de repositorios institucionales.
- `JSON-LD` con `schema.org/LearningResource` — describe la obra como recurso educativo:
  autoría, ORCID, afiliación, nivel educativo, licencia, versión y DOI.
- Etiqueta `citation_doi` y `DC.identifier` en el `<head>`, y el DOI visible en el bloque de
  créditos de la propia actividad.

## Créditos y licencia

Dra. Dalia Imelda Castillo Márquez · Docente investigadora
ORCID: [0000-0002-5890-0437](https://orcid.org/0000-0002-5890-0437)
Universidad Autónoma de Nayarit · Unidad Académica de Ciencias Básicas e Ingenierías
DOI: [10.5281/zenodo.23195334](https://doi.org/10.5281/zenodo.23195334)

Versión 1.1 · octubre de 2026

Obra bajo licencia
[Creative Commons Atribución-NoComercial-CompartirIgual 4.0 Internacional (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es).
Puede compartirse y adaptarse con fines no comerciales, dando crédito a la autora y distribuyendo
las obras derivadas bajo la misma licencia. Véase `LICENSE`.
