---
UID : NN:dbgeng.IDebugClient
title : IDebugClient
author : windows-driver-content
description : IDebugClient interface
old-location : debugger\idebugclient.htm
old-project : debugger
ms.assetid : 2e47f7ae-2017-4f05-9a06-6c09bb401e21
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
req.alt-api : IDebugClient,IDebugClient.GetOutputWidth,IDebugClient.SetOutputWidth,IDebugClient.GetOutputLinePrefix,IDebugClient.SetOutputLinePrefix
req.alt-loc : dbgeng.h
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

# IDebugClient interface



## Methods

<p>The <b>IDebugClient</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [dbgeng.IDebugClient.GetOutputLinePrefix](nf-dbgeng-idebugclient-getoutputlineprefix.md) | Gets the prefix used for multiple lines of output. |
| [dbgeng.IDebugClient.GetOutputWidth](nf-dbgeng-idebugclient-getoutputwidth.md) | Gets the width of an output line for commands that produce formatted output. |
| [dbgeng.IDebugClient.SetOutputLinePrefix](nf-dbgeng-idebugclient-setoutputlineprefix.md) | Sets a prefix for multiple lines of output. |
| [dbgeng.IDebugClient.SetOutputWidth](nf-dbgeng-idebugclient-setoutputwidth.md) | Controls the width of an output line for commands that produce formatted output. |

## Remarks



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum UMDF version** |  |
| **Header** | dbgeng.h (include Dbgeng.h) |
| **DLL** |  |

    ## See Also

        <dl>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugclient2.md">IDebugClient2</a>
</dt>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugclient3.md">IDebugClient3</a>
</dt>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugclient4.md">IDebugClient4</a>
</dt>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugclient5.md">IDebugClient5</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugClient interface%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>