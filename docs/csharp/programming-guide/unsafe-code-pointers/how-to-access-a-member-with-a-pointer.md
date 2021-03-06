---
title: Руководство по программированию на C#. Доступ к элементу с использованием указателя
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], member access
ms.assetid: 1e998498-8c85-4a78-8ce2-4d8c20f08342
ms.openlocfilehash: 9762b9e2487c30b81b7ef6ae22827b64e3cb02e2
ms.sourcegitcommit: 41c0637e894fbcd0713d46d6ef1866f08dc321a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/01/2019
ms.locfileid: "57200355"
---
# <a name="how-to-access-a-member-with-a-pointer-c-programming-guide"></a>Практическое руководство. Доступ к члену с использованием указателя (Руководство по программированию в C#)
Чтобы получить доступ к члену или структуре, которые объявлены в небезопасном контексте, можно использовать оператор доступа к члену, как показано в следующем примере, где `p` — это указатель на [структуру](../../../csharp/language-reference/keywords/struct.md), содержащую член `x`.  
  
```  
CoOrds* p = &home;  
p -> x = 25; //member access operator ->  
```  
  
## <a name="example"></a>Пример  
 В этом примере объявляется [структура](../../../csharp/language-reference/keywords/struct.md), `CoOrds`, содержащая координаты `x` и `y`, а также создается ее экземпляр. С помощью оператора доступа к члену `->` и указателя на экземпляр `home` присваиваются значения `x` и `y`.  
  
> [!NOTE]
>  Обратите внимание, что выражение `p->x` эквивалентно выражению `(*p).x` и с помощью любого из них можно получить тот же результат.  
  
 [!code-csharp[csProgGuidePointers#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers2.cs#9)]  
  
 [!code-csharp[csProgGuidePointers#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers.cs#10)]  
  
## <a name="see-also"></a>См. также

- [Руководство по программированию на C#](../../../csharp/programming-guide/index.md)
- [Выражения указателей](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)
- [Типы указателей](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [Типы](../../../csharp/language-reference/keywords/types.md)
- [unsafe](../../../csharp/language-reference/keywords/unsafe.md)
- [Оператор fixed](../../../csharp/language-reference/keywords/fixed-statement.md)
- [stackalloc](../../../csharp/language-reference/keywords/stackalloc.md)
