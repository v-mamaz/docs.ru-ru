---
title: Практическое руководство. Получение метрик шрифтов
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- fonts [Windows Forms], obtaining metrics
- font metrics [Windows Forms], obtaining
ms.assetid: ff7c0616-67f7-4fa2-84ee-b8d642f2b09b
ms.openlocfilehash: c1701b07958509e663f0ac651471e82a60120618
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2019
ms.locfileid: "57723378"
---
# <a name="how-to-obtain-font-metrics"></a>Практическое руководство. Получение метрик шрифтов
<xref:System.Drawing.FontFamily> Класс предоставляет следующие методы для получения различных метрик для определенного семейства/style сочетания:  
  
-   <xref:System.Drawing.FontFamily.GetEmHeight%2A>(FontStyle)  
  
-   <xref:System.Drawing.FontFamily.GetCellAscent%2A>(FontStyle)  
  
-   <xref:System.Drawing.FontFamily.GetCellDescent%2A>(FontStyle)  
  
-   <xref:System.Drawing.FontFamily.GetLineSpacing%2A>(FontStyle)  
  
 Между номерами, возвращаемыми этими методами, в единицах измерения конструктора, поэтому они не зависят от размера и единиц измерения конкретного <xref:System.Drawing.Font> объекта.  
  
 На следующем рисунке различные метрики.  
  
 ![Текст шрифтов](./media/fontstext7a.png "fontstext7A")  
  
## <a name="example"></a>Пример  
 В следующем примере отображается метрики для семейства шрифтов Arial обычного стиля. Код также создает <xref:System.Drawing.Font> объект (в зависимости от семейства шрифтов Arial) с размером 16 пикселей и отображаются метрики (в пикселях) для этой конкретной <xref:System.Drawing.Font> объекта.  
  
 Ниже показан результат выполнения примера кода.  
  
 ![Fonts Text](./media/csfontstext8.png "csFontsText8")  
  
 Обратите внимание, первые две строки выходных данных на предыдущем рисунке. <xref:System.Drawing.Font> Объект возвращает размер 16 и <xref:System.Drawing.FontFamily> объект возвращает em, равный 2048. Эти два числа (16 и 2048 бит) являются основой для преобразования между единицах измерения конструктора и единиц (в данном случае это пиксели) <xref:System.Drawing.Font> объекта.  
  
 Например можно преобразовать единицах измерения конструктора верхнего выносного элемента в пиксели следующим образом:  
  
 ![Fonts Text](./media/fontstext9.png "FontsText9")  
  
 Следующий код располагает текст по вертикали, задав <xref:System.Drawing.PointF.Y%2A> данными-членом <xref:System.Drawing.PointF> объекта. Координата по оси y будет увеличена путем `font.Height` для каждой новой строки текста. <xref:System.Drawing.Font.Height%2A> Свойство <xref:System.Drawing.Font> объект возвращает межстрочный интервал (в пикселях) для этой конкретной <xref:System.Drawing.Font> объекта. В данном случае возвращаемое значение <xref:System.Drawing.Font.Height%2A> равно 19. Обратите внимание на то, что это то же самое, как число (округленный в целое число), получаемому при преобразовании метрики межстрочного интервала в пикселях.  
  
 Обратите внимание на то, что (также называемый размер эм) не равен сумме Восхождение и спуск. Сумма размеров верхнего и спуск называется высота ячейки. Высота ячейки минус внутренней начальные равно высоту максимального пробела. Высота ячейки, а также внешнее межстрочное расстояние равно междустрочного интервала.  
  
 [!code-csharp[System.Drawing.FontsAndText#71](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#71)]
 [!code-vb[System.Drawing.FontsAndText#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#71)]  
  
## <a name="compiling-the-code"></a>Компиляция кода  
 Предыдущий пример кода предназначен для работы с Windows Forms и требует <xref:System.Windows.Forms.PaintEventArgs> `e`, который является параметром <xref:System.Windows.Forms.PaintEventHandler>.  
  
## <a name="see-also"></a>См. также
- [Объекты Graphics и Drawing в Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Работами со шрифтами и текстом](using-fonts-and-text.md)
