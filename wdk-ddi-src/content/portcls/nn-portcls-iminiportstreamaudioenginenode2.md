---
UID : NN:portcls.IMiniportStreamAudioEngineNode2
title : IMiniportStreamAudioEngineNode2
author : windows-driver-content
description : The IMiniportStreamAudioEngineNode2 interface allows an audio miniport driver to extend the capabilities of the IMiniportStreamAudioEngineNode interface.
old-location : audio\iminiportstreamaudioenginenode2.htm
old-project : audio
ms.assetid : 38888C17-31FC-47F4-A49B-A46A9DF962AF
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : PcUnregisterIoTimeout
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : interface
req.header : portcls.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 8.1
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IMiniportStreamAudioEngineNode2
req.alt-loc : Portcls.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Portcls.lib
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
---

# IMiniportStreamAudioEngineNode2 interface

The <b>IMiniportStreamAudioEngineNode2</b> interface allows an audio miniport driver to extend the capabilities of the <a href="..\portcls\nn-portcls-iminiportstreamaudioenginenode.md">IMiniportStreamAudioEngineNode</a> interface.

## Methods

<p>The <b>IMiniportStreamAudioEngineNode2</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [portcls.IMiniportStreamAudioEngineNode2.SetStreamCurrentWritePositionForLastBuffer](nf-portcls-iminiportstreamaudioenginenode2-setstreamcurrentwritepositionforlastbuffer.md) | Sets the current cursor position in the last audio data stream that was written to the audio buffer. |

## Remarks



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum UMDF version** |  |
| **Header** | portcls.h |
| **DLL** |  |