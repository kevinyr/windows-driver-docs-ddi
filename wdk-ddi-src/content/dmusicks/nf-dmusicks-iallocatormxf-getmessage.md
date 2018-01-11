---
UID: NF.dmusicks.IAllocatorMXF.GetMessage
title: IAllocatorMXF::GetMessage method
author: windows-driver-content
description: The GetMessage method serves as the retrieval point for any DirectMusic kernel-mode component that utilizes the port driver's allocator to reuse DMUS_KERNEL_EVENT structures.
old-location: audio\iallocatormxf_getmessage.htm
old-project: audio
ms.assetid: d5b56926-bcfb-4411-b24d-cc0758852510
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IAllocatorMXF, IAllocatorMXF::GetMessage, GetMessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dmusicks.h
req.include-header: Dmusicks.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IAllocatorMXF.GetMessage
req.alt-loc: dmusicks.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: <=DISPATCH_LEVEL
---

# IAllocatorMXF::GetMessage method



## -description
The <code>GetMessage</code> method serves as the retrieval point for any DirectMusic kernel-mode component that utilizes the port driver's allocator to reuse <a href="audio.dmus_kernel_event">DMUS_KERNEL_EVENT</a> structures.



## -syntax

````
NTSTATUS GetMessage(
  [out] PDMUS_KERNEL_EVENT *ppDMKEvt
);
````


## -parameters

### -param ppDMKEvt [out]

Output pointer for the MIDI event. This parameter points to a caller-allocated pointer variable into which the method writes a pointer to the event structure being retrieved from the allocator. The structure itself is empty (zeroed by the allocator).


## -returns
<code>GetMessage</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code.


## -remarks
The miniport driver uses the <code>GetMessage</code> method to retrieve event structures for MIDI rendering and capture. This method retrieves <a href="audio.dmus_kernel_event">DMUS_KERNEL_EVENT</a> structures from the same pool that <a href="audio.imxf_putmessage">IMXF::PutMessage</a> puts them into when it discards them to the allocator.

In the case of a MIDI capture stream, the port driver retrieves capture events from the miniport driver when prompted by the usual Service DPC.

For more information about the allocator, see <a href="https://msdn.microsoft.com/8f263288-2f79-4f1d-b740-d78d40f47b32">Allocator</a>.


## -requirements
<table>
<tr>
<th width="30%">
Target platform

</th>
<td width="70%">
<dl>
<dt>Desktop</dt>
</dl>
</td>
</tr>
<tr>
<th width="30%">
Header

</th>
<td width="70%">
<dl>
<dt>Dmusicks.h (include Dmusicks.h)</dt>
</dl>
</td>
</tr>
<tr>
<th width="30%">
IRQL

</th>
<td width="70%">
&lt;=DISPATCH_LEVEL

</td>
</tr>
</table>

## -see-also
<dl>
<dt>
<a href="..\dmusicks\nn-dmusicks-iallocatormxf~r1.md">IAllocatorMXF</a>
</dt>
<dt>
<a href="audio.dmus_kernel_event">DMUS_KERNEL_EVENT</a>
</dt>
<dt>
<a href="audio.imxf_putmessage">IMXF::PutMessage</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [audio\audio]:%20IAllocatorMXF::GetMessage method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
