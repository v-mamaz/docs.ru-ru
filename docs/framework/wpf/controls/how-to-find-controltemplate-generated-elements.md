---
title: Практическое руководство. Найти, созданного шаблоном ControlTemplate
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ControlTemplates [WPF], finding elements
- finding ControlTemplate elements [WPF]
ms.assetid: d7b25447-ceff-4bb4-9be5-fd7c40ef00af
ms.openlocfilehash: 9a6609d70a6b863f16533aac81ffce4daf171bcf
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57364508"
---
# <a name="how-to-find-controltemplate-generated-elements"></a>Практическое руководство. Найти, созданного шаблоном ControlTemplate
В этом примере показано, как для поиска элементов, создаваемых <xref:System.Windows.Controls.ControlTemplate>.  
  
## <a name="example"></a>Пример  
 В следующем примере показано стиль, который создает простой <xref:System.Windows.Controls.ControlTemplate> для <xref:System.Windows.Controls.Button> класса:  
  
 [!code-xaml[FindGeneratedItems#CT](~/samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml#ct)]  
  
 Чтобы найти элемент в шаблоне, после применения шаблона, можно вызвать <xref:System.Windows.FrameworkTemplate.FindName%2A> метод <xref:System.Windows.Controls.Control.Template%2A>. В следующем примере создается окно сообщения, которое показывает фактическое значение ширины <xref:System.Windows.Controls.Grid> в шаблоне элемента управления:  
  
 [!code-csharp[FindGeneratedItems#CTFindElement](~/samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml.cs#ctfindelement)]
 [!code-vb[FindGeneratedItems#CTFindElement](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FindGeneratedItems/VisualBasic/Window1.xaml.vb#ctfindelement)]  
  
## <a name="see-also"></a>См. также
- [Поиск элементов, созданных с использованием шаблона DataTemplate](../data/how-to-find-datatemplate-generated-elements.md)
- [Стилизация и использование шаблонов](styling-and-templating.md)
- [Области видимости имен XAML в WPF](../advanced/wpf-xaml-namescopes.md)
- [Деревья в WPF](../advanced/trees-in-wpf.md)
