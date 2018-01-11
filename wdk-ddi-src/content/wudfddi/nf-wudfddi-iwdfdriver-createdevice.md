---
UID: NF.wudfddi.IWDFDriver.CreateDevice
title: IWDFDriver::CreateDevice method
author: windows-driver-content
description: The CreateDevice method configures and creates a new framework device object.
old-location: wdf\iwdfdriver_createdevice.htm
old-project: wdf
ms.assetid: df921271-b708-43bf-a250-048b7f638cac
ms.author: windowsdriverdev
ms.date: 12/15/2017
ms.keywords: IWDFDriver, IWDFDriver::CreateDevice, CreateDevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wudfddi.h
req.include-header: Wudfddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.5
req.alt-api: IWDFDriver.CreateDevice
req.alt-loc: WUDFx.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: WUDFx.dll
req.irql: 
req.product: Windows 10 or later.
---

# IWDFDriver::CreateDevice method



## -description
<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>CreateDevice</b> method configures and creates a new framework device object.



## -syntax

````
HRESULT CreateDevice(
  [in]           IWDFDeviceInitialize *pDeviceInit,
  [in, optional] IUnknown             *pCallbackInterface,
  [out]          IWDFDevice           **ppDevice
);
````


## -parameters

### -param pDeviceInit [in]

A pointer to the <a href="..\wudfddi\nn-wudfddi-iwdfdeviceinitialize.md">IWDFDeviceInitialize</a> interface that represents the configuration properties for the new device to create.


### -param pCallbackInterface [in, optional]

A pointer to the <b>IUnknown</b> interface that the framework uses to obtain the interfaces that the driver provides for the new device object. These interfaces provide the callback functions that the framework calls when relevant events occur. For more information, see the following Remarks section.


### -param ppDevice [out]

A pointer to a buffer that receives a pointer to the <a href="..\wudfddi\nn-wudfddi-iwdfdevice.md">IWDFDevice</a> interface for the new device object.


## -returns
<b>CreateDevice</b> returns S_OK if the operation succeeds. Otherwise, this method returns one of the error codes that are defined in Winerror.h.


## -remarks
The <b>IUnknown</b> interface that the driver supplies for the <i>pCallbackInterface</i> parameter can support several interfaces. The framework calls the <b>QueryInterface</b> method of the supplied <b>IUnknown</b> interface multiple times to retrieve the interfaces that the driver supports. The driver's <b>QueryInterface</b> method can return the following interfaces:


<a href="..\wudfddi\nn-wudfddi-ifilecallbackcleanup.md">IFileCallbackCleanup</a>



<a href="..\wudfddi\nn-wudfddi-ifilecallbackclose.md">IFileCallbackClose</a>



<a href="..\wudfddi\nn-wudfddi-iobjectcleanup.md">IObjectCleanup</a>



<a href="..\wudfddi\nn-wudfddi-ipnpcallback.md">IPnpCallback</a>



<a href="..\wudfddi\nn-wudfddi-ipnpcallbackhardware.md">IPnpCallbackHardware</a>



<a href="..\wudfddi\nn-wudfddi-ipnpcallbackhardware2.md">IPnpCallbackHardware2</a>



<a href="..\wudfddi\nn-wudfddi-ipnpcallbackhardwareinterrupt.md">IPnpCallbackHardwareInterrupt</a>



<a href="..\wudfddi\nn-wudfddi-ipnpcallbackselfmanagedio.md">IPnpCallbackSelfManagedIo</a>



<a href="..\wudfddi\nn-wudfddi-ipowerpolicycallbackwakefroms0.md">IPowerPolicyCallbackWakeFromS0</a>



<a href="..\wudfddi\nn-wudfddi-ipowerpolicycallbackwakefromsx.md">IPowerPolicyCallbackWakeFromSx</a>


When the device changes state, the framework calls the method that is related to the change (such as the <a href="wdf.ipnpcallback_ond0entry">IPnpCallback::OnD0Entry</a> method) to notify the driver. 

If the call to <b>CreateDevice</b> is successful, the driver must eventually call the <b>IWDFDevice::Release</b> method. Note that the framework has its own reference count on the object.

For more information, see <a href="wdf.adding_a_device">Adding a Device</a>.

The following code example shows an implementation of the <a href="wdf.idriverentry_ondeviceadd">OnDeviceAdd</a> method of the <a href="..\wudfddi\nn-wudfddi-idriverentry.md">IDriverEntry</a> interface. The framework calls <b>OnDeviceAdd</b> when a device is added to a computer.


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
End of support

</th>
<td width="70%">
Unavailable in UMDF 2.0 and later.

</td>
</tr>
<tr>
<th width="30%">
Minimum UMDF version

</th>
<td width="70%">
1.5

</td>
</tr>
<tr>
<th width="30%">
Header

</th>
<td width="70%">
<dl>
<dt>Wudfddi.h (include Wudfddi.h)</dt>
</dl>
</td>
</tr>
<tr>
<th width="30%">
DLL

</th>
<td width="70%">
<dl>
<dt>WUDFx.dll</dt>
</dl>
</td>
</tr>
</table>

## -see-also
<dl>
<dt>
<a href="..\wudfddi\nn-wudfddi-iwdfdriver.md">IWDFDriver</a>
</dt>
<dt>
<a href="wdf.idriverentry_ondeviceadd">IDriverEntry::OnDeviceAdd</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-ifilecallbackcleanup.md">IFileCallbackCleanup</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-ifilecallbackclose.md">IFileCallbackClose</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-iobjectcleanup.md">IObjectCleanup</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-ipnpcallback.md">IPnpCallback</a>
</dt>
<dt>
<a href="wdf.ipnpcallback_ond0entry">IPnpCallback::OnD0Entry</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-ipnpcallbackhardware.md">IPnpCallbackHardware</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-ipnpcallbackselfmanagedio.md">IPnpCallbackSelfManagedIo</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-iwdfdevice.md">IWDFDevice</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-iwdfdeviceinitialize.md">IWDFDeviceInitialize</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20IWDFDriver::CreateDevice method%20 RELEASE:%20(12/15/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
