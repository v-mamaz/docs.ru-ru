---
title: Переменная <variablename> используется до того, как ей присвоено значение
ms.date: 07/20/2015
f1_keywords:
- vbc42104
- BC42104
helpviewer_keywords:
- BC42104
ms.assetid: 6909aa0b-b4a1-46f5-a18c-ba3e565c1dd8
ms.openlocfilehash: 23201b89f44f6384ae9f75d941d264e8d59bef80
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2019
ms.locfileid: "55268838"
---
# <a name="variable-variablename-is-used-before-it-has-been-assigned-a-value"></a>Переменной "\<имя_переменной >" используется, прежде чем ей было назначено значение
Переменной "\<имя_переменной >" используется, прежде чем ей было назначено значение. Во время выполнения может возникнуть исключение "пустая ссылка".  
  
 Приложение имеет по крайней мере один возможный путь во всем коде, который считывает значение переменной, прежде чем к нему было назначено значение.  
  
 Если переменной никогда не назначалось значение, она содержит значение по умолчанию для своего типа данных. Для ссылочного типа данных значение по умолчанию — [Nothing](../../../visual-basic/language-reference/nothing.md). Чтение переменной ссылки, которая имеет значение `Nothing` , в некоторых случаях может привести к исключению <xref:System.NullReferenceException> .  
  
 По умолчанию данное сообщение является предупреждением. Дополнительные сведения о скрытии предупреждений или обработке предупреждений как ошибок см. в разделе [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **Идентификатор ошибки:** BC42104  
  
## <a name="to-correct-this-error"></a>Исправление ошибки  
  
-   Проверьте логику потока управления и убедитесь, что переменная имеет допустимое значение, прежде чем управление передается оператору, который считывает его.  
  
-   Для инициализации его как часть объявления является один из способов, чтобы гарантировать, что переменная всегда имеет допустимое значение. См. в разделе «Инициализация» в [оператор Dim](../../../visual-basic/language-reference/statements/dim-statement.md).  
  
## <a name="see-also"></a>См. также
- [Оператор Dim](../../../visual-basic/language-reference/statements/dim-statement.md)
- [Объявление переменных](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [Устранение неполадок, связанных с переменными](../../../visual-basic/programming-guide/language-features/variables/troubleshooting-variables.md)
