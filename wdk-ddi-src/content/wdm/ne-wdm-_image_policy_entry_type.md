---
UID : NE:wdm._IMAGE_POLICY_ENTRY_TYPE
title : _IMAGE_POLICY_ENTRY_TYPE
author : windows-driver-content
description : This enumeration is not supported.
old-location : kernel\_image_policy_entry_type.htm
old-project : kernel
ms.assetid : f8ce3297-5a57-4ece-a74c-ae5e4e15ce3e
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _IMAGE_POLICY_ENTRY_TYPE, IMAGE_POLICY_ENTRY_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : wdm.h
req.include-header : Wdm.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IMAGE_POLICY_ENTRY_TYPE
req.alt-loc : wdm.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : IMAGE_POLICY_ENTRY_TYPE
req.product : Windows 10 or later.
---

# _IMAGE_POLICY_ENTRY_TYPE Enumeration
This enumeration is not supported.

## Syntax
````
typedef enum _IMAGE_POLICY_ENTRY_TYPE { 
  ImagePolicyEntryTypeBool,
  ImagePolicyEntryTypeInt8,
  ImagePolicyEntryTypeUInt8,
  ImagePolicyEntryTypeInt16,
  ImagePolicyEntryTypeUInt16,
  ImagePolicyEntryTypeInt32,
  ImagePolicyEntryTypeUInt32,
  ImagePolicyEntryTypeInt64,
  ImagePolicyEntryTypeUInt64,
  ImagePolicyEntryTypeAnsiString,
  ImagePolicyEntryTypeUnicodeString,
  ImagePolicyEntryTypeMaximum
} IMAGE_POLICY_ENTRY_TYPE;
````

## Constants

<table>

<tr>
<td>ImagePolicyEntryTypeAnsiString</td>
<td>Reserved.</td>
</tr>

<tr>
<td>ImagePolicyEntryTypeBool</td>
<td>Reserved.</td>
</tr>

<tr>
<td>ImagePolicyEntryTypeInt16</td>
<td>Reserved.</td>
</tr>

<tr>
<td>ImagePolicyEntryTypeInt32</td>
<td>Reserved.</td>
</tr>

<tr>
<td>ImagePolicyEntryTypeInt64</td>
<td>Reserved.</td>
</tr>

<tr>
<td>ImagePolicyEntryTypeInt8</td>
<td>Reserved.</td>
</tr>

<tr>
<td>ImagePolicyEntryTypeMaximum</td>
<td>Reserved.</td>
</tr>

<tr>
<td>ImagePolicyEntryTypeUInt16</td>
<td>Reserved.</td>
</tr>

<tr>
<td>ImagePolicyEntryTypeUInt32</td>
<td>Reserved.</td>
</tr>

<tr>
<td>ImagePolicyEntryTypeUInt64</td>
<td>Reserved.</td>
</tr>

<tr>
<td>ImagePolicyEntryTypeUInt8</td>
<td>Reserved.</td>
</tr>

<tr>
<td>ImagePolicyEntryTypeUnicodeString</td>
<td>Reserved.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h) |