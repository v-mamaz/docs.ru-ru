---
title: Практическое руководство. Создание родительских MDI-форм
ms.date: 03/30/2017
helpviewer_keywords:
- parent forms
- MDI [Windows Forms], creating forms
ms.assetid: 12c71221-2377-4bb6-b10b-7b4b300fd462
ms.openlocfilehash: 5da7f1a53412cf30a5898fec096aaa01e3aa65d2
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2019
ms.locfileid: "57722988"
---
# <a name="how-to-create-mdi-parent-forms"></a>Практическое руководство. Создание родительских MDI-форм
> [!IMPORTANT]
>  В этом разделе используется элемент управления <xref:System.Windows.Forms.MainMenu>, который был заменен на элемент управления <xref:System.Windows.Forms.MenuStrip>. Элемент управления <xref:System.Windows.Forms.MainMenu> сохраняется для обеспечения обратной совместимости и использования в будущем.  Сведения о создании MDI родительской формы с помощью <xref:System.Windows.Forms.MenuStrip>, см. в разделе [как: Создание списка в окне интерфейса MDI с помощью MenuStrip](../controls/how-to-create-an-mdi-window-list-with-menustrip-windows-forms.md).  
  
 Базой для приложения многодокументного интерфейса (MDI) является родительская MDI-форма. Это форма, содержащая дочерние MDI-окна, которые являются вложенными окнами, когда пользователи взаимодействуют с MDI-приложением. Создание родительской MDI-формы представляет собой несложный процесс, как с помощью конструктора Windows Forms, так и на программном уровне.  
  
### <a name="to-create-an-mdi-parent-form-at-design-time"></a>Создание родительской MDI-формы во время разработки  
  
1.  Создайте проект приложения Windows.  
  
2.  В **свойства** окне <xref:System.Windows.Forms.Form.IsMdiContainer%2A> свойства **true**.  
  
     При этом форма назначается в качестве MDI-контейнера для дочерних окон.  
  
    > [!NOTE]
    >  При необходимости, при настройке свойств в окне **Свойства** для свойства `WindowState` также можно задать значение **Maximized**, так как управлять дочерними MDI-окнами проще, когда родительская форма развернута. Кроме того, следует помнить, что граница родительской MDI-формы будет окрашена в системный цвет (заданный на панели управления Windows), а не в черный цвет, заданный с помощью свойства <xref:System.Windows.Forms.Control.BackColor%2A?displayProperty=nameWithType>.  
  
3.  Перетащите элемент управления **MenuStrip** из **панели элементов** в форму. Создайте пункт меню верхнего уровня — для свойства **Text** задайте значение **&File**, пункты меню должны называться **&New** и **&Close**. Также создайте пункт меню верхнего уровня **&Window**.  
  
     Первое меню будет создавать и скрывать пункты меню во время выполнения, а второе меню будет отслеживать открытые дочерние MDI-окна. На этом этапе вы создали родительское MDI-окно.  
  
4.  Нажмите клавишу **F5** для запуска приложения. Сведения о создании дочерних MDI-окон, действующих в родительской MDI-формы, см. в разделе [как: Создание дочерних MDI-форм](how-to-create-mdi-child-forms.md).  
  
## <a name="see-also"></a>См. также
- [Приложения с интерфейсом MDI](multiple-document-interface-mdi-applications.md)
- [Практическое руководство. Создание дочерних MDI-форм](how-to-create-mdi-child-forms.md)
- [Практическое руководство. Определить активную дочернюю форму MDI](how-to-determine-the-active-mdi-child.md)
- [Практическое руководство. Отправки данных в активную дочернюю форму MDI](how-to-send-data-to-the-active-mdi-child.md)
- [Практическое руководство. Упорядочение дочерних форм MDI](how-to-arrange-mdi-child-forms.md)
