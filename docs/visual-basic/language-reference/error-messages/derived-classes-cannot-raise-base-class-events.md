---
title: Производные классы не могут вызывать события базового класса
ms.date: 07/20/2015
f1_keywords:
- vbc30029
- bc30029
helpviewer_keywords:
- BC30029
ms.assetid: 63afa1c6-2f93-4512-a2f0-372455979771
ms.openlocfilehash: 3cb61a40e4522695b876d85f67dac1a109d3c3e0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54595868"
---
# <a name="derived-classes-cannot-raise-base-class-events"></a>Производные классы не могут вызывать события базового класса
Событие может вызываться только из области объявления, в котором она объявлена. Таким образом класс не может вызвать событие из другого класса, хотя бы один из которого он является производным.  
  
 **Идентификатор ошибки:** BC30029  
  
## <a name="to-correct-this-error"></a>Исправление ошибки  
  
-   Переместить `Event` инструкции или `RaiseEvent` инструкции, поэтому они находятся в том же классе.  
  
## <a name="see-also"></a>См. также
- [Оператор Event](../../../visual-basic/language-reference/statements/event-statement.md)
- [Оператор RaiseEvent](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
