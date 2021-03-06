---
UID: NS:bdamedia._KSM_BDA_PIN
title: "_KSM_BDA_PIN"
author: windows-driver-content
description: The KSM_BDA_PIN structure describes a method request to create or delete a pin factory for a filter.
old-location: stream\ksm_bda_pin.htm
old-project: stream
ms.assetid: 7e7778ba-cf4f-44e8-91ce-c53458d3db9a
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: "*PKSM_BDA_PIN, KSM_BDA_PIN, KSM_BDA_PIN structure [Streaming Media Devices], PKSM_BDA_PIN, PKSM_BDA_PIN structure pointer [Streaming Media Devices], _KSM_BDA_PIN, bdamedia/KSM_BDA_PIN, bdamedia/PKSM_BDA_PIN, bdaref_190ab329-704e-472a-926c-1aa04d4b6df5.xml, stream.ksm_bda_pin"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdamedia.h
req.include-header: Bdamedia.h
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
-	bdamedia.h
api_name:
-	KSM_BDA_PIN
product: Windows
targetos: Windows
req.typenames: KSM_BDA_PIN, *PKSM_BDA_PIN
---

# _KSM_BDA_PIN structure


## -description


The KSM_BDA_PIN structure describes a method request to create or delete a pin factory for a filter. 


## -syntax


````
typedef struct _KSM_BDA_PIN {
  KSMETHOD Method;
  union {
    ULONG PinId;
    ULONG PinType;
  };
  ULONG    Reserved;
} KSM_BDA_PIN, *PKSM_BDA_PIN;
````


## -struct-fields




### -field Method

KSMETHOD structure that describes a method and request type of a method request.


### -field Reserved

Reserved.


#### - PinId

Member of the union in KSM_BDA_PIN that contains the identifier (ID) of a pin factory of a filter.


#### - PinType

Member of the union in KSM_BDA_PIN that contains the value that specifies the pin type.


## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff563398">KSMETHOD</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KSM_BDA_PIN structure%20 RELEASE:%20(2/23/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

