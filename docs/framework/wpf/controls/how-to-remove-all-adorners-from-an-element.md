---
title: Практическое руководство. Удаление всех декоративных элементов из элемента
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], removing
ms.assetid: fe5303a3-b76e-4643-aafb-51419032b47b
ms.openlocfilehash: 6b2b1832898a847f54f11cca26ecd50dbd7285ff
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57374171"
---
# <a name="how-to-remove-all-adorners-from-an-element"></a>Практическое руководство. Удаление всех декоративных элементов из элемента
В этом примере показано, как программным способом удаление всех декоративных элементов из указанного <xref:System.Windows.UIElement>.  
  
## <a name="example"></a>Пример  
 Этот подробный пример кода удаляет всех графических элементов в массиве декоративных элементов, возвращенных <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.  В этом примере происходит с графические <xref:System.Windows.UIElement> с именем *myTextBox*.  Если этот элемент указан в вызове <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> нет графических объектов, `null` возвращается.  Этот код явно проверяет пустой массив и лучше всего подходит для приложений, где должен быть относительно распространенную пустой массив.  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersLong](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornerslong)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersLong](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornerslong)]  
  
## <a name="example"></a>Пример  
 Данный сжатый пример кода функционально эквивалентен подробному примеру, приведенному выше. Этот код явно не проверяет пустой массив, так что вполне возможно, <xref:System.NullReferenceException> может быть вызвано исключение.  Этот код лучше всего подходит для приложений, где ожидается пустой массив довольно редки.  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersShort](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornersshort)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersShort](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornersshort)]  
  
## <a name="see-also"></a>См. также
- [Общие сведения о декоративных элементах](adorners-overview.md)
