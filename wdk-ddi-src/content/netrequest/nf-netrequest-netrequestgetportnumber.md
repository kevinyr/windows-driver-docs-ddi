---
UID: NF:netrequest.NetRequestGetPortNumber
title: NetRequestGetPortNumber function
author: windows-driver-content
description: Retrieves the port number for the network request object. 
ms.assetid: edf2d400-bfde-4cec-8164-7908cc008cf2
ms.author: windowsdriverdev
ms.date: 02/08/2018
ms.topic: function
ms.keywords: NetRequestGetPortNumber
req.header: netrequest.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver: 1.21
req.umdf-ver:
req.lib:
req.dll:
req.irql: <= DISPATCH_LEVEL
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library: 
req.alt-api:
req.alt-loc:
topictype: 
-	apiref
apitype: 
-	HeaderDef
apilocation: 
-	netrequest.h
apiname: 
-	NetRequestGetPortNumber
product: Windows
targetos: Windows
req.product: Windows 10 or later.
---

# NetRequestGetPortNumber function


## -description

> [!WARNING]
> Some information in this topic relates to prereleased product, which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.
>
> NetAdapterCx is preview only in Windows 10, version 1803.

Retrieves the port number for the network request object. 

## -parameters

### -param Request
A handle to a network request object.

## -returns
Returns the port number corresponding to the network request object. If the port is unknown or default, returns zero.

## -remarks
The minimum NetAdapterCx version for **NetRequestGetPortNumber** is 1.0.

## -see-also

[NDIS_OID_REQUEST](../ndis/ns-ndis-_ndis_oid_request.md)