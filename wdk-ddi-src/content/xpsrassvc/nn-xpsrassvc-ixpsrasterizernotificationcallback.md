---
UID: NN:xpsrassvc.IXpsRasterizerNotificationCallback
title: IXpsRasterizerNotificationCallback
author: windows-driver-content
description: The IXpsRasterizerNotificationCallback interface enables the XPS rasterization service to determine whether to continue a rasterization operation that was previously initiated by an XPSDrv filter.
old-location: print\ixpsrasterizernotificationcallback_interface.htm
old-project: print
ms.assetid: 7616b5c7-a21f-4db1-923b-ebf2a039b5ec
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IXpsRasterizerNotificationCallback, IXpsRasterizerNotificationCallback interface [Print Devices], IXpsRasterizerNotificationCallback interface [Print Devices],described, print.ixpsrasterizernotificationcallback_interface, print_xpsrast_fe5791b3-111b-454e-a033-45dfa128d325.xml, xpsrassvc/IXpsRasterizerNotificationCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: xpsrassvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
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
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsrassvc.h
api_name:
-	IXpsRasterizerNotificationCallback
product:
- Windows
targetos: Windows
req.typenames: 
---

# IXpsRasterizerNotificationCallback interface


## -description


The IXpsRasterizerNotificationCallback interface enables the XPS rasterization service to determine whether to continue a rasterization operation that was previously initiated by an XPSDrv filter. The filter implements this interface and passes an IXpsRasterizerNotificationCallback pointer as a parameter to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556365">IXpsRasterizer::RasterizeRect</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsRasterizerNotificationCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsRasterizerNotificationCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsRasterizerNotificationCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451185">Continue</a>
</td>
<td align="left" width="63%">
The <code>Continue</code> method tells the caller (the XPS rasterization service) whether to continue rasterizing the current XPS fixed page.

</td>
</tr>
</table> 

