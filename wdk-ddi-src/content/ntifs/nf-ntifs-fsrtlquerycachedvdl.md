---
UID: NF:ntifs._FSRTL_ADVANCED_FCB_HEADER.FsRtlQueryCachedVdl
title: FsRtlQueryCachedVdl function (ntifs.h)
description: The current valid data length (VDL) for a cached file is retrieved with the FsRtlQueryCachedVdl routine.
old-location: ifsk\fsrtlquerycachedvdl.htm
tech.root: ifsk
ms.assetid: 5D4F3D70-6E2B-4B2E-91A4-6852AF8FEAD0
ms.date: 04/16/2018
ms.keywords: FsRtlQueryCachedVdl, FsRtlQueryCachedVdl routine [Installable File System Drivers], ifsk.fsrtlquerycachedvdl, ntifs/FsRtlQueryCachedVdl
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available in starting with Windows 8.
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- NtosKrnl.exe
api_name:
- FsRtlQueryCachedVdl
product:
- Windows
targetos: Windows
req.typenames: 
---

# FsRtlQueryCachedVdl function


## -description


The current valid data length (VDL) for a cached file is retrieved with the <b>FsRtlQueryCachedVdl</b> routine.


## -parameters




### -param FileObject [in]

The file object to retrieve the cached VDL for.


### -param Vdl [out]

 A pointer to a caller supplied value which receives the VDL.


## -returns



<b>FsRtlQueryCachedVdl</b> returns <b>STATUS_SUCCESS</b> if the cached VDL is obtained successfully for the <i>FileObject</i> specified. Otherwise, another appropriate <b>NTSTATUS</b> value is returned.




## -remarks



The <b>FsRtlQueryCachedVdl</b> routine will return the VDL for a full span file region. This is a region beginning at an offset of 0 and having a length of <b>MAXLONGLONG</b>.



