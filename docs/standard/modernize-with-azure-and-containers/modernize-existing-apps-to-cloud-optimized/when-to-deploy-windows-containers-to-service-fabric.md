---
title: Когда следует развернуть контейнеры Windows Service Fabric
description: Модернизировать существующие приложения .NET с контейнерами Windows и облако Azure | Когда следует развернуть контейнеры Windows Service Fabric
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/30/2018
ms.openlocfilehash: c41db8b37c883f9369a6b8d1f8bccbc0535f504c
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2018
---
# <a name="when-to-deploy-windows-containers-to-service-fabric"></a><span data-ttu-id="76ed1-103">Когда следует развернуть контейнеры Windows Service Fabric</span><span class="sxs-lookup"><span data-stu-id="76ed1-103">When to deploy Windows Containers to Service Fabric</span></span>

<span data-ttu-id="76ed1-104">Приложения, основанные на доступ к контейнерам Windows необходимо быстро платформы, которые подключаются и еще более немедленно ВМ IaaS.</span><span class="sxs-lookup"><span data-stu-id="76ed1-104">Applications that are based on Windows Containers will quickly need to use platforms that move even further away from IaaS VMs.</span></span> <span data-ttu-id="76ed1-105">Это необходимо для автоматических масштабируемость и высокий уровень масштабируемости и получить значительные улучшения в возможности полного управления для развертываний, обновления, управление версиями, откат и наблюдение за работоспособностью.</span><span class="sxs-lookup"><span data-stu-id="76ed1-105">This is for improved automated scalability and high scalability, and to gain significant improvements in a complete management experience for deployments, upgrades, versioning, rollbacks, and health monitoring.</span></span> <span data-ttu-id="76ed1-106">Эти цели можно добиться с orchestrator Azure Service Fabric, доступным в облако Microsoft Azure, но и в локальной или даже в другом облаке.</span><span class="sxs-lookup"><span data-stu-id="76ed1-106">You can achieve these goals with the orchestrator Azure Service Fabric, available in the Microsoft Azure cloud, but also on-premises, or even in another cloud.</span></span>

<span data-ttu-id="76ed1-107">Во многих организациях поднимая и перенос существующих приложений монолитные в контейнеры по двум причинам:</span><span class="sxs-lookup"><span data-stu-id="76ed1-107">Many organizations are lifting and shifting existing monolithic applications to containers for two reasons:</span></span>

-   <span data-ttu-id="76ed1-108">Сокращение, либо из-за консолидацию и удаление существующего оборудования или по запуску приложений с более высокой плотности.</span><span class="sxs-lookup"><span data-stu-id="76ed1-108">Cost reductions, either due to consolidation and removal of existing hardware, or from running applications at a higher density.</span></span>

-   <span data-ttu-id="76ed1-109">Согласованное развертывание контракт между процессы разработки и эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="76ed1-109">A consistent deployment contract between development and operations.</span></span>

<span data-ttu-id="76ed1-110">Проводит сокращение расходов понятно и вполне вероятно, что все организации прослеживании этой цели.</span><span class="sxs-lookup"><span data-stu-id="76ed1-110">Pursuing cost reductions is understandable, and it's likely that all organizations are chasing that goal.</span></span> <span data-ttu-id="76ed1-111">Согласованное развертывание сложно оценить, но это одинаково, как важные.</span><span class="sxs-lookup"><span data-stu-id="76ed1-111">Consistent deployment is harder to evaluate, but it's equally as important.</span></span> <span data-ttu-id="76ed1-112">Контракт согласованного развертывания говорит, разработчики могут выбрать использование технология, которая подходит для них, что рабочая группа возвращает один способ развертывания и управления приложениями.</span><span class="sxs-lookup"><span data-stu-id="76ed1-112">A consistent deployment contract says that developers are free to choose to use the technology that suits them, and the operations team gets a single way to deploy and manage applications.</span></span> <span data-ttu-id="76ed1-113">Это соглашение устраняет усилий, затрачиваемых на наличие операций сложность множество различных технологий или принудительное разработчикам возможность работать только с определенных технологий.</span><span class="sxs-lookup"><span data-stu-id="76ed1-113">This agreement alleviates the pain of having operations deal with the complexity of many different technologies, or forcing developers to work only with certain technologies.</span></span> <span data-ttu-id="76ed1-114">По сути каждое приложение имеет контейнерных автономное развертывание образа.</span><span class="sxs-lookup"><span data-stu-id="76ed1-114">Essentially, each application is containerized in a self-contained deployment image.</span></span>

<span data-ttu-id="76ed1-115">В некоторых организациях продолжит модернизация, добавив микрослужбами (собственный облачные приложения), но во многих организациях окончится здесь (оптимизированную для облачных приложений).</span><span class="sxs-lookup"><span data-stu-id="76ed1-115">Some organizations will continue modernizing by adding microservices (Cloud-Native applications) but many other organizations will stop here (Cloud-Optimized applications).</span></span> <span data-ttu-id="76ed1-116">Как показано на рисунке 4-8, так как они могут не потребоваться этих организаций не перемещается микрослужбами архитектур.</span><span class="sxs-lookup"><span data-stu-id="76ed1-116">As shown in Figure 4-8, these organizations won't move to microservices architectures because they might not need to.</span></span> <span data-ttu-id="76ed1-117">В любом случае они уже получить преимущества, с помощью контейнеров, а также Service Fabric интерфейс предоставляет a полного управления, который включает в себя развертывание, обновление, управление версиями, откат и наблюдение за работоспособностью.</span><span class="sxs-lookup"><span data-stu-id="76ed1-117">In any case, they already get the benefits that using containers plus Service Fabric provides-a complete management experience that includes deployment, upgrades, versioning, rollbacks, and health monitoring.</span></span>

> ![Точность прогноза и приложение Service Fabric](./media/image8.png)
>
> <span data-ttu-id="76ed1-119">**Рис. 4-8.**</span><span class="sxs-lookup"><span data-stu-id="76ed1-119">**Figure 4-8.**</span></span> <span data-ttu-id="76ed1-120">Точность прогноза и приложение Service Fabric</span><span class="sxs-lookup"><span data-stu-id="76ed1-120">Lift and shift an application to Service Fabric</span></span>

<span data-ttu-id="76ed1-121">Для повторного использования существующего кода и точности прогнозов и shift является ключевой подход к Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="76ed1-121">A key approach to Service Fabric is to reuse existing code and lift and shift.</span></span> <span data-ttu-id="76ed1-122">Таким образом можно перенести имеющиеся приложения .NET Framework, с помощью контейнеров Windows и развертывать их в Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="76ed1-122">Therefore, you can migrate your current .NET Framework applications, by using Windows Containers, and deploy them to Service Fabric.</span></span> <span data-ttu-id="76ed1-123">Будет проще будет модернизация, в конечном счете, путем добавления новых микрослужбами.</span><span class="sxs-lookup"><span data-stu-id="76ed1-123">It will be easier to keep going modernizing, eventually, by adding new microservices.</span></span>

<span data-ttu-id="76ed1-124">При сравнении Service Fabric для других orchestrators, важно обратить внимание, что Service Fabric для старшего при запуске служб и приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="76ed1-124">When comparing Service Fabric to other orchestrators, it's important to highlight that Service Fabric is mature at running Windows-based applications and services.</span></span> <span data-ttu-id="76ed1-125">Службы на основе Windows и приложений, включая продукты корпорации Майкрософт для уровня 1, критически важных лет выполнения Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="76ed1-125">Service Fabric has been running Windows-based services and applications, including Tier-1, mission-critical products from Microsoft for years.</span></span> <span data-ttu-id="76ed1-126">Она была первой orchestrator иметь общей доступности для контейнеров Windows.</span><span class="sxs-lookup"><span data-stu-id="76ed1-126">It was the first orchestrator to have general availability for Windows Containers.</span></span> <span data-ttu-id="76ed1-127">Другие контейнеры, такие как Kubernetes, DC/OS и помощью Docker Swarm более развитым в Linux, но менее зрелой чем Service Fabric для приложений Windows и контейнеров Windows.</span><span class="sxs-lookup"><span data-stu-id="76ed1-127">Other containers, like Kubernetes, DC/OS, and Docker Swarm, are more mature in Linux, but less mature than Service Fabric for Windows-based applications and Windows Containers.</span></span>

<span data-ttu-id="76ed1-128">Для уменьшения сложности создания приложений по принципу микрослужбами является конечной целью Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="76ed1-128">The ultimate goal of Service Fabric is to reduce the complexities of building applications by using a microservices approach.</span></span> <span data-ttu-id="76ed1-129">Со временем необходимо микрослужбами для определенных типов приложений, чтобы избежать дорогостоящих переделки проекта.</span><span class="sxs-lookup"><span data-stu-id="76ed1-129">You eventually want a microservices for certain types of applications to avoid costly redesigns.</span></span> <span data-ttu-id="76ed1-130">Можно приступить к работе, масштабирование, при необходимости, устаревание служб, добавлять новые службы и развивать приложения с использованием клиента.</span><span class="sxs-lookup"><span data-stu-id="76ed1-130">You can start small, scale when needed, deprecate services, add new services, and evolve your application with customer use.</span></span> <span data-ttu-id="76ed1-131">Существует много других проблем, которые еще решаемой вносить микрослужбами более доступным для большинства разработчиков.</span><span class="sxs-lookup"><span data-stu-id="76ed1-131">There are many other problems that are yet to be solved to make microservices more approachable for most developers.</span></span> <span data-ttu-id="76ed1-132">Если в настоящее время просто поднимая и сдвиг приложения с контейнерами Windows, но вы собираетесь Добавление микрослужбами основании контейнеры в будущем, это место sweet Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="76ed1-132">If you currently are just lifting and shifting an application with Windows Containers, but you are thinking about adding microservices based on containers in the future, that is the Service Fabric sweet spot.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="76ed1-133">[Назад](when-to-deploy-windows-containers-to-azure-vms-iaas-cloud.md)
[Вперед](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)</span><span class="sxs-lookup"><span data-stu-id="76ed1-133">[Previous](when-to-deploy-windows-containers-to-azure-vms-iaas-cloud.md)
[Next](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)</span></span>