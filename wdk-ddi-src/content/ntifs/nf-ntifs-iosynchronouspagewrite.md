---
UID : NF:ntifs.IoSynchronousPageWrite
title : IoSynchronousPageWrite function
author : windows-driver-content
description : Reserved for system use.
old-location : ifsk\iosynchronouspagewrite.htm
old-project : ifsk
ms.assetid : 3d66b517-91cd-44f7-8dfe-853468c49352
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : IoSynchronousPageWrite
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntifs.h
req.include-header : Ntifs.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IoSynchronousPageWrite
req.alt-loc : ntifs.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : 
req.typenames : TOKEN_TYPE
---


# IoSynchronousPageWrite function
The <b>IoSynchronousPageWrite</b> routine is reserved for system use. See <a href="..\ntifs\nf-ntifs-cccopywrite.md">CcCopyWrite</a>, <a href="..\ntifs\nf-ntifs-ccpreparemdlwrite.md">CcPrepareMdlWrite</a>, and <a href="..\wdm\nf-wdm-iobuildsynchronousfsdrequest.md">IoBuildSynchronousFsdRequest</a>.

## Syntax

````
  IoSynchronousPageWrite(
    
);
````

## Parameters

`FileObject`



`MemoryDescriptorList`



`StartingOffset`



`Event`



`IoStatusBlock`




## Return Value

None


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntifs.h (include Ntifs.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |