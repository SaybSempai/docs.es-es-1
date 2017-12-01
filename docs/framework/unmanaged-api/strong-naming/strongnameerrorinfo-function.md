---
title: "StrongNameErrorInfo (Función)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: StrongNameErrorInfo
api_location:
- mscoree.dll
- mscorsn.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type: DLLExport
f1_keywords: StrongNameErrorInfo
helpviewer_keywords: StrongNameErrorInfo function [.NET Framework strong naming]
ms.assetid: e91bf8c3-7c26-4732-938e-2e5b04abfc99
topic_type: apiref
caps.latest.revision: "17"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 0fbe77f16ed022458a036b6627b82f80d194276c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="strongnameerrorinfo-function"></a><span data-ttu-id="22ca0-102">StrongNameErrorInfo (Función)</span><span class="sxs-lookup"><span data-stu-id="22ca0-102">StrongNameErrorInfo Function</span></span>
<span data-ttu-id="22ca0-103">Obtiene el último código de error que se genera mediante una de las funciones de nombre seguro.</span><span class="sxs-lookup"><span data-stu-id="22ca0-103">Gets the last error code that was raised by one of the strong name functions.</span></span>  
  
 <span data-ttu-id="22ca0-104">Esta función está desusada.</span><span class="sxs-lookup"><span data-stu-id="22ca0-104">This function has been deprecated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22ca0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22ca0-105">Syntax</span></span>  
  
```  
HRESULT StrongNameErrorInfo ();   
```  
  
## <a name="return-value"></a><span data-ttu-id="22ca0-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22ca0-106">Return Value</span></span>  
 <span data-ttu-id="22ca0-107">El último código de error de COM establecido por una de las funciones de nombre seguro.</span><span class="sxs-lookup"><span data-stu-id="22ca0-107">The last COM error code set by one of the strong name functions.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="22ca0-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22ca0-108">Remarks</span></span>  
 <span data-ttu-id="22ca0-109">La mayoría de los métodos de nombre seguro devuelven una simple `true` o `false` indicación de una realización correcta.</span><span class="sxs-lookup"><span data-stu-id="22ca0-109">Most of the strong name methods return a simple `true` or `false` indication of successful completion.</span></span> <span data-ttu-id="22ca0-110">Use la `StrongNameErrorInfo` función para recuperar un valor HRESULT que especifica el último error generado por las funciones de nombre seguro.</span><span class="sxs-lookup"><span data-stu-id="22ca0-110">Use the `StrongNameErrorInfo` function to retrieve an HRESULT that specifies the last error generated by the strong name functions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="22ca0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22ca0-111">Requirements</span></span>  
 <span data-ttu-id="22ca0-112">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="22ca0-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22ca0-113">**Encabezado:** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="22ca0-113">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="22ca0-114">**Biblioteca:** incluye como recurso en MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="22ca0-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="22ca0-115">**Versiones de .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22ca0-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22ca0-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="22ca0-116">See Also</span></span>  
 [<span data-ttu-id="22ca0-117">Las funciones estáticas globales de nombres seguros</span><span class="sxs-lookup"><span data-stu-id="22ca0-117">Strong Naming Global Static Functions</span></span>](http://msdn.microsoft.com/en-us/efa715df-e8cc-48f2-9ec4-26586f0dc8d0)