---
title: Практическое руководство. Применение шаблона PropertyNameChanged
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], property changes (using code)
- data binding [Windows Forms], custom controls
- PropertyNameChanged pattern [Windows Forms], applying
ms.assetid: aa47ddf6-5223-40c4-833f-a78992194836
ms.openlocfilehash: 889a7f5f7a84db378acaa88b717b6011f1a3dfdc
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2019
ms.locfileid: "57703482"
---
# <a name="how-to-apply-the-propertynamechanged-pattern"></a>Практическое руководство. Применение шаблона PropertyNameChanged
В следующем примере кода демонстрируется применение *PropertyName*Changed шаблон для пользовательского элемента управления. Применяйте этот шаблон при реализации пользовательских элементов управления, используемых с ними механизм привязки данных Windows Forms.  
  
## <a name="example"></a>Пример  
 [!code-csharp[System.Windows.Forms.ChangeNotification#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ChangeNotification/CS/Form1.cs#3)]
 [!code-vb[System.Windows.Forms.ChangeNotification#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ChangeNotification/VB/Form1.vb#3)]  
  
## <a name="compiling-the-code"></a>Компиляция кода  
 Для компиляции в предыдущем примере кода:  
  
-   Вставьте код в пустой файл кода. Необходимо использовать пользовательский элемент управления на форму Windows, которая содержит `Main` метод.  
  
## <a name="see-also"></a>См. также
- [Практическое руководство. Реализация интерфейса INotifyPropertyChanged](how-to-implement-the-inotifypropertychanged-interface.md)
- [Уведомления об изменениях в привязке данных Windows Forms](change-notification-in-windows-forms-data-binding.md)
- [Привязка данных Windows Forms](windows-forms-data-binding.md)
