---
title: "AssemblyOptions (Enumeración)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: AssemblyOptions
api_location: alink.dll
api_type: COM
f1_keywords: AssemblyOptions
helpviewer_keywords:
- Alink API, AssemblyOptions enumeration
- AssemblyOptions enumeration
ms.assetid: 84f83921-64cb-49e3-ac8b-22a0b77b18a8
topic_type: apiref
caps.latest.revision: "5"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: ccbbcabd3fbb372322ca6334f6ab6db4fdafc2f1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="assemblyoptions-enumeration"></a><span data-ttu-id="5e490-102">AssemblyOptions (Enumeración)</span><span class="sxs-lookup"><span data-stu-id="5e490-102">AssemblyOptions Enumeration</span></span>
<span data-ttu-id="5e490-103">Enumera las opciones de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5e490-103">Enumerates the assembly options.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e490-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e490-104">Syntax</span></span>  
  
```  
typedef enum _AssemblyOptions {  
    optAssemTitle = 0,  
    optAssemDescription,  
    optAssemConfig,  
    optAssemOS,  
    optAssemProcessor,  
    optAssemLocale,  
    optAssemVersion,  
    optAssemCompany,  
    optAssemProduct,  
    optAssemProductVersion,  
    optAssemCopyright,  
    optAssemTrademark,  
    optAssemKeyFile,  
    optAssemKeyName,  
    optAssemAlgID,  
    optAssemFlags,  
    optAssemHalfSign,  
    optAssemFileVersion,  
    optAssemSatelliteVer,  
    optLastAssemOption  
}   AssemblyOptions;  
```  
  
## <a name="fields"></a><span data-ttu-id="5e490-105">Campos</span><span class="sxs-lookup"><span data-stu-id="5e490-105">Fields</span></span>  
  
|<span data-ttu-id="5e490-106">Campo</span><span class="sxs-lookup"><span data-stu-id="5e490-106">Field</span></span>|<span data-ttu-id="5e490-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e490-107">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="5e490-108">optAssemTitle</span><span class="sxs-lookup"><span data-stu-id="5e490-108">optAssemTitle</span></span>|<span data-ttu-id="5e490-109">Cadena: representa el título del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5e490-109">String - Represents the assembly title.</span></span>|  
|<span data-ttu-id="5e490-110">optAssemDescription</span><span class="sxs-lookup"><span data-stu-id="5e490-110">optAssemDescription</span></span>|<span data-ttu-id="5e490-111">Cadena: contiene la descripción del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5e490-111">String - Contains the assembly description.</span></span>|  
|<span data-ttu-id="5e490-112">optAssemConfig</span><span class="sxs-lookup"><span data-stu-id="5e490-112">optAssemConfig</span></span>|<span data-ttu-id="5e490-113">Cadena: contiene la configuración del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5e490-113">String - Contains the assembly configuration.</span></span>|  
|<span data-ttu-id="5e490-114">optAssemOS</span><span class="sxs-lookup"><span data-stu-id="5e490-114">optAssemOS</span></span>|<span data-ttu-id="5e490-115">Cadena: está codificada como: "dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion".</span><span class="sxs-lookup"><span data-stu-id="5e490-115">String - Encoded as: "dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion".</span></span>|  
|<span data-ttu-id="5e490-116">optAssemProcessor</span><span class="sxs-lookup"><span data-stu-id="5e490-116">optAssemProcessor</span></span>|<span data-ttu-id="5e490-117">ULONG</span><span class="sxs-lookup"><span data-stu-id="5e490-117">ULONG</span></span>|  
|<span data-ttu-id="5e490-118">optAssemLocale</span><span class="sxs-lookup"><span data-stu-id="5e490-118">optAssemLocale</span></span>|<span data-ttu-id="5e490-119">Cadena: contiene la configuración regional del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5e490-119">String - Contains the assembly locale.</span></span>|  
|<span data-ttu-id="5e490-120">optAssemVersion</span><span class="sxs-lookup"><span data-stu-id="5e490-120">optAssemVersion</span></span>|<span data-ttu-id="5e490-121">Cadena: está codificada como: "Principal.secundaria.compilación.revisión".</span><span class="sxs-lookup"><span data-stu-id="5e490-121">String - Encoded as: "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="5e490-122">optAssemCompany</span><span class="sxs-lookup"><span data-stu-id="5e490-122">optAssemCompany</span></span>|<span data-ttu-id="5e490-123">Cadena: contiene la empresa.</span><span class="sxs-lookup"><span data-stu-id="5e490-123">String - Contains the company.</span></span>|  
|<span data-ttu-id="5e490-124">optAssemProduct</span><span class="sxs-lookup"><span data-stu-id="5e490-124">optAssemProduct</span></span>|<span data-ttu-id="5e490-125">Cadena: contiene el nombre del producto.</span><span class="sxs-lookup"><span data-stu-id="5e490-125">String - Contains the product name.</span></span>|  
|<span data-ttu-id="5e490-126">optAssemProductVersion</span><span class="sxs-lookup"><span data-stu-id="5e490-126">optAssemProductVersion</span></span>|<span data-ttu-id="5e490-127">Cadena (también conocido como InformationalVersion).</span><span class="sxs-lookup"><span data-stu-id="5e490-127">String (also known as InformationalVersion).</span></span>|  
|<span data-ttu-id="5e490-128">optAssemCopyright</span><span class="sxs-lookup"><span data-stu-id="5e490-128">optAssemCopyright</span></span>|<span data-ttu-id="5e490-129">Cadena: contiene la información de copyright.</span><span class="sxs-lookup"><span data-stu-id="5e490-129">String - Contains the copyright information.</span></span>|  
|<span data-ttu-id="5e490-130">optAssemTrademark</span><span class="sxs-lookup"><span data-stu-id="5e490-130">optAssemTrademark</span></span>|<span data-ttu-id="5e490-131">Cadena: contiene la información de marca comercial.</span><span class="sxs-lookup"><span data-stu-id="5e490-131">String - Contains the trademark information.</span></span>|  
|<span data-ttu-id="5e490-132">optAssemKeyFile</span><span class="sxs-lookup"><span data-stu-id="5e490-132">optAssemKeyFile</span></span>|<span data-ttu-id="5e490-133">Cadena (nombre de archivo).</span><span class="sxs-lookup"><span data-stu-id="5e490-133">String (file name).</span></span>|  
|<span data-ttu-id="5e490-134">optAssemKeyName</span><span class="sxs-lookup"><span data-stu-id="5e490-134">optAssemKeyName</span></span>|<span data-ttu-id="5e490-135">Cadena (el nombre de clave).</span><span class="sxs-lookup"><span data-stu-id="5e490-135">String (The key name).</span></span>|  
|<span data-ttu-id="5e490-136">optAssemAlgID</span><span class="sxs-lookup"><span data-stu-id="5e490-136">optAssemAlgID</span></span>|<span data-ttu-id="5e490-137">ULONG</span><span class="sxs-lookup"><span data-stu-id="5e490-137">ULONG</span></span>|  
|<span data-ttu-id="5e490-138">optAssemFlags</span><span class="sxs-lookup"><span data-stu-id="5e490-138">optAssemFlags</span></span>|<span data-ttu-id="5e490-139">ULONG</span><span class="sxs-lookup"><span data-stu-id="5e490-139">ULONG</span></span>|  
|<span data-ttu-id="5e490-140">optAssemHalfSign</span><span class="sxs-lookup"><span data-stu-id="5e490-140">optAssemHalfSign</span></span>|<span data-ttu-id="5e490-141">BOOL (también conocido como DelaySign).</span><span class="sxs-lookup"><span data-stu-id="5e490-141">Bool (Also known as DelaySign).</span></span>|  
|<span data-ttu-id="5e490-142">optAssemFileVersion</span><span class="sxs-lookup"><span data-stu-id="5e490-142">optAssemFileVersion</span></span>|<span data-ttu-id="5e490-143">Cadena: está codificada como "Major.Minor.Build.Revision" como ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="5e490-143">String - Encoded as "Major.Minor.Build.Revision"--same as ProductVersion.</span></span>|  
|<span data-ttu-id="5e490-144">optAssemSatelliteVer</span><span class="sxs-lookup"><span data-stu-id="5e490-144">optAssemSatelliteVer</span></span>|<span data-ttu-id="5e490-145">Cadena: está codificada como "Major.Minor.Build.Revision".</span><span class="sxs-lookup"><span data-stu-id="5e490-145">String - Encoded as "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="5e490-146">optLastAssemOption</span><span class="sxs-lookup"><span data-stu-id="5e490-146">optLastAssemOption</span></span>|<span data-ttu-id="5e490-147">Un contador del número de elementos.</span><span class="sxs-lookup"><span data-stu-id="5e490-147">A counter of the number of elements.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5e490-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e490-148">Requirements</span></span>  
 <span data-ttu-id="5e490-149">**Encabezado:** alink.h</span><span class="sxs-lookup"><span data-stu-id="5e490-149">**Header:** alink.h</span></span>  
  
 <span data-ttu-id="5e490-150">**Biblioteca**: alink.dll</span><span class="sxs-lookup"><span data-stu-id="5e490-150">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e490-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e490-151">See Also</span></span>  
 [<span data-ttu-id="5e490-152">Al.exe (Assembly Linker)</span><span class="sxs-lookup"><span data-stu-id="5e490-152">Al.exe (Assembly Linker)</span></span>](../../../../docs/framework/tools/al-exe-assembly-linker.md)