---
UID: NS:ks.KSP_TIMEFORMAT
title: KSP_TIMEFORMAT
author: windows-driver-content
description: The KSP_TIMEFORMAT structure corresponds to KSPROPERTY_MEDIASEEKING_CONVERTTIMEFORMAT.
old-location: stream\ksp_timeformat.htm
old-project: stream
ms.assetid: 18ce5fc5-927c-4261-8966-bb12849b95c9
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: "*PKSP_TIMEFORMAT, KSP_TIMEFORMAT, KSP_TIMEFORMAT structure [Streaming Media Devices], PKSP_TIMEFORMAT, PKSP_TIMEFORMAT structure pointer [Streaming Media Devices], ks-struct_086a975b-f249-44e9-b1fa-4a945509722e.xml, ks/KSP_TIMEFORMAT, ks/PKSP_TIMEFORMAT, stream.ksp_timeformat"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ks.h
req.include-header: Ks.h
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
-	ks.h
api_name:
-	KSP_TIMEFORMAT
product: Windows
targetos: Windows
req.typenames: KSP_TIMEFORMAT, *PKSP_TIMEFORMAT
---

# KSP_TIMEFORMAT structure


## -description


The KSP_TIMEFORMAT structure corresponds to <a href="https://msdn.microsoft.com/library/windows/hardware/ff565181">KSPROPERTY_MEDIASEEKING_CONVERTTIMEFORMAT</a>.


## -syntax


````
typedef struct {
  KSPROPERTY Property;
  GUID       SourceFormat;
  GUID       TargetFormat;
  LONGLONG   Time;
} KSP_TIMEFORMAT, *PKSP_TIMEFORMAT;
````


## -struct-fields




### -field Property

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564262">KSPROPERTY</a> structure.


### -field SourceFormat

Pointer to a GUID that specifies the format to convert. If <b>NULL</b>, the current format is used.


### -field TargetFormat

Pointer to a GUID that specifies the target format. If <b>NULL</b>, the current format is used.


### -field Time

Specifies the time value to convert.


## -remarks



The fields of the structure correspond one to one with DirectShow's IMediaSeeking::ConvertTimeFormat.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff565181">KSPROPERTY_MEDIASEEKING_CONVERTTIMEFORMAT</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KSP_TIMEFORMAT structure%20 RELEASE:%20(2/23/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

