---
description: Esta referencia proporciona más información sobre las pruebas que realiza el Auditor para la presencia de etiquetas.
seo-description: Esta referencia proporciona más información sobre las pruebas que realiza el Auditor para la presencia de etiquetas.
seo-title: Presencia de etiquetas
title: Presencia de etiquetas
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Presencia de etiquetas

Esta referencia proporciona más información sobre las pruebas que realiza el Auditor para la presencia de etiquetas.

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
   <td colname="col1"> <p><b>Analytics: cargado en DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Información adicional</a> </p> </td> 
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
   <td colname="col2"> <p> No se detectó la etiqueta DTM <code> pageBottom</code> . </p> <p>Esto podría ocurrir si la llamada se encuentra dentro de una <code> if</code> instrucción que resulta en algo similar a <code> if (false) {_satellite.pageBottom()}</code>. Así que, si bien puede existir y estar colocada correctamente, la etiqueta podría no activarse. </p> </td> 
   <td colname="col3"> <p>Instale la llamada de la DTM <code> pageBottom</code> en todas las páginas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servicio Experience Cloud ID: presencia de código</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p>No se encontró el código del servicio Experience Cloud ID. Experience Cloud ID (MCID) es muy recomendable para garantizar que obtiene el máximo valor de sus soluciones de Experience Cloud y es fundamental para la administración de ID en todas las soluciones de Experience Cloud. </p> </td> 
   <td colname="col3"> <p> Instale la versión más reciente de MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servicio Experience Cloud ID: presencia de cookies</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> No se encontró la <span class="codeph"> cookie AMCV_</span> . Debe crear una instancia de un objeto visitor desde el código <span class="codeph"> VisitorAPI.js</span> . </p> </td> 
   <td colname="col3"> <p> Si se trata de una implementación de DTM, compruebe que el ID de AdobeOrg se ha introducido correctamente en la herramienta MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servicio de ID de Experience Cloud: valor de MID presente</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> No se encontró el valor MID en la <span class="codeph"> cookie AMCV_</span> . </p> </td> 
   <td colname="col3"> <p>Vuelva a realizar la prueba para comprobar si hay latencia de API de MCID. Si la condición persiste, póngase en contacto con el Servicio de atención al cliente de Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> Inicio: biblioteca cargada</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> No se encontró un objeto _satellite global en el DOM. Launch no está instalado o no se puede ejecutar. </p> </td> 
   <td colname="col3"> <p>Compruebe que la biblioteca de Launch está implementada en la página y que no está bloqueada por las actividades de script posteriores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch: no hay varios scripts incrustados</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p>No debe haber varios scripts incrustados cargados en la página. Los sitios de producción solo deben cargar una biblioteca de Launch. </p> </td> 
   <td colname="col3"> <p>Compruebe que solo se está cargando la biblioteca de producción en la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - pageBottom callback existe en &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> La <span class="codeph"> llamada de retorno _satellite.pageBottom()</span> no se encontró dentro del <span class="codeph"> &lt;body&gt;</span> de la página, que Launch requiere. </p> <p>Esta prueba falla si no se encuentra la <span class="codeph"> llamada pageBottom en la </span>página o si está en la etiqueta <span class="codeph"> &lt;head&gt;</span> (o en alguna otra ubicación inesperada). Solo pasará si <span class="codeph"> pageBottom</span> se encuentra en algún lugar dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span> . Si no está en la página, no funcionará y las otras dos pruebas <span class="codeph"> pageBottom</span> también fallarán. </p> </td> 
   <td colname="col3"> <p>Agregue la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la funcionalidad de Launch adecuada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - pageBottom La llamada de retorno no debe existir cuando se implementa de forma asincrónica</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p>La <span class="codeph"> llamada de retorno _satellite.pageBottom()</span> se encontró en la página, lo cual no debería suceder cuando Launch se implementa de forma asíncrona. </p> </td> 
   <td colname="col3"> <p>Elimine el<span class="codeph"> script _satellite.pageBottom()</span> para habilitar la funcionalidad de Launch adecuada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target: presencia de código</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p>Target debe definirse en el DOM. </p> </td> 
   <td colname="col3"> <p>Instale la versión más reciente de Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> Target: biblioteca cargada en &lt;head&gt;</b> </p> <p>Peso: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Información adicional</a> </p> </td> 
   <td colname="col2"> <p> La biblioteca de Target debe cargarse en la etiqueta <span class="codeph"> &lt;head&gt;</span> . </p> </td> 
   <td colname="col3"> <p> Asegúrese de que la biblioteca de Target se carga en la etiqueta <span class="codeph"> &lt;head&gt;</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>
