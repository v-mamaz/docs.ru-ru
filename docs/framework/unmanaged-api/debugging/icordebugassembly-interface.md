---
title: Интерфейс ICorDebugAssembly
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly
helpviewer_keywords:
- ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: 9d657a28-6984-4c5e-8a54-89d20080baff
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a2b802845e36e818a962484c1fea09cbcc1ceefd
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2019
ms.locfileid: "56974579"
---
# <a name="icordebugassembly-interface"></a>Интерфейс ICorDebugAssembly

Представляет сборку.  
  
## <a name="methods"></a>Методы  
  
|Метод|Описание:|  
|------------|-----------------|  
|[Метод EnumerateModules](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-enumeratemodules-method.md)|Получает перечислитель для модулей, содержащихся в сборке.|  
|[Метод GetAppDomain](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getappdomain-method.md)|Получает указатель интерфейса на домен приложения, который содержит это `ICorDebugAssembly` экземпляра.|  
|[Метод GetCodeBase](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getcodebase-method.md)|Не реализован в текущей версии платформы .NET Framework.|  
|[Метод GetName](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getname-method.md)|Возвращает имя сборки.|  
|[Метод GetProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getprocess-method.md)|Получает экземпляр ICorDebugProcess, в которой выполняется сборка.|  
  
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
