---
title: "ICorDebugInternalFrame::GetFrameType (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugInternalFrame.GetFrameType
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugInternalFrame::GetFrameType
helpviewer_keywords:
- GetFrameType method [.NET Framework debugging]
- ICorDebugInternalFrame::GetFrameType method [.NET Framework debugging]
ms.assetid: da278a29-dc2e-4bf7-96ce-801bdc4d7025
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d9d3dd087662c938b2f733458d1e92cff577e9f7
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="icordebuginternalframegetframetype-method"></a><span data-ttu-id="75acd-102">ICorDebugInternalFrame::GetFrameType (Método)</span><span class="sxs-lookup"><span data-stu-id="75acd-102">ICorDebugInternalFrame::GetFrameType Method</span></span>
<span data-ttu-id="75acd-103">Obtiene el tipo de este marco interno.</span><span class="sxs-lookup"><span data-stu-id="75acd-103">Gets the type of this internal frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="75acd-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75acd-104">Syntax</span></span>  
  
```  
HRESULT GetFrameType (  
    [out] CorDebugInternalFrameType  *pType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="75acd-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75acd-105">Parameters</span></span>  
 `pType`  
 <span data-ttu-id="75acd-106">[out] Un puntero a un valor de la enumeración CorDebugInternalFrameType que indica el tipo de marco interno representado por este `ICorDebugInternalFrame` objeto.</span><span class="sxs-lookup"><span data-stu-id="75acd-106">[out] A pointer to a value of the CorDebugInternalFrameType enumeration that indicates the type of internal frame represented by this `ICorDebugInternalFrame` object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="75acd-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="75acd-107">Remarks</span></span>  
 <span data-ttu-id="75acd-108">El tipo de marco interno nunca será STUBFRAME_NONE.</span><span class="sxs-lookup"><span data-stu-id="75acd-108">The internal frame type will never be STUBFRAME_NONE.</span></span> <span data-ttu-id="75acd-109">Depuradores deberían omitir correctamente los tipos de marco internos no reconocidos.</span><span class="sxs-lookup"><span data-stu-id="75acd-109">Debuggers should gracefully ignore unrecognized internal frame types.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="75acd-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75acd-110">Requirements</span></span>  
 <span data-ttu-id="75acd-111">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="75acd-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="75acd-112">**Encabezado:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="75acd-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="75acd-113">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="75acd-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="75acd-114">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="75acd-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>