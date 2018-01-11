---
UID: NF.prcomoem.IPrintOemPS2.WritePrinter
title: IPrintOemPS2::WritePrinter method
author: windows-driver-content
description: The IPrintOemPS2::WritePrinter method, if supported, enables a rendering plug-in to capture all output data generated by a Postscript driver.
old-location: print\iprintoemps2_writeprinter.htm
old-project: print
ms.assetid: 76037a86-757a-4b6a-b5ba-a742a18938c2
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IPrintOemPS2, IPrintOemPS2::WritePrinter, WritePrinter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: prcomoem.h
req.include-header: Prcomoem.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IPrintOemPS2.WritePrinter
req.alt-loc: prcomoem.h
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
req.product: Windows 10 or later.
---

# IPrintOemPS2::WritePrinter method



## -description
The <code>IPrintOemPS2::WritePrinter</code> method, if supported, enables a rendering plug-in to capture all output data generated by a Postscript driver. If this method is not supported, the output data would otherwise be sent to the spooler in a call to the spooler's <b>WritePrinter</b> API (described in the Microsoft Windows SDK documentation).



## -syntax

````
HRESULT WritePrinter(
   PDEVOBJ pdevobj,
   PVOID   pBuf,
   DWORD   cbBuffer,
   PDWORD  pcbWritten
);
````


## -parameters

### -param pdevobj 

Pointer to a <a href="print.devobj">DEVOBJ</a> structure.


### -param pBuf 

Pointer to the first byte of an array of bytes that contains the output data generated by the PostScript driver.


### -param cbBuffer 

Specifies the size, in bytes, of the array pointed to by <i>pBuf</i>.


### -param pcbWritten 

Pointer to a DWORD value that receives the number of bytes of data that the plug-in sent to the spooler's <b>WritePrinter</b> function (described in the Windows SDK documentation).


## -returns
If successful, this method returns S_OK. Otherwise, this method should return an appropriate value in the returned HRESULT.


## -remarks
At <a href="display.drvenablepdev">DrvEnablePDEV</a> time, the PostScript driver calls this method with <i>pBuf</i> and <i>pdevobj</i> set to <b>NULL</b>, and <i>cbBuf</i> set to 0, to detect whether the plug-in implements this function. The plug-in should return S_OK to indicate it implements this method, and should return E_NOTIMPL otherwise.

This method should report the number of bytes written to the spooler's <b>WritePrinter</b> function in <i>pcbWritten</i>. A value of zero carries no special meaning; errors must be reported through the returned HRESULT.


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
<dt>Prcomoem.h (include Prcomoem.h)</dt>
</dl>
</td>
</tr>
</table>