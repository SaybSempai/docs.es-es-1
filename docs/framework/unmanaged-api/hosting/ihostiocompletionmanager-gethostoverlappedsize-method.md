---
title: "IHostIoCompletionManager::GetHostOverlappedSize (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostIoCompletionManager.GetHostOverlappedSize
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostIoCompletionManager::GetHostOverlappedSize
helpviewer_keywords:
- IHostIoCompletionManager::GetHostOverlappedSize method [.NET Framework hosting]
- GetHostOverlappedSize method [.NET Framework hosting]
ms.assetid: 2902578b-d5e2-4f8d-a103-0c7b6dceda9e
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 6633e0271f29d44bb1d14495d80ffdf9868485a1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="ihostiocompletionmanagergethostoverlappedsize-method"></a><span data-ttu-id="b3706-102">IHostIoCompletionManager::GetHostOverlappedSize (Método)</span><span class="sxs-lookup"><span data-stu-id="b3706-102">IHostIoCompletionManager::GetHostOverlappedSize Method</span></span>
<span data-ttu-id="b3706-103">Obtiene el tamaño de los datos personalizados que el host pretende anexar a las solicitudes de E/S.</span><span class="sxs-lookup"><span data-stu-id="b3706-103">Gets the size of any custom data the host intends to append to I/O requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b3706-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3706-104">Syntax</span></span>  
  
```  
HRESULT GetHostOverlappedSize (  
    [out] DWORD *pcbSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b3706-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3706-105">Parameters</span></span>  
 `pcbSize`  
 <span data-ttu-id="b3706-106">[out] Un puntero al número de bytes que common language runtime (CLR) debe asignar además del tamaño de Win32 `OVERLAPPED` objeto.</span><span class="sxs-lookup"><span data-stu-id="b3706-106">[out] A pointer to the number of bytes that the common language runtime (CLR) should allocate in addition to the size of the Win32 `OVERLAPPED` object.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b3706-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3706-107">Return Value</span></span>  
  
|<span data-ttu-id="b3706-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b3706-108">HRESULT</span></span>|<span data-ttu-id="b3706-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3706-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b3706-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b3706-110">S_OK</span></span>|<span data-ttu-id="b3706-111">`GetHostOverlappedSize`se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="b3706-111">`GetHostOverlappedSize` returned successfully.</span></span>|  
|<span data-ttu-id="b3706-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b3706-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b3706-113">El CLR no se han cargado en un proceso o el CLR está en un estado en el que no se puede ejecutar código administrado o procesar la llamada correctamente.</span><span class="sxs-lookup"><span data-stu-id="b3706-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b3706-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b3706-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b3706-115">La llamada agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="b3706-115">The call timed out.</span></span>|  
|<span data-ttu-id="b3706-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b3706-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b3706-117">El llamador no posee el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="b3706-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b3706-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b3706-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b3706-119">Se canceló un evento mientras un subproceso bloqueado o fibra esperó en él.</span><span class="sxs-lookup"><span data-stu-id="b3706-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b3706-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b3706-120">E_FAIL</span></span>|<span data-ttu-id="b3706-121">Se ha producido un error catastrófico desconocido.</span><span class="sxs-lookup"><span data-stu-id="b3706-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b3706-122">Cuando un método devuelve E_FAIL, CLR ya no es utilizable dentro del proceso.</span><span class="sxs-lookup"><span data-stu-id="b3706-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b3706-123">Las llamadas posteriores a métodos de hospedaje devuelven HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="b3706-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b3706-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3706-124">Remarks</span></span>  
 <span data-ttu-id="b3706-125">Todas las llamadas de E/S asincrónicas a las API de plataforma de Windows toman Win32 `OVERLAPPED` object, que proporciona información como la posición del puntero de archivo.</span><span class="sxs-lookup"><span data-stu-id="b3706-125">All asynchronous I/O calls to Windows Platform APIs take a Win32 `OVERLAPPED` object, which provides information such as the file pointer position.</span></span> <span data-ttu-id="b3706-126">Para mantener el estado, las aplicaciones que hacen llamadas de E/S asincrónicas normalmente agregan datos personalizados a la estructura.</span><span class="sxs-lookup"><span data-stu-id="b3706-126">To maintain state, applications that make asynchronous I/O calls typically add custom data to the structure.</span></span> <span data-ttu-id="b3706-127">`GetHostOverlappedSize`y [IHostIoCompletionManager:: InitializeHostOverlapped](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-initializehostoverlapped-method.md) proporcionan una oportunidad para que el host de incluir dichos datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="b3706-127">`GetHostOverlappedSize` and [IHostIoCompletionManager::InitializeHostOverlapped](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-initializehostoverlapped-method.md) provide an opportunity for the host to include such custom data.</span></span>  
  
 <span data-ttu-id="b3706-128">CLR llama el `GetHostOverlappedSize` método para determinar el tamaño de los datos personalizados que el host pretende anexar a la `OVERLAPPED` objeto.</span><span class="sxs-lookup"><span data-stu-id="b3706-128">The CLR calls the `GetHostOverlappedSize` method to determine the size of the custom data that the host intends to append to the `OVERLAPPED` object.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b3706-129">`GetHostOverlappedSize`se llama solo una vez.</span><span class="sxs-lookup"><span data-stu-id="b3706-129">`GetHostOverlappedSize` is called only once.</span></span> <span data-ttu-id="b3706-130">Datos personalizados del host deben tener el mismo tamaño para cada solicitud de E/S.</span><span class="sxs-lookup"><span data-stu-id="b3706-130">The host's custom data must be the same size for every I/O request.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="b3706-131">El tamaño de la `OVERLAPPED` propio objeto no se incluye en el valor de `pcbSize`.</span><span class="sxs-lookup"><span data-stu-id="b3706-131">The size of the `OVERLAPPED` object itself is not included in the value of `pcbSize`.</span></span>  
  
 <span data-ttu-id="b3706-132">Para obtener más información sobre la `OVERLAPPED` de la estructura, consulte la documentación de la plataforma de Windows.</span><span class="sxs-lookup"><span data-stu-id="b3706-132">For more information about the `OVERLAPPED` structure, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b3706-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3706-133">Requirements</span></span>  
 <span data-ttu-id="b3706-134">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b3706-134">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b3706-135">**Encabezado:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b3706-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b3706-136">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b3706-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b3706-137">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b3706-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3706-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3706-138">See Also</span></span>  
 <xref:System.Threading.NativeOverlapped>  
 [<span data-ttu-id="b3706-139">ICLRIoCompletionManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="b3706-139">ICLRIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md)  
 [<span data-ttu-id="b3706-140">IHostIoCompletionManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="b3706-140">IHostIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)