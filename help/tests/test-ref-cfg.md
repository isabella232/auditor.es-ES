---
description: Esta referencia proporciona más información sobre las pruebas que realiza Adobe Experience Platform Auditor para mantener la configuración.
seo-description: Esta referencia proporciona más información sobre las pruebas que realiza Adobe Experience Platform Auditor para mantener la configuración.
seo-title: Configuración
title: Configuración
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: ht
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: ht
source-wordcount: '846'
ht-degree: 100%

---


# Configuración

Esta referencia proporciona más información sobre las pruebas que realiza Adobe Experience Platform Auditor para mantener la configuración.

Las pruebas de configuración analizan la configuración, los valores o los posibles conflictos específicos de la implementación. Platform Auditor evalúa las etiquetas comparándolas con otras normas y prácticas recomendadas.

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
    --> <p><b>Launch: Última versión</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>Estas páginas no ejecutan la última versión de la biblioteca de códigos de Platform Launch (Turbine). Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y ofrecer las últimas funciones. </p> </td> 
   <td colname="col3"> <p> Actualice la biblioteca de Platform Launch reconstruyendo y publicando la biblioteca de Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target: Última versión</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/implementing/target/update-target-tool.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> Las páginas no ejecutan la última versión de la biblioteca de códigos de Target. Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y ofrecer las últimas funciones. </p> </td> 
   <td colname="col3"> <p>Instale la última versión de la biblioteca de Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target: mboxDefault es anterior a mboxCreate </b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/target/using/implement-target/client-side/mbox-implement/mbox-download.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>El uso correcto de <span class="codeph"> mboxCreate</span> es similar al siguiente: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Customer content--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Recuerde incluir una etiqueta <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> antes de aplicar <span class="codeph"> mboxCreate()</span>. at.js no añadirá una para usted. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target: DOCTYPE válido</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/help/es-ES/target/using/implement-target/client-side/faq-at-js/target-atjs-faq.html#what-html-doctype-does-atjs-require" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> Se ha detectado un DOCTYPE no válido. En este escenario no se activará ningún mbox. </p> <p>Para at.js, DOCTYPE debe estar en modo Estándares o Target no funcionará. </p> </td> 
   <td colname="col3"> <p>Actualice DOCTYPE en la página. </p> </td> 
  </tr> 
 </tbody> 
</table>

