---
UID: NC:d3d10umddi.PFND3D10DDI_CREATESAMPLER
title: PFND3D10DDI_CREATESAMPLER
author: windows-driver-content
description: The CreateSampler function creates a sampler.
old-location: display\createsampler.htm
old-project: display
ms.assetid: 603bb033-390b-4965-b6ea-6acc2c7a8fcf
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CreateSampler, CreateSampler callback function [Display Devices], PFND3D10DDI_CREATESAMPLER, UserModeDisplayDriverDx10_Functions_16c89dca-e337-42c7-a666-f0f4c9a6d3e3.xml, d3d10umddi/CreateSampler, display.createsampler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
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
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	d3d10umddi.h
api_name:
-	CreateSampler
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D10DDI_CREATESAMPLER callback


## -description


The <b>CreateSampler</b> function creates a sampler.


## -prototype


````
PFND3D10DDI_CREATESAMPLER CreateSampler;

VOID APIENTRY CreateSampler(
  _In_       D3D10DDI_HDEVICE       hDevice,
  _In_ const D3D10_DDI_SAMPLER_DESC *pSamplerDesc,
  _In_       D3D10DDI_HSAMPLER      hSampler,
  _In_       D3D10DDI_HRTSAMPLER    hRTSampler
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param *


### -param D3D10DDI_HSAMPLER


### -param D3D10DDI_HRTSAMPLER








#### - hDevice [in]

 A handle to the display device (graphics context).


#### - hRTSampler [in]

 A handle to the sampler that the driver should use anytime it calls back into the Direct3D runtime. 


#### - hSampler [in]

 A handle to the driver's private data for the sampler. The driver returns the size, in bytes, of the memory region that the Microsoft Direct3D runtime must allocate for the private data from a call to the driver's <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_calcprivatesamplersize.md">CalcPrivateSamplerSize</a> function. The handle is really just a pointer to a region of memory, the size of which the driver requested. The driver uses this region of memory to store internal data structures that are related to its sampler object.


#### - pSamplerDesc [in]

 A pointer to a <a href="..\d3d10umddi\ns-d3d10umddi-d3d10_ddi_sampler_desc.md">D3D10_DDI_SAMPLER_DESC</a> structure that describes the parameters that the user-mode display driver uses to create a sampler. 


## -returns



None

The driver can use the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> callback function to set an error code. For more information about setting error codes, see the following Remarks section.




## -remarks



The driver can pass E_OUTOFMEMORY (if the driver runs out of memory) or D3DDDIERR_DEVICEREMOVED (if the device has been removed) in a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> function. The Direct3D runtime will determine that any other errors are critical. If the driver passes any errors, including D3DDDIERR_DEVICEREMOVED, the Direct3D runtime will determine that the handle is invalid; therefore, the runtime will not call the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_destroysampler.md">DestroySampler</a> function to destroy the handle that the <i>hSampler</i> parameter specifies.

The user-mode display driver is not required to create more than 4,096 unique instances of sampler objects on a device at a time. 




## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d10_ddi_sampler_desc.md">D3D10_DDI_SAMPLER_DESC</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_calcprivatesamplersize.md">CalcPrivateSamplerSize</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_destroysampler.md">DestroySampler</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddi_devicefuncs.md">D3D10DDI_DEVICEFUNCS</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3D10DDI_CREATESAMPLER callback function%20 RELEASE:%20(2/26/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

