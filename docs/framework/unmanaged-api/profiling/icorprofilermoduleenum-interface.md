---
title: ICorProfilerModuleEnum (Interfaz)
ms.date: 03/30/2017
api_name:
- ICorProfilerModuleEnum
api_location:
- mscorwks.cll
api_type:
- COM
f1_keywords:
- ICorProfilerModuleEnum
helpviewer_keywords:
- ICorProfilerModuleEnum interface [.NET Framework profiling]
ms.assetid: 24d0fcfa-1601-4fba-868f-da8c97303467
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8966a2fc9e38594e8b2727077b7e1e85c3e52b16
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54705487"
---
# <a name="icorprofilermoduleenum-interface"></a>ICorProfilerModuleEnum (Interfaz)
Proporciona métodos para iterar secuencialmente por una colección de módulos cargados por la aplicación o por el generador de perfiles.  
  
## <a name="methods"></a>Métodos  
  
|Método|Descripción|  
|------------|-----------------|  
|[Clone (método)](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-clone-method.md)|Obtiene un puntero de interfaz a una copia de esta interfaz `ICorProfilerModuleEnum`.|  
|[GetCount (método)](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-getcount-method.md)|Obtiene el número de módulos administrados que se cargaron en la aplicación.|  
|[Next (método)](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-next-method.md)|Obtiene el número especificado de módulos contiguos de una colección secuencial de módulos, comenzando en la posición actual del enumerador en la secuencia.|  
|[Reset (método)](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-reset-method.md)|Mueve el cursor del enumerador a la posición inicial de la secuencia.|  
|[Skip (método)](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-skip-method.md)|Desplaza la posición del cursor del enumerador de manera que se omite el número especificado de elementos.|  
  
## <a name="remarks"></a>Comentarios  
 La interfaz `ICorProfilerModuleEnum` es un enumerador. Permite al receptor de una matriz extraer los elementos del remitente a una velocidad que sea adecuada para el receptor. En otras palabras, el receptor es capaz de controlar explícitamente el flujo de elementos de matriz, lo que evita los problemas asociados con pasar matrices de gran tamaño como parámetros de método.  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** Consulte [Requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Encabezado**: CorProf.idl, CorProf.h  
  
 **Biblioteca:** CorGuids.lib  
  
 **Versiones de .NET Framework:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Vea también
- [ICorProfilerInfo (interfaz)](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [Interfaces para generación de perfiles](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [EnumModules (método)](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-enummodules-method.md)
