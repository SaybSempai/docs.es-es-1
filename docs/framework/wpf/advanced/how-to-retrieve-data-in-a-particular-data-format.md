---
title: Procedimiento Recuperar datos en un formato concreto
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drag-and-drop [WPF], retrieving data
- DataFormats class [WPF], retrieving data
- DataObject class [WPF], retrieving data
ms.assetid: a625acf3-1144-44cd-add7-456aefc3859f
ms.openlocfilehash: d11374cbc70210e648e93a385c4a9fbca112c09f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54718304"
---
# <a name="how-to-retrieve-data-in-a-particular-data-format"></a>Procedimiento Recuperar datos en un formato concreto
Los ejemplos siguientes muestran cómo recuperar datos de un objeto de datos en un formato especificado.  
  
## <a name="example"></a>Ejemplo  
  
### <a name="description"></a>Descripción  
 El código de ejemplo siguiente usa el <xref:System.Windows.DataObject.GetDataPresent%28System.String%29> sobrecarga compruebe primero si dar formato a datos especificado está disponible (de forma nativa o mediante la conversión automática); si el formato especificado está disponible, el ejemplo recupera los datos mediante el <xref:System.Windows.DataObject.GetData%28System.String%29> método.  
  
### <a name="code"></a>Código  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getspecificdataformat)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getspecificdataformat)]  
  
## <a name="example"></a>Ejemplo  
  
### <a name="description"></a>Descripción  
 El código de ejemplo siguiente usa el <xref:System.Windows.DataObject.GetDataPresent%28System.String%2CSystem.Boolean%29> sobrecarga compruebe primero si un formato de datos especificado está disponible de forma nativa (se filtran los formatos de datos); si el formato especificado está disponible, el ejemplo recupera los datos mediante el uso de la <xref:System.Windows.DataObject.GetData%28System.String%29>método.  
  
### <a name="code"></a>Código  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat_Native](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getspecificdataformat_native)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat_Native](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getspecificdataformat_native)]  
  
## <a name="see-also"></a>Vea también
- <xref:System.Windows.IDataObject>
- [Información general sobre la función de arrastrar y colocar](../../../../docs/framework/wpf/advanced/drag-and-drop-overview.md)
