---
UID: NS:avcstrm.tagKS_DATARANGE_DV_AVC
title: tagKS_DATARANGE_DV_AVC
author: windows-driver-content
description: The KS_DATARANGE_DV_AVC structure stores a range of AV/C digital video formats.
old-location: stream\ks_datarange_dv_avc.htm
old-project: stream
ms.assetid: 92759ba0-79f1-4dec-aea5-62c24253c6f0
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: "*PKS_DATARANGE_DV_AVC, KS_DATARANGE_DV_AVC, KS_DATARANGE_DV_AVC structure [Streaming Media Devices], PKS_DATARANGE_DV_AVC, PKS_DATARANGE_DV_AVC structure pointer [Streaming Media Devices], avcsref_e5ebf0ed-91f2-415a-a6b1-346cfebf16b5.xml, avcstrm/KS_DATARANGE_DV_AVC, avcstrm/PKS_DATARANGE_DV_AVC, stream.ks_datarange_dv_avc, tagKS_DATARANGE_DV_AVC"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: avcstrm.h
req.include-header: Avcstrm.h
req.target-type: Windows
req.target-min-winverclnt: 
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
-	HeaderDef
api_location:
-	avcstrm.h
api_name:
-	KS_DATARANGE_DV_AVC
product: Windows
targetos: Windows
req.typenames: KS_DATARANGE_DV_AVC, *PKS_DATARANGE_DV_AVC
---

# tagKS_DATARANGE_DV_AVC structure


## -description


The KS_DATARANGE_DV_AVC structure stores a range of AV/C digital video formats.


## -syntax


````
typedef struct tagKS_DATARANGE_DV_AVC {
  KSDATARANGE       DataRange;
  DVINFO            DVVideoInfo;
  AVCPRECONNECTINFO ConnectInfo;
} KS_DATARANGE_DV_AVC, *PKS_DATARANGE_DV_AVC;
````


## -struct-fields




### -field DataRange

Specifies the range of supported AV/C digital video formats.


### -field DVVideoInfo

Specifies the digital video information, for example, sound tracks and video information.


### -field ConnectInfo

Specifies the AV/C preconnection info.


## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff561658">KSDATARANGE</a>



<a href="..\avcstrm\ns-avcstrm-_dvinfo.md">DVINFO</a>



<a href="..\avc\ns-avc-_avcpreconnectinfo.md">AVCPRECONNECTINFO</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KS_DATARANGE_DV_AVC structure%20 RELEASE:%20(2/23/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

