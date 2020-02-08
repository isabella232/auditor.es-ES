---
description: Los filtros de inclusión restringen los vínculos que una auditoría puede rastrear desde la dirección URL de inicio. Los filtros de exclusión impiden que una auditoría rastree los vínculos.
seo-description: Los filtros de inclusión restringen los vínculos que una auditoría puede rastrear desde la dirección URL de inicio. Los filtros de exclusión impiden que una auditoría rastree los vínculos.
seo-title: Filtros Incluir y Excluir
title: Filtros Incluir y Excluir
uuid: 477fc38c-7351-42dd-8209-2fb7549ee34c
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Filtros Incluir y Excluir{#include-and-exclude-filters}

Los filtros de inclusión restringen los vínculos que una auditoría puede rastrear desde la dirección URL de inicio. Los filtros de exclusión impiden que una auditoría rastree los vínculos.

<!--
Content from ObservePoint (https://help.observepoint.com/articles/2872121-include-and-exclude-filters) with their permission. Modified slightly for style and Auditor emphasis.
-->

Incluir filtros y Excluir filtros proporcionan directrices para las auditorías. Al dejar vacíos los filtros Incluir y Excluir, una auditoría puede rastrear cualquier vínculo que se encuentre, empezando por los vínculos en la dirección URL de inicio.

![](assets/filter.png)

Al aplicar filtros de inclusión, filtros de exclusión o una combinación de ambos, instrucciones sobre los vínculos que puede rastrear una auditoría.

Cualquier elemento del campo Incluir filtros restringe la exploración solo a las páginas que coincidan con ese elemento. Cualquier elemento del campo Excluir filtros evita que se digitalice cualquier página que coincida con ese elemento.

Los filtros Incluir y Excluir pueden ser direcciones URL completas, direcciones URL parciales o expresiones regulares que coincidan con una página válida.

## Orden de precedencia {#section-e9d42419dd3f459bb20e7a33c6104f12}

1. **La dirección URL** de inicio tiene prioridad sobre todo lo demás y siempre se visitará durante una auditoría, incluso si una dirección URL coincide con un elemento de los filtros Excluir. La dirección URL de inicio siempre se visita antes que cualquier otra dirección URL.

   ![](assets/startingpage.png)

   En la imagen anterior, una auditoría detecta los vínculos de la propiedad de la página `document.links` de inicio. Estos vínculos pueden analizarse en la auditoría.

1. **Las direcciones URL** de inclusión deben vincularse desde una página de inicio; de lo contrario, no se pueden descubrir ni se visitarán.

   ![](assets/includefilter.png)

   En la imagen de arriba, al agregar un filtro Incluir se restringen las direcciones URL elegibles a las que coinciden con el filtro. Ahora sólo cinco enlaces pueden ser analizados por la auditoría.

1. **Excluir direcciones URL** elimina los vínculos de los requisitos.

   ![](assets/excludefilter.png)

   En la imagen de arriba, al agregar un filtro Excluir, se evita que las direcciones URL de los vínculos elegibles. Ahora sólo tres vínculos pueden ser analizados por la auditoría.

## Dirección URL de inicio {#section-ccb46abcd96f4a8ab171245015d2b724}

Auditor requiere una sola página para la dirección URL de inicio. La dirección URL de inicio siempre se visita antes que cualquier otra dirección URL. Los vínculos descubiertos desde la página de inicio pueden visitarse, con sujeción a los filtros Incluir y Excluir. Si un elemento Excluir coincide con una dirección URL de inicio, se omitirá.

## Incluir filtros {#section-7626060a56a24b658f8c05f031ac3f5f}

Los filtros Incluir limitan los vínculos que pueden analizarse durante una auditoría. Los filtros de inclusión pueden ser:

* Direcciones URL completas
* URL parcial
* Expresiones regulares que coinciden con direcciones URL completas o parciales
* Cualquier combinación de lo anterior

La adición de direcciones URL o expresiones regulares al filtro Incluir no garantiza que esas direcciones URL específicas se analizarán en la auditoría. La auditoría inspecciona los vínculos en la dirección URL de inicio y luego navega por los vínculos elegibles. La auditoría continúa este proceso de inspección y navegación hasta que se alcance el límite de 500 direcciones URL escaneadas o hasta que no se encuentren más vínculos elegibles.

>[!NOTE]
>
>En algunos casos, puede tomar hasta 48 horas completar un análisis de 500 páginas.

De forma predeterminada, una auditoría analizará todos los subdominios de la dirección URL inicial. A menos que se sobrescriba explícitamente al proporcionar un filtro de inclusión, la exploración utilizará el siguiente filtro de inclusión de regex:

`^https?://([^/:\?]*\.)?mysite.com`

Esto hace que cualquier vínculo encontrado en la página de URL de inicio sea elegible para visitar. Coincide con cualquier página de cualquier subdominio desde la dirección URL de inicio.

El uso del filtro Incluir predeterminado proporciona un intervalo amplio para que una auditoría se rastree. Para acceder a ciertas secciones o páginas, proporcione instrucciones específicas para la auditoría mediante la adición de filtros en este cuadro. En ese caso, reemplace el valor predeterminado por los directorios que desea que analice la auditoría. También puede utilizar filtros de inclusión para realizar auditorías entre dominios donde necesite iniciar la auditoría en un dominio y finalizar en otro. Para ello, escriba los dominios que desee recorrer. En cualquier caso, para encontrar cualquier URL de filtro de inclusión, deben descubrirse en una página auditada.

Los filtros de inclusión pueden contener direcciones URL exactas, direcciones URL parciales o expresiones regulares. Por ejemplo, si la dirección URL inicial es [!DNL http://mysite.com], las siguientes páginas podrían explorarse de forma predeterminada (observe los caracteres en negrita):

```
http://mysite.com
http
<b>s</b>://mysite.com
http://
<b>www</b>.mysite.com/home
http://
<b>dev</b>.mysite.com/home
http://
<b>my</b>.mysite.com/products/products_and_services.html
```

Para patrones de URL complejos, utilice el probador [de expresiones regulares de](http://regex.observepoint.com/)ObservePoint.

Consulte también el documento Expresiones regulares [comunes para ObservePoint](https://help.observepoint.com/articles/2872116-common-regular-expressions-for-observepoint) para ver los casos de uso de coincidencia de patrones comunes.

## Excluir filtros {#section-00aa5e10c878473b91ba0844bebe7ca9}

Los filtros Excluir impiden que se auditen las direcciones URL. Puede utilizar direcciones URL exactas, direcciones URL parciales o expresiones regulares. No se visita ninguna dirección URL que coincida con un elemento de los filtros Excluir. Si la URL de inicio se incluye en los filtros Excluir, no se excluye. Una auditoría siempre analiza la dirección URL de inicio.

## Prueba de filtros y direcciones URL {#section-3cfa125b1756411395a64701e128efa0}

Puede probar los filtros y las direcciones URL en Auditor.

Durante la creación de la auditoría, haga clic en **[!UICONTROL Probar filtros]** avanzados. Introduzca los filtros y las direcciones URL y, a continuación, haga clic en **[!UICONTROL Aplicar]**.

![](assets/test-advanced-filters.png)

## Documentación de ObservePoint {#section-79cdc8e850d047969b6d2badf6bbd6f9}

Este artículo fue desarrollado en cooperación con ObservePoint. Para obtener la información más reciente, consulte la documentación [de](https://help.observepoint.com/articles/2872121-include-and-exclude-filters)ObservePoint.
