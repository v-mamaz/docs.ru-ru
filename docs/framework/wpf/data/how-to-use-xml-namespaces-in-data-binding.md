---
title: Практическое руководство. Использование пространств имен XML при связывании данных
ms.date: 03/30/2017
helpviewer_keywords:
- XML [WPF], namespaces
- data binding [WPF], XML namespaces
- namespaces [WPF], XML
ms.assetid: a47c832f-dc84-48f2-96d5-cde18fc4284b
ms.openlocfilehash: 190bf22544bd17cb215870728333211795040294
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "57377336"
---
# <a name="how-to-use-xml-namespaces-in-data-binding"></a>Практическое руководство. Использование пространств имен XML при связывании данных
## <a name="example"></a>Пример  
 В этом примере демонстрируется обработка пространств имен, указанных в источнике привязки [!INCLUDE[TLA#tla_xml](../../../../includes/tlasharptla-xml-md.md)].  
  
 Если данные [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] имеют следующее определение пространства имен [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)].  
  
 `<rss version="2.0" xmlns:dc="http://purl.org/dc/elements/1.1/">`  
  
 Можно использовать <xref:System.Windows.Data.XmlNamespaceMapping> элемент для сопоставления пространства имен, чтобы <xref:System.Windows.Data.XmlNamespaceMapping.Prefix%2A>, как показано в следующем примере. Затем можно использовать <xref:System.Windows.Data.XmlNamespaceMapping.Prefix%2A> для ссылки на [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] пространства имен. <xref:System.Windows.Controls.ListBox> В этом примере отображается *title* и *DC: Date* каждого *элемент*.  
  
 [!code-xaml[XmlnsBindSnippet#XmlNamespaceMapping](~/samples/snippets/csharp/VS_Snippets_Wpf/XmlnsBindSnippet/CS/Window1.xaml#xmlnamespacemapping)]  
  
 Обратите внимание, что <xref:System.Windows.Data.XmlNamespaceMapping.Prefix%2A> вами не должно соответствовать использованному в [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] источника; Если префикс изменяется в [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] источника, то сопоставление по-прежнему работает.  
  
 В данном конкретном примере [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] данные поступают из веб-службы, но <xref:System.Windows.Data.XmlNamespaceMapping> элемент также работает со встроенными [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] или [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] данных во внедренном файле.  
  
## <a name="see-also"></a>См. также
- [Практическое руководство. Привязка к XML-данным с помощью XMLDataProvider и запросов XPath](how-to-bind-to-xml-data-using-an-xmldataprovider-and-xpath-queries.md)
- [Общие сведения о привязке данных](data-binding-overview.md)
- [Разделы практического руководства](data-binding-how-to-topics.md)
