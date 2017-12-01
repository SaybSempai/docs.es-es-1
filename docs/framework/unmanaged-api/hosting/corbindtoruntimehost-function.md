---
title: "CorBindToRuntimeHost (Función)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorBindToRuntimeHost
api_location: mscoree.dll
api_type: DLLExport
f1_keywords: CorBindToRuntimeHost
helpviewer_keywords: CorBindToRuntimeHost function [.NET Framework hosting]
ms.assetid: 5c826ba3-8258-49bc-a417-78807915fcaf
topic_type: apiref
caps.latest.revision: "28"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: eff6fdf0294e3b1cc9830e58bc8103a64102d5b1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="corbindtoruntimehost-function"></a><span data-ttu-id="7f369-102">CorBindToRuntimeHost (Función)</span><span class="sxs-lookup"><span data-stu-id="7f369-102">CorBindToRuntimeHost Function</span></span>
<span data-ttu-id="7f369-103">Permite a los hosts cargar una versión determinada de Common Language Runtime (CLR) en un proceso.</span><span class="sxs-lookup"><span data-stu-id="7f369-103">Enables hosts to load a specified version of the common language runtime (CLR) into a process.</span></span>  
  
 <span data-ttu-id="7f369-104">Esta función está desusada en [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="7f369-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f369-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f369-105">Syntax</span></span>  
  
```  
HRESULT CorBindToRuntimeHost (  
    [in] LPCWSTR       pwszVersion,   
    [in] LPCWSTR       pwszBuildFlavor,   
    [in] LPCWSTR       pwszHostConfigFile,   
    [in] VOID*         pReserved,   
    [in] DWORD         startupFlags,   
    [in] REFCLSID      rclsid,   
    [in] REFIID        riid,   
    [out] LPVOID FAR  *ppv  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7f369-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f369-106">Parameters</span></span>  
 `pwszVersion`  
 <span data-ttu-id="7f369-107">[in] Cadena que describe la versión de CLR que se desea cargar.</span><span class="sxs-lookup"><span data-stu-id="7f369-107">[in] A string that describes the version of the CLR you want to load.</span></span>  
  
 <span data-ttu-id="7f369-108">Un número de versión de .NET Framework consta de cuatro partes separadas por puntos: *principal.secundaria.compilación.revisión*.</span><span class="sxs-lookup"><span data-stu-id="7f369-108">A version number in the .NET Framework consists of four parts separated by periods: *major.minor.build.revision*.</span></span> <span data-ttu-id="7f369-109">La cadena que se pasó como `pwszVersion` debe comenzar con el carácter "v" seguido de las primeras tres partes del número de versión (por ejemplo, "v1.0.1529").</span><span class="sxs-lookup"><span data-stu-id="7f369-109">The string passed as `pwszVersion` must start with the character "v" followed by the first three parts of the version number (for example, "v1.0.1529").</span></span>  
  
 <span data-ttu-id="7f369-110">Algunas versiones de CLR se instalan con una instrucción de directiva que especifica la compatibilidad con versiones anteriores de CLR.</span><span class="sxs-lookup"><span data-stu-id="7f369-110">Some versions of the CLR are installed with a policy statement that specifies compatibility with previous versions of the CLR.</span></span> <span data-ttu-id="7f369-111">De forma predeterminada, el proceso intermedio ("shim") de inicio evalúa `pwszVersion` con las instrucciones de directiva y carga la versión más reciente del runtime compatible con la versión solicitada.</span><span class="sxs-lookup"><span data-stu-id="7f369-111">By default, the startup shim evaluates `pwszVersion` against policy statements and loads the latest version of the runtime that is compatible with the version being requested.</span></span> <span data-ttu-id="7f369-112">Un host puede hacer que el proceso intermedio ("shim") omita la evaluación de directivas y cargue exactamente la versión especificada en `pwszVersion`, pasando el valor STARTUP_LOADER_SAFEMODE para el parámetro `startupFlags`.</span><span class="sxs-lookup"><span data-stu-id="7f369-112">A host can force the shim to skip policy evaluation and load the exact version specified in `pwszVersion` by passing a value of STARTUP_LOADER_SAFEMODE for the `startupFlags` parameter.</span></span>  
  
 <span data-ttu-id="7f369-113">Si `pwszVersion` es `null,` el método no carga ninguna versión de CLR.</span><span class="sxs-lookup"><span data-stu-id="7f369-113">If `pwszVersion` is `null,` the method does not load any version of the CLR.</span></span> <span data-ttu-id="7f369-114">En su lugar, devuelve CLR_E_SHIM_RUNTIMELOAD, que indica que no se cargó el runtime.</span><span class="sxs-lookup"><span data-stu-id="7f369-114">Instead, it returns CLR_E_SHIM_RUNTIMELOAD, which indicates that it failed to load the runtime.</span></span>  
  
 `pwszBuildFlavor`  
 <span data-ttu-id="7f369-115">[in] Cadena que especifica si se debe cargar la compilación de CLR para servidor o para estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="7f369-115">[in] A string that specifies whether to load the server or the workstation build of the CLR.</span></span> <span data-ttu-id="7f369-116">Los valores válidos son `svr` y `wks`.</span><span class="sxs-lookup"><span data-stu-id="7f369-116">Valid values are `svr` and `wks`.</span></span> <span data-ttu-id="7f369-117">La compilación para servidor está optimizada para aprovechar las ventajas que aportan varios procesadores al realizar recolecciones de elementos no utilizados, mientras que la compilación para estación de trabajo está optimizada para aplicaciones cliente que se ejecutan en equipos con un solo procesador.</span><span class="sxs-lookup"><span data-stu-id="7f369-117">The server build is optimized to take advantage of multiple processors for garbage collections, and the workstation build is optimized for client applications running on a single-processor machine.</span></span>  
  
 <span data-ttu-id="7f369-118">Si `pwszBuildFlavor` se establece en null, se cargará la compilación para estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="7f369-118">If `pwszBuildFlavor` is set to null, the workstation build is loaded.</span></span> <span data-ttu-id="7f369-119">Cuando se ejecuta en un equipo con un solo procesador, siempre se carga con la compilación de la estación de trabajo, incluso si `pwszBuildFlavor` está establecido en `svr`.</span><span class="sxs-lookup"><span data-stu-id="7f369-119">When running on a single-processor machine, the workstation build is always loaded, even if `pwszBuildFlavor` is set to `svr`.</span></span> <span data-ttu-id="7f369-120">Sin embargo, si `pwszBuildFlavor` está establecido en `svr` y se especifica una colección de elementos no utilizados simultánea (vea la descripción de la `startupFlags` parámetro), se carga la versión del servidor.</span><span class="sxs-lookup"><span data-stu-id="7f369-120">However, if `pwszBuildFlavor` is set to `svr` and concurrent garbage collection is specified (see the description of the `startupFlags` parameter), the server build is loaded.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7f369-121">No se admite la recolección de elementos no utilizados simultánea en aplicaciones en las que se ejecuta el emulador WOW64 x86 en sistemas de 64 bits y que implementan la arquitectura Intel Itanium (denominada anteriormente IA-64).</span><span class="sxs-lookup"><span data-stu-id="7f369-121">Concurrent garbage collection is not supported in applications running the WOW64 x86 emulator on 64-bit systems that implement the Intel Itanium architecture (formerly called IA-64).</span></span> <span data-ttu-id="7f369-122">Para obtener más información sobre el uso de WOW64 en sistemas de Windows de 64 bits, consulte [aplicaciones Running 32 bits](http://msdn.microsoft.com/library/windows/desktop/aa384249.aspx).</span><span class="sxs-lookup"><span data-stu-id="7f369-122">For more information about using WOW64 on 64-bit Windows systems, see [Running 32-bit Applications](http://msdn.microsoft.com/library/windows/desktop/aa384249.aspx).</span></span>  
  
 `pwszHostConfigFile`  
 <span data-ttu-id="7f369-123">[in] Nombre de un archivo de configuración de host que especifica la versión de CLR que se debe cargar.</span><span class="sxs-lookup"><span data-stu-id="7f369-123">[in] The name of a host configuration file that specifies the version of the CLR to load.</span></span> <span data-ttu-id="7f369-124">Si el nombre de archivo no incluye una ruta de acceso completa, se supone que este se encuentra en el mismo directorio que el ejecutable que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="7f369-124">If the file name does not include a fully qualified path, the file is assumed to be in the same directory as the executable that is making the call.</span></span>  
  
 `pReserved`  
 <span data-ttu-id="7f369-125">[in] Reservado para extensibilidad futura.</span><span class="sxs-lookup"><span data-stu-id="7f369-125">[in] Reserved for future extensibility.</span></span>  
  
 `startupFlags`  
 <span data-ttu-id="7f369-126">[in] Conjunto de marcas que controla la recolección de elementos no utilizados simultánea, el código neutral respecto al dominio y el comportamiento del parámetro `pwszVersion`.</span><span class="sxs-lookup"><span data-stu-id="7f369-126">[in] A set of flags that controls concurrent garbage collection, domain-neutral code, and the behavior of the `pwszVersion` parameter.</span></span> <span data-ttu-id="7f369-127">Si no se establece ninguna marca, el valor predeterminado es un dominio único.</span><span class="sxs-lookup"><span data-stu-id="7f369-127">The default is single domain if no flag is set.</span></span> <span data-ttu-id="7f369-128">Para obtener una lista de valores admitidos, consulte el [STARTUP_FLAGS (enumeración)](../../../../docs/framework/unmanaged-api/hosting/startup-flags-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="7f369-128">For a list of supported values, see the [STARTUP_FLAGS enumeration](../../../../docs/framework/unmanaged-api/hosting/startup-flags-enumeration.md).</span></span>  
  
 `rclsid`  
 <span data-ttu-id="7f369-129">[in] El `CLSID` de la coclase que implementa la [ICorRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md) o [ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="7f369-129">[in] The `CLSID` of the coclass that implements either the [ICorRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md) or the [ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md) interface.</span></span> <span data-ttu-id="7f369-130">Los valores admitidos son CLSID_CorRuntimeHost o CLSID_CLRRuntimeHost.</span><span class="sxs-lookup"><span data-stu-id="7f369-130">Supported values are CLSID_CorRuntimeHost or CLSID_CLRRuntimeHost.</span></span>  
  
 `riid`  
 <span data-ttu-id="7f369-131">[in] El `IID` de la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="7f369-131">[in] The `IID` of the interface you are requesting.</span></span> <span data-ttu-id="7f369-132">Los valores admitidos son IID_ICorRuntimeHost o IID_ICLRRuntimeHost.</span><span class="sxs-lookup"><span data-stu-id="7f369-132">Supported values are IID_ICorRuntimeHost or IID_ICLRRuntimeHost.</span></span>  
  
 `ppv`  
 <span data-ttu-id="7f369-133">[out] Puntero de interfaz a la versión del runtime que se cargó.</span><span class="sxs-lookup"><span data-stu-id="7f369-133">[out] An interface pointer to the version of the runtime that was loaded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f369-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f369-134">Requirements</span></span>  
 <span data-ttu-id="7f369-135">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7f369-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7f369-136">**Encabezado:** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="7f369-136">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="7f369-137">**Biblioteca:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7f369-137">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7f369-138">**Versiones de .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7f369-138">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f369-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f369-139">See Also</span></span>  
 [<span data-ttu-id="7f369-140">CorBindToCurrentRuntime (función)</span><span class="sxs-lookup"><span data-stu-id="7f369-140">CorBindToCurrentRuntime Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md)  
 [<span data-ttu-id="7f369-141">CorBindToRuntime (función)</span><span class="sxs-lookup"><span data-stu-id="7f369-141">CorBindToRuntime Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md)  
 [<span data-ttu-id="7f369-142">CorBindToRuntimeByCfg (función)</span><span class="sxs-lookup"><span data-stu-id="7f369-142">CorBindToRuntimeByCfg Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md)  
 [<span data-ttu-id="7f369-143">CorBindToRuntimeEx (función)</span><span class="sxs-lookup"><span data-stu-id="7f369-143">CorBindToRuntimeEx Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)  
 [<span data-ttu-id="7f369-144">ICorRuntimeHost (interfaz)</span><span class="sxs-lookup"><span data-stu-id="7f369-144">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)  
 [<span data-ttu-id="7f369-145">Funciones de hospedaje de CLR en desuso</span><span class="sxs-lookup"><span data-stu-id="7f369-145">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)