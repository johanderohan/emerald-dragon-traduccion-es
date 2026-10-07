# Emerald Dragon — Traducción al castellano

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/pc-engine-cd/emerald-dragon)**.

Traducción al **español de España** de *Emerald Dragon* para **PC Engine Super CD-ROM²**, desarrollada sobre la edición japonesa **Rev 1**.

Se distribuye como **parche**. Necesitas tu propia copia del juego; la descarga no incluye el disco ni la BIOS.

## Estado

Última versión: **[v1.0 — Primera edición castellana](../../releases/tag/v1.0)**. Disponible y en revisión durante la partida.

Se han comprobado en **Beetle PCE Fast** el arranque, una partida nueva, la narración, varias conversaciones, los menús, el guardado y la carga de una partida, el inventario y un combate dirigido. También se han recorrido completas tres escenas habladas afectadas por los cambios del motor. Se han corregido los campos internos que recortaban Guardar y alteraban Cambiar/Tirar.

La revisión en emulador es **parcial**: no se ha completado una partida de principio a fin ni probado una consola física. El cotejo íntegro del doblaje queda pendiente. Los cambios de mapa, combate y escenas se han probado también mediante las funciones de desarrollo del juego, activadas únicamente en la RAM de las sesiones de prueba.

La pista traducida v1.0 debe tener MD5 **`94ad9c6ec6ac60dfbe2d294d215432e8`** y SHA-256 **`b2f3fa2082471dfc4ee92b068dda400732eef176a72ba800166cbf8a670ee14b`**. El paquete incluye las huellas del original, del resultado y del parche.

## Traducción

El proyecto incluye el guion, las descripciones de objetos, los menús, los mensajes de combate y subtítulos para las escenas habladas. Las voces y la música se conservan en japonés. El título se mantiene en inglés, con el diseño de Stargood.

La traducción se ha redactado desde el japonés con una biblia editorial, glosario y revisión de nombres, tratamientos, indicaciones de ruta y puzles. Se incorporan **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿** a las fuentes del juego, respetando sus colores.

El trabajo de texto abarca **5.314 entradas canónicas** y **232 rótulos visibles**. Son unidades del sistema de edición: incluyen diálogos, nombres, instrucciones, créditos y pausas. Los duplicados se insertan conservando sus referencias originales. Los **585 registros de subtítulos**, incluidas 20 pausas, se han comprobado con el motor real a un máximo de dos líneas por pantalla.

La extracción se cotejó con la Rev 1: los **14.674 registros originales** coinciden exactamente con una extracción nueva del disco. Se recuperaron ocho entradas japonesas que el texto de referencia dejaba vacías. Trece fragmentos truncados o mezclados del extractor quedan documentados aparte y no se cuentan como traducción terminada.

## Aplicar el parche

1. Conserva una copia intacta del juego japonés **Rev 1**, en formato **BIN/CUE con 31 pistas**.
2. Comprueba la pista de datos:

   | Dato | Valor |
   |---|---|
   | Archivo | `Emerald Dragon (Japan) (Rev 1) (Track 02).bin` |
   | Tamaño | **116.506.320 bytes** |
   | MD5 | `0ba5d167f87152fc5341246fd18670a1` |
   | SHA-256 | `80ff18df41e41e375d9ff0c01b8a549b195e52921f993ad03fbb68f8ddd73925` |

3. Descarga el paquete del parche desde **[Releases](../../releases)** y extrae el archivo `.xdelta`.
4. Duplica la carpeta completa del juego. Aplica el parche a la **pista 02 original**, con [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases) o xdelta3, y guarda el resultado en la carpeta duplicada con el **mismo nombre de la pista 02**.
5. Conserva allí el CUE y las otras 30 pistas. Abre el **CUE** de esa copia en el emulador y utiliza una System Card 3.0 compatible con Super CD-ROM².

Ejemplo, desde la carpeta original, con otra carpeta de salida ya preparada:

```bash
xdelta3 -d -s "Emerald Dragon (Japan) (Rev 1) (Track 02).bin" \
  Emerald_Dragon_es-ES.xdelta \
  "../Emerald Dragon castellano/Emerald Dragon (Japan) (Rev 1) (Track 02).bin"
```

El parche modifica únicamente la pista de datos. **No lo apliques a la primera edición japonesa, a una ISO de 2048 bytes por sector, a un CHD ni a una copia previamente parcheada.** Cada actualización se aplica sobre la pista 02 Rev 1 original. Las pruebas se realizan con partidas nuevas; no reutilices estados de emulador de otra versión del juego o del parche.

## Criterios de traducción

Nombres principales: Atorushan, Tamrin, Haslam, Falna, Hosrou, Bagin, Yaman y Saoshyant. Se usa **Dones Esmeralda** para los cinco objetos que articulan la historia; **pulsos** para la moneda, **PV** para puntos de vida y **PA** para puntos de acción.

La biblia y el glosario completos acompañan a las fuentes del paquete. La traducción y sus revisiones han contado con asistencia de IA. Los textos del disco se contrastaron con japonés extraído; las escenas habladas parten de transcripciones japonesas y mantienen algunos matices anotados para una revisión de audio completa.

## Créditos y fuentes

- **Edición castellana:** proyecto de [johanderohan](https://github.com/johanderohan).
- **Herramientas, motor de texto y subtítulos:** Supper, [Stargood Translations](https://stargood.org/trans/emdr.php), proyecto [emdrtools](https://github.com/suppertails66/emdrtools).
- **Revisión y pruebas de la edición inglesa original:** cccmar y Oddoai-sama. Estos créditos no implican que hayan revisado esta edición castellana.

Se conserva la licencia GPLv3 y las excepciones de la infraestructura utilizada. El paquete incorpora las modificaciones y fuentes correspondientes para reconstruir la edición castellana, sin distribuir el guion inglés ni los archivos del juego.

## Aviso

Traducción realizada por afición, sin relación con Glodia, Alfa System, Media Works ni NEC Home Electronics. Los derechos del juego pertenecen a sus titulares. Si detectas un fallo, abre una incidencia indicando el lugar, el texto y, si es posible, una captura y la versión del parche.
