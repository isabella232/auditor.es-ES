---
description: Esta referencia proporciona más información sobre las alertas que el Auditor muestra para las pruebas.
seo-description: Esta referencia proporciona más información sobre las alertas que el Auditor muestra para las pruebas.
seo-title: Alertas
title: Alertas
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: tm+mt
source-git-commit: 762ff31ca4d5ed69d1b813589e419c51a40d5920

---


# Alertas{#alerts}

Esta referencia proporciona más información sobre las alertas que el Auditor muestra para las pruebas.

Las alertas muestran los problemas que debe tener en cuenta, pero que no afectan a su puntuación. Estas son recomendaciones de mejores prácticas que, en algunos casos, pueden no aplicarse a su implementación.

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Prueba </th> 
   <th colname="col2" class="entry"> Criterios </th> 
   <th colname="col3" class="entry"> Recomendación </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud: se implementó la etiqueta de conversión correcta</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Compruebe si se utiliza la etiqueta de conversión correcta. </p> <p> <p>Advertencia:  El uso de etiquetas de conversión TubeMogul obsoletas puede provocar la pérdida de datos. </p> </p> </td> 
   <td colname="col3"> <p>Actualice los píxeles de conversión a las nuevas etiquetas de conversión solo de imagen de Advertising Cloud. </p> <p>Esto se puede lograr fácilmente con la extensión de lanzamiento de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud: se usa la etiqueta JS correcta</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud debe utilizar las últimas etiquetas de JavaScript. </p> </td> 
   <td colname="col3"> <p>Actualice el JavaScript de Advertising Cloud a la versión más reciente. El uso de las versiones de JavaScript obsoletas puede provocar la pérdida de funcionalidad. </p> <p>Esto se puede lograr más fácilmente mediante el uso de la extensión de lanzamiento de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud: etiqueta de solo imagen</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>El formato de píxel de imagen de Advertising Cloud debe coincidir con uno de los siguientes formatos recomendados: </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;VALOR_HASH&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;VALOR_HASH&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Actualice los píxeles de Advertising Cloud a las nuevas etiquetas de solo imagen de Advertising Cloud, lo que le garantiza que aprovechará toda la funcionalidad de Advertising Cloud. </p> <p>Esto se puede lograr fácilmente con la extensión de lanzamiento de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud: Píxeles de segmento: sincronización DSP habilitada</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Compruebe si el píxel del segmento TubeMogul contiene un ajuste de sincronización de DSP y recomiende que el ajuste se añada al píxel. </p> <p>La configuración de sincronización de DSP está determinada por el uso de un parámetro de cadena de consulta, por lo que </p> <p>SI la etiqueta se está activando en<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> O <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> O <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>Y la etiqueta contiene el parámetro de URL <span class="codeph"> "sid=")</span> </p> <p>A CONTINUACIÓN, compruebe si el parámetro de URL <span class="codeph"> "cs=0"</span> o<span class="codeph"> "cs=1"</span> existe y, si no, recomiende que <span class="codeph"> "cs=1"</span> se agregue a esos píxeles para que las tasas de coincidencia de audiencia puedan mejorar. </p> </td> 
   <td colname="col3"> <p> Agregue el parámetro de URL <span class="codeph"> "cs=1"</span> a los píxeles de Advertising Cloud para que se pueda sincronizar con DSP, lo que aumenta las tasas de coincidencia de audiencia. </p> <p>Esto se puede lograr fácilmente con la extensión de lanzamiento de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    </draft-comment> <p><b>DTM: colocación de la devolución de llamada pageBottom</b> </p> <p>Peso: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Información adicional</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>La administración dinámica de etiquetas requiere la función <span class="codeph"> _satellite.pageBottom()</span> . Agregue la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la funcionalidad adecuada de la DTM. </p> <p> <p>Nota: Se recomienda que la etiqueta sea la <i>última</i> etiqueta en el <span class="codeph"> &lt;body&gt;</span>. Si se encuentra dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span> , tiene la posibilidad de funcionar, pero como no es una práctica recomendada, podría funcionar incorrectamente o con resultados inesperados o no deseados. </p> </p> </td> 
   <td colname="col3"> <p>Agregue la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la funcionalidad adecuada de la DTM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - Alojado automáticamente</b> </p> <p>Peso: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/deployment.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> La biblioteca de la DTM se aloja en la instancia de Adobe Akamai en <span class="filepath"> assets.adobedtm.com</span>. </p> <p> El autoalojamiento es el método recomendado para cargar la DTM, ya que proporciona un mayor control del rendimiento del sitio web mediante el control de caché, la reducción de las dependencias de scripts de terceros y un mayor control del proceso de publicación. Las bibliotecas de la DTM se pueden alojar y administrar a través de su propio alojamiento web o CDN. </p> </td> 
   <td colname="col3"> <p>El alojamiento propio es el método recomendado para cargar la DTM en una página. Aunque el alojamiento de DTM a través de la CDN de Akamai funciona en la mayoría de los casos, el autoalojamiento mejora el rendimiento de la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Servicio de ID de Experience Cloud: use solo una AdobeOrg</b> </p> <p>Peso: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_id_request.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p>En una implementación MCID normal, se debe utilizar un solo AdobeOrg. </p> </td> 
   <td colname="col3"> <p>Valide que existan varios ID de AdobeOrg para esta implementación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - pageColocación de llamada de retorno inferior</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Información adicional</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>Launch debe tener una <span class="codeph"> función de </span>llamada de retorno pageBottom definida en último lugar en el cuerpo de la página si se implementa sincrónicamente. </p> <p> <p>Nota: Se recomienda que la etiqueta sea la <i>última</i> etiqueta en el <span class="codeph"> &lt;body&gt;</span>. Si se encuentra dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span> , tiene la posibilidad de funcionar, pero como no es una práctica recomendada, podría funcionar incorrectamente o con resultados inesperados o no deseados. </p> </p> </td> 
   <td colname="col3"> <p>Launch requiere la <span class="codeph"> función _satellite.pageBottom()</span> para implementaciones sincrónicas. Agregue la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la funcionalidad de Launch adecuada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Inicio: autoalojado</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Introducción a Launch</a> </p> <p><a href="https://docs.adobelaunch.com/client-side-information/asynchronous-deployment" format="https" scope="external"> Iniciar implementación asincrónica</a> </p> </td> 
   <td colname="col2"> <p>La biblioteca de Launch se aloja en la instancia de Adobe Akamai en <span class="filepath"> assets.adobedtm.com</span>. </p> <p>El autoalojamiento es el método recomendado para cargar Launch, ya que proporciona un mayor control del rendimiento del sitio web mediante el control de caché, la reducción de las dependencias de scripts de terceros y un mayor control del proceso de publicación. Las bibliotecas de Launch se pueden alojar y administrar a través de su propio alojamiento web o CDN. </p> </td> 
   <td colname="col3"> <p>Aunque el alojamiento de Launch a través de la CDN de Akamai funciona en la mayoría de los casos, se recomienda implementar el alojamiento propio como el primer paso para mejorar el rendimiento de la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch: debe implementarse asincrónicamente</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p>Launch debe implementarse asincrónicamente para obtener un rendimiento óptimo. </p> </td> 
   <td colname="col3"> <p>Incluya el parámetro async en la secuencia de comandos en línea para garantizar la funcionalidad de inicio asincrónico adecuada </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target: contenido en mboxDefault</b> </p> <p>Peso: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> El contenido debe existir en mboxDefault al usar at.js. </p> </td> 
   <td colname="col3"> <p>Compruebe que el contenido está disponible. </p> </td> 
  </tr> 
 </tbody> 
</table>

