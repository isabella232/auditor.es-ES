---
description: Esta referencia proporciona más información sobre las pruebas que realiza el Auditor para la configuración.
seo-description: Esta referencia proporciona más información sobre las pruebas que realiza el Auditor para la configuración.
seo-title: Configuración
title: Configuración
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Configuración

Esta referencia proporciona más información sobre las pruebas que realiza el Auditor para la configuración.

Las pruebas de configuración analizan la configuración, los valores o los posibles conflictos específicos de la implementación. Auditor evalúa las etiquetas comparándolas con otras reglas y prácticas recomendadas.

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
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud: los nombres de conversión solo usan caracteres alfanuméricos</b> </p> <p>Peso: 3 </p> </td> 
   <td colname="col2"> <p>El parámetro <span class="codeph"> ev_conversion_property_name</span> sólo debe contener valores numéricos y decimales EXCEPTO para el parámetro "<span class="codeph"> ev_transid</span>" (el valor <span class="codeph"> ev_transid</span> puede contener valores numéricos o de texto) </p> <p>Busque <span class="codeph"> everesttech.net</span> píxeles que contengan un parámetro de URL que comience por <span class="codeph"> ev_</span>. </p> <p>Ejemplo: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Asegúrese de que los parámetros de la propiedad de transacción solo contienen valores numéricos y decimales. </p> <p> <p>Advertencia:  Cualquier otro tipo de valor puede causar pérdida de datos. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud: los nombres de conversión utilizan caracteres seguros para URL</b> </p> <p>Peso: 3 </p> </td> 
   <td colname="col2"> <p> Los nombres de propiedades de conversión no deben contener un símbolo de unión o un signo de interrogación. </p> <p> Ejemplo: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Asegúrese de que los parámetros de propiedad de transacción no contienen un símbolo de interrogación o un signo de interrogación no codificado. Estos rompen el formato de la dirección URL. </p> <p> <p>Advertencia: Parámetros de propiedad que contienen un signo de interrogación o un signo de interrogación no codificado (por ejemplo: <span class="codeph"> ev_formComplete?=1</span> o <span class="codeph"> ev_formComplete&amp;Submit=1</span>), puede provocar la pérdida de datos. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud: ID de transacción implementado correctamente</b> </p> <p>Peso: 1 </p> </td> 
   <td colname="col2"> <p> El nombre de propiedad <span class="codeph"> ev_transid=</span> no debe estar vacío. </p> <p>Ejemplo: </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>El nombre de propiedad <span class="codeph"> ev_transid=</span> no debe dejarse sin un valor (<span class="codeph"> ev_transid=</span>). Si esto se deja sin valor, podría haber pérdida de datos de transacción. Asigne un valor al <span class="codeph"> ev_transid=</span> o elimine el parámetro del píxel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics: se crea una instancia en DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/impl_testing.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> El código de Adobe Analytics no está instalado o no se puede ejecutar. Devuelve 0 cuando no se encuentra ninguna página web con código de análisis. </p> </td> 
   <td colname="col3"> <p>Compruebe que la etiqueta de Analytics está implementada en la página y que no está bloqueada por las actividades de script posteriores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics: se crea una instancia una vez</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> El código de Adobe Analytics se detectó más de una vez en la página. . Devuelve 0 cuando no se encuentra ninguna página web con código de análisis. </p> </td> 
   <td colname="col3"> <p>Asegúrese de que solo hay una etiqueta de Analytics en la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics: última versión</b> </p> <p>Peso: 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> Sus páginas no están ejecutando la versión más reciente de la biblioteca de códigos de Analytics. Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y proporcionar las últimas funciones. Devuelve 0 cuando no se encuentra ninguna página web con código de análisis. </p> </td> 
   <td colname="col3"> <p>Instale la versión más reciente de la biblioteca de Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM: las etiquetas de terceros se cargan asincrónicamente después de DOM ready</b> </p> <p>Peso: 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/load_order.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p>Para lograr un equilibrio entre una buena experiencia de usuario y la recopilación de datos precisos, las etiquetas de terceros deben activarse en DOM ready. Esto garantizará que las secuencias de comandos de seguimiento se ejecuten sin afectar a la funcionalidad del sitio. </p> </td> 
   <td colname="col3"> <p>Resuelva este problema ajustando todas las reglas que ejecutan píxeles de terceros para que se activen en DOM Ready. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servicio Experience Cloud ID: versión más reciente</b> </p> <p>Peso: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/macid.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> Las páginas no están ejecutando la versión más reciente de la biblioteca de códigos del servicio de ID de visitante, visitorAPI.js <span class="codeph"></span>. Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y proporcionar las últimas funciones. </p> </td> 
   <td colname="col3"> <p>Instale la versión más reciente de la biblioteca del servicio de ID de visitante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Lanzamiento: versión más reciente</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p>Estas páginas no están ejecutando la versión más reciente de la biblioteca de códigos de Launch (Turbine). Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y proporcionar las últimas funciones. </p> </td> 
   <td colname="col3"> <p> Actualice la biblioteca de Launch reconstruyendo y publicando la biblioteca de Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target: última versión</b> </p> <p>Peso: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/dtm/update-target-tool.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> Sus páginas no están ejecutando la versión más reciente de la biblioteca de códigos de Target. Las bibliotecas de códigos que alimentan las tecnologías de Experience Cloud se actualizan y modifican constantemente para aprovechar las mejoras de rendimiento y proporcionar las últimas funciones. </p> </td> 
   <td colname="col3"> <p>Instale la versión más reciente de la biblioteca de Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target: mboxDefault precede a mboxCreate </b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p>El uso correcto de <span class="codeph"> mboxCreate</span> es similar a este: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Contenido del cliente—&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Asegúrese de incluir una etiqueta <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> antes de invocar <span class="codeph"> mboxCreate()</span>. at.js no agregará una para usted. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - DOCTYPE válido</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> Se detectó un DOCTYPE no válido. En este escenario no se activará ningún mbox. </p> <p>Para at.js, DOCTYPE debe estar en modo de estándares o Target no funcionará. </p> </td> 
   <td colname="col3"> <p>Actualice DOCTYPE en la página. </p> </td> 
  </tr> 
 </tbody> 
</table>

