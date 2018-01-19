---
UID : NC:d3dkmddi.DXGKDDI_MAPCPUHOSTAPERTURE
title : DXGKDDI_MAPCPUHOSTAPERTURE
author : windows-driver-content
description : DxgkDdiMapCpuHostAperture is called to map an allocation that is resident in a local memory segment into the CPU host aperture in order to make it visible to the CPU.
old-location : display\dxgkddimapcpuhostaperture.htm
old-project : display
ms.assetid : 78729B9A-A9FA-4D1E-8D30-3FFD61B1A7D3
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DD_MULTISAMPLEQUALITYLEVELSDATA, DD_MULTISAMPLEQUALITYLEVELSDATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3dkmddi.h
req.include-header : D3dkmddi.h
req.target-type : Desktop
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DxgkDdiMapCpuHostAperture
req.alt-loc : d3dkmddi.h
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
req.typenames : DD_MULTISAMPLEQUALITYLEVELSDATA
---


# DXGKDDI_MAPCPUHOSTAPERTURE function
<b>DxgkDdiMapCpuHostAperture</b> is called to map an allocation that is resident in a local memory segment into the CPU host aperture in order to make it visible to the CPU.

## Syntax

```
DXGKDDI_MAPCPUHOSTAPERTURE DxgkddiMapcpuhostaperture;

NTSTATUS DxgkddiMapcpuhostaperture(
  IN_CONST_HANDLE hAdapter,
  IN_CONST_PDXGKARG_MAPCPUHOSTAPERTURE pArgs
)
{...}
```

## Parameters

`hAdapter`

A handle to the display adapter.

`pArgs`




## Return Value

Returns <b>STATUS_SUCCESS</b> if it succeeds. Otherwise, it returns one of the error codes defined in <b>Ntstatus.h</b>.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h (include D3dkmddi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |