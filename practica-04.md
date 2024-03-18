Práctica 4. Descarga y preprocesa fuentes de elevación
================
<b>José-Ramón Martínez-Batlle</b> (<jmartinez19@uasd.edu.do>) <br>
Facultad de Ciencias, Universidad Autónoma de Santo Domingo (UASD) <br>
Santo Domingo, República Dominicana

<!-- Este archivo se genera a partir de otro del mismo nombre con extensión .Rmd. Por favor, edita ese archivo. -->

# Práctica 4. Descarga y preprocesa fuentes de elevación

> Fecha límite de entrega: 1 de abril, 16:00 horas.

> Entregable: documento. Entrega tu archivo vía correo electrónico en
> formato nativo. En el caso de usar software de interfaz gráfica, como
> Microsoft Word o LibreOffice Writer, entrega tanto el archivo nativo
> .docx o .odt como el PDF. En el caso de usar procesadores de texto
> como LaTeX, Overleaf, RMmarkdown, entrega tanto el PDF como la carpeta
> (comprimida en ZIP) conteniendo los archivos necesarios para compilar
> el PDF.

## EJERCICIO 1: Descarga un modelo digital de elevaciones y represéntalo

> En lo adelante, usaré las siglas DEM, de *digital elevation model*,
> para referirme al modelo digital de elevaciones del Shuttle Radar
> Topography Mission (SRTM).

<table class="table table-hover table-condensed" style="margin-left: auto; margin-right: auto;">
<caption>
</caption>
<thead>
<tr>
<th style="text-align:left;">
Nombre
</th>
<th style="text-align:left;">
Poligono
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
estudiante-01
</td>
<td style="text-align:left;">
data/practica-04/poligono_a.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
estudiante-02
</td>
<td style="text-align:left;">
data/practica-04/poligono_f.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
estudiante-03
</td>
<td style="text-align:left;">
data/practica-04/poligono_k.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
estudiante-04
</td>
<td style="text-align:left;">
data/practica-04/poligono_e.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
estudiante-05
</td>
<td style="text-align:left;">
data/practica-04/poligono_c.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
estudiante-06
</td>
<td style="text-align:left;">
data/practica-04/poligono_b.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
estudiante-07
</td>
<td style="text-align:left;">
data/practica-04/poligono_j.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
estudiante-08
</td>
<td style="text-align:left;">
data/practica-04/poligono_g.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
estudiante-09
</td>
<td style="text-align:left;">
data/practica-04/poligono_d.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
estudiante-10
</td>
<td style="text-align:left;">
data/practica-04/poligono_i.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
estudiante-11
</td>
<td style="text-align:left;">
data/practica-04/poligono_h.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
estudiante-12
</td>
<td style="text-align:left;">
data/practica-04/poligono_l.kml
</td>
</tr>
</tbody>
</table>

Basándote en el SRTM-DEM de 1 arcosegundo (\~30 m), construye un DEM
para tu polígono asignado usando QGIS. Para lograrlo, sigue estos pasos:

- Desde el [EarthExplorer](https://earthexplorer.usgs.gov/), descarga
  las teselas (cuadros) del SRTM-DEM de 1 arcosegundo que abarquen, como
  mínimo, tu polígono asignado. Las teselas del DEM que descargarás,
  abarcarán un área mucho mayor inicialmente, pero en el ejercicio 2
  harás recortes para ajustar al área de tu polígono asignado. Para
  descargar, no uses el complemento SRTM Downloader de QGIS, pues
  necesitarás los cuadros independientes para cumplir el mandato.

- Despliega los cuadros descargados en QGIS.

- Muestra, en una captura de pantalla dentro de tu entregable, tus dos
  DEM de forma independiente, simbolizados como prefieras.

- En QGIS, construye un mosaico mediante ráster virtual (`.vrt`).

- Muestra, en una captura de pantalla dentro de tu entregable, tu
  mosaico de DEM, simbolizado como prefieras.

- Usando el tiempo pasado, ya sea en voz pasiva o en voz activa,
  *describe en un máximo de dos párrafos, con qué y cómo realizaste el
  proceso (esto es, básicamente, lo que se conoce como “materiales y
  método”) y qué obtuviste (esto es lo que se conoce como
  “resultados”)*. Recordar las recomendaciones al respecto que di en la
  [práctica 2](practica-02.md), así como en las [asignaciones de
  manuscrito 1 y 2](https://github.com/geomorfologia-202401/manuscrito).

## Ejercicio 2. Recorta y representa tu DEM

- En QGIS, recorta tu DEM para que coincida con el área de tu polígono
  asignado, por medio de menú
  `Ráster>Extracción>Cortar ráster por capa de máscara`, donde la capa
  de máscara es tu polígono asignado.

- Representa tu DEM recortado de forma que tengas la imagen de sombras
  (en el `Tipo de renderizador`, elige la opción
  `Mapa de Sombras (*hillshade*)`), y la hipsometría coloreada
  (`Tipo de renderizador`, elige la opción `Pseudocolor de monobanda`)
  mezcladas en una visualización, colocando algún tipo de rótulo que te
  ayude a reconocer el área en cuestión.

- Captura la pantalla e insértala en tu entregable.

- Usando el tiempo pasado, ya sea en voz pasiva o en voz activa,
  *describe en un máximo de dos párrafos, con qué y cómo realizaste el
  proceso (esto es, básicamente, lo que se conoce como “materiales y
  método”) y qué obtuviste (esto es lo que se conoce como
  “resultados”)*. Recordar las recomendaciones al respecto que di en la
  [práctica 2](practica-02.md), así como en las [asignaciones de
  manuscrito 1 y 2](https://github.com/geomorfologia-202401/manuscrito).

## Ejercicio 3. Aplica la herramienta *FeaturePreserveSmoothing*, de Whitebox Tools

> La herramienta *FeaturePreservingSmoothing* de Whitebox Tools, es un
> filtro de análisis geomorfométrico que reduce la rugosidad (“suaviza”
> las asperezas) generada por el ruido en el DEM. Para aplicar esta
> herramienta, instala primero el complemento Whitebox Tools de QGIS,
> descarga el ejecutable de Whitebox Tools (*Open Core*) y especifícale
> a QGIS dónde se encuentra dicho ejecutable. Tanto para instalar como
> para aplicar la herramienta, sigue las instrucciones que facilitaré en
> el aula, sugerencias de tu tutor de IA, o tutoriales en línea.

- Primero, necesitarás exportar tu DEM recortado a formato GeoTIFF, pues
  Whitebox Tools no recibe como entrada el formato ráster virtual. Para
  exportar en QGIS, haz clic derecho sobre el nombre de la capa del
  ráster virtual y, en el menú contextual, presiona
  `Exportar>Guardar como...`, en formato elige `GeoTIFF`, escribe un
  nombre de archivo/ruta y presiona `Aceptar`.

- Aplica la herramienta *FeaturePreserveSmoothing*, de Whitebox Tools a
  tu DEM recortado en formato GeoTIFF, para generar un DEM
  filtrado/suavizado. Ejecuta la herramienta desde la caja de
  herramientas de procesos de QGIS (menú
  `Procesos>Caja de herramienta`). Elije como DEM de entrada el
  recortado en formato GeoTIFF que generaste en el paso anterior. Deja
  todos los valores por defecto, sólo edita estos dos: en
  `Maximum Elevation Change [optional]` escribe `8` y en
  `Z Conversion Factor [optional]` coloca `0.000009`.

- Visualiza el DEM filtrado/suavizado y el que usaste como entrada (tu
  DEM recortado en formato GeoTIFF), usando como “renderizador” la
  opción “Mapa de Sombras (*hillshade*)”. En una oración, destaca las
  diferencias encontradas.

- Captura dos pantallas, una mostrando el DEM en formato GeoTIFF sin
  filtrado/suavizado, y otra mostrando el DEM filtrado/suavizado.
  Insértalas ambas en tu entregable.

-. Usando el tiempo pasado, ya sea en voz pasiva o en voz activa,
*describe en un máximo de dos párrafos, con qué y cómo realizaste el
proceso (esto es, básicamente, lo que se conoce como “materiales y
método”) y qué obtuviste (esto es lo que se conoce como “resultados”)*.
Recordar las recomendaciones al respecto que di en la [práctica
2](practica-02.md), así como en las [asignaciones de manuscrito 1 y
2](https://github.com/geomorfologia-202401/manuscrito).

## Criterios de evaluación y escala de valoración

| Criterio / Escala de valoración                   | Nivel 1 (En Desarrollo)                                                  | Nivel 2 (Aceptable)                                                          | Nivel 3 (Bueno)                                                                         | Nivel 4 (Excelente)                                                          |
|---------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| **Ejercicio 1: Descarga de DEM**                  | Incompleto o incorrecto                                                  | Ha descargado solo un DEM                                                    | Ha descargado ambos DEM pero falta clara visualización                                  | Ha descargado correctamente ambos DEM y se visualizan claramente             |
| **Ejercicio 1: Mosaico de DEM**                   | No ha construido el mosaico                                              | Ha construido el mosaico pero presenta errores                               | El mosaico está bien construido pero falta claridad en la visualización                 | Mosaico de DEM bien construido y visualizado claramente                      |
| **Ejercicio 2: Recorte del DEM**                  | No ha recortado el DEM                                                   | Ha recortado el DEM pero no coincide exactamente con el polígono asignado    | El DEM recortado coincide con el polígono pero falta claridad en la visualización       | DEM recortado y visualizado con precisión                                    |
| **Ejercicio 2: Representación**                   | No hay visualización de sombras ni hipsometría                           | Sólo una de las visualizaciones (sombra o hipsometría) está presente         | Ambas visualizaciones están presentes pero sin mezcla o claridad adecuada               | Perfecta mezcla de imagen de sombras y hipsometría con rótulo claro          |
| **Ejercicio 3: Uso de FeaturePreserveSmoothing**  | No ha aplicado la herramienta                                            | Ha intentado aplicar la herramienta pero hay errores evidentes               | Ha aplicado la herramienta pero no ha logrado la correcta configuración o visualización | Aplicación perfecta de la herramienta con claridad en los resultados         |
| **Ejercicio 3: Comparación de DEMs**              | No hay comparación o está incorrecta                                     | La comparación está presente pero es vaga                                    | La comparación es clara pero carece de detalles específicos                             | Comparación detallada y clara entre el DEM original y filtrado               |
| **Calidad de la Redacción (Materiales y Método)** | Redacción poco clara, con errores y falta de estructura                  | Redacción básica con algunos errores y falta de cohesión                     | Redacción clara y bien estructurada, con mínimos errores                                | Redacción excelente, coherente, detallada y sin errores                      |
| **Calidad de la Redacción (Resultados)**          | Resultados poco claros o incorrectos, con errores de redacción           | Resultados presentados de manera básica, con algunos errores                 | Resultados bien presentados y claros, con pocos errores                                 | Excelente presentación de resultados, detallada y sin errores                |
| **Presentación y Formato del Documento**          | El entregable está desordenado y falta alguno de los formatos requeridos | El entregable presenta todos los formatos pero está desordenado o poco claro | El entregable es ordenado pero puede mejorar en detalles                                | El entregable es claro, ordenado y cumple con todos los formatos solicitados |

## Referencias
