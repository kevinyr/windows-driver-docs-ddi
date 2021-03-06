---
UID: NE:wwan._WWAN_UICCSLOT_STATE
title: "_WWAN_UICCSLOT_STATE"
author: windows-driver-content
description: The WWAN_UICCSLOT_STATE enumeration lists the different states of a UICC (SIM) card slot on a modem. The slot state represents a summary of both the slot state and the card state.
old-location: netvista\wwan_uiccslot_state.htm
old-project: netvista
ms.assetid: 63A3C2AA-6EBF-469D-933A-C51F5EC31C47
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: "*PWWAN_UICCSLOT_STATE, UICCSlotStateActive, UICCSlotStateEmpty, UICCSlotStateError, UICCSlotStateNotReady, UICCSlotStateOff, UICCSlotStateOffEmpty, UICCSlotStateUnknown, WWAN_UICCSLOT_STATE, WWAN_UICCSLOT_STATE enumeration [Network Drivers Starting with Windows Vista], _WWAN_UICCSLOT_STATE, netvista.wwan_uiccslot_state, wwan/UICCSlotStateActive, wwan/UICCSlotStateEmpty, wwan/UICCSlotStateError, wwan/UICCSlotStateNotReady, wwan/UICCSlotStateOff, wwan/UICCSlotStateOffEmpty, wwan/UICCSlotStateUnknown, wwan/WWAN_UICCSLOT_STATE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wwan.h
req.include-header: Wwan.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703
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
-	HeaderDef
api_location:
-	wwan.h
api_name:
-	WWAN_UICCSLOT_STATE
product:
- Windows
targetos: Windows
req.typenames: WWAN_UICCSLOT_STATE, *PWWAN_UICCSLOT_STATE
---

# _WWAN_UICCSLOT_STATE enumeration


## -description


The <b>WWAN_UICCSLOT_STATE</b> enumeration lists the different states of a UICC (SIM) card slot on a modem. The slot state represents a summary of both the slot state and the card state.


## -enum-fields




### -field WwanUiccSlotStateUnknown


### -field WwanUiccSlotStateOffEmpty


### -field WwanUiccSlotStateOff


### -field WwanUiccSlotStateEmpty


### -field WwanUiccSlotStateNotReady


### -field WwanUiccSlotStateActive


### -field WwanUiccSlotStateError


### -field WwanUiccSlotStateActiveEsim


### -field WwanUiccSlotStateActiveEsimNoProfile


### -field WwanUiccSlotStateMax




#### - UICCSlotStateActive

The card in the slot is available and ready to accept commands. This has no association with the SIM PIN locked state.


#### - UICCSlotStateEmpty

The card slot is powered on but no card is present.


#### - UICCSlotStateError

The card in the slot is in an error state and cannot be used.


#### - UICCSlotStateNotReady

The card in the slot is not ready; i.e., it has been reset but has not finished initializing. It cannot be used at this time.


#### - UICCSlotStateOff

The card slot is powered off and a card is present.


#### - UICCSlotStateOffEmpty

The card slot is powered off and empty. An implementation that is unable to determine the presence of a card in a slot that is powered off reports its state as <i>Off</i>.


#### - UICCSlotStateUnknown

The modem is still in the process of initializing so the SIM slot state is not deterministic.


## -remarks



The set of reported states is constrained by the capability of the slot hardware. In the most restrictive case, the slot hardware may only be able to determine that a card is present when it is powered on and active; in such a case the <b>OffEmpty</b> and <b>Off</b> states will not be reported.




## -see-also




<a href="https://msdn.microsoft.com/F45D253E-E7D7-4600-AF8C-6D4EB096030D">WWAN_SLOT_INFO</a>
 

 

