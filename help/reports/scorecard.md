---
description: Después de ejecutar una prueba, el cuadro de mandos muestra información sobre una auditoría.
seo-description: Después de ejecutar una prueba, el cuadro de mandos muestra información sobre una auditoría.
seo-title: Cuadro de mandos
title: Cuadro de mandos
uuid: a765cd6a-d3d6-4438-9621-d7899385a518
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Cuadro de mandos{#scorecard}

Después de ejecutar una prueba, el cuadro de mandos muestra información sobre una auditoría.

Haga clic en el nombre de la auditoría en la página Auditor para ver los resultados de la prueba.

![](assets/report.png)

Use el cuadro de mandos para ver cómo se realizó la auditoría en las siguientes categorías:

* Puntuación general
* Presencia de etiquetas

   Evalúa si la etiqueta existe y si está en el lugar correcto en el código de página.
* Coherencia de etiquetas

   Evalúa si las etiquetas son coherentes en todas las direcciones URL.
* Configuración

   Evalúa las etiquetas en relación con otras reglas y las prácticas recomendadas.
* Alerta

   Las alertas muestran los problemas que debe tener en cuenta, pero que no afectan a su puntuación.

La puntuación depende del peso de cada prueba y de si se supera o no. Si se aprueba, la puntuación aumenta en el número de puntos igual al peso de la prueba.

* 0: Le alerta de problemas que debe tener en cuenta, pero que no afectan a su puntuación.
* 1: Recomienda una optimización. No afecta a la precisión de los datos.
* 2: Si no realiza esta prueba, no tendrá acceso a las últimas funciones y correcciones de Adobe Experience Cloud.
* 3: Prueba de la eficiencia y si la implementación se ajusta a las mejores prácticas recomendadas.
* 4: Si falla, es posible que esté recopilando datos poco fiables.
* 5: Error significa que puede ver la pérdida de datos.

El cuadro de mandos enumera los problemas de nivel 4 o 5 como **altamente recomendados** para corregirlos.

El cuadro de mandos enumera los problemas de nivel 1 a 3 **recomendados** para corregirlos.

Haga clic en **[!UICONTROL Descargar el informe]** para descargar un archivo de Excel o PDF con la información registrada en la auditoría.

Además de la puntuación de cada categoría, el cuadro de mandos enumera las correcciones que se recomiendan o se recomiendan con mayor frecuencia, así como los elementos que superaron la prueba. Haga clic en cada número para ver detalles adicionales en el cuadro de la derecha. Haga clic de nuevo para explorar en profundidad y ver recomendaciones sobre cómo solucionar el problema. A continuación se muestran los detalles de un problema de Recomendaciones en el cuadro de mandos que se muestra arriba:

![](assets/report-issue-details.png)

Haga clic en las categorías en la parte superior de la pantalla para ver los problemas encontrados en cada categoría.

## ¿Qué páginas formaban parte de la prueba? {#section-fd38ffeb868648e89c34c5772fa65f46}

Puede ver las listas de direcciones URL que superaron o suspendieron la prueba.

En Cuadro de mandos, haga clic en un nombre de prueba o en el vínculo **[!UICONTROL Ver todo]** debajo de cada encabezado de categoría. Esto le lleva a conocer los detalles de las pruebas. Para cada prueba, puede ver la descripción de la prueba y una lista de todas las direcciones URL que fallaron y pasaron. Esta información también se incluye en los informes descargados.
