---
UID: NN:printerextension.IPrinterBidiSetRequestCallback
title: IPrinterBidiSetRequestCallback (printerextension.h)
description: Describes the signature of the callback object that receives the Bidi response.
old-location: print\iprinterbidisetrequestcallback.htm
tech.root: print
ms.assetid: C85690D0-3CA7-46C7-B597-E36555879F08
ms.date: 04/20/2018
ms.keywords: IPrinterBidiSetRequestCallback, IPrinterBidiSetRequestCallback interface [Print Devices], IPrinterBidiSetRequestCallback interface [Print Devices],described, print.iprinterbidisetrequestcallback, printerextension/IPrinterBidiSetRequestCallback
ms.topic: interface
req.header: printerextension.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Printerextension.h
api_name:
- IPrinterBidiSetRequestCallback
product:
- Windows
targetos: Windows
req.typenames: 
---

# IPrinterBidiSetRequestCallback interface


## -description


Describes the signature of the callback object that receives the Bidi response.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrinterBidiSetRequestCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPrinterBidiSetRequestCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrinterBidiSetRequestCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/printerextension/nf-printerextension-iprinterbidisetrequestcallback-completed">Completed</a>
</td>
<td align="left" width="63%">
Invoked when the Bidi “Set”” operation is completed.

</td>
</tr>
</table> 


## -remarks



<b>IPrinterBidiSetRequestCallback</b> provides the Bidi response string, and <b>HRESULT</b> value returned from the <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/bidispl/nf-bidispl-ibidispl2-sendrecvxmlstring">IBidiSpl2::SendRecvXmlString</a> method. In other words,  this interface provides the results of the attempt to send data to the device. 

<b>IPrinterBidiSetRequestCallback</b>  helps to make it possible to perform device maintenance from a UWP  device app or from a printer extension. For more information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/print/device-maintenance">Device Maintenance</a>.




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/print/device-maintenance">Device Maintenance</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/bidispl/nf-bidispl-ibidispl2-sendrecvxmlstring">IBidiSpl2::SendRecvXmlString</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/printerextension/nf-printerextension-iprinterqueue2-sendbidisetrequestasync">SendBidiSetRequestAsync</a>
 

 

