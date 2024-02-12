Práctica 4. Descarga y preprocesa fuentes de elevación
================
<b>José-Ramón Martínez-Batlle</b> (<jmartinez19@uasd.edu.do>) <br>
Facultad de Ciencias, Universidad Autónoma de Santo Domingo (UASD) <br>
Santo Domingo, República Dominicana

<!-- Este archivo se genera a partir de otro del mismo nombre con extensión .Rmd. Por favor, edita ese archivo. -->

> Fecha límite de entrega: 15 de octubre, 23:59 horas.

> Entregable: documento. Entrega tu archivo vía correo electrónico en
> formato nativo. En el caso de usar software de interfaz gráfica, como
> Microsoft Word o LibreOffice Writer, entrega tanto el archivo nativo
> .docx o .odt como el PDF. En el caso de usar procesadores de texto
> como LaTeX, Overleaf, RMmarkdown, entrega tanto el PDF como la carpeta
> (comprimida en ZIP) conteniendo los archivos necesarios para compilar
> el PDF.

## EJERCICIO 1: Descarga un modelo digital de elevaciones y represéntalo

> En lo adelante, usaré las siglas DEM, de *digital elevation model*,
> para referirme al modelo digital de elevaciones.

Basándote en el SRTM-DEM de 1 arcosegundo, construye un DEM para tu
polígono asignado usando QGIS

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
Debora Ayala Nolasco
</td>
<td style="text-align:left;">
data/practica-04/poligono_7.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
Ernesto Vladimir Santana Martinez
</td>
<td style="text-align:left;">
data/practica-04/poligono_6.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
Frank Félix De la Cruz Díaz
</td>
<td style="text-align:left;">
data/practica-04/poligono_1.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
Gregorio Rivas V
</td>
<td style="text-align:left;">
data/practica-04/poligono_11.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
Iliana Santiago
</td>
<td style="text-align:left;">
data/practica-04/poligono_4.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
Joel Benjamin Perez Garcia
</td>
<td style="text-align:left;">
data/practica-04/poligono_3.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
José Ramón Martínez Batlle
</td>
<td style="text-align:left;">
data/practica-04/poligono_2.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
Maria Dolores Alvarado Florimon
</td>
<td style="text-align:left;">
data/practica-04/poligono_5.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
Mayki Morel
</td>
<td style="text-align:left;">
data/practica-04/poligono_9.kml
</td>
</tr>
<tr>
<td style="text-align:left;">
Reynaldo Rafael Espaillat Santos
</td>
<td style="text-align:left;">
data/practica-04/poligono_10.kml
</td>
</tr>
</tbody>
</table>

Sigue estos pasos:

1.  Desde el [EarthExplorer](https://earthexplorer.usgs.gov/), descarga
    los dos cuadros del SRTM-DEM de 1 arcosegundo que abarquen, como
    mínimo, tu polígono asignado. Los cuadros abarcarán un área mucho
    mayor inicialmente, pero luego lo recortarás. Para descargar, no
    uses el complemento SRTM Downloader de QGIS, pues necesitarás los
    cuadros independientes para cumplir el mandato.

2.  Despliega los cuadros descargados en QGIS.

3.  Muestra, en una captura de pantalla dentro de tu entregable, tus dos
    DEM de forma independiente, simbolizados como prefieras.

4.  En QGIS, construye un mosaico mediante ráster virtual (`.vrt`).

5.  Muestra, en una captura de pantalla dentro de tu entregable, tu
    mosaico de DEM, simbolizado como prefieras.

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

## Criterios de evaluación y escala de valoración

| Criterio / Escala de valoración                  | Nivel 1 (En desarrollo)                                                  | Nivel 2 (Aceptable)                                                          | Nivel 3 (Bueno)                                                                         | Nivel 4 (Excelente)                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| **Ejercicio 1: Descarga de DEM**                 | Incompleto o incorrecto                                                  | Ha descargado solo un DEM                                                    | Ha descargado ambos DEM pero falta clara visualización                                  | Ha descargado correctamente ambos DEM y se visualizan claramente             |
| **Ejercicio 1: Mosaico de DEM**                  | No ha construido el mosaico                                              | Ha construido el mosaico pero presenta errores                               | El mosaico está bien construido pero falta claridad en la visualización                 | Mosaico de DEM bien construido y visualizado claramente                      |
| **Ejercicio 2: Recorte del DEM**                 | No ha recortado el DEM                                                   | Ha recortado el DEM pero no coincide exactamente con el polígono asignado    | El DEM recortado coincide con el polígono pero falta claridad en la visualización       | DEM recortado y visualizado con precisión                                    |
| **Ejercicio 2: Representación**                  | No hay visualización de sombras ni hipsometría                           | Sólo una de las visualizaciones (sombra o hipsometría) está presente         | Ambas visualizaciones están presentes pero sin mezcla o claridad adecuada               | Perfecta mezcla de imagen de sombras y hipsometría con rótulo claro          |
| **Ejercicio 3: Uso de FeaturePreserveSmoothing** | No ha aplicado la herramienta                                            | Ha intentado aplicar la herramienta pero hay errores evidentes               | Ha aplicado la herramienta pero no ha logrado la correcta configuración o visualización | Aplicación perfecta de la herramienta con claridad en los resultados         |
| **Ejercicio 3: Comparación de DEMs**             | No hay comparación o está incorrecta                                     | La comparación está presente pero es vaga                                    | La comparación es clara pero carece de detalles específicos                             | Comparación detallada y clara entre el DEM original y filtrado               |
| **Presentación y formato**                       | El entregable está desordenado y falta alguno de los formatos requeridos | El entregable presenta todos los formatos pero está desordenado o poco claro | El entregable es ordenado pero puede mejorar en detalles                                | El entregable es claro, ordenado y cumple con todos los formatos solicitados |

## Referencias
