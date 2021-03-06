---
title: Protected Friend (Visual Basic)
ms.date: 05/10/2018
helpviewer_keywords:
- Protected Friend keyword [Visual Basic]
- Protected Friend keyword [Visual Basic], syntax
ms.openlocfilehash: 1858411e5543448e6d822c97b6e5c18da4a6c11e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54639605"
---
# <a name="protected-friend-visual-basic"></a>Protected Friend (Visual Basic)

Комбинация ключевых слов `Protected Friend` является модификатором доступа к члену. Он предоставляет оба [Friend](friend.md) доступа и [Protected](protected.md) доступ к объявленным элементам, поэтому они доступны в любом месте той же сборки, из собственного класса, а также из производных классов. Можно указать `Protected Friend` только для членов классов; нельзя применить `Protected Friend` к членам структуры, так как структуры не может быть унаследован.

> [!NOTE]
> В Visual Studio, выбрав Справка F1 на `protected friend` предоставляет справку для любого [защищенные](protected.md) или [friend](friend.md). Интегрированная среда разработки выбирает один токен в курсор, а не составное слово.

## <a name="rules"></a>Правила

- **Контекст объявления.** Можно использовать `Protected Friend` только на уровне класса. Это означает, что контекст объявления для `Protected` элемент должен быть классом и не может быть исходный файл, пространство имен, интерфейс, модуль, структуру или процедуры. 


## <a name="see-also"></a>См. также

- [Public](../../../visual-basic/language-reference/modifiers/public.md)
- [Protected](../../../visual-basic/language-reference/modifiers/protected.md)
- [Friend](friend.md)
- [Закрытые](../../../visual-basic/language-reference/modifiers/private.md)
- [Private Protected](./private-protected.md)
- [Уровни доступа в Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [Процедуры](../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [Структуры](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [Объекты и классы](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
