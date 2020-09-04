---
description: información sobre las pruebas de Adobe Auditor
seo-description: información sobre las pruebas de Adobe Auditor
seo-title: Prueba de implementación 1.0.1
title: Prueba de implementación 1.0.1
uuid: 2ed2572e-ddb8-4899-b3a9-1329afdd7905
translation-type: tm+mt
source-git-commit: 77ced60ff8e05515521d89d16c32cbad42d1e8d0
workflow-type: tm+mt
source-wordcount: '2684'
ht-degree: 100%

---


# Prueba de implementación 1.0.1 {#test-rubric}

## Prueba de implementación 1.0.1 {#topic-25ed23afdfaf4a12b149ff276965b043}

## Alertas {#alerts}

Esta referencia proporciona más información sobre las alertas que Auditor muestra para las pruebas.

Las alertas muestran los problemas que deben tenerse en cuenta, aunque eso no afecta a la puntuación. Las siguientes son algunas prácticas recomendadas que, en algunos casos, no serán útiles para su aplicación.

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
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud: Se ha implementado la etiqueta de conversión correcta</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Compruebe si se utiliza la etiqueta de conversión correcta. </p> <p> <p>Advertencia: El uso de etiquetas de conversión TubeMogul obsoletas puede causar la pérdida de datos. </p> </p> </td> 
   <td colname="col3"> <p>Actualice los píxeles de conversión a las nuevas etiquetas de conversión solo de imagen de Advertising Cloud. </p> <p>Esto puede realizarse fácilmente con la extensión de Launch de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud: Se ha utilizado la etiqueta JS correcta</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud debe utilizar las últimas etiquetas de JavaScript. </p> </td> 
   <td colname="col3"> <p>Actualice el JavaScript de Advertising Cloud con la última versión. El uso de versiones de JavaScript no compatibles puede causar la pérdida de funcionalidad. </p> <p>Esto puede realizarse más fácilmente mediante la extensión de Launch de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud: Etiqueta de solo imagen</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>El formato de píxel de imagen de Advertising Cloud debe tener uno de los siguientes formatos recomendados: </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph">http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph">http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph">http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Actualice los píxeles de Advertising Cloud con las nuevas etiquetas de solo imagen de Advertising Cloud para garantizar que dispone de toda la funcionalidad de Advertising Cloud. </p> <p>Esto puede realizarse fácilmente con la extensión de Launch de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud: píxeles de segmento: sincronización DSP habilitada</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Compruebe si el píxel del segmento TubeMogul contiene un ajuste de sincronización de DSP y recomiende que el ajuste se añada al píxel. </p> <p>La configuración de sincronización de DSP se determina por el uso de un parámetro de cadena de consulta, por lo que </p> <p>SI la etiqueta se está activando en<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> O <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> O <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>Y la etiqueta contiene el parámetro de URL <span class="codeph"> "sid=")</span> </p> <p>ENTONCES, compruebe si existe el parámetro de URL <span class="codeph"> "cs=0"</span> o<span class="codeph"> "cs=1"</span> y, en caso contrario, recomiende que <span class="codeph"> "cs=1"</span> se añada a esos píxeles para que mejoren los índices de coincidencia de audiencia. </p> </td> 
   <td colname="col3"> <p> Añada el parámetro de URL <span class="codeph"> "cs=1"</span> a los píxeles de Advertising Cloud para que se sincronice con DSP, lo que aumenta los índices de coincidencia de audiencia. </p> <p>Esto se puede realizar fácilmente con la extensión de Advertising Cloud Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM: colocación de la llamada de retorno pageBottom</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Más información</a> </p> 
    <!--
      TEa9df69942f404055a64262889c8b21d3 
    --> </td> 
   <td colname="col2"> <p>Dynamic Tag Management (DTM) exige la función <span class="codeph"> _satellite.pageBottom()</span>. Añada la secuencia de comandos en línea inmediatamente antes de la etiqueta body de cierre para garantizar la correcta funcionalidad de la DTM. </p> <p> <p>Nota: Se recomienda que la etiqueta sea la <i>última</i> etiqueta en el <span class="codeph"> &lt;body&gt;</span>. Si se encuentra dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span>, puede funcionar, pero como no es una práctica recomendada, podría funcionar incorrectamente o dar resultados inesperados o no deseados. </p> </p> </td> 
   <td colname="col3"> <p>Añada la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la correcta funcionalidad de la DTM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM: Sistema autoalojado</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/client-side/client-side-information.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> La biblioteca de DTM se aloja en la instancia de Adobe Akamai en <span class="filepath"> assets.adobedtm.com</span>. </p> <p> El autoalojamiento es el método recomendado para cargar DTM, ya que ofrece un mayor control del rendimiento del sitio web mediante el control de caché, la reducción de las dependencias de scripts de terceros y un mayor control durante el proceso de publicación. Las bibliotecas de DTM se pueden alojar y administrar a través de su propio alojamiento web o CDN. </p> </td> 
   <td colname="col3"> <p>El autoalojamiento es el método recomendado para cargar DTM en una página. Aunque el alojamiento de DTM a través de la CDN de Akamai generalmente funciona, el autoalojamiento mejora el rendimiento de la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Servicio de Experience Cloud ID: utilice solo un AdobeOrg</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/id-service/using/intro/id-request.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>En una implementación ECID normal, debe utilizarse un único AdobeOrg. </p> </td> 
   <td colname="col3"> <p>Verifique que existen varios ID de AdobeOrg para esta implementación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch: colocación de llamada de retorno pageBottom</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Más información</a> </p> 
    <!--
      TE48c499b022f545c5bccc6f8bde169685 
    --> </td> 
   <td colname="col2"> <p>Launch debe tener una función de llamada de retorno <span class="codeph"> pageBottom </span> definida en último lugar del cuerpo de la página si se utiliza sincrónicamente </p> <p> <p>Nota: Se recomienda que la etiqueta sea la <i>última</i> etiqueta en el <span class="codeph"> &lt;body&gt;</span>. Si se encuentra dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span>, puede funcionar, pero como no es una práctica recomendada, podría funcionar incorrectamente o dar resultados inesperados o no deseados. </p> </p> </td> 
   <td colname="col3"> <p>Añada la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la correcta funcionalidad de la DTM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch: Autoalojado</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>La biblioteca de Launch se aloja en la instancia de Adobe Akamai en <span class="filepath"> assets.adobedtm.com</span>. </p> <p>El autoalojamiento es el método recomendado para cargar Launch, ya que ofrece un mayor control del rendimiento del sitio web mediante el control de caché, la reducción de las dependencias de scripts de terceros y un mayor control durante el proceso de publicación. Las bibliotecas de Launch se pueden alojar y administrar a través de su propio alojamiento web o CDN. </p> </td> 
   <td colname="col3"> <p>Aunque el alojamiento de Launch a través de la CDN de Akamai funciona en la mayoría de los casos, se recomienda utilizar el alojamiento propio como el primer paso para mejorar el rendimiento de la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch: Debe implementarse asincrónicamente</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>Launch debe implementarse asincrónicamente para obtener un rendimiento óptimo. </p> </td> 
   <td colname="col3"> <p>Incluya el parámetro async en la secuencia de comandos en línea para garantizar la correcta funcionalidad asincrónica de Launch </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Target: Contenido en mboxDefault</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/target/using/implement-target/implementing-target.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> El contenido debe estar presente en mboxDefault si se utiliza at.js. </p> </td> 
   <td colname="col3"> <p>Compruebe que el contenido está disponible. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Configuración {#configuration}

Esta referencia proporciona más información sobre las pruebas que realiza Auditor para la configuración.

Las pruebas de configuración analizan la configuración, los valores o los posibles conflictos específicos de la implementación. Auditor evalúa las etiquetas comparándolas con otras normas y prácticas recomendadas.

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
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud: Los nombres de conversión solo utilizan caracteres alfanuméricos</b> </p> <p>Peso: 3 </p> </td> 
   <td colname="col2"> <p>El parámetro <span class="codeph"> ev_conversion_property_name</span> solo debe contener valores numéricos y decimales, EXCEPTO para el parámetro “<span class="codeph"> ev_transid</span>” (el valor <span class="codeph"> ev_transid</span> puede contener valores numéricos o de texto) </p> <p>Busque píxeles <span class="codeph"> everesttech.net</span> que contengan un parámetro de URL que empiece por <span class="codeph"> ev_</span>. </p> <p>Ejemplo: </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Compruebe que los parámetros de la propiedad de transacción solo contienen valores numéricos y decimales. </p> <p> <p>Advertencia: Cualquier otro tipo de valor puede causar pérdida de datos. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud: Los nombres de conversión utilizan caracteres seguros para URL</b> </p> <p>Peso: 3 </p> </td> 
   <td colname="col2"> <p> Los nombres de propiedades de conversión no deben contener un signo &amp; o un signo de interrogación. </p> <p> Ejemplo: </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Compruebe que los parámetros de propiedad de transacción no contienen un signo &amp; o un signo de interrogación no codificado. Estos signos rompen el formato de la dirección URL. </p> <p> <p>Advertencia: Los parámetros de propiedad que contienen un signo de interrogación o un signo de interrogación no codificado (por ejemplo: <span class="codeph"> ev_formComplete?=1</span> o <span class="codeph"> ev_formComplete&amp;Submit=1</span>), puede causar la pérdida de datos. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud: ID de transacción implementado correctamente</b> </p> <p>Peso: 1 </p> </td> 
   <td colname="col2"> <p> El nombre de propiedad <span class="codeph"> ev_transid=</span> no debe estar vacío. </p> <p>Ejemplo: </p> <p> <span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>El nombre de propiedad <span class="codeph"> ev_transid=</span> debe contener un valor (<span class="codeph"> ev_transid=</span>). Si no se introduce un valor, puede causar la pérdida de datos de transacción. Asigne un valor al <span class="codeph"> ev_transid=</span> o elimine el parámetro desde el píxel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics: Instanciado en DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/analytics/implementation/home.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> El código de Adobe Analytics no está instalado o no puede ejecutarse. Devuelve el valor 0 cuando no se encuentra ninguna página web con código de Analytics. </p> </td> 
   <td colname="col3"> <p>Compruebe que la etiqueta de Analytics está implementada en la página y no está bloqueada por las siguientes actividades de script. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics: Instanciado una vez</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/analytics/implementation/home.html" format="https" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> El código de Adobe Analytics se ha detectado más de una vez en la página. Devuelve el valor 0 cuando no se encuentra ninguna página web con código de Analytics. </p> </td> 
   <td colname="col3"> <p>Compruebe que solo hay una etiqueta de Analytics en la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics: Última versión</b> </p> <p>Peso: 3 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> Las páginas no ejecutan la última versión de la biblioteca de códigos de Analytics. Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y ofrecer las últimas funciones. Devuelve el valor 0 cuando no se encuentra ninguna página web con código de Analytics. </p> </td> 
   <td colname="col3"> <p>Instale la última versión de la biblioteca de Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM: Las etiquetas de terceros se cargan asincrónicamente después de DOM ready</b> </p> <p>Peso: 3 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/resources/load-order.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>Para ofrecer un equilibrio entre una buena experiencia de usuario y la obtención de datos precisos, las etiquetas de terceros deben activarse en DOM ready. Esto garantizará que las secuencias de comandos de seguimiento se ejecuten sin afectar a la funcionalidad del sitio. </p> </td> 
   <td colname="col3"> <p>Resuelva este problema ajustando todas las normas que ejecutan píxeles de terceros para que se activen en DOM Ready. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Servicio de Experience Cloud ID: Última versión</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/tools/macid.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> Las páginas no están ejecutando la versión más reciente de la biblioteca de códigos del servicio de ID de visitante, <span class="codeph"> visitorAPI.js</span>. Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y ofrecer las últimas funciones. </p> </td> 
   <td colname="col3"> <p>Instale la última versión de la biblioteca del servicio de ID de visitante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch: Última versión</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>Estas páginas no ejecutan la última versión de la biblioteca de códigos de Launch (Turbine). Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y ofrecer las últimas funciones. </p> </td> 
   <td colname="col3"> <p> Actualice la biblioteca de Launch reconstruyendo y publicando la biblioteca de Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target: Última versión</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/tools/target.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> Las páginas no ejecutan la última versión de la biblioteca de códigos de Target. Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y ofrecer las últimas funciones. </p> </td> 
   <td colname="col3"> <p>Instale la última versión de la biblioteca de Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target: mboxDefault es anterior a mboxCreate </b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/target/using/implement-target/implementing-target.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>El uso correcto de <span class="codeph"> mboxCreate</span> es similar al siguiente: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Customer content--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Recuerde incluir una etiqueta <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> antes de aplicar <span class="codeph"> mboxCreate()</span>. at.js no añadirá una para usted. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target: DOCTYPE válido</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/target/using/implement-target/implementing-target.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> Se ha detectado un DOCTYPE no válido. En este escenario no se activará ningún mbox. </p> <p>Para at.js, DOCTYPE debe estar en modo Estándares o Target no funcionará. </p> </td> 
   <td colname="col3"> <p>Actualice DOCTYPE en la página. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Coherencia de etiquetas {#tag-consistency}

Esta referencia proporciona más información sobre las pruebas que realiza Auditor para mantener la coherencia de las etiquetas.

Las pruebas de coherencia de Auditor buscan incoherencias en todas las páginas digitalizadas. Son valores o configuraciones que deben ser iguales en todas las páginas del sitio para garantizar una recopilación de datos precisa.

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
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics: versión de código coherente </b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/analytics/implementation/home.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> Se ha encontrado más de una versión del código de Analytics. </p> </td> 
   <td colname="col3"> <p>Reemplazar todas las instancias de Analytics con la versión actual. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Presencia de etiquetas {#tag-presence}

Esta referencia proporciona más información sobre las pruebas que realiza Auditor para detectar la presencia de etiquetas.

Auditor evalúa si la etiqueta existe y si está en el lugar correcto en el código de la página.

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
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud: Presencia de código</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> La etiqueta de Advertising Cloud no está disponible en el DOM. </p> </td> 
   <td colname="col3"> <p>Aplique la etiqueta de Advertising Cloud mediante la extensión de Launch de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud: Píxel de segmento implementado</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> Actualice los píxeles del segmento de Advertising Cloud con las nuevas etiquetas de solo imagen de Advertising Cloud. El uso de etiquetas de segmento AMO no soportadas puede causar la pérdida de datos. </p> </td> 
   <td colname="col3"> <p>Implemente el píxel del segmento de Advertising Cloud con la extensión de Launch de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics: Cargado en DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/analytics/implementation/home.html" format="https" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> No se ha detectado la etiqueta de Adobe Analytics. </p> </td> 
   <td colname="col3"> <p>Instale la última versión de Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> DTM: Biblioteca cargada</b> </p> <p>Peso: 5 </p> <p>Más información: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> Resolución de problemas de DTM</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Adición de código de Encabezado y Pie de página</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> No se ha encontrado un objeto _satellite global en el DOM. Dynamic Tag Management no está instalada o no se puede ejecutar. </p> </td> 
   <td colname="col3"> <p>Compruebe que la biblioteca de la DTM está aplicada en la página y que no está bloqueada por las actividades de script posteriores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> DTM: Un código incrustado</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/client-side/code.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> Los sitios de producción solo deben cargar una biblioteca de la DTM. </p> </td> 
   <td colname="col3"> <p>Compruebe que solo se está cargando la biblioteca de producción en la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM: la devolución de llamada pageBottom existe en &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> No se ha encontrado la llamada de retorno <span class="codeph"> _satellite.pageBottom()</span> dentro del <span class="codeph"> &lt;body&gt;</span> de la página, que exige Dynamic Tag Management. </p> <p>Esta prueba falla si no se encuentra la <span class="codeph"> llamada pageBottom en la </span>página o si está en la etiqueta <span class="codeph"> &lt;head&gt;</span> (o en otra ubicación inesperada). Solo funcionará correctamente si <span class="codeph"> pageBottom</span> se encuentra en algún lugar dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span>. Si no está en la página, no funcionará y las otras dos pruebas <span class="codeph"> pageBottom</span> también fallarán. </p> </td> 
   <td colname="col3"> <p>Añada la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la correcta funcionalidad de la DTM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM: etiqueta pageBottom activada</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> No se ha detectado la etiqueta <span class="codeph"> pageBottom</span> de la DTM. </p> <p>Esto puede ocurrir si la llamada está dentro de una condición <span class="codeph"> if</span> (si) que genera algo parecido a <span class="codeph"> if (false) {_satellite.pageBottom()}</span>. Por tanto, aunque puede existir y estar colocada correctamente, la etiqueta podría no activarse. </p> </td> 
   <td colname="col3"> <p>Instale la llamada <span class="codeph"> pageBottom</span> de DTM en todas las páginas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Servicio de Experience Cloud ID: presencia de código</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/id-service/using/implementation/implementation-methods.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>No se ha encontrado el código del servicio de Experience Cloud ID. El Experience Cloud ID (ECID) es muy recomendable para garantizarle que obtiene el máximo valor de sus soluciones de Experience Cloud y es fundamental para la administración de ID en todas las soluciones de Experience Cloud. </p> </td> 
   <td colname="col3"> <p> Instale la última versión de ECID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Servicio de Experience Cloud ID: presencia de cookies</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/id-service/using/implementation/implementation-guides.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> No se ha encontrado la cookie <span class="codeph"> AMCV_</span>. Debe crear una instancia de un objeto visitante desde el código<span class="codeph"> VisitorAPI.js</span>. </p> </td> 
   <td colname="col3"> <p> Si se trata de una aplicación de DTM, compruebe que el ID de AdobeOrg se ha introducido correctamente en la herramienta ECID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Servicio de Experience Cloud ID: Valor de MID presente</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/id-service/using/intro/cookies.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> No se ha encontrado el valor MID en la cookie <span class="codeph"> AMCV_</span>. </p> </td> 
   <td colname="col3"> <p>Vuelva a realizar la prueba para comprobar si hay latencia de API de ECID. Si esta situación persiste, póngase en contacto con el Servicio de atención al cliente de Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Launch: biblioteca cargada</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> No se ha encontrado un objeto _satellite global en el DOM. Launch no está instalado o no se puede ejecutar. </p> </td> 
   <td colname="col3"> <p>Compruebe que la biblioteca de Launch está aplicada en la página y que no está bloqueada por las actividades de script posteriores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch: no hay varios scripts incrustados</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>No debe haber varios scripts incrustados cargados en la página. Los sitios de producción solo deben cargar una biblioteca de Launch. </p> </td> 
   <td colname="col3"> <p>Compruebe que solo se está cargando la biblioteca de producción en la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch: la llamada de retorno pageBottom se encuentra en &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> La <span class="codeph"> llamada de retorno _satellite.pageBottom()</span> no se ha encontrado en el <span class="codeph"> &lt;body&gt;</span> de la página, que exige Launch. </p> <p>Esta prueba falla si no se encuentra la <span class="codeph"> llamada pageBottom en la </span>página o si está en la etiqueta <span class="codeph"> &lt;head&gt;</span> (o en otra ubicación inesperada). Solo funcionará correctamente si <span class="codeph"> pageBottom</span> se encuentra en algún lugar dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span>. Si no está en la página, no funcionará y las otras dos pruebas <span class="codeph"> pageBottom</span> también fallarán. </p> </td> 
   <td colname="col3"> <p>Añada la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la correcta funcionalidad de Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch: la llamada de retorno pageBottom no debe existir cuando se aplica de forma asincrónica</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>La llamada de retorno <span class="codeph"> _satellite.pageBottom()</span> se ha encontrado en la página, cosa que no debería suceder cuando Launch se aplica de forma asíncrona. </p> </td> 
   <td colname="col3"> <p>Elimine el script <span class="codeph">_satellite.pageBottom()</span> para habilitar la correcta funcionalidad de Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Target: presencia de código</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/target/using/implement-target/implementing-target.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>Target debe definirse en el DOM. </p> </td> 
   <td colname="col3"> <p>Instale la última versión de Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Target: biblioteca cargada en &lt;head&gt;</b> </p> <p>Peso: 4 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/target/using/implement-target/implementing-target.html" format="html" scope="external"> Más información</a> </p> 
    <!--
      TE61c380082a4b4706b28a84aa047599a7 
    --> </td> 
   <td colname="col2"> <p> La biblioteca de Target debe cargarse en la etiqueta <span class="codeph"> &lt;head&gt;</span>. </p> </td> 
   <td colname="col3"> <p> Compruebe que la biblioteca de Target se carga en la etiqueta <span class="codeph"> &lt;head&gt;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

