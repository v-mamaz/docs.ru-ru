---
title: Практическое руководство. Преобразование привязанных данных
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- converting [WPF], bound data
- data binding [WPF], converting bound data
- binding data [WPF], converting bound data
ms.assetid: b00aaa19-c6df-4c3b-a9fd-88a0b488df2b
ms.openlocfilehash: c98f8e4e5c837e6fbbe836a9eb2f228d2d689542
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57352300"
---
# <a name="how-to-convert-bound-data"></a>Практическое руководство. Преобразование привязанных данных
В этом примере показано, как применить преобразования к данным, который используется в привязках.  
  
 Чтобы преобразовать данные во время привязки, необходимо создать класс, реализующий <xref:System.Windows.Data.IValueConverter> интерфейс, который включает в себя <xref:System.Windows.Data.IValueConverter.Convert%2A> и <xref:System.Windows.Data.IValueConverter.ConvertBack%2A> методы.  
  
## <a name="example"></a>Пример  
 В следующем примере показана реализация преобразователя, преобразующий значение даты, переданный так, чтобы отобразить только года, месяца и дня. При реализации <xref:System.Windows.Data.IValueConverter> интерфейс, он является хорошей практикой для оформления для реализации с <xref:System.Windows.Data.ValueConversionAttribute> для указания того, для разработки средств типы данных, участвующие в преобразовании, как показано в следующем примере:  
  
 [!code-csharp[DataBindingLab#18](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/DateConverter.cs#18)]
 [!code-vb[DataBindingLab#18](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataBindingLab/VisualBasic/DateConverter.vb#18)]  
  
 После создания преобразователь, его можно добавить как ресурс в вашей [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] файл. В следующем примере *src* соответствует пространству имен, в котором *DateConverter* определен.  
  
 [!code-xaml[DataBindingLab#15](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/DataBindingLabApp.xaml#15)]  
  
 Наконец можно использовать преобразователь в привязке, используя следующий синтаксис. В следующем примере текстовое содержимое <xref:System.Windows.Controls.TextBlock> привязан к *StartDate*, который является свойством из внешнего источника данных.  
  
 [!code-xaml[DataBindingLab#17](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/DataBindingLabApp.xaml#17)]  
  
 Ресурсы стиля, указанные в приведенном выше примере определяются в разделе ресурсов, не приведенные в этом разделе.  
  
## <a name="see-also"></a>См. также
- [Реализация проверки привязки](how-to-implement-binding-validation.md)
- [Общие сведения о привязке данных](data-binding-overview.md)
- [Разделы практического руководства](data-binding-how-to-topics.md)
