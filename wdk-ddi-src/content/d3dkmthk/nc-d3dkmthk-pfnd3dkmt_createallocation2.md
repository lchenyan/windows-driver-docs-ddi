---
UID: NC:d3dkmthk.PFND3DKMT_CREATEALLOCATION2
title: PFND3DKMT_CREATEALLOCATION2
author: windows-driver-content
description: Reserved for system use. Do not use in your driver.
old-location: display\d3dkmtcreateallocation2.htm
old-project: display
ms.assetid: 416DE730-44A6-4BA3-BFC2-C11A179AD422
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: D3DKMTCreateAllocation2, D3DKMTCreateAllocation2 callback function [Display Devices], PFND3DKMT_CREATEALLOCATION2, d3dkmthk/D3DKMTCreateAllocation2, display.d3dkmtcreateallocation2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 7 and later versions of the Windows operating systems.
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
-	d3dkmthk.h
api_name:
-	D3DKMTCreateAllocation2
product: Windows
targetos: Windows
req.typenames: DXGK_TARGETMODE_DETAIL_TIMING
---

# PFND3DKMT_CREATEALLOCATION2 callback


## -description


Reserved for system use. Do not use in your driver.


## -prototype


````
NTSTATUS APIENTRY D3DKMTCreateAllocation2(
  _Inout_ D3DKMT_CREATEALLOCATION *pData
);
````


## -parameters




### -param *








#### - pData [in, out]

