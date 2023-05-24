---
description: Preguntas y respuestas comunes sobre Adobe Experience Platform Auditor
seo-description: Common questions and answers about Adobe Experience Platform Auditor
seo-title: Adobe Experience Platform Auditor FAQ
title: Preguntas frecuentes sobre Adobe Experience Platform Auditor
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
exl-id: 75ab4497-5822-4f64-9b6d-6cbf13687e8d
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 100%

---

# Preguntas frecuentes sobre Adobe Experience Platform Auditor{#auditor-faq}

Este artículo incluye las respuestas a las preguntas frecuentes sobre Adobe Experience Platform Auditor.

* [¿Qué es Adobe Experience Platform Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [¿Mi empresa puede utilizar Platform Auditor?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [¿Qué tecnologías de Adobe clasifica Platform Auditor?](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [¿Cuántas auditorías puedo realizar?](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [¿Qué se rastrea durante una auditoría?](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [¿Cuánto tiempo necesita una auditoría?](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [¿Qué información incluye un informe?](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [¿Hasta qué punto se puede procesar esa información?](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [¿Platform Auditor puede auditar tecnologías que no son de Adobe?](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [¿Puedo autorizar mis direcciones IP para permitir la digitalización de páginas...?](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [¿Platform Auditor utiliza los mismos intervalos de IP que Observepoint?](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## ¿Qué es Adobe Experience Platform Auditor?  {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Platform Auditor es un servicio de Adobe Experience Cloud que se ha desarrollado en colaboración con ObservePoint, expertos en validación de implementaciones digitales.

Con Platform Auditor, los clientes pueden analizar hasta 500 páginas web a la vez y recibir un informe que especifica cómo mejorar sus implementaciones de Adobe Experience Cloud y recibir el valor total de su inversión en Adobe.

## ¿Puedo utilizar Platform Auditor?  {#section-f90094050d1e44929066a942833435cf}

Todas las organizaciones de clientes de Adobe Experience Cloud disponen de acceso gratuito a Platform Auditor (desde el 1 de mayo de 2018). Antes de acceder a la funcionalidad, todos los usuarios deben aceptar las condiciones de uso de Adobe/ObservePoint en la interfaz de usuario de Adobe Experience Cloud. Para rechazar las condiciones, póngase en contacto con el Administrador de cuentas.

## ¿Cómo puedo acceder a Platform Auditor?  {#section-531ff85f94384831a89cbb4109549daf}

Inicie sesión en [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), haga clic en la opción Platform Auditor en **[!UICONTROL Activation]**, en la barra de navegación superior. También puede ir directamente a [https://auditor.adobe.com](https://auditor.adobe.com).

## ¿Qué tecnologías de Adobe clasifica Platform Auditor?  {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Servicio de Experience Cloud ID (anteriormente, servicio de Marketing Cloud ID)
* Target

Actualmente, las siguientes soluciones de Adobe no están incluidas en las pruebas de implementación. Se prevé ofrecer soporte para estas soluciones en futuras actualizaciones.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Adobe Experience Platform Launch

## ¿Cuántas auditorías puedo realizar?  {#section-caac1e50ce1249aeba76308f3ef03fa0}

No hay límite en el número de auditorías que se pueden realizar. Los usuarios están limitados a realizar una auditoría a la vez. Si intenta iniciar una auditoría con la misma configuración que la que se está ejecutando, se produce un error.

## ¿Qué se rastrea para una auditoría?  {#section-6d068ed69ece4a1bb6d0c34454550c45}

Actualmente, la tecnología ObservePoint rastrea las direcciones URL presentes en los enlaces de documentos. No se rastrean los enlaces encontrados en botones, widgets de paginación y otros elementos de página similares.

## ¿Cómo puedo sugerir nuevos criterios para las pruebas de Platform Auditor?  {#section-926e6ef9225b4f0bb19c2927d634cd77}

Puede enviar sugerencias para las pruebas a través de la comunidad de Platform Auditor haciendo clic en **[!UICONTROL Compartir comentario]** en esta página: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## ¿Cuánto tiempo necesita una auditoría?  {#section-5086ae27ef1f4671a9d951348654633a}

El tiempo para realizar una auditoría depende de muchos factores, entre ellos:

* Tiempo de carga de la página

   El motor ObservePoint carga cada página de la auditoría en un explorador. Cuanto más rápido se carga una página, más rápido se realiza la auditoría.
* Conexiones simultáneas

   Platform Auditor utiliza una única conexión para visitar cada página. Las cuentas completas de ObservePoint utilizan hasta 10 motores a la vez.
* Silencio de red

   Después de cargar cada página, la auditoría espera un silencio de red de siete segundos antes de pasar a la siguiente página. Si una página envía muchas solicitudes de red que se producen después de cargarse la página, la espera finaliza en 60 segundos.
* Reintentos de página

   Si no se encuentra una página o etiqueta, la auditoría guarda esa dirección URL y más tarde vuelve a la misma durante la auditoría. La auditoría visita una página hasta tres veces para asegurarse de que el error no se debe a un problema transitorio.
* Procesamiento

   Tras realizar una auditoría, todos los datos obtenidos se procesan y se filtran a través de las normas. Este tiempo de procesamiento es considerable, aunque no tarda tanto como el propio análisis.

>[!NOTE]
>
>Platform Auditor hace un único análisis a la vez. Las cuentas de Full ObservePoint pueden realizar varias auditorías consecutivamente.

## ¿Qué información incluye un informe?  {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

Cada análisis genera un informe que incluye las direcciones URL analizadas, los problemas encontrados en esas páginas web y las recomendaciones sobre cómo corregir dichos problemas.

Los resultados de los análisis se clasifican en tres categorías:

* Configuración
* Coherencia de etiquetas
* Presencia de etiqueta

Además de estas tres categorías, el informe incluye alertas con información que debe tenerse en cuenta, aunque no necesariamente exigen una acción inmediata.

Las recomendaciones de estas categorías se clasifican en otras tres categorías:

* Muy recomendado
* Recomendado
* Aprobado

## ¿Cómo es de procesable esa información?  {#section-9308c1ea882048b781087ae6d2eee9f0}

Todas las recomendaciones que ofrece Platform Auditor le ayudan a solucionar un problema durante la implementación de soluciones de Adobe Experience Cloud, como DTM o Target. Para facilitarle este proceso, el equipo de Platform Auditor ha trabajado intensamente para ofrecer unas instrucciones de uso específicas. Para identificar las zonas problemáticas con facilidad, puede exportar una hoja de cálculo con todas las direcciones URL analizadas y todos los resultados de la prueba. Seguidamente, se incluye un ejemplo de una recomendación para implementación de DTM:

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Última devolución de llamada pageBottom</b> </p> <p>Para una correcta implementación de la DTM, se necesita una función _satellite.pageBottom(). Para garantizar la funcionalidad adecuada de la DTM, añada la secuencia de comandos en línea justo antes de la etiqueta &lt;/body&gt; de cierre. </p> </td> 
  </tr> 
 </tbody> 
</table>

## ¿Platform Auditor puede auditar tecnologías que no son de Adobe?  {#section-f6e73c56083b4815bbf901296038bcd4}

No. Sin embargo, la opción Full ObservePoint permite auditar y controlar todas las etiquetas y tecnologías de marketing. Como cliente de Adobe, dispone de una cuenta de prueba gratuita. Para acceder a su cuenta de prueba, visite [Página de Platform Auditor de ObservePoint](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium).

## ¿Puedo autorizar mis direcciones IP para permitir la digitalización de páginas protegidas con un inicio de sesión?  {#section-011e4f54c58140ffb93bedeb0745b6cc}

Actualmente, esta funcionalidad solo está incluida en la opción Full ObservePoint.

## ¿Platform Auditor utiliza los mismos intervalos de IP que ObservePoint?  {#section-39512b156e194787981bdd572ff5b5a9}

ObservePoint realiza el rastreo, por lo que se utilizan las mismas direcciones IP.

Para obtener más información, consulte el [manual de ObservePoint](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list).
