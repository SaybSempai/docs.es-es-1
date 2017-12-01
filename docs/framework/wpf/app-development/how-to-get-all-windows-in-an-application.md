---
title: "Cómo: obtener todas las ventanas en una aplicación"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords: window objects [WPF], getting
ms.assetid: f120f06e-993b-4a97-9657-af0d1986981f
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 8577817f62ece1465f9c7577f3e1b7ff5ecefe44
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/22/2017
---
# <a name="how-to-get-all-windows-in-an-application"></a><span data-ttu-id="6003d-102">Cómo: obtener todas las ventanas en una aplicación</span><span class="sxs-lookup"><span data-stu-id="6003d-102">How to: Get all Windows in an Application</span></span>
<span data-ttu-id="6003d-103">Este ejemplo muestra cómo obtener todos los <xref:System.Windows.Window> objetos en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="6003d-103">This example shows how to get all <xref:System.Windows.Window> objects in an application.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6003d-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6003d-104">Example</span></span>  
 <span data-ttu-id="6003d-105">Cada crea una instancia <xref:System.Windows.Window> objeto, si es visible o no, se agrega automáticamente a una colección de referencias de ventana que está administrado por <xref:System.Windows.Application>y está expuesto desde <xref:System.Windows.Application.Windows%2A>.</span><span class="sxs-lookup"><span data-stu-id="6003d-105">Every instantiated <xref:System.Windows.Window> object, whether visible or not, is automatically added to a collection of window references that is managed by <xref:System.Windows.Application>, and exposed from <xref:System.Windows.Application.Windows%2A>.</span></span>  
  
 <span data-ttu-id="6003d-106">Puede enumerar <xref:System.Windows.Application.Windows%2A> para obtener todas las instancias de windows con el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="6003d-106">You can enumerate <xref:System.Windows.Application.Windows%2A> to get all instantiated windows using the following code:</span></span>  
  
 [!code-csharp[HOWTOWindowManagementSnippets#GetAllWindows](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/CustomWindow.xaml.cs#getallwindows)]
 [!code-vb[HOWTOWindowManagementSnippets#GetAllWindows](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/customwindow.xaml.vb#getallwindows)]