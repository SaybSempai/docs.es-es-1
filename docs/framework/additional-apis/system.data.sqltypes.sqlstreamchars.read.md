---
title: Método SqlStreamChars.Read (Char [], Int32, Int32) (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Read
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: da891ac1fcff0247a690770665ef1f3e487497b8
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/07/2019
ms.locfileid: "55825373"
---
# <a name="sqlstreamcharsreadchar-int32-int32-method"></a>SqlStreamChars.Read(Char[], Int32, Int32) Method

Cuando se invalida en una clase derivada, lee el siguiente conjunto de caracteres del flujo de entrada. El ensamblado que contiene este método tiene una relación de confianza con SQLAccess.dll. Está pensado para su uso con SQL Server. Para otras bases de datos, utilice el mecanismo de hospedaje proporcionado por esa base de datos.

```csharp
public abstract int Read (char[] buffer, int offset, int count);
```

## <a name="parameters"></a>Parámetros

`buffer`\
Una matriz de caracteres para leer.

`offset`\
Un desplazamiento con respecto al origen.

`count`\
El número de caracteres que leer en la secuencia actual.

## <a name="returns"></a>Valores devueltos

<xref:System.Int32>\
Número total de caracteres leídos en el búfer.

## <a name="remarks"></a>Comentarios

> [!WARNING]
> El `SqlStreamChars.Read` método es privado y no está pensado para usarse directamente en el código.
>
> Microsoft no admite el uso de este campo en una aplicación de producción bajo ninguna circunstancia.

## <a name="requirements"></a>Requisitos

**Espacio de nombres:** <xref:System.Data.SqlTypes>

**Ensamblado:** System.Data (en System.Data.dll)

**Versiones de .NET framework:** Disponible desde la versión 2.0.