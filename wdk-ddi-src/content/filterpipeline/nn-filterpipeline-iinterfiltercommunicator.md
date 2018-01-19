---
UID : NN:filterpipeline.IInterFilterCommunicator
title : IInterFilterCommunicator
author : windows-driver-content
description : The IInterFilterCommunicator interface is implemented in an object that resides in the PrintFilterPipelineSvc service and is made available to filters through methods in the IPrintPipelineFilter interface.
old-location : print\iinterfiltercommunicator.htm
old-project : print
ms.assetid : 777da1db-5522-48fc-bf35-8e6bf9203d6a
ms.author : windowsdriverdev
ms.date : 1/8/2018
ms.keywords : IXpsPartIterator, IXpsPartIterator::Reset, Reset
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : interface
req.header : filterpipeline.h
req.include-header : Filterpipeline.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IInterFilterCommunicator
req.alt-loc : filterpipeline.h
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
req.typenames : EXpsFontRestriction
---

# IInterFilterCommunicator interface

The <b>IInterFilterCommunicator</b> interface is implemented in an object that resides in the PrintFilterPipelineSvc service and is made available to filters through methods in the <a href="..\filterpipeline\nn-filterpipeline-iprintpipelinefilter.md">IPrintPipelineFilter</a> interface.<b>IInterFilterCommunicator</b> inherits from the <b>IUnknown</b> interface.

## Methods

<p>The <b>IInterFilterCommunicator</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [filterpipeline.IInterFilterCommunicator.RequestReader](nf-filterpipeline-iinterfiltercommunicator-requestreader.md) | The RequestReader method retrieves the reader interface for an IInterFilterCommunicator object. |
| [filterpipeline.IInterFilterCommunicator.RequestWriter](nf-filterpipeline-iinterfiltercommunicator-requestwriter.md) | The RequestWriter method retrieves the writer interface for an IInterFilterCommunicator object. |

## Remarks



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum UMDF version** |  |
| **Header** | filterpipeline.h (include Filterpipeline.h) |
| **DLL** |  |