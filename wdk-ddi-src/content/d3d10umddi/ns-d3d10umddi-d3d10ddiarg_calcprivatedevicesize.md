---
UID: NS:d3d10umddi.D3D10DDIARG_CALCPRIVATEDEVICESIZE
title: D3D10DDIARG_CALCPRIVATEDEVICESIZE (d3d10umddi.h)
description: The D3D10DDIARG_CALCPRIVATEDEVICESIZE structure describes the parameters that the user-mode display driver uses to calculate the size of a memory block that the driver requires to store frequently-accessed data.
old-location: display\d3d10ddiarg_calcprivatedevicesize.htm
ms.assetid: 79bb55db-dd4d-4cad-927e-e1126463bded
ms.date: 05/10/2018
ms.keywords: D3D10DDIARG_CALCPRIVATEDEVICESIZE, D3D10DDIARG_CALCPRIVATEDEVICESIZE structure [Display Devices], UMDisplayDriver_Dx10param_Structs_5d15afa8-1d91-4823-ba91-391e64e9374d.xml, d3d10umddi/D3D10DDIARG_CALCPRIVATEDEVICESIZE, display.d3d10ddiarg_calcprivatedevicesize
ms.topic: struct
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
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
- d3d10umddi.h
api_name:
- D3D10DDIARG_CALCPRIVATEDEVICESIZE
product:
- Windows
targetos: Windows
tech.root: display
req.typenames: D3D10DDIARG_CALCPRIVATEDEVICESIZE
---

# D3D10DDIARG_CALCPRIVATEDEVICESIZE structure


## -description


The D3D10DDIARG_CALCPRIVATEDEVICESIZE structure describes the parameters that the user-mode display driver uses to calculate the size of a memory block that the driver requires to store frequently-accessed data.


## -struct-fields




### -field Interface

[in] The Microsoft Direct3D interface version. The high 16 bits store the major release number (such as 10, 11, and so on); the low 16 bits store the minor release number (such as 0, 1, 2, and so on). The minor release number will be increased when a change to the interface is released.


### -field Version

[in] A number that the driver can use to identify when the Direct3D runtime was built. The high 16 bits represent the build number; the low 16 bits represent the revision number. 

The driver is required only to monitor the high 16 bits. The driver should ensure that the runtime build version that is passed in is greater than or equal to the current build version of the driver. The driver should return a failure from its <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/d3d10umddi/nc-d3d10umddi-pfnd3d10ddi_calcprivatedevicesize">CalcPrivateDeviceSize</a> function if the passed in build version is incompatible. 


### -field Flags

[in] A valid bitwise OR of flag values that identify how to create a rendering device. The Direct3D runtime supports the following flags:  





#### D3D10DDI_CREATEDEVICE_FLAG_DISABLE_EXTRA_THREAD_CREATION (0x1)

If this flag is set, the user-mode display driver should not run multiple threads simultaneously when it processes calls to its functions from the Direct3D runtime. A driver can typically start and run multiple threads to process operations faster, unless the D3D10DDI_CREATEDEVICE_FLAG_DISABLE_EXTRA_THREAD_CREATION flag is set.



#### D3D11DDI_CREATEDEVICE_FLAG_SINGLETHREADED (0x10)

Supported in Windows 7 and later versions. 

This flag informs the user-mode display driver that the application is single threaded. The Direct3D version 11 runtime allows multiple application threads to enter the driver if the driver allows this mode of operation. However, not all applications can run multiple threads. If this flag is set, the driver does not expect multiple threads to enter it and run simultaneously. The driver can avoid synchronization if this flag is set.



#### The flag that is set in the 0xE mask of the Flags member

Supported in Windows 7 and later versions. 

This flag represents the level of 3-D pipeline that the driver should support for the display device. The driver uses the following constant and macros to extract one of the values from the <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/d3d10umddi/ne-d3d10umddi-d3d11ddi_3dpipelinelevel">D3D11DDI_3DPIPELINELEVEL</a> enumeration that represent the 3-D pipeline level to support. The value in the <b>Flags</b> member is formatted like the <b>Caps</b> member of the <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/d3d10umddi/ns-d3d10umddi-d3d11ddi_3dpipelinesupport_caps">D3D11DDI_3DPIPELINESUPPORT_CAPS</a> structure.

```cpp
#define D3D11DDI_CREATEDEVICE_FLAG_3DPIPELINESUPPORT_SHIFT (0x1)
#define D3D11DDI_CREATEDEVICE_FLAG_3DPIPELINESUPPORT_MASK (0x7 << D3D11DDI_CREATEDEVICE_FLAG_3DPIPELINESUPPORT_SHIFT)
#define D3D11DDI_EXTRACT_3DPIPELINELEVEL_FROM_FLAGS( Flags ) \
    ((D3D11DDI_3DPIPELINELEVEL)(((Flags) & D3D11DDI_CREATEDEVICE_FLAG_3DPIPELINESUPPORT_MASK) >> \
    D3D11DDI_CREATEDEVICE_FLAG_3DPIPELINESUPPORT_SHIFT))
```

## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/d3d10umddi/nc-d3d10umddi-pfnd3d10ddi_calcprivatedevicesize">CalcPrivateDeviceSize</a>
 

 

