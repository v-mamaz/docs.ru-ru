---
title: Элемент <supportedRuntime>
ms.date: 04/10/2018
ms.custom: updateeachrelease
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#supportedRuntime
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/startup/supportedRuntime
helpviewer_keywords:
- supportedRuntime element
- <supportedRuntime> element
ms.assetid: 1ae16e23-afbe-4de4-b413-bc457f37b69f
ms.openlocfilehash: 93e69290062e1b82dddbb68f7a139763695a42fb
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271776"
---
# <a name="supportedruntime-element"></a>\<supportedRuntime > элемент

Указывает, какие версии среды CLR поддерживает приложение. Этот элемент должен использоваться всеми приложениями, собранными с применением версии 1.1 или более поздней версии .NET Framework.  
  
[\<configuration>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
&nbsp;&nbsp;[\<Startup >](../../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<supportedRuntime >**  
  
## <a name="syntax"></a>Синтаксис
  
```xml  
<supportedRuntime version="runtime version" sku="sku id"/>  
```  
  
## <a name="attributes"></a>Атрибуты
  
|Атрибут|Описание:|  
|---------------|-----------------|  
|**version**|Необязательный атрибут.<br /><br /> Строковое значение, задающее версию среды CLR, которая поддерживается данным приложением. Допустимые значения `version` атрибут, см. в разделе [значения «runtime version»](#version) раздел. **Примечание.**  Через .NET Framework 3.5 "*версии среды выполнения*" значение принимает форму *основных*. *дополнительный номер*. *Построение*. Начиная с [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)], требуются только основной и дополнительный номера версии (то есть "v4.0" вместо "v4.0.30319"). Рекомендуется использовать более короткие строки.|  
|**sku**|Необязательный атрибут.<br /><br /> Строковое значение, которое указывает единицу складского хранения (SKU), которая, в свою очередь, указывает выпуск .NET Framework, поддерживаемый этим приложением.<br /><br /> Начиная с .NET Framework 4.0, рекомендуется использовать атрибут `sku`.  Если он присутствует, он указывает целевую версию .NET Framework приложения.<br /><br /> Допустимые значения атрибута sku см. в разделе [значения «sku id»](#sku) раздел.|  
  
## <a name="remarks"></a>Примечания

Если  **\<supportedRuntime >** элемент отсутствует в файле конфигурации приложения, используется версия среды выполнения, используемый для построения приложения.  

**\<SupportedRuntime >** элемент должен использоваться всеми приложениями, собранными с применением версии 1.1 или более поздней версии среды выполнения. Приложения, созданные для поддержки только версии 1.0 среды выполнения, должны использовать [ \<requiredRuntime >](../../../../../docs/framework/configure-apps/file-schema/startup/requiredruntime-element.md) элемент.  
  
> [!NOTE]
>  Если вы используете [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md) функции для указания файла конфигурации, необходимо использовать `<requiredRuntime>` элемент для всех версий среды выполнения. `<supportedRuntime>` Элемент учитывается при использовании [CorBindToRuntimeByCfg](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md).  
  
Для приложений, поддерживающих версии среды выполнения от .NET Framework 1.1 до 3.5, при поддержке нескольких версий среды выполнения первый элемент должен задавать наиболее предпочтительную версию среды, а последний — наименее предпочтительную. Для приложений, поддерживающих .NET Framework 4.0 или более поздних версий, атрибут `version` указывает версию CLR, общую для .NET Framework 4 и более поздних версий, а атрибут `sku` указывает одну целевую версию .NET Framework приложения.  
  
> [!NOTE]
>  Если приложение использует устаревшие активации пути, такие как [функция CorBindToRuntimeEx](../../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md), и нужно, чтобы эти пути для активации версии 4 среды CLR вместо более ранней версии, или если приложение создано с помощью [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], но имеет зависимость от сборки смешанного режима, созданных с помощью более ранней версии платформы .NET Framework, недостаточно для указания [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] в список поддерживаемых сред выполнения. Кроме того, в [ \<startup > элемент](../../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) в файле конфигурации необходимо задать `useLegacyV2RuntimeActivationPolicy` атрибут `true`. Однако при установке для этого атрибута значения `true` все компоненты, собранные с более ранними версиями .NET Framework, будут работать с использованием [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], а не сред выполнения, с которыми они были собраны.  
  
Приложения рекомендуется тестировать со всеми версиями .NET Framework, в которых они могут работать.  
  
<a name="version"></a>   
## <a name="runtime-version-values"></a>Значения "runtime version"  
`runtime` Атрибут указывает версию Common Language Runtime (CLR), которая требуется для данного приложения. Обратите внимание, что все версии .NET Framework версий 4.x укажите `v4.0` среды CLR. В следующей таблице перечислены допустимые значения для *версии среды выполнения* значение `version` атрибута.  

|Версия платформы .NET Framework|Атрибут `version`|  
|----------------------------|-------------------------|  
|1.0|"v1.0.3705"|  
|1.1|"v1.1.4322"|  
|2.0|"v2.0.50727"|  
|3.0|"v2.0.50727"|  
|3.5|"v2.0.50727"|  
|4.0-4.7.2|"v4.0"|  

<a name="sku"></a>   
## <a name="sku-id-values"></a>Значения "sku id"

`sku` Атрибут использует моникера целевой платформы (TFM), чтобы указать версию .NET Framework, который предназначен для приложения и требуется для ее выполнения. В следующей таблице перечислены допустимые значения, которые поддерживаются `sku` атрибут, начиная с .NET Framework 4.
  
|Версия платформы .NET Framework|Атрибут `sku`|  
|----------------------------|---------------------|  
|4.0|".NETFramework,Version=v4.0"|  
|4.0, клиентский профиль|".NETFramework,Version=v4.0,Profile=Client"|  
|4.0, обновление платформы 1|". NETFramework, версия = v4.0.1»|  
|4.0, клиентский профиль, обновление 1|". NETFramework, версия = v4.0.1, профиль = клиента»|  
|4.0, обновление платформы 2|". NETFramework, версия = v4.0.2»|  
|4.0, клиентский профиль, обновление 2|". NETFramework, версия = v4.0.2, профиль = клиента»|  
|4.0, обновление платформы 3|". NETFramework, версия = verze 4.0.3»|  
|4.0, клиентский профиль, обновление 3|". NETFramework, версия = verze 4.0.3, профиль = клиента»|  
|4.5|".NETFramework,Version=v4.5"|  
|4.5.1|".NETFramework,Version=v4.5.1"|  
|4.5.2|".NETFramework,Version=v4.5.2"|  
|4.6|".NETFramework,Version=v4.6"|  
|4.6.1|".NETFramework,Version=v4.6.1"|  
|4.6.2|". NETFramework, версия = v4.6.2»|  
|4.7|". NETFramework, версия = v4.7»|
|4.7.1|". NETFramework, версия = v4.7.1»|
|4.7.2|". NETFramework, версия = v4.7.2»|

## <a name="example"></a>Пример  
 В следующем примере показано задание в файле конфигурации поддерживаемых версий среды выполнения. В файле конфигурации указано, что приложение предназначено для .NET Framework 4.7.  
  
```xml  
<configuration>  
   <startup>  
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.7" />  
   </startup>  
</configuration>  
```  
  
## <a name="configuration-file"></a>файл конфигурации

Этот элемент может использоваться в файле конфигурации приложения.

## <a name="see-also"></a>См. также

- [Схема параметров запуска](../../../../../docs/framework/configure-apps/file-schema/startup/index.md)
- [Схема файла конфигурации](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [Внутрипроцессное параллельное выполнение](../../../../../docs/framework/deployment/in-process-side-by-side-execution.md)
