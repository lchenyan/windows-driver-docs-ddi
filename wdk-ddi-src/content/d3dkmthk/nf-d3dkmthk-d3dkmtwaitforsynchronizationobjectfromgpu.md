---
UID: NF:d3dkmthk.D3DKMTWaitForSynchronizationObjectFromGpu
title: D3DKMTWaitForSynchronizationObjectFromGpu function
author: windows-driver-content
description: D3DKMTWaitForSynchronizationObjectFromGpu waits for a monitored fence to reach a certain value before processing subsequent context commands.
old-location: display\d3dkmtwaitforsynchronizationobjectfromgpu.htm
old-project: display
ms.assetid: 93705446-8B87-46DD-9CFE-DD0473DEE6B6
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: D3DKMTWaitForSynchronizationObjectFromGpu, D3DKMTWaitForSynchronizationObjectFromGpu function [Display Devices], d3dkmthk/D3DKMTWaitForSynchronizationObjectFromGpu, display.d3dkmtwaitforsynchronizationobjectfromgpu
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Universal
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
req.lib: GDI32.lib
req.dll: GDI32.dll
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	GDI32.dll
-	API-MS-Win-DX-D3DKMT-L1-1-1.dll
-	GDI32.dll
-	API-MS-Win-DX-D3DKMT-L1-1-2.dll
api_name:
-	D3DKMTWaitForSynchronizationObjectFromGpu
product: Windows
targetos: Windows
req.typenames: D3DKMT_DRIVERVERSION
---

# D3DKMTWaitForSynchronizationObjectFromGpu function


## -description


<b>D3DKMTWaitForSynchronizationObjectFromGpu</b> waits for a monitored fence to reach a certain value before processing subsequent context commands.
<div class="alert"><b>Note</b>  For Windows Display Driver Model (WDDM) v2 drivers, existing <a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtwaitforsynchronizationobject.md">D3DKMTWaitForSynchronizationObject</a> and <a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtwaitforsynchronizationobject2.md">D3DKMTWaitForSynchronizationObject2</a> callbacks are deprecated and will eventually be removed. </div><div> </div>

## -syntax


````
EXTERN_C _Check_return_ NTSTATUS APIENTRY D3DKMTWaitForSynchronizationObjectFromGpu(
  _In_ const D3DKMT_WAITFORSYNCHRONIZATIONOBJECTFROMGPU *pData
);
````


## -parameters




### -param D3DKMT_WAITFORSYNCHRONIZATIONOBJECTFROMGPU

TBD




#### - pData [in]

A pointer to a <a href="..\d3dkmthk\ns-d3dkmthk-_d3dkmt_waitforsynchronizationobjectfromgpu.md">D3DKMT_WAITFORSYNCHRONIZATIONOBJECTFROMGPU</a> structure that describes the operation.


## -returns



Returns one of the following values:

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
The operation was performed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER </b></dt>
</dl>
</td>
<td width="60%">

         Parameters were validated and determined to be incorrect.

</td>
</tr>
</table>
 

This function might also return other <b>NTSTATUS</b> values.




## -remarks



This function semantics are similar to existing <a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtwaitforsynchronizationobject2.md">D3DKMTWaitForSynchronizationObject2</a> call, except that this function also supports monitored fence objects and an array of monitored fence values to wait for.




## -see-also

<a href="..\d3dkmthk\ns-d3dkmthk-_d3dkmt_waitforsynchronizationobjectfromgpu.md">D3DKMT_WAITFORSYNCHRONIZATIONOBJECTFROMGPU</a>



<a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtwaitforsynchronizationobject.md">D3DKMTWaitForSynchronizationObject</a>



<a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtwaitforsynchronizationobject2.md">D3DKMTWaitForSynchronizationObject2</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3DKMTWaitForSynchronizationObjectFromGpu function%20 RELEASE:%20(2/26/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

