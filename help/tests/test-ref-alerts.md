---
description: Esta referencia proporciona más información sobre las alertas que Auditor muestra para las pruebas.
seo-description: Esta referencia proporciona más información sobre las alertas que Auditor muestra para las pruebas.
seo-title: Alertas
title: Alertas
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: ht
source-git-commit: 78105ff6766f48f3aaccfeda281e5b4883be856a

---


# Alertas {#alerts}

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
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud: Se ha implementado la etiqueta de conversión correcta</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Compruebe si se utiliza la etiqueta de conversión correcta. </p> <p> <p>Advertencia: El uso de etiquetas de conversión TubeMogul obsoletas puede causar la pérdida de datos. </p> </p> </td> 
   <td colname="col3"> <p>Actualice los píxeles de conversión a las nuevas etiquetas de conversión solo de imagen de Advertising Cloud. </p> <p>Esto puede realizarse fácilmente con la extensión de Launch de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud: Se ha utilizado la etiqueta JS correcta</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud debe utilizar las últimas etiquetas de JavaScript. </p> </td> 
   <td colname="col3"> <p>Actualice el JavaScript de Advertising Cloud con la última versión. El uso de versiones de JavaScript no compatibles puede causar la pérdida de funcionalidad. </p> <p>Esto puede realizarse más fácilmente mediante la extensión de Launch de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud: Etiqueta de solo imagen</b> </p> <p>Peso: 0 </p> </td> 
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
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud: píxeles de segmento: sincronización DSP habilitada</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Compruebe si el píxel del segmento TubeMogul contiene un ajuste de sincronización de DSP y recomiende que el ajuste se añada al píxel. </p> <p>La configuración de sincronización de DSP se determina por el uso de un parámetro de cadena de consulta, por lo que </p> <p>SI la etiqueta se está activando en<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> O <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> O <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>Y la etiqueta contiene el parámetro de URL <span class="codeph"> "sid=")</span> </p> <p>ENTONCES, compruebe si existe el parámetro de URL <span class="codeph"> "cs=0"</span> o<span class="codeph"> "cs=1"</span> y, en caso contrario, recomiende que <span class="codeph"> "cs=1"</span> se añada a esos píxeles para que mejoren los índices de coincidencia de audiencia. </p> </td> 
   <td colname="col3"> <p> Añada el parámetro de URL <span class="codeph"> "cs=1"</span> a los píxeles de Advertising Cloud para que se sincronice con DSP, lo que aumenta los índices de coincidencia de audiencia. </p> <p>Esto se puede realizar fácilmente con la extensión de Advertising Cloud Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    </draft-comment> <p><b>DTM: colocación de la llamada de retorno pageBottom</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Más información</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>Dynamic Tag Management (DTM) exige la función <span class="codeph"> _satellite.pageBottom()</span>. Añada la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la correcta funcionalidad de la DTM. </p> <p> <p>Nota: Se recomienda que la etiqueta sea la <i>última</i> etiqueta en el <span class="codeph"> &lt;body&gt;</span>. Si se encuentra dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span>, puede funcionar, pero como no es una práctica recomendada, podría funcionar incorrectamente o dar resultados inesperados o no deseados. </p> </p> </td> 
   <td colname="col3"> <p>Añada la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la correcta funcionalidad de la DTM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM: Sistema autoalojado</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/dtm/using/client-side/client-side-information.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> La biblioteca de DTM se aloja en la instancia de Adobe Akamai en <span class="filepath"> assets.adobedtm.com</span>. </p> <p> El autoalojamiento es el método recomendado para cargar DTM, ya que ofrece un mayor control del rendimiento del sitio web mediante el control de caché, la reducción de las dependencias de scripts de terceros y un mayor control durante el proceso de publicación. Las bibliotecas de DTM se pueden alojar y administrar a través de su propio alojamiento web o CDN. </p> </td> 
   <td colname="col3"> <p>El autoalojamiento es el método recomendado para cargar DTM en una página. Aunque el alojamiento de DTM a través de la CDN de Akamai generalmente funciona, el autoalojamiento mejora el rendimiento de la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Servicio de Experience Cloud ID: utilice solo un AdobeOrg</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/id-service/using/intro/id-request.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>En una implementación ECID normal, debe utilizarse un único AdobeOrg. </p> </td> 
   <td colname="col3"> <p>Verifique que existen varios ID de AdobeOrg para esta implementación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch: colocación de llamada de retorno pageBottom</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Más información</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>Launch debe tener una función de llamada de retorno <span class="codeph"> pageBottom </span> definida en último lugar del cuerpo de la página si se utiliza sincrónicamente. </p> <p> <p>Nota: Se recomienda que la etiqueta sea la <i>última</i> etiqueta en el <span class="codeph"> &lt;body&gt;</span>. Si se encuentra dentro de la etiqueta <span class="codeph"> &lt;body&gt;</span>, puede funcionar, pero como no es una práctica recomendada, podría funcionar incorrectamente o dar resultados inesperados o no deseados. </p> </p> </td> 
   <td colname="col3"> <p>Launch exige la función <span class="codeph"> _satellite.pageBottom()</span> para implementaciones sincrónicas. Añada la secuencia de comandos en línea inmediatamente antes de la etiqueta de cierre <span class="codeph"> &lt;/body&gt;</span> para garantizar la correcta funcionalidad de Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch: Autoalojado</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="https" scope="external">Introducción de Launch</a> </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/reference/client-side-info/asynchronous-deployment.html" format="https" scope="external"> Implementación asincrónica de Launch</a> </p> </td> 
   <td colname="col2"> <p>La biblioteca de Launch se aloja en la instancia de Adobe Akamai en <span class="filepath"> assets.adobedtm.com</span>. </p> <p>El autoalojamiento es el método recomendado para cargar Launch, ya que ofrece un mayor control del rendimiento del sitio web mediante el control de caché, la reducción de las dependencias de scripts de terceros y un mayor control durante el proceso de publicación. Las bibliotecas de Launch se pueden alojar y administrar a través de su propio alojamiento web o CDN. </p> </td> 
   <td colname="col3"> <p>Aunque el alojamiento de Launch a través de la CDN de Akamai funciona en la mayoría de los casos, se recomienda utilizar el alojamiento propio como el primer paso para mejorar el rendimiento de la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch: Debe implementarse asincrónicamente</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p>Launch debe implementarse asincrónicamente para obtener un rendimiento óptimo. </p> </td> 
   <td colname="col3"> <p>Incluya el parámetro async en la secuencia de comandos en línea para garantizar la correcta funcionalidad asincrónica de Launch </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target: Contenido en mboxDefault</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/es-ES/target/using/implement-target/implementing-target.html" format="html" scope="external"> Más información</a> </p> </td> 
   <td colname="col2"> <p> El contenido debe estar presente en mboxDefault si se utiliza at.js. </p> </td> 
   <td colname="col3"> <p>Compruebe que el contenido está disponible. </p> </td> 
  </tr> 
 </tbody> 
</table>

