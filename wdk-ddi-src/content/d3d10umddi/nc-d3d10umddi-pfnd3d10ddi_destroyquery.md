---
UID: NC:d3d10umddi.PFND3D10DDI_DESTROYQUERY
title: PFND3D10DDI_DESTROYQUERY
author: windows-driver-content
description: The DestroyQuery(D3D10) function destroys the specified query object. The query object can be destoyed only if it is not currently bound to a display device.
old-location: display\destroyquery_d3d10_.htm
old-project: display
ms.assetid: 74bb85df-6d64-49e8-b431-2f4a9954eff2
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DestroyQuery, DestroyQuery callback function [Display Devices], PFND3D10DDI_DESTROYQUERY, UserModeDisplayDriverDx10_Functions_9c0fdf87-a47b-45b5-9ec9-5c307d412c9c.xml, d3d10umddi/DestroyQuery, display.destroyquery_d3d10_
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
-	DestroyQuery
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D10DDI_DESTROYQUERY callback


## -description


The <b>DestroyQuery(D3D10)</b> function destroys the specified query object. The query object can be destoyed only if it is not currently bound to a display device. 


## -prototype


````
PFND3D10DDI_DESTROYQUERY DestroyQuery;

VOID APIENTRY DestroyQuery(
  _In_ D3D10DDI_HDEVICE hDevice,
  _In_ D3D10DDI_HQUERY  hQuery
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param D3D10DDI_HQUERY








#### - hDevice [in]

 A handle to the display device (graphics context).


#### - hQuery [in]

 A handle to the driver's private data for the query object to destroy. The Microsoft Direct3D runtime will free the memory region that it previously allocated for the object. Therefore, the driver can no longer access this memory region. 


## -returns



None

The driver can use the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> callback function to set an error code. For more information about setting error codes, see the following Remarks section.




## -remarks



The driver should not encounter any error, except for D3DDDIERR_DEVICEREMOVED. Therefore, if the driver passes any error, except for D3DDDIERR_DEVICEREMOVED, in a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> function, the Direct3D runtime will determine that the error is critical. Even if the device was removed, the driver is not required to return D3DDDIERR_DEVICEREMOVED; however, if device removal interfered with the operation of <b>DestroyQuery(D3D10)</b> (which typically should not happen), the driver can return D3DDDIERR_DEVICEREMOVED.




## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddi_devicefuncs.md">D3D10DDI_DEVICEFUNCS</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3D10DDI_DESTROYQUERY callback function%20 RELEASE:%20(2/26/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

