---
UID: NN:wiamindr_lh.IWiaMiniDrvTransferCallback
title: IWiaMiniDrvTransferCallback (wiamindr_lh.h)
description: This is a Callback interface that is called by the WIA mini-driver for stream-based transfers.
old-location: image\iwiaminidrvtransfercallback.htm
tech.root: image
ms.assetid: A3D874CB-1F43-4AA0-975B-35C0C5F7A13C
ms.date: 05/03/2018
ms.keywords: IWiaMiniDrvTransferCallback, IWiaMiniDrvTransferCallback interface [Imaging Devices], IWiaMiniDrvTransferCallback interface [Imaging Devices],described, image.iwiaminidrvtransfercallback, wiamindr_lh/IWiaMiniDrvTransferCallback
ms.topic: interface
req.header: wiamindr_lh.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows 8
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
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wiamindr_lh.h
api_name:
- IWiaMiniDrvTransferCallback
product:
- Windows
targetos: Windows
req.typenames: 
---

# IWiaMiniDrvTransferCallback interface

## -description

This is a Callback interface that is called by the WIA mini-driver for stream-based transfers.

## -inheritance

## -members

The **IWiaMiniDrvTransferCallback** interface has these methods.

| Method | Description |
| --- | --- |
| [GetNextStream](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wiamindr_lh/nf-wiamindr_lh-iwiaminidrvtransfercallback-getnextstream) | Called by the WIA mini-driver to obtain a stream for the current data transfer (download or upload). |
| [SendMessage](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wiamindr_lh/nf-wiamindr_lh-iwiaminidrvtransfercallback-sendmessage) | Periodically called by the WIA mini-driver during a data transfer, to update the WIA application client about the progress and status of the transfer. |

## -see-also

[Cancellation of Data Transfers in Windows Vista](https://docs.microsoft.com/windows-hardware/drivers/image/cancellation-of-data-transfers-in-windows-vista)

[Data Transfer Between Legacy Application and Windows Vista Driver](https://docs.microsoft.com/windows-hardware/drivers/image/data-transfer-between-legacy-application-and-windows-vista-driver)

[IStream Transfer Driver Example](https://docs.microsoft.com/windows-hardware/drivers/image/istream-transfer-driver-example)

[Introduction to WIA](https://docs.microsoft.com/windows-hardware/drivers/image/introduction-to-wia)
