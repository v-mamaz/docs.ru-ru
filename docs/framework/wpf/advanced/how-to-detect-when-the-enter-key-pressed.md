---
title: Практическое руководство. Обнаружить, когда нажата клавиша ВВОД
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Enter key [WPF], detecting
- keys [WPF], Enter
ms.assetid: a66f39d2-ef4a-43a5-b454-a4ea0fe88655
ms.openlocfilehash: 1796127d33087a3fd4504d03f175f8afe5323630
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57351870"
---
# <a name="how-to-detect-when-the-enter-key-pressed"></a>Практическое руководство. Обнаружить, когда нажата клавиша ВВОД
В этом примере показано, как определить, когда <xref:System.Windows.Input.Key.Enter> клавиши на клавиатуре.  
  
 В этом примере состоит из [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] файл и файл с выделенным кодом.  
  
## <a name="example"></a>Пример  
 Когда пользователь нажимает <xref:System.Windows.Input.Key.Enter> в <xref:System.Windows.Controls.TextBox>, входные данные в текстовом поле отображается в другой области [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)].  
  
 Следующие [!INCLUDE[TLA2#tla_titlexaml](../../../../includes/tla2sharptla-titlexaml-md.md)] создает пользовательский интерфейс, который состоит из <xref:System.Windows.Controls.StackPanel>, <xref:System.Windows.Controls.TextBlock>и <xref:System.Windows.Controls.TextBox>.  
  
 [!code-xaml[keydown#KeyDownUI](~/samples/snippets/csharp/VS_Snippets_Wpf/KeyDown/CSharp/Window1.xaml#keydownui)]  
  
 Следующий код создает <xref:System.Windows.UIElement.KeyDown> обработчик событий.  Если нажата клавиша является <xref:System.Windows.Input.Key.Enter> ключа, выводится сообщение в <xref:System.Windows.Controls.TextBlock>.  
  
 [!code-csharp[keydown#KeyDownSample](~/samples/snippets/csharp/VS_Snippets_Wpf/KeyDown/CSharp/Window1.xaml.cs#keydownsample)]
 [!code-vb[keydown#KeyDownSample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/KeyDown/VisualBasic/Window1.xaml.vb#keydownsample)]  
  
## <a name="see-also"></a>См. также
- [Общие сведения о входных данных](input-overview.md)
- [Общие сведения о перенаправленных событиях](routed-events-overview.md)
