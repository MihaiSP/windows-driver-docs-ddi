---
UID: NN:printerextension.IPrinterScriptableStream
title: IPrinterScriptableStream (printerextension.h)
description: The IPrinterScriptableStream interface builds on IPrinterScriptableSequentialStream and adds IStream-like semantics.
old-location: print\iprinterscriptablestream.htm
tech.root: print
ms.assetid: AD3CDF90-76ED-498B-8DE1-B191504EB415
ms.date: 04/20/2018
ms.keywords: IPrinterScriptableStream, IPrinterScriptableStream interface [Print Devices], IPrinterScriptableStream interface [Print Devices],described, print.iprinterscriptablestream, printerextension/IPrinterScriptableStream
ms.topic: interface
req.header: printerextension.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
- IPrinterScriptableStream
product:
- Windows
targetos: Windows
req.typenames: 
---

# IPrinterScriptableStream interface


## -description


The IPrinterScriptableStream interface builds on <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/printerextension/nn-printerextension-iprinterscriptablesequentialstream">IPrinterScriptableSequentialStream</a> and adds IStream-like semantics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrinterScriptableStream</b> interface inherits from <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/printerextension/nn-printerextension-iprinterscriptablesequentialstream">IPrinterScriptableSequentialStream</a>. <b>IPrinterScriptableStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrinterScriptableStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/printerextension/nf-printerextension-iprinterscriptablestream-commit">Commit</a>
</td>
<td align="left" width="63%">
Commits the operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/printerextension/nf-printerextension-iprinterscriptablestream-seek">Seek</a>
</td>
<td align="left" width="63%">
Sets the seek pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/printerextension/nf-printerextension-iprinterscriptablestream-setsize">SetSize</a>
</td>
<td align="left" width="63%">
Sets the size of the scriptable stream, in bytes.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/printerextension/nn-printerextension-iprinterscriptablepropertybag">IPrinterScriptablePropertyBag</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/printerextension/nf-printerextension-iprinterscriptablepropertybag-getreadstream">IPrinterScriptablePropertyBag::GetReadStream</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/printerextension/nf-printerextension-iprinterscriptablepropertybag-getwritestream">IPrinterScriptablePropertyBag::GetWriteStream</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/printerextension/nn-printerextension-iprinterscriptablesequentialstream">IPrinterScriptableSequentialStream</a>
 

 

