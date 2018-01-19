---
UID : NN:dbgeng.IDebugSymbols5
title : IDebugSymbols5
author : windows-driver-content
description : This interface supports using index values for the current frame.
old-location : debugger\idebugsymbols5.htm
old-project : debugger
ms.assetid : 0D239C0E-96C8-49F9-BDFD-182F3F7C3976
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : IDebugSystemObjects4, IDebugSystemObjects4::SetImplicitThreadDataOffset, SetImplicitThreadDataOffset
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : interface
req.header : dbgeng.h
req.include-header : Dbgeng.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IDebugSymbols5
req.alt-loc : Dbgeng.h
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
req.typenames : "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugSymbols5 interface

This interface supports using index values for the current frame.

## Methods

<p>The <b>IDebugSymbols5</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [dbgeng.IDebugSymbols5.GetCurrentScopeFrameIndexEx](nf-dbgeng-idebugsymbols5-getcurrentscopeframeindexex.md) | Gets the index of the current frame. |
| [dbgeng.IDebugSymbols5.GetFieldOffset](nf-dbgeng-idebugsymbols5-getfieldoffset.md) | The GetFieldOffset function returns the offset of a member from the beginning of a structure. |
| [dbgeng.IDebugSymbols5.SetScopeFrameByIndexEx](nf-dbgeng-idebugsymbols5-setscopeframebyindexex.md) | Sets the current frame by using an index. |

## Remarks



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum UMDF version** |  |
| **Header** | dbgeng.h (include Dbgeng.h) |
| **DLL** |  |