---
UID: NS:windot11._DOT11_WPS_DEVICE_NAME
title: _DOT11_WPS_DEVICE_NAME (windot11.h)
description: The DOT11_WPS_DEVICE_NAME structure contains a friendly name of the P2P device.
old-location: netvista\dot11_wps_device_name.htm
tech.root: netvista
ms.assetid: 6C2B8E87-A88F-4244-81B2-0241E2DAE756
ms.date: 02/16/2018
ms.keywords: "*PDOT11_WPS_DEVICE_NAME, DOT11_WPS_DEVICE_NAME, DOT11_WPS_DEVICE_NAME structure [Network Drivers Starting with Windows Vista], PDOT11_WPS_DEVICE_NAME, PDOT11_WPS_DEVICE_NAME structure pointer [Network Drivers Starting with Windows Vista], _DOT11_WPS_DEVICE_NAME, netvista.dot11_wps_device_name, windot11/DOT11_WPS_DEVICE_NAME, windot11/PDOT11_WPS_DEVICE_NAME"
ms.topic: struct
req.header: windot11.h
req.include-header: Windot11.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with   Windows 8.
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
- Windot11.h
api_name:
- DOT11_WPS_DEVICE_NAME
product:
- Windows
targetos: Windows
req.typenames: DOT11_WPS_DEVICE_NAME, *PDOT11_WPS_DEVICE_NAME
product:
- Windows 10 or later.
---

# _DOT11_WPS_DEVICE_NAME structure


## -description


<div class="alert"><b>Important</b>  The <a href="https://docs.microsoft.com/previous-versions/windows/hardware/wireless/ff560689(v=vs.85)">Native 802.11 Wireless LAN</a> interface is deprecated in Windows 10 and later. Please use the WLAN Device Driver Interface (WDI) instead. For more information about WDI, see <a href="https://docs.microsoft.com/windows-hardware/drivers/network/wifi-universal-driver-model">WLAN Universal Windows driver model</a>.</div><div> </div>The <b>DOT11_WPS_DEVICE_NAME</b> structure contains a friendly name of the P2P device.


## -syntax


```cpp
typedef struct _DOT11_WPS_DEVICE_NAME {
   ULONG
uDeviceNameLength;
  UCHAR   ucDeviceName[DOT11_WPS_DEVICE_NAME_MAX_LENGTH];
} DOT11_WPS_DEVICE_NAME, *PDOT11_WPS_DEVICE_NAME;
```


## -struct-fields




### -field uDeviceNameLength

The length, in bytes, of the device name.


### -field ucDeviceName






#### - ucDeviceName[DOT11_WPS_DEVICE_NAME_MAX_LENGTH]

A UTF-8–encoded descriptive name of the device.

