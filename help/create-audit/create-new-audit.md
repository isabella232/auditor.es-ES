---
description: Crear una nueva auditoría en Auditor
seo-description: Crear una nueva auditoría en Auditor
seo-title: Crear una nueva auditoría en Auditor
title: Crear una nueva auditoría en Auditor
uuid: bd6798bb-3fab-4091-9e07-d3d1e5fdd087
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Create a new audit{#create-a-new-audit}

>[!NOTE]
>
>Los usuarios están limitados a una auditoría que se ejecuta a la vez. Se produce un error si intenta iniciar una auditoría con la misma configuración que la que se está ejecutando. Puede utilizar el vínculo del mensaje de error si desea cancelar la auditoría que se está ejecutando para poder crear una nueva.

Si lo desea, utilice el vínculo de la parte inferior de la página para acceder a una cuenta de prueba gratuita con todas las funciones con ObservePoint.

1. En la lista Auditor, haga clic en **[!UICONTROL Nueva auditoría]**.

   The [!DNL New Audit] screen opens.

   ![](assets/config.png)

1. (Requerido) Asigne un nombre a la auditoría.

   El nombre puede tener hasta 250 caracteres.
1. (Requerido) Especifique la dirección URL inicial.

   Se requiere el protocolo al especificar la dirección URL inicial. La dirección URL de inicio es la página donde la auditoría comienza a rastrear. Una vez iniciada, Auditor rastrea hasta 500 páginas, siguiendo los vínculos que comienzan en la dirección URL de inicio. Consulte [Incluir y excluir filtros](../create-audit/filters.md#concept-23531490bb124981ba807ed1806e3257) para obtener más información. La dirección URL inicial puede tener hasta 250 caracteres.

   >[!NOTE]
   >
   >En algunos casos, puede tomar hasta 48 horas completar un análisis de 500 páginas.

1. Especifique una o varias direcciones de correo electrónico para las notificaciones sobre esta auditoría.

   Puede especificar varios correos electrónicos separando cada dirección con una coma. El solicitante recibe una notificación predeterminada. Las direcciones de correo electrónico se validan en tiempo real. Si introduce una dirección no válida, se le notificará en la pantalla.

   Cada correo electrónico está limitado a no más de 250 caracteres, incluido el final de dominio (por ejemplo, .com).
1. Especifique Incluir filtros.

   Este campo puede contener direcciones URL exactas, direcciones URL parciales o expresiones regulares. Utilice este campo para los criterios con los que desea que todas las direcciones URL coincidan. Las direcciones URL rastreadas que no coincidan con los criterios de inclusión de filtros no se incluirán en los resultados de la auditoría.

   Puede introducir los directorios que desea que analice la auditoría. O bien, puede realizar una auditoría de varios dominios o de referencia automática, donde debe iniciar la auditoría en un dominio y finalizar en otro. Para ello, escriba los dominios que desee recorrer; para patrones de URL complejos, utilice una expresión regular.

   >[!NOTE]
   >
   >Si incluye una página en los filtros, pero no está conectada a la dirección URL de inicio, o el Auditor explora 500 páginas antes de llegar a esa página, la página no se analizará y no se incluirá en los resultados de la prueba.

   Los filtros de inclusión están limitados a 1000 caracteres por línea.

   Consulte [Incluir lista](../create-audit/filters.md#section-7626060a56a24b658f8c05f031ac3f5f) para obtener más información.
1. Especifique Excluir filtros.

   La lista Excluir evita que se auditen las direcciones URL. Use direcciones URL exactas, direcciones URL parciales o expresiones regulares, como haría en la lista de inclusión.

   Una práctica común es excluir un vínculo de cierre de sesión si la auditoría tiene una sesión de usuario (por ejemplo: `/logout`, es decir, cualquier dirección URL que contenga la cadena `/logout`).

   Los filtros de exclusión están limitados a 1000 caracteres por línea.

   Consulte [Excluir lista](../create-audit/filters.md#section-00aa5e10c878473b91ba0844bebe7ca9) para obtener más información.
1. (Opcional) Si lo desea, puede probar los filtros de inclusión y exclusión y probar las direcciones URL.

   Introduzca los filtros y las direcciones URL y, a continuación, haga clic en **[!UICONTROL Aplicar]** para ejecutar la prueba.

   ![](assets/test-advanced-filters.png)

1. Haga clic en **[!UICONTROL Ejecutar informe]**.
