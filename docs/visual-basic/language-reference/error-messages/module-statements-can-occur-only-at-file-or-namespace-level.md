---
title: Операторы Module могут присутствовать только на уровне файлов или пространств имен
ms.date: 07/20/2015
f1_keywords:
- bc30617
- vbc30617
helpviewer_keywords:
- BC30617
ms.assetid: 5e9de8e5-d26b-4fb2-9e28-814413fe9cef
ms.openlocfilehash: 0820763cce9cc27f9a379ed5e766e0691a75f36b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271269"
---
# <a name="module-statements-can-occur-only-at-file-or-namespace-level"></a>Операторы Module могут присутствовать только на уровне файлов или пространств имен
`Module` операторы должны находиться в начале файла исходного кода сразу же после `Option` и `Imports` инструкции, глобальных атрибутов и деклараций пространств имен, но перед всеми объявлениями.  
  
 **Идентификатор ошибки:** BC30617  
  
## <a name="to-correct-this-error"></a>Исправление ошибки  
  
-   Переместите оператор `Module` в начало объявления пространства имен или исходного файла.  
  
## <a name="see-also"></a>См. также
- [Оператор Module](../../../visual-basic/language-reference/statements/module-statement.md)
