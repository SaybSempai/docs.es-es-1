---
title: System.ServiceModel.ManualFlowThrottleLimitReached
ms.date: 03/30/2017
ms.assetid: 9aba851f-1830-493b-8e3e-60f454eb923e
ms.openlocfilehash: 86d47ab0a83ff3e4a68bfa8ccf1349cf2b345b23
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54597741"
---
# <a name="systemservicemodelmanualflowthrottlelimitreached"></a>System.ServiceModel.ManualFlowThrottleLimitReached
System.ServiceModel.ManualFlowThrottleLimitReached  
  
## <a name="description"></a>Descripción  
 El sistema alcanzó el límite establecido para el acelerador de ManualFlowControlLimit. El valor de acelerador se puede cambiar modificando la propiedad ManualFlowControlLimit en ServiceHost o InstanceContext, según sea aplicable.  
  
 Se emite este seguimiento cuando el límite del control de flujo manual se reduce inicialmente a 0. No se realiza un seguimiento de los cambios subsiguientes hasta 0. Para cada contexto se realiza un seguimiento del límite del control de flujo en el contexto de la instancia.  
  
## <a name="see-also"></a>Vea también
- [Traza](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [Uso del seguimiento para solucionar problemas de su aplicación](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [Administración y diagnóstico](../../../../../docs/framework/wcf/diagnostics/index.md)
