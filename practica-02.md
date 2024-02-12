Practica 2. Geomorfometría, reproducibilidad, redacción, estilos de
formato, figuras, tablas, citas y referencias
================
<b>José-Ramón Martínez-Batlle</b> (<jmartinez19@uasd.edu.do>) <br>
Facultad de Ciencias, Universidad Autónoma de Santo Domingo (UASD) <br>
Santo Domingo, República Dominicana

<!-- README.md se genera a partir de README.Rmd. Por favor, edita ese archivo. -->

> Fecha de entrega: 1 de octubre, 23:59 horas.

Comenzarás tu manuscrito con la asignación de la próxima semana, y con
esta práctica vas a “calentar motores”. Tanto el fondo como la forma de
dicho ensayo son importantes. En cuanto al fondo, es decir, el tema y su
desarrollo, tratará **sobre geomorfometría de un área de República
Dominicana**. En cuanto a la forma, deberás lograr una investigación
reproducible y bien redactada, presentando un documento que cumpla con
estilos de formato, uso apropiado de figuras, tablas, citas y
referencias. Esta práctica, en sus dos partes, constituye un apoyo para
mejorar tus habilidades de manejar datos y presentarlos con nivel
científico, antes de que comiences a redactar formalmente tú manuscrito.
Vamos allá.

## Parte 1. Calcular una sencilla pendiente y redactar.

1.  Ve a [rdrr.io](https://rdrr.io/snippets/) y genera una matriz de
    datos 3x3 con el código que te dejo a continuación. La matriz que
    generarás no será igual a la que te muestro abajo, y cada corrida
    genera matrices diferentes. Asimismo, el código pegado abajo,
    representa la matriz en forma de un ráster. IMPORTANTE: ¡captura la
    pantalla tras ejecutar el código! (pregunta a un tutor de
    inteligencia artificial cómo hacerlo)

``` r
d <- matrix(#Estas líneas generan la matriz
  data = floor(x = rnorm(n = 9, mean = sample(50:2000)[1], sd = 50)),
  nrow=3, ncol=3)
d #Imprime la matriz
library(raster) #Carga paquete raster
plot(raster(d)) #Muestra la matriz en forma de un ráster
```

2.  Con la matriz que obtengas, calcula la pendiente por el método
    Evans-Young, tal cual se explica en la página 10 de Hengl et al.
    (2009). Usa todos los apoyos que necesites, desde una simple
    calculadora de mano u hojas de cálculo, hasta inteligencia
    artificial (IA). Si usas IA, no le pidas que te resuelva el
    ejercicio pasándole el mandato tal cual y luego copiando pegando.
    Más bien, pídele que te explique cómo resolverlo y hazlo por tu
    cuenta (modo tutor).

3.  Redacta un documento sobre este ejercicio, un miniensayo. Deberás
    usar estilos de formato (“Título 1”, “Normal”, etc.), y no podrás
    usar listas de viñetas ni listas numeradas.

> **RECUADRO: recomendaciones básicas de redacción**
>
> Usa una voz (activa o pasiva) de forma consistente, pero sólo ten
> presente que la redacción de manuscritos científicos a menudo se
> utilizan ambas voces, dependiendo del contexto y el mensaje que el/la
> autor/a quiera transmitir. Veamos algunos ejemplos:
>
> **Voz activa en manuscrito científicos:**
>
> -   **Analicé** los datos utilizando el software R.
>
> -   El experimento **mostró** que la temperatura afecta directamente
>     la tasa de reacción.
>
> -   Los investigadores **encontraron** una correlación significativa
>     entre las dos variables.
>
> La voz activa puede hacer que la redacción parezca más directa y
> clara, y es especialmente útil cuando el/la autor/a quiere enfatizar
> quién llevó a cabo una acción o cuándo se desea hacer una afirmación
> fuerte.
>
> **Voz pasiva en artículos científicos:**
>
> -   Los datos **fueron analizados** utilizando el software R.
>
> -   **Se observó** que la temperatura afecta directamente la tasa de
>     reacción.
>
> -   Una correlación significativa **fue encontrada** entre las dos
>     variables.
>
> La voz pasiva es común en la redacción científica porque a menudo se
> prefiere un tono más impersonal, enfocando la atención en los
> resultados y procedimientos en lugar de en quienes llevaron a cabo la
> investigación. También puede ser útil cuando no se quiere o no es
> relevante especificar quién realizó la acción.
>
> **En todas mis prácticas, está completamente permitido usar IA
> (e.g. chatGPT), pero te recomiendo que la uses más como tutor que como
> redactor**. Tal como te sugerí arriba, no le pidas que te resuelva los
> problemas del mandato. Pídele que te dé ideas, y que luego tú las
> mejores o las descartes. No abuses tampoco del texto, pues mucha
> redacción no siempre es mejor; en redacción de ensayos “menos es más”.
> Cruza las redacciones que te ofrezca con tu conocimiento, y revisa si
> los términos o conceptos usados son descabellados (toda IA se inventa
> cosas, cuidate de no caer en esa trampa). Nunca le pidas referencias
> bibliográficas, porque se va equivocar.

Distribuye tu texto en las siguientes cinco secciones:

-   **Introducción** (tamaño recomendado: 3 párrafos). Desde lo amplio,
    comienza escribiendo sobre geomorfometría (qué es). A continuación,
    explica que es la pendiente, su importancia, por qué es necesario
    calcularla, para qué se usa. Plantea tu o tus objetivos, que en este
    caso son bastante sencillos. Cierra con la importancia del cálculo
    de la pendiente respecto del conjunto de la ciencia.

    Dentro de esta sección, debes incluir al menos tres citas. Los
    conceptos y afirmaciones ajenas, deben citarse bibliográficamente, y
    nunca deberás usar cita literal, pues se considera plagio. Las citas
    bibliográficas que incluyas, deberán estar respaldadas por sus
    correspondientes cuyas referencias, que deberán aparecer en la
    sección final (Referencias). Las citas y la lista de referencias,
    deberán seguir el estándar APA 7ma edición (APA7). Es casi
    imprescindible que uses un gestor de citas y referencias, como
    Zotero.

-   **Materiales y métodos** (tamaño recomendado: 2 párrafos). Explica
    cómo obtuviste los datos que usaste, y describe brevemente el método
    Evans-Young y cómo lo aplicaste. Dentro de la redacción, debes
    incluir al menos dos citas. También deberás incluir la matriz de
    datos en forma de tabla, y también deberás mostrarla en forma de una
    figura (“Figura 1”), y la o las fórmulas empleadas (no adelantes
    resultados, es decir, no des el resultado de la pendiente calculada,
    simplemente explica cómo la calculaste). La tabla, la figura y la
    cita debes referirlas en el texto (“ver tabla X”), usando un sistema
    de referencia cruzada asistido por el procesador de texto que uses
    (pregunta a tu tutor de inteligencia artificial de preferencia cómo
    insertar títulos a tablas y figuras, y cómo referirlos en el texto;
    también pregúntale cómo insertar y referir fórmulas).

-   **Resultados** (tamaño recomendado: 1 párrafo). El cálculo de
    pendiente que obtuviste, presentándolo en sus respectivas
    componentes. No hagas valoraciones en esta sección, simplemente
    incluye el resultado obtenido.

-   **Discusión** (tamaño recomendado: 2 párrafos). Abre la discusión
    indicando si alcanzaste tus objetivos. Describe por qué era
    importante alcanzarlos. Comenta sobre las limitacines, de cualquier
    tipo, ya sea las limitaciones de los datos, de la técnicas, de los
    objetivos de aprendizaje. Cierra indicando qué desafíos futuros
    quedan abiertos tras este trabajo.

-   **Referencias**. Las referencias que hayas citado arriba, las
    deberás incluir aquí en formato APA 7ma edición.

## Parte 2. Elige una técnica y un sistema geomorfológico, y justifícalos

1.  Revisa demostraciones y aplicaciones de geomorfometría en Hengl
    et al. (2009). Usarás una técnica geomorfométrica (por ejemplo,
    acumulación de flujo, clasificación del relieve) para aplicarla a un
    sistema geomorfológico dominicano (por ejemplo, un río, un karst,
    una vertiente). Es una decisión importante, porque será el mismo
    tema que desarrollarás en tu manuscrito. Guíate de las listas a
    continuación, y de las demostraciones que encontrarás en el libro
    citado. Algunas recomendaciones viables:

-   Tecnica geomorfométrica:

    -   Parámetros básicos de la superficie del terreno (locales y
        regionales). Capítulo 6 de Hengl et al. (2009).

    -   Parámetros de la superficie del terreno y objetos hidrológicos.
        Capítulo 7 de Hengl et al. (2009).

    -   Parámetros de la superficie del terreno para topoclimas.
        Capítulo 8 de Hengl et al. (2009).

    -   Formas y formas elementales. Capítulo 10 de Hengl et al. (2009).

-   Sistemas geomorfológicos:

    -   Fluvial (ríos y relacionados).

    -   De vertiente.

    -   Litoral y costa.

    -   Eólico.

    -   Kárstico

2.  Elige la técnica y el sistema geomorfológico que usarás, y
    justifícalo.

-   Tecnica geomorfométrica elegido:

-   Sistema geomorfológico elegido:

-   Justificación:

## Criterios de evaluación y escala de valoración

| Criterio                                             | Insatisfactorio (0-1)                            | Básico (2-3)                                     | Competente (4-5)                                                 | Avanzado (6-7)                               | Experto (8-10)                                          |
|------------------------------------------------------|--------------------------------------------------|--------------------------------------------------|------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------|
| **Geomorfometría**                                   |                                                  |                                                  |                                                                  |                                              |                                                         |
| Cálculo de pendiente por método Evans-Young          | No realiza cálculo                               | Realiza cálculo con errores                      | Cálculo realizado correctamente                                  | Cálculo detallado y preciso                  | Cálculo experto con justificación                       |
| **Reproducibilidad**                                 |                                                  |                                                  |                                                                  |                                              |                                                         |
| Uso de datos y código                                | No muestra datos o código                        | Muestra datos pero no código                     | Muestra ambos pero con falta de claridad                         | Usa datos y código de manera clara           | Usa datos y código con perfecta claridad y reproducción |
| **Redacción**                                        |                                                  |                                                  |                                                                  |                                              |                                                         |
| Claridad y estructura del texto                      | Texto confuso sin estructura, voz no consistente | Redacción básica con errores, voz no consistente | Redacción clara con estructura, voz consistente pero con errores | Texto muy bien estructurado, voz consistente | Redacción impecable y articulada, voz consistente       |
| **Estilos de formato**                               |                                                  |                                                  |                                                                  |                                              |                                                         |
| Uso de estilos en el documento                       | No utiliza estilos                               | Usa estilos pero no consistentemente             | Usa estilos consistentemente                                     | Usa estilos de manera avanzada               | Usa estilos con maestría                                |
| **Figuras, tablas y fórmulas**                       |                                                  |                                                  |                                                                  |                                              |                                                         |
| Presentación e integración en el texto               | No incluye figuras, tablas o fórmulas            | Incluye pero no las referencia correctamente     | Incluye y referencia adecuadamente                               | Uso avanzado y preciso de figuras y tablas   | Presentación experta y perfectamente integrada          |
| **Citas y Referencias**                              |                                                  |                                                  |                                                                  |                                              |                                                         |
| Uso del formato APA7                                 | No utiliza APA7                                  | Usa APA7 pero con errores                        | Usa APA7 con mínimos errores                                     | Usa APA7 casi perfectamente                  | Uso experto y perfecto de APA7                          |
| **Técnica geomorfométrica y sistema geomorfológico** |                                                  |                                                  |                                                                  |                                              |                                                         |
| Elección y justificación                             | No elige o justifica                             | Elección sin justificación                       | Elección con justificación básica                                | Elección con buena justificación             | Elección con justificación experta                      |

## Referencias

<div id="refs" class="references csl-bib-body hanging-indent"
line-spacing="2">

<div id="ref-hengl2009geomorphometry" class="csl-entry">

Hengl, T., Reuter, H. I. y Institute for Environment and Sustainability
(European Commission. Joint Research Centre) (Eds.). (2009).
*Geomorphometry: concepts, software, applications* (1st ed). Elsevier.

</div>

</div>
