---
UID: NF:wdtfpnpaction.IWDTFPNPAction2.RemoveDevice
title: IWDTFPNPAction2::RemoveDevice (wdtfpnpaction.h)
description: Removes the device.
old-location: dtf\iwdtfpnpaction2_removedevice.htm
tech.root: dtf
ms.assetid: 68e15b98-e58a-4789-80d0-fc31f936345e
ms.date: 04/04/2018
ms.keywords: IWDTFPNPAction2 interface [Windows Device Testing Framework],RemoveDevice method, IWDTFPNPAction2.RemoveDevice, IWDTFPNPAction2::RemoveDevice, Microsoft.WDTF.IWDTFPNPAction2.RemoveDevice, Microsoft::WDTF::IWDTFPNPAction2::RemoveDevice, RemoveDevice, RemoveDevice method [Windows Device Testing Framework], RemoveDevice method [Windows Device Testing Framework],IWDTFPNPAction2 interface, dtf.iwdtfpnpaction2_removedevice, wdtfpnpaction/IWDTFPNPAction2::RemoveDevice
ms.topic: method
req.header: wdtfpnpaction.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFPNPAction.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTFDriverPNPAction.Interop.dll
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- WDTFDriverPNPAction.Interop.dll
api_name:
- IWDTFPNPAction2.RemoveDevice
product:
- Windows
targetos: Windows
req.typenames: 
---

# IWDTFPNPAction2::RemoveDevice


## -description


Removes the device.


## -parameters




### -param pbSuccess [out, retval]

True if the operation succeeds; otherwise, false.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Under the covers, this will call DIF_REMOVE.




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdtfpnpaction/nn-wdtfpnpaction-iwdtfpnpaction2">IWDTFPNPAction2</a>
 

 

