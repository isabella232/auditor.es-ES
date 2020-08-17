---
description: Esta referencia proporciona más información sobre las pruebas que realiza Auditor para detectar la presencia de etiquetas.
seo-description: Esta referencia proporciona más información sobre las pruebas que realiza Auditor para detectar la presencia de etiquetas.
seo-title: Presencia de etiquetas
title: Presencia de etiquetas
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: tm+mt
source-git-commit: a76ecb232c29d83ef82b14be460d9ce60f5e8662
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 100%

---


# Presencia de etiquetas

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
   <td colname="col1"> <p><b>Advertising Cloud: Presencia de código</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> La etiqueta de Advertising Cloud no está disponible en el DOM. </p> </td> 
   <td colname="col3"> <p>Aplique la etiqueta de Advertising Cloud mediante la extensión de Launch de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud: Píxel de segmento implementado</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> Actualice los píxeles del segmento de Advertising Cloud con las nuevas etiquetas de solo imagen de Advertising Cloud. El uso de etiquetas de segmento AMO no soportadas puede causar la pérdida de datos. </p> </td> 
   <td colname="col3"> <p>Implemente el píxel del segmento de Advertising Cloud con la extensión de Launch de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analytics: Cargado en DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/analytics/implementation/home.html" format="https" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> No se ha detectado la etiqueta de Adobe Analytics. </p> </td> 
   <td colname="col3"> <p>Instale la última versión de Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM: Biblioteca cargada</b> </p> <p>Peso: 5 </p> <p>Más información: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> Resolución de problemas de DTM</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Adición de código de Encabezado y Pie de página</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> No se ha encontrado un objeto _satellite global en el DOM. Dynamic Tag Management no está instalada o no se puede ejecutar. </p> </td> 
   <td colname="col3"> <p>Compruebe que la biblioteca de la DTM está aplicada en la página y que no está bloqueada por las actividades de script posteriores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM: Un código incrustado</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/client-side/code.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> Los sitios de producción solo deben cargar una biblioteca de la DTM. </p> </td> 
   <td colname="col3"> <p>Compruebe que solo se está cargando la biblioteca de producción en la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM: la devolución de llamada pageBottom existe en &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> No se ha encontrado la llamada de retorno <span class="codeph"> _satellite.pageBottom()</span> dentro del <span class="codeph"> &lt;body&gt;</span> de la página, que exige Dynamic Tag Management. </p> <p>Esta prueba falla si no se encuentra la <span class="codeph"> llamada pageBottom en la </span>página o si está en la etiqueta <span class="codeph"> &lt;head&gt;</span> (o en otra ubicación inesperada). Solo funcionará correctamente si <span class="codeph"> pageBottom</span> se encuentra en algún lugar dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span>. Si no está en la página, no funcionará y las otras dos pruebas <span class="codeph"> pageBottom</span> también fallarán. </p> </td> 
   <td colname="col3"> <p>Añada la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la correcta funcionalidad de la DTM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM: etiqueta pageBottom activada</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> No se ha detectado la etiqueta DTM <code> pageBottom</code>. </p> <p>Esto puede suceder si la llamada se encuentra dentro de una <code> if</code> instrucción que genera algo parecido a <code> if (false) {_satellite.pageBottom()}</code>. Por tanto, aunque puede existir y estar colocada correctamente, la etiqueta podría no activarse. </p> </td> 
   <td colname="col3"> <p>Instale la llamada de DTM <code> pageBottom</code> en cada página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servicio de Experience Cloud ID: presencia de código</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/id-service/using/intro/overview.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>No se ha encontrado el código del servicio de Experience Cloud ID. El Experience Cloud ID (ECID) es muy recomendable para garantizarle que obtiene el máximo valor de sus soluciones de Experience Cloud y es fundamental para la administración de ID en todas las soluciones de Experience Cloud. </p> </td> 
   <td colname="col3"> <p> Instale la última versión de ECID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servicio de Experience Cloud ID: presencia de cookies</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/tools/macid.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> No se ha encontrado la cookie <span class="codeph"> AMCV_</span>. Debe crear una instancia de un objeto visitante desde el código<span class="codeph"> VisitorAPI.js</span>. </p> </td> 
   <td colname="col3"> <p> Si se trata de una aplicación de DTM, compruebe que el ID de AdobeOrg se ha introducido correctamente en la herramienta ECID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Servicio de Experience Cloud ID: Valor de MID presente</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/id-service/using/intro/cookies.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> No se ha encontrado el valor MID en la cookie <span class="codeph"> AMCV_</span>. </p> </td> 
   <td colname="col3"> <p>Vuelva a realizar la prueba para comprobar si hay latencia de API de ECID. Si esta situación persiste, póngase en contacto con el Servicio de atención al cliente de Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> Launch: biblioteca cargada</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> No se ha encontrado un objeto _satellite global en el DOM. Launch no está instalado o no se puede ejecutar. </p> </td> 
   <td colname="col3"> <p>Compruebe que la biblioteca de Launch está aplicada en la página y que no está bloqueada por las actividades de script posteriores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch: no hay varios scripts incrustados</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>No debe haber varios scripts incrustados cargados en la página. Los sitios de producción solo deben cargar una biblioteca de Launch. </p> </td> 
   <td colname="col3"> <p>Compruebe que solo se está cargando la biblioteca de producción en la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch: la llamada de retorno pageBottom se encuentra en &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> La <span class="codeph"> llamada de retorno _satellite.pageBottom()</span> no se ha encontrado en el <span class="codeph"> &lt;body&gt;</span> de la página, que exige Launch. </p> <p>Esta prueba falla si no se encuentra la <span class="codeph"> llamada pageBottom en la </span>página o si está en la etiqueta <span class="codeph"> &lt;head&gt;</span> (o en otra ubicación inesperada). Solo funcionará correctamente si <span class="codeph"> pageBottom</span> se encuentra en algún lugar dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span>. Si no está en la página, no funcionará y las otras dos pruebas <span class="codeph"> pageBottom</span> también fallarán. </p> </td> 
   <td colname="col3"> <p>Añada la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la correcta funcionalidad de Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch: la llamada de retorno pageBottom no debe existir cuando se aplica de forma asincrónica</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>La llamada de retorno <span class="codeph"> _satellite.pageBottom()</span> se ha encontrado en la página, cosa que no debería suceder cuando Launch se aplica de forma asíncrona. </p> </td> 
   <td colname="col3"> <p>Elimine el script <span class="codeph">_satellite.pageBottom()</span> para habilitar la correcta funcionalidad de Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target: presencia de código</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/target/using/implement-target/implementing-target.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>Target debe definirse en el DOM. </p> </td> 
   <td colname="col3"> <p>Instale la última versión de Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> Target: biblioteca cargada en &lt;head&gt;</b> </p> <p>Peso: 4 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/target/using/implement-target/implementing-target.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> La biblioteca de Target debe cargarse en la etiqueta <span class="codeph"> &lt;head&gt;</span>. </p> </td> 
   <td colname="col3"> <p> Compruebe que la biblioteca de Target se carga en la etiqueta <span class="codeph"> &lt;head&gt;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>
