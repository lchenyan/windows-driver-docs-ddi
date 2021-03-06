---
UID: NS:hidpi._HIDP_EXTENDED_ATTRIBUTES
title: "_HIDP_EXTENDED_ATTRIBUTES"
author: windows-driver-content
description: The HIDP_EXTENDED_ATTRIBUTES structure contains information about the global items specified for a HID control that the HID parser did not recognize.
old-location: hid\hidp_extended_attributes.htm
old-project: hid
ms.assetid: 03be8b22-2108-4a13-be1e-642373095ab5
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: "*PHIDP_EXTENDED_ATTRIBUTES, HIDP_EXTENDED_ATTRIBUTES, HIDP_EXTENDED_ATTRIBUTES structure [Human Input Devices], PHIDP_EXTENDED_ATTRIBUTES, PHIDP_EXTENDED_ATTRIBUTES structure pointer [Human Input Devices], _HIDP_EXTENDED_ATTRIBUTES, hid.hidp_extended_attributes, hidpi/HIDP_EXTENDED_ATTRIBUTES, hidpi/PHIDP_EXTENDED_ATTRIBUTES, hidstrct_7f0e134c-f292-4558-b805-02861407032f.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: hidpi.h
req.include-header: Hidpi.h
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	hidpi.h
api_name:
-	HIDP_EXTENDED_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: HIDP_EXTENDED_ATTRIBUTES, *PHIDP_EXTENDED_ATTRIBUTES
---

# _HIDP_EXTENDED_ATTRIBUTES structure


## -description


The HIDP_EXTENDED_ATTRIBUTES structure contains information about the global items specified for a HID control that the HID parser did not recognize.


## -syntax


````
typedef struct _HIDP_EXTENDED_ATTRIBUTES {
  UCHAR               NumGlobalUnknowns;
  UCHAR               Reserved[3];
  PHIDP_UNKNOWN_TOKEN GlobalUnknowns;
  ULONG               Data[1];
} HIDP_EXTENDED_ATTRIBUTES, *PHIDP_EXTENDED_ATTRIBUTES;
````


## -struct-fields




### -field NumGlobalUnknowns

Specifies the number of <a href="..\hidpi\ns-hidpi-_hidp_unknown_token.md">HIDP_UNKNOWN_TOKEN</a> structures in the list specified by <b>Data</b>.


### -field Reserved

Reserved for internal system use only.


### -field GlobalUnknowns

Reserved for internal system use only.


### -field Data

Specifies the memory location where <a href="..\hidpi\nf-hidpi-hidp_getextendedattributes.md">HidP_GetExtendedAttributes</a> returns a variable length array of <a href="..\hidpi\ns-hidpi-_hidp_unknown_token.md">HIDP_UNKNOWN_TOKEN</a> structures.


## -remarks



The HIDP_EXTENDED_ATTRIBUTES structure is designed to be used with <b>HidP_GetExtendedAttributes</b>.




## -see-also

<a href="..\hidpi\ns-hidpi-_hidp_unknown_token.md">HIDP_UNKNOWN_TOKEN</a>



<a href="..\hidpi\nf-hidpi-hidp_getextendedattributes.md">HidP_GetExtendedAttributes</a>



 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [hid\hid]:%20HIDP_EXTENDED_ATTRIBUTES structure%20 RELEASE:%20(2/24/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

