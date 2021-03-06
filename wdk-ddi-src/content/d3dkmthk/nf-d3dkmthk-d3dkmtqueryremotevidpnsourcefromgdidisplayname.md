---
UID: NF:d3dkmthk.D3DKMTQueryRemoteVidPnSourceFromGdiDisplayName
title: D3DKMTQueryRemoteVidPnSourceFromGdiDisplayName function
author: windows-driver-content
description: Maps a GDI display name to a remote video present network (VidPN) source ID that is needed for a call to the D3DKMTOutputDuplPresent function.
old-location: display\d3dkmtqueryremotevidpnsourcefromgdidisplayname.htm
old-project: display
ms.assetid: 3606d5f4-760f-4ba1-84ea-218b6c2a2e20
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: D3DKMTQueryRemoteVidPnSourceFromGdiDisplayName, D3DKMTQueryRemoteVidPnSourceFromGdiDisplayName callback function [Display Devices], PFND3DKMT_QUERYREMOTEVIDPNSOURCEFROMGDIDISPLAYNAME, d3dkmthk/D3DKMTQueryRemoteVidPnSourceFromGdiDisplayName, display.d3dkmtqueryremotevidpnsourcefromgdidisplayname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Universal
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
-	D3dkmthk.h
api_name:
-	D3DKMTQueryRemoteVidPnSourceFromGdiDisplayName
product: Windows
targetos: Windows
req.typenames: D3DKMT_DRIVERVERSION
---

# D3DKMTQueryRemoteVidPnSourceFromGdiDisplayName function


## -description


Maps a GDI display name to a remote video present network (VidPN) source ID that is needed for a call to the <a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtoutputduplpresent.md">D3DKMTOutputDuplPresent</a> function.


## -syntax


````
EXTERN_C _Check_return_ NTSTATUS APIENTRY D3DKMTQueryRemoteVidPnSourceFromGdiDisplayName(
  _Inout_ D3DKMT_QUERYREMOTEVIDPNSOURCEFROMGDIDISPLAYNAME *pData
);
````


## -parameters






#### - pData [in, out]

A pointer to a <a href="..\d3dkmthk\ns-d3dkmthk-_d3dkmt_queryremotevidpnsourcefromgdidisplayname.md">D3DKMT_QUERYREMOTEVIDPNSOURCEFROMGDIDISPLAYNAME</a> structure that describes information that is required to perform the mapping.


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
The mapping was performed successfully.

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
 

This function might also return other NTSTATUS values.




## -see-also

<a href="..\d3dkmthk\ns-d3dkmthk-_d3dkmt_queryremotevidpnsourcefromgdidisplayname.md">D3DKMT_QUERYREMOTEVIDPNSOURCEFROMGDIDISPLAYNAME</a>



<a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtoutputduplpresent.md">D3DKMTOutputDuplPresent</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3DKMT_QUERYREMOTEVIDPNSOURCEFROMGDIDISPLAYNAME callback function%20 RELEASE:%20(2/26/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

