---
title: "ICorProfilerCallback::JITCompilationFinished (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.JITCompilationFinished
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::JITCompilationFinished
helpviewer_keywords:
- JITCompilationFinished method [.NET Framework profiling]
- ICorProfilerCallback::JITCompilationFinished method [.NET Framework profiling]
ms.assetid: 8dcd7537-d0c6-498c-8a56-2c060310ef65
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 9719ce1474c2111692c6176655b75bd2d7edf923
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallbackjitcompilationfinished-method"></a><span data-ttu-id="f3409-102">ICorProfilerCallback::JITCompilationFinished (Método)</span><span class="sxs-lookup"><span data-stu-id="f3409-102">ICorProfilerCallback::JITCompilationFinished Method</span></span>
<span data-ttu-id="f3409-103">Notifica al generador de perfiles que el compilador de just-in-time (JIT) ha terminado de compilar una función.</span><span class="sxs-lookup"><span data-stu-id="f3409-103">Notifies the profiler that the just-in-time (JIT) compiler has finished compiling a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3409-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3409-104">Syntax</span></span>  
  
```  
HRESULT JITCompilationFinished(  
    [in] FunctionID functionId,  
    [in] HRESULT    hrStatus,  
    [in] BOOL       fIsSafeToBlock);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f3409-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3409-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="f3409-106">[in] El identificador de la función que se compiló.</span><span class="sxs-lookup"><span data-stu-id="f3409-106">[in] The ID of the function that was compiled.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="f3409-107">[in] Un valor que indica si la compilación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f3409-107">[in] A value indicating whether compilation was successful.</span></span>  
  
 `fIsSafeToBlock`  
 <span data-ttu-id="f3409-108">[in] Un valor que indica al generador de perfiles si el bloqueo afectará al funcionamiento del tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f3409-108">[in] A value indicating to the profiler whether blocking will affect the operation of the runtime.</span></span> <span data-ttu-id="f3409-109">El valor es `true` Si bloqueo puede hacer que el tiempo de ejecución esperar el subproceso de llamada devolver desde esta devolución de llamada; de lo contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="f3409-109">The value is `true` if blocking may cause the runtime to wait for the calling thread to return from this callback; otherwise, `false`.</span></span>  
  
 <span data-ttu-id="f3409-110">Aunque un valor de `true` no dañarán el tiempo de ejecución, se pueden falsear los resultados de la generación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="f3409-110">Although a value of `true` will not harm the runtime, it can skew the profiling results.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f3409-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3409-111">Requirements</span></span>  
 <span data-ttu-id="f3409-112">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f3409-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f3409-113">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="f3409-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="f3409-114">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f3409-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f3409-115">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f3409-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3409-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3409-116">See Also</span></span>  
 [<span data-ttu-id="f3409-117">ICorProfilerCallback (interfaz)</span><span class="sxs-lookup"><span data-stu-id="f3409-117">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="f3409-118">JITCompilationStarted (método)</span><span class="sxs-lookup"><span data-stu-id="f3409-118">JITCompilationStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-jitcompilationstarted-method.md)