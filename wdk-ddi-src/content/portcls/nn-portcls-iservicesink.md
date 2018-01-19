---
UID : NN:portcls.IServiceSink
title : IServiceSink
author : windows-driver-content
description : The IServiceSink interface encapsulates handling of a service request.
old-location : audio\iservicesink.htm
old-project : audio
ms.assetid : 329ae226-02fb-438b-b461-da51e3afd6eb
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : PcUnregisterIoTimeout
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : interface
req.header : portcls.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IServiceSink
req.alt-loc : portcls.h
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

# IServiceSink interface

The <code>IServiceSink</code> interface encapsulates handling of a service request. The source of the service request is typically the miniport driver's interrupt service routine. PortCls supports the <code>IServiceSink</code> interface. An <code>IServiceSink</code> object is typically a member of a service group that is managed by an <a href="..\portcls\nn-portcls-iservicegroup.md">IServiceGroup</a> object. <code>IServiceSink</code> inherits from the <b>IUnknown</b> interface.

<code>IServiceSink</code> is the base interface for <b>IServiceGroup</b>. This allows an <b>IServiceGroup</b> object to add itself (as an object with an <code>IServiceSink</code> interface) to another <b>IServiceGroup</b> object's service group.

Although the PortCls system driver provides a <a href="..\portcls\nf-portcls-pcnewservicegroup.md">PcNewServiceGroup</a> function for creating a service group object, no similar function exists for creating a service sink object. Instead, a driver object that requires a service sink simply implements an <code>IServiceSink</code> interface in the driver object. For convenience, header file portcls.h includes an <b>IMP_IServiceSink</b> constant for adding the <code>IServiceSink</code> implementation to the object's class definition. The cost of adding an <code>IServiceSink</code> interface to an object is small because the interface supports only a single method. A port driver typically adds an <code>IServiceSink</code> interface to its port object and stream objects so that they can receive notification of interrupts from an audio device.

For more information, see <a href="https://msdn.microsoft.com/00e17e01-8889-4fae-a0ff-e110d7a9b21e">Service Sink and Service Group Objects</a>.

## Methods

<p>The <b>IServiceSink</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [portcls.IServiceSink.RequestService](nf-portcls-iservicesink-requestservice.md) | The RequestService method is called to forward a service request to an IServiceSink object. |

## Remarks



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum UMDF version** |  |
| **Header** | portcls.h |
| **DLL** |  |