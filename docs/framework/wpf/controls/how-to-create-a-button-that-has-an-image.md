---
title: Практическое руководство. Создание кнопки, содержащей изображение
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Button controls [WPF], creating
ms.assetid: 607a193c-4098-4dd8-8dc0-51256cec2020
ms.openlocfilehash: fe9f35a6f83c5a839823d94c4d3c55e01b192fb1
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57352039"
---
# <a name="how-to-create-a-button-that-has-an-image"></a>Практическое руководство. Создание кнопки, содержащей изображение
В этом примере показано, как включить изображение в <xref:System.Windows.Controls.Button>.  
  
## <a name="example"></a>Пример  
 В следующем примере создается два <xref:System.Windows.Controls.Button> элементов управления. Один <xref:System.Windows.Controls.Button> содержит текст, а другой образ. Изображение находится в папке Data, которая является подпапкой папки проекта в примере. Когда пользователь щелкает <xref:System.Windows.Controls.Button> имеет изображения, фон и текст другого <xref:System.Windows.Controls.Button> изменить.  
  
 В этом примере создается <xref:System.Windows.Controls.Button> элементы управления с помощью разметки, но использует код для записи <xref:System.Windows.Controls.Primitives.ButtonBase.Click> обработчики событий.  
  
 [!code-xaml[BtnColor#4](~/samples/snippets/csharp/VS_Snippets_Wpf/BtnColor/CSharp/Pane1.xaml#4)]  
  
 [!code-csharp[BtnColor#6](~/samples/snippets/csharp/VS_Snippets_Wpf/BtnColor/CSharp/Pane1.xaml.cs#6)]
 [!code-vb[BtnColor#6](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BtnColor/VisualBasic/Pane1.xaml.vb#6)]  
  
## <a name="see-also"></a>См. также
- [Элементы управления](index.md)
- [Библиотека элементов управления](control-library.md)
