---
title: N-уровневое использование LINQ to SQL с ASP.NET
ms.date: 03/30/2017
ms.assetid: f6cc863a-d6a6-4281-ba8b-197c01cf6c6f
ms.openlocfilehash: b85392408d2fa62c481381c5028e228f280a1dc8
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56093656"
---
# <a name="linq-to-sql-n-tier-with-aspnet"></a>N-уровневое использование LINQ to SQL с ASP.NET
В приложениях [!INCLUDE[vstecasp](../../../../../../includes/vstecasp-md.md)] , использующих [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], применяется серверный веб-элемент управления <xref:System.Web.UI.WebControls.LinqDataSource> . Этот элемент управления обрабатывает большую часть логики, необходимой для выполнения запросов в [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], передает данные в браузер, извлекает их и отправляет классу [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.DataContext> , который затем обновляет базу данных. Чтобы элемент управления полностью обрабатывал передачу данных между [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] и браузером, достаточно настроить его в разметке. Поскольку элемент управления обрабатывает взаимодействия с уровнем представления, а [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] обрабатывает взаимодействие с уровнем данных, то в многоуровневых приложениях [!INCLUDE[vstecasp](../../../../../../includes/vstecasp-md.md)] особое внимание следует уделять написанию пользовательской бизнес-логики.  
  
 Дополнительные сведения о `LINQDataSource`, см. в разделе [Обзор элемента управления веб-сервера LinqDataSource](https://docs.microsoft.com/previous-versions/aspnet/bb547113(v=vs.100)).  
  
## <a name="see-also"></a>См. также
- [N-уровневые и удаленные приложения и LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/n-tier-and-remote-applications-with-linq-to-sql.md)
