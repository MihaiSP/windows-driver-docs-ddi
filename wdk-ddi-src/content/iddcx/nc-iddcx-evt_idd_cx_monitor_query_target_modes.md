---
UID: NC:iddcx.EVT_IDD_CX_MONITOR_QUERY_TARGET_MODES
title: EVT_IDD_CX_MONITOR_QUERY_TARGET_MODES (iddcx.h)
description: EVT_IDD_CX_MONITOR_QUERY_TARGET_MODES is called by the OS to get a list of target modes supported by the driver for a monitor connected to the endpoint.
old-location: display\evt_idd_cx_monitor_query_target_modes.htm
tech.root: display
ms.assetid: a83ed1a3-e279-45be-b229-137fa61d9b38
ms.date: 05/10/2018
ms.keywords: EVT_IDD_CX_MONITOR_QUERY_TARGET_MODES, EVT_IDD_CX_MONITOR_QUERY_TARGET_MODES callback, EvtIddCxMonitorQueryTargetModes, EvtIddCxMonitorQueryTargetModes callback function [Display Devices], PFN_IDD_CX_MONITOR_QUERY_TARGET_MODES, PFN_IDD_CX_MONITOR_QUERY_TARGET_MODES callback function pointer [Display Devices], display.evt_idd_cx_monitor_query_target_modes, iddcx/EvtIddCxMonitorQueryTargetModes
ms.topic: callback
req.header: iddcx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
req.irql: "_requires_same_"
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- iddcx.h
api_name:
- PFN_IDD_CX_MONITOR_QUERY_TARGET_MODES
product:
- Windows
targetos: Windows
req.typenames: 
---

# EVT_IDD_CX_MONITOR_QUERY_TARGET_MODES callback function


## -description


<b>EVT_IDD_CX_MONITOR_QUERY_TARGET_MODES</b> is called by the OS to get a list of target modes supported by the driver for a monitor connected to the endpoint.


## -parameters




### -param MonitorObject [in]

A handle by the OS to identify the monitor to generate a list of target modes for.


### -param pInArgs [in]

Input arguments used by <b>EVT_IDD_CX_MONITOR_QUERY_TARGET_MODES</b>.


### -param pOutArgs [out]

Output arguments generated by <b>EVT_IDD_CX_MONITOR_QUERY_TARGET_MODES</b>.


## -returns




(NTSTATUS) If the operation is successful, the callback function must return STATUS_SUCCESS, or another status value for which NT_SUCCESS(status) equals TRUE. Otherwise, an appropriate <a href="https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values">NTSTATUS</a> error code. 
                    



