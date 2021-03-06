---
title: -warnaserror (параметры компилятора C#)
ms.date: 07/20/2015
f1_keywords:
- /warnaserror
helpviewer_keywords:
- /warnaserror compiler option [C#]
- -warnaserror compiler option [C#]
- warnaserror compiler option [C#]
ms.assetid: 04680ec3-08d6-4e2e-a274-38310e10e33c
ms.openlocfilehash: b208f6e4e768e400af203117d185944be285cb72
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54634614"
---
# <a name="-warnaserror-c-compiler-options"></a>-warnaserror (параметры компилятора C#)
Параметр **-warnaserror+** предписывает обрабатывать все предупреждения как ошибки  
  
## <a name="syntax"></a>Синтаксис  
  
```console  
-warnaserror[+ | -][:warning-list]  
```  
  
## <a name="remarks"></a>Примечания  
 Все сообщения, которые до этого получали статус предупреждений, будут возвращаться как ошибки, в результате чего процесс построения прерывается без создания выходных файлов.  
  
 По умолчанию действует параметр **-warnaserror-**, при котором наличие предупреждений не препятствует созданию выходного файла. Если задан параметр **-warnaserror** или эквивалентный ему **-warnaserror+**, все предупреждения обрабатываются как ошибки.  
  
 Если требуется обрабатывать как ошибки только конкретные предупреждения, укажите их номера через запятую.  
  
 Параметр [-warn](../../../csharp/language-reference/compiler-options/warn-compiler-option.md) позволяет указать уровень предупреждений, которые будет отображать компилятор. Параметр [-nowarn](../../../csharp/language-reference/compiler-options/nowarn-compiler-option.md) позволяет отключать определенные предупреждения.  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio  
  
1.  Откройте страницу **Свойства** проекта.  
  
2.  Щелкните страницу свойств **Сборка**.  
  
3.  Измените свойство **Обрабатывать предупреждения как ошибки**.  
  
 Сведения об установке этого параметра компилятора программными средствами см. в разделе <xref:VSLangProj80.CSharpProjectConfigurationProperties3.TreatWarningsAsErrors>.  
  
## <a name="example"></a>Пример  
 Компиляция файла `in.cs` без отображения предупреждений:  
  
```console  
csc -warnaserror in.cs  
csc -warnaserror:642,649,652 in.cs  
```  
  
## <a name="see-also"></a>См. также

- [Параметры компилятора C# ](../../../csharp/language-reference/compiler-options/index.md)
- [Управление свойствами проектов и решений](/visualstudio/ide/managing-project-and-solution-properties)
