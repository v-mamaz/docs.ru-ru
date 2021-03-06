---
title: Практическое руководство. Добавление и удаление элементов меню с помощью компонента ContextMenu в Windows Forms
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- context menus [Windows Forms], removing items
- ContextMenu component [Windows Forms], adding items
- shortcut menus [Windows Forms], removing items
- shortcut menus [Windows Forms], examples
- context menus [Windows Forms], adding items
- shortcut menus [Windows Forms], adding items
- ContextMenu component [Windows Forms], removing items
- context menus [Windows Forms], examples
- examples [Windows Forms], context menus
ms.assetid: 426d1eaf-7fb8-4b0b-8a33-5e8721786ea4
ms.openlocfilehash: 8b63182bdb37e47a71bee2d22500263cd4889ac9
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2019
ms.locfileid: "57725068"
---
# <a name="how-to-add-and-remove-menu-items-with-the-windows-forms-contextmenu-component"></a>Практическое руководство. Добавление и удаление элементов меню с помощью компонента ContextMenu в Windows Forms
Объясняется, как добавлять и удалять элементы контекстного меню в Windows Forms.  
  
 Windows Forms <xref:System.Windows.Forms.ContextMenu> компонент предоставляет меню часто используемых команд, относящихся к выбранному объекту. Элементы добавляются в контекстное меню, добавив <xref:System.Windows.Forms.MenuItem> объектов <xref:System.Windows.Forms.Menu.MenuItems%2A> коллекции.  
  
 Элементы контекстного меню можно удалить без возможности восстановления; Тем не менее во время выполнения он может быть более подходящим для скрытия или отключение элементов.  
  
> [!IMPORTANT]
>  Несмотря на то что <xref:System.Windows.Forms.MenuStrip> и <xref:System.Windows.Forms.ContextMenuStrip> заменяют и расширяют функциональные возможности для <xref:System.Windows.Forms.MainMenu> и <xref:System.Windows.Forms.ContextMenu> элементы управления из предыдущих версий <xref:System.Windows.Forms.MainMenu> и <xref:System.Windows.Forms.ContextMenu> можно сохранить для обратной совместимости и использования в будущем, если выбран.  
  
### <a name="to-remove-items-from-a-shortcut-menu"></a>Чтобы удалить элементы из контекстного меню  
  
1.  Используйте <xref:System.Windows.Forms.Menu.MenuItemCollection.Remove%2A> или <xref:System.Windows.Forms.Menu.MenuItemCollection.RemoveAt%2A> метод <xref:System.Windows.Forms.Menu.MenuItems%2A> коллекцию <xref:System.Windows.Forms.ContextMenu> компонента для удаления определенного элемента меню.  
  
    ```vb  
    ' Removes the first item in the shortcut menu.  
    ContextMenu1.MenuItems.RemoveAt(0)  
    ' Removes a particular object from the shortcut menu.  
    ContextMenu1.MenuItems.Remove(mnuItemNew)  
    ```  
  
    ```csharp  
    // Removes the first item in the shortcut menu.  
    contextMenu1.MenuItems.RemoveAt(0);  
    // Removes a particular object from the shortcut menu.  
    contextMenu1.MenuItems.Remove(mnuItemNew);  
    ```  
  
    ```cpp  
    // Removes the first item in the shortcut menu.  
    contextMenu1->MenuItems->RemoveAt(0);  
    // Removes a particular object from the shortcut menu.  
    contextMenu1->MenuItems->Remove(mnuItemNew);  
    ```  
  
     - или -  
  
2.  Используйте `Clear` метод `MenuItems` коллекцию <xref:System.Windows.Forms.ContextMenu> компонента для удаления всех элементов в меню.  
  
    ```vb  
    ContextMenu1.MenuItems.Clear()  
    ```  
  
    ```csharp  
    contextMenu1.MenuItems.Clear();  
    ```  
  
    ```cpp  
    contextMenu1->MenuItems->Clear();  
    ```  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Forms.ContextMenu>
- [Компонент ContextMenu](contextmenu-component-windows-forms.md)
- [Общие сведения об элементе управления ContextMenu](contextmenu-component-overview-windows-forms.md)
