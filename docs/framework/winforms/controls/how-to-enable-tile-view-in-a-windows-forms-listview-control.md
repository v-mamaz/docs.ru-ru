---
title: Практическое руководство. Включить мозаичное представление в элементе управления ListView формы Windows
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tile view feature
- tiling
- Windows Forms, controls
- ListView control [Windows Forms], tile view
ms.assetid: c20e67a3-2d94-413d-9fcf-ecbd0fe251da
ms.openlocfilehash: ad0a925601d3cfaebcd21a2082e3d208d82151bc
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2019
ms.locfileid: "57722897"
---
# <a name="how-to-enable-tile-view-in-a-windows-forms-listview-control"></a>Практическое руководство. Включить мозаичное представление в элементе управления ListView формы Windows
Функция мозаичного представления элемента управления <xref:System.Windows.Forms.ListView> обеспечивает визуальный баланс между графическими и текстовыми представлениями информации. Текстовые данные, отображаемые для мозаичного представления элемента совпадают с данными о столбцах, определенных для подробного представления. Мозаичное представление работает в сочетании с возможностями группирования или вставки метки элемента управления <xref:System.Windows.Forms.ListView>.  
  
 Мозаичное представление использует значок размером 32 x 32 пикселя и несколько строк текста, как показано на следующих рисунках.  
  
 ![Мозаичное представление в элементе управления ListView](./media/how-to-enable-tile-view-in-a-windows-forms-listview-control/tile-view-in-listview-control.gif "плитки, значки и текст")  
 
 Чтобы включить мозаичное представление, присвойте свойству <xref:System.Windows.Forms.ListView.View%2A> значение <xref:System.Windows.Forms.View.Tile>. Размер элементов мозаики можно настроить, задав свойство <xref:System.Windows.Forms.ListView.TileSize%2A> и количество отображаемых строк текста в плитке путем настройки коллекции <xref:System.Windows.Forms.ListView.Columns%2A>.  
  
> [!NOTE]
>  Функция мозаичного представления доступна только в [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)], когда приложение вызывает метод <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType>. В предыдущих версиях операционных систем код, связанный с мозаичным представлением, не оказывает никакого влияния, элемент управления <xref:System.Windows.Forms.ListView> отображается в представлении крупных значков. Для получения дополнительной информации см. <xref:System.Windows.Forms.ListView.View%2A?displayProperty=nameWithType>.  
  
### <a name="to-set-tile-view-programmatically"></a>Выбор мозаичного представления программными средствами  
  
1.  Используйте перечисление <xref:System.Windows.Forms.View> элемента управления <xref:System.Windows.Forms.ListView>.  
  
    ```vb  
    ListView1.View = View.Tile  
    ```  
  
    ```csharp  
    listView1.View = View.Tile;  
    ```  
  
## <a name="example"></a>Пример  
 В завершенном примере кода ниже показано мозаичное представление с плиткой, в которой отображаются три строки текста. Размер мозаики был подобран для предотвращения переноса строк.  
  
 [!code-cpp[System.Windows.Forms.ListView.Tiling#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Tiling/CPP/listviewtilingexample.cpp#1)]
 [!code-csharp[System.Windows.Forms.ListView.Tiling#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Tiling/CS/listviewtilingexample.cs#1)]
 [!code-vb[System.Windows.Forms.ListView.Tiling#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListView.Tiling/VB/listviewtilingexample.vb#1)]  
  
## <a name="compiling-the-code"></a>Компиляция кода  
 Для этого примера требуются:  
  
-   ссылки на сборки System и System.Windows.Forms.  
  
-   файл значка с именем book.ico в том же каталоге, что и исполняемый файл.  
  
 Сведения о выполнении сборки этого примера из командной строки для Visual Basic или Visual C#, см. в разделе [построение из командной строки](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) или [командной строки создания с помощью csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Можно также сборке этого примера в Visual Studio путем вставки кода в новый проект.  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListView.TileSize%2A>
- [Элемент управления ListView](listview-control-windows-forms.md)
- [Общие сведения об элементе управления ListView](listview-control-overview-windows-forms.md)
