---
description: 'null'
seo-description: 'null'
seo-title: Prueba de la regla 0.0.8
title: Prueba de la regla 0.0.8
uuid: c62b7169-a650-4650-876f-c254eb57cb25
translation-type: tm+mt
source-git-commit: b56d3d2bd79c812fda6a75827d14044d9a8a3b4c

---


# Prueba de la regla 0.0.8{#test-rubric}

## Prueba de la regla 0.0.8

<!-- Note to writer: Please review the tables on this page for formatting and accuracy. Compare to original file.-->

![](assets/space.png)

## Alertas {#alerts}

Esta referencia proporciona más información sobre las alertas que el Auditor muestra para las pruebas.

Las alertas muestran los problemas que debe tener en cuenta, pero que no afectan a su puntuación.

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
    <td colname="col1"> <p><b>Advertising Cloud: se implementó la etiqueta de conversión correcta</b> </p> <p>Peso: 0 </p> </td> 
    <td colname="col2"> <p>Compruebe si se utiliza la etiqueta de conversión correcta. </p> <p> <p>Advertencia:  El uso de etiquetas de conversión TubeMogul obsoletas puede provocar la pérdida de datos. </p> </p> </td> 
    <td colname="col3"> <p>Actualice los píxeles de conversión a las nuevas etiquetas de conversión solo de imagen de Advertising Cloud. </p> <p>Esto se puede lograr fácilmente con la extensión de lanzamiento de Advertising Cloud. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud: etiqueta de solo imagen</b> </p> <p>Peso: 0 </p> </td> 
    <td colname="col2"> <p>El formato de píxel de imagen de Advertising Cloud debe coincidir con uno de los siguientes formatos recomendados: </p> <p> 
      <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
       <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;VALOR_HASH&gt;</span> </p> </li> 
       <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;VALOR_HASH&gt;</span> </p> </li> 
       <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
      </ul> </p> </td> 
    <td colname="col3"> <p>Actualice los píxeles de Advertising Cloud a las nuevas etiquetas de solo imagen de Advertising Cloud, lo que le garantiza que aprovechará toda la funcionalidad de Advertising Cloud. </p> <p>Esto se puede lograr fácilmente con la extensión de lanzamiento de Advertising Cloud. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud: Píxeles de segmento: sincronización DSP habilitada</b> </p> <p>Peso: 0 </p> </td> 
    <td colname="col2"> <p>Compruebe si el píxel del segmento TubeMogul contiene un ajuste de sincronización de DSP y recomiende que el ajuste se añada al píxel. </p> <p>La configuración de sincronización de DSP está determinada por el uso de un parámetro de cadena de consulta, por lo que </p> <p>SI la etiqueta se está activando en<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> O <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> O <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>Y la etiqueta contiene el parámetro de URL <span class="codeph"> "sid=")</span> </p> <p>A CONTINUACIÓN, compruebe si el parámetro de URL <span class="codeph"> "cs=0"</span> o<span class="codeph"> "cs=1"</span> existe y, si no, recomiende que <span class="codeph"> "cs=1"</span> se agregue a esos píxeles para que las tasas de coincidencia de audiencia puedan mejorar. </p> </td> 
    <td colname="col3"> <p> Agregue el parámetro de URL <span class="codeph"> "cs=1"</span> a los píxeles de Advertising Cloud para que se pueda sincronizar con DSP, lo que aumenta las tasas de coincidencia de audiencia. </p> <p>Esto se puede lograr fácilmente con la extensión de lanzamiento de Advertising Cloud. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM: colocación de la devolución de llamada pageBottom</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Información adicional</a> </p> 
     <draft-comment>
       TEa9df69942f404055a64262889c8b21d3 
     </draft-comment> </td> 
    <td colname="col2"> <p> La administración dinámica de etiquetas requiere la función<span class="codeph"> _satellite.pageBottom()</span> . </p> <p> Se recomienda que la etiqueta sea la <i>última</i> etiqueta en el <span class="codeph"> &lt;body&gt;</span>. Si se encuentra dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span> , tiene la posibilidad de funcionar, pero como no es una práctica recomendada, podría funcionar incorrectamente o con resultados inesperados o no deseados. </p> </td> 
    <td colname="col3"> <p>Agregue la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la funcionalidad adecuada de la DTM. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Servicio de ID de Experience Cloud: use solo una AdobeOrg</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/id-request.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p>En una implementación MCID normal, se debe utilizar un solo AdobeOrg. </p> </td> 
    <td colname="col3"> <p>Valide que existan varios ID de AdobeOrg para esta implementación. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Target: contenido en mboxDefault</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> El contenido debe existir en mboxDefault al usar at.js. </p> </td> 
    <td colname="col3"> <p>Compruebe que el contenido está disponible. </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## Configuración {#configuration}

Esta referencia proporciona más información sobre las pruebas que realiza el Auditor para la configuración.

Auditor evalúa las etiquetas comparándolas con otras reglas y prácticas recomendadas.

<table id="table_A8A1FC360482447185C8460A18426638"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> Prueba </th> 
    <th colname="col2" class="entry"> Criterios </th> 
    <th colname="col3" class="entry"> Recomendación </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud: los nombres de conversión solo usan caracteres alfanuméricos</b> </p> <p>Peso: 3 </p> </td> 
    <td colname="col2"> <p>El parámetro <span class="codeph"> ev_conversion_property_name</span> sólo debe contener valores numéricos y decimales EXCEPTO para el parámetro "<span class="codeph"> ev_transid</span>" (el valor <span class="codeph"> ev_transid</span> puede contener valores numéricos o de texto) </p> <p>Busque <span class="codeph"> everesttech.net</span> píxeles que contengan un parámetro de URL que comience por <span class="codeph"> ev_</span>. </p> <p>Ejemplo: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47</span> </p> </td> 
    <td colname="col3"> <p> Asegúrese de que los parámetros de la propiedad de transacción solo contienen valores numéricos y decimales. </p> <p> <p>Advertencia:  Cualquier otro tipo de valor puede causar pérdida de datos. </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud: los nombres de conversión utilizan caracteres seguros para URL</b> </p> <p>Peso: 3 </p> </td> 
    <td colname="col2"> <p> Los nombres de propiedades de conversión no deben contener un símbolo de unión o un signo de interrogación. </p> <p> Ejemplo: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>Asegúrese de que los parámetros de propiedad de transacción no contienen un símbolo de interrogación o un signo de interrogación no codificado. Estos rompen el formato de la dirección URL. </p> <p> <p>Advertencia: Parámetros de propiedad que contienen un signo de interrogación o un signo de interrogación no codificado (por ejemplo: <span class="codeph"> ev_formComplete?=1</span> o <span class="codeph"> ev_formComplete&amp;Submit=1</span>), puede provocar la pérdida de datos. </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud: ID de transacción implementado correctamente</b> </p> <p>Peso: 1 </p> </td> 
    <td colname="col2"> <p> El nombre de propiedad <span class="codeph"> ev_transid=</span> no debe estar vacío. </p> <p>Ejemplo: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>El nombre de propiedad <span class="codeph"> ev_transid=</span> no debe dejarse sin un valor (<span class="codeph"> ev_transid=</span>). Si esto se deja sin valor, podría haber pérdida de datos de transacción. Asigne un valor al <span class="codeph"> ev_transid=</span> o elimine el parámetro del píxel. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics: se crea una instancia en DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/testing-and-validation-process/impl-validation.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> El código de Adobe Analytics no está instalado o no se puede ejecutar. Devuelve 0 cuando no se encuentra ninguna página web con código de análisis. </p> </td> 
    <td colname="col3"> <p>Compruebe que la etiqueta de Analytics está implementada en la página y que no está bloqueada por las actividades de script posteriores. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics: se crea una instancia una vez</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="https" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> El código de Adobe Analytics se detectó más de una vez en la página. . Devuelve 0 cuando no se encuentra ninguna página web con código de análisis. </p> </td> 
    <td colname="col3"> <p>Asegúrese de que solo hay una etiqueta de Analytics en la página. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics: última versión</b> </p> <p>Peso: 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> Sus páginas no están ejecutando la versión más reciente de la biblioteca de códigos de Analytics. Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y proporcionar las últimas funciones. Devuelve 0 cuando no se encuentra ninguna página web con código de análisis. </p> </td>       
    <td colname="col3"> <p>Instale la versión más reciente de la biblioteca de Analytics. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - Alojado automáticamente</b> </p> <p>Peso: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/client-side-information.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> La biblioteca de la DTM se aloja en la instancia de Adobe Akamai en <span class="filepath"> assets.adobedtm.com</span>. </p> <p> El autoalojamiento es el método recomendado para cargar la DTM, ya que proporciona un mayor control del rendimiento del sitio web mediante el control de caché, la reducción de las dependencias de scripts de terceros y un mayor control del proceso de publicación. Las bibliotecas de la DTM se pueden alojar y administrar a través de su propio alojamiento web o CDN. </p> </td> 
    <td colname="col3"> <p>El alojamiento propio es el método recomendado para cargar la DTM en una página. Aunque el alojamiento de DTM a través de la CDN de Akamai funciona en la mayoría de los casos, el autoalojamiento mejora el rendimiento de la página. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM: las etiquetas de terceros se cargan asincrónicamente después de DOM ready</b> </p> <p>Peso: 3 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/resources/load-order.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p>Para lograr un equilibrio entre una buena experiencia de usuario y la recopilación de datos precisos, las etiquetas de terceros deben activarse en DOM ready. Esto garantizará que las secuencias de comandos de seguimiento se ejecuten sin afectar a la funcionalidad del sitio. </p> </td> 
    <td colname="col3"> <p>Resuelva este problema ajustando todas las reglas que ejecutan píxeles de terceros para que se activen en DOM Ready. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Servicio Experience Cloud ID: versión más reciente</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/tools/macid.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> Las páginas no están ejecutando la versión más reciente de la biblioteca de códigos del servicio de ID de visitante, visitorAPI.js <span class="codeph"></span>. Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y proporcionar las últimas funciones. </p> </td> 
    <td colname="col3"> <p>Instale la versión más reciente de la biblioteca del servicio de ID de visitante. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target: última versión</b> </p> <p>Peso: 2 </p> <p><a href="https://marketing.adobe.com/resources/help/en_US/dtm/target/" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> Sus páginas no están ejecutando la versión más reciente de la biblioteca de códigos de Target. Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y proporcionar las últimas funciones. </p> </td> 
    <td colname="col3"> <p>Instale la versión más reciente de la biblioteca de Target. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target: mboxDefault precede a mboxCreate </b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p>El uso correcto de <span class="codeph"> mboxCreate</span> es similar a este: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Contenido del cliente—&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
    <td colname="col3"> <p>Asegúrese de incluir una etiqueta <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> antes de invocar <span class="codeph"> mboxCreate()</span>. at.js no agregará una para usted. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target - DOCTYPE válido</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> Se detectó un DOCTYPE no válido. En este escenario no se activará ningún mbox. </p> <p>Para at.js, DOCTYPE debe estar en modo de estándares o Target no funcionará. </p> </td> 
    <td colname="col3"> <p>Actualice DOCTYPE en la página. </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## Coherencia de etiquetas {#tag-consistency}

Esta referencia proporciona más información sobre las pruebas que realiza el Auditor para mantener la coherencia de las etiquetas.

Auditor evalúa si las etiquetas son coherentes en todas las direcciones URL.

<table id="table_4F9ED873BAF741D19BFB0F297B3A1FDB"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> Prueba </th> 
    <th colname="col2" class="entry"> Criterios </th> 
    <th colname="col3" class="entry"> Recomendación </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Analytics: versión de código coherente </b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/choose-implementation-method.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> Se encontró más de una versión del código de Analytics. </p> </td> 
    <td colname="col3"> <p>Reemplazar todas las instancias de Analytics con la versión actual. </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## Presencia de etiquetas {#tag-presence}

Esta referencia proporciona más información sobre las pruebas que realiza el Auditor para la presencia de etiquetas.

Auditor evalúa si la etiqueta existe, si está en el lugar correcto en el código de la página, etc.

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> Prueba </th> 
    <th colname="col2" class="entry"> Criterios </th> 
    <th colname="col3" class="entry"> Recomendación </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud: presencia de código</b> </p> <p>Peso: 5 </p> </td> 
    <td colname="col2"> <p> La etiqueta de Advertising Cloud no está disponible en el DOM. </p> </td> 
    <td colname="col3"> <p>Implemente la etiqueta de Advertising Cloud mediante la extensión de lanzamiento de Advertising Cloud. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud: Píxel de segmento implementado</b> </p> <p>Peso: 5 </p> </td> 
    <td colname="col2"> <p> Actualice los píxeles del segmento de Advertising Cloud a las nuevas etiquetas de solo imagen de Advertising Cloud. El uso de etiquetas de segmento AMO desaprobado puede provocar la pérdida de datos. </p> </td> 
    <td colname="col3"> <p>Implemente el píxel del segmento de Advertising Cloud mediante la extensión de lanzamiento de Advertising Cloud. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics: cargado en DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="https" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> No se detectó la etiqueta de Adobe Analytics. </p> </td> 
    <td colname="col3"> <p>Instale la versión más reciente de Analytics. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> DTM: biblioteca cargada</b> </p> <p>Peso: 5 </p> <p>Información adicional: </p> <p> 
      <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
       <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/en/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> Resolución de problemas de DTM</a> </li> 
       <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Adición de código de Encabezado y Pie de página</a> </li> 
      </ul> </p> </td> 
    <td colname="col2"> <p> No se encontró un objeto _satellite global en el DOM. La administración dinámica de etiquetas no está instalada o no se puede ejecutar. </p> </td> 
    <td colname="col3"> <p>Compruebe que la biblioteca de la DTM está implementada en la página y que no está bloqueada por las actividades de script posteriores. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> DTM: un código incrustado</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/code.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> Los sitios de producción solo deben cargar una biblioteca de la DTM. </p> </td> 
    <td colname="col3"> <p>Compruebe que solo se está cargando la biblioteca de producción en la página. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM: la devolución de llamada pageBottom existe en &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> No se encontró la rellamada <span class="codeph"> _satellite.pageBottom()</span> dentro del <span class="codeph"> &lt;body&gt;</span> de la página, que requiere la administración dinámica de etiquetas. </p> <p>Esta prueba falla si no se encuentra la <span class="codeph"> llamada pageBottom en la </span>página o si está en la etiqueta <span class="codeph"> &lt;head&gt;</span> (o en alguna otra ubicación inesperada). Solo pasará si <span class="codeph"> pageBottom</span> se encuentra en algún lugar dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span> . Si no está en la página, no funcionará y las otras dos pruebas <span class="codeph"> pageBottom</span> también fallarán. </p> </td> 
    <td colname="col3"> <p>Agregue la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la funcionalidad adecuada de la DTM. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM: etiqueta pageBottom activada</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> No se detectó la etiqueta <span class="codeph"> pageBottom</span> de la DTM. </p> <p>Esto podría ocurrir si la llamada se encuentra dentro de una instrucción <span class="codeph"> if</span> que resulta en algo similar a <span class="codeph"> if (false) {_satellite.pageBottom()}</span>. Así que, si bien puede existir y estar colocada correctamente, la etiqueta podría no activarse. </p> </td> 
    <td colname="col3"> <p>Instale la llamada <span class="codeph"> pageBottom</span> de DTM en todas las páginas. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Servicio Experience Cloud ID: presencia de cookies</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> No se encontró la <span class="codeph"> cookie AMCV_</span> . Debe crear una instancia de un objeto visitor desde el código <span class="codeph"> VisitorAPI.js</span> . </p> </td> 
    <td colname="col3"> <p> Si se trata de una implementación de DTM, compruebe que el ID de AdobeOrg se ha introducido correctamente en la herramienta MCID. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Servicio de ID de Experience Cloud: valor de MID presente</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> No se encontró el valor medio en la <span class="codeph"> cookie AMCV_</span> . </p> </td> 
    <td colname="col3"> <p>Vuelva a realizar la prueba para comprobar si hay latencia de API de MCID. Si la condición persiste, póngase en contacto con el Servicio de atención al cliente de Adobe. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Servicio de ID de Experience Cloud: debería estar instalado</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> Información adicional</a> </p> </td> 
    <td colname="col2"> <p> No se encontró el código del servicio Experience Cloud ID. El ECID es muy recomendable para garantizar que obtiene el máximo valor de sus soluciones de Experience Cloud y es fundamental para la administración de ID en todas las soluciones de EC. </p> </td> 
    <td colname="col3"> <p>Instale la versión más reciente de MCID. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Target: biblioteca cargada en &lt;head&gt;</b> </p> <p>Peso: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Información adicional</a> </p> 
     <draft-comment>
       TE61c380082a4b4706b28a84aa047599a7 
     </draft-comment> </td> 
    <td colname="col2"> <p> La biblioteca de Target debe cargarse en la etiqueta <span class="codeph"> &lt;head&gt;</span> . </p> </td> 
    <td colname="col3"> <p> Asegúrese de que la biblioteca de Target se carga en la etiqueta <span class="codeph"> &lt;head&gt;</span> . </p> </td> 
   </tr> 
  </tbody> 
</table>
