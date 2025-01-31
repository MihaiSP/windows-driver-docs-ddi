---
UID: NS:ndiswwan._NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS
title: _NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS (ndiswwan.h)
description: The NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS structure encapsulates data for OID_WWAN_SUBSCRIBE_DEVICE_SERVICES_EVENTS.
old-location: netvista\ndis_wwan_subscribe_device_service_events.htm
tech.root: netvista
ms.assetid: 99A772EF-C67C-48B0-A3F9-0B32A14247D6
ms.date: 05/02/2018
ms.keywords: "*PNDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS, NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS, NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS structure [Network Drivers Starting with Windows Vista], PNDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS, PNDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS structure pointer [Network Drivers Starting with Windows Vista], _NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS, ndiswwan/NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS, ndiswwan/PNDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS, netvista.ndis_wwan_subscribe_device_service_events"
ms.topic: struct
req.header: ndiswwan.h
req.include-header: Ndiswwan.h
req.target-type: Windows
req.target-min-winverclnt: Versions:\_Supported in Windows 8 and later versions of Windows.
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
- ndiswwan.h
api_name:
- NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS
product:
- Windows
targetos: Windows
req.typenames: NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS, *PNDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS
---

# _NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS structure


## -description


The NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS structure encapsulates data for OID_WWAN_SUBSCRIBE_DEVICE_SERVICES_EVENTS.


## -struct-fields




### -field Header

The header with type, revision, and size information about the NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS structure. The MB
     Service sets the header with the values that are shown in the following table when it sends the data
     structure to the miniport driver for 
     <i>set</i> operations. Miniport drivers must set the header with the same values when they send the data
     structure to the MB service.
     

<table>
<tr>
<th>Header submember</th>
<th>Value</th>
</tr>
<tr>
<td>
Type

</td>
<td>
NDIS_OBJECT_TYPE_DEFAULT

</td>
</tr>
<tr>
<td>
Revision

</td>
<td>
NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS_REVISION_1

</td>
</tr>
<tr>
<td>
Size

</td>
<td>
sizeof(NDIS_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS)

</td>
</tr>
</table>
 

For more information about these members, see 
     <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ntddndis/ns-ntddndis-_ndis_object_header">NDIS_OBJECT_HEADER</a>.


### -field DeviceServiceListHeader

A formatted WWAN_LIST_HEADER object that represents a list of device services and the number of services  in the list.

This is the list of device service that the MB service has subscribed for NDIS_STATUS_WWAN_DEVICE_SERVICE_EVENT notifications.

This member points to the list of the GUIDs (WwanStructDeviceServiceGuid) by using the WWAN_LIST_HEADER structure.


## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wwan/ns-wwan-_wwan_list_header">WWAN_LIST_HEADER</a>
 

 

