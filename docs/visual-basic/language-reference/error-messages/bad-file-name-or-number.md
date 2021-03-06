---
title: Недопустимое имя файла или номер
ms.date: 07/20/2015
f1_keywords:
- vbrID52
ms.assetid: d0e96aea-7621-48f6-a78b-5d37d18aaa4e
ms.openlocfilehash: c57f431350d4f63507ee7374616b62ca32151c86
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54639410"
---
# <a name="bad-file-name-or-number"></a>Недопустимое имя файла или номер
Произошла ошибка при попытке доступа к указанному файлу. Среди возможных причин этой ошибки:  
  
-   Оператор ссылается на файл с именем файла или номер, который не был указан в `FileOpen` инструкции или был указан в `FileOpen` инструкции однако впоследствии был закрыт.  
  
-   Инструкция ссылается на файл с номером, который находится за пределами диапазона номеров файлов.  
  
-   Инструкция ссылается на имя файла или число, которое является недопустимым.  
  
## <a name="to-correct-this-error"></a>Исправление ошибки  
  
1.  Убедитесь, что имя файла указано в `FileOpen` инструкции. Обратите внимание, что при вызове `FileClose` инструкции без аргументов, могут случайно закрыты все открытые файлы.  
  
2.  Если ваш код создает номера файлов алгоритмически, убедитесь, что значения действительны.  
  
3.  Проверьте имена файлов, чтобы убедиться в том, что она соответствует соглашениям операционной системы.  
  
## <a name="see-also"></a>См. также
- <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>
- [Соглашения об именах Visual Basic](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)
