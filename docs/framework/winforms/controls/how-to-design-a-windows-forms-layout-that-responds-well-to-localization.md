---
title: Практическое руководство. Разработка макета формы Windows, с учетом будущей локализации
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms]
- application design [Windows Forms], localization
- Windows Forms, localization
- localization [Windows Forms], Windows Forms layout
ms.assetid: d13eff2d-701c-4b6e-8838-3885cbfb7223
ms.openlocfilehash: ff88d876ffc05c85c6d3c1011df776b814ed7aea
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2019
ms.locfileid: "57709724"
---
# <a name="how-to-design-a-windows-forms-layout-that-responds-well-to-localization"></a>Практическое руководство. Разработка макета формы Windows, с учетом будущей локализации
Создание готовых для локализации форм значительно ускоряет разработку продуктов для международных рынков. Элемент управления <xref:System.Windows.Forms.TableLayoutPanel> можно использовать для реализации макетов, которые поддерживают изменение размера элементов управления при изменении значений их свойств <xref:System.Windows.Forms.Control.Text%2A>.  
  
## <a name="example"></a>Пример  
 Эта форма показывает, как создать макет, который пропорционально корректируется при отображении строковых значений на других языках. Такой процесс перевода называется *локализацией*. Подробнее об этом см. в разделе [Локализация](../../../standard/globalization-localization/localization.md).  
  
 В Visual Studio предусмотрена расширенная поддержка данной задачи.  См. также [Пошаговое руководство: Создание структуры, сохраняющей пропорции при локализации](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/7k9fa71y(v=vs.100)).  
  
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/CS/localizableform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/VB/localizableform.vb#1)]  
  
## <a name="additional-resources"></a>Дополнительные ресурсы
1.  [Практическое руководство. Выравнивание и Растягивание элемента управления в элементе управления TableLayoutPanel](how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control.md)  
  
2.  [Пошаговое руководство: Упорядочение элементов управления в Windows Forms, с помощью элемента FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)  

3.  [Практическое руководство. Объединение строк и столбцов в элементе управления TableLayoutPanel](how-to-span-rows-and-columns-in-a-tablelayoutpanel-control.md)  
  
4.  [Практическое руководство. Изменение столбцов и строк в элементе управления TableLayoutPanel](how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control.md)  
  
5.  [Пошаговое руководство: Выполнение типичных задач с помощью смарт-тегов в Windows Forms элементы управления](performing-common-tasks-using-smart-tags-on-wf-controls.md)  
  
6.  [Пошаговое руководство: Упорядочение элементов управления в Windows Forms, с помощью элемента управления TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)  

7.  [Пошаговое руководство: Создание структуры Windows Forms элементов управления с помощью свойств Padding, Margins и свойство AutoSize](windows-forms-controls-padding-autosize.md)  
  
8.  [Практическое руководство. Поддержки локализации в Windows Forms, с помощью функции AutoSize и элемента управления TableLayoutPanel](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/1zkt8b33(v=vs.100))  
  
9. [Пошаговое руководство: Создание переменного размера Windows формы для ввода данных](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/991eahec(v=vs.100))  
  
## <a name="compiling-the-code"></a>Компиляция кода  
 Для этого примера требуются:  
  
-   ссылки на сборки System, System.Data, System.Drawing и System.Windows.Forms.  
  
 Сведения о выполнении сборки этого примера из командной строки для Visual Basic или Visual C#, см. в разделе [построение из командной строки](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) или [командной строки создания с помощью csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Можно также сборке этого примера в Visual Studio путем вставки кода в новый проект.  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Forms.TableLayoutPanel>
- <xref:System.Windows.Forms.FlowLayoutPanel>
- [Локализация](../../../standard/globalization-localization/localization.md)
