---
title: Нахождение элемента автоматизации пользовательского интерфейса для элемента списка
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- list items, finding elements for
- elements, finding for list items
- UI Automation, finding elements for List items
ms.assetid: c326ad2b-2144-4f64-ae4c-d850c74f95c5
ms.openlocfilehash: 4cc4c976f8e9eb7f1779139f8266e22477d269e4
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2019
ms.locfileid: "57673773"
---
# <a name="find-a-ui-automation-element-for-a-list-item"></a>Нахождение элемента автоматизации пользовательского интерфейса для элемента списка
> [!NOTE]
>  Эта документация предназначена для разработчиков .NET Framework, желающих использовать управляемые классы [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] , заданные в пространстве имен <xref:System.Windows.Automation> . Для получения последних сведений о [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], см. в разделе [API автоматизации Windows: Модели автоматизации пользовательского интерфейса](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 В этом разделе показано, как получить <xref:System.Windows.Automation.AutomationElement> для элемента в списке, если известен индекс элемента.  
  
## <a name="example"></a>Пример  
 В следующем примере показано два способа получения указанного элемента из списка, с помощью <xref:System.Windows.Automation.TreeWalker> и другой, используя <xref:System.Windows.Automation.AutomationElement.FindAll%2A>.  
  
 Во-первых, как правило, быстрее для [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] элементов управления, а второй имеет большее ускорение для элементов управления Windows Presentation Foundation (WPF).  
  
 [!code-csharp[UIAClient_snip#184](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClient_snip/CSharp/ClientForm.cs#184)]
 [!code-vb[UIAClient_snip#184](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClient_snip/VisualBasic/ClientForm.vb#184)]  
  
## <a name="see-also"></a>См. также
- [Получение элементов модели автоматизации пользовательского интерфейса](../../../docs/framework/ui-automation/obtaining-ui-automation-elements.md)
