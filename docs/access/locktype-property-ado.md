---
title: "LockType Property (ADO)"
 
 
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
  
localization_priority: Normal
ms.assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f

---

# LockType Property (ADO)

Indicates the type of locks placed on records during editing.
  
## Settings and Return Values

Sets or returns a [LockTypeEnum](locktypeenum.md) value. The default value is **adLockReadOnly**. 
  
## Remarks

Set the **LockType** property before opening a [Recordset](recordset-object-ado.md) to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object. 
  
Providers may not support all lock types. If a provider cannot support the requested **LockType** setting, it will substitute another type of locking. To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**. 
  
The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **LockType** will be used instead. 
  
The **LockType** property is read/write when the **Recordset** is closed and read-only when it is open. 
  
 **Remote Data Service Usage** When used on a client-side Recordset object, the **LockType** property can only be set to **adLockBatchOptimistic**. 
  
