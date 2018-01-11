---
UID: NF.dbgeng.IDebugSymbols3.GetSourceFileLineOffsets
title: IDebugSymbols3::GetSourceFileLineOffsets method
author: windows-driver-content
description: The GetSourceFileLineOffsets method maps each line in a source file to a location in the target's memory.
old-location: debugger\getsourcefilelineoffsets.htm
old-project: Debugger
ms.assetid: ace9e23a-d7ea-480a-8001-f25310adee22
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IDebugSymbols3, IDebugSymbols3::GetSourceFileLineOffsets, GetSourceFileLineOffsets
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IDebugSymbols.GetSourceFileLineOffsets,IDebugSymbols2.GetSourceFileLineOffsets,IDebugSymbols3.GetSourceFileLineOffsets
req.alt-loc: dbgeng.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
---

# IDebugSymbols3::GetSourceFileLineOffsets method



## -description
The <b>GetSourceFileLineOffsets</b>  method maps each line in a source file to a location in the target's memory.



## -syntax

````
HRESULT GetSourceFileLineOffsets(
  [in]            PCSTR    File,
  [out, optional] PULONG64 Buffer,
  [in]            ULONG    BufferLines,
  [out, optional] PULONG   FileLines
);
````


## -parameters

### -param File [in]

Specifies the name of the file whose lines will be turned into locations in the target's memory.  The symbols for each module in the target are queried for this file.  If the file is not located, the path is dropped and the symbols are queried again.


### -param Buffer [out, optional]

Receives the locations in the target's memory that correspond to the lines of the source code.  The first entry returned to this array corresponds to the first line of the file, so that <code>Buffer[i]</code> contains the location for line <code>i+1</code>.  If no symbol information is available for a line, the corresponding entry in <i>Buffer</i> is set to DEBUG_INVALID_OFFSET.  If <i>Buffer</i> is <b>NULL</b>, this information is not returned.


### -param BufferLines [in]

Specifies the number of PULONG64 objects that the <i>Buffer</i> array can hold.


### -param FileLines [out, optional]

Receives the number of lines in the source file specified by <i>File</i>.


## -returns
This method can also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.
<dl>
<dt><b>S_OK</b></dt>
</dl>The method was successful.
<dl>
<dt><b>S_FALSE</b></dt>
</dl>The method was successful.  However, the number of lines in the source file exceeded the number of entries in the <i>Buffer</i> array and some of the results were discarded.

 


## -remarks
For more information about using the source path, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff560141">Using Source Files</a>.


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
<dt>Dbgeng.h (include Dbgeng.h)</dt>
</dl>
</td>
</tr>
</table>

## -see-also
<dl>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugsymbols.md">IDebugSymbols</a>
</dt>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugsymbols2.md">IDebugSymbols2</a>
</dt>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugsymbols3.md">IDebugSymbols3</a>
</dt>
<dt>
<a href="debugger.findsourcefile">FindSourceFile</a>
</dt>
<dt>
<a href="debugger.getsourceentriesbyline">GetSourceEntriesByLine</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [Debugger\debugger]:%20IDebugSymbols::GetSourceFileLineOffsets method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
