---
title: Интерфейс ICorDebugFunction2
ms.date: 03/30/2017
api_name:
- ICorDebugFunction2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction2
helpviewer_keywords:
- ICorDebugFunction2 interface [.NET Framework debugging]
ms.assetid: 2b936bef-9b75-48bf-859f-42e419c65f1c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d051c7d61d6ade1fc0d313c47125d9c196bcca1d
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2019
ms.locfileid: "56979592"
---
# <a name="icordebugfunction2-interface"></a>Интерфейс ICorDebugFunction2

Логически расширяет интерфейс ICorDebugFunction для обеспечения поддержки Just My Code пошаговую отладку, который пропускает непользовательский код.  
  
## <a name="methods"></a>Методы  
  
|Метод|Описание|  
|------------|-----------------|  
|[Метод EnumerateNativeCode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction2-enumeratenativecode-method.md)|(Еще не реализовано). Получает указатель на интерфейс ICorDebugCodeEnum, содержащий инструкции машинного кода в функции, на которые ссылается этот объект ICorDebugFunction2.|  
|[Метод GetJMCStatus](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction2-getjmcstatus-method.md)|Получает значение, указывающее, помечена ли эта функция как пользовательский код.|  
|[Метод GetVersionNumber](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction2-getversionnumber-method.md)|Получает версию "Изменить и продолжить" этой функции.|  
|[Метод SetJMCStatus](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction2-setjmcstatus-method.md)|Помечает эту функцию только мой код пошагового выполнения.|  
  
## <a name="remarks"></a>Примечания  
  
> [!NOTE]
>  Этот интерфейс не поддерживает удаленные вызовы между компьютерами или между процессами.  
  
## <a name="requirements"></a>Требования  
 **Платформы:** См. раздел [Требования к системе](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Заголовок.** CorDebug.idl, CorDebug.h  
  
 **Библиотека:** CorGuids.lib  
  
 **Версии платформы .NET Framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>См. также
- [Интерфейсы отладки](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
