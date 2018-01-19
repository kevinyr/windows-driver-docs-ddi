---
UID : NE:d3d12umddi.D3D12DDI_VIDEO_SCALE_SUPPORT_FLAGS_0022
title : D3D12DDI_VIDEO_SCALE_SUPPORT_FLAGS_0022
author : windows-driver-content
description : Contains the options for video scale support.
old-location : display\d3d12ddi_video_scale_support_flags.htm
old-project : display
ms.assetid : A0E1AA43-FE1A-4754-B8E6-BFE87CA810E2
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D12DDI_VIDEO_SCALE_SUPPORT_FLAGS_0022, D3D12DDI_VIDEO_SCALE_SUPPORT_FLAGS_0022
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3d12umddi.h
req.include-header : D3d12umddi.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3D12DDI_VIDEO_SCALE_SUPPORT_FLAGS_0022
req.alt-loc : D3d12umddi.h
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
req.typenames : D3D12DDI_VIDEO_SCALE_SUPPORT_FLAGS_0022
---

# D3D12DDI_VIDEO_SCALE_SUPPORT_FLAGS_0022 Enumeration
Contains the options for video scale support.

## Syntax
````
typedef enum D3D12DDI_VIDEO_SCALE_SUPPORT_FLAGS_0022 { 
  D3D12DDI_VIDEO_SCALE_SUPPORT_FLAG_0020_NONE                  = 0x0,
  D3D12DDI_VIDEO_SCALE_SUPPORT_FLAG_0022_POW2_ONLY             = 0x1,
  D3D12DDI_VIDEO_SCALE_SUPPORT_FLAG_0022_EVEN_DIMENSIONS_ONLY  = 0x2
} D3D12DDI_VIDEO_SCALE_SUPPORT_FLAGS_0022;
````

## Constants

<table>

<tr>
<td>D3D12DDI_VIDEO_SCALE_SUPPORT_FLAG_0022_EVEN_DIMENSIONS_ONLY</td>
<td>The scaler supports only output sizes that have even output dimensions.</td>
</tr>

<tr>
<td>D3D12DDI_VIDEO_SCALE_SUPPORT_FLAG_0022_POW2_ONLY</td>
<td>The scaler supports only output sizes at a pow2 scale factors within the range.  The x and y scale factors must be the same for both dimensions when this flag is set.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d12umddi.h (include D3d12umddi.h) |