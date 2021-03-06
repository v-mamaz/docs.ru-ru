---
title: Приложения SOA
description: Имейте в виду, что контейнеры могут быть также это вариант развертывания полезных приложений SOA.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: ee71873ac15246f979fd2b08d92280ba797ff6ee
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2019
ms.locfileid: "57675801"
---
# <a name="service-oriented-applications"></a>Сервис ориентированных приложений

Сервис-ориентированной архитектуры (SOA) был это большой нагрузкой термин, который означает множество разных вещей для разных людей. Но в качестве общего знаменателя термин SOA подразумевает структурирование архитектуры приложения путем его разделения на несколько служб (чаще всего в качестве HTTP-службы), которые можно классифицировать различными типами, такие как подсистемы или в других случаях, как уровни.

В настоящее время эти службы можно развернуть как контейнеры Docker, средства решения проблем, связанных с развертыванием, так как в образ контейнера включены все зависимости. Тем не менее когда необходимо горизонтальное масштабирование SOA, могут возникнуть трудности при развертывании на основе отдельных экземпляров. Этот запрос может обрабатываться с помощью кластеризации программного обеспечения или оркестратор Docker. Мы рассмотрим оркестраторы более подробно в следующем разделе, при изучении микрослужбы.

Контейнеры Docker являются полезным (но необязательным) элементом как для традиционных архитектур, ориентированных на службы, так и более сложных архитектур с микрослужбами.

В конце дня кластерные решения контейнера удобно для обоих традиционной архитектуры SOA, а также более сложные архитектуры микрослужб, в котором каждая микрослужба имеет свою модель данных. И благодаря нескольких баз данных, также можно масштабировать уровень данных, а не для работы с монолитных базами данных, совместно использоваться службами SOA. Тем не менее рассказ о разделении данных является чисто об архитектуре и разработке.

>[!div class="step-by-step"]
>[Назад](state-and-data-in-docker-applications.md)
>[Вперед](orchestrate-high-scalability-availability.md)
