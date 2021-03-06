---
title: <paramref> — руководство по программированию на C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- paramref
- <paramref>
helpviewer_keywords:
- <paramref> C# XML tag
- paramref C# XML tag
ms.assetid: 756c24c1-f591-40e8-a838-559761539b0b
ms.openlocfilehash: 9612fb61151953e0d3b70a4803aafeb571aec7dd
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "57477948"
---
# <a name="paramref-c-programming-guide"></a>\<paramref> (руководство по программированию на C#)
## <a name="syntax"></a>Синтаксис  
  
```xml  
<paramref name="name"/>  
```  
  
## <a name="parameters"></a>Параметры  
 `name`  
 Имя параметра, на который указывается ссылка. Имя заключается в двойные кавычки (" ").  
  
## <a name="remarks"></a>Примечания  
 Тег \<paramref> позволяет указать, что слово в комментариях к коду, например в блоке \<summary> или \<remarks>, ссылается на параметр. В XML-файл такое слово может выделяться особым образом, например курсивом или полужирным шрифтом.  
  
 Чтобы обработать и сохранить комментарии документации в файл, при компиляции необходимо использовать параметр [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md).  
  
## <a name="example"></a>Пример  
 [!code-csharp[csProgGuideDocComments#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDocComments/CS/DocComments.cs#7)]  
  
## <a name="see-also"></a>См. также

- [Руководство по программированию на C#](../../../csharp/programming-guide/index.md)
- [Рекомендуемые теги для комментариев документации](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
