---
title: "Campos explícitos: palabra clave val (F#)"
description: "Obtenga información sobre F # 'val' palabra clave, que se utiliza para declarar una ubicación para almacenar un valor en un tipo de clase o estructura sin inicializar el tipo."
keywords: "visual f#, f#, programación funcional"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 3bdbc745-436b-407f-bf54-5d11ca829cd0
ms.openlocfilehash: cee53a48f08aec89b0bdd40189ed331cadee877d
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="explicit-fields-the-val-keyword"></a><span data-ttu-id="31337-104">Campos explícitos: palabra clave val</span><span class="sxs-lookup"><span data-stu-id="31337-104">Explicit Fields: The val Keyword</span></span>

<span data-ttu-id="31337-105">La palabra clave `val` se usa para declarar una ubicación para almacenar un valor en un tipo de clase o estructura sin inicializarlo.</span><span class="sxs-lookup"><span data-stu-id="31337-105">The `val` keyword is used to declare a location to store a value in a class or structure type, without initializing it.</span></span> <span data-ttu-id="31337-106">Ubicaciones de almacenamiento que se declaran de esta manera se denominan *campos explícitos*.</span><span class="sxs-lookup"><span data-stu-id="31337-106">Storage locations declared in this manner are called *explicit fields*.</span></span> <span data-ttu-id="31337-107">Otra manera de usar la palabra clave `val` es conjuntamente con la palabra clave `member` para declarar una propiedad implementada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="31337-107">Another use of the `val` keyword is in conjunction with the `member` keyword to declare an auto-implemented property.</span></span> <span data-ttu-id="31337-108">Para obtener más información sobre las propiedades implementadas automáticamente, vea [propiedades](properties.md).</span><span class="sxs-lookup"><span data-stu-id="31337-108">For more information on auto-implemented properties, see [Properties](properties.md).</span></span>


## <a name="syntax"></a><span data-ttu-id="31337-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31337-109">Syntax</span></span>

```fsharp
val [ mutable ] [ access-modifier ] field-name : type-name
```

## <a name="remarks"></a><span data-ttu-id="31337-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31337-110">Remarks</span></span>
<span data-ttu-id="31337-111">La forma más habitual de definir campos en un tipo de clase o estructura es usar un enlace `let`.</span><span class="sxs-lookup"><span data-stu-id="31337-111">The usual way to define fields in a class or structure type is to use a `let` binding.</span></span> <span data-ttu-id="31337-112">Sin embargo, los enlaces `let` deben inicializarse como parte del constructor de clase, lo que no siempre es posible, necesario o deseable.</span><span class="sxs-lookup"><span data-stu-id="31337-112">However, `let` bindings must be initialized as part of the class constructor, which is not always possible, necessary, or desirable.</span></span> <span data-ttu-id="31337-113">Puede usar la palabra clave `val` cuando quiera un campo que no se haya inicializado.</span><span class="sxs-lookup"><span data-stu-id="31337-113">You can use the `val` keyword when you want a field that is uninitialized.</span></span>

<span data-ttu-id="31337-114">Los campos explícitos pueden ser estáticos o no estáticos.</span><span class="sxs-lookup"><span data-stu-id="31337-114">Explicit fields can be static or non-static.</span></span> <span data-ttu-id="31337-115">El *modificador de acceso* puede ser `public`, `private`, o `internal`.</span><span class="sxs-lookup"><span data-stu-id="31337-115">The *access-modifier* can be `public`, `private`, or `internal`.</span></span> <span data-ttu-id="31337-116">De forma predeterminada, los campos explícitos son públicos.</span><span class="sxs-lookup"><span data-stu-id="31337-116">By default, explicit fields are public.</span></span> <span data-ttu-id="31337-117">Esto difiere de los enlaces `let` de las clases, que siempre son privados.</span><span class="sxs-lookup"><span data-stu-id="31337-117">This differs from `let` bindings in classes, which are always private.</span></span>

<span data-ttu-id="31337-118">El [DefaultValue](https://msdn.microsoft.com/library/a3a3307b-8c05-441e-b109-245511614d58) atributo es necesario en los campos explícitos en tipos de clase que tienen un constructor primario.</span><span class="sxs-lookup"><span data-stu-id="31337-118">The [DefaultValue](https://msdn.microsoft.com/library/a3a3307b-8c05-441e-b109-245511614d58) attribute is required on explicit fields in class types that have a primary constructor.</span></span> <span data-ttu-id="31337-119">Este atributo especifica que el campo se inicializa en cero.</span><span class="sxs-lookup"><span data-stu-id="31337-119">This attribute specifies that the field is initialized to zero.</span></span> <span data-ttu-id="31337-120">El tipo del campo debe admitir la inicialización en cero.</span><span class="sxs-lookup"><span data-stu-id="31337-120">The type of the field must support zero-initialization.</span></span> <span data-ttu-id="31337-121">Los tipos que admiten la inicialización en cero son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="31337-121">A type supports zero-initialization if it is one of the following:</span></span>

- <span data-ttu-id="31337-122">Un tipo primitivo que tenga un valor de cero.</span><span class="sxs-lookup"><span data-stu-id="31337-122">A primitive type that has a zero value.</span></span>

- <span data-ttu-id="31337-123">Un tipo que admita un valor nulo, ya sea como valor normal, como valor anormal o como representación de un valor.</span><span class="sxs-lookup"><span data-stu-id="31337-123">A type that supports a null value, either as a normal value, as an abnormal value, or as a representation of a value.</span></span> <span data-ttu-id="31337-124">Esto incluye clases, tuplas, registros, funciones, interfaces, tipos de referencia .NET, el tipo `unit` y tipos de unión discriminada.</span><span class="sxs-lookup"><span data-stu-id="31337-124">This includes classes, tuples, records, functions, interfaces, .NET reference types, the `unit` type, and discriminated union types.</span></span>

- <span data-ttu-id="31337-125">Un tipo de valor. NET.</span><span class="sxs-lookup"><span data-stu-id="31337-125">A .NET value type.</span></span>

- <span data-ttu-id="31337-126">Una estructura cuyos campos admitan el valor cero predeterminado.</span><span class="sxs-lookup"><span data-stu-id="31337-126">A structure whose fields all support a default zero value.</span></span>


<span data-ttu-id="31337-127">Por ejemplo, un campo inmutable denominado `someField` tiene un campo de respaldo en la representación compilada de .NET con el nombre `someField@` y el usuario accede al valor almacenado con una propiedad denominada `someField`.</span><span class="sxs-lookup"><span data-stu-id="31337-127">For example, an immutable field called `someField` has a backing field in the .NET compiled representation with the name `someField@`, and you access the stored value using a property named `someField`.</span></span>

<span data-ttu-id="31337-128">Para un campo mutable, la representación compilada de .NET es un campo .NET.</span><span class="sxs-lookup"><span data-stu-id="31337-128">For a mutable field, the .NET compiled representation is a .NET field.</span></span>


>[!WARNING] 
<span data-ttu-id="31337-129">`Note`El espacio de nombres de .NET Framework `System.ComponentModel` contiene un atributo que tiene el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="31337-129">`Note` The .NET Framework namespace `System.ComponentModel` contains an attribute that has the same name.</span></span> <span data-ttu-id="31337-130">Para obtener más información sobre el atributo, vea `System.ComponentModel.DefaultValueAttribute`.</span><span class="sxs-lookup"><span data-stu-id="31337-130">For information about this attribute, see `System.ComponentModel.DefaultValueAttribute`.</span></span>


<span data-ttu-id="31337-131">El código siguiente muestra el uso de campos explícitos y, para la comparación, un `let` de enlace en una clase que tiene un constructor primario.</span><span class="sxs-lookup"><span data-stu-id="31337-131">The following code shows the use of explicit fields and, for comparison, a `let` binding in a class that has a primary constructor.</span></span> <span data-ttu-id="31337-132">Tenga en cuenta que el campo enlazado a `let``myInt1` es privado.</span><span class="sxs-lookup"><span data-stu-id="31337-132">Note that the `let`-bound field `myInt1` is private.</span></span> <span data-ttu-id="31337-133">Si se hace referencia al campo enlazado a `let` `myInt1` desde un método de miembro, el identificador propio `this` no es necesario.</span><span class="sxs-lookup"><span data-stu-id="31337-133">When the `let`-bound field `myInt1` is referenced from a member method, the self identifier `this` is not required.</span></span> <span data-ttu-id="31337-134">Pero si hace referencia a los campos explícitos `myInt2` y `myString`, se requiere el identificador propio.</span><span class="sxs-lookup"><span data-stu-id="31337-134">But when you are referencing the explicit fields `myInt2` and `myString`, the self identifier is required.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet6701.fs)]

<span data-ttu-id="31337-135">La salida es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="31337-135">The output is as follows:</span></span>

```
11 12 abc
30 def
```

<span data-ttu-id="31337-136">En el código siguiente se muestra el uso de campos explícitos en una clase que no tiene constructor primario.</span><span class="sxs-lookup"><span data-stu-id="31337-136">The following code shows the use of explicit fields in a class that does not have a primary constructor.</span></span> <span data-ttu-id="31337-137">En este caso, el atributo `DefaultValue` no es necesario, pero todos los campos deben estar inicializados en los constructores definidos para el tipo.</span><span class="sxs-lookup"><span data-stu-id="31337-137">In this case, the `DefaultValue` attribute is not required, but all the fields must be initialized in the constructors that are defined for the type.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet6702.fs)]

<span data-ttu-id="31337-138">El resultado es `35 22`</span><span class="sxs-lookup"><span data-stu-id="31337-138">The output is `35 22`.</span></span>

<span data-ttu-id="31337-139">En el código siguiente se muestra el uso de campos explícitos en una estructura.</span><span class="sxs-lookup"><span data-stu-id="31337-139">The following code shows the use of explicit fields in a structure.</span></span> <span data-ttu-id="31337-140">Como una estructura es un tipo de valor, automáticamente tiene un constructor predeterminado que establece los valores de sus campos en cero.</span><span class="sxs-lookup"><span data-stu-id="31337-140">Because a structure is a value type, it automatically has a default constructor that sets the values of its fields to zero.</span></span> <span data-ttu-id="31337-141">Por lo tanto, el atributo `DefaultValue` no es necesario.</span><span class="sxs-lookup"><span data-stu-id="31337-141">Therefore, the `DefaultValue` attribute is not required.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet6703.fs)]

<span data-ttu-id="31337-142">El resultado es `11 xyz`</span><span class="sxs-lookup"><span data-stu-id="31337-142">The output is `11 xyz`.</span></span>

<span data-ttu-id="31337-143">Los campos explícitos no están pensados para un uso rutinario.</span><span class="sxs-lookup"><span data-stu-id="31337-143">Explicit fields are not intended for routine use.</span></span> <span data-ttu-id="31337-144">En general, siempre que sea posible debe usar un enlace `let` en una clase en lugar de un campo explícito.</span><span class="sxs-lookup"><span data-stu-id="31337-144">In general, when possible you should use a `let` binding in a class instead of an explicit field.</span></span> <span data-ttu-id="31337-145">Los campos explícitos son útiles en determinados escenarios de interoperabilidad, como cuando se necesita definir una estructura que se usará en una llamada de invocación a una plataforma API nativa o en escenarios de interoperabilidad COM.</span><span class="sxs-lookup"><span data-stu-id="31337-145">Explicit fields are useful in certain interoperability scenarios, such as when you need to define a structure that will be used in a platform invoke call to a native API, or in COM interop scenarios.</span></span> <span data-ttu-id="31337-146">Para obtener más información, consulte [funciones externas](../functions/external-functions.md).</span><span class="sxs-lookup"><span data-stu-id="31337-146">For more information, see [External Functions](../functions/external-functions.md).</span></span> <span data-ttu-id="31337-147">Otra situación en la que podría ser necesario un campo explícito es cuando se trabaja con un generador de código F # que emite clases sin un constructor primario.</span><span class="sxs-lookup"><span data-stu-id="31337-147">Another situation in which an explicit field might be necessary is when you are working with an F# code generator which emits classes without a primary constructor.</span></span> <span data-ttu-id="31337-148">Los campos explícitos también son útiles para las variables de subproceso estático o construcciones similares.</span><span class="sxs-lookup"><span data-stu-id="31337-148">Explicit fields are also useful for thread-static variables or similar constructs.</span></span> <span data-ttu-id="31337-149">Para obtener más información, consulta `System.ThreadStaticAttribute`.</span><span class="sxs-lookup"><span data-stu-id="31337-149">For more information, see `System.ThreadStaticAttribute`.</span></span>

<span data-ttu-id="31337-150">Cuando las palabras clave `member val` aparecen juntas en una definición de tipo, se trata de la definición de una propiedad implementada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="31337-150">When the keywords `member val` appear together in a type definition, it is a definition of an automatically implemented property.</span></span> <span data-ttu-id="31337-151">Para obtener más información, consulte [propiedades](properties.md).</span><span class="sxs-lookup"><span data-stu-id="31337-151">For more information, see [Properties](properties.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="31337-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="31337-152">See Also</span></span>
[<span data-ttu-id="31337-153">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31337-153">Properties</span></span>](properties.md)

[<span data-ttu-id="31337-154">Miembros</span><span class="sxs-lookup"><span data-stu-id="31337-154">Members</span></span>](index.md)

<span data-ttu-id="31337-155">[`let` Bindings in Classes](let-bindings-in-classes.md) (Enlaces `let` en clases)</span><span class="sxs-lookup"><span data-stu-id="31337-155">[`let` Bindings in Classes](let-bindings-in-classes.md)</span></span>