---
title: "IMetaDataEmit::SetFieldProps (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataEmit.SetFieldProps
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataEmit::SetFieldProps
helpviewer_keywords:
- IMetaDataEmit::SetFieldProps method [.NET Framework metadata]
- SetFieldProps method [.NET Framework metadata]
ms.assetid: 47132dda-fa92-4bd1-ae4b-24cd9a60665a
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 5f031e79deab57184043eaa44d2d8a3d369187c7
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataemitsetfieldprops-method"></a><span data-ttu-id="3f836-102">IMetaDataEmit::SetFieldProps (Método)</span><span class="sxs-lookup"><span data-stu-id="3f836-102">IMetaDataEmit::SetFieldProps Method</span></span>
<span data-ttu-id="3f836-103">Establece o actualiza el valor predeterminado para el campo al que hace referencia el token de campo especificado.</span><span class="sxs-lookup"><span data-stu-id="3f836-103">Sets or updates the default value for the field referenced by the specified field token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f836-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f836-104">Syntax</span></span>  
  
```  
HRESULT SetFieldProps (  
    [in]  mdFieldDef  fd,   
    [in]  DWORD       dwFieldFlags,   
    [in]  DWORD       dwCPlusTypeFlag,   
    [in]  void const  *pValue,   
    [in]  ULONG       cchValue   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3f836-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f836-105">Parameters</span></span>  
 `fd`  
 <span data-ttu-id="3f836-106">[in] El token para el campo de destino.</span><span class="sxs-lookup"><span data-stu-id="3f836-106">[in] The token for the target field.</span></span>  
  
 `dwFieldFlags`  
 <span data-ttu-id="3f836-107">[in] Atributos de campo.</span><span class="sxs-lookup"><span data-stu-id="3f836-107">[in] Field attributes.</span></span> <span data-ttu-id="3f836-108">Se trata de una máscara de bits de `CorFieldAttr` valores.</span><span class="sxs-lookup"><span data-stu-id="3f836-108">This is a bitmask of `CorFieldAttr` values.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="3f836-109">[in] El `ELEMENT_TYPE_`  *\**  para el valor constante.</span><span class="sxs-lookup"><span data-stu-id="3f836-109">[in] The `ELEMENT_TYPE_`*\** for the constant value.</span></span> <span data-ttu-id="3f836-110">Se trata de un `CorElementType` valor.</span><span class="sxs-lookup"><span data-stu-id="3f836-110">This is a `CorElementType` value.</span></span> <span data-ttu-id="3f836-111">Si no se está definiendo una constante, establezca este valor en `ELEMENT_TYPE_END`.</span><span class="sxs-lookup"><span data-stu-id="3f836-111">If a constant is not being defined, set this value to `ELEMENT_TYPE_END`.</span></span>  
  
 `pValue`  
 <span data-ttu-id="3f836-112">[in] El valor constante para el campo.</span><span class="sxs-lookup"><span data-stu-id="3f836-112">[in] The constant value for the field.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="3f836-113">[in] El tamaño, en caracteres Unicode, de `pValue`.</span><span class="sxs-lookup"><span data-stu-id="3f836-113">[in] The size, in Unicode characters, of `pValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f836-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f836-114">Requirements</span></span>  
 <span data-ttu-id="3f836-115">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3f836-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3f836-116">**Encabezado:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="3f836-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3f836-117">**Biblioteca:** usada como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3f836-117">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3f836-118">**Versiones de .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3f836-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f836-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f836-119">See Also</span></span>  
 [<span data-ttu-id="3f836-120">IMetaDataEmit (interfaz)</span><span class="sxs-lookup"><span data-stu-id="3f836-120">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="3f836-121">IMetaDataEmit2 (interfaz)</span><span class="sxs-lookup"><span data-stu-id="3f836-121">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)