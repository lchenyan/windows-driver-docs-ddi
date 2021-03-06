---
UID: NS:ksmedia.tagKS_DATARANGE_IMAGE
title: tagKS_DATARANGE_IMAGE
author: windows-driver-content
description: Specifies an image data range that is used in the KSPIN_DESCRIPTOR structure that describes a pin (or stream).
old-location: stream\ks_datarange_image.htm
old-project: stream
ms.assetid: 81ad341a-5f68-43aa-98ea-193780a7c5b2
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: "*PKS_DATARANGE_IMAGE, KS_DATARANGE_IMAGE, KS_DATARANGE_IMAGE structure [Streaming Media Devices], PKS_DATARANGE_IMAGE, PKS_DATARANGE_IMAGE structure pointer [Streaming Media Devices], ksmedia/KS_DATARANGE_IMAGE, ksmedia/PKS_DATARANGE_IMAGE, stream.ks_datarange_image, tagKS_DATARANGE_IMAGE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ksmedia.h
req.include-header: Ksmedia.h
req.target-type: Windows
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
-	HeaderDef
api_location:
-	Ksmedia.h
api_name:
-	KS_DATARANGE_IMAGE
product: Windows
targetos: Windows
req.typenames: KS_DATARANGE_IMAGE, *PKS_DATARANGE_IMAGE
---

# tagKS_DATARANGE_IMAGE structure


## -description


Specifies an image data range that is used in the <a href="..\ks\ns-ks-kspin_descriptor.md">KSPIN_DESCRIPTOR</a> structure that describes a pin (or stream).


## -syntax


````
typedef struct tagKS_DATARANGE_IMAGE {
  KSDATARANGE                 DataRange;
  KS_VIDEO_STREAM_CONFIG_CAPS ConfigCaps;
  KS_BITMAPINFOHEADER         ImageInfoHeader;
} KS_DATARANGE_IMAGE, *PKS_DATARANGE_IMAGE;
````


## -struct-fields




### -field DataRange

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff561658">KSDATARANGE</a> structure that specifies the data range supported by this pin type.


### -field ConfigCaps

A <a href="..\ksmedia\ns-ksmedia-_ks_video_stream_config_caps.md">KS_VIDEO_STREAM_CONFIG_CAPS</a> structure that specifies the configuration of the stream, including scaling, cropping, and frame and data rates.


### -field ImageInfoHeader

A <a href="..\ksmedia\ns-ksmedia-tagks_bitmapinfoheader.md">KS_BITMAPINFOHEADER</a> structure that specifies image color and dimension information that the still image capture stream would provide.


## -see-also

<a href="..\ks\ns-ks-kspin_descriptor.md">KSPIN_DESCRIPTOR</a>



<a href="..\ksmedia\ns-ksmedia-_ks_video_stream_config_caps.md">KS_VIDEO_STREAM_CONFIG_CAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561658">KSDATARANGE</a>



<a href="..\ksmedia\ns-ksmedia-tagks_bitmapinfoheader.md">KS_BITMAPINFOHEADER</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KS_DATARANGE_IMAGE structure%20 RELEASE:%20(2/23/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

