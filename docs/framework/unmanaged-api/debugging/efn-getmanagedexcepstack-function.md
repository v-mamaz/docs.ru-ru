---
title: Функция _EFN_GetManagedExcepStack
ms.date: 03/30/2017
api_name:
- _EFN_GetManagedExcepStack
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- _EFN_GetManagedExcepStack
helpviewer_keywords:
- _EFN_GetManagedExcepStack function [.NET Framework debugging]
ms.assetid: 21ceed9e-62b2-4024-b027-6d095109955a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7e86a1d2dfeb0d36b369d3b6cd7ea985591b5959
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "57488415"
---
# <a name="efngetmanagedexcepstack-function"></a>Функция _EFN_GetManagedExcepStack
Учитывая адрес объекта управляемого исключения, возвращает строковую версию трассировки стека, содержащейся внутри.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
HRESULT _EFN_GetManagedExcepStack(  
    [in]  PDEBUG_CLIENT Client,  
    [in]  ULONG64       StackObjAddr,  
    [out] __out_ecount(cbString) PSTR szStackString,  
    [out] ULONG         cbString  
);  
```  
  
## <a name="parameters"></a>Параметры  
 `Client`  
 [in] Клиент, для которого выполняется отладка.  
  
 `StackObjAddr`  
 [in] Указатель на управляемый объект, производный от <xref:System.Exception>.  
  
 szStackString  
 [out] Возвращаемая строка.  
  
 `cbString`  
 [out] Доступное число символов в буфере строк.  
  
## <a name="remarks"></a>Примечания  
 Если отсутствует управляемый код в потоке в данный момент в контексте, функция возвращает HRESULT SOS_E_NOMANAGEDCODE со значением сообщения 0xa0 и кодом ошибки 0x1000.  
  
## <a name="requirements"></a>Требования  
 **Платформы:** См. раздел [Требования к системе](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Заголовок.** SOS_Stacktrace.h  
  
 **Версии платформы .NET framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>См. также
- [Глобальные статические функции отладки](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)
