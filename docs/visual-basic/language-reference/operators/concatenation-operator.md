---
title: '&amp; Operator (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.&
helpviewer_keywords:
- And (&) operator
- ampersand operator (&)
- '& operator'
- concatenation operators [Visual Basic], syntax
- strings [Visual Basic], concatenating
ms.assetid: fefc3d00-cbf1-475c-8c5e-6fb213b3f85a
ms.openlocfilehash: 2237da5d64ada6817d3a9a88b04b76f573bd76c0
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2019
ms.locfileid: "56976516"
---
# <a name="amp-operator-visual-basic"></a>&amp; Operator (Visual Basic)
Приводит к возникновению ошибки объединения строк из двух выражений.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
result = expression1 & expression2  
```  
  
## <a name="parts"></a>Части  
 `result`  
 Обязательный. Любой `String` или `Object` переменной.  
  
 `expression1`  
 Обязательный. Любое выражение с типом данных, который расширяется до `String`.  
  
 `expression2`  
 Обязательный. Любое выражение с типом данных, который расширяется до `String`.  
  
## <a name="remarks"></a>Примечания  
 Если тип данных `expression1` или `expression2` не `String` , но можно расширить до `String`, он преобразуется в `String`. Если один из типов данных не расширяется до `String`, компилятор выдает ошибку.  
  
 Тип данных `result` является `String`. Если один или оба выражения [ничего не](../../../visual-basic/language-reference/nothing.md) или иметь значение <xref:System.DBNull.Value?displayProperty=nameWithType>, они обрабатываются как строки со значением «».  
  
> [!NOTE]
>  `&` Оператор может быть *перегружены*, что означает, что класс или структура может переопределить его поведение, если операнд имеет тип этого класса или структуры. Если ваш код использует этот оператор для такого класса или структуры, убедитесь, что его переопределенное. Для получения дополнительной информации см. [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
> [!NOTE]
>  Символ амперсанда (&) может также использоваться для определения переменных, как тип `Long`. Дополнительные сведения см. в разделе [символы типа](../../../visual-basic/programming-guide/language-features/data-types/type-characters.md).  
  
## <a name="example"></a>Пример  
 В этом примере используется `&` оператор для принудительного объединения строк. Результатом является строковое значение, представляющее объединение двух строковых операндов.  
  
 [!code-vb[VbVbalrOperators#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#2)]  
  
## <a name="see-also"></a>См. также
- [Оператор &=](../../../visual-basic/language-reference/operators/and-assignment-operator.md)
- [Операторы объединения](../../../visual-basic/language-reference/operators/concatenation-operators.md)
- [Порядок применения операторов в Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Список операторов, сгруппированных по функциональному назначению](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Операторы объединения в Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/concatenation-operators.md)
