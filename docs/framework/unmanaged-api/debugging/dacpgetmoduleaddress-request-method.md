---
title: Метод DacpGetModuleAddress::Request
ms.date: 01/16/2019
api.name:
- DacpGetModuleAddress::Request Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpGetModuleAddress::Request Method
helpviewer.keywords:
- DacpGetModuleAddress::Request Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 3cc3b0258381b10c27dd58bee66dbb6b2cf5b2c8
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57351090"
---
# <a name="dacpgetmoduleaddressrequest-method"></a>Метод DacpGetModuleAddress::Request

Выполняет запрос для заполнения структуры из структуры данной среды выполнения.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Синтаксис

```
HRESULT Request(
    [in] IXCLRDataModule* pDataModule
);
```

## <a name="parameters"></a>Параметры

`pDataModule`\
[in] Указатель на модуль начальное значение данных.

## <a name="remarks"></a>Примечания

Эта структура находится внутри среды выполнения и не предоставляется через любой заголовков или библиотек. Чтобы использовать его, проще всего имитируют реализации:

- Возвращает значение, полученное от вызова `Request` метод `IXCLRDataModule*` параметра со следующими параметрами: `((uint32) 0xf0000000, 0, 0, (uint32) sizeof(*this), (uint8*) this)`


## <a name="requirements"></a>Требования

**Платформы:** См. раздел [Требования к системе](../../../../docs/framework/get-started/system-requirements.md).  
**Заголовок.** Нет     
**Библиотека:** Нет  
**Версии платформы .NET Framework:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>См. также

- [Отладка](index.md)
- [Интерфейс DacpGetModuleAddress](dacpgetmoduleaddress-structure.md)