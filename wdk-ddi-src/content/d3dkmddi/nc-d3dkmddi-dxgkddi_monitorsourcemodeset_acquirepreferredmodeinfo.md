---
UID: NC:d3dkmddi.DXGKDDI_MONITORSOURCEMODESET_ACQUIREPREFERREDMODEINFO
title: DXGKDDI_MONITORSOURCEMODESET_ACQUIREPREFERREDMODEINFO
author: windows-driver-content
description: The pfnAcquirePreferredModeInfo returns a descriptor of the preferred mode in a specified monitor source mode set object.
old-location: display\dxgk_monitorsourcemodeset_interface_pfnacquirepreferredmodeinfo.htm
old-project: display
ms.assetid: 80d3d199-42ad-4f21-8122-05dfad37016d
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DXGKDDI_MONITORSOURCEMODESET_ACQUIREPREFERREDMODEINFO, VidPnFunctions_c7c55840-18b7-40ad-8cf9-5350c7723246.xml, d3dkmddi/pfnAcquirePreferredModeInfo, display.dxgk_monitorsourcemodeset_interface_pfnacquirepreferredmodeinfo, pfnAcquirePreferredModeInfo, pfnAcquirePreferredModeInfo callback function [Display Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	d3dkmddi.h
api_name:
-	pfnAcquirePreferredModeInfo
product: Windows
targetos: Windows
req.typenames: DD_MULTISAMPLEQUALITYLEVELSDATA
---

# DXGKDDI_MONITORSOURCEMODESET_ACQUIREPREFERREDMODEINFO callback


## -description


The <b>pfnAcquirePreferredModeInfo</b> returns a descriptor of the preferred mode in a specified monitor source mode set object.


## -prototype


````
DXGKDDI_MONITORSOURCEMODESET_ACQUIREPREFERREDMODEINFO pfnAcquirePreferredModeInfo;

NTSTATUS APIENTRY pfnAcquirePreferredModeInfo(
  _In_  const D3DKMDT_HMONITORSOURCEMODESET hMonitorSourceModeSet,
  _Out_ const D3DKMDT_MONITOR_SOURCE_MODE   **ppFirstMonitorSourceModeInfo
)
{ ... }
````


## -parameters




### -param hMonitorSourceModeSet [in]

[in] A handle to a monitor source mode set object. The display miniport driver previously obtained this handle by calling the <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_monitor_acquiremonitorsourcemodeset.md">pfnAcquireMonitorSourceModeSet</a> function of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568433">Monitor interface</a>.


### -param ppFirstMonitorSourceModeInfo [out]

[out] A pointer to a variable that receives a pointer to a <a href="..\d3dkmdt\ns-d3dkmdt-_d3dkmdt_monitor_source_mode.md">D3DKMDT_MONITOR_SOURCE_MODE</a> structure. The structure contains a variety of information about the preferred monitor source mode, including its ID and video signal.


## -returns



The <b>pfnAcquirePreferredModeInfo</b> function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function successfully returned a descriptor of the preferred mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATIS_GRAPHICS_NO_PREFERRED_MODE</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded, but the specified monitor source mode set does not have a preferred mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_GRAPHICS_INVALID_MONITOR_SOURCEMODESET</b></dt>
</dl>
</td>
<td width="60%">
The handle supplied in <i>hMonitorSourceModeSet</i> was invalid.

</td>
</tr>
</table>
 




## -remarks



When you have finished using the <a href="..\d3dkmdt\ns-d3dkmdt-_d3dkmdt_monitor_source_mode.md">D3DKMDT_MONITOR_SOURCE_MODE</a> structure, you must release the structure by calling <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_monitorsourcemodeset_releasemodeinfo.md">pfnReleaseModeInfo</a>.

The D3DKMDT_HMONITORSOURCEMODESET data type is defined in <i>D3dkmdt.h</i>. 



