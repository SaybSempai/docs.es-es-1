---
title: "ICorProfilerInfo4::GetReJITIDs (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo4.GetReJITIDs
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo4::GetReJITIDs
helpviewer_keywords:
- GetReJITIDs method, ICorProfilerInfo4 interface [.NET Framework profiling]
- ICorProfilerInfo4::GetReJITIDs method [.NET Framework profiling]
ms.assetid: 634ac28c-a5b7-4fc3-af84-256c24ca8177
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: cc16cd932fc2ce0cf5cb53c227081501e79ed2d5
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfo4getrejitids-method"></a><span data-ttu-id="032f8-102">ICorProfilerInfo4::GetReJITIDs (Método)</span><span class="sxs-lookup"><span data-stu-id="032f8-102">ICorProfilerInfo4::GetReJITIDs Method</span></span>
<span data-ttu-id="032f8-103">Devuelve una matriz de identificadores que identifican todas las recompilado con JIT versiones de la función especificada que todavía se asignarán.</span><span class="sxs-lookup"><span data-stu-id="032f8-103">Returns an array of IDs that identify all JIT-recompiled versions of the specified function that are still allocated.</span></span> <span data-ttu-id="032f8-104">Esto incluye versiones recompilado con JIT de funciones que se han revertido posteriormente pero que aún no se ha liberado (por ejemplo, cuando el dominio de aplicación que contiene la función revertida aún está en uso).</span><span class="sxs-lookup"><span data-stu-id="032f8-104">This includes JIT-recompiled versions of functions that have been subsequently reverted but not yet freed (for example, when the application domain that contains the reverted function is still in use).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="032f8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="032f8-105">Syntax</span></span>  
  
```  
HRESULT GetReJITIDs (  
     [in]  FunctionID          functionId,  
     [in]  ULONG               cReJitIds,  
     [out] ULONG *             pcReJitIds,  
     [out, size_is(cReJitIds), length_is(*pcReJitIds)]   ReJITID        reJitIds[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="032f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="032f8-106">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="032f8-107">[in] El `FunctionID` de la instancia de la función para la que se va a enumerar versiones.</span><span class="sxs-lookup"><span data-stu-id="032f8-107">[in] The `FunctionID` of the function instance for which to enumerate versions.</span></span>  
  
 `cReJitIds`  
 <span data-ttu-id="032f8-108">[in] El número de identificadores recompilado con JIT asignada en el `reJitIds` matriz.</span><span class="sxs-lookup"><span data-stu-id="032f8-108">[in] The number of JIT-recompiled IDs allocated in the `reJitIds` array.</span></span>  
  
 `pcReJitIds`  
 <span data-ttu-id="032f8-109">[out] El número real de identificadores recompilado con JIT.</span><span class="sxs-lookup"><span data-stu-id="032f8-109">[out] The actual number of JIT-recompiled IDs.</span></span>  
  
 `reJitIds`  
 <span data-ttu-id="032f8-110">[out] Una matriz asignada por el llamador que contendrá los identificadores recompilado con JIT para la función especificada.</span><span class="sxs-lookup"><span data-stu-id="032f8-110">[out] A caller-allocated array that will contain the JIT-recompiled IDs for the specified function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="032f8-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="032f8-111">Remarks</span></span>  
 <span data-ttu-id="032f8-112">`GetReJITIDs`Enumera los identificadores activos recompilado con JIT para una instancia de la función especificada.</span><span class="sxs-lookup"><span data-stu-id="032f8-112">`GetReJITIDs` enumerates the active JIT-recompiled IDs for a given function instance.</span></span> <span data-ttu-id="032f8-113">Sigue el mismo patrón de uso que otros `ICorProfilerInfo` funciones que aceptan búferes asignados al llamador.</span><span class="sxs-lookup"><span data-stu-id="032f8-113">It follows the same usage pattern as other `ICorProfilerInfo` functions that accept caller-allocated buffers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="032f8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="032f8-114">Requirements</span></span>  
 <span data-ttu-id="032f8-115">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="032f8-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="032f8-116">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="032f8-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="032f8-117">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="032f8-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="032f8-118">**Versiones de .NET framework:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="032f8-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="032f8-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="032f8-119">See Also</span></span>  
 [<span data-ttu-id="032f8-120">ICorProfilerInfo4 (interfaz)</span><span class="sxs-lookup"><span data-stu-id="032f8-120">ICorProfilerInfo4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)  
 [<span data-ttu-id="032f8-121">Interfaces de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="032f8-121">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="032f8-122">Generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="032f8-122">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)