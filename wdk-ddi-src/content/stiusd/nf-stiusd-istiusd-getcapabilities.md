---
UID: NF.stiusd.IStiUSD.GetCapabilities
title: IStiUSD::GetCapabilities method
author: windows-driver-content
description: A still image minidriver's IStiUSD::GetCapabilities method returns a still image device's capabilities.
old-location: image\istiusd_getcapabilities.htm
old-project: Image
ms.assetid: baec1e38-360e-4f4f-82bd-bc89e3f8483d
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IStiUSD, IStiUSD::GetCapabilities, GetCapabilities
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: stiusd.h
req.include-header: Stiusd.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IStiUSD.GetCapabilities
req.alt-loc: stiusd.h
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

# IStiUSD::GetCapabilities method



## -description
A still image minidriver's <b>IStiUSD::GetCapabilities</b> method returns a still image device's capabilities.



## -syntax

````
HRESULT GetCapabilities(
   PSTI_USD_CAPS pUsdCaps
);
````


## -parameters

### -param pUsdCaps 

Caller-supplied pointer to an empty <a href="image.sti_usd_caps">STI_USD_CAPS</a> structure.


## -returns
If the operation succeeds, the method should return S_OK. Otherwise, it should return one of the STIERR-prefixed error codes defined in <i>stierr.h</i>.


## -remarks
The <b>IStiUSD::GetCapabilities</b> method should set appropriate device capability flags in the caller-supplied <a href="image.sti_usd_caps">STI_USD_CAPS</a> structure. It should also set the version number to STI_VERSION.


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
<dt>Stiusd.h (include Stiusd.h)</dt>
</dl>
</td>
</tr>
</table>

## -see-also
<dl>
<dt>
<a href="image.istidevice_getcapabilities">IStiDevice::GetCapabilities</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [Image\image]:%20IStiUSD::GetCapabilities method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
