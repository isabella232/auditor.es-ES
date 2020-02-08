---
description: Esta referencia proporciona más información sobre las pruebas que realiza el Auditor.
seo-description: Esta referencia proporciona más información sobre las pruebas que realiza el Auditor.
seo-title: Referencia de prueba
title: Referencia de prueba
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
translation-type: tm+mt
source-git-commit: 0c116f699b697ad010ee074ac67159a49ec09ccd

---


# Referencia de prueba{#test-reference}

Esta referencia proporciona más información sobre las pruebas que realiza el Auditor.

**Versión de criterios de evaluación actuales:** 1.0.5

Cada prueba está ponderada. La puntuación de la prueba es igual al peso asignado. Si supera una prueba con un peso de cinco puntos, recibirá cinco puntos.

* 0: Le alerta de problemas que debe tener en cuenta, pero que no afectan a su puntuación.
* 1: Recomienda una optimización. No afecta a la precisión de los datos.
* 2: Si no realiza esta prueba, no tendrá acceso a las últimas funciones y correcciones de Experience Cloud.
* 3: Prueba de la eficiencia y si la implementación sigue las optimizaciones.
* 4: Si falla, es posible que esté recopilando datos poco fiables.
* 5: Error significa que puede ver la pérdida de datos.

Las pruebas son superadas o no. Proban el cumplimiento o el incumplimiento de las condiciones de prueba, por lo que no hay puntuaciones parciales para el cumplimiento parcial. Por ejemplo, si la prueba comprueba la versión más reciente de una solución de Adobe y solo está una versión por detrás, obtendrá la misma puntuación que si hubiera vuelto a cinco versiones. Las versiones más recientes incluyen mejoras de rendimiento y correcciones de errores, por lo que se recomienda que esté en la versión más reciente.

Se **recomienda encarecidamente** corregir cualquier resultado de los niveles 4 o 5.

Se **recomienda** corregir cualquier resultado de los niveles 1 a 3.

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

## Categorías de prueba {#section-630181db21ef4eec9ce6a13a0482bb55}

Esta referencia de prueba divide las pruebas en las siguientes categorías:
