---
UID: NS:ntifs._PREFETCH_OPEN_ECP_CONTEXT
title: _PREFETCH_OPEN_ECP_CONTEXT (ntifs.h)
description: The PREFETCH_OPEN_ECP_CONTEXT structure communicates whether the prefetcher performs a given open request on a file.
old-location: ifsk\prefetch_open_ecp_context.htm
tech.root: ifsk
ms.assetid: 199a3003-a7dd-48a3-aa76-550332be26f3
ms.date: 04/16/2018
ms.keywords: "*PPREFETCH_OPEN_ECP_CONTEXT, ECP_Structures_bd946e05-ef42-4fcc-93f8-bf96b6440817.xml, PPREFETCH_OPEN_ECP_CONTEXT, PPREFETCH_OPEN_ECP_CONTEXT structure pointer [Installable File System Drivers], PREFETCH_OPEN_ECP_CONTEXT, PREFETCH_OPEN_ECP_CONTEXT structure [Installable File System Drivers], _PREFETCH_OPEN_ECP_CONTEXT, ifsk.prefetch_open_ecp_context, ntifs/PPREFETCH_OPEN_ECP_CONTEXT, ntifs/PREFETCH_OPEN_ECP_CONTEXT"
ms.topic: struct
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Windows
req.target-min-winverclnt: This structure is available starting with Windows Vista.
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
- HeaderDef
api_location:
- ntifs.h
api_name:
- PREFETCH_OPEN_ECP_CONTEXT
product:
- Windows
targetos: Windows
req.typenames: PREFETCH_OPEN_ECP_CONTEXT, *PPREFETCH_OPEN_ECP_CONTEXT
---

# _PREFETCH_OPEN_ECP_CONTEXT structure


## -description


The PREFETCH_OPEN_ECP_CONTEXT structure communicates whether the prefetcher performs a given open request on a file. 


## -struct-fields




### -field Context

A pointer to an opaque context that is associated with the open request. 


## -remarks



The prefetcher is a component of the operating system that is tightly integrated with the cache manager and the memory manager to make disk accesses more efficient and therefore improve performance. If other components interfere with the prefetcher, system performance decreases and might deadlock. Therefore, the prefetcher attaches the PREFETCH_OPEN_ECP_CONTEXT structure to a file to communicate that the prefetcher has performed an open request on the file. The prefetcher uses the GUID_ECP_PREFETCH_OPEN GUID in a call to the <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltcreatefileex2">FltCreateFileEx2</a> or <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-iocreatefileex">IoCreateFileEx</a> routine to attach the PREFETCH_OPEN_ECP_CONTEXT structure. A file system filter driver can call the <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltfindextracreateparameter">FltFindExtraCreateParameter</a> routine to determine whether PREFETCH_OPEN_ECP_CONTEXT is attached to the file and then take appropriate action. The file system filter driver should call the <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltisecpfromusermode">FltIsEcpFromUserMode</a> routine to determine whether the PREFETCH_OPEN_ECP_CONTEXT context structure originated from kernel mode. To prevent malicious applications from spoofing the prefetcher, the file system filter driver should not accept PREFETCH_OPEN_ECP_CONTEXT if it originated from user mode.

After the prefetcher attaches the PREFETCH_OPEN_ECP_CONTEXT structure to a file, all additional prefetcher activity for the file involves the file object that has PREFETCH_OPEN_ECP_CONTEXT attached. If a file system filter driver must identify prefetcher file system requests other than create requests, the file system filter driver should maintain its own state (for example, filter manager handle contexts). The file system filter driver maintains its own state in order to determine whether a particular file object is a prefetcher file object.

The memory manager can cache the prefetcher file object. The memory manager can then use the prefetcher file object for other applications that perform mapped I/O or cached I/O by using the cache manager. Therefore, the prefetcher file object can be used for paging I/O before or after the prefetcher closes its handle. This paging I/O can include paging writes, even though the prefetcher never writes any data. The paging writes are generated by other applications. The memory manager writes data from the applications by using its cached prefetcher file object. Therefore, if a file system filter driver performs work that is triggered by paging writes, the file system filter driver should still perform that work, even if the paging writes come on a prefetcher file object. 

When a file system filter driver determines that a cleanup operation occurred on a prefetcher file object, the file system filter driver should no longer consider that file object to be prefetcher-opened.

The following are common operations that the prefetcher performs (however, in these operations, the prefetcher never changes file contents):

<ul>
<li>
Volume open and close

</li>
<li>
File open and close

</li>
<li>
Query file information

</li>
<li>
Set file information (only to instruct the file system not to update last access time for this open)

</li>
<li>
Create image and data section

</li>
<li>
Perform asynchronous paging I/O

</li>
</ul>
To avoid inducing a possible deadlock situation, a file system filter driver should:

<ul>
<li>
Never block any prefetcher operations.

</li>
<li>
Pass prefetcher operations through without issuing other file system requests. 

</li>
</ul>
For any application or driver to access any of the data that is being prefetched, it must open its own handle to the file or create a section or both.

For information about how to use ECPs to associate additional information with an <a href="https://docs.microsoft.com/windows-hardware/drivers/ifs/irp-mj-create">IRP_MJ_CREATE</a> operation on a file, see <a href="https://docs.microsoft.com/windows-hardware/drivers/ifs/using-extra-create-parameters-with-an-irp-mj-create-operation">Using Extra Create Parameters with an IRP_MJ_CREATE Operation</a>. 

The PREFETCH_OPEN_ECP_CONTEXT structure is read-only. You should use it to retrieve information about a prefetcher open ECP only. For more information about this issue, see <a href="https://docs.microsoft.com/windows-hardware/drivers/ifs/system-defined-ecps">System-Defined ECPs</a>.



