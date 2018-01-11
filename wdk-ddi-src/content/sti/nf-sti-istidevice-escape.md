---
UID: NF.sti.IStiDevice.Escape
title: IStiDevice::Escape method
author: windows-driver-content
description: The IStiDevice::Escape method sends a request for a vendor-specific I/O operation to a still image device.
old-location: image\istidevice_escape.htm
old-project: Image
ms.assetid: ca2aae12-b4b8-4bae-bc3b-812a1ae539c0
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IStiDevice, IStiDevice::Escape, Escape
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sti.h
req.include-header: Sti.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IStiDevice.Escape
req.alt-loc: sti.h
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

# IStiDevice::Escape method



## -description
The <b>IStiDevice::Escape</b> method sends a request for a vendor-specific I/O operation to a still image device.



## -syntax

````
HRESULT Escape(
  [in]      STI_RAW_CONTROL_CODE EscapeFunction,
  [in]      LPVOID               lpInData,
            DWORD                cbInDataSize,
  [in, out] LPVOID               pOutData,
            DWORD                dwOutDataSize,
  [out]     LPDWORD              pdwActualData
);
````


## -parameters

### -param EscapeFunction [in]

Caller-supplied, vendor-defined, DWORD-sized value representing an I/O operation. The device's minidriver must recognize this value and must export an <b>IStiUSD</b> interface. Vendor-defined values must be greater than STI_RAW_RESERVED, which is defined in <i>Sti.h</i>.


### -param lpInData [in]

Caller-supplied pointer to a buffer containing data to be sent to the device.


### -param cbInDataSize 

Caller-supplied length, in bytes, of the data contained in the buffer pointed to by <i>lpInData</i>.


### -param pOutData [in, out]

Caller-supplied pointer to a memory buffer to receive data from the device.


### -param dwOutDataSize 

Caller-supplied length, in bytes, of the buffer pointed to by <i>lpOutData</i>.


### -param pdwActualData [out]

Receives the number of bytes actually written to <i>pOutData</i>.


## -returns
If the operation succeeds, the method returns S_OK. Otherwise, it returns one of the STIERR-prefixed error codes defined in <i>stierr.h</i>.


## -remarks
The <b>IStiDevice::Escape</b> method calls <a href="image.istiusd_escape">IStiUSD::Escape</a>, which is exported by vendor-supplied minidrivers. The device's minidriver defines the Method parameter usage.

Before calling <b>IStiDevice::Escape</b>, clients of the <b>IStiDevice</b> COM interface must call <a href="image.istillimage_createdevice">IStillImage::CreateDevice</a> to obtain an <b>IStiDevice</b> interface pointer, which provides access to a specified device.

A call to <b>IStiDevice::Escape</b> must be preceded by a call to <a href="image.istidevice_lockdevice">IStiDevice::LockDevice</a> and followed by a call to <a href="image.istidevice_unlockdevice">IStiDevice::UnLockDevice</a>.


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
<dt>Sti.h (include Sti.h)</dt>
</dl>
</td>
</tr>
</table>