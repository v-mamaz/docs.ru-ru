---
title: Поддержка наследования
ms.date: 03/30/2017
ms.assetid: 19bb2794-b4e7-402e-8307-1d1517381a08
ms.openlocfilehash: 791cc68ce89ad8e56b8feeebe6bf84434c3e89c6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54692682"
---
# <a name="inheritance-support"></a>Поддержка наследования
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] поддерживает *однотабличное сопоставление*. Другими словами, в одной таблице базы данных хранится полная иерархия наследования. Таблица содержит плоское объединение всех возможных столбцов данных для всей иерархии. (Объединение является результатом сочетания двух таблиц в одной, в которой имеются строки любой из исходных таблиц.) Каждая строка в столбцах содержит значения NULL, которые не применяются к типу экземпляра, представленного строкой.  
  
 Стратегия однотабличного сопоставления представляет собой простейшее представление наследования и обеспечивает высокую производительность для многих различных категорий запросов.  
  
 Чтобы реализовать данное сопоставление в [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], в корневом классе иерархии наследования необходимо указать атрибуты и свойства атрибутов. Дополнительные сведения см. в разделе [Как Сопоставление иерархий наследования](../../../../../../docs/framework/data/adonet/sql/linq/how-to-map-inheritance-hierarchies.md).  
  
 Разработчики, использующие Visual Studio можно также использовать [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] сопоставить иерархии наследования.  
  
## <a name="see-also"></a>См. также
- [Основные сведения](../../../../../../docs/framework/data/adonet/sql/linq/background-information.md)
