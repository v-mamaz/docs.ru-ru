---
title: Практическое руководство. Рисование линий с наконечниками
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drawing [Windows Forms], lines
- lines [Windows Forms], drawing
- pens [Windows Forms], drawing lines
- drawing lines [Windows Forms], line caps
ms.assetid: eb68c3e1-c400-4886-8a04-76978a429cb6
ms.openlocfilehash: 7ebb49ad5e1262dcb71dcd31c9073dfe52c49789
ms.sourcegitcommit: 3630c2515809e6f4b7dbb697a3354efec105a5cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2019
ms.locfileid: "58409865"
---
# <a name="how-to-draw-a-line-with-line-caps"></a>Практическое руководство. Рисование линий с наконечниками
Можно нарисовать начала и конца строки в одну из нескольких фигур, называемых наконечниками. [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] поддерживает несколько отрезков, например циклический, квадрат, ромб и стрелки с наконечником.  
  
## <a name="example"></a>Пример  
 Можно указать отрезков в начале строки (начала штриха), в конец строки (конечного элемента) или дефисы пунктирной линии (штриховой наконечник).  
  
 В следующем примере рисуется линию со стрелкой на одном конце и кружком на другом конце. На рисунке показаны результирующие строки.  
  
 ![Рисунок, показывающий линий с кружком.](./media/how-to-draw-a-line-with-line-caps/line-cap-arrowhead-example.gif)  
  
 [!code-csharp[System.Drawing.UsingAPen#71](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#71)]
 [!code-vb[System.Drawing.UsingAPen#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#71)]  
  
## <a name="compiling-the-code"></a>Компиляция кода  
  
-   Создайте форму Windows и обработки формы <xref:System.Windows.Forms.Control.Paint> событий. Вставьте код в примере <xref:System.Windows.Forms.Control.Paint> обработчик событий передачи `e` как <xref:System.Windows.Forms.PaintEventArgs>.  
  
## <a name="see-also"></a>См. также
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- <xref:System.Drawing.Drawing2D.LineCap?displayProperty=nameWithType>
- [Объекты Graphics и Drawing в Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Рисование линий и фигур с помощью пера](using-a-pen-to-draw-lines-and-shapes.md)
