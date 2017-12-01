---
title: "IMetaDataImport2::GetGenericParamConstraintProps (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport2.GetGenericParamConstraintProps
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport2::GetGenericParamConstraintProps
helpviewer_keywords:
- IMetaDataImport2::GetGenericParamConstraintProps method [.NET Framework metadata]
- GetGenericParamConstraintProps method [.NET Framework metadata]
ms.assetid: c5fee4a0-b132-4e5e-8730-e586ce314b9a
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 7d1e560dd511758652e1acbc262b4ddc3efdd12c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimport2getgenericparamconstraintprops-method"></a><span data-ttu-id="33c64-102">IMetaDataImport2::GetGenericParamConstraintProps (Método)</span><span class="sxs-lookup"><span data-stu-id="33c64-102">IMetaDataImport2::GetGenericParamConstraintProps Method</span></span>
<span data-ttu-id="33c64-103">Obtiene los metadatos asociados con la restricción de parámetro genérico representada por el token de restricción especificada.</span><span class="sxs-lookup"><span data-stu-id="33c64-103">Gets the metadata associated with the generic parameter constraint represented by the specified constraint token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="33c64-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33c64-104">Syntax</span></span>  
  
```  
HRESULT GetGenericParamConstraintProps (  
   [in]  mdGenericParamConstraint  gpc,  
   [out] mdGenericParam            *ptGenericParam,  
   [out] mdToken                   *ptkConstraintType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="33c64-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33c64-105">Parameters</span></span>  
 `gpc`  
 <span data-ttu-id="33c64-106">[in] El token a la restricción de parámetro genérico para el que se va a devolver los metadatos.</span><span class="sxs-lookup"><span data-stu-id="33c64-106">[in] The token to the generic parameter constraint for which to return the metadata.</span></span>  
  
 `ptGenericParam`  
 <span data-ttu-id="33c64-107">[out] Un puntero al token que representa el parámetro genérico que está restringido.</span><span class="sxs-lookup"><span data-stu-id="33c64-107">[out] A pointer to the token that represents the generic parameter that is constrained.</span></span>  
  
 `ptkConstraintType`  
 <span data-ttu-id="33c64-108">[out] Un puntero a un token de TypeDef, TypeRef o TypeSpec que representa una restricción en `ptGenericParam`.</span><span class="sxs-lookup"><span data-stu-id="33c64-108">[out] A pointer to a TypeDef, TypeRef, or TypeSpec token that represents a constraint on `ptGenericParam`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="33c64-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33c64-109">Requirements</span></span>  
 <span data-ttu-id="33c64-110">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="33c64-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="33c64-111">**Encabezado:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="33c64-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="33c64-112">**Biblioteca:** usada como recurso en MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="33c64-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="33c64-113">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="33c64-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33c64-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="33c64-114">See Also</span></span>  
 [<span data-ttu-id="33c64-115">IMetaDataImport2 (interfaz)</span><span class="sxs-lookup"><span data-stu-id="33c64-115">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)  
 [<span data-ttu-id="33c64-116">IMetaDataImport (interfaz)</span><span class="sxs-lookup"><span data-stu-id="33c64-116">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)