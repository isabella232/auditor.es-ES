---
description: 'null'
seo-description: 'null'
seo-title: Auditor Preguntas más frecuentes
title: Preguntas más frecuentes sobre el auditor
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Preguntas más frecuentes sobre el auditor{#auditor-faq}

Este artículo contiene las respuestas a las preguntas más frecuentes sobre Adobe Experience Platform Auditor.

* [¿Qué es Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [¿Mi empresa cumple los requisitos para utilizar Auditor?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [¿Qué tecnologías de Adobe clasifica Auditor?](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [¿Cuántas auditorías puedo realizar?](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [¿Qué se busca para una auditoría?](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [¿Cuánto tarda una auditoría?](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [¿Qué información se proporciona en un informe?](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [¿Qué tan procesable es esa información?](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [¿Auditor puede auditar la tecnología que no es de Adobe?](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [¿Puedo incluir en la lista blanca mis direcciones IP para permitir la digitalización de páginas...](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [¿Utiliza Auditor los mismos intervalos de IP que Observepoint?](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## ¿Qué es Auditor? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Auditor es un servicio de Adobe Experience Cloud que se ha desarrollado conjuntamente con ObservePoint, expertos en validación de implementaciones digitales.

Con Auditor, los clientes pueden analizar hasta 500 páginas web a la vez y recibir un informe que muestre cómo mejorar sus implementaciones de Adobe Experience Cloud para que reciban el valor total de su inversión en Adobe.

## ¿Puedo usar Auditor? {#section-f90094050d1e44929066a942833435cf}

Todas las organizaciones de clientes de Adobe Experience Cloud tienen acceso gratuito a Auditor (a partir del 1 de mayo de 2018). Cada usuario debe aceptar las condiciones de uso de Adobe/ObservePoint en la interfaz de usuario de Adobe Experience Cloud antes de acceder a la funcionalidad. Para optar por la exclusión de los términos, comuníquese con el administrador de cuentas.

## ¿Cómo puedo acceder a Auditor? {#section-531ff85f94384831a89cbb4109549daf}

Después de iniciar sesión en [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), encontrará la opción Auditor haciendo clic en **[!UICONTROL Activación]** en la barra de navegación superior. También puede ir directamente a [https://auditor.adobe.com](https://auditor.adobe.com).

## ¿Qué tecnologías de Adobe clasifica Auditor? {#section-52833b71c05448aaae508e6070a387f5}

* DSP de Advertising Cloud
* Búsqueda en Advertising Cloud
* Analytics
* DTM
* Servicio de ID de Experience Cloud (anteriormente Servicio de Marketing Cloud ID)
* Target

Actualmente, las siguientes soluciones de Adobe no están incluidas en la rúbrica de prueba. Está previsto ofrecer soporte para estas soluciones en futuras actualizaciones.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Launch

## ¿Cuántas auditorías puedo realizar? {#section-caac1e50ce1249aeba76308f3ef03fa0}

No hay límite en el número de auditorías que puede ejecutar. Los usuarios están limitados a una auditoría que se ejecuta a la vez. Se produce un error si intenta iniciar una auditoría con la misma configuración que la que se está ejecutando.

## ¿Qué se busca para una auditoría? {#section-6d068ed69ece4a1bb6d0c34454550c45}

La tecnología ObservePoint rastrea actualmente las direcciones URL que se encuentran en los vínculos de documentos. Los vínculos encontrados en botones, utilidades de paginación y otros elementos de página de este tipo no se rastrean.

## ¿Cómo puedo sugerir nuevos criterios para las pruebas de Auditor? {#section-926e6ef9225b4f0bb19c2927d634cd77}

Puede enviar sugerencias para las pruebas a través de la Comunidad de auditores haciendo clic en **[!UICONTROL Compartir comentarios]** en esta página: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## ¿Cuánto tarda una auditoría? {#section-5086ae27ef1f4671a9d951348654633a}

Hay muchos factores que contribuyen al tiempo que lleva completar una auditoría, entre ellos:

* Tiempo de carga de la página

   El motor ObservePoint carga cada página de la auditoría en un explorador. Cuanto más rápido se carga una página, más rápido se completa la auditoría.
* Conexiones simultáneas

   Adobe Auditor utiliza una sola conexión para visitar cada página. Las cuentas completas de ObservePoint utilizan hasta 10 motores a la vez.
* Silencio de red

   Después de cargar cada página, la auditoría espera un silencio de red de siete segundos antes de pasar a la página siguiente. Si una página envía muchas solicitudes de red que se producen después de que se cargue la página, la espera se agotará al cabo de 60 segundos.
* Reintentos de página

   Si no se encuentra una página o etiqueta, la auditoría almacena esa dirección URL y regresa a ella más adelante en la auditoría. La auditoría visitará una página hasta tres veces para asegurarse de que el error no fue causado por un problema transitorio.
* Procesando

   Después de ejecutar una auditoría, todos los datos recopilados se procesan y filtran a través de las reglas. Este tiempo de procesamiento es significativo, aunque no tarda tanto como el análisis en sí.

>[!NOTE]
>
>Adobe Auditor ejecuta un único análisis a la vez. Las cuentas completas de ObservePoint pueden ejecutar muchas auditorías de forma consecutiva.

## ¿Qué información se proporciona en un informe? {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

Cada análisis genera un informe que muestra qué direcciones URL se analizaron, los problemas encontrados en esas páginas web y las recomendaciones sobre cómo corregir los problemas encontrados.

Los resultados de los análisis se dividen en tres categorías:

* Configuración
* Coherencia de etiquetas
* Presencia de etiqueta

Además de estas tres categorías, el informe proporciona alertas que contienen información que debe conocer, pero que no necesariamente requieren una acción inmediata.

Las recomendaciones incluidas en estas categorías se dividen en tres categorías adicionales:

* Altamente recomendado
* Recomendado
* Aprobado

## ¿Qué tan procesable es esa información? {#section-9308c1ea882048b781087ae6d2eee9f0}

Todas las recomendaciones que se proporcionan a través de Auditor están destinadas a ayudarle a tomar medidas para solucionar un problema con la implementación de soluciones de Adobe Experience Cloud, como DTM o Target. Para facilitar esto, el equipo del Auditor ha trabajado extensamente para proporcionar instrucciones muy detalladas sobre lo que debe hacerse. Puede exportar una hoja de cálculo con todas las direcciones URL analizadas y todos los resultados de la prueba para poder identificar fácilmente las áreas problemáticas. Este es un ejemplo de una recomendación para una implementación de DTM:

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom llamada de retorno última</b> </p> <p>Se requiere una función _satellite.pageBottom() para una implementación correcta de la DTM. Agregue la secuencia de comandos en línea inmediatamente antes de la etiqueta &lt;/body&gt; de cierre para garantizar la funcionalidad adecuada de la DTM. </p> </td> 
  </tr> 
 </tbody> 
</table>

## ¿Auditor puede auditar la tecnología que no es de Adobe? {#section-f6e73c56083b4815bbf901296038bcd4}

No. Sin embargo, la oferta completa de ObservePoint permite a los clientes auditar y monitorear todas las etiquetas y tecnologías de mercadotecnia. Como cliente de Adobe, tiene acceso a una cuenta de prueba gratuita. Para acceder a su cuenta de prueba, visite la página [del auditor de](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&utm_medium=Auditor&utm_campaign=Premium)ObservePoint.

## ¿Puedo incluir en la lista blanca mis direcciones IP para permitir el escaneo de páginas protegidas por un inicio de sesión? {#section-011e4f54c58140ffb93bedeb0745b6cc}

Esta funcionalidad no se admite actualmente sin la oferta completa de ObservePoint.

## ¿Utiliza Auditor los mismos intervalos de IP que ObservePoint? {#section-39512b156e194787981bdd572ff5b5a9}

ObservePoint realiza el rastreo, por lo que se utilizan las mismas direcciones IP.

Consulte la documentación [de](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list) ObservePoint para obtener más detalles.
